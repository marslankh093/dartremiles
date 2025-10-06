You’re stuck in a half-finished rebase, which is why you’re seeing all those “cannot rename branch / already in rebase” errors.
Here’s the exact terminal sequence you can copy-paste to safely fix everything 👇

# 1️⃣ Abort the unfinished rebase to clean up
git rebase --abort

# 2️⃣ Ensure you are on main
git checkout main

# 3️⃣ Pull latest code safely, ignoring unrelated history
git pull origin main --allow-unrelated-histories

# 4️⃣ Resolve any conflict if it appears (open and fix README.md, then:)
git add .
git commit -m "Resolved merge conflicts"

# 5️⃣ Force push your local copy to GitHub
git push -u origin main --force


------------ 1st do this alwasys 
# Initialize new git repo git init # Add all project files git add . # Commit changes git commit -m "Initial commit" # Rename branch to main git branch -M main # Connect to GitHub repo git remote add origin https://github.com/marslankh093/dartremiles.git # Pull existing code (merge safely) git pull origin main --rebase # Push your local code to GitHub git push -u origin main this one

<<<<<<< HEAD
# Initialize new git repo
git init

# Add all project files
git add .

# Commit changes
git commit -m "Initial commit"

# Rename branch to main
git branch -M main

# Connect to GitHub repo
git remote add origin https://github.com/marslankh093/dartremiles.git

# Pull existing code (merge safely)
git pull origin main --rebase

# Push your local code to GitHub
git push -u origin main


 ![Image 1](1.PNG)
![I  ma ge 1   ](     2.   PNG) 
