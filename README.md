**Name:** Karolina Dąbrowska

**Date:** 22.11.2003

 Assignment about Git and GitHub for a BT4BR class.

## What is Git

Git is a version-control tool that tracks changes made to the files and directories in a project.

## Why is Git useful

Git helps us:
- Track changes made to files.
- Return to earlier versions of a project.
- Work on different versions using branches.
- Collaborate with other people.

## How does Git work

Git saves snapshots of the project when we create commits. Each commit represents a saved version of our work.

This makes it possible to:
- See the history of changes.
- Return to an earlier version.
- Create branches to work on different ideas.
- Combine changes from different branches.

## First time using Git

Before using Git, we should configure our username and email address. This information is connected to our commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

To check the configuration:
```bash
git config --list
```

## Creating repository on Github

To create a new repository:

1. Open [GitHub](https://github.com).
2. Sign in to your account.
3. Click the **New repository** button.
4. Enter a repository name.
5. Add a short description if needed.
6. Choose whether the repository should be public or private.
7. Click **Create repository**.

A repository is a place where project files and their version history are stored.

## Connecting Your Computer to GitHub Using SSH

SSH keys allow us to connect to GitHub securely.

First, check whether you already have SSH keys:

```bash
ls -al ~/.ssh
```

To create a new SSH key:

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

To display your public key:

```bash
cat ~/.ssh/id_ed25519.pub
```

Copy the public key and add it to GitHub:

1. Open GitHub **Settings**.
2. Go to **SSH and GPG keys**.
3. Click **New SSH key**.
4. Paste your public key.
5. Save the changes.

## Creating a Local Copy of a Repository

To download an existing repository from GitHub to your computer, use `git clone`.

```bash
git clone repository-address
```

This creates a local copy of the repository.

After cloning, enter the repository folder:

```bash
cd repository-name
```

## Adding Files to a Repository

After creating or editing files, we can add them to the staging area.

First, check the current status:

```bash
git status
```

To add one specific file:

```bash
git add README.md
```

To add all changed files:

```bash
git add .
```

The staging area allows us to choose which changes will be included in the next commit.

## Committing Changes

A commit saves the staged changes as a new version in the Git history.

To create a commit:

```bash
git commit -m "Describe your changes"
```

A commit message should briefly explain what was changed.

For example:

```bash
git commit -m "Add information about Git commands"
```

## Pushing Changes to GitHub

The `git push` command sends local commits to the remote repository on GitHub.

```bash
git push
```

This allows us to update the online repository with our latest changes.

## Branching and Merging

A branch is a separate line of development. It allows us to work on a new feature or idea without changing the main version of the project immediately.

To display existing branches:

```bash
git branch
```

To create a new branch:

```bash
git branch new-branch
```

To switch to another branch:

```bash
git checkout new-branch
```

Merging combines changes from one branch into another.

For example, to merge `new-branch` into `main`:

```bash
git checkout main
git merge new-branch
```

## Restoring Previous Versions

Git allows us to recover earlier versions of files or undo unwanted changes.

Before restoring anything, it is useful to check the repository status and commit history.

```bash
git status
git show
```

The `git show` command displays information about a commit, including the changes it contains.

It is important to understand what changes we want to undo before restoring files, because some operations can overwrite current work.

## Pulling changes from GitHub

The `git pull` command downloads changes from a remote repository and integrates them into the current local branch.

```bash
git pull
```

The `git fetch` command downloads information about changes from the remote repository but does not automatically integrate them into the current branch.

```bash
git fetch
```

**The main difference:** `git pull` also integrates the downloaded changes, while `git fetch` only retrieves them.

## Basic Git commands

| Command | Description |
|---|---|
| `git init` | Creates a new local Git repository. |
| `git status` | Shows the current status of the repository. |
| `git add` | Adds changes to the staging area. |
| `git commit` | Saves staged changes. |
| `git push` | Sends commits to a remote repository. |
| `git clone` | Creates a local copy of a repository. |
| `git branch` | Displays or creates branches. |
| `git checkout` | Switches between branches. |
| `git merge` | Combines changes from different branches. |
| `git pull` | Downloads and integrates remote changes. |
| `git fetch` | Downloads information about remote changes. |
| `git show` | Displays information about a commit. |

## Basic Bash commands

Bash commands are useful when working with files and directories in the Terminal.

| Command | Description |
|---|---|
| `cd` | Changes the current directory. |
| `mv` | Moves or renames files. |
| `cp` | Copies files. |
| `nano` | Opens a text editor in the Terminal. |
| `ls` | Lists files and directories. |
| `pwd` | Displays the current directory. |

## Markdown Formatting Cheat Sheet

Markdown is a simple language used to format text in files such as README.md. GitHub automatically displays Markdown formatting when we open a README file.

### Headings

Use the `#` symbol to create headings. The number of symbols determines the heading level.

```markdown
# Main heading
## Second-level heading
### Third-level heading
```

### Text Formatting

```markdown
**Bold text**
*Italic text*
~~Strikethrough text~~
```

### Lists

For a bullet list:

```markdown
- First item
- Second item
- Third item
```

For a numbered list:

```markdown
1. First step
2. Second step
3. Third step
```

### Links

To add a link:

```markdown
[GitHub](https://github.com)
```

### Code

To display a command inside a sentence, use one backtick on each side:

```markdown
`git status`
```

To display several commands in a separate code block, use three backticks before and after the commands.

For terminal commands, write `bash` after the opening backticks:

```bash
git status
git add README.md
git commit -m "Update README"
git push
```

### Blockquotes

To create a blockquote, use the `>` symbol:

```markdown
> This is an example of a blockquote.
```

### Task Lists

To create a task list:

```markdown
- [ ] First task
- [x] Completed task
```

### Horizontal Line

To create a horizontal line, use three hyphens:

```markdown
---
```

---

## Useful Resources

- [GitHub – Basic Writing and Formatting Syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Pro Git Book](http://book.git-scm.com/book/en/v2)
- [Git Training](https://ufresearchcomputing.github.io/git-training/)
- [Git Installation Guide](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

These resources provide additional information about Git, GitHub, version control and Markdown.

## Disclaimer

The information about Git, GitHub and Markdown in this README was prepared with the help of AI and other sources, such as GitHub documentation and other GitHub repositories.

I wrote the whole text myself, using these sources to help me understand the topics and prepare the guide.
