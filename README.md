# Build-a-Language-Translation-Bot-using-Amazon-Lex

Steps to Build-a-Language-Translation-Bot-using-Amazon-Lex
1. Creating an empty chatbot
2. Specifying intents and slots
3. Specify Fulfilment
4. Create an IAM role
5. Create a Lambda function
6. Test the Lambda function
7. Test the chatbot

### Services Used 🛠
* Amazon Lex: Build the chatbot and define conversation flow.
* AWS Lambda: For translation.
* AWS IAM: Ensures secure access by managing user permissions.
* Amazon Translate: Used for translation of the sentence according to the input language specified.

### Estimated Time & Cost ⚙️
* This project is estimated to take about 1-2 Hours
* Cost: Free (When using the AWS Free Tier)

### Project Architecture:
<img width="1630" height="711" alt="translator_bot_arch" src="https://github.com/user-attachments/assets/af219e6b-0850-4582-b8d1-f4228d608be9" />

### Final Result:
<img width="345" height="681" alt="final_product" src="https://github.com/user-attachments/assets/1322ef79-4978-4aa0-95c1-c6b50c3f816e" />

```sh
Sample Utterances:

I want to translate
Can you help me translate
Translate for me
I want to translate in {language}
Translate in {language}
Can you translate in {language} for me

Language Slot Type:
French
Japanese
Chinese
Spanish
German
Norwegian

Lambda Role:
TranslateFullAccess
AWSLambdaBasicExecutionRole
```

### Lambda Test Event:

```JSON
{
  "sessionState": {
    "intent": {
      "name": "TranslateIntent",
      "slots": {
        "text": {
          "value": {
            "interpretedValue": "Hello",
            "originalValue": "Hello"
          }
        },
        "language": {
          "value": {
            "interpretedValue": "French",
            "originalValue": "French"
          }
        }
      }
    }
  }
}


