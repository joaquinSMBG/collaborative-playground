# collaborative-playground
This repository is used to show an example of usual collaborative workflows when more than one person works on the same repository, what happens when there is a merge conflict, and the possible ways to solve it.

In this exercise, you’ll simulate a real-world team workflow using Git. You’ll experience the good, the bad, and the frustrating parts of working in a team — all in a safe learning environment.

## What You'll Learn

* Cloning and branching
* Committing and pushing
* Creating pull requests
* Experiencing merge conflicts
* Solving them with git merge and git rebase
* Writing good commit messages

## Your Task

We're all going to work on a single file: `todo.txt`
This file is a shared to-do list for a fake project.

**Your goal:**
Add 1-2 task to the file on your own branch and submit a pull request. But you'll do it in a way that causes conflicts - and learn to resolve them?

## Steps
1. **Fork the repo** (on GitHub)
2. **Clone it** to your local machine
3. **Create a new branch** with your name or a feature

```bash
git checkout -b add-task-yourname
```

4. **Open todo.txt** and add 1-2 new to-do's **at the top of the list** (this guarantees conflict later).
5. **Commit your changes.**
6. **Push your branch to github**
7. **Open a pull request** on the main repository.

## Merge Conflict Simulation
To simulate a conflict, go back to the `main` branch, create a new branch, and perform the same steps to add changes and open a pull request. Merge the pull request and then go back to the first pull request created. You'll see that you can't merge because there exist conflict on `todo.txt`.

After that, on your machine:
1. Pull the latest main branch into your branch:

```bash
git fetch origin
git checkout main
git pull origin main

git checkout add-task-yourname
git merge main # or try git rebase main
```

2. You **will** get a merge conflict in todo.txt
3. Open the file, resolve the conflict manually, then:

```bash
git add todo.txt
git commit  # or git rebase --continue
```

## Merge vs Rebase
Try both methods on different attempts and compare:
* `git merge main` — creates a merge commit, keeps all history.
* `git rebase main` — rewrites history to create a linear timeline.

You’ll learn which one feels more intuitive (and when each is appropriate).
