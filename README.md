# Docker Builder

A Concourse pipeline for building a Docker image and pushing it to dockerhub. The pipeline doesn't require pushing the Dockerfile to any resource as it loads it in the set pipeline

1. Create a `secrets.yml` containing your dockerhub credentials:

    ```yaml
    username:
    password:
    ```

1. Given that you are logged into a Concourse installation, use `set_pipeline`:

    ```sh
    ./set_pipeline $CONCOURSE_TARGET $DESTINATION path/to/Dockerfile
    ```

    i.e.

    ```sh
    ./set_pipeline lite user/empty-image Dockerfile
    ```

1. Unpause pipeline and trigger manually.
