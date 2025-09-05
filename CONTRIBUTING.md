# Contributing Guidelines

Thank you for considering contributing to this project! 🎉  
We welcome contributions of all kinds, including bug reports, feature
requests, documentation improvements, and code.

---

## Getting Started

Before contributing, ensure you have: 
- A [GitHub account](https://github.com/join) 
- [Git](https://git-scm.com/) installed 
- [Node.js](https://nodejs.org/) (LTS recommended) 
- [npm](https://docs.npmjs.com/) or [yarn](https://yarnpkg.com/) installed

---

## Setup

1. **Fork** the repository on GitHub.

2. **Clone** your fork locally:

    ```bash
    git clone https://github.com/<your-username>/coding-logs.git
    cd coding-logs
    ```
    Note: or the name you chose during fork

3.  **Add the upstream remote** (to keep your fork up to date):

    ```bash
    git remote add upstream https://github.com/EscamillaJuan/coding-logs.git
    ```

4. **Install dependencies**

   Ensure Node.js and npm are installed with the recommended versions.  
   We recommend using **nvm** (Node Version Manager) to manage Node.js versions.

   - **nvm (Node Version Manager)**
     - Recommended for installing and switching Node versions
     - [Download for Windows](https://github.com/coreybutler/nvm-windows/releases)
     - Use version: **1.1.12 or later**

   - **Node.js**
     - Required version: **>=20.x (LTS)**
     - If not using nvm, install directly: [Download for Windows](https://nodejs.org/en/download/)
     - Check version:
       ```bash
       node -v
       ```

   - **npm**
     - Required version: **>=10.x**
     - Installed automatically with Node.js
     - Update if needed:
       ```bash
       npm install -g npm@latest
       ```
     - [Download for Windows (bundled with Node.js)](https://nodejs.org/en/download/)

   Then install project dependencies:

    ```bash
    npm install
    ```

5. **Open in VS Code**

    ```bash
    code .
    ```
    - The built-in Extension Development Host allows debugging your extension.
    - To debug:
        1. Open the **Run and Debug** panel (`Ctrl+Shift+D` / `Cmd+Shift+D`).
        2. Save a `launch.json` in `.vscode/launch.json` with:

        ```jsonc
        {
          "version": "0.2.0",
          "configurations": [
            {
              "name": "Launch Extension",
              "type": "extensionHost",
              "request": "launch",
              "runtimeExecutable": "${execPath}",
              "args": [
                "--extensionDevelopmentPath=${workspaceFolder}"
              ]
            }
          ]
        }
        ```
        3. Press **F5** to launch the Extension Development Host.

---

## Build Instructions

1. Compile TypeScript → JavaScript:

    ```bash
    npm run compile
    ```

    - Output: `out/extension.js`

2. For development with automatic rebuild:

    ```bash
    npm run watch
    ```

3. Prepublish step:

    ```bash
    npm run vscode:prepublish
    ```

---

## Test Instructions

1. **Run linting:**

    ```bash
    npm run lint -- --fix
    ```

2. **Run tests:**

    ```bash
    npm test
    ```

    - Runs `vscode-test` using `@vscode/test-electron`
    - Launches a VS Code instance and executes extension tests
    - Warnings about built-in extensions (e.g., `vscode.git`, Live Share, Pylance) or API proposals can be safely ignored
    - Sample output:
      ```bash
      ✔ Sample test
      1 passing (142ms)
      ```

3. **Debug tests:**
    - Set breakpoints in `src/test/` files
    - Press **F5** in the Run and Debug panel

> All tests **must pass** and lint checks should be clean before submitting a pull request.

---

## Development Workflow

- Run & debug the extension by pressing **F5** → opens a new Extension Development Host
- Make changes in `src/` → recompile (`npm run watch`) or use the debugger
- Write tests in `src/test/` and run with `npm test`

---

## Pull Request Process

1. Create a new branch:

    ```bash
    git checkout -b feature/my-new-feature
    ```

2. Make changes and commit with a clear message:

    ```bash
    git commit -m "feat: add my new feature"
    ```

    > Recommended: follow [Conventional Commits](https://www.conventionalcommits.org/)

3. Push your branch:

    ```bash
    git push origin feature/my-new-feature
    ```

4. Open a **Pull Request** against the `main` branch

---

## Code Style

- Follow existing code style
- Run the linter before committing:

    ```bash
    npm run lint -- --fix
    ```

- Keep commits focused and meaningful
- Include tests for new functionality when possible

---

## Reporting Issues

- Search the [issue tracker](https://github.com/EscamillaJuan/coding-logs/issues) to avoid duplicates
- Include:
  - Steps to reproduce
  - Expected vs actual behavior
  - Environment details (Node.js version, OS, etc.)

---

## Community

- Be respectful and inclusive in all interactions
- Follow the project's [Code of Conduct](CODE_OF_CONDUCT.md)
