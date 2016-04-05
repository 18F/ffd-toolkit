## Development standards for FFD Projects

This is a collection of the standards and style choices made by the developers on Federal Front Door. This aims to be an evolving document as the standards and styles likewise evolve, but should provide new developers on the project the information they need to quickly ramp up.

### GitHub

#### Branch vs. Fork

All development should be done on branches as opposed to personal forks.

#### Pull Requests and Merging

All development should be done on a branch – even typo fixes – before filing a PR against master. You must always get someone else to merge the PR for you. This ensures that every pull request gets some sort of review.

### Code Review

All PRs need to go through review by another person on the team – again, even typo fixes.

Code review is an important part of development, and should not be viewed as a chore by any of the parties involved. Both reviewing code and getting your code reviewed should be approached as something that will help the individual checkin, the project as a whole, and all of us as developers. `</rant>`

#### Things to look for in code review:
1. Does the code do what it claims to do?
1. Are there unit tests? Are they passing?
1. Do you understand what the code is doing? Remember, code is meant to be read by humans first.
    1. Do the variable names make sense?
    1. Has cleverness gotten in the way of clarity?
    1. Is the code documented?
1. Is the code idiomatic? This should be a softer requirement, but remember that for some languages (Python comes to mind) the notion of idiomatic code is a bit of a touchpoint.
1. Was the code linted? If not, it should be!

### Development Best Practices

Style holy wars aside, it's important to have a consistent set of style guidelines for a project for readability, ease of onboarding, and for maintenance. The following style guides should be used for all FFD projects, and you should totally set up linting in your editor so the rules become second nature.

#### Editor

Regardless of which editor you like to use, most text editors have the ability
to set a lot things like `line-endings` and whether or not an indentation
character is a `space` or a `tab`. [EditorConfig] [editor-config] is a python
library which helps standardize these settings between various editors in one
place. This repository includes a generic `.editorconfig` file. Use this file to
setup your text editors across your team.

[editor-config]: http://editorconfig.org/#download "EditorConfig: Download a plugin"

#### Python

Use Python 3! Use [Flake8](https://pypi.python.org/pypi/!)!

#### Ruby

#### JavaScript

For working with JavaScript on the server, use a version of NodeJS greater than
or equal to `5.5.0`. When using `npm`, use a version greater than or equal to
`3.0.0`.

Use `eslint` to lint your JavaScript files and enforce code style and
conventions for the team. This repository includes a generic `.eslintrc` file.
Use this file to setup your JavaScript linting across your team.

#### CSS / Sass

Use the [18F Frontend Guild CSS Style Guide](https://pages.18f.gov/frontend/css-coding-styleguide/).

For Sass files, please use the [`.scss-lint.yml`] [18f-lint-scss] file recommended
from the style guide link above.

[18f-lint-scss]: https://raw.githubusercontent.com/18F/frontend/18f-pages-staging/.scss-lint.yml "18F Frontend CSS Styleguide .scss-lint.yml file"
