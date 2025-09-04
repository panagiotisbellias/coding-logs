# Contributing Guidelines

Thank you for considering contributing to this project! 🎉\
We welcome contributions of all kinds, including bug reports, feature
requests, documentation improvements, and code.

------------------------------------------------------------------------

## Getting Started

Before contributing, please make sure you have: 
- A [GitHub account](https://github.com/join) 
- [Git](https://git-scm.com/) installed 
- [Node.js](https://nodejs.org/) (LTS recommended) 
- [npm](https://docs.npmjs.com/) or [yarn](https://yarnpkg.com/) installed

------------------------------------------------------------------------

## Setup

1.  **Fork** the repository on GitHub.

2.  **Clone** your fork locally:

    ``` bash
    git clone https://github.com/<your-username>/<repo-name>.git
    cd <repo-name>
    ```
    where repo-name is `coding-logs` except for the case you defined another name during fork process

3.  **Add the upstream remote** (to keep your fork up to date):

    ``` bash
    git remote add upstream https://github.com/EscamillaJuan/coding-logs.git
    ```

4.  **Install dependencies**:

    ``` bash
    npm install
    # or
    yarn install
    ```

------------------------------------------------------------------------

## Build Instructions

If the project uses **TypeScript**, you'll need to compile it before
running.

1.  Build the project:

    ``` bash
    npm run build
    # or
    yarn build
    ```

    By convention, this generates output in the `dist/` directory.

2.  For local development with automatic rebuild:

    ``` bash
    npm run dev
    # or
    yarn dev
    ```

------------------------------------------------------------------------

## Test Instructions

1.  Run all tests:

    ``` bash
    npm test
    # or
    yarn test
    ```

2.  Run tests with coverage:

    ``` bash
    npm run test:coverage
    # or
    yarn test:coverage
    ```

3.  Run linting to ensure code style:

    ``` bash
    npm run lint
    # or
    yarn lint
    ```

All tests **must pass** and lint checks should be clean before
submitting a pull request.

------------------------------------------------------------------------

## Pull Request Process

1.  Create a new branch:

    ``` bash
    git checkout -b feature/my-new-feature
    ```

2.  Make your changes and commit with a clear message:

    ``` bash
    git commit -m "feat: add my new feature"
    ```

    > We follow [Conventional Commits](https://www.conventionalcommits.org/) (recommended).

3.  Push your branch:

    ``` bash
    git push origin feature/my-new-feature
    ```

4.  Open a **Pull Request** against the `main` branch.

------------------------------------------------------------------------

## Code Style

-   Follow the existing code style.

-   Run the linter before committing:

    ``` bash
    npm run lint -- --fix
    ```

-   Keep commits focused and meaningful.

-   Include tests for new functionality whenever possible.

------------------------------------------------------------------------

## Reporting Issues

-   Search the [issue tracker](https://github.com/EscamillaJuan/coding-logs/issues) to avoid duplicates.
-   When opening a new issue, provide:
    -   Steps to reproduce
    -   Expected vs actual behavior
    -   Environment details (Node.js version, OS, etc.)

------------------------------------------------------------------------

## Community

-   Be respectful and inclusive in all interactions.
-   Follow the project's [Code of Conduct](CODE_OF_CONDUCT.md).
