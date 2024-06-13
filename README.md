# Setting Up and Pushing Code to GitHub Repository

Author: Jake Peters

Date: June 2024

### Step 0: Adding someone to the GitHub Organization
> **Note:** This step must be done by an "Owner".
1. Log in to GitHub and navigate to the "Analyticsverse" organization page.
2. Go to the "People" tab in the organization.
3. Click on "Invite Member".
4. Enter the colleague's username and email address.
5. Select the appropriate role (e.g., Member, depending on the level of access you want to provide).
6. Click "Send Invitation". Your colleague will receive an invitation to join the organization.

### Step 1: Initialize the Local Directory as a Git Repository

> **Note:** The remaining steps should be done by the new "Member" who wishes to set up a repository.

1. **Open Terminal or Command Prompt** and navigate to the local directory:
   ```bash
   cd /path/to/your/local/directory
   ```

2. **Initialize the directory as a Git repository**:
   ```bash
   git init
   ```

### Step 2: Add Remote Repository

1. **Log in to GitHub** and navigate to the "Analyticsverse" organization page.
2. **Create a New Repository**:
   - Click on the "Repositories" tab.
   - Click on the "New" button.
   - Fill in the repository details:
     - **Repository name**: Choose a descriptive name for your repository.
     - **Description**: Provide a brief description of the repository.
     - **Public/Private**: Choose the visibility of the repository.
     - Do **not** initialize the repository with a README, .gitignore, or license (this can cause conflicts).
   - Click on "Create repository".

3. **Add the remote repository to your local Git repository**:
   ```bash
   git remote add origin https://github.com/Analyticsverse/<repository-name>.git
   ```

### Step 3: Stage, Commit, and Push Local Files

1. **Stage all the files** in the local directory:
   ```bash
   git add .
   ```

2. **Commit the changes** with a meaningful message:
   ```bash
   git commit -m "Initial commit of existing project"
   ```

3. **Push the changes** to the remote repository:
   ```bash
   git push -u origin main
   ```

### Step 4: Best Practices and Tips

1. **Use Branches**: For future changes, create new branches for features or fixes and merge them into the main branch via pull requests.
   ```bash
   git checkout -b new-feature
   # After making changes
   git add .
   git commit -m "Add new feature"
   git push origin new-feature
   ```
   - Open a pull request on GitHub to merge the changes into the main branch.

2. **Write Descriptive Commit Messages**: Use clear and concise commit messages to describe your changes.

3. **Include a README**: Provide detailed instructions and documentation in the README file.

4. **Use .gitignore**: Include a .gitignore file to exclude files that should not be tracked by Git (e.g., sensitive data, logs).
