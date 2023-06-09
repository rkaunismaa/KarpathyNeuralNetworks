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

### 1:38pm

I noticed the base conda environment had PyTorch 1.12, so I pip uninstalled it, rebooted, then tried this notebook again under nlpwt, and it looks like this still works. Nice!
Hmmm but I still see PyTorch '1.31.1+cu116' in the base environment! I am gonna try to also kill that ... 

### 2:08pm

So I am now gonna run this stuff under docker container sad_nightingale, just because it runs fine and already has PyTorch gpu!

### 6:22pm

It's strange to see stuff runs slower on the gpu, and other stuff just does not run if we use the gpu. So I will continue doing the .to(device) stuff in the code, but will default to using torch.device('cpu').

## Friday, June 9, 2023

### 8:50am

Continuing working through "Building makemore Part 3: Activations & Gradients, BatchNorm"

## Monday, June 12, 2023

Finish with "Building makemore Part 3: Activations & Gradients, BatchNorm". Soo much stuff to unpack from the video. The final code was set into makemore_part2_bn.ipynb. 

## Wednesday, June 14, 2023

Continuing with "Building makemore Part 4: Becoming a Backprop Ninja". I am getting the same results in my version of the code 'makemore_part4_backprop.ipynb' compared with when I run the Karpathy version of this code which I replicated into 'makemore_part4_backprop_Karpathy.ipynb'. The video shows all cmp results as equal but I noticed a divergence from when we calculate 'hpreact'. I am not going to try to 'fix' this. 

## Thursday, June 15

I have been trying to understand why the makemore part 4 code runs significantly faster on the CPU than the GPU. I isolated the code I wanted to compare into the files 'makemore_part4_CPU.ipynb' and 'makemore_part4_GPU.ipynb'. The training loop in the CPU version took 10min 27s while the exact same code in the GPU version took 27min 52s. The question is WHY?!

