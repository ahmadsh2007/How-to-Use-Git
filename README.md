## Git & GitHub Guide

### 1. Uploading a Folder to GitHub Using Git

#### a. Install Git
- Download and install Git from [Git SCM](https://git-scm.com/).

#### b. Initialize a Local Repository
```sh
cd /path/to/your/folder
git init
```

#### c. Stage and Commit Files
```sh
git add .
git commit -m "Initial commit"
```

#### d. Create a GitHub Repository
- Log in to GitHub and create a new repository.

#### e. Link Local Repository to GitHub
```sh
git remote add origin https://github.com/username/repository.git
```

#### f. Push to GitHub
```sh
git branch -M main
git push -u origin main
```

#### g. Verify
- Check the repository on GitHub to confirm the upload.

---

### 2. Updating an Existing Repository

#### a. Make Local Changes
- Modify, add, or delete files as needed.

#### b. Check Repository Status
```sh
git status
```

#### c. Stage the Changes
```sh
git add .
```

#### d. Commit the Changes
```sh
git commit -m "Describe the changes"
```

#### e. Pull Latest Changes (if necessary)
```sh
git pull origin main
```

#### f. Push to GitHub
```sh
git push
```

#### g. Verify
- Check GitHub to confirm the updates.

---

### 3. Downloading (Cloning) a Repository

#### a. Clone the Repository
```sh
git clone https://github.com/username/repository.git
```

#### b. Navigate to the Cloned Repository
```sh
cd repository
```

#### c. Verify the Contents
```sh
ls  # Linux/Mac
dir # Windows
```

#### d. (Optional) Clone a Specific Branch
```sh
git clone --branch branch_name https://github.com/username/repository.git
```

#### e. Alternative: Download as ZIP
- Use GitHub’s "Download ZIP" option.

---

### 4. Switching Git Accounts

#### a. Check Current Configuration
```sh
git config --global user.name
git config --global user.email
```

#### b. Change Account for a Specific Repository
```sh
cd /path/to/your/repo
git config user.name "Your GitHub Username"
git config user.email "your.email@example.com"
```

#### c. Change Account Globally
```sh
git config --global user.name "Your GitHub Username"
git config --global user.email "your.email@example.com"
```

#### d. Using SSH for Multiple Accounts
```sh
ssh-keygen -t ed25519 -C "your.email@example.com"
ssh-add ~/.ssh/id_ed25519_github
```

- Configure `~/.ssh/config`:
```ini
Host github-personal
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_ed25519_github
```

- Clone using the custom host:
```sh
git clone git@github-personal:username/repository.git
```

---

### 5. Cloning, Updating, and Uploading a Repository

#### a. Clone the Repository
```sh
git clone https://github.com/username/repository.git
cd repository
```

#### b. Update the Repository
- Make changes locally.
- Stage and commit changes:
```sh
git add .
git commit -m "Your commit message"
```

#### c. Pull the Latest Changes (if needed)
```sh
git pull origin main
```

#### d. Push Your Changes
```sh
git push origin main
```

#### e. Verify
- Check GitHub to confirm the updates.
