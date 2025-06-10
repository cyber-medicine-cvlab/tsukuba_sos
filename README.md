---
title: Intel® AI for Enterprise Inference
emoji: 📚
colorFrom: yellow
colorTo: purple
sdk: streamlit
sdk_version: 1.45.1
app_file: app.py
pinned: false
license: apache-2.0
short_description: 'LLM Chatbot with Intel® Gaudi®'
---

# LLM Chatbot
Similar to ChatGPT, this application provides a user-friendly interface to chat with various LLMs. This application uses fully open-source models, all hosted with the inference endpoint [Intel® AI for Enterprise Inference](https://github.com/opea-project/Enterprise-Inference), powered by Intel® Gaudi® AI accelerators. The chatbot supports streaming responses and offers a selection of different LLMs, including Llama, DeepSeek, and Qwen. 

[![llmchatbot](images/llmchatbot.png)](https://huggingface.co/spaces/Intel/intel-ai-enterprise-inference)

## Setup

If you want to host the application locally with Streamlit, you can follow the steps below. If you want to host the application on Hugging Face Spaces, the easiest way is to duplicate the Hugging Face Space (per the screenshot below), and set up your own API secrets as detailed below. Just like any GitHub repository, you can use the same Git actions with the Hugging Face Space to clone, add, push, and commit your changes.

[![hf_dup](images/hf_dup.png)](https://huggingface.co/spaces/Intel/intel-ai-enterprise-inference)

1. Clone the repository:
```bash
git clone https://huggingface.co/spaces/Intel/intel-ai-enterprise-inference
cd intel-ai-enterprise-inference
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

### Secrets Management

This application requires API credentials to be set up in Streamlit's secrets management. You need an OpenAI-compatible API key and model endpoint URL. In the case of this application, it is using an API key from [Denvr Dataworks](https://www.denvrdata.com/intel).

1. If hosting on Hugging Face Spaces:
- Add your OpenAI-compatible API key under "Secrets" in the HF settings as `openai_apikey`
- Add the base URL for your model endpoint under "Variables" as `base_url`

2. For local development, create a `.streamlit/secrets.toml` file with:
```toml
openai_apikey = "your-api-key-here"
```
Set the `base_url` environment variable to point to your OpenAI-compliant model endpoint with hosted models. For example,
```bash
export base_url="https://api.inference.denvrdata.com/v1/"
```
Run the Streamlit application locally:

```bash
streamlit run app.py
```

Enjoy using the speedy LLM chat application for any number of language-based tasks like essay writing, summarizing text, or code generation.

## License

This project is licensed under the Apache License 2.0.

## Follow Up

Connect to LLMs on Intel Gaudi AI accelerators with just an endpoint and an OpenAI-compatible API key, using the inference endpoint [Intel® AI for Enterprise Inference](https://github.com/opea-project/Enterprise-Inference), powered by OPEA. At the time of writing, the endpoint is available on cloud provider [Denvr Dataworks](https://www.denvrdata.com/intel). 

Chat with 6K+ fellow developers on the [Intel DevHub Discord](https://discord.gg/kfJ3NKEw5t).

Follow [Intel Software on LinkedIn](https://www.linkedin.com/showcase/intel-software/).

For more Intel AI developer resources, see [developer.intel.com/ai](https://developer.intel.com/ai).
