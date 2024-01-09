helm charts
===========

## How to develop
1. install [helm](https://helm.sh/docs/intro/install/) & [taskfile](https://taskfile.dev/#/installation)

2. cd into chart folder. example:
    ```bash
    cd helm/generic/
    ```

3. (optional) choose an value files:
    ```bash
    export VALUES=examples/statefulset.yaml
    ```

4. generate/build chart locally
    ```bash
    task helm:gen

    # charts will generate into ./build folder
    # to clear it
    task helm:clean
    ```

5. apply/show changes in k8s cluster
    ```bash
    # show changes
    task helm:diff

    # apply changes (or install)
    task helm:apply

    # uninstall helm release
    task helm:destroy
    ```
