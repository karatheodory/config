[source](https://www.atlassian.com/git/tutorials/dotfiles)

# How to use

```bash
git clone --bare https://bitbucket.org/karatheodory/config.git ${HOME}/.cfg
function config {
   /usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME $@
}

config checkout
if [ $? = 0 ]; then
  echo "Checked out config.";
  else
    echo "Backing up pre-existing dot files.";
    mkdir -p .config-backup
    config checkout 2>&1 | egrep "\s+\." | awk {'print $1'} | xargs -I{} mv {} .config-backup/{}
fi;
config checkout
config config status.showUntrackedFiles no
```

# How to start from scratch

```bash
# Init a repository in your home directory:
git init --bare ${HOME}/.cfg

# Create alias in the current shell
alias config='/usr/bin/git --git-dir=${HOME}/.cfg/ --work-tree=${HOME}'

# Ignore untracked files, so everything would look clean:
config config --local status.showUntrackedFiles no

# Add alias to shells:
echo "alias config='/usr/bin/git --git-dir=${HOME}/.cfg/ --work-tree=$HOME'" >> ${HOME}/.bashrc
echo "alias config='/usr/bin/git --git-dir=${HOME}/.cfg/ --work-tree=$HOME'" >> ${HOME}/.zshrc
```
