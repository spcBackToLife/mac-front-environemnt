# mac-front-environemnt
每次换了系统后，总是需要自己去重新安装前端开发环境十分麻烦，在这里对过程做个记录。

## 基本工具安装
### brew

1. 安装指令

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
### iterm2

1. 安装：

```
brew cask install iterm2
```

2. 安装：`on-my-zsh`
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

3. 主题：http://iterm2colorschemes.com/
  - 左上角 - iterm2 - perferences - Profiles - colors 右下角：color presets - import 从上面官网下载的文件
 

### autojump

1. 安装
```
  brew install autojump
```
2. 添加到: ~/.zshrc

```
[[ -s $(brew --prefix)/etc/profile.d/autojump.sh ]] && . $(brew --prefix)/etc/profile.d/autojump.sh
source $ZSH/oh-my-zsh.sh
```
3. 添加到～/.zshrc
```
# 已添加则不用加
plugins=(
	git
	zsh-syntax-highlighting
	zsh-autosuggestions
	autojump
)
```

4. source ~/.zshrc
### autosuggestion

1. 安装(必须先安装item2 和 Oh-my-zsh)
```
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

2. 添加到～/.zshrc
```
# 已添加则不用加
plugins=(
	git
	zsh-syntax-highlighting
	zsh-autosuggestions
	autojump
)
```

### 

1. 安装(必须先安装item2 和 Oh-my-zsh)
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
2. 添加到～/.zshrc
```
# 已添加则不用加
plugins=(
	git
	zsh-syntax-highlighting
	zsh-autosuggestions
	autojump
)
```



### git、nvm + node、yarn 
1. git 

```
  brew install git
```

- 配置 git 常用快捷命令、配置 git 的账号

  ```
    vim ~/.gitconfig 
  ```

  复制：

  ```
  [user]
    name = xxx
    email = xxx
  [credential]
    helper=manager
  [alias]
    b = branch
    s = status
    co = checkout
    lg = log --oneline --decorate --all --graph
  ```




2. nvm

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.29.0/install.sh | bash
```

3. node 

```
  nvm install v12.13.0 // 可自行下载相应版本
```

- 切记不要去官网下载node，容易在npm安装依赖的时候存在权限问题

4. yarn 

```
npm install -g yarn 
```
