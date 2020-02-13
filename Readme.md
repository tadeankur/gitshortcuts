# How to create git shortcuts using doskey utility on windows

## Sample git short shortcuts
Instead for writing `git` everytime on command prompt it's possible to use just shortcut g which will execute `git` command on the command prompt.
This is possible to due to doskey utility on windows. 
```
g=git 
ga=git add 
gaa=git add . 
gaaa=git add --all 
gau=git add --update 
gb=git branch 
gbd=git branch --delete 
gc=git commit 
gcm=git commit --message  
gcf=git commit --fixup 
gco=git checkout 
gcob=git checkout -b 
gcom=git checkout master 
gcos=git checkout staging 
gcod=git checkout develop 
gd=git diff 
gda=git diff HEAD 
gi=git init 
glg=git log --graph --oneline --decorate --all 
gld=git log --pretty=format:"%h %ad %s" --date=short --all 
gm=git merge --no-ff 
gma=git merge --abort 
gmc=git merge --continue 
gpu=git push 
gpl=git pull 
gplr=git pull --rebase 
gr=git rebase 
gs=git status 
gss=git status --short 
gst=git stash 
gsta=git stash apply 
gstd=git stash drop 
gstl=git stash list 
gstp=git stash pop 
gsts=git stash save
```

## Steps

**Note:** I have tested below mentioned steps on Windows 10. 

 1. Checkout Repo to your local directory
 2. Open to the registry editor using command `regedit`.
 3. Goto location  `HKEY_LOCAL_MACHINE\Software\Microsoft\Command Processor\`
 4. Right-click and add a new `"String Value"` sub-key. Name it `Autorun`.
 5. Value data ->    `DOSKEY /MACROFILE="<Repo path>\shortcuts.doskey"`
 6. Open command prompt and run command as `doskey /macros` and you should be able to see all the marcos.

# Referances :
1. Doskey : https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/doskey
2. Git Commands : https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf
3. Stackoverflow : https://superuser.com/questions/1134368/create-permanent-doskey-in-windows-cmd
4. Git shortcuts : https://jonsuh.com/blog/git-command-line-shortcuts/
