# functional-programming

All the functional code made during my functional programming studies

## Setup (Manjaro)

### Installing Ruby

```bash
yay -S rbenv
export PATH="$HOME/.rbenv/shims:$PATH"
mkdir -p "$(rbenv root)"/plugins
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
git clone git://github.com/jf/rbenv-gemset.git $HOME/.rbenv/plugins/rbenv-gemset

curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash
echo 2.6.5 > $HOME/.rbenv/version
export PATH="$HOME/.rbenv/bin:$PATH"
echo 'eval "$(rbenv init -)"' >> ~/.zshenv
echo 'source $HOME/.zshenv' >> ~/.zshrc
exec $SHELL
rbenv install 2.6.5
```

### Installing NodeJS

```bash
yay -S nvm
echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.zshrc
source ~/.zshrc
nvm install 8.12.0
nvm use 8.12.0
node # starts node repl
```

### Installing Clojure

```bash
yay -S clojure aur/leiningen
lein repl # starts clojure repl
```

### Installing Elixir

```bash
yay -S elixir
iex # starts elixir repl
```
