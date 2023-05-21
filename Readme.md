<div align="center">

# T3D GN Presets
##  A Collection of Incredibly useful nodes for Geometry Nodes - Blender 3.6 LTS (Beta)
![T3D GN Presets](https://user-images.githubusercontent.com/106262964/234839626-d88f0ce9-2399-4193-9940-2257bc728351.png)

<br>
</div>

# 💡 Introduction:

* [T3D GN Presets](https://github.com/Tams3d/T3D-GN-Presets/) contains Node groups for Geometry Nodes which include Deformers, Fields, SDF, UV, Utilities and much more for **free!**
* This is an essential component of an artist’s toolkit which enables users to combine multiple nodes with endless possibilities in non-destructive workflows with existing Blender tools.

# 🪄 Release Notes:

- **T3D-GN-Presets (v1.3.0)** to be released on 27.05.2023
- Download stable version for Blender 3.5 & below [here](https://github.com/Tams3d/T3D-GN-Presets/releases)    

# ⚙️ Core:

## Source Files
- Removed unnecessary code comments, empty lines and spaces [(0d4126a)](https://github.com/Tams3d/T3D-GN-Presets/commit/0d4126a9272584c5f80e585ce6ace9d085e8bce2)
- Optimised all icons for Deformers. **Displacer** and **Smooth Geometry** are now assets. Filled necessary informations [(42fdcbc)](https://github.com/Tams3d/T3D-GN-Presets/commit/42fdcbce5ce1547c0f42f93cfab3eb0191b9b14c)
- Removed Exif data from images, solves empty Icon issue
- Solved conflicts with other addons [(3a45e95)](https://github.com/Tams3d/T3D-GN-Presets/commit/3a45e95160c7debb92531a1a297737428bc5e6ed)

## Nodes
- Nodes are rearranged based on usability with separations. Tooltips are made mandatory for all nodes.
- Support for NURBS in all curve nodes
- Fixed implicit issues with nodes [(c7acb1c)](https://github.com/Tams3d/T3D-GN-Presets/commit/c7acb1c97e18864f473bb6a37d39b4d48f8beac3)
  - Fix rotation center in Parent To Object
  - Maintain consistency in input and output names

## 🪅 Performance:
- Nodes with Store Named Attribute are slightly faster and memory efficient [(b54398c16c)](https://projects.blender.org/blender/blender/commit/b54398c16cfee14a054e2c3ec82d091b34c79a34)
- Assets are now loaded faster, saves upto 10 mb [(42fdcbc)](https://github.com/Tams3d/T3D-GN-Presets/commit/42fdcbce5ce1547c0f42f93cfab3eb0191b9b14c)
- Fixed overhead with **UV To Mesh** and **UV Project** with high poly mesh
- Removed internal dependencies in **Sweep Curve** 
- All curve primitives are made to use Curve Circle or Arc as default. Removes Resample Curve computation
- `Deformers` work up to 35% faster and more stable.
# 🎉 New Nodes, Features & Changes:

## New Nodes:

### Input
- **Island Center** - Outputs individual Mesh Island center
- **Geometry Size** - Outputs bound geometry size, bound center and max size

### Mesh
- **Align Island** - Aligns Mesh Island by axis
- **Match Topology** - Transforms Mesh by Topology
- **Simple Decimate** - Merge Faces by distance by proximate points

## 🎆 New Features & Changes:

- **Rotate Elements** now supports Edges
- Renamed **Linear Instancer** inputs same as **Mesh Line**
  - Start >>> **Start Location**
  - End >>> **Offset**
- **Radial Instancer** is rewritten, supports instances and removal of Trim Start as replacement of **Offset** and **Trim End**
- Removed Clamp from **Mesh To Field** & **Mesh To SDF**
- Easing nodes are rearranged based on easing strength [(ff3cbc9)](https://github.com/Tams3d/T3D-GN-Presets/commit/ff3cbc97200fff4e4262fb747f2c9fe88f19a27b)
- **Vertex Slide** has been ported with new Index of Nearest [(1ab598b)](https://github.com/Tams3d/T3D-GN-Presets/commit/1ab598bb74ef5d80a6cc69caff7a3f897f844815)

### Curve
- **Lathe Curve:** Removed Curvature, uses evaluated points [(855f108)](https://github.com/Tams3d/T3D-GN-Presets/commit/855f1087a1c09dc2ac028785eb6196f1ca77b5c7)
- **Sweep Curve:** Removed Radius, uses default radius implicitly. Removed all internal dependencies and replaced them with Capture Attribute
- Resolution input is made constant to fix overlapping issues in all curve primitives
- Fixed inputs in **Logarithmic Spiral**

### Deformer
- All `Deformers` are completely rewritten to work faster, allowing direct input of instances. Instances are realised internally.
- **Bend** works dynamically and does not change the geometry's location. **Expansion** is converted to float and works along with **Angle**
- **Displacer** supports point clouds and inputs normal. Normal attribute is used by default.
- **Smooth Geometry** works more efficiently
  - Does not restore initial size and position to avoid jitter [(c7acb1c)](https://github.com/Tams3d/T3D-GN-Presets/commit/c7acb1c97e18864f473bb6a37d39b4d48f8beac3) 
  - Shade Smooth is enabled by default [(cbda951)](https://github.com/Tams3d/T3D-GN-Presets/commit/cbda9510f702be35f9425adeb8effa5b37f3096d)
  - Selection input works as expected, dynamically works with stiffness
- Fixed **Shear** inverted **Angle**
- Changes in internal dependencies **(Named attributes)**

### Fields
- Exposed Clamp in Fields
- Spherical Field uses Gradient Texture

### Point Primitives
- **Point Honeycomb** inputs Point Radius
- **Point Phyllotaxis** has been changed to curve to points method. Now inputs Point Radius and outputs Normal and Rotation

### UV
- **UV To Mesh** used `UVMap` as default
- **UV Project** has been rewritten, inputs selection, uses Euler Angles to project - defaulted to (0,180°,0) as Z positive (Top project) and fit mesh islands inside a 1-meter boundary

### Vector
- **Vector Clamp** uses Min Max as Clamp Type [(2dc59bc)](https://github.com/Tams3d/T3D-GN-Presets/commit/2dc59bc45c39f187f5b4ce382b3d8edc91ed2bb1)
- Renamed **Transforms To Position** >>> **Transform Position**
- **Transform Position** is moved to Vector (category) [(c7acb1c)](https://github.com/Tams3d/T3D-GN-Presets/commit/c7acb1c97e18864f473bb6a37d39b4d48f8beac3)


## Breaking Changes:
- Removed **Spiroshell** due to its instability
- Removed **Select Index Range** 
- Breaks backward compatibility in **Vertex Slide**. **Index of Nearest** does not support offsetting, _Nearest Index_ is removed.
- Removal of _Generate UV_ in **UV To Mesh** 

# 🎯 Development
- Developments are happening locally regularly regarding bug fixes, and support for every upcoming [Blender](https://www.blender.org/) release.
- Documentation is currently in **_work-in-progress_**
- Supports **Blender 4.0** without any issues. 

## 👻 Bug Reports
- Bug reports are always welcomed in the form of reports or suggestions.
- Suggestions can be included with brief explanations of usability.
- Submit Bug reports and feature requests [here](https://github.com/Tams3d/T3D-GN-Presets/issues)

# Licencing & Files:
## 📄 Licence
- The Node groups, including the Addon, are licensed as [GNU GPL](https://github.com/Tams3d/T3D-GN-Presets/blob/Master/LICENSE)
  * You are free for any purpose
  * You are free to distribute unless the license is modified
  * You can distribute changed versions
  * What you create with this Addon is your sole property
  * You are not allowed to change the license or introduce additional terms and conditions

## 📂 Access to Files:
- [ `_init_.py` ](https://github.com/Tams3d/T3D-GN-Presets/blob/Master/__init__.py) defines the addon followed by [geonode_groups.json](https://github.com/Tams3d/T3D-GN-Presets/blob/Master/geonode_groups.json) which contains a list of categories with nodes.
- [geonode_nodes.blend](https://github.com/Tams3d/T3D-GN-Presets/blob/Master/geonode_nodes.blend) contains all the Node-groups which are displayed under `T3D GN Presets`
- **All Files & Assets** follow the same [Licence](https://github.com/Tams3d/T3D-GN-Presets/blob/Master/README.md#licencing--files)

# 🦄 About 
  - Hey! I am **Tamil Selvan**, also known as **tams_3d**. I am a 16-Year-Old Self Taught Blender Artist from **India**
  - My Vision is to create *Free* for the Blender, which requires complex setups provided in a simplified and effective way.
  - Currently developing Presets for Geometry Nodes which are similar to tools and features of other 3D Packages and some add-ons.
  - I believe that my work contributes to a better world for 3D Artists, Game Developers and other artists who create incredible works.
  
  # 🥂 Socials
  - Catch up with me here:
    * [Behance](https://www.behance.net/tamilselvan3d)
    * [Discord](https://discord.gg/TNgzbZCdnY)
    * [GitHub](https://github.com/Tams3d)
    * [Twitter](https://twitter.com/Tams_3d)
