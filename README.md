#!/bin/bash

# Step 1: Create a New Directory
mkdir new-project

# Step 2: Change to the Project Directory
cd new-project

# Step 3: Initialize a Git Repository
git init

# Step 4: Create and Edit README.md
touch README.md
echo "# My New Project" > README.md

# Step 5: Stage README.md for Commit
git add README.md

# Step 6: Commit Changes
git commit -m "init"

# Step 7: Create and Switch to the Development Branch
git branch development
git checkout development

# Step 8: Add Instructions to README.md
echo -e "\n## Project Setup Instructions\n\nFollow these steps to set up the project:" >> README.md

# Step 9: Stage README.md for Commit in Development Branch
git add README.md

# Step 10: Commit Changes in Development Branch
git commit -m "Add project setup instructions"

# Step 11: Merge Development into Main Branch
git checkout main
git merge development

# Step 12: Check Status and Ensure Up-to-Date
git status

# Step 13: Commit Changes in Main Branch
git commit -m "Merge development into main"

