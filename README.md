# mathelementary
Welcome to our elementary math problem-solving project, inspired by the Zalo Ai competition.
## Introduction ##
This project focuses on solving multiple-choice math problems commonly found in elementary schcool. 
Challenge focuses on developing a language model/system capable of answering
elementary-level math questions in alignment with the Vietnamese Education Program
Input: A multiple choices math question which have 4 possible choices which only one is the
correct answer.
Output: The correct choice for the given math question.
## Problem ##

Allowances:
- You are encouraged to utilize pre-trained Large Language Models (LLMs) that are freely available
online, such as Bloom, Llama, and others. However, it is essential to ensure that the pre-trained models
you use are both free and publicly accessible on the internet. If you decide to train your own pre-trained
models, you must provide us with the original textual data and the complete script outlining the entire
process of creating these models.

- We have set a limit on the size of pre-trained models to 14 billion parameters, which allows you to make
use of some open-source pre-trained models.
Restrictions:
- Using APIs that call any external services (e.g. Open AI, Google, ...) during training and inference.
- Training & inference with Internet access.

## Dataset ##
math_train.json - a set of 1200 questions with the answer column
math_test.json - a set of 189 questions
Example:

{
         "id": "1",
         "question": "Một người bán hàng bỏ ra 80,000 đồng tiền vốn và bị lỗ 6%. Để tính số tiền lỗ ta phải tính",
         "choices": [
            "A. 80,000 : 6",
            "B. 80,000 x 6",
            "C. 80,000 : (6 x 100)",
            "D. (80,000 x 6) : 100"
         ],
         "explanation": "Theo đề bài, số tiền lỗ bằng 6% của 80 000 đồng . Để tìm số tiền lỗ ta có thể lấy 80 000 chia cho 100 rồi nhân với 6 (tức là 80 000 : 100 × 6) hoặc lấy 80000 nhân với 6 rồi chia cho 100 (tức là 80 000 × 6 : 100).",
         "answer": "D. (80,000 x 6) : 100"
      },
      

## Model Finetuning ## 
In this section, we focus on fine-tuning the DeBERTa v3 model for our specific task. 
