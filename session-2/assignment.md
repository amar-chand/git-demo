# Assignment: Advanced Git Operations with Python

---

## Objective
This assignment extends the previous one by introducing advanced Git operations including remote repository management on GitHub, branching, merging, and pull requests.

## Prerequisites
- Completion of the previous assignment: "Introduction to Git with Python"
- Basic understanding of GitHub and SSH

## Instructions

### Part 1: Remote Repository Management

1. **Initializing Remote Repository on GitHub:**
   - Create a new repository named `calculator` on GitHub.
   - Leave the repository empty without initializing it with any files.

2. **Adding Remote Repository as Origin:**
   - Use the following command to add the GitHub repository as the origin of your local repository:
     ```
     git remote add origin <repository_url>
     ```
   - Replace `<repository_url>` with the URL of the GitHub repository.

3. **Create a Personal Access Token (Optional):**
   - If you haven't created a personal access token:
     - Follow GitHub's instructions on [managing personal access tokens](https://docs.github.com/en/enterprise-server@3.9/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

4. **Pushing Local Repository to Origin:**
   - Push the contents of your local repository to the remote repository on GitHub, using the personal access token:
     ```
     git push -u origin main
     ```
   - This command pushes the `main` branch of your local repository to the `main` branch of the remote repository.

### Part 2: Cloning and Branching

5. **Generate SSH Keys (Optional):**
   - If you haven't generated an SSH key:
     - Follow GitHub's instructions on [generating an SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
   - Configure the SSH key in GitHub:
     - Follow GitHub's instructions on [adding an SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account).

6. **Cloning Remote Repository with SSH:**
   - Clone the remote repository to a different location using SSH.

5. **Creation of Branches:**
   - Create a new branch named `feature/calculator` in the cloned repository:
     ```
     git checkout -b feature/calculator
     ```

6. **Renaming the Branch:**
   - Rename the branch to `feature/calculator-improvements`:
     ```
     git branch -m feature/calculator-improvements
     ```

### Part 3: Working on the Branch

7. **Do Some Work on the Branch:**
   - Implement additional functionalities or improvements to the `calculator.py` script in the `feature/calculator-improvements` branch. For instance, you can add a function to perform modulo operation.

### Part 4: Branch Comparison and Pull Request

8. **Comparing the Branch with Main:**
   - Compare the `feature/calculator-improvements` branch with the `main` branch:
     ```
     git diff main..feature/calculator-improvements
     ```

9. **Pushing to Remote Repository:**
   - Push the changes in the `feature/calculator-improvements` branch to the remote repository using SSH:
     ```
     git push origin feature/calculator-improvements
     ```

10. **Creating a Pull Request:**
    - Go to the GitHub repository and create a pull request for the `feature/calculator-improvements` branch.

11. **Merging the Pull Request:**
    - Merge the pull request into the `main` branch on GitHub.

12. **Deleting the Branch Locally:**
    - After the pull request is merged, delete the `feature/calculator-improvements` branch locally:
      ```
      git branch -d feature/calculator-improvements
      ```

## Note
- Document each step of the assignment with screenshots or code snippets where appropriate.
- Write a summary of your experience, highlighting any challenges faced and lessons learned.
- Don't hesitate to seek help from your teammates or instructor if you encounter any difficulties during the assignment.

