# Llama-2-7B-Chat-PEFT

Parameter Efficient Finetuning(PEFT) a 4bit quantized Llama-2-7b-Chat from TheBloke/Llama-2-7b-Chat-GPTQ on flytech/python-codes-25k dataset.

LLM drawbacks are they are LLM :smiley: . LLM parameters now range in Billions scale. While their performance keeps increasing, 
the cost to finetune and maintain them is also inceasing drastically. Here comes the beifit of quatization and PEFT.
Quantization refers to converting model weights to lower precision representation to save memory. Parameter Efficient Fine Tunining (PEFT) 
works the way its name describe. In PEFT instead of finetuning on entire model, we train a subset of original model parametrs. This lowers the memory 
reqirements for training and also makes the training more efficient. The efficiency comes from the fact that we are finetuning on a subset of task so 
conventianlly it makes more sense to update a subset of parameters yielding better finetuned results.

In the notebooks we show practical implemetation of QUANTIZATION AND PEFT. There are several existing approach to both Quantization and PEFT.
Here we limit to application to GPTQ quantization and LoRA PEFT.

- gptq_intro.ipynb:- Describe GPTQ quantization 
- peft_training.ipynb:- Finetuning code
- inference.ipynb:- Performing sanity check on finetuned model.

For more deatils have a look at [Model Card](https://huggingface.co/SwastikM/Llama-2-7B-Chat-text2code) @HuggingFace
