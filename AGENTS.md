# AGENTS.md - Guidelines for Agentic Coding

## Repository Overview

This repository serves two purposes:
1. **Git learning playground** - For practicing Git and GitHub workflows
2. **GitHub Profile README** - Auto-updating portfolio for Elkin Jaramillo (Data Engineer)

This is NOT a programming project with build/lint/test commands.

---

## Build, Lint, and Test Commands

Since this is a Git learning repository (not a code project), there are no traditional build commands. However, here's how to work with the Git workflow:

### Git Commands

```bash
# Check repository status
git status

# View current branch
git branch

# Stage all changes
git add .

# Commit with message
git commit -m "description of changes"

# Push to remote
git push

# Pull latest changes
git pull

# View commit history
git log --oneline
```

### Running a Single Test

Not applicable - this repository contains no testable code.

### Linting

Not applicable - this repository contains no lintable code.

---

## Code Style Guidelines

### General Principles

This repository uses standard Git practices. All contributions should follow:

1. **Meaningful commit messages** - Use clear, concise descriptions
2. **Atomic commits** - One logical change per commit
3. **Branch naming** - Use descriptive branch names (e.g., `feature/description`, `fix/issue-name`)

### Commit Message Convention

Follow conventional commits format:

```
<type>(<scope>): <description>

[optional body]
[optional footer]
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation only
- `style`: Formatting, no code change
- `refactor`: Code change that neither fixes nor adds
- `test`: Adding or updating tests
- `chore`: Maintenance tasks

Examples:
```
feat: add new Git workflow documentation
fix: correct typo in README
docs: update installation instructions
```

### File Organization

```
.
├── README.md              # Main profile README (auto-updated)
├── .github/
│   ├── workflows/         # GitHub Actions
│   └── recent-activity.config.yml
└── .vscode/
    └── settings.json     # VS Code preferences
```

### Naming Conventions

- **Files**: Use lowercase with hyphens (e.g., `my-file.md`)
- **Branches**: Use descriptive names with slashes (e.g., `feature/add-new-section`)
- **Commits**: Imperative mood ("add" not "added" or "adds")

### VS Code Settings

The repository includes VS Code settings for terminal auto-approval:

```json
{
    "chat.tools.terminal.autoApprove": {
        "git remote": true,
        "git add": true,
        "git commit": true,
        "git push": true
    }
}
```

### Error Handling

When making changes:

1. **Always verify before pushing**:
   ```bash
   git status
   git diff
   ```

2. **Test in a branch first** (if applicable):
   ```bash
   git checkout -b feature/your-feature
   # make changes
   git push -u origin feature/your-feature
   ```

3. **Never force push** to main/master branch

### GitHub Actions Workflow

The repository uses a GitHub Action to auto-update the README with recent activity:

- Runs every 12 hours
- Can be triggered manually via `workflow_dispatch`
- Uses `Readme-Workflows/recent-activity@v2.4.1`

Do NOT modify the workflow file unless necessary.

---

## Important Notes

1. **No code to review** - This repository is for Git practice and portfolio display
2. **README is auto-generated** - Sections between `<!--RECENT_ACTIVITY:start-->` and `<!--RECENT_ACTIVITY:end-->` are automatically updated
3. **Keep the workflow intact** - The GitHub Action is essential for the profile

---

## Agent Instructions

When working in this repository:

1. Do NOT add programming code (this is not a code project)
2. Do NOT add build/lint/test configurations
3. Focus on Git workflow improvements if needed
4. Maintain the README structure for auto-updates
5. Do NOT push secrets or sensitive data
6. Use descriptive commit messages following conventional commits

For questions about the repository purpose, refer to the README.md file.
