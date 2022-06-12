# Git commit

## Setup

- Checkout remote branch `01-commit-practice`

```shell
git checkout -b 01-commit-practice origin/01-commit-practice
```

> project branch changed to 01-commit-practice

## Commit

- Create a new file in a project folder for example with `touch` command if you are running **Linux/Mac-OS**

```shell
touch test
```

- If you are using **Windows** you can create an empty file with `copy` command:

```powershell
copy NUL test
```

- Run `git status` to check the state of the repository 

```shell
git status
```

![img.png](images/commit_01.png)

> File marked ass untracked

- Add created untracked file to the git index with `git add FILE_NAME` command:

```shell
git add test
```

- Check operation with `git status`

![img.png](images/commit_02.png)

> File marked as ready to be committed

- Save changes in local git repository with `git commit` command:

```shell
git commit
```

> Default text edit will be open, you need to add a commit message and save the file to perform commit:

![img.png](images/commit_03.png)

> `vi` press `ESC` to exit from edit mode, write `:wq` to save commit message and exit

> `emacs` press `CTRL` + `S` to save message and then `CTRL` + `C` to exit editor

- Use `git status` to check the operation result:

```shell
git status
```

![img.png](images/commit_04.png)

- Push commit to the remote repository with `git push` command:

```shell
git push
```

![img.png](images/commit_05.png)

- Add 2 new files to the project folder with `touch` command if you are running **Linux/Mac-OS**

```shell
touch test_file_1
touch test_file_2
```

- If you are using **Windows**, use `copy` command to create empty files:

```powershell
copy NUL test_file_1
copy NUL test_file_2
```

> Created files are not added to git, check it with `git status` command:

```shell
git status                                                                                                                                     
```

![img.png](images/commit_06.png)

- Add both files to git index, this time we will add all files with `git add .` command:

```shell
git add .
```

![img.png](images/commit_07.png)

> We can use `git add --all` or `git add -A`
> Both files added to index

- Commit files with the message by `git commit -m "COMMIT_MESSAGE"` command:

```shell
git commit -m "Added test files"
```

![img.png](images/commit_08.png)

- Push files to remote repository with `git push` command

```shell
git push
```

### Commit with staging

- Make some changed in `commit_file_1` and `commit_file_2` files (Add some text for example)

Try to run git commit without adding files to staging

```shell
git commit -m "Stage files"
```

> Files was not committed, use `git status` command to check file status: 

```shell
git status
```

![img.png](images/commit_09.png)

- Add all files to the stage and then commit at once with `git commit`:

```shell
git commit -a -m "Added no stage file"
```

> Check that files was committed
> This command will work only with files previously added to git index

```shell
git status
```

### Rephrase last commit

- Add another change to `commit_file_1`
- Commit file with error message

```shell
git commit -am "Stage commit_file_xxxxxx"
```

- Check the last commit with `git log` command:

```shell
git log --oneline -1
```

![img.png](images/commit_10.png)

- We can change the commit message of last commit:

```shell
git commit --amend -m "New corrected commit message"
```

- Check the last commit:

```shell
git log --oneline -1
```

![img.png](images/commit_11.png)

## Navigation

[<<< git merge](../01_branching/README.md) |
[git merge >>>](../03_merge/README.md)
