# ZSH
`chsh -s /bin/zsh`

# HOMEBREW
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`

# GIT
`brew install git`
`which git`

`git config --global color.ui true`
`git config --global user.name "YOUR NAME"`
`git config --global user.email "YOUR@EMAIL.com"`

# SSH
`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
`eval "$(ssh-agent -s)"`
`touch ~/.ssh/config`
`open ~/.ssh/config`
```
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa
```
`ssh-add -K ~/.ssh/id_rsa`
`pbcopy < ~/.ssh/id_rsa.pub`
Add SSH key via UI
`ssh -T git@github.com`

# VIM
`mkdir -p ~/.vim/pack/tpope/start`
`cd ~/.vim/pack/tpope/start`
`git clone https://tpope.io/vim/sensible.git`

# RUBY
`brew install rbenv ruby-build`

`echo 'eval "$(rbenv init -)"' >> ~/.zshrc`
`source ~/.zshrc`
`sudo chown -R $(whoami) $(brew --prefix)/*`

`rbenv install 2.6.3`
`rbenv global 2.6.3`
`ruby -v`
`rbenv versions`
`rbenv version`

# BUNDLER
`which gem`
`gem install bundler`

# RAILS
`gem install rails`
`rbenv rehash`
`rails -v`

# POSTGRESQL
`brew install postgresql`
`brew services start postgresql`
`brew services restart postgresql`

# YARN
`brew install yarn`
`echo 'PATH="$PATH:/opt/yarn-[version]/bin"' >> ~/.zshrc`
`yarn --version`

# HEROKU
`brew tap heroku/brew`
`brew install heroku`

# VSC
Code > Preferences > Settings
```
{
  "editor.tabSize": 2,
  "editor.rulers": [80],
  "files.insertFinalNewline": true,
  "files.trimTrailingWhitespace": true,
  "workbench.editor.enablePreview": false
}
```

# TEST
`rails new testapp -d postgresql`
`cd testapp`
`rake db:create`
`rails server
