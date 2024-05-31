# Llama2-7B-Chat-PEFT

In this work we have implemented the concept of Quantization and Parameter Efficient Fine Tuning (PEFT) on Llama2 7B model.
Quantization and PEFT are the major tools that support large scale adoption of LLM. Quantization offers the benifit of fitting a
Memory Intensive Model into smaller spaces while preserving accuracy. PEFT allows us to fine tune Very Large Models even with limited
resources. Without PEFT it would be impossible for most of us to fine-tune LLM. There are several existing approach to both Quantization and PEFT.
Here we limit to application to GPTQ quantization and LoRA PEFT.



Parameter Efficient Finetuning(PEFT) a 4bit quantized Llama-2-7b-Chat from TheBloke/Llama-2-7b-Chat-GPTQ on flytech/python-codes-25k dataset.

<img src="https://github.com/swastikmaiti/Llama-2-7B-Chat-PEFT/blob/5dc74f8982916384bb73a010d006c3669e9a35a1/llama2-peft.png">

# Description

LLM drawbacks are they are LLM :smiley: . LLM parameters now range in Billions scale. While their performance keeps increasing, 
the cost to finetune and maintain them is also inceasing drastically. Here comes the beifit of quatization and PEFT.
Quantization refers to converting model weights to lower precision representation to save memory. Parameter Efficient Fine Tunining (PEFT) 
works the way its name describe. In PEFT instead of finetuning on entire model, we train a subset of original model parametrs. This lowers the memory 
reqirements for training and also makes the training more efficient. The efficiency comes from the fact that we are finetuning on a subset of task so 
conventianlly it makes more sense to update a subset of parameters yielding better finetuned results.

# File Structure

- gptq_intro.ipynb:- Describe GPTQ quantization 
- peft_training.ipynb:- Finetuning code
- inference.ipynb:- Performing sanity check on finetuned model.

# TOOLS
- ***Qunatization:*** GPTQ 4bit
- ***PEFT:*** QLoRA
- ***Training:*** HuggingFace Accelerate with Training Loop

# Models and Datasets
- ***Pre-Trained Model:*** Llama-2-7b-Chat-GPTQ
- ***Dataset:*** flytech/python-codes-25k dataset


# Hugging Face

The Model is hosted on Hugging Face Repository. Refer to the Model Card for Training and uasage details.

[Model Card](https://huggingface.co/SwastikM/Llama-2-7B-Chat-text2code) @HuggingFace

#
### If you find the repo helpful, please drop a ⭐
