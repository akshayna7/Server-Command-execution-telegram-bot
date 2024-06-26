🤖 ShellRunner Telegram Bot 🚀

This repository hosts a fully functional Telegram bot capable of executing commands and streaming live output back to users. Send a command, and watch as the bot executes it in real-time, providing you with the output. Plus, you can interact with the commands by replying to the output messages, enabling seamless communication.

This bot is not your average run-of-the-mill executioner. It simulates a terminal environment, interpreting escape sequences, and dynamically updating messages if their content changes. This means interactive programs like wget function naturally, with status bars updating in real-time.

In addition to command execution, the bot supports file uploads and downloads, making it versatile for various tasks. Need to quickly edit a text file? No problem! The bot also features a simple text editor for added convenience.

Join the bot revolution and streamline your command execution and file management tasks effortlessly!

🔧 Feel free to contribute and enhance this project further! Let's make it even more awesome together! 💻



**Note:** Due to the tight integration, running this bot on Windows is
currently *not* supported.

## Install

First install [node-pty dependencies](https://github.com/Microsoft/node-pty#dependencies). For example, if you're in Ubuntu/Debian:

~~~
sudo apt install -y make python build-essential
~~~

If you're using fedora instead:
```
sudo dnf install -y python
sudo dnf group install -y "C Development Tools and Libraries" 
```


~~~
git clone this repo
npm install
~~~

To start the bot:

~~~
node server
~~~

The first time you run it, it will ask you some questions and create
the configuration file automatically: `config.json`. You can also
write it manually, see `config.example.json`.

When started it will print a `Bot ready.` message when it's up and running.
For convenience, you might want to talk to the BotFather and set the
command list to the contents of `commands.txt`.

## Authorization

When first started, the bot will just accept messages coming from your user.
This is for security reasons: you don't want arbitrary people to issue
commands to your computer!

If you want to allow another user to use the bot, use `/token` and give
that user the resulting link. If you want to use this bot on a group,
`/token` will give you a message to forward into the group.

## Proxy server

shell-bot obeys the `https_proxy` or `all_proxy` environment variable
to use a proxy, and supports HTTP/HTTPS/SOCKS4/SOCKS4A/SOCKS5 proxies.
Examples:

~~~ bash
export https_proxy="http://168.63.76.32:3128"
node server

export https_proxy="socks://127.0.0.1:9050"
node server
~~~

**Warning:** For SOCKS proxies, you need to use an IP address (not a DNS hostname).
