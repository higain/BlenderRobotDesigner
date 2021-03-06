Application Program Interface (API)
===================================

Software structure
------------------

::

    RobotDesigner/
    ├── doc                                 Documentation
    │   ├── Makefile                        Create documentation (e.g., make html)
    │   ├── build                           Location of the generated documentation
    │   ├── make.bat                        Windows command for generation
    │   └── source                          Source files for the documentation
    │ 
    ├── resources                           Additional Resources
    │   ├── generateDOM.sh                  Bash script for generating the DOM from XSD
    │   ├── mock_bpy                        A mock module for the Blender classes
    │   │   │                               (required for building the documentation)
    │   │   ├── bpy
    │   │   │   ├── __init__.py
    │   │   │   ├── ops.py
    │   │   │   ├── props.py
    │   │   │   ├── types.py
    │   │   ├── mathutils.py
    │   ├── test.urdf                       A test URDF file
    │   ├── urdf.xsd                        The XML scheme definition of URDF
    │   └── urdf_xml_validator.py           A script for validating a URDF file
    │ 
    └── robot_designer_plugin               The base directory of the Plugin
        ├── LICENSE                         License file
        ├── README.md
        ├── __init__.py
        ├── armatures.py                    Classes/operators for robot models
        ├── bones.py                        Classes/operators for joints/links
        ├── collada.py                      Collada support for version 1.5
        ├── controllers.py                  Classes/operators for joints/links
        ├── export                          Exporters
        │   ├── __init__.py
        │   └── urdf                        URDF Import/Export
        │       ├── __init__.py
        │       ├── helpers.py              Helper functions
        │       ├── urdf_blender.py         Blender related import/export code
        │       ├── urdf_dom.py             Autogenerated Document object model
        │       └── urdf_tree.py            Generic (non blender dependent) class
        │                                   for parsing/writing a URDF file
        │  
        ├── files.py                        Classes/operators for file dialogs
        ├── fix.py
        ├── main.py                         Main entry of the plugin
        ├── markers.py                      Classes/operators for sensors
        ├── meshes.py                       Classes/operators for geometric models
        ├── physics.py                      Classes/operators for physical attributes
        ├── properties.py                   Annotations for Blender data types
        └── simox.py                        Import of files for the Simox simulator

Reference
---------
.. toctree::
   :maxdepth: 4

   robot_designer_plugin
