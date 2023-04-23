# Contribution guidelines

Welcome to the contributing guidelines.We appreciate your interest in helping us improve and evolve the UZH BCC DAO. This document outlines the steps and best practices for contributing to our open-source project.

Contributions can take many forms, including bug fixes, feature enhancements, documentation improvements, and more. By contributing to our project, you will help the community to create a better DAO for everyone.

![Coding in Swiss landscape](/static/cover.png "Coding in Swiss landscape")

## Good development practices

### Share early, share Often

We believe in the "share early, share often" approach, which involves announcing your plans before starting work and breaking your changes into small, easily reviewable commits following the [Ideal git commit structure](#ideal-git-commit-structure).

Announcing plans before starting work avoids duplication and ensures consistency with the existing architecture. This minimizes the chance of rejected changes and reduces time spent rebasing and keeping up with the main code base.

It is important to note that significant changes to the codebase or the addition of new features must be proposed and decided upon through our DAO governance process. This ensures that all members of the community have a say in the direction of the project and that decisions are made transparently and democratically.

### Don't trust, verify and test

To ensure accurate and bug-free code, we aims for a high test coverage using various test frameworks. New code must be accompanied by tests for correct behavior and error handling (if applies), while bug fixes must have corresponding tests to prove resolution and prevent future regressions.

### Document and comment

Developers spend more time reading code than writing it, making code documentation and commenting essential. All functions must be commented with their purpose and any assumptions they make. A good practice is to assume no prior knowledge of the code and ask if the comment provides enough information on the function's purpose and usage.

## Ideal git commit structure

We prefer small, self-contained commits in pull requests, rather than large commits that modify multiple files or packages. Commits should contain isolated changes within a single package that follows the structure inspired by Angular's Contribution Guideline.

### Commit message format

To ensure an easily readable commit history, we adhere to specific rules for formatting Git commit messages. Each commit must contain a concise and descriptive header with the following structure:

```
<type>(<scope>): <short summary>
  │       │             │
  │       │             └─⫸ Summary in present tense. Not capitalized. No period at the end.
  │       │
  │       └─⫸ Commit Scope
  │
  └─⫸ Commit Type: build|ci|docs|feat|fix|refactor|test
```

The `<type>` must be one of the following:

- **build**: Changes that affect the build system or external dependencies.
- **ci**: Changes to our CI configuration files and scripts.
- **docs**: Documentation only changes.
- **feat**: A new feature.
- **fix**: A bug fix.
- **refactor**: A code change that neither fixes a bug nor adds a feature.
- **test**: Adding missing tests or correcting existing tests

The scope should be the name of the module affected (as perceived by the person reading the changelog generated from commit messages).

The following is the list of supported scopes:

- `Common`

### Sign your commits

Signing git commits is also recommended to ensure tree integrity. To sign a commit, provide the -S flag (or `--gpg-sign`) to git commit when you commit your changes, for example:

```shell
git commit -m "Commit message" -S
```

You can also choose to specify a particular key by adding a key id after the -S option when signing. If you prefer to auto-sign all commits in `git`, you can add the following lines to your `~/.gitconfig` file:

```text
[commit]
        gpgsign = true
```

To verify if your commit is signed, use:

```shell
git log --show-signature
```

## Submitting a pull request

To contribute to the code, please follow these steps:

1. Search for an open or closed PR that relates to your submission.
2. Be sure that an issue describes the problem you're fixing, or documents the design for the feature you'd like to add.
3. Fork this repository to your own account.
4. Clone the forked repository to your local machine.
5. Create a separate branch using a clear name that describes what your are doing (example: `feat/feature-name`).
6. Make your changes and commit them with clear and concise commit messages following the [Ideal git commit structure](#ideal-git-commit-structure).
7. Ensure that your code is thoroughly documented and tested.
8. Push your changes to your forked repository.
9. Create a new pull request (PR) with your changes and await review.
10. Your PR may be accepted, rejected, or require changes before being accepted.
11. Once your PR has been reviewed and approved, we will merged your work into the main branch.

## Code Aproval Process

This code is crucial for the UZH BCC DAO functioning and is open-source, but changes and new features require approval from the community and official maintainers (from the technical side).

Code review times can vary based on factors such as the size and complexity of the contribution and adherence to guidelines. The review ensures code stability and security, proper API usage, and alignment with the overall architecture.

Following the code review, if no issues are found, your change will be accepted immediately. However, if there are concerns or questions, you will receive feedback and instructions for the next steps needed to merge your contribution. Sometimes, code reviewer(s) or interested committers may assist you in modifying the code, but usually, you will only be given feedback for you to make the required changes. This process will continue until your code is accepted.

## Acknowledgements

This document drew significant inspiration from similar guidelines created by [btcsuite](https://github.com/btcsuite), [lnd](https://github.com/lightningnetwork/lnd), [Effective Go](https://go.dev/doc/effective_go), and [Angular](https://github.com/angular/angular/blob/main/CONTRIBUTING.md).
