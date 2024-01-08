# DialogSum - AI Text Summarization using FLAN-T5

DialogSum is a project that leverages the FLAN-T5 model for automatic text summarization of dialogues. It utilizes Hugging Face's Transformers library and a custom dataset for training and evaluation.

## Features

- **FLAN-T5 Model Integration:** The project incorporates the powerful FLAN-T5 model from Google for sequence-to-sequence learning, making it adept at summarizing dialogues.

- **Dataset:** Utilizes a custom dataset (`knkarthick/dialogsum`) for training and testing the summarization model. The dataset includes dialogues and corresponding human-generated summaries.

- **Interactive Examples:** Demonstrates how to use the FLAN-T5 model for dialogue summarization with interactive examples. You can explore the input dialogue, baseline human summary, and model-generated summaries.

- **Prompt Engineering Strategies:** Explores different prompt engineering strategies, such as zero-shot and few-shot learning, to showcase the versatility of the summarization model.

## Use Cases

DialogSum can be applied in various scenarios:

- **Educational Content Summarization:** Summarize educational dialogues to provide concise and informative summaries for students and educators.

- **Conversational AI:** Enhance conversational AI systems by integrating the model to generate succinct summaries of user interactions.

- **Information Retrieval:** Improve information retrieval systems by summarizing lengthy dialogues, making it easier for users to grasp essential information quickly.

## Getting Started

1. **Installation:**
    ```bash
    %pip install --upgrade pip
    %pip install --disable-pip-version-check torch==1.13.1 torchdata==0.5.1 --quiet
    %pip install transformers==4.27.2 datasets==2.11.0 --quiet
    ```

2. **Dataset Loading:**
    ```python
    huggingface_dataset_name = "knkarthick/dialogsum"
    dataset = load_dataset(huggingface_dataset_name)
    ```

3. **Model Initialization:**
    ```python
    model_name = 'google/flan-t5-base'
    model = AutoModelForSeq2SeqLM.from_pretrained(model_name)
    tokenizer = AutoTokenizer.from_pretrained(model_name, use_fast=True)
    ```

4. **Example Usage:**
    Explore example scripts in the code to understand how to use the model for summarization with different prompt engineering strategies.

5. **Custom Prompt Generation:**
    Use the provided functions to generate custom prompts for one-shot and few-shot summarization.

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

---

Feel free to contribute, report issues, or suggest improvement.

Keep exploring and keep learning. Happy summarizing!

