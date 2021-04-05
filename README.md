# 🥒 Chatpickle

## Conversation Tests for Chatbots

* Describe conversational flows using Gherkin syntax.
* Run them as tests against your deployed chatbot.
* Supported chatbot service integrations:
  * AWS Lex

### Installing Chatpickle
`npm install chatpickle --save-dev`

### Create a chatpickle configuration json and chatpickle folder
The following sample project, [examples/parentProject](https://github.com/libertymutual/chatpickle/tree/master/examples/parentProject), is designed to be pointed at the OrderFlowersBot as provided by AWS as a blueprint.

You need a [chatpickle.config.json](https://github.com/libertymutual/chatpickle/tree/master/examples/parentProject/chatpickle.config.json) in the root of your node.js project and it should be formatted like the example provided.

You also need a [chatpickle/](https://github.com/libertymutual/chatpickle/tree/master/examples/parentProject/chatpickle) folder in the root of your project.  This is where you will put your gherkin feature files which can leverage the extended chatpickle syntax.

### Setup a Lex Chatbot
To setup an OrderFlowersBot from a blueprint in your AWS account, follow this [AWS Lex Guide](https://docs.aws.amazon.com/lex/latest/dg/gs-bp-create-bot.html).

Or if you want to get started with chatpickling a custom lex bot,  alter your project's chatpickle config; see example at [chatpickle.config.json](https://github.com/libertymutual/chatpickle/tree/master/examples/parentProject/chatpickle.config.json) 

### Setup IAM Credentials
You will need to create IAM credentials that can invoke your bot. You can use the Amazon managed policies as shown below. Load them in your `.aws` directory or follow this [AWS CLI Configure Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html).

![Lex Execution IAM Credentials](https://miro.medium.com/max/750/0*m55m6A95OcpcFRDa.png)

### Running Chatpickle
From your project root, or added as a script to your package.json:

`chatpickle`

### Extending Chatpickle
This release of Chatpickle was focussed around the AWS Lex service.  You can help extend chatpickle by contributing to our open source project [https://github.com/libertymutual/chatpickle](https://github.com/libertymutual/chatpickle) and by adding more bot clients to [src/lib/botClients](src/lib/botClients).