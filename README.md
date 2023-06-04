# Using Deep Reinforcement Learning to Play Super Mario Bros.

This project utilizes (Double/Dueling) Deep-Q Networks to play Super Mario Bros. The goal is to develop an AI agent that can learn and improve its performance in playing the game.

![DDQN-SMB-1-4](https://user-images.githubusercontent.com/2184469/113493396-8e6d3080-94a4-11eb-8e4c-956c277ac76f.gif)

## Installation

### `virtualenv`

To create an isolated Python environment for this project using `virtualenv`, follow these steps:

#### Setup

```shell
virtualenv -p python3 .env
source .env/bin/activate
```

To deactivate the environment when you're finished:

```shell
deactivate
```

### Dependencies

The required Python dependencies, along with their frozen versions, are listed in the [requirements.txt](requirements.txt) file. To install these dependencies, use the following command:

```shell
python -m pip install -r requirements.txt
```

**NOTE:** If you are not using `virtualenv`, make sure that `python` is aliased to `python3`, as `python2` is not supported.

## Usage

The instructions below assume you have a shell open at the top-level directory of the project. For comprehensive documentation on command-line options, execute the following command:

```shell
python . -h
```

### Test Cases

To run the `unittest` suite for the project, use the following command:

```shell
python -m unittest discover .
```

### Random Agent

You can play games with an agent that makes random decisions using the following command:

```shell
python . -m random -e <environment ID>
```

- `<environment ID>` represents the ID of the environment for random gameplay.

#### Example

For example, to play with a random agent in the Pong environment, run:

```shell
python . -m random -e Pong-v0
```

### Training a Deep-Q Agent

To train a Deep-Q agent to play a game, execute the following command:

```shell
python . -m train -e <environment ID>
```

- `<environment ID>` corresponds to the ID of the environment to train the agent on.

#### Example

For instance, to train a Deep-Q agent on the Pong game, use the following command:

```shell
python . -m train -e Pong-v0
```

### Playing With a Trained Agent

To run a trained Deep-Q agent on validation games, use this command:

```shell
python . -m play -o <results directory>
```

- `<results directory>` should be a directory containing a `weights.h5` file from a previous training session.

#### Example

For example, to play with a Deep-Q agent on the Pong game, execute:

```shell
python . -m play -e results/Pong-v0/DeepQAgent/2018-06-07_09-24
```

I have taken inspiration from the original author for personal and educational purposes.s