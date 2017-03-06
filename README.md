# MATLAB.devTools - Contribute the smart way

Making a contribution to any `git` repository from `MATLAB` is straightforward.

[![asciicast](https://asciinema.org/a/e4n0qtwmip3xfsyod97e7i16l.png)](https://asciinema.org/a/e4n0qtwmip3xfsyod97e7i16l)

## Pre-requisites

Please follow the [configuration instructions](PREREQUISITES.md) for the first time. You may skip this if your system is already set up and you have `git` configured. Please ensure that
```
$ git config --list
```
contains `user.name` and `user.email` set to `yourGitHubUsername` and `first.last@server.com` with your respective credentials.

## How can I contribute?

Type in `MATLAB` within the `devTools` folder:
```
>> contribute
```

You will then be presented by a menu:
```
   [1] Initialize a contribution.
   [2] Continue a contribution.
   [3] Submit/publish a contribution.
   [4] Delete a contribution.

-> Please select what you want to do (enter the number):
```

The first time, the original repository will be downloaded (cloned), and you will be asked to specify a folder in which this copy will be downloaded to. The folder will be named `fork-gitRepoName`.

Please note that **only files that are in the `fork-gitRepoName` folder** will be considered for contribution. Any changes made to a downloaded official `git` repository will be ignored by the system.

Once you submit your contribution (menu item 3), you will be presented with a link that leads you directly to the pull request (PR). You may then fill out the form and submit the PR.

**Note 1:** You can abort any process using CTRL-C.

**Note 2:** In order to speed up the review process, please initiate a contribution per theme/topic/feature/bug fix that you work on. Please don't mix features and think of an explicit name for your contribution, i.e. `bug-fix-solveCobraLP` or `add-tests-FBA`. Avoid generic names, such as `my-great-feature` or `fix` or `contribution-myName`.

## Contributing to The COBRA Toolbox

In order to start contributing, follow the [installation instructions](https://github.com/opencobra/cobratoolbox/blob/master/README.md) of The COBRA Toolbox. If you don't want to get your hands dirty right away, start-off by reading the [Contributing Guide](https://github.com/opencobra/cobratoolbox/blob/master/.github/CONTRIBUTING.md).

## Check the history of a file

At any time, you can check the history of a file by typing in MATLAB:
```
>> history('fileName.m')
```

## Turn on the verbose mode

If you encounter a problem, or suspect that something is not behaving properly, please run:
```
>> contribute(true)
```
and follow the process as normally. Alternatively, you can set `gitConf.verbose = true;` in `assets/confDevTools.m`.

## Resolve unexpected behavior - reset

If you encounter unexpected behavior, please try to reset the `devTools` with:
```
>> resetDevTools
```

If you have files or changes that appear and would like to reset your local fork (without re-cloning) again, type:
```
>> resetLocalFork
```
