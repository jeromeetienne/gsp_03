# gsp_03

- implementation of scene graph in user-space
- GSP very bare
  - no official dependancy (not even numpy)
  - no scene graph - only model_matrix, view_matrix, projection_matrix are given by user
    - user is responsible for managing scene graph if needed
    - see [examples/gsp_extra/object3d.py](examples/gsp_extra/object3d.py) as example implementation
    - user-space implementation of matrix computation via [glm.py](examples/gsp_extra/glm.py)
- gsp_matplotlib
  - implementation of a renderer using matplotlib [gsp_matplotlib](src/gsp_matplotlib/))


## Issues

### Matplotlib doesnt support removing Artists from a figure
- Artists is the basic drawing element in matplotlib
- there is a lot of issues in `matplotlib` with removing Artists from a figure
- e.g. when changing the number of group in a visual, it would require removing old Artists and adding new Artists
  - this trigger the bug in matplotlib

## Installation

Create a virtual environment and install the required packages:

```bash
python -m venv .venv
source .venv/bin/activate
pip install -e . 
```
