# IELTS Essay Assessment with Fine-Tuned LLaMA2

## Overview
This project involves the fine-tuning of the LLaMA2 chat model on a dataset of approximately 1400 IELTS essays to generate Summary of the essay and the feedback along wth the grade. The project is distinctive due to its use of synthetically generated summaries created using OpenAI's GPT-3.5 Turbo model.

## Dataset
The dataset comprises 1436 IELTS essays along with their corresponding summaries, which were generated using OpenAI's GPT-3.5 Turbo model. This approach provides additional context, assisting the model in effectively analyzing and assessing the essays.

## Model Fine-Tuning
The LLaMA2 model was fine-tuned using advanced methods to optimize the process:
- **Parameter-Efficient Fine-Tuning (PEFT)**: Implemented with the QLoRa (Quantized Low-Rank) method, allowing for efficient tuning of the model's parameters.
- **Transformer Reinforcement Learning (TRL)**: Utilized for Supervised Fine-Tuning (SFT) via a Trainer API, enhancing the model's learning and adaptation to the task.

### Fine-Tuning Steps:
1. **Model and Tokenizer Loading**: Load the LLaMA2 model and its tokenizer in the Google Colab notebook.
2. **PEFT Configuration**: Set up the PEFT configuration using the QLoRa method.
3. **Fine-Tuning Execution**: Conduct fine-tuning using the TRL's SFT Trainer API on the enhanced IELTS essays dataset.

## Usage
To use the fine-tuned model:

1. **Access the Notebook**: The fine-tuning is conducted in a Jupyter notebook hosted on Google Colab. The notebook can be accessed through the provided link.
2. **Run the Notebook**: Follow the step-by-step instructions within the notebook to either perform the fine-tuning process or use the pre-fine-tuned model.
3. **Essay Assessment**: Input an IELTS essay as instructed in the notebook. The model will provide an assessment based on its training and enhanced understanding of essay structure.

## Limitations
- **GPU Memory Size**: The fine-tuning process is resource-intensive and is constrained by the GPU memory available in Google Colab. This may limit the batch size and length of the sequences that can be processed.
- **Amount of Data**: The model is trained on a dataset of 1400 essays, which may affect its ability to generalize across a broader spectrum of writing styles and topics.
