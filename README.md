# 🎉 Command AI - ai-cli

```text
 ██████╗ ██████╗ ███╗   ███╗███╗   ███╗ █████╗ ███╗   ██╗██████╗  █████╗ ██╗
██╔════╝██╔═══██╗████╗ ████║████╗ ████║██╔══██╗████╗  ██║██╔══██╗██╔══██╗██║
██║     ██║   ██║██╔████╔██║██╔████╔██║███████║██╔██╗ ██║██║  ██║███████║██║
██║     ██║   ██║██║╚██╔╝██║██║╚██╔╝██║██╔══██║██║╚██╗██║██║  ██║██╔══██║██║
╚██████╗╚██████╔╝██║ ╚═╝ ██║██║ ╚═╝ ██║██║  ██║██║ ╚████║██████╔╝██║  ██║██║
 ╚═════╝ ╚═════╝ ╚═╝     ╚═╝╚═╝     ╚═╝╚═╝  ╚═╝╚═╝  ╚═══╝╚═════╝ ╚═╝  ╚═╝╚═╝
 ```

[Join our Discord](https://discord.gg/wPsFbpFHVH)

Welcome to Command AI, your new AI-powered command-line buddy! This program makes handling tasks a breeze. Whether you need to automate routine tasks, set up new projects, or run background operations, just tell it what you want, and it'll get to work. Check out some cool things it can do:

- **Automate Your Routine Tasks:** Need a cron job that checks your IP and pings a specific URL if it changes? Just ask!

  ```bash
  ai "make a cron job that checks my IP and calls https://myipchanged.com when it changes"
  ```

- **Set Up Projects on the Fly:** Want to start an npm project that spins up a configurable web server greeting you with "hello world"? No problem.

  ```bash
  ai "create an npm project in ~/hello-world that starts a webserver saying 'hello world' and reads configs from a .env file"
  ```

- **Run Background Jobs:** Need to list all the JavaScript files on your computer and save them in a file? It can handle that in the background.

  ```bash
  ai "in the background, list all the JS files on this computer and put them in ~/js.txt"
  ```

Just type your request into the CLI with `ai "your requests here"`, and watch the magic happen. It's like having a personal assistant for your terminal!

## 🚧 ALPHA Stage Alert 🚧

This tool is still in its alpha stage, so expect some hiccups as we fine-tune our prompts for different models. The default settings show you execution plans and descriptions before running scripts to keep you in the loop / safe.

## 🔥 Features

- **AI Service Selection**: Pick between Ollama and ChatGPT to generate scripts for you.
- **Easy Configuration**: Set everything up quickly with a few prompts.
- **Execution Plans**: See what’s going to happen before it happens.
- **Optional Logging**: Keep track of everything for debugging or just for fun.

## 📋 Requirements

- Node.js
- npm

## 🚀 Installation

1. **Install globally via npm**:

    ```bash
    npm install -g command-ai
    ```

2. **Upgrade**:

    ```bash
    npm update -g command-ai
    ```

## 🎮 Usage

### Initial Setup

The first time you run it, you’ll set up your AI service and other settings. It saves everything in `~/.commandai/config.json`.

```bash
ai
```

### Provide Command Input

Type your command either as an argument or enter it when prompted.

```bash
ai "your requests here"

# Example requests (use quotes if your shell needs them):
ai make a cron job that checks my IP and calls https://myipchanged.com when it changes

ai create an npm project in ~/hello-world that starts a webserver saying "hello world" and reads configs from a .env file

ai in the background, list all the JS files on this computer and put them in ~/js.txt
```

If you don't provide an argument, `ai` will just ask you to enter it.

```bash
ai
```

### Execution Plans & Descriptions

After you enter a command, Command AI will fetch a script and show you the plan and description. You decide if you want to run it!

### Logging

If you turn logging on, commands and results are stored so you can revisit them anytime. (also please turn on and send if you open up a bug ticket)

## ⚙️ Configuration

Settings are stored at `~/.commandai/config.json`. Here’s what it looks like:

```json
{
  "aiService": "",                   // Pick "Ollama" or "ChatGPT"
  "ollamaUrl": "",                   // Ollama server URL
  "ollamaModel": "",                 // Model for Ollama
  "chatgptApiKey": "",               // ChatGPT API key
  "chatgptModel": "",                // Model for ChatGPT
  "showExecutionDescription": true,  // Show descriptions
  "showExecutionPlan": true,         // Show plans
  "enableLogging": false             // Enable logging
}
```

## 💻 Development

Want to help out? Great! Clone the repo and install dependencies:

```bash
git clone https://github.com/username/command-ai.git
cd command-ai
npm install
```

Run the project:

```bash
npm start
```

## 🤝 Contributing

We’d love your help! Fork the repo, make some changes, and send over a pull request.

## 📜 License

This project is licensed under the MIT License.

---

Enjoy making your CLI life easier with Command AI!
