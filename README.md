# python-api-documentation
Python API documentation to create plugins for the Ikomia platform

Consult the documentation [here](https://ikomia-dev.github.io/python-api-documentation/).

The aim of this API is to offer a simple interface to add user-defined plugin into the Ikomia platform. A plugin is a Python implementation of an algorithm executed on image based data.

The software gives the possibility to build custom image processing pipelines through the use of a graph-based editor called workflow. A workflow is thus composed of several connected tasks that get inputs, process them and give results through outputs. When you create your own task (i.e. plugin), there are some few essential components to deal with:

- Task: algorithm implementation
- Parameters: to setup the algorithm
- Metadata: information attached to the task (description, icon, authors, articles…)
- Inputs: required input data
- Outputs: produced output data
- Widget: user interaction interface (to adjust parameters for example)

Each of these components is implemented by a specific class. We use inheritance and factory design pattern to build the interface between Ikomia software and plugins. Once implemented, you will be able to handle your plugin like all others internal processes. It means that you will be able to add it to a workflow and visualize your outputs directly.
