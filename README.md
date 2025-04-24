# 🚀 Git Assignment Guide

## 📋 Project Description
This repository contains a step-by-step implementation of various Git workflows and features. The project includes a basic calculator application with arithmetic operations, a geometry calculator for calculating areas of different shapes, and demonstrates Git LFS for handling large files. This assignment showcases best practices for branching, merging, collaboration, and version control.

## 🛠️ Prerequisites
- ✨ Git installed on your local machine
- 🌐 GitHub account
- 🐍 Basic knowledge of Python
- 📦 Git LFS installed (for Question 2)
- 💻 Access to terminal or command prompt

## 📁 Project Structure
```
git_assignment_HeroVired/
├── .git/                  # Git repository data
├── .gitattributes         # Git LFS configuration file
├── calculator.py          # Basic calculator implementation
├── geometry_calculator.py # Geometry calculator implementation
└── README.md              # Project documentation
```

## 🌿 Branches
- 🟢 main (default)
- 🛠️ dev
- 🔴 feature/circle-area
- 📏 feature/rectangle-area
- 🧮 feature/sqrt
- 📐 geometry-calculator
- 📦 lfs

## ✅ Question 1: Setup & Basic Git Workflow

### 📝 Create a GitHub Repository
- Name: `git_assignment_HeroVired`
- Visibility: Private
- Initialize with README

### 📥 Clone to Local Machine
```bash
git clone https://github.com/yourusername/git_assignment_HeroVired.git
cd git_assignment_HeroVired
```

### 🌱 Create Development Branch
```bash
git checkout -b dev
```

### 💻 Add Calculator Code
Add `calculator.py` with basic arithmetic operations.

### 📤 Commit & Push Changes
```bash
git add .
git commit -m "Added initial calculator code"
git push origin dev
```

### 🔄 Merge & Tag Release v1.0
```bash
git checkout main
git merge dev
git push origin main
git tag v1.0
git push origin v1.0
```

### 👥 Add a Collaborator
Invite ranyabrkumar via Settings → Collaborators → Add people.

## 🧮 Add Square Root Feature
```bash
git checkout -b feature/sqrt
```
Add `square_root` method, test it, commit, and push.

## 🐛 Fix Bug in Dev Branch
Fix divide by zero error in `dev`, commit, and push.

## 🔄 Update Feature Branch
Merge dev into `feature/sqrt` and push.

## 🔀 Create Pull Request
Create PR from `feature/sqrt` → `dev`. Add ranyabrkumar as reviewer.

## 🔀 Merge to Dev After Approval
Merge after ranyabrkumar's review and push.

## 🏷️ Release v2.0
```bash
git checkout main
git merge dev
git push origin main
git tag v2.0
git push origin v2.0
```

---

## 📦 Question 2: Git LFS for Large Files

### 💿 Install Git LFS
```bash
git lfs install
```

### 🗃️ Setup Repository for LFS
```bash
git checkout -b lfs
git lfs track "*.zip"
git add .gitattributes test.zip
git commit -m "Added large file using Git LFS"
git push origin lfs
```

### ✅ Verify LFS Tracking
```bash
git lfs ls-files
```

### 🧪 Test Clone on Another Machine
Clone and use `git lfs pull` to download large files.

---

## 📐 Question 3: Geometry Calculator with Feature Branches

### 🏗️ Initial Setup
```bash
git checkout dev
git checkout -b geometry-calculator
```
Create `geometry_calculator.py` with shape area methods.

### ⭕ Circle Area Feature
```bash
git checkout -b feature/circle-area
```
Add circle area code, stash, commit, and push.

### 📏 Rectangle Area Feature
```bash
git checkout -b feature/rectangle-area
```
Add rectangle area code, stash, commit, and push.

### 🔀 Create Pull Requests
- feature/circle-area → dev
- feature/rectangle-area → dev

### 👀 Code Review
Add ranyabrkumar for PR reviews, respond to feedback.

### 🚀 Final Integration
```bash
git checkout main
git merge dev
git push origin main
```

---

## 📋 Workflow Summary
| Step | Command | Purpose |
|------|---------|---------|
| 📥 Clone repository | `git clone` | Get local copy |
| 📐 Create calculator branch | `git checkout -b geometry-calculator` | Base branch |
| ⭕ Create circle feature | `git checkout -b feature/circle-area` | Feature branch |
| 💾 Save circle changes | `git stash` | Store temporarily |
| 📏 Create rectangle feature | `git checkout -b feature/rectangle-area` | Feature branch |
| 💾 Save rectangle changes | `git stash` | Store temporarily |
| ⭕ Complete circle feature | `git checkout feature/circle-area && git stash pop` | Resume work |
| 📤 Push circle feature | `git push origin feature/circle-area` | Share with team |
| 📏 Complete rectangle feature | `git checkout feature/rectangle-area && git stash pop` | Resume work |
| 📤 Push rectangle feature | `git push origin feature/rectangle-area` | Share with team |
| 👀 Review & merge | Pull Requests | Quality control |
| 🚀 Release | Merge to main | Production ready |

---

## 📊 Expected Output
```
The area of the circle with radius 5 = 78.53981633974483
The area of the rectangle with length 10 and width 6 = 60
```

---

## 🤝 Collaboration
In collaboration with ranyabrkumar 👩‍💻

Throughout this project, I've worked closely with ranyabrkumar to implement the Git workflow and features. ranyabrkumar has:
- 👀 Reviewed my pull requests for the calculator features
- 💬 Provided feedback on my code implementation
- 🧪 Helped test the geometry calculator functionality
- 📦 Collaborated on the Git LFS setup

This collaboration demonstrates effective teamwork using Git's branching and review features, allowing us to work independently while maintaining code quality through peer reviews. 🌟

