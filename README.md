# Deep-Learning-Text-to-SVG-Generation
> There are two versions of the full version of the Notebook: One for Google Colab and One for Kaggle. There are minor differences between the two with certain parameters being adjusted to better suit the limitations of the GPU and keep training time to an acceptable amount. Paths to access inputs are also different.

> The A100 GPU was used for testing in the Google Colab while the GPU T4 x2 was used in Kaggle. 

## Notebook can be broken down to three sections:
> The notebook is compromised of three parts: the preprocessing of data, training the model and inference for output generation.
> Three smaller notebooks were created that can be run on their own (dl-midterm-preprocessing-notebook-kaggle.ipynb, dl-midterm-training-notebook-kaggle.ipynb, and dl-midterm-generation-inference-kaggle.ipynb)

### 1. Preprocessing
> [dl-midterm-preprocessing-notebook-kaggle.ipynb](https://github.com/tk2558/Deep-Learning-Text-to-SVG-Generation/blob/main/dl-midterm-preprocessing-notebook-kaggle.ipynb)

> This section focuses on preprocessing the data provided from train.csv

> Make sure notebook has access to train.csv as an input or adjust path for notebook to access it 

> Here we focus on creating a data pipeline that: compresses a SVG training data, scales it to a 256x256 canvas size, and then compresses it again along with suitability checks to determine whether to use it for training. 

### 2. Training
> [dl-midterm-training-notebook-kaggle.ipynb](https://github.com/tk2558/Deep-Learning-Text-to-SVG-Generation/blob/main/dl-midterm-training-notebook-kaggle.ipynb)

> This section focuses on training the model on the new train_compressed.csv

> You can either upload train_compressed.csv as an input or access the public version of the train_compressed.csv dataset through HuggingFace. Adjustments may need to be made depending on your choice

> Here we focus on creating a training set and evaluation set before the model is then trained on them with SFTTrainer

### 3. Inference/Generation
> [dl-midterm-generation-inference-kaggle.ipynb](https://github.com/tk2558/Deep-Learning-Text-to-SVG-Generation/blob/main/dl-midterm-generation-inference-kaggle.ipynb)

> This section focuses on generating outputs with the model

> Make sure notebook has access to test.csv as an input if you want to test the model against it and access to a HuggingFace Token to use the pre-fine-tuned model!

> Here we focus on generating outputs based on given prompts. There are two versions of outputting: single prompt output and batch prompt outputs

### **Important**
> Make sure that train.csv and test.csv is downloaded to upload them as inputs for the notebooks to access! You can also download train_compressed from HuggingFace to skip preprocessing part 1 (train_compressed.csv was created through data compression pipeline and uploaded to HuggingFace as a public dataset for ease of access)

> Have a HuggingFace Token Key for Reading and Writing. Make sure notebook has access to them before running it!

### Misc
> If you want to see a graph of token distribution in train.csv vs train_compressed.csv, check out the [Submission and Figures Folder](https://github.com/tk2558/Deep-Learning-Text-to-SVG-Generation/tree/main/Submission%20and%20Figures)
> You can also see all the outputs the model generated for 1000 test prompts in [submission.csv](https://github.com/tk2558/Deep-Learning-Text-to-SVG-Generation/blob/main/Submission%20and%20Figures/submission.csv)

### **Links**

> [Midterm Report in ACL Format](https://drive.google.com/file/d/1urAfCZN6PuFEgmFVQYVjykXzaEXdAuox/view?usp=sharing)

> [Model Weights in Hugging Face](https://huggingface.co/tk2558/qwen_lora_midterm)

> [Public Version of Created train_compressed Dataset](https://huggingface.co/datasets/tk2558/train_compressed)

> [Download train.csv and test.csv from Kaggle](https://www.kaggle.com/competitions/dl-spring-2026-svg-generation-from-text-prompts-extended-deadline/data)

> [Github Repo](https://github.com/tk2558/Deep-Learning-Text-to-SVG-Generation)
