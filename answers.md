# Git exo — Answers

## Part 1: Setup & config
- Git version: `2.52.0`
- Config commands used:
  - git config --global user.name "AmineBenbachir"
  - git config --global user.email "b00821087@essec.edu"

## Part 2: Create Your First Repository
Commands used:
- mkdir my-first-repo
- cd my-first-repo
- git init
- touch readme.txt

## Part 3: Your First Commit

- Command that shows the current state of the repository:
  - git status
- Command that stages readme.txt for commit:
  - git add readme.txt
- Command that commits with the message "Add readme file":
  - git commit -m "Add readme file"
- Command that shows the commit history:
  - git log

## Part 4: Make Changes

After editing readme.txt, git status showed that the file had been modified
but the changes were not staged yet. This means Git detected the update,
but it would not be included in a commit until it was added to the staging area.

Number of commits so far: 5

## Part 5: Exploration

- git diff:
  Displays the differences between the working directory and the last commit.
  It helps check what changed before creating a new commit.

- git log --oneline:
  Displays a compact version of the commit history with one commit per line,
  including a short commit hash and the associated message.

## Part 6: Working with Branches

- Command to list all branches:
  - git branch
- Command to create a new branch called feature-script:
  - git branch feature-script
- Command to switch to feature-script:
  - git switch feature-script
- Command to create and switch to a new branch called dev:
  - git switch -c dev
- Command to switch back to feature-script:
  - git switch feature-script
- To verify the current branch:
  - git status or git branch

## Part 7: Bash Script on a Branch

- Created install.sh on the feature-script branch
- Added a shebang line
- Printed a start message and an end message
- Updated package lists and installed a package
- Made the script executable
- Committed the script on the feature branch

## Part 8: Merge Branches

Before merging, install.sh was not present on main because it had been created on the feature-script branch.
After merging feature-script into main, install.sh appeared in the directory.
The commit history then included commits coming from both branches.
The feature-script branch was deleted after the merge.

## Part 9: Push to GitHub

- Command that links local repo to GitHub:
  - git remote add origin https://github.com/AmineBenbachir/my-first-repo.git
- Command that pushes commits to GitHub:
  - git push -u origin main

After refreshing GitHub, I could see the files and the commit history on the repository page.

## Part 10: Delete and Clone

- Command to delete the local repository folder:
  - rm -rf my-first-repo
- Command to clone the repository from GitHub:
  - git clone https://github.com/AmineBenbachir/my-first-repo.git

After cloning, I moved into the folder and checked that the files were present using ls.
