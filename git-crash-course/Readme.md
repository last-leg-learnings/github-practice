## Git hidden folder

Hidden `.git` folder that tells project is git repo. 
To create git repo in new project make folder and init repo with `git init`
Make tmp dir in codespaces workdir

```mkdir /workspace/tmp 
cd /workspace/tmp
git init 
touch Readme.md
code Readme.md #make changes to Readme.md
git add Readme.md 
git commit -a -m "Add Readme file"
```

## Clone 
>clone by HTTPS, SSH, Github CLI

### HTTPS
```sh
git clone https://github.com/last-leg-learnings/github-practice.git
```
>gen a personal access token (PAT) as password for login - permissions - content and commits. not needed in gitbash - probably better 

### SSH
```ssh 
git@github.com:last-leg-learnings/github-practice.git
```
>create an ssh key 

#### Generate SSH Key  
```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```
#### 
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```
#### 
```bash 
cat ~/.ssh/id_ed25519.pub
```
>copy key

#### 
```bash 
ssh -T git@github.com
```
>test connection and then ready to push 

### Github CLI 

Install CLI on windows

```cmd 
winget install --id GitHub.cli
```

## Commits
>opens up commit_editmsg in the default editor of choice - have to configure for local setup unlike codespaces
```sh
git commit
```
Set global editor
```sh 
git config --global core.editor emacs
```
Make commit without opening editor 
```sh
git commit -m "msg"
```
## Branches
## Remotes
## Staging 
## Merging 
## Status
```sh 
git status
```
>shows what files will or will not be committed
## Git config
> .gitconfig stores global config for git like username, email, editor, etc.
```sh 
git config --list  
```
>shows file content
First installation configs
```sh 
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## Log 

git log will show recent git commits to git tree 

```sh
git log 
```

## Add
```sh 
git add Readme.md
git add .
```
## Reset 

```sh 
git add .
git reset
```
>unstage staged changes;
>git reset reverts a git add .

## Push 

push repo to remote origin 
```sh git push```