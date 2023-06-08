# KarpathyNeuralNetworks

This is a walk through of the excellent Andrej Karpathy [Neural Networks: Zero to Hero](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ) video series on youtube.

I am using the conda environment 'nlpwt' for this repository.

## Wednesday, May 31, 2023

I initially began this notebook yesterday, using docker container heuristic_kilby, but was unable to get the graphviz stuff running, so I switched to the 'nlpwt' conda environment. 

### 6:25pm 

Done the first video, [The spelled-out intro to neural networks and backpropagation: building micrograd](https://www.youtube.com/watch?v=VMj-3S1tku0) I am really glad I went through the process of watching this video and coding it out myself!

## Thursday, June 1, 2023

### 12:53pm

Starting to go through the second video [The spelled-out intro to language modeling: building makemore](https://www.youtube.com/watch?v=PaCmpygFfXo)

## Wednesday, June 7, 2023

Continuing to go through and code the third video [Building makemore Part2:MLP](https://www.youtube.com/watch?v=TCH_1BHY58I)

### 5:39pm 

Finished up the third video. 

## Thursday, June 8, 2023

### 12:56pm

I was working through the 4th video and noticed the conda environment nlpwt is using the cpu only version of PyTorch but I want to use the gpu version of PyTorch, so I am going to conda install the gpu version ...

Hmmm ... actually, I am not gonna do that. I am going to create a new conda environment that uses PyTorch and I don't want to use docker just because I don't like those permission issues I get.

