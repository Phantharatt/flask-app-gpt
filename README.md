# flask-app-gpt (Test Only) api

## Template openai connect model
```python
import openai

# Set your OpenAI API key
openai.api_key = "your-openai-api-key"

# Define the text you want to analyze or interact with
text = "I am very happy today!"

# Make a request to the OpenAI GPT-3.5 API
response = openai.ChatCompletion.create(
    model="gpt-3.5-turbo-0125",
    messages=[
        {"role": "system", "content": "tell me about all ingredient of the following text and change it to thai language:"},
        {"role": "user", "content": text}
    ]
)

# Extract the response text
response_text = response['choices'][0]['message']['content'].strip()

print("Response from GPT-3.5:", response_text)
```
