## Github Aliases

```
view = log --graph --decorate --oneline
sta = stash --include-untracked
cm = commit -m
ce = commit --allow-empty -m empty
cb = checkout -b
ph = push -u origin HEAD
dh = diff --staged HEAD
alias = ! git config --get-regexp ^alias\. | sed -e s/^alias\.// -e s/\ /\ =\ /
ct = !sh -c 'git checkout -b $1 origin/$1 && git pull' -
clean = !f(){ git branch | grep -v master | grep -v ^* | xargs git branch -d; }; f
force-clean = !f(){ git branch | grep -v master | grep -v ^* | xargs git branch -D; }; f
master = !git checkout master && git pull
tests = !git add . && git cm tests && git ph
```
