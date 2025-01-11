## Welcome to "Hello World" with GitHub Actions and Azure Pipelines

This project demonstrates how to set up and use GitHub Actions and Azure Pipelines for continuous integration and deployment.

### GitHub Actions

The GitHub Actions workflow is defined in `.github/workflows/main.yml`. It triggers on every push to the repository and performs the following steps:
- Checks out the repository using `actions/checkout@v2`.
- Caches the node modules to speed up subsequent runs.
- Runs a custom action located in `./action-a` with the environment variable `MY_NAME` set to "Mona".

### Azure Pipelines

The Azure Pipelines configuration is defined in `.azure/pipelines/main.yml`. It triggers on every push to the master branch and performs the following steps:
- Uses the latest Debian container image.
- Caches the npm dependencies to speed up subsequent runs.
- Runs a custom script located at `action-a/entrypoint.sh` with the environment variable `MY_NAME` set to "Johnny".

### Getting Started

To get started with this project:
1. Clone the repository.
2. Make sure you have the necessary permissions to run GitHub Actions and Azure Pipelines.
3. Customize the workflows and scripts as needed.

**Ready to get started? Navigate to the first issue.**