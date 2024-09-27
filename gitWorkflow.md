
# Git Workflow

In terminal

## Local version control

- Create directory
- `git status` 
    - Use this a lot to check where everything is at.
- `git init`
- `git status`
    - Confirm main branch.
- Create files
    - touch blahblahblah.py
- `git status`
    - Should see untracked file(s).
- `git add .` *or* `filename.py`
    - . adds all files in dir. 
- Optionally create .gitignore file
    - This contains files to exclude from the git add command.
    - Use nano to add one file name per line
- `git commit -m "message"`
    - Won't commit w/o message.
    - git commit will open VS Code to finish the message. CLI is quicker.
    - git commit -am "message" performs add and commit together.

## Remote/GitHub version control

- git remote
    - Tells if you're on a remote branch.
- git remote -v
    - Checks for remote connection. No response means no connection.
- Create new repo in GitHub. Copy HTTPS URL. 
- git remote add origin, *URL*
    - Origin if starting new, could be another branch if making changes.
- git remote -v
    - Should now show fetch and push branches and URLs.
- git push -u origin main
    - This connects main branch (local) with origin (remote).
    - -u sets upstream link that allows future pushes w/o specifying branches each time.
- git push
    - Pushes commits to remote branch after initial -u setup.

***For pulling files down from remote branch***
- git fetch
    - Gets info, but doesn't put repos in my work area.
- git pull *or* git pull origin main
    - Adds everything into working area.
    - Like doing fetch and merge at once.
