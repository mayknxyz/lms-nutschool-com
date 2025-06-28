# Contributing to NutSchool LMS Community Edition

We are thrilled you're interested in contributing to the NutSchool LMS Community Edition! Your contributions help us achieve our mission of making programming education accessible to everyone, especially kids and learners in the Philippines.

By contributing to this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

## 💬 Communication

For general questions, discussions about new ideas, feature brainstorming, or seeking help that isn't a bug report, please use our **[GitHub Discussions](https://github.com/your-username/nutschool-lms/discussions)** tab. This is our primary mode of communication for the time being.

Please check the [GitHub Issues](https://github.com/your-username/nutschool-lms/issues) for reproducible bugs or clearly defined tasks.

## 🚀 Getting Started

This project is in early development. Detailed setup instructions and a local development guide will be added here soon. For now, we appreciate contributions related to:

* **Project Structure & Initial Setup:** Help define and implement the foundational architecture.
* **Core Feature Implementation:** Work on basic user authentication, course creation, and lesson delivery.
* **Documentation:** Improve this `CONTRIBUTING.md`, the `README.md`, or create new documentation.
* **Issue Triage:** Help us categorize and organize incoming issues.

## 🌱 How to Contribute

We encourage contributions of all sizes! Here's a general workflow:

1.  **Fork the Repository:** Start by forking the `nutschool-lms` repository to your GitHub account.
2.  **Clone Your Fork:**
    ```bash
    git clone [https://github.com/your-username/nutschool-lms.git](https://github.com/your-username/nutschool-lms.git)
    cd nutschool-lms
    ```
3.  **Create a New Branch:** For each feature or bug fix, create a new branch.
    ```bash
    git checkout -b feat/your-feature-name-or-issue-id
    # or for bug fixes:
    git checkout -b fix/issue-id-short-description
    ```
4.  **Make Your Changes:** Implement your feature or fix the bug.
5.  **Write Tests (if applicable):** Ensure your changes are covered by tests to prevent regressions.
6.  **Run Tests & Linters:** Before committing, ensure all existing tests pass and your code adheres to our Go formatting (e.g., `go fmt` and `go vet`).

7.  **Commit Your Changes: Follow Conventional Commits**

    We follow the [Conventional Commits specification](https://www.conventionalcommits.org/) for clear and consistent commit messages. This helps us understand the purpose of each change, generate changelogs, and maintain a clean history.

    Each commit message should consist of a **header**, a **blank line**, and an optional **body**. We strongly encourage adding a descriptive body for every commit to provide context and explain the "why" behind your changes.

    **A. Header (Subject Line)**
    * **Format:** `<type>(<scope>): <description>`
    * **`<type>`**: Must be one of the following standardized types. This indicates the kind of change.
    * **`<scope>` (Optional)**: A noun describing the section of the codebase affected (e.g., `auth`, `courses`, `frontend`, `db`, `api`, `readme`, `issues`). Use sparingly if the change is broad.
    * **`<description>`**: A very concise summary of the change.
        * Use the **imperative, present tense**: "Add user registration" not "Added user registration".
        * **Do not** capitalize the first letter.
        * **No period** at the end.
        * Keep it short (aim for ~50-72 characters).

    **B. Body (Recommended)**
    * Start the body with a blank line after the header.
    * Provide a more detailed explanation of the change.
    * Explain the *motivation* for the change and contrast it with previous behavior (the "why").
    * Use the imperative, present tense.
    * Wrap lines at around 72 characters for readability.
    * Reference any relevant issues (e.g., `Closes #123`, `Fixes #456`).

    ### Standardized Commit Types:

    Here is the comprehensive list of commit types to use for NutSchool LMS:

    * **`feat:`**
        * **Purpose:** Introducing a **new feature** or significant enhancement to the codebase.
        * **When to use:** When you add new functionality that wasn't there before, like a new user registration endpoint, a new course creation form, or a new type of quiz.
        * **Example:** `feat(auth): add email verification during registration`

    * **`fix:`**
        * **Purpose:** A **bug fix**. This addresses a defect or an incorrect behavior in the code.
        * **When to use:** When you correct something that was broken or not working as intended.
        * **Example:** `fix(courses): resolve progress tracking error for completed modules`

    * **`docs:`**
        * **Purpose:** **Documentation-only changes**.
        * **When to use:** For updates to `README.md`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, comments in code, or any other documentation files.
        * **Example:** `docs(readme): update project status to alpha release`

    * **`style:`**
        * **Purpose:** Changes that **do not affect the meaning of the code**, focusing on code style.
        * **When to use:** For whitespace, formatting, missing semicolons (if applicable for Go), or minor reordering that doesn't change logic.
        * **Example:** `style(main): format code with gofmt`

    * **`refactor:`**
        * **Purpose:** A **code change that neither fixes a bug nor adds a feature**. It's about restructuring or improving the internal structure of existing code.
        * **When to use:** When you rewrite parts of the code for better readability, maintainability, or efficiency without altering its external behavior.
        * **Example:** `refactor(auth): move session management to dedicated package`

    * **`perf:`**
        * **Purpose:** A code change that **improves performance**.
        * **When to use:** When your changes make the application faster, more resource-efficient, or reduce latency.
        * **Example:** `perf(db): optimize user query for faster retrieval`

    * **`test:`**
        * **Purpose:** Adding **missing tests or correcting existing tests**.
        * **When to use:** When writing new unit tests, integration tests, or fixing issues in the testing suite.
        * **Example:** `test(auth): add unit tests for password hashing utility`

    * **`build:`**
        * **Purpose:** Changes that affect the **build system or external dependencies**.
        * **When to use:** For updates to Go module dependencies (`go.mod`, `go.sum`), build scripts, or project configurations related to the build process.
        * **Example:** `build(deps): update gin-gonic to v1.9.1`

    * **`ci:`**
        * **Purpose:** Changes to our **CI (Continuous Integration) configuration files and scripts**.
        * **When to use:** For updates to GitHub Actions workflows (e.g., `github/workflows/*.yml`), or other CI-related configurations.
        * **Example:** `ci(github-actions): add Go test workflow`

    * **`chore:`**
        * **Purpose:** **Other changes that don't modify source or test files**, or don't fit into other types.
        * **When to use:** For routine maintenance, `.gitignore` updates, configuration file changes (not related to build/CI), or managing repository setup.
        * **Example:** `chore: update .gitignore to exclude build artifacts`

    * **`revert:`**
        * **Purpose:** Reverts a **previous commit**.
        * **When to use:** When undoing a previous change that was found to be incorrect or problematic. The body should typically reference the commit being reverted.
        * **Example:** `revert: feat(admin): add experimental dashboard widget`

8.  **Push to Your Fork:**
    ```bash
    git push origin your-branch-name
    ```
9.  **Open a Pull Request (PR):**
    * Go to your forked repository on GitHub.
    * Click "Compare & pull request" next to your newly pushed branch.
    * **Fill out the Pull Request Template thoroughly.** Provide a clear description of your changes, why they are needed, and how they were tested.
    * Reference any relevant issues (e.g., `Closes #123`).

## ✍️ Code Style and Guidelines

* **Go Standard Formatting:** Please run `go fmt` and `go vet` on your code before committing.
* **Clear Variable Names:** Use descriptive variable and function names.
* **Comments:** Add comments where necessary to explain complex logic.
* **Modularity:** Aim for small, focused functions and well-organized packages.

## 🚧 Features Reserved for NutSchool Pro

The NutSchool LMS operates on an **open-core model**. This means that while the Community Edition provides a robust and free foundation, certain advanced or specialized features are reserved for the commercial **NutSchool Pro** offering. This strategy helps ensure the long-term sustainability and continued development of the entire NutSchool ecosystem.

Please be aware that contributions attempting to implement the following types of features in the Community Edition may not be accepted:

* **Advanced Analytics & Reporting:** Detailed insights into student performance, usage patterns, or class comparisons.
* **Comprehensive User & Class Management:** Bulk user import/export, advanced role-based access control beyond basic student/teacher, school-level administration features.
* **Integration with External Educational Systems:** Such as LTI (Learning Tools Interoperability) or SIS (Student Information System) integration.
* **Automated Code Grading/Unit Testing Frameworks:** Sophisticated code assessment tools beyond simple pass/fail checks.
* **Custom Branding & White-Labeling:** Features allowing extensive customization of the LMS interface for institutions.
* **Dedicated Priority Support Channels:** Direct support beyond community forums.
* **Monetization/Payment Gateway Integrations:** Functionality for selling courses or subscriptions within the LMS itself (this is handled by the Pro platform).

If you have an idea for a feature that seems to fall into these categories, we encourage you to discuss it on our **[GitHub Discussions](https://github.com/your-username/nutschool-lms/discussions)** or visit [NutSchool.com/pro](https://www.nutschool.com/pro) (placeholder) to see if it's part of our commercial roadmap.

## 🤝 Code of Conduct

We are committed to fostering an inclusive and welcoming community. Please review our [Code of Conduct](CODE_OF_CONDUCT.md) before participating.

## 💡 Reporting Bugs

If you find a bug, please help us by [opening an issue](https://github.com/your-username/nutschool-lms/issues) on GitHub. Provide as much detail as possible, including steps to reproduce the bug, expected behavior, and actual behavior.

## 🙏 Thank You!

Your contributions are vital to the success of NutSchool LMS and our mission. Thank you for being a part of our journey!