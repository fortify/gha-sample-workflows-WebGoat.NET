# Using the EightBall example project as a template

This section describes how to use this repository as a template for other repositories,
for example if you wish to add sample pipelines/workflows/... that demonstrate how to 
scan the EightBall application in a particular CI/CD environment.

Use the following steps to set up a new repository that is derived from this EightBall sample project:

1. Create new, empty Git repository
2. Pull the contents of the main sample repository:
    * `git pull https://github.com/fortify/sample-eightball.git`  
3. Configure repository, commit some useful scripts, and add new README.md
    * `template/setup-derived.sh`
4. Update README.md in the root of the repository to describe your project
5. Commit your updated README.md file:
    * `git commit -m "Updated README.md" README.md
	
After initial set-up, the following utility scripts are available:
* `run-after-clone.sh`: This script should be run whenever the repository has been cloned into a new local repository
* `template/pull.sh`: This script pulls any changes from the main EightBall sample project into the current repository
    * Based on `.gitattributes` in the repository root, README.md will be ignored during merges





