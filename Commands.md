## Git Commands For Professionals who used those daily

## GIT INITIALIZE A REPO OR CLONE

    - git init      : creates a new repository
    - git clone <Repo URL> : downloads an existing repo

## SETTING USER CONFIGS

    -   git config user.name "Your Name"
    -   git config user.email "your.email@example.com"
    -   git config --global user.name "Your Name"
    -   git config --global user.email "your.email@example.com"

## GETTING CONFIGS OF GIT   

    -   git config -l
    -   git config --get propertyName

## CHECKING THE GIT STATUS

    -   git status

## STAGE CHANGES :

    -   git add <file>
    -   git add .

## Commit Changes:

    -   git commit -m "Descriptive commit message"
    -   git commit -am "Message"  # Stages and commits tracked files in one step

## View Commit History:

    -   git log
    -   git log -oneline  # Shortened view
    -   git log --graph --oneline --all  # Visual branch graph

## Amend Last Commit :

    -   git commit --amend  # Edit message or add more changes

## Branching and Merging :

    -   git branch
    -   git branch -a  # Includes remote branches
    -   git branch <branch-name>   : creates a new branch 
    -   git checkout <branch-name>
    -   git switch <branch-name>
    -   git checkout -b <branch-name>   : Create and Switch to a Branch
    -   git switch -b <branch-name>   : Create and Switch to a Branch

## Merge a Branch:

    -   git checkout main
    -   git merge <branch-name>
    
## Delete a Branch:

    -   git branch -d <branch-name>  # Local, safe deletion
    -   git branch -D <branch-name>  # Force deletion
    -   git push origin --delete <branch-name>  # Remote deletion


## 4. Remote Operations :

    -   git remote add origin <repository-url>  : add a remote
    -   git remote -v   : list remotes
    -   git fetch origin    : fetch changes ( without merging )
    -   git pull origin <branch-name>   : (Fetch + Merge (or) pull)
    -   git push origin <branch-name>
    -   git push origin <branch-name> --force  # Overwrite remote (use with caution)
    -   git push --set-upstream origin <branch-name>
    -   git push -u origin <branch-name>  # Shorthand

## Stashing Changes :

    -   git stash  ( save uncommited changes)
    -   git stash push -m "Descriptive message"  # With a message 

    -   git stash list  ( List Stashes: )

    -   git stash apply  # Applies latest stash ( Apply a Stash: )
    -   git stash apply stash{1}  # Applies specific stash

    -   git stash drop stash{0}
    -   git stash clear  # Deletes all stashes

    -   git stash pop { Pop a Stash (Apply + Drop): }

## 7. Undoing Changes :

    -   Discard Unstaged Changes: git restore <file>     (or)   git checkout -- <file>  # Older command
    -   Unstage Changes:   git restore --staged <file>   (or)   git reset <file>  # Older command
    -   Reset to Previous Commit:   git reset --soft HEAD^  # Keeps changes in staging  (or)    git reset --hard HEAD^  # Discards changes completely
    -   Revert a Commit:    git revert <commit-hash>  # Creates a new commit undoing the specified one

## 8. Inspecting and Debugging :

    -   Show Changes: git diff  # Unstaged changes  (or) git diff --staged  # Staged changes (or) git diff <commit1> <commit2>  # Compare commits
    -   Blame (Who Changed What): git blame <file>
    -   Find a Commit: git log --grep="search term"  # Search commit messages

## Tagging Releases :

    -   Create a Tag: git tag v1.0.0  # Lightweight tag  (or)   git tag -a v1.0.0 -m "Release 1.0.0"  # Annotated tag
    -   Push Tags:  git push origin v1.0.0  (or)   git push origin --tags  # Push all tags 
    -   List Tags:  git tag
