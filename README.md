# ChatGPT Siri Shortcut

Talk to ChatGPT with Siri shortcuts on iOS, macOS, and watchOS devices. This open-source project is lightweight and highly customizable.

## Features

- Supports both the [OpenAI API](https://platform.openai.com/docs/api-reference/chat "API Reference – OpenAI API") and [Microsoft Azure OpenAI Services API](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/reference "Azure OpenAI Service REST API reference – Azure OpenAI – Microsoft Learn").
- Conduct conversations through text or with full voice input and output via Siri.
- Available on iOS, macOS, watchOS, and can be used with Siri through voice on HomePod and CarPlay.
- Automatically saves conversation logs in Markdown format (by default, logs are only saved for one day, but [Advanced Configuration](#Advanced%20Configuration) allows customization for any duration), and calculates the number of tokens used and corresponding cost.
- Localization support: currently available in 🇬🇧 English, 🇪🇸 Español, 🇫🇷 Français, 🇵🇹 Português, 🇨🇳 简体中文 and 🇹🇼 繁體中文.

## Privacy

- No app installation required and no data is uploaded, only except for your prompt and calls to the official API. There is no developer data tracking and your personal information is never collected. Everything is transparent.
- Eliminates any risk of your API keys being exposed.

## Prerequisites

**1. Apply for your API key:**

- OpenAI: You can find your API key or create new secret keys in [User settings](https://platform.openai.com/account/api-keys). Please confirm that your country is on the list of [supported countries](https://platform.openai.com/docs/supported-countries "Supported countries and territories – OpenAI API") by OpenAI, as failure to do so may result in your API key not working or violating OpenAI's terms and policies.
- Microsoft Azure OpenAI Service: If you have an Azure subscription, you will need to [submit an additional request](https://azure.microsoft.com/en-us/products/cognitive-services/openai-service "Advanced Language Models – Microsoft Azure") and wait for approval before deploying the model. You can find the `Endpoint` and keys in the Resource Management section. You can use either `KEY 1` or `KEY 2`.

**2. Enable iCloud:**

ChatGPT Siri shortcuts store log files in the Shortcuts folder on iCloud Drive, named `ChatGPT.md`. Therefore, you need to sign in to your Apple ID and enable iCloud on your device. Unless you manually update the log file storage location in the shortcut and change it to another directory on your device.

## Installation

To allow third-party shortcuts from outside the Gallery to run on your iPhone, iPad, or Mac, you need to enable _Private Sharing_ settings for the Shortcuts app. Please refer to: [https://support.apple.com/guide/shortcuts/adjust-privacy-settings-apd961a4fc65/ios](https://support.apple.com/guide/shortcuts/adjust-privacy-settings-apd961a4fc65/ios "Adjust basic privacy settings in Shortcuts on iPhone and iPad – Apple Support")

- On your iOS or iPadOS device, go to _Settings_  \> _Shortcuts_ and then turn on _Private Sharing_.
- On your Mac, choose _Shortcuts_ \> _Settings_ from the menu bar (at the top of the screen). In the _General_ pane, select _Private Sharing_.

Next, [download the ChatGPT Siri Shortcut here](https://www.icloud.com/shortcuts/1675a399a3b14894a6da848b21074edb "Ask AI") and add it to your Shortcuts app.

Then, you need to answer three questions to initialize the shortcut. Skipping this setup will prevent you from using the shortcut correctly.

**1. Language settings:**

Enter the ISO 639-1 standard code for the language you want to use. Currently supported languages are English (`en`), Spanish (`es`), French (`fr`), Portuguese (`pt`), Simplified Chinese (`zh-CN`), and Traditional Chinese (`zh-TW`). The `en` is the default option.

**2. Chat completion API endpoint:**

- The OpenAI API endpoint `https://api.openai.com/v1/chat/completions` is the default option, and no modification is required if you plan to use it.
- For Microsoft Azure OpenAI Service, the API endpoint depends on your Azure account configuration and has the format `https://{your-resource-name}.openai.azure.com/openai/deployments/{deployment-id}/completions?api-version={api-version}`. Refer to the [Prerequisites](#Prerequisites) section for instructions on using your key to send requests to your API endpoint.

**3. API key:**

If you choose to use the OpenAI API endpoint, your key should start with `sk-`. For Microsoft Azure OpenAI Service, the key is a randomly generated string. Refer to the [Prerequisites](#Prerequisites) section for instructions on how to apply for an API key.

## Usage

You can use the shortcut in the following four ways:

**1. Direct use:**

Open the Shortcuts app and select Ask AI, then start a conversation with ChatGPT. It supports continuous conversation with context until you exit the current session. By default, your session history is saved in Markdown format in the `ChatGPT.md` file in the Shortcuts folder.

**2. Share sheet:**

You can choose to share a piece of text or a Safari webpage with the shortcut, then select how you want it to handle the content. The shortcut provides four preset methods to handle shared content: _Translate from / to…_, _Summarize and provide an abstract_, _Polish and edit_, and _Analyze and interpret code_. You can also select _Customize_ to describe any other ideas you have.

**3. Use Siri with your voice:**

You can use “_Hey Siri, ask AI_” to launch the shortcut, wait for Siri to respond with “_What can I help you with?_” and then start your conversation. Siri will speak ChatGPT’s response through voice and prompt you with “_Please continue…_” to indicate it is waiting for your subsequent language input. You can use commands such as “_Cancel_” or “_Quit_” to terminate the conversation.

**4. Use on your Apple Watch:**

For usage on watchOS, please refer to: [https://support.apple.com/en-us/guide/watch/apd99050d435/watchos](https://support.apple.com/en-us/guide/watch/apd99050d435/watchos "Use shortcuts on Apple Watch – Apple Support")

## License

This project is licensed under the GNU AGPLv3 license. See the [LICENSE](LICENSE) file for details.
