# GitFlow Workflow Overview
## What is GitFlow?
GitFlow is a branching model for Git, developed by Vincent Driessen, that defines a strict branching model designed around the project release cycle. It is widely used in software development to manage features, releases, and hotfixes.
The primary goal of GitFlow is to manage complexity in software development by using well-defined branches for various stages of the project, allowing for organized collaboration and deployment.
## Key Branches in GitFlow
GitFlow defines five primary branches:
1. *main (or master)*:
   - This branch holds the stable, production-ready code.
   - All releases and hotfixes are eventually merged into this branch.
2. *develop*:
   - This branch is where the development of features and the next release occurs.
   - All new development should start from here.
   - This branch will eventually be merged into main when it's time for a release.
3. *feature branches*:
   - Used for developing new features.
   - Branch off from develop and should be merged back into develop once the feature is complete.
   - Naming convention: feature/<feature-name>
4. *release branches*:
   - Used for preparing a new production release.
   - Created from the develop branch when the development for a release is complete.
   - Allows for final bug fixes and testing before merging into main.
   - Naming convention: release/<version-number>
5. *hotfix branches*:
   - Used to quickly patch production releases in the main branch.
   - Created from the main branch when critical issues or bugs need to be addressed.
   - After fixes are made, hotfixes are merged back into both main and develop.
   - Naming convention: hotfix/<version-number>
## Workflow Overview
### 1. Start a New Feature
- Create a new feature branch from develop:
  ```bash
  git checkout develop
  git checkout -b feature/<feature-name>