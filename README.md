# 2020/06/16 SWC git workshop for UD

## Local

- `git init`: create a git repository in the current directory
- `git status`: tells you what is going on
- `git add <FILENAME>`: adds <FILENAME> to the staging area (aka index)
- `git commit`: opens up nano, commits the files in staging with a message
- `git log`: shows the history of commits we have done
    - `git log --oneline`: shows a shorter oneline version of `git log`
- `git diff`: compare current state to last known git state
    - `git diff HEAD~1 <FILE>`: compares current state from 1 state ago
    - `git diff <HASH> <FILE>`: compares current state form state in <HASH>
    - `git diff --staged <FILE>`: comparing differences when files are in the staging area
- `git checkout <HASH> <FILE>`: reverts the <FILE> from <HASH> back to your current state
- `git checkout <HASH>`: revert entire folder state to <HASH>
    - `git checkout master`: to go back to your latest work
- `HEAD`: this tells you where you are looking at in history

## Remotes

- `git remote add <name> <url>`: gives the remote URL a short NAME
- `git push <where> <what>`: e.g., `git push origin master` takes the master branch on your local computer and pushes it to the origin location (e.g., github)
- `git pull <where> <what>`: e.g., `git pull origin master` takes the remote master branch, and brings it to our local master branch

## Conflicts

- You can have multiple people (yourself included) work on the same file and at the same place
- Git will either automatically resolve the differences or show you a conflict.

- You won't know there will be a conflict, until you run `git pull` when the remote and your local computer is out of sync
    - It will either auto merge the changes
    - Or show you which files have a conflict.
        - You open the file and manually look for the `>>>`, `===`, and `<<<` and fix the file until you are satisfied.
        - You can then `git add` and `git commit` your changes and re `git push`

