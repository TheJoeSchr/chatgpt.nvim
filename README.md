## chatgpt.vim 🤖

**chatgpt.nvim** is a neovim plugin that lets you query chatgpt directly in
neovim.

### Demo

[![asciicast](https://asciinema.org/a/9YqFDchOVaQS5QRbGOzWiYNPb.svg)](https://asciinema.org/a/9YqFDchOVaQS5QRbGOzWiYNPb)

### Requirements

You must have **python3** and **pip3** installed on your machine in order to
install and use this plugin.

### Installation

You can install this plugin with packer or any other vim plugin manager:

```lua
use({
  'terror/chatgpt.nvim',
  run = 'pip3 install revChatGPT --upgrade'
})
```

### Configuration

The plugin looks for a configuration file in your home directory called
`.chatgpt-nvim.json`, and it expects a valid `session_token` to be set for
queries to work.

You can find this session token by completing the following steps:
1. Navigate to [https://chat.openai.com/chat](https://chat.openai.com/chat)
   after logging in or signing up
2. Open the developer console (F12)
3. Application > Cookies
4. Copy `__Secure-next-auth.session-token` into the `session_token` field
   present in the `.chatgpt-nvim.json` configuration file

### Credits

The underlying API wrapper this plugin uses (for now) is `revChatGPT`, which is
open source and can be found here:
[https://github.com/acheong08/ChatGPT](https://github.com/acheong08/ChatGPT).