# XML

XML is a LLM based on the open-source version of OpenAI’s GPT-2 specifically modified to better train and function on Apple Silicon.

# Important Considerations

• XML does not always give accurate answers.
• XML does not currently utilize GPU architectures such as Nvidia’s CUDA or AMD’s ROCm.
• XML throttles training speed to relieve CPU/GPU from the intensive process. XML throttles by giving the CPU/GPU a break in between training batches, minimizes the amount of threads used during the training process, and utilizes the native version of PyTorch for Apple Silicon to allow the model to use the most out of Metal.