# Assembly-to-C transformer experiment

An exploratory sequence-to-sequence experiment using `t5-small` to map assembly snippets to C snippets. The [training examples](data/) are deliberately tiny, so this project demonstrates a modeling workflow rather than a capable decompiler.

## Explore the project

- [Training script](scripts/train.py)
- [Model and dataset code](scripts/)
- [Inference notebook](test_the_model.ipynb)
- [Dependency list](requirements.txt)

The original workflow installs dependencies, runs `python scripts/train.py` from the repository root, and opens the notebook to inspect generated output. Training downloads a pretrained model and writes a local `saved_model/` directory. The script assumes its dependency versions and import paths are compatible with the local environment; it has not been retested against recent libraries.

## Interpretation

A few paired examples cannot establish translation quality across compilers, architectures, optimizations, or unseen programs. Treat outputs as experimental and inspect them manually. This is not a production reverse-engineering tool.

Inspired by publicly discussed assembly-to-source research, including [RevEng.AI's write-up](https://blog.reveng.ai/training-an-llm-to-decompile-assembly-code/).
