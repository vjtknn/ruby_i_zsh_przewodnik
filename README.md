# Jak zainstalować zsh i skonfigurować z Ruby

## 1. Zainstaluj zsh
```bash
sudo apt-get install zsh
```

## 2. Sprawdź czy zsh na pewno się zainstalowało
```bash
zsh --version
```
## 3. Zmień domyślną powłokę na zsh
```bash
chsh -s $(which zsh)
```
## 4. Zamknij termina i otwórz go na nowo

## 5. Sprawdź czy po ponownym otworzeniu terminalu domyślną powłoką jest zsh
```bash
echo $SHELL
```

## 6.1 Jeżeli kożystasz z rbenv dodaj
```bash
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(rbenv init -)"' >> ~/.zshrc
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.zshrc
```

## 6.2 Jeźeli kożystasz z rvm dodaj
```bash
echo '[[ -s "$HOME/.rvm/scripts/rvm" ]] && . "$HOME/.rvm/scripts/rvm" "' >> ~/.zshrc

```

## 7. Zainstaluj oh-my-zsh
### via curl
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
### via wget
```bash
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```


