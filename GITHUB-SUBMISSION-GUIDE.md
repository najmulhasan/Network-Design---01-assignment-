# GitHub Submission Guide

## Quick Setup (5 Minutes)

Follow these steps to upload your assignment to GitHub and submit the repository link.

---

## Step 1: Create GitHub Repository (1 minute)

1. Go to **https://github.com/new**
2. Sign in to your GitHub account (or create one if needed)
3. Fill in repository details:
   - **Repository name**: `real-estate-network-architecture`
   - **Description**: `Network Architecture for Real Estate Finder Platform - Multi-Region AWS Design`
   - **Visibility**: Choose **Public** (so instructors can access)
   - **DO NOT** initialize with README (we already have one)
4. Click **"Create repository"**

---

## Step 2: Initialize Git in Your Project (1 minute)

Open PowerShell in your project directory and run:

```powershell
cd "C:\Users\user\Desktop\networking assignment"
git init
```

---

## Step 3: Add and Commit Files (1 minute)

```powershell
git add .
git commit -m "Complete network architecture assignment for Real Estate Finder Platform"
```

This adds all your files:
- README.md
- Real-Estate-Network-Architecture-Page-1.drawio.png
- Networking Documentation.pdf
- DIAGRAM-CREATION-GUIDE.md
- ASSIGNMENT-CHECKLIST.md

---

## Step 4: Connect to GitHub (1 minute)

Replace `YOUR-USERNAME` with your actual GitHub username:

```powershell
git remote add origin https://github.com/YOUR-USERNAME/real-estate-network-architecture.git
git branch -M main
```

---

## Step 5: Push to GitHub (1 minute)

```powershell
git push -u origin main
```

If prompted for credentials:
- **Username**: Your GitHub username
- **Password**: Use a Personal Access Token (not your password)

### How to Create Personal Access Token:
1. Go to **GitHub.com** → Settings → Developer Settings → Personal Access Tokens → Tokens (classic)
2. Click **"Generate new token (classic)"**
3. Select scopes: ✅ `repo` (full control of private repositories)
4. Click **"Generate token"**
5. Copy the token and use it as your password

---

## Step 6: Verify Upload

1. Go to your GitHub repository URL:
   ```
   https://github.com/YOUR-USERNAME/real-estate-network-architecture
   ```

2. Check that all files are uploaded:
   - ✅ README.md (should display automatically)
   - ✅ Real-Estate-Network-Architecture-Page-1.drawio.png
   - ✅ Networking Documentation.pdf
   - ✅ Other files

3. The diagram should be visible in the README!

---

## Step 7: Submit Repository Link

Copy your repository URL and submit it:

```
https://github.com/YOUR-USERNAME/real-estate-network-architecture
```

---

## Alternative: Using GitHub Desktop (No Commands)

If you prefer a GUI instead of command line:

1. Download **GitHub Desktop**: https://desktop.github.com/
2. Install and sign in to GitHub
3. Click **"Add"** → **"Add existing repository"**
4. Browse to: `C:\Users\user\Desktop\networking assignment`
5. Click **"Publish repository"**
6. Choose name: `real-estate-network-architecture`
7. Make it **Public**
8. Click **"Publish"**

Done! Your repository is now on GitHub.

---

## Troubleshooting

### Issue: "Git is not recognized"
**Solution**: Install Git for Windows
- Download from: https://git-scm.com/download/win
- Install with default settings
- Restart PowerShell

### Issue: Authentication Failed
**Solution**: Use Personal Access Token instead of password
- See "How to Create Personal Access Token" above

### Issue: Files too large
**Solution**: GitHub has a 100MB file size limit
- Your files should be fine (diagram PNG and PDF are typically <10MB)
- If PDF is large, consider compressing it

---

## Quick Command Reference

```powershell
# Initialize Git
git init

# Check status
git status

# Add all files
git add .

# Commit with message
git commit -m "Your message here"

# Add remote repository
git remote add origin https://github.com/USERNAME/REPO.git

# Push to GitHub
git push -u origin main

# View remote URL
git remote -v
```

---

## Final Check Before Submission

✅ Repository is public (or accessible to instructor)  
✅ All 5 files are uploaded  
✅ README.md displays correctly with diagram  
✅ Repository has a clear name  
✅ Description is added  

---

## Your Repository Should Look Like This:

```
real-estate-network-architecture/
├── README.md (displays by default)
├── Real-Estate-Network-Architecture-Page-1.drawio.png
├── Networking Documentation.pdf
├── DIAGRAM-CREATION-GUIDE.md
├── ASSIGNMENT-CHECKLIST.md
└── GITHUB-SUBMISSION-GUIDE.md (this file)
```

**Diagram will be visible in README!** 🎉

---

## Need Help?

If you encounter any issues:
1. Check GitHub's documentation: https://docs.github.com/
2. Try GitHub Desktop (easier than command line)
3. Make sure all files are in the correct folder

---

**Good luck with your submission!** 🚀
