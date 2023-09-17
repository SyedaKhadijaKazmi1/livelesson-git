# Git Notes

## Working with git locally

- 'git init': initialize current folder as a git repository
- 'git clone <URL>': brings the git repo from <URL> to current folder
- 'git status': tells us what we need to know about our repository
- 'git add <FILE>': adds <FILE> to the staging area
- 'git commit': open a text editor to write commit message
    - 'git commit -m "MESSAGE"': writes MESSAGE as a commit without a text editor

- 'git log': shows the log (history) of our commits
    - 'git log --oneline': shows the shorter oneline commit
- 'git diff': compare current uncommited state with last known git state
    - 'git diff --staged': runs git diff between the staging area and last known state
- 'git diff HEAD~<NUMBER>': compares HEAD with commit <NUMBER> ago (relative)
- 'git diff <HASH>': compares HEAD with the commit in <HASH> 

- 'git restore --source <HASH OR HEAD~> <FILE>': restore file to <HASH OR HEAD~>
   - 'git checkout <HASH OR HEAD~> <FILE>': restores file to <HASH OR HEAD~>
   - 'git checkout main': go back to main
   - 'git switch main': go back to main

## Working with remotes

- 'git remote add <NAME> <URL>': adds the <URL> as a remote with the name <NAME>
   - <NAME> is by convention called 'origin'
- 'git remote rm <NAME>': removes the remote called <NAME> 
- 'git remote -v': look at all the remotes you have
- 'git push <WHERE> <WHAT>': pushes the <WHAT> branch to <WHERE>
  - 'git push origin main'
- 'git pull <WHERE> <WHAT>': pulls the <WHAT> branch in <WHERE> to local computer

## Branches

- 'git branch <NAME>': create branch <NAME> where you are (HEAD)
- 'git switch <NAME>': move to the branch <NAME>
  - 'git checkout <NAME>': also move to the branch <NAME>
- 'git switch -c <NAME>': create and move to the branch <NAME> in 1 command
  - 'git checkout -b <NAME>': also create and move to branch <NAME> in 1 command

- 'git merge <BRANCH>': merge <BRANCH> into your current branch
- 'git rebase': command to change the history of a commit
  - Commits from 'git merge' can be automatically combined 
- 'git rebase <BRANCH>': incorporate changes from <BRANCH> into current branch
  - 'git status': is your friend
  - 'git add <FILE>': to mark conflict resolution
  - 'git rebase --continue': move to next commit in rebase
  - 'git rebase --abort': undo git rebase step

