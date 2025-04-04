# PaliGemma
![Screenshot 2025-02-05 082123](https://github.com/user-attachments/assets/81a025d9-5d98-4a3b-97b5-6dc7a16a7da2)

### Check finetuned model on [Hugging Face](https://huggingface.co/MLap/paligemma_intersections) 

## Model description

This model is a fine-tuned version of [google/paligemma-3b-pt-224](https://huggingface.co/google/paligemma-3b-pt-224) on [ariG23498/intersection-dataset](https://huggingface.co/datasets/ariG23498/intersection-dataset).



## Training procedure

Finetuning done using (LoRA) PEFT method. Rank = 8 choosen.

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 2e-05
- train_batch_size: 1
- eval_batch_size: 8
- seed: 42
- gradient_accumulation_steps: 4
- total_train_batch_size: 4
- optimizer: Use OptimizerNames.ADAMW_BNB with betas=(0.9,0.999) and epsilon=1e-08 and optimizer_args=No additional optimizer arguments
- lr_scheduler_type: linear
- lr_scheduler_warmup_steps: 2
- num_epochs: 2


### Framework versions

- PEFT 0.14.0
- Transformers 4.50.2
- Pytorch 2.6.0+cu124
- Datasets 3.5.0
- Tokenizers 0.21.1
