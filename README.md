<img src="logo/MAML_logo.png" width="550px">

# Münster App Modeling Language

MAML is a framework for cross-platform development of native business apps using a graphical modeling language.

## Repository content
This repository contains the latest source code, which may be unstable.
MAML resides in the namespace de.wwu.maml and has the following packages:

* ~.dsl: MAML Ecore meta models
* ~.editor: MAML editor based on the [Eclipse Sirius](https://eclipse.org/sirius/) project
  * ~.design: The editor and its services
  * ~.diagram: Custom diagram elements for the editor
  * ~.dialog: Custom dialogs for the editor
* ~.inference: Data model inference from graphical MAML artifacts using hypergraph data structure (based on [JUNG library](https://github.com/jrtom/jung))
* ~.generator: MAML app generation project
  * ~.md2converter: [QVTo](https://projects.eclipse.org/projects/modeling.mmt.qvt-oml) model-to-model transformation to the textual MD² DSL from which platform code can be generated according to the [MD² website](http://wwu-pi.github.io/md2-web/)

## MAML generation approach
This is a sample use case modeled using the graphical MAML syntax.

<img src="resources/MAML_example.png" width="1000px"><br><br>

The framework is based on [MD²](http://wwu-pi.github.io/md2-web/), a textual DSL for Business Apps.
Therefore, a MAML model is transformed to this syntax and reuses existing code generators for the generation of app sources.

<img src="resources/MAML_process.png" width="300px"><br><br>

As example output, the first two steps of the exemplary model result in the following two Android views:

<img src="resources/MAML_app_result.png" width="550px"><br><br>

## Setting up the modeling environment
The following guide describes the installation for users of the language. See next chapter for developers.
Note: The installation was tested for the Eclipse Neon release.

1. Download and unzip the [Eclipse Modeling Tools package](http://www.eclipse.org/downloads/packages/eclipse-modeling-tools/neon1a)
1. Get the four .jar files from the current `/release` directory of this repository and copy them to the `/plugins` directory of the Eclipse installation
1. Start eclipse and choose a workspace of your choice
1. Go to Help > Eclipse Marketplace and install "Sirius 4.0" (make sure to tick at least the Environment and AQL Support features)
1. Restart Eclipse
1. Make sure you are in the Sirius perspective (red icon in top right corner) or open it first
<br/><img src="resources/Guide_sirius_perspective.png" width="200px">
1. Create new project using `File` > `New` > `Modeling project`
1. Create new model by right-clicking on the project and selecting `New` > `Other...` > `MAML model`, choose a name and select `Use Case` as model object
1. Right-click on the project and select `Viewpoint Selection` > `MAML`
<br/><img src="resources/Guide_viewpoint_selection.png" width="400px">
1. A "MAML editor" should show up in the model explorer within the .maml file that opens the visual editor
<br/><img src="resources/Guide_maml_editor.png" width="400px">
1. Enjoy modeling!

## Setup for developers
TODO

## Pull requests welcome!

Spotted an error? Something doesn't make sense? Ideas for improvement? Send me a pull request!
