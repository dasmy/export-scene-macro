## VTK.js - Paraview Export Scene Macro

Sparked by some missing features in the `*.vtkjs` export of [Paraview](https://www.paraview.org), see discussion in the [Paraview Discourse Support Channel](https://discourse.paraview.org/t/trouble-exporting-scene-to-vtkjs/9829/10), the script [`export-scene-macro.py`](export-scene-macro.py) in this repository tries to fix some of the original script.
Starting from a verbatim copy of [`export-scene-macro.py` in the vtk.js github repository](https://github.com/Kitware/vtk-js/blob/master/Utilities/ParaView/export-scene-macro.py), the following changes and fixes have been applied:

* Fix errors (Python 3 compatibility, name of imported modules)
* Do not ignore `vtkMultiBlockDataset` when exporting
* Export all numeric arrays instead only the one needed for coloring the scene items
* Do not skip `vtkStringArray` when exporting to `*.vtkjs`
* Fixed export when names of scene items contain spaces or other special characters
* Support for coloring of scene items by non-numeric arrays (tested with string arrays)
* Python-style formatting
