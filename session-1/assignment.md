# Assignment: Introduction to Git with Python

---

## Objective
The objective of this assignment is to familiarize yourself with Git version control system by performing hands-on tasks on a local Git repository. You will learn how to initialize a Git repository, create commits, revert unwanted commits, create additional commits, and perform a reset operation.

## Prerequisites
- Basic understanding of Python programming language.
- No prior knowledge of Git commands is required.
- Git should be installed on your machine. For more information on how to install git, check [Git's official website](https://git-scm.com/).

## Instructions

1. **Setup:**
   - Open your terminal or command prompt.
   - Navigate to a directory where you want to create your Git repository.

2. **Initialize Git Repository:**
   - Use the following command to initialize a new Git repository:
     ```
     git init
     ```
   - This command creates a hidden `.git` directory in your current directory, which contains the necessary files for Git to manage your repository.

3. **Create Python Script:**
   - Create a new Python script named `calculator.py` in your repository directory.
   - Open the `calculator.py` file and write the code so that following tests can be executed:

     ```python
     # Test the functions
     result = add(5, 3)
     print("5 + 3 =", result)
     
     result = subtract(7, 2)
     print("7 - 2 =", result)
     
     result = multiply(4, 6)
     print("4 * 6 =", result)
     
     result = divide(8, 2)
     print("8 / 2 =", result)
     ```

4. **Create Commits:**
   - Use the following commands to stage and commit your changes:
     ```
     git add calculator.py
     git commit -m "Add initial calculator script"
     ```
   - This creates your first commit with a message describing the changes made.

5. **Revert Unwanted Commits:**
   - Imagine you accidentally added a flawed division function to the `calculator.py` script in your last commit.
   - Use the following command to view the commit history:
     ```
     git log
     ```
   - Identify the commit hash of the commit you want to revert.
   - Use the following command to revert the commit:
     ```
     git revert <commit_hash>
     ```
   - Replace `<commit_hash>` with the hash of the commit you want to revert.
   - Follow the prompts to create a revert commit.

6. **Create Additional Commits:**
   - **Requirement 1:**
     - Add a new function named `power` to calculate the power of a number.
     - The function should take two parameters: `base` and `exponent`.
     - It should return the result of raising `base` to the power of `exponent`.
     - Test the `power` function with different base and exponent values.
  
     ```python
     def power(base, exponent):
         return base ** exponent
     
     result = power(2, 3)
     print("2 ^ 3 =", result)
     ```

   - **Requirement 2:**
     - Modify the existing `divide` function to handle division by zero gracefully.
     - If the divisor is zero, the function should return a string `"Error: Cannot divide by zero"`.
     - Test the `divide` function with both valid and invalid divisor values.

     ```python
     def divide(a, b):
         if b == 0:
             return "Error: Cannot divide by zero"
         return a / b
     
     result = divide(8, 0)
     print("8 / 0 =", result)
     ```

   - **Requirement 3:**
     - Add a new function named `factorial` to calculate the factorial of a non-negative integer.
     - The function should take a single parameter: `n`.
     - It should return the factorial of `n`.
     - Test the `factorial` function with different values of `n`.

     ```python
     def factorial(n):
         if n == 0:
             return 1
         else:
             return n * factorial(n - 1)
     
     result = factorial(5)
     print("Factorial of 5 =", result)
     ```

     After implementing each requirement, remember to stage and commit your changes using the following commands:

     ```
     git add calculator.py
     git commit -m "Add Requirement <number> implementation"
     ```

     Replace `<number>` with the corresponding requirement number. This will create additional commits in your Git repository, documenting the changes made to the `calculator.py` script.

7. **Perform Reset:**
   - Now, imagine you want to undo all the changes made after the initial commit and start over.
   - Use the following command to perform a soft reset:
     ```
     git reset --soft HEAD~<number_of_commits>
     ```
   - Replace `<number_of_commits>` with the number of commits you want to reset.
   - This command moves the `HEAD` pointer to the specified commit, keeping your changes staged.


## Note
- Feel free to explore additional Git commands and options as you work through the tasks.
- Don't hesitate to seek help from your teammates or instructor if you encounter any difficulties during the assignment.
