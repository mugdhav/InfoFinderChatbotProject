# InfoFinderChatbotProject
This repository houses my submission to the [Google Dialogflow CX Competition](https://events.withgoogle.com/dialogflow-cx-competition-global/).
I have created a single-flow chatbot that helps its user find information about products of a fictitious CorpX.
It collects the following input from its user to identify the product information required by the user:
- Product name
- Product version
- Information type

The flow I have designed for my competition submission can handle the following errors made by its user:
- Unrecognized input
- Insufficient input (user does not provide one or two of the above-mentioned input)
- Partially-correct input (user provides only one or two of the above-mentioned input correctly)

User may provide:
- Any random text as input. The chatbot prompts user with a list of existing products to request information for one of those products.
- All required input in a single turn when initiating a conversation with the chatbot. The chatbot prompts user only for confirmation.
- An obsolete/discontinued product that may or may not have been replaced with another. The chatbot prompts user to confirm if they want information about the replacing product.
- A version that does not exist. The chatbot considers the latest version of a given product in such a case.

*Judges, please refer to the screenshot of interactions showing such inputs.*

When the chatbot receives all required input, it is supposed to make a REST API call to the CorpX documentation portal service, providing the collected input at request parameters (only a placeholder provided). It is supposed to receive a JSON response from the API about matching document(S) containing information requested by the user. The response is to contain one or more entries, each entry containing the document name, URL of an icon indicating the document type (Text/Word/PDF/EXL etc), and a download link for the document. The chatbot will then render these as custom payload in its turn to the user.
