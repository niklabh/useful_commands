Useful Commands
===============

A set of useful shell commands.

###Remove all node_module folders (or any type of folder/file)

```
find . -name "node_modules" -exec rm -rf '{}' +
```

###Print a colourful git log history with branches

```
git log --graph --pretty=format:'\''%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'' --abbrev-commit --date=relative
```
###Show git commits from a particular user

```
git show `git log | grep "Ranjan" -C 3| grep commit | awk '{print $2}'`
```
