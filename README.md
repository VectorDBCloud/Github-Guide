# GitHub Repository Guide

This guide outlines best practices for creating and managing GitHub repositories. It includes naming conventions, branching strategies, approvals, reviews, assignments, comments, documentation, and more.

---

## **1. Repository Naming Convention**

Use consistent and descriptive names for your repositories to make them easily identifiable. Follow this format:

`<team>-<project>-<purpose>`

Examples:
- `ai-chatbot-backend`
- `frontend-ecommerce-dashboard`
- `backend-inventory-management`

---

## **2. Branching Strategy**

Follow a structured branching strategy such as **Git Flow** or a simplified version:

### **Main Branches**
- `main`: The production-ready code. Always stable.
- `dev`: The development branch where features are integrated.

### **Feature Branches**
- Use this format: `feature/<feature-name>`
  - Example: `feature/login-page`, `feature/chatbot-integration`

### **Bugfix Branches**
- Use this format: `bugfix/<bug-description>`
  - Example: `bugfix/fix-login-error`

### **Hotfix Branches**
- For critical fixes in production: `hotfix/<description>`
  - Example: `hotfix/security-vulnerability`

---

## **3. Branch Protection Rules**

- Require pull requests (PRs) to merge into `main` or `dev`.
- Set a minimum number of reviewers (e.g., 2).
- Enable **status checks** (e.g., CI/CD pipelines must pass before merging).

---

## **4. Commit Message Guidelines**

Use descriptive and consistent commit messages. Follow this format:

`<type>: <short description>`

[Optional: Long description of the change, reasons, etc.]


### **Types**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation update
- `style`: Code style changes (formatting, whitespace)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance or configuration

### **Example**

`feat: add user authentication API`

Added an endpoint for user login and registration. This includes JWT-based token authentication.


---

## **5. Code Review and Approval Process**

### **Pull Request Creation**
- Developers create a pull request (PR) to merge their branch into `main` or `dev`.
- Include a clear title and description of the changes in the PR.

### **Assign Reviewers**
- Assign at least two reviewers based on expertise:
  - **Backend**: Backend team members
  - **Frontend**: Frontend team members
  - **AI/ML**: AI team members

### **Review Guidelines**
- Reviewers check for:
  - Code quality and readability
  - Adherence to standards and best practices
  - Functionality (run and test the code)
  - Security and performance issues

### **Approval**
- Reviewers approve the PR if everything is fine.
- If changes are needed, provide constructive comments and request changes.

### **Merge Strategy**
- Use **Squash and Merge** or **Rebase and Merge** for a cleaner commit history.

---

## **6. Assigning and Tracking Tasks**

### **Use GitHub Issues**
- Create issues for each task, bug, or feature.
- Assign issues to team members.

### **Labeling**
- Use labels to categorize issues and PRs:
  - `bug`
  - `feature`
  - `enhancement`
  - `documentation`

### **Milestones**
- Create milestones for major releases or sprints.
- Add issues to milestones for tracking progress.

### **Linking PRs to Issues**
- Link PRs to issues using keywords like `Fixes #<issue-number>` to auto-close issues upon merging.

---

## **7. Comments and Documentation**

### **Code Comments**
- Add meaningful comments to explain complex logic or algorithms.
- Use `TODO` comments for incomplete features or tasks.

### **README.md**
Include a comprehensive `README.md` in the repository:
- Project description
- How to set up and run the project
- Contribution guidelines
- License information

### **Technical Documentation**
- Use a `docs/` folder for technical and architectural documentation.
- Include diagrams (e.g., API flow, database schema) when necessary.

### **Wiki**
- Use the GitHub Wiki feature for in-depth documentation.

---

## **8. Reviews and Collaboration**

### **Code Reviews**
- Reviewers should provide specific, actionable, and respectful feedback.
- Example:
  - _"Consider renaming `x` to `userInput` for better readability."_

### **Collaboration Tools**
- Use GitHub Discussions for brainstorming and team communication.
- Use project boards for tracking tasks and workflows.

---

## **9. CI/CD and Testing**

### **Set Up Continuous Integration**
- Use GitHub Actions or other CI tools to run tests automatically for every PR.
- Example:
  - Unit tests
  - Integration tests
  - Linting and code formatting checks

### **Testing Guidelines**
- Write test cases for every feature or bug fix.
- Store tests in `tests/` with proper organization (e.g., `unit/`, `integration/`).

---

## **10. Best Practices**

### **Consistency**
- Follow a consistent coding style (use linters like ESLint or Prettier for JS/TS projects).

### **Security**
- Avoid committing sensitive information like API keys or passwords.
- Use `.env` files for environment variables and add them to `.gitignore`.

### **Documentation**
- Keep documentation updated with every feature or change.

### **Small Commits**
- Commit changes incrementally for better traceability.

---

## **11. Naming Conventions**

### **Variables and Functions**
- Use camelCase for JavaScript/TypeScript (e.g., `getUserData`).
- Use snake_case for Python (e.g., `get_user_data`).

### **Files and Directories**
- Use **kebab-case** for filenames (e.g., `user-profile.component.ts`).

---

## **12. Example Workflow**

1. Developer pulls the latest `dev` branch:

```
   git pull origin dev
```

2. Creates a feature branch:

```
git checkout -b feature/login-page
```

3. Implements the feature and commits changes:

```
git commit -m "feat: add login page"
```

4. Pushes the branch:

```
git push origin feature/login-page
```

5. Opens a pull request and assigns reviewers.

6. Reviewers approve the PR, and it is merged into `dev`.

7. The 'dev' branch is tested and merged into 'main' for production.

---

## **13. Tools and Resources**

### **GitHub Features**
Issues, PRs, Actions, Discussions, and Projects.

### **Linters**
ESLint, Prettier, Flake8, etc.

### **CI/CD**
GitHub Actions, CircleCI, TravisCI.

### **Documentation**
MkDocs, JSDoc, or Sphinx for detailed documentation.
