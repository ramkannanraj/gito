# gito


## Stashes. 		

``` git stash save "stash name" &&  git stash ```  Save changes to a stash. 	
  
``` git stash list ```  	List all stashes. 	
  
``` git stash show ``` NAME-OF-STASH
  
``` git stash apply STASH-NAME ``` applies the changes and leaves a copy in the stash
  
``` git stash pop  STASH-NAME ``` 	Apply a stash and delete it from stash list.


## Undo


```  git reset --hard HEAD``` Discard all local changes in your working directory

```  git checkout <file>``` Discard local changes in a specific file

```  git revert <commit>``` Revert a commit (by producing a new commit with contrary changes)

```  git reset --hard <commit>``` Reset your HEAD pointer to a previous commit & discard all changes since then

```  git reset <commit>``` Reset your HEAD pointer to a previous commit & preserve all changes as unstaged changes

```  git reset --keep <commit>``` Reset your HEAD pointer to a previous commit & preserve uncommitted local changes


## Cleanup. 	
	
``` git clean -f ```	Delete all untracked files. 	

``` git clean -df ```	Delete all untracked files and directories. 	

``` git checkout -- .``` 	Undo local modifications to all files. 	

``` git reset HEAD myfile ```	Unstage a file.


  ## Tags 
  
``` git pull --tags ``` 	Get remote tags. 	
  
``` git checkout tag_name ``` 	Switch to an existing tag. 	
  
``` git tag ``` 	List all tags. 	
  
``` git tag -a tag_name -m "tag message" ``` 	Create a new tag. 	
  
``` git push --tags ``` 	Push all tags to remote repo. 	


## Logs. 		

``` git log --oneline ``` 	Show commit history in single lines. 	

``` git log -2 ``` 	Show commit history for last N commits. 	

``` git log -p -2 ``` 	Show commit history for last N commits with diff. 	

``` git diff ``` 	Show all local file changes in the working tree. 	

``` git diff myfile ``` 	Show changes made to a file. 	

``` git blame myfile ``` 	Show who changed what & when in a file. 	

``` git remote show origin ``` 	Show remote branches and their mapping to local.


## Create


``` git clone ssh://user@domain.com/repo.git ``` Clone and Existing Repository

``` git init ``` Create a new local repository  


## Local Changes

Changed files in your working directory
``` 
git status  
```
Changes to tracked files
 ```  
git diff  
```
Add all current changes to the next commit
```  
git add .  
```
Add some changes in <file> to the next commit
``` 
git add -p <file>
```
Commit all local changes in tracked files
```  
git commit -a  
```
Commit previously staged changes
```  
git add -p <file>  
```
Add some changes in to the next commit
```  
git commit  
```

Change the last commit
Don‘t amend published commits!

```  
git commit --amend   
```

## Branching & Tags

List all existing branches

```  
git branch 
```

Switch HEAD branch

```  
git checkout <branch>
```

Create a new branch based on your current HEAD

```  
git branch <new-branch>
```

Create a new tracking branch based on a remote branch

```  
git checkout --track <remote/branch>
```

Delete a local branch

```  
git branch -d <branch>
```

Mark the current commit with a tag

```  
git tag <tag-name>
```

  
  ## Update & Publish

List all currently configured remotes

``` git remote -v```

Show information about a remote

```  git remote show <remote>```

Add new remote repository, named <remote>

```  git remote add <remote> <url>```

Download all changes from <remote>, but don‘t integrate into HEAD

```  git fetch <remote>```

Download changes and directly merge/integrate into HEAD

```  git pull <remote> <branch>```

Publish local changes on a remote

```  git push <remote> <branch>```

Delete a branch on the remote

```  git branch -dr <remote/branch>```

Publish your tags

```  git push --tags```
  
  
## Merge & Rebase

Merge <branch> into your current HEAD

```  git merge <branch>```

Rebase your current HEAD onto <branch>
Don‘t rebase published commits!

```  git rebase <branch>```

Abort a rebase

```  git rebase --abort```

Continue a rebase after resolving conflicts

```  git rebase --continue```

Use your configured merge tool to solve conflicts

```  git mergetool```

Use your editor to manually solve conflicts

```  git add <resolved-file>```

After resolving mark file as resolved

```  git rm <resolved-file>```



  
