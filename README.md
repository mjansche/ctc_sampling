# Sampling from Stochastic Finite Automata with Applications to CTC Decoding

This repository contains code and data to accompany the paper
[Sampling from Stochastic Finite Automata with Applications to CTC Decoding](https://arxiv.org/abs/1905.08760),
to appear in [Interspeech 2019](https://www.interspeech2019.org).

## Abstract

> Stochastic finite automata arise naturally in many language and speech processing tasks. They include stochastic acceptors, which represent certain probability distributions over random strings. We consider the problem of efficient sampling: drawing random string variates from the probability distribution represented by stochastic automata and transformations of those. We show that path-sampling is effective and can be efficient if the epsilon-graph of a finite automaton is acyclic. We provide an algorithm that ensures this by conflating epsilon-cycles within strongly connected components. Sampling is also effective in the presence of non-injective transformations of strings. We illustrate this in the context of decoding for Connectionist Temporal Classification (CTC), where the predictive probabilities yield auxiliary sequences which are transformed into shorter labeling strings. We can sample efficiently from the transformed labeling distribution and use this in two different strategies for finding the most probable CTC labeling.

## Usage example

Compile the code with [Bazel](https://bazel.build):
```
bazel build -c opt src/...
```

Decode a CTC phoneme lattice, generating verbose output:
```
bazel-bin/src/best-labeling -v=1 data/fsts/esw_04310_01381679842.fst
```

## License

Code and data are Copyright 2018-2019 Google LLC,
originally from [google/language-resources](https://github.com/google/language-resources),
originally made available and redistributed here under the following licenses:
* Data files in [data/fsts](data/fsts) and [data/logits](data/logits) are derived from a
  [Crowdsourced high-quality Argentinian Spanish speech data set](http://openslr.org/61)
  under a [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license](data/LICENSE)
  and redistributed here under that same license.
* All other files are derived from [google/language-resources](https://github.com/google/language-resources)
  under an [Apache 2.0 license](LICENSE) and redistributed here under that same license.
