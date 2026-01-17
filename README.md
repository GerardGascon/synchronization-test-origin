# Synchronization Test

An experiment to synchronize two repos via automated PR creation.

## Setup

1. Create a Fine-grained personal access token with these permissions:
    - First select the repository for the PR
    - Pull requests (Read and write)
    - Contents (Read and write)
2. Add the token to the repository secrets under the name: `DEST_REPO_TOKEN`
3. Update the environment variables for the GitHub Action:
    - DEST_REPO: the repo url name (i.e. synchronization-test-destination)
    - DEST_REPO_OWNER: the owner of the repository (i.e. GerardGascon)
    - DEST_REPO_BRANCH: the branch that the PR will target
    - ORIGIN_PATH: folder from the original repository from which to gather the contents for the PR (i.e.
      folder-to-synchronize)
    - DEST_PATH: the path from the target repository in which the files will be located (i.e. folder-synchronized)
    - PR_MESSAGE: The title of the PR
4. Update the Action trigger wildcard. Use whatever fits your use case.