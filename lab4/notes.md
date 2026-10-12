# Lab 4 Notes

## Question 1: Meaning of --global in git config and omitting it
The --global flag configures Git settings globally for your entire user account across all repositories on the machine. Omitting it applies the configuration only to the specific repository you are currently working inside.

## Question 2: Contents of .git revealed by ls -a
The .git directory contains all metadata and the object database for the repository, including commit history, branch pointers, and configuration files. Running ls -a reveals hidden files and folders, showing this core directory alongside standard project files.

## Question 3: Approximate untracked file count and identifying untracked code
Untracked files are new files in your directory that Git is not yet monitoring or tracking in version control. You can identify them by running git status, which lists them under a specific section for untracked files.

## Question 4: Difference in git status after creating .gitignore
After creating a .gitignore file, git status stops listing the specified ignored files and folders as untracked files. This keeps the status output clean by hiding temporary files you do not want to commit to version control.

## Question 5: Why .gitignore itself should be committed rather than ignored
The .gitignore file should be committed to the repository so that all collaborators share the exact same rules for which files to ignore. If it were ignored, other team members would still see untracked clutter in their local environments.

## Question 6: Movement of README.md across sections in git status (three-places model)
In Git's three-places model, a new README.md starts as an untracked file in the working directory. Running git add moves it to the staging area, and committing moves it into the permanent local repository history.

## Question 7: Output produced by git commit and count of changed files
Running git commit produces a confirmation message displaying the branch name, short commit hash, commit message, and a summary line counting changed files and insertions/deletions. This count indicates how many files were modified and how many lines of code were added or removed.

## Question 8: Name and purpose of the first seven characters of a commit hash
The first seven characters of a commit hash are commonly referred to as the short hash or abbreviated commit SHA. Their purpose is to uniquely identify a specific commit in commands like git log or git show without needing to type out the full 40-character string.

## Question 9: The 4 steps of the repetitive Git loop
The repetitive Git workflow loop consists of editing or creating files in the working directory, staging those modifications using git add, saving them permanently with git commit, and optionally sharing them via git push. This cycle repeats continuously as software development progresses.

## Question 10: Special purpose and placement of README.md
A README.md file serves as the primary introduction and documentation page for a project, typically placed in the root directory. When someone visits the repository, platforms like GitHub automatically render this file to explain what the project does, how to install it, and how to use it.

## Question 11: How gh auth login eliminates future password prompts
The gh auth login command authenticates your GitHub CLI tool using a secure token or browser-based OAuth flow instead of your account password. This securely stores credentials locally, allowing future Git pushes and operations to authenticate automatically without repeated password prompts.

## Question 12: File rendered on GitHub's front page and the reason why
GitHub automatically renders the root README.md file on a repository's front page to provide instant documentation and project context to visitors. Developers rely on this convention so users immediately understand the project's purpose and instructions upon arrival.

## Question 13: Effect of git push on local history
Executing git push uploads your local commits and branch history to a remote repository like GitHub without altering your local history. It synchronizes the remote server with your local state, ensuring your changes are safely backed up and shared.

## Question 14: Distinction between a private repository vs. no repository on GitHub
A private repository on GitHub securely hosts your code and version history while restricting access solely to you or explicitly authorized collaborators. Having no repository means your project code exists only locally on your machine with zero cloud backup or remote version control collaboration features.
