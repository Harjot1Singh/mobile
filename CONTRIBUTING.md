# Contributing Guildeines

We're glad you're interested in contributing!

## Style

This repository follows the **Airbnb's Javascript Style Guide**, with a few minor modifications. Notably, spaces should be included inside parentheses and brackets (weird, right!).

An ESLint file is provided,
and your code will automatically be checked on-commit for style.
It is recommended to install an ESLint plugin for your editor (VS Code's `ESLint` plugin works out of the box), so you can receive linter suggestions as you type.

## Commit Message Guidelines

Each commit message consists of a header, body, and footer. The header has a special format that includes a type, scope, and subject:

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
````

The header's type and subject is mandatory, while it's scope is optional.

Any line of the commit message cannot be longer than 100 characters! This allows the message to be read easily on GitHub as well as in various git tools.

The footer should contain references to any issues, such as `Closes #21` or `Related #75`.

Using keywords in the footer, such as `Close, Closes, Fix, Fixes #32`, will automatically close an issue when the corresponding commit is merged.

Examples:
```
docs(readme): add contributing guidelines
```
```
fix(backend): synchronise state with frontend

The backend would not send all required data to the frontend.

Fixes #53
```

### Revert
If the commit reverts a previous commit, it should begin with `revert:` , followed by the header of the reverted commit. In the body it should say: `This reverts commit <hash>.`, where the hash is the SHA of the commit being reverted.

Example:
```
revert: docs(readme): add contributing guidelines

This reverts commit 18db94aed359fdea.
```

### Type

Must be one of the following:

- *build*: Changes that affect the build system or external dependencies (example scopes:  -gulp, broccoli, npm)
- *ci*: Changes to our CI configuration files and scripts (example scopes: Circle,  -BrowserStack, SauceLabs)
- *docs*: Documentation only changes
- *feat*: A new feature or enhancement, always an addition or improvement
- *fix*: A fix, usually bugs, but also incorrect data
- *perf*: A code change that improves performance
- *refactor*: A code change that neither fixes a bug nor adds a feature, changing nothing for a user
- *style*: Changes that do not affect the meaning of the code (white-space, formatting,  -missing semi-colons, etc)
- *test*: Adding missing tests or correcting existing tests

**Note:** Typos are always mistakes, and therefore fixes. Additions/enhancements to content are features.

### Scope

The scope should be the name of the npm package affected (as perceived by the person reading the changelog generated from commit messages.

The following is the list of supported scopes:

- There are currently no scopes

There are currently a few exceptions to the "use package name" rule:

- *none/empty string*: useful for `style`, `test`, and `refactor` changes that are done across all packages (e.g. style: add missing semicolons) and for docs changes that are not related to a specific package (e.g. docs: fix typo in tutorial).

### Subject

The subject contains a succinct description of the change:

- use the imperative, present tense: "change" not "changed" nor "changes"
- don't capitalize the first letter
- no dot (.) at the end

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes". The body should include the motivation for the change and contrast this with previous behavior.

### Footer
The footer should contain any information about **Breaking Changes** and is also the place to reference GitHub issues that this commit Closes.

Breaking Changes should start with the word `BREAKING CHANGE:` with a space or two newlines. The rest of the commit message is then used for this.

