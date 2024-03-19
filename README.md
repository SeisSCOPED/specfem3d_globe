# Container Template
This repository is a template repo for containers built on the [base containers](https://github.com/SeisSCOPED/container-base).


There are multiple dockerfiles corresponding to the platforms and the utilities preinstalled, and they are triggered to build automatically when changes are made on the base containers. Here are the steps to build a new container repo from the base containers:


1. Create a new repository: When creating a new repo, select "SeisSCOPED/container-template" as the repository template. The new repo will copy all the template dockerfiles and workflow files.


2. Change the name of packages: In your new repo, go to .github/workflows, and set the environment variable "IMAGE_NAME" to an appropriate name for your images.


3. Make changes: Add your new layers on the dockerfiles.

