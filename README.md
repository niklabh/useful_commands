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

###Jshint all important files in projects

```
find . -type f -name '*.js' -and -not -path './node_modules/*' -and -not -path './public/*' -and -not -path './doc/*' | xargs jshint | less
```

###Update a linux box

```
sudo apt-get update && sudo apt-get upgrade && sudo apt-get clean
```

###Split a File on a particular line pattern

```
awk '/IAMAPATTERN/{x="itc_codes"++i;next}{print > x;}' filename
```
