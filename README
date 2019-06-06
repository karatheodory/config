# How to store dotfiles

```bash
# Init a repository in your home directory:
git init --bare ${HOME}/.cfg
# Create alias in the current shell
alias config='/usr/bin/git --git-dir=${HOME}/.cfg/ --work-tree=${HOME}'
# Ignore untracked files, so everything would look clean
config config --local status.showUntrackedFiles no
# add alias to shells
echo "alias config='/usr/bin/git --git-dir=${HOME}/.cfg/ --work-tree=$HOME'" >> ${HOME}/.bashrc
echo "alias config='/usr/bin/git --git-dir=${HOME}/.cfg/ --work-tree=$HOME'" >> ${HOME}/.zshrc
```

