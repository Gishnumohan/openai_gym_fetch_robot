## Requirements
- python3
- openai-gym 
- mujoco200 (follow mujoco installation process to get license and install) 
- mujoco-py=1.50.1.56 
- pytorch
- mpi4py

## Instruction to run the code

1. train the **FetchReach-v1**:
"mpirun -np 1 python -u train_model.py --env-name='FetchReach-v1' --n-cycles=10 2>&1 | tee reach.log"

2. train the **FetchPush-v1**:
"mpirun -np 8 python -u train_model.py --env-name='FetchPush-v1' 2>&1 | tee push.log"
3. train the **FetchPickAndPlace-v1**:
"mpirun -np 16 python -u train_model.py --env-name='FetchPickAndPlace-v1' 2>&1 | tee pick.log"
4. train the **FetchSlide-v1**:
"mpirun -np 8 python -u train_model.py --env-name='FetchSlide-v1' --n-epochs=200 2>&1 | tee slide.log"

### Run fetch robot model
```bash
python run.py --env-name=<environment name>
```

## Acknowledgement:
- [Openai Baselines](https://github.com/openai/baselines)
