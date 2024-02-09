# AxonDeepSeg GUI on o²S²PARC

![](https://github.com/axondeepseg/axondeepseg/blob/master/docs/source/_static/logo_ads-alpha.png?raw=true)

This repository packages AxonDeepSeg as part of a JupyterLab Service on o²S²PARC. It also adds support for pytorch+GPU/CUDA.

AxonDeepSeg is an open-source software using deep learning and aiming at automatically segmenting axons and myelin sheaths from microscopy images. It performs 3-class semantic segmentation using a convolutional neural network. AxonDeepSeg was developed at NeuroPoly Lab, Polytechnique Montreal, University of Montreal, Canada. See [GitHub repository](https://github.com/axondeepseg/axondeepseg/) and [Documentation](https://axondeepseg.readthedocs.io/en/latest/index.html) for more information.

The base of the Service was built with the [cookiecutter-osparc-ui-module](https://git.speag.com/oSparc/cookiecutter-osparc-ui-module), using [supervisord](http://supervisord.org/), [xtigervnc](https://tigervnc.org/), [novnc](https://novnc.com/info.html) and [openbox](http://openbox.org/wiki/Main_Page)

## Citation

If you use this work in your research, please cite:

Zaimi, A., Wabartha, M., Herman, V., Antonsanti, P.-L., Perone, C. S., & Cohen-Adad, J. (2018). AxonDeepSeg: automatic axon and myelin segmentation from microscopy data using convolutional neural networks. Scientific Reports, 8(1), 3816. [Link to the paper](https://doi.org/10.1038/s41598-018-22181-4).

## How to develop this o²S²PARC Service

### Usage

Build the module:
```console
$ make build
```
To run locally at and visit http://127.0.0.1:8888
```console
make run-local
```
To publish in local throw-away registry:
```console
make publish-local
```


### Versioning
Service version is updated with ``make version-*``

### CI/CD Integration 
A template ci config file is created in ```.github/workflows/check-image.yml```, it checks that the image builds. When the workflow runs successfully for a new version (on the main branch), this is automatically detected and published on the internal registry (see also "Deployment on o²S²PARC" in this README)

### Deployment on o²S²PARC

The required CI is already packaged.
To build and push to the internal registry you must add it to the [oSparc/docker-publisher-osparc-services](https://git.speag.com/oSparc/docker-publisher-osparc-services) repository.

## How to test the Application
Run locally and visit http://127.0.0.1:8888:
```console
make run-local
```
Or publish it in a local o²S²PARC deploy:
```console
make publish-local
```
Perform a test segmentation as shown in this [video tutorial](https://youtu.be/zibDbpko6ko). You can use as input the image from this repository (from ```validation/inputs/input_1```) or others provided by AxonDeepSeg (e.g. [in this repository](https://github.com/axondeepseg/default-SEM-model/tree/main/model_seg_rat_axon-myelin_sem/data_test)). The input folder will be mounted in ```tmp/inputs```

## Changelog


### [1.0.0] - 2023-12-22
First version
