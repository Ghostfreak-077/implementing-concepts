# Sequential Test-time compute

In the file, We've tried to implement [this](https://huggingface.co/spaces/HuggingFaceH4/blogpost-scaling-test-time-compute) blog from huggingface. In this blog, they've tried to scale test-time computing ability of relatively small models like Llama-3.2-1B-Instruct & 3B-Instruct, to perform as well as its larger variants like 8B & 70B respectively, on datasets like MATH-500.

## Models used

In the notebook, we have used Llama-3.2-1B-Instruct through transformers.AutoModelForCausalLM library for the generation, and TinyLlama-1.1B-Chat-v1.0 for Process Reward Model(PRM). 

## Methods used

The paper introduces multiple search-based verifiers, which includes Best-of-N, Beam Search and DVTS. Here, I've proceeded with Beam Search, since it is the most common one.

The blog compares multiple scoring methods like 
- min: Considering the minimum score of the path
- product: Product of the scores in the path
- Last: The score of the last step

We are using the last scoring method for this implementation

## Results
_(The results are yet to be calculated)_

## References
- Article: [HuggingFaceH4/blogpost-scaling-test-time-compute](https://huggingface.co/spaces/HuggingFaceH4/blogpost-scaling-test-time-compute)
- Paper: Beeching, Edward, and Tunstall, Lewis, and Rush, Sasha, "Scaling test-time compute with open models.", 2024.

## Contributing
If you'd like to contribute to the code, please refer to `contribute.md` in the root folder

## To be done
- [ ] Add results
- [ ] Add more models
- [ ] Add more verifiers
- [ ] Streamline the models, verifiers and results