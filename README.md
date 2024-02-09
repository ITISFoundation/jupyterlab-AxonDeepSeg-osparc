# 

AxonDeepSeg in JupyterLab

## Usage

```console
$ make help

$ make build
$ make run-local

```

## Workflow
1. The [Dockerfile](jupyter-axondeepseg/src/Dockerfile) shall be modified to install additional packages and/or Jupyter kernels
2. The [.osparc](.osparc) is the configuration folder and source of truth for metadata: describes service info and expected inputs/outputs of the service.
3. The service docker image may be built with ``make build`` (see usage above)
4. The service docker image may be built with ``make run-local`` (see usage above)
5. If the image works correctly, you'll be able to access the JupyterLab interface in your browser at ``localhost:8888``

## Have an issue or question?
Please open an issue [in this repository](https://github.com/ITISFoundation/cookiecutter-osparc-service/issues/).
---
<p align="center">
<image src="https://github.com/ITISFoundation/osparc-simcore-python-client/blob/4e8b18494f3191d55f6692a6a605818aeeb83f95/docs/_media/mwl.png" alt="Made with love at www.z43.swiss" width="20%" />
</p>
