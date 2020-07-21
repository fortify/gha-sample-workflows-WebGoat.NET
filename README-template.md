# Use existing repository as a template

This repository provides scripts and resources that allow any Git repository to
be used as a template for a derived repository. 

For example, the following steps can be used to create a new repository that is derived 
from https://github.com/fortify-sample-eightball.git:

1. `mkdir derivedRepo && cd derivedRepo && git init`  
  Set up new, empty repository and `cd` into this new repository
2. `git pull https://github.com/rsenden/repo-as-template.git`  
  Pull the contents of the `repo-as-template` repository
3. `./repo-as-template/setup.sh https://github.com/fortify/sample-eightball.git`  
  Pull the contents of the repository that we want to derive from, and configure this repository as a derived repository
4. Update README.md in the root of the repository to describe your project
5. `git add README.md && git commit -m "Updated README.md"`  
  Commit your updated README.md file
	
After initial set-up, the following utility scripts are available:
* `./run-after-clone.sh`: This script should be run whenever the repository has been cloned into a new local repository
* `./repo-as-template/pull.sh`: This script pulls any changes from the original repository into the current repository
    * Based on `.gitattributes` in the repository root, README.md will be ignored during merges





