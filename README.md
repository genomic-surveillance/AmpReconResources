# AmpliconResources

This repository contains any auxillary data required to run [AmpSeq pipeline](https://gitlab.internal.sanger.ac.uk/malariagen1/ampseq-pipeline.git)

## Getting started

To use this submodule in your project use these commands:

```shell
# Add the scripts submodule as a folder called "modules"
git submodule add https://gitlab.internal.sanger.ac.uk/malariagen1/ampliconresources.git
git commit -am "added scripts submodule"
# push optional at this stage, but definitely necessary after a few commits have been made
git push
```

### Cloning a repository that uses this submodule
```shell
git clone --recurse-submodules <your repo>

# Or if you've already cloned and just need to pull the submodules
submodule update --init --recursive
```

## Updating this submodule to latest commit on your repository
Create a new feature branch specifying the module you want to create/update.
After your work is done, create a pull request vs master.
Once that's been reviewed and merged, run:
```shell
git submodule update --remote
```
**A word of warning**, this will update all submodules in your repo (if you have more than one).
To only update this submodule, run the following instead:
```shell
cd modules
git fetch
git merge origin/master
cd ..
```
