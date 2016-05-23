
## bash's PS1 with GIT branch
(https://www.leaseweb.com/labs/2013/08/git-tip-show-your-branch-name-on-the-linux-prompt/)

```
parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[01;31m\]$(parse_git_branch)\[\033[00m\] \n\$ '
```
