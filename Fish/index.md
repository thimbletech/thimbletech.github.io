## Fish
### Package Manager
https://github.com/jorgebucaran/fisher
### Bash support for Fish
https://github.com/edc/bass

## TypeScript Compiler 
### Setup
Note to self: Could run into future issue due to specifying node version

If your shell can not find the tsc command, the node /bin folders needs to be added to the path:
#### Bash
Add
```bash
export PATH="$PATH:"/usr/local/Cellar/node/14.4.0/bin/"";
```
To Your `~/.bash_profile`
#### Fish
```bash
set -Ua fish_user_paths /usr/local/Cellar/node/14.4.0/bin/
```