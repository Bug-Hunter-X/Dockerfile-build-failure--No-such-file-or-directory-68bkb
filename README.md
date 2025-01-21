# Dockerfile Bug: Missing File in Context
This repository demonstrates a common error in Dockerfiles: attempting to copy a file that is not present in the build context.  The Docker build process fails because it cannot find the specified file.

## Bug Description
The provided `Dockerfile` attempts to copy and run a file named `app.py`.  However, this file is not included in the directory sent to the Docker build process. This leads to a failure during the build stage.

## Solution
The solution involves ensuring that `app.py` (or whatever file you actually want to use) exists within the directory that's used when building the Docker image. 