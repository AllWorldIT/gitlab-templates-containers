# GitLab CI Docker Image Template

## Repository Format

DockerHub tag paths:
```
PROJECT_PATH:latest              ($CI_DEFAULT_BRANCH)
PROJECT_PATH:latest-$BRANCH      ($CI_COMMIT_BRANCH)
PROJECT_PATH:$TAG                (generally in the format of vX.Y.Z-R.R)
```

Our repository tag paths:
```
PROJECT_PATH:latest              ($CI_DEFAULT_BRANCH)
PROJECT_PATH:$timestamp          ($CI_DEFAULT_BRANCH)
PROJECT_PATH:$BRANCH/latest      (branch name will have leading v stripped)
PROJECT_PATH:$BRANCH/$timestamp  (branch name will have leading v stripped)
PROJECT_PATH:$TAG_NOREL/latest   (TAG_NOREL is leading v is removed, aswell as trailing -R.R release)
PROJECT_PATH:$TAG_NOREL/$TAG_REL (TAG_REL has only leading v removed)
```