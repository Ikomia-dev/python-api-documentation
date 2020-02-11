# python-api-documentation
API documentation to create plugins for Ikomia platform in Python

The aim of this API is to offer a simple interface to add user-defined plugin into the Ikomia platform. A plugin is the Python implementation of an algorithm executed on image based data.

The software gives the possibility to build custom image processing pipelines through the use of a graph-based editor called workflow. A workflow is thus composed of several connected tasks that get inputs, process it and gives results through outputs. When you create your own task (ie plugin), there are some few essential components to deal with:

- Task: algorithm implementation
- Parameters: to setup the algorithm
- Metadata: information attached to the task (description, icon, authors, articles…)
- Inputs: input data the task requires
- Outputs: output data the task produces
- Widget: allows user interaction (to adjust parameters for example)

Each of this components is implemented by a specific class. We use inheritance and factory design pattern to build the interface between Ikomia software and plugins. Once implemented, you will be able to handle your plugin like all others internal process. It means that you will be able to add it to a workflow and visualize your outputs directly.
