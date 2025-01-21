# Git Branch Naming Convension and Commite Messages Best Practices

---

## Frontend Branch Names Best Practices

When creating branch names, it's important to follow industry standards that make your branches easy to understand, manage, and collaborate on. Here are the best practices:

### Use a Clear and Consistent Naming Convention

#### Feature Branches:

- **Purpose**: For new features or enhancements.
- **Format**: `feature/short-description`
- **Example**: `feature/user-authentication`

#### Refactor Branches:

- **Purpose**: For improving or refactoring existing features.
- **Format**: `refactor/short-description`
- **Example**: `refactor/user-authentication`

#### Bug Fixes:

- **Purpose**: For fixing bugs or issues.
- **Format**: `bugfix/short-description`
- **Example**: `bugfix/fix-login-error`

#### Hotfixes:

- **Purpose**: For critical fixes that need to go directly to production.
- **Format**: `hotfix/short-description`
- **Example**: `hotfix/patch-security-issue`

#### Chore/Tasks:

- **Purpose**: For non-functional tasks like updating dependencies or refactoring code.
- **Format**: `chore/short-description`
- **Example**: `chore/update-dependencies`

#### Release Branches:

- **Purpose**: For preparing a release.
- **Format**: `release/version-number`
- **Example**: `release/1.0.0`

### Use Lowercase Letters

Stick to lowercase letters, using hyphens (`-`) to separate words.

- **Example**: `feature/add-user-profile` (not `Feature/AddUserProfile`).

### Keep It Descriptive Yet Concise

Branch names should clearly describe the purpose but remain as short as possible.

- **Example**: `feature/dark-mode` instead of `feature/added-dark-mode-functionality`.

### Include Task/Issue IDs (Optional)

If you use project management tools like JIRA or GitHub Issues, include the task or issue ID.

- **Format**: `feature/ID-short-description`
- **Example**: `feature/JIRA-1234-add-user-authentication`

### Consider Team Conventions

Align with any existing team or company-specific branch naming conventions to maintain consistency.

<p align="center">
  <hr style="border: none; border-top: 1px solid #fd8c73; width: 100%;">
</p>

## Backend Branch Names Best Practices

When creating branch names for backend development, it’s essential to maintain clarity and consistency, just like with frontend projects. Here are some specific practices:

### Focus on the Scope of the Work

Ensure the branch name reflects the specific backend task or feature being worked on.

### Common Branch Types for Backend Projects

#### Chore/Dependencies:

- **Purpose**: For non-functional tasks like updating dependencies or adding new documents.
- **Format**: `chore/short-description`
- **Examples**:
  - `chore/add-typescript`
  - `chore/add-readme`

#### API Development:

- **Purpose**: For new API endpoints or changes.
- **Format**: `api/short-description`
- **Example**: `api/user-registration`

#### Database Changes:

- **Purpose**: For migrations, schema updates, or data-related tasks.
- **Format**: `db/short-description`
- **Examples**:
  - `model/authentication`
  - `db/user-table`

#### Refactoring:

- **Purpose**: For code restructuring without adding new features.
- **Format**: `refactor/short-description`
- **Example**: `refactor/optimize-query-performance`

#### Performance Improvements:

- **Purpose**: For tasks aimed at improving backend performance.
- **Format**: `perf/short-description`
- **Example**: `perf/improve-caching-strategy`

#### Security Enhancements:

- **Purpose**: For security-related updates.
- **Format**: `security/short-description`
- **Example**: `security/add-encryption-to-passwords`

### Include Contextual Information

#### Technology-Specific:

If the branch deals with a specific technology or framework, include that in the branch name.

- **Example**: `api/express-add-authentication`, `db/mongo-update-schema`

#### Component-Based:

If working on specific components or modules within the backend.

- **Example**: `module/payment-processing`, `service/user-auth`

### Use Identifiers for Specific Tasks

Include identifiers like feature IDs or ticket numbers if your team uses a tracking system.

- **Examples**:
  - `api/JIRA-5678-add-payment-endpoint`
  - `db/ISSUE-123-add-index-to-users`

### Consider CI/CD Pipelines

If your CI/CD pipeline has specific naming requirements or conventions (e.g., `release/` or `hotfix/` prefixes), ensure your branch names align with those.

### Environment-Specific Branches

For tasks that are environment-specific (like staging or production):

- **Format**: `env/environment-name/short-description`
- **Example**: `env/staging/fix-db-connection-issue`

### Prioritize Clarity

Even for complex backend tasks, strive for branch names that can be easily understood by anyone on the team. Avoid overly technical jargon unless necessary and understood by all team members.

### Avoid Ambiguity

Be as specific as possible to avoid confusion.

- **Example**: Instead of `fix-error`, use `fix-null-pointer-error`.

### Align with the Development Workflow

If your team follows a specific Git workflow (like Git Flow), ensure that your branch names fit within that structure.

- **Examples**:
  - `feature/add-order-controller`
  - `hotfix/fix-shopify-api-timeout`

