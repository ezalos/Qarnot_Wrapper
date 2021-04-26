# Qarnot Wrapper

Python interface for using Qarnot computing resources

## Installation

```sh
cp config.py.template config.py
```
You then need to modify `config.py` by replacing the string `"YOUR TOKEN"` by your actual Token from Qarnot.

This token can be found under this link https://account.qarnot.com/compute once you have created an acocunt (15 euros given at account creation)


## Usage example

	- Will execute `echo HelloWorld` in the docker `ezalos/qarnot_1stdqn:2.00` from docker.hub as a task named `First_Task`

```sh
python3 main.py -c "echo HelloWorld" -o "ezalos/qarnot_1stdqn:2.00" -n First_Task
```

	- Will execute `python3 main.py` with files recursively uploaded from `my_dir` in an input bucket. Carefull: uploaded files will all be put in current directory, regardless of how they were arranged in `my_dir`

```sh
python3 main.py -c "python3 main.py" -d my_dir -n Second_Task
```

