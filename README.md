# BU Advanced NLP Homework 1: Transformer Language Modeling from Scratch

This assignment is adapted from the Spring 2026 edition of Stanford CS336 ([original repository](https://github.com/stanford-cs336/)). All credit for its development goes to the Stanford course staff. This README and all of the following code are adapted from theirs. **If you are enrolled in this course at BU and have any questions about this assignment, email Aaron Mueller; do not email the Stanford course staff.**

For a full description of the assignment, see the assignment handout at 
[hw1.pdf](https://aaronmueller.github.io/teaching/cs599b1_fall26/homeworks/hw1/CS599_HW1_Instructions.pdf).

## Setup

### Environment
We will be using `uv` to manage Python packages. `uv` is a package managing system that is designed to ensure reproducibility, portability, and ease of use. Install `uv` [here](https://github.com/astral-sh/uv) (recommended), or run `pip install uv`/`brew install uv` in your terminal. We recommend reading a bit about managing projects in `uv` [here](https://docs.astral.sh/uv/guides/projects/#managing-dependencies).

You can now run any code in the repo using
```sh
uv run <python_file_path>
```
and the environment will be automatically solved and activated when necessary.

### Run unit tests


```sh
uv run pytest
```

Initially, all tests should fail with `NotImplementedError`s.
To connect your implementation to the tests, complete the
functions in [./tests/adapters.py](./tests/adapters.py).

### Download data
Download the TinyStories data:

``` sh
mkdir -p data
cd data

wget https://huggingface.co/datasets/roneneldan/TinyStories/resolve/main/TinyStoriesV2-GPT4-train.txt
wget https://huggingface.co/datasets/roneneldan/TinyStories/resolve/main/TinyStoriesV2-GPT4-valid.txt

cd ..
```