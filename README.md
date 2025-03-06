# XML-GPT

XML-GPT is a simple yet capable GPT that can be quickly and easily trained.

# Important Considerations

-  XML-GPT does not always produce understandable text.
-  XML-GPT utilizes Apple's Metal through Torch MPS in the main branch and Nvidia's CUDA in the cuda-old/cuda branch. XML-GPT does not currently natively support AMD's ROCm, but you could manually add it using the steps listed below.

# Required Dependencies

-   `PyTorch`<sup>†<sup>
-   `Numpy`
-   `transformers` for huggingface transformers.
-   `datasets` for loading in datasets.
-   `tiktoken` OpenAI's fast BPE code.
-   `tqdm` for progress bars.
-   `MLX` for optimization on Apple Silicon. **Only Required for Metal**

To install these dependencies enter this code into your terminal:

**With Default PyTorch**
```
pip install torch numpy transformers datasets tiktoken tqdm mlx
```
**Without PyTorch**
```
pip install numpy transformers datasets tiktokem tqdm mlx
```



<sup>†<sup> = install either the default version of PyTorch if using the main branch and Cuda version if using cuda-old/cuda branch.
# Linux Only • How to add support for AMD's ROCm

1. First of all make sure that you have the latest version of python installed.
2. Install the appropriate version of PyTorch or Torch that supports ROCm by entering this command in the Command Prompt. 
**Please Note:** PyTorch with ROCm support is currently only available on Linux.
```
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/rocm6.2.4
```
3. And replace all instances of "mps" in model.py with "rocm"
4. Run model.py

**Please Note:** Manually adding ROCm could have unexpected consiquences.
