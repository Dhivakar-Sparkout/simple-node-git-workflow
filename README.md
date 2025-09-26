# Simple Node.js Project with Git Workflow

This project demonstrates a simple Node.js app along with a **Git workflow**, including initializing a repository, committing changes, creating feature branches, merging, and pushing to a remote repository.

---

## Project Setup

1. **Initialize Node.js project**

```bash
npm init -y
```

2. **Create a simple file**

```bash
echo "console.log('Hello World');" > index.js
```

---

## Git Commands Used

### Initialize Git Repository

```bash
git init
```

* Initializes a new Git repository in the current folder.

### Check Status

```bash
git status
```

* Shows the state of the working directory and staging area.

### Commit Changes

```bash
git add .
git commit -m "initialize commit: Setup Node.js project with index.js"
```

* Commits staged changes with a meaningful message.

### Make More Changes and Commit

```bash
# Add a greeting function
echo "function greet(name) { console.log('Hello, ' + name); } greet('Git');" >> index.js
git add index.js
git commit -m "Add greet function in index.js"

# Add start script to package.json
npm pkg set scripts.start="node index.js"
git add package.json
git commit -m "Add start script to package.json"
```

---

## Branching

### Create a Feature Branch

```bash
git checkout -b feature-logging
```

* Creates and switches to the branch `feature-logging`.

### Make Changes in the Branch

```bash
echo "console.log('Logging feature enabled');" >> index.js
git add index.js
git commit -m "Add logging feature"
```

### Switch Back to Main Branch

```bash
git checkout master
git branch -M main
```

* Renames `master` to `main` and switches to it.

---

## Merging Branches

```bash
git merge feature-logging
```

* Merges the `feature-logging` branch into `main`.
* Fast-forward merge occurs if no conflicts exist.

---

## Remote Repository Setup

### Add a Remote Repository

```bash
git remote add origin https://github.com/Dhivakar-Sparkout/Simple-node-app.git
```

### Push Main Branch

```bash
git push origin main
```

* Pushes local `main` branch to the remote repository.

### Push Feature Branch and Set Upstream

```bash
git push -u origin feature-logging
```

* Pushes the `feature-logging` branch to remote and sets it to track the upstream branch.

---

## Run Project

```bash
npm start
```

* Runs `index.js` using Node.js.

---

## Summary

This workflow demonstrates:

1. Initializing a Git repository.
2. Staging and committing changes.
3. Creating and working with feature branches.
4. Merging branches.
5. Pushing branches to a remote repository.
6. Running the Node.js project.
