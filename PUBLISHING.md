# Publish This GitHub Profile

GitHub displays a profile README when a public repository has exactly the same
name as the account. For this profile, the repository must be:

`taukhir/taukhir`

## Option 1: GitHub Website and Git

1. Sign in to [GitHub](https://github.com).
2. Select **New repository**.
3. Set the repository name to `taukhir`.
4. Keep it **Public**.
5. Do not initialize it with a README, `.gitignore`, or license.
6. Select **Create repository**.
7. Open PowerShell and run:

```powershell
cd "D:\BE Projects\taukhir"
git init
git add README.md PUBLISHING.md assets
git commit -m "Create GitHub profile"
git branch -M master
git remote add origin https://github.com/taukhir/taukhir.git
git push -u origin master
```

GitHub may open a browser window for authentication during the first push.

## Option 2: Upload Through GitHub

1. Create the public `taukhir/taukhir` repository as described above.
2. Select **uploading an existing file** on the empty-repository page.
3. Upload `README.md`.
4. Upload the `assets` folder containing `profile-banner.svg`.
5. Commit the files to the `main` branch.

Keeping the `assets/profile-banner.svg` path unchanged is important because the
README uses that relative path.

## Update the Profile Later

After publishing, edit files locally and run:

```powershell
cd "D:\BE Projects\taukhir"
git add .
git commit -m "Update GitHub profile"
git push
```

Visit [github.com/taukhir](https://github.com/taukhir) after pushing. The README
should appear at the top of the profile automatically.
