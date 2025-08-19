# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

# Date: 19/08/2025
# Register no. 212223060291
# Aim: Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools

# AI Tools Required:
```
1. OpenAI GPT (ChatGPT API)

2. Hugging Face Transformers

3. LangChain Framework

4. Google Generative AI API (optional)
```
# Explanation:
```
In this experiment, the Persona Prompting Pattern is applied by assuming the role of a programmer. The application area selected is text summarization and analysis of user feedback for a product.

Steps followed:

Define the persona: Programmer writing Python code for summarization across AI tools.

Develop Python code to interact with multiple AI tools.

Generate outputs from different tools for the same input text (customer reviews).

Compare and analyze results based on clarity, conciseness, and usefulness.
```
# Conclusion:
```
# Example: Python code that integrates with multiple AI tools

from transformers import pipeline
import openai

# 1. Hugging Face Summarization
summarizer = pipeline("summarization")
text = """The product is good but delivery was delayed. Customer support was helpful,
but the mobile app has frequent crashes. Overall, satisfied but improvements needed."""
hf_summary = summarizer(text, max_length=40, min_length=10, do_sample=False)

# 2. OpenAI GPT Summarization (requires API key)
openai.api_key = "YOUR_API_KEY"
response = openai.Completion.create(
    model="text-davinci-003",
    prompt="Summarize the following review:\n" + text,
    max_tokens=50
)
gpt_summary = response["choices"][0]["text"].strip()

print("Hugging Face Summary:", hf_summary[0]['summary_text'])
print("OpenAI GPT Summary:", gpt_summary)
```
The experiment demonstrated the use of Python code compatible with multiple AI tools for summarization. By applying Persona Prompting Pattern, we analyzed outputs from Hugging Face and OpenAI GPT. The comparison showed differences in clarity and detail, proving that tool selection depends on the application requirements.

# Result: The corresponding Prompt is executed successfully.
