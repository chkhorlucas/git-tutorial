# git-tutorial
## Git basics for beginners

1. Download git from https://git-scm.com/downloads.  
2. Install git.  
3. Open Terminal for Mac; command-prompt for Windows.  
4. Follow below instructions:  

5. Create a new folder.
```
$ mkdir git-tutorial
$ cd git-tutorial
```
6. Initialize repository to the folder.
```
$ git init
```

7. Create a readme file.
```
$ touch readme.txt
```

8. Check repository status and it will show that readme is untrack.
```
$ git status

On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	readme.txt

nothing added to commit but untracked files present (use "git add" to track)
```

9. Stage the readme for commit.
```
$ git add readme.txt
```

10. Check status and see a new file added.
```
$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   readme.txt
```

11. Type in some text inside the readme, save, and check status again. Notice there is 1 tracked item and 1 untrack item.
```
$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   readme.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   readme.txt
```

12. We have to stage our changes.
```
$ git add readme.txt
```

13. Check repository status again.
```
$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   readme.txt
```

14. Commit to the repository.
```
$ git commit
```

15. A screen will show up to let us key in commit message. Press ‘I’ into insert mode, and key in your commit message.
After inserting message, press ‘Esc’ to quit insert mode and key in ‘:wq’. Hit enter to finish commit.
```
[master (root-commit) 98abc39] initial commit
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
```
16. Or we can use a more simplified way.
```
$ git commit -m ‘initial commit’
```


16. View commit history.
```
$ git log
commit 98abc39a35ad3452dce145734c8328c19082d0dc
Author: lucas <chkhor86@gmail.com>
Date:   Fri Jun 16 22:51:16 2017 +0800

    initial commit
```

17. Create a new branch.
```
$ git branch MyBranch
```
18. Switch to the new branch.
```
$ git checkout MyBranch
Switched to branch 'MyBranch'
```
19. Changes made in MyBranch will not affect the master branch. To merge MyBranch into master, 1st switch to master branch.
```
$ git checkout master
Switched to branch 'master'
```

20. Merge destination branch into source branch(master).
```
$ git merge MyBranch
Updating 98abc39..a679d83
Fast-forward
 newfile.txt  | 0
 1 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 newfile.txt
```