## Additional Best Practices for All Branches

- **Use Consistent Prefixes**: Standardize prefixes across teams, e.g., `feature/`, `bugfix/`.
- **Document Naming Conventions**: Maintain documentation of branch naming conventions to onboard new team members easily.
- **Review Branch Names**: Before pushing, verify that the branch name adheres to the agreed conventions.
- **Avoid Special Characters**: Do not use special characters or spaces in branch names; stick to alphanumeric characters and hyphens (`-`).

By adhering to these practices, your Git workflow will be more efficient, collaborative, and scalable.

<p align="center">
  <hr style="border: none; border-top: 1px solid #fd8c73; width: 100%;">
</p>

# Best Practices for Writing Git Commit Messages

Effective commit messages are vital for understanding the history of a project, simplifying collaboration, and maintaining a clean and organized repository. A well-structured commit message often follows a standard format with a **header**, **body**, and **footer**.

---

## Commit Message Format

### 1. **Header**

- Contains a concise description of the changes.
- Limited to **50 characters** or fewer.
- Written in **imperative mood** (e.g., "Fix," "Add," "Update").
- No period at the end.

**Example**:  
`fix(ui): resolve issue with button alignment`

### 2. **Body** (Optional but Recommended)

- Provides additional details about the commit.
- Explains **what**, **why**, and sometimes **how** of the changes.
- Wrapped at **72 characters per line** for better readability.
- Focus on **why the change was made**, not just what was changed.

**Example**:

```
Lorem Ipsum is simply dummy text of the printing and typesetting industry.

Lorem Ipsum has been the industry's standard dummy text ever since the 1500s.
```

### 3. **Footer** (Optional)

- Includes references to issues, tickets, or reviewers.
- Follows specific conventions based on project or team requirements.

**Example**:

```
Reviewed-by: John Doe
Refs: #345
```

---

## Commit Types (Conventional Commits)

Use a prefix to categorize the purpose of the commit:

| **Type**   | **Description**                                   | **Example**                       |
| ---------- | ------------------------------------------------- | --------------------------------- |
| `feat`     | Introduces a new feature                          | `feat(auth): add user login`      |
| `fix`      | Fixes a bug                                       | `fix(ui): resolve button overlap` |
| `chore`    | Non-functional changes (e.g., dependency updates) | `chore: update dependencies`      |
| `docs`     | Documentation changes                             | `docs: update README`             |
| `refactor` | Code refactoring without functional changes       | `refactor: optimize query`        |
| `test`     | Adding or modifying tests                         | `test: add unit tests for login`  |
| `style`    | Code style changes (e.g., formatting)             | `style: fix indentation`          |
| `perf`     | Performance improvements                          | `perf: improve caching strategy`  |
| `build`    | Changes to build process or tools                 | `build: add CI/CD configuration`  |

---

## Best Practices for Commit Messages

### 1. Use **Imperative Mood**

Write commit messages as if you're commanding the codebase to perform an action.

- ✅ `fix: correct typo in the navbar`
- ❌ `fixed a typo in the navbar`

### 2. Make **Atomic Commits**

Each commit should represent one logical change. Avoid bundling unrelated changes into a single commit.

- ✅ Separate commits for fixing a bug and adding a feature.
- ❌ A single commit for fixing a bug and updating documentation.

### 3. Avoid Generic Messages

Generic messages like "update code" or "fix issue" don't convey meaningful information. Be descriptive yet concise.

### 4. Do Not Add Periods

Avoid using periods at the end of commit messages. They're unnecessary in short, descriptive headers.

### 5. Use a Consistent Style

Follow a standard style guide for all commit messages within the team or organization.

### 6. Avoid Commit Messages Like:

- "WIP" (Work in Progress): Instead, use draft pull requests.
- "Fixed stuff": Be explicit about the fix.
- "Temp changes": Avoid committing temporary or debugging code.

---

## Examples of Good Commit Messages

### Header Only

`feat(dark-mode): implement dark mode for dashboard`

### Header with Body

```
fix(validation): resolve issue with email validation

Previously, the email validation logic failed to handle certain edge cases
(e.g., emails with a '+' character). Updated the regex to correctly match
valid email addresses.
```

### Header, Body, and Footer

```
feat(ui): add color converter utility

Added a utility function to convert colors from hexadecimal to RGBA format.
This helps standardize color handling across the app.

Reviewed-by: John Doe
Refs: #456
```

---

## Benefits of Following Best Practices

- Improved collaboration and understanding of the codebase.
- Easier debugging and reverting changes when necessary.
- Better integration with tools like Jira, GitHub, or GitLab for tracking.

---

By adhering to these guidelines, your Git commit history will be more meaningful, maintainable, and professional.

---

## Author

[Gaurav Jain](https://github.com/gauravjainse/git-best-practices)  
Senior Software Engineer,  
[Techinfini Solutions Pvt. Ltd.](https://techinfini.in/)
