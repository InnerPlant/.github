# Best Practices for InnerPlant Software Development

### Table of Contents

1. [Naming](#Naming-Convention)
2. [Readmes](#README)
3. [Issues](#Issues)
4. [Tests](#Tests)
5. [Pull Requests](#Pull-Requests)
6. [Versioning](#Versioning)
7. [Project Requirements Doc](#Project-Requirements)
8. [Tools](#Tools)

---

#### Naming Convention

Name your repo something descriptive. Use only lowercase letters and dashes. No underscores unless you ***really*** need them, please!

Be sure to fill out the *About* section on the right-hand side so people can see a quick overview of the contents without having to click into the repo.

---

#### README

A README is a very important piece of your repository - it's the first thing someone will read about your code, and should help be a primer for understanding what it does and how it works. Find a template README [here](https://github.com/InnerPlant/.github/blob/main/readme-template.md).

Here are some sections to consider including when creating a README. This is flexible, so modify as needed:

1. **Project Overview**: Begin with a brief overview of your project. Explain what the project does, its purpose, and why it's valuable. This section should give readers a high-level understanding of what your project is about.

2. **Installation Instructions**: Provide clear, step-by-step instructions on how to install and set up your project. Include any dependencies that need to be installed and specify the supported platforms.

3. **Usage**: Explain how to use your project. Provide code examples or usage scenarios to help users understand how they can interact with your project. This section should guide users on how to get the most out of your project. If this is deployed on the cloud somewhere, provide a link (and consider putting it at the top of the README and in the about section as well) 

4. **Configuration**: If your project requires configuration, explain how users can configure it to suit their needs. Include information about configuration files, environment variables, or any other settings users might need to adjust.

5. **Documentation**: Link to comprehensive documentation if available. Even if the README covers the basics, having detailed documentation provides additional clarity and helps users dive deeper into your project.


Remember to keep your README concise, well-organized, and easy to read. If you have a lot of documentation that won't fit in a README, consider creating docs in the [InnerPlant Software Wiki](https://sites.google.com/innerplant.com/innerwiki/software).

---

#### Issues

Issues can essentially just be a to-do list for the project. It's best to keep issues small and specific. They should be bite-sized tasks that can be completed in a day or two.

We recommend using [GitHub Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects) for tracking and collborating on issues. The Kanban board is particularly useful.

---

#### Tests
Writing tests is a GREAT way to ensure that contributors don't break code. We should do more of it. CircleCI has a [really nice blog post](https://circleci.com/blog/test-driven-development-tdd/) on Test-Driven Development. We probably don't need to be that hardcore. Here are a few loose best practices:

1. **Define Clear Testing Objectives**: Clearly define the objectives of your software testing efforts. Understand what aspects of the software you need to test, what quality attributes are most important, and what risks you want to mitigate through testing.

2. **Start Testing Early**: Begin testing as early as possible in the software development lifecycle. Testing early helps identify issues sooner, making them easier and cheaper to fix.

3. **Use a Combination of Testing Techniques**: Employ a combination of testing techniques, including unit testing, integration testing, and system testing Each type of testing focuses on different aspects of the software and helps ensure comprehensive test coverage.

4. **Automate Testing Wherever Possible**: Automate repetitive and time-consuming tests to increase efficiency and reduce manual effort. Automated testing can be particularly beneficial for regression testing, where you need to ensure that changes haven't introduced unintended side effects.

5. **Prioritize Tests Based on Risk and Impact**: Prioritize tests based on the level of risk and potential impact on the software's functionality and users. Focus more testing effort on critical and high-risk areas to ensure that they are thoroughly tested.

6. **Test in Different Environments**: Test your software in various environments to ensure compatibility and reliability across different platforms, operating systems, browsers, and devices. This includes testing in development, staging, and production environments.

---

#### Pull Requests

Code review is always a good idea. Consider using Pull Requests and tagging a couple of other collaborators whenever you want to merge a series of commits into the active branch. Here are a few best practices:

1. **Create Descriptive Titles**: Use clear and descriptive titles for your pull requests. A good title summarizes the changes introduced by the PR.

2. **Provide Context**: In the PR description, provide context about the changes made, why they are necessary, and any related issues or tasks.

3. **Keep PRs Small and Focused**: Avoid bundling unrelated changes into a single PR. Keep PRs small, focused, and addressing a single concern or feature.

4. **Follow Coding Conventions**: Adhere to the project's coding style and conventions. Consistent code makes reviewing easier and maintains code quality.

5. **Write Meaningful Commit Messages**: Write clear and concise commit messages that describe the purpose of each commit. This helps reviewers understand the changes at a glance.

6. **Run Tests Before Submitting**: Ensure that all tests pass before submitting the PR. Running tests locally helps catch issues early and demonstrates that the changes are functional.

8. **Rebase Your Branch**: Before merging, rebase your branch onto the latest main branch to incorporate any changes and resolve conflicts.

9. **Avoid Force-Pushing**: Avoid force-pushing to your branch after pushing changes to a shared repository. Force-pushing can disrupt the work of collaborators and lead to data loss.

10. **Close Related Issues**: Once the PR is merged, consider assigning and closing related issues to keep the project's issue tracker organized and up-to-date. 

---

#### Versioning

[Semver](https://semver.org/) is a widely accepted standard, so we'll use it. Versioning should be notated somewhere in the *pyproject.toml* (for Poetry projects) or in the version section in the GitHub Repo.

Given a version number **MAJOR.MINOR.PATCH**, increment the:
1. **MAJOR** version when you make incompatible API changes
2. **MINOR** version when you add functionality in a backward compatible manner
3. **PATCH** version when you make backward compatible bug fixes

Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

---

#### Project Requirements Documentation

Find a template [here](https://docs.google.com/document/d/16rlG2PMNmhj8rH4q4BryuydS9yjCwQJGWo11tVci-AU/edit).

This is less about GitHub usage and more just a best practice for any large projects. PRDs are linked to several of the newer projects here -- have a look to see how helpful they can be!

---

#### Tools

There are a lot of great tools out there, and it would be great for us to use a unified toolchain wherever possible for better fluency. Here's a running list of the ones we've found helpful. Most are in Python, but feel free to add from in any language. 

- **[Poetry](https://python-poetry.org/)** Python Packaging and dependency management.
- **[Ruff](https://docs.astral.sh/ruff/)** An extremely fast Python linter and code formatter.
- **[PyTest](https://docs.pytest.org/en/8.2.x/)** Testing framework for Python.
- Add some more!



