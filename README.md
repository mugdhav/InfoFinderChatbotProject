# InfoFinderChatbotProject
This repository houses my submission to the [Google Dialogflow CX Competition](https://events.withgoogle.com/dialogflow-cx-competition-global/).
I have created a single-flow chatbot that collects the following input from its user to identify the product information required by the user:
- Product name
- Product version
- Information type

The flow I have designed for my competetion submission can handle the following errors made by its user:
- Unrecognized input
- Insufficient input (user does not provide one or two of the above-mentioned input)
- Partially-correct input (user provides only one or two of the above-mentioned input correctly)

User may provide:
- Any random text as input. The chatbot prompts user to confirm if they want information about the replacing product.
- All required input in a single turn when initiating a conversation with the chatbot. The chatbot prompts user only for confirmation.
- An obsolete/discontinued product that may or may not have been replaced with another. The chatbot prompts user to confirm if they want information about the replacing product.
- A version that does not exist. The chatbot considers the most latest version of a given product in such a case.
