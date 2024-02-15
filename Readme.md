<div align="center">

# T3D GN Presets
##  A Collection of Incredibly Useful Nodes for Geometry Nodes - Blender 4.1 (Beta)

![T3D GN Presets (v1.4.0)](https://github.com/Tams3d/T3D-GN-Presets/assets/106262964/c3efe10c-5478-4ad7-954a-8a838cf1a0b1)

<br>
</div>

# 💡 Introduction:

* [T3D GN Presets](https://github.com/Tams3d/T3D-GN-Presets/#t3d-gn-presets) contains Node groups for Geometry Nodes, which include Deformers, Fields, UV, Utilities, and much more for **free!**
* This is an essential component of an artist’s toolkit, enabling users to combine multiple nodes with endless possibilities in non-destructive workflows with existing Blender tools.

# 🪄 Release Notes:

- **T3D-GN-Presets (v1.4.0)** to be released on 11.03.2024
- For Blender 4.0 & below, check out the latest releases [here](https://github.com/Tams3d/T3D-GN-Presets/releases)

# ⚙️ Core:
## Source Files

- Follow **Black** code style [(6ca7f8b)](https://github.com/Tams3d/T3D-GN-Presets/commit/6ca7f8b)
- Renamed **geonode_groups.json** >>> [**t3d_nodegroups.json**](https://github.com/Tams3d/T3D-GN-Presets/blob/main/t3d_nodegroups.json)
- Renamed **geonode_nodes.blend** >>> [**t3d_nodes.blend**](https://github.com/Tams3d/T3D-GN-Presets/blob/main/t3d_nodes.blend)

## Repository
- Renamed branch name from **Master** to [`main`](https://github.com/Tams3d/T3D-GN-Presets/tree/main) to avoid grammar conflicts.
- Include [workflows](https://github.com/Tams3d/T3D-GN-Presets/actions) for linting.

# 🎉 New Nodes, Features & Changes:

## 🎆 New Features & Changes:
- Icon in the add menu has been changed to 🔹, which is similar to other Geometry Node-based addons. ([c6e1442](https://github.com/Tams3d/T3D-GN-Presets/commit/c6e1442))
- **Rotation** inputs are changed to Rotation Sockets.
- Position and Normal inputs are set as default.
- **Geometry To Spline** inputs selection. Supports Mesh, Curve, and instances. Adapted new Points to Curve node. ([0a2f609](https://github.com/Tams3d/T3D-GN-Presets/commit/0a2f609))
- **Instancers** get option panel for inputs. ([3df94bc](https://github.com/Tams3d/T3D-GN-Presets/commit/3df94bc))
- Dropdown menu implemented for **Delete Island**.
- Seamless Vector does not require inputs for Translation anymore.

### Deformer
- `Deformers` no longer support direct input of instances. The "Realize Instance" node must now be used prior to applying deformers. ([510b7d1](https://github.com/Tams3d/T3D-GN-Presets/commit/510b7d1)). Deformers as Assets no longer exist. ([074b970](https://github.com/Tams3d/T3D-GN-Presets/commit/074b970))

# 🚨 Depreciated Features:
- Removed **Shade Auto Smooth** as a replacement for the built-in [node](https://projects.blender.org/blender/blender/pulls/108014).
- Removed `SDF` nodes ([95ae7c2](https://github.com/Tams3d/T3D-GN-Presets/commit/95ae7c2)).
- Removed **Simple Decimate** ([95ae7c2](https://github.com/Tams3d/T3D-GN-Presets/commit/95ae7c2)).
- Replaced **Transform Position** with **Vector Mapping**, expected the same behavior ([07b67e8](https://github.com/Tams3d/T3D-GN-Presets/commit/07b67e8)).

## 🪛 Compatibility
- Make sure to have a supported **Blender** version and the corresponding addon version.
- Nodes with a **Rotation** socket are not compatible with Blender versions 4.0 and below.
- `Deformer` assets will work as expected.
- [Depreciate nodes](https://github.com/Tams3d/T3D-GN-Presets?tab=readme-ov-file#-depreciationed-features) may still function as expected. Nodes modified by the user will remain modified. [Changes](https://github.com/Tams3d/T3D-GN-Presets#-new-features--changes) in newer addon versions are not useful for files migrated from Blender 4.0 and below, as nodes are only appended, not [linked](https://github.com/Tams3d/T3D-GN-Presets/blob/main/__init__.py#L170).
- The nodes that come with the addon are regular node groups; they do not include any additional code or provide new functionality to existing ones.
- In case of any **missing data blocks**, raise an issue [here](https://github.com/Tams3d/T3D-GN-Presets/issues).

# 🎯 Development
- Developments are happening regularly regarding bug fixes, and support for every upcoming [Blender Release](https://www.blender.org/download/releases/)
- **Contributions are always welcomed!**

## 👻 Bug Reports
- Bug reports are always welcomed in the form of reports or suggestions.
- Suggestions can be included with brief explanations of usability.
- Submit Bug reports and feature requests [here](https://github.com/Tams3d/T3D-GN-Presets/issues)

# 📂 Access to Files:
- [ `_init_.py` ](https://github.com/Tams3d/T3D-GN-Presets/blob/main/__init__.py) defines the addon followed by [t3d_nodegroups.json](https://github.com/Tams3d/T3D-GN-Presets/blob/main/t3d_nodegroups.json), which contains a list of categories with nodes.
- [t3d_nodes.blend](https://github.com/Tams3d/T3D-GN-Presets/blob/main/t3d_nodes.blend) contains all the Node-groups which are displayed under `T3D GN Presets`

# 🦄 About 
  - Hey! I am **Tamil Selvan**, also known as **tams_3d**. I am a 16-Year-Old Self Taught Blender Artist from **India**
  - My Vision is to create *Free* for the Blender, which requires complex setups provided in a simplified and effective way.
  - Currently developing Presets for Geometry Nodes which are similar to tools and features of other 3D Packages and some add-ons.
  - I believe that my work contributes to a better world for 3D Artists, Game Developers and other artists who create incredible works.
  
  # 🥂 Socials
  - Catch up with me here:
    * [Behance](https://www.behance.net/tamilselvan3d)
    * [GitHub](https://github.com/Tams3d)
    * [X (Twitter)](https://twitter.com/Tams_3d)
