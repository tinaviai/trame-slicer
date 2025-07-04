# trame-slicer

![Welcome to trame-slicer](https://raw.githubusercontent.com/KitwareMedical/trame-slicer/main/docs/trame-slicer-medical-app-example.png)

trame-slicer is a Python library bringing
[3DSlicer](https://github.com/Slicer/Slicer/) components in trame as a
composable library.

It uses 3D Slicer\'s python wrapping and adds a thin wrapping to make it
available with the [trame framework](https://github.com/Kitware/trame/).

## Warning

As the 3D Slicer Python wheel is not yet generated by the 3D Slicer CI, manually
generated wheels are provided for Python 3.10 for Windows and Linux WSL.

The API has not been stabilized / reviewed by the 3D Slicer core developers so
please use this library with caution.

## Installing

The library can be installed as follows :

- Setup a Python 3.10 environment
- Activate your environment
- Git clone the library
- cd into the library
- Use the [pip install -e . command]{.title-ref} to install the library along
  it\'s dependencies
- Copy the vtk_mrml wheel file matching your OS
- Pip install the wheel using the find links command (see below)

```console
pip install -e .
pip install vtk_mrml-9.4.0-cp310-cp310-win_amd64.whl  --find-links . # Windows
pip install vtk_mrml-9.4.0-cp310-cp310-manylinux_2_35_x86_64.whl  --find-links . # Linux WSL
```

## Getting started

To get started using trame, please have a look at the
[introductory trame course](https://kitware.github.io/trame/guide/intro/course.html).

To start using the trame-slicer library, have a look and run the
[medical viewer app](examples/medical_viewer_app.py)

## Features

The following subset of 3D Slicer features are currently supported :

- (limited) file loading
- Volume files (DCM, NRRD, NIFTI, \...)
- Model files (STL, OBJ)
- MRML / MRB files
- Segmentations (NRRD, NIFTI, \...)
- **Display**
  - 2D/3D with 3D Slicer UI manipulation
  - Volume Rendering preset / shift
- Bare bone access to 3D Slicer MRML scene and Core logic components

## Work in progress

To make it easier for users to use trame-slicer, the following work are in
progress :

- Slicer wheel generation merge into 3D Slicer\'s preview release
- CI changes to build the Slicer wheel along 3D Slicer\'s release
- 3D Slicer extension to install trame-slicer and launch a trame-slicer server
  directly from 3D Slicer

## Troubleshooting

If you get the following error:

`ImportError: cannot import name 'vtkMRMLDisplayableNode' from 'slicer' (XXX/lib/python3.10/site-packages/slicer/__init__.py)`

You might be using a statically compiled Python. Please switch to a shared
version of Python.

## Contributing

Contributions are welcomed, please follow the
[CONTRIBUTING.md](https://github.com/KitwareMedical/trame-slicer/blob/main/CONTRIBUTING.md)
file for more information.

## License

The library is distributed with a permissive license. Please look at the
[LICENSE](https://github.com/KitwareMedical/trame-slicer/blob/main/LICENSE) file
for more information.

## Acknowledgment

This library was funded by the following projects :

- [Cure Overgrowth Syndromes (COSY) RHU Project (ANR-18-RHUS-005)](https://rhu-cosy.com/en/accueil-english/).
- [Handling heterogeneous Imaging and signal data for analysing the Neurodevelopmental Trajectories of premature newborns (HINT) ANR project (ANR-22-CE45-0034)](https://anr-hint.pages.in2p3.fr/)

This library was created from the
[trame-cookicutter](https://github.com/Kitware/trame-cookiecutter/) library.

## Contact

If you are interested in learning how you can use trame-slicer for your use case
in the near future, or want to get an early start using the framework, don\'t
hesitate to [contact us](https://www.kitware.eu/contact/). Or reach out in the
[issue tracker](https://github.com/KitwareMedical/trame-slicer/issues) and
[3DSlicer discourse community](https://discourse.slicer.org/).
