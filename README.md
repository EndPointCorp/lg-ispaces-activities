# Overview
This repository houses a repo manifest and some VERY basic instructions for cloning, building, and using the Liquid Galaxy activities for systems powered by Interactive Spaces.

# Prerquisite Setup
These activities are written for the Interactive Spaces(IS) platform. As such, you should install an IS Master, Controller, and Workbench. Begin with the documentation found here: http://www.interactive-spaces.org/home/documentation and familiarize yourself with the very helpful PDF included with every IS release: http://www.interactive-spaces.org/home/releases

# Cloning all Liquid Galaxy Activities
For developer convenience, this repo houses a manifest for use with Google's tool called "git-repo" (https://gerrit.googlesource.com/git-repo/).

Expect the default manifest to reference both production-quality activity repositories with few known bugs **and** bleeding-edge, experimental activities with show-stopping bugs.

Use **repo** as follows to initialize your IS Workbench:
```
$ cd path/to/workbench
$ repo init -u git@github.com:EndPointCorp/lg-ispaces-activities.git
```
Then, use the following command to get a working directory for repository in the manifest:
```
$ repo sync
```
Now you can build the activities. Some activities may require an extra setup step, or two, reference the README within each activity repository for more information.

# Two quick examples for Activity Building
## Building a single activity
```
$ cd path/to/workbench
$ ./bin/isworkbench.bash com.endpoint.lg.foo clean build
```

## Building all the activities in the workbench
```
$ cd path/to/workbench
$ ./bin/isworkbench.bash ./ walk clean build
```
Reference the IS documentation for more information about the workbench, including generating IDE information.

# Contributing
GitHub issue trackers are available for each activity individually. Feel free to contribute to the issues, discussion, or submit pull requests. Currently, we are in special need of help with per-activity documentation to make it easy for newly-interested parties to try the activities.
