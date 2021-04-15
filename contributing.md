# Contributing to AirQo

The following is a set of guidelines to contribute to AirQo-modules, which is
hosted on the [AirQo Organization](https://github.com/airqo-platform) on GitHub.

## Reporting issues

Reporting issues are a great way to contribute to the project. We are perpetually grateful about a well-written, thorough bug report.

Before raising a new issue, check our issue lists to determine if it already contains the problem that you are facing.

- [AirQo-frontend issues](https://github.com/airqo-platform/AirQo-frontend/issues)
- [AirQo-api issues](https://github.com/airqo-platform/AirQo-api/issues)
- [AirQo-modules issues](https://github.com/airqo-platform/AirQo-modules/issues)

A good bug report shouldn't leave others needing to chase you for more information. Please be as detailed as possible. The following questions might serve as a template for writing a detailed
report:

- What were you trying to achieve?
- What are the expected results?
- What are the received results?
- What are the steps to reproduce the issue?
- In what environment did you encounter the issue?

Before closing an issue, please ensure that you leave a comment describing the solution that solved that specific issue. This information can be extremely helpful to future contributors of the project.

## Pull requests

Good pull requests (e.g. patches, improvements, new features) are a fantastic help. They should remain focused in scope and avoid unrelated commits.

**Please ask first** before embarking on any significant pull request (e.g. implementing new features, refactoring code etc.), otherwise you risk spending a lot of time working on something that the maintainers might not want to merge into the project.

Please adhere to the coding conventions used throughout the project. If in doubt, consult the different style guides for the tech stack of the service you are contributing to.

To contribute to the project, [fork](https://help.github.com/articles/fork-a-repo/) it,
clone your fork repository, and configure the remotes:

```
git clone https://github.com/<your-username>/<repository-name>.git
cd AirQo-api
git remote add upstream https://github.com/airqo-platform/<repository-name>.git
```

If your cloned repository is behind the upstream commits, then get the latest changes from upstream:

```
git checkout master
git pull --rebase upstream master
```

Create a new topic branch from `master` using the naming convention `[type]-[issue/task-number/name]` to help us keep track of your contribution scope. The names should not exceed three words for easy readability. Make sure you use git merge instead of git rebase while updating your feature branch with the master - we just want to ensure that the integration of changes into the master branch is as simple as possible. We shall also have short lived branches.

```
git checkout -b issue-23
git checkout -b feature-adding-users
```

Commit your changes in logical chunks. When you are ready to commit, make sure to write a Good Commit Message. Ensure to group your commits into logical units of work before making it public.

Use your real name (sorry, no pseudonyms or anonymous contributions). If you set your `user.name` and `user.email` git configs, you can sign your commit automatically with `git commit -s`.

Locally merge (or rebase) the upstream development branch into your topic branch:

```
git pull --rebase upstream master
```

Push your topic branch up to your fork:

```
git push origin issue-[issue-number]
```

[Open a Pull Request](https://help.github.com/articles/using-pull-requests/) with a clear title and detailed description.

## Jira integration

If you are part of the core project team, please append your branches, pull requests and commit messages with the Jira card number you are working on e.g. for a branch

```
ch-merge-configs-PLAT-117
```

This will enable Jira to automatically link to your work in GitHub, making the information in Jira more valuable.

## Documentation

Documentation for the AirQo-modules repo is built automatically with Sphinx, using Google/PEP8 formatting for docstrings. https://www.python.org/dev/peps/pep-0008/