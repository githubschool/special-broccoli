Welcome!

**Please note** We'll be using Gitter, a chat service that integrates with GitHub, for Q&A. Please click on the button below to join the chat room associated with this repo.

[![Gitter](https://badges.gitter.im/githubteacher/special-broccoli.svg)](https://gitter.im/githubteacher/special-broccoli?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)


### Extras
To print the name of your currently checked out branch in your prompt, include this line as part of your `PS1`:

```bash
git branch 2>/dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
```

People sometimes ask about the Terminal.app theme they see on screen. It is [ocean-terminal](https://github.com/mdo/ocean-terminal). The prompt (`PS1`) is:

```bash
export PS1="\[\$(tput bold)\]\[\$(tput setaf 6)\]\w\[\$(tput setaf 3)\]\$(git branch 2>/dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/')\[\$(tput setaf 6)\] > \[\$(tput sgr0)\]"
```
