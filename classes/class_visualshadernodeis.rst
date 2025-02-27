:github_url: hide

.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the VisualShaderNodeIs.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_VisualShaderNodeIs:

VisualShaderNodeIs
==================

**Inherits:** :ref:`VisualShaderNode<class_VisualShaderNode>` **<** :ref:`Resource<class_Resource>` **<** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

A boolean comparison operator to be used within the visual shader graph.

Description
-----------

Returns the boolean result of the comparison between ``INF`` or ``NaN`` and a scalar parameter.

Properties
----------

+---------------------------------------------------+-------------------------------------------------------------+-------+
| :ref:`Function<enum_VisualShaderNodeIs_Function>` | :ref:`function<class_VisualShaderNodeIs_property_function>` | ``0`` |
+---------------------------------------------------+-------------------------------------------------------------+-------+

Enumerations
------------

.. _enum_VisualShaderNodeIs_Function:

.. _class_VisualShaderNodeIs_constant_FUNC_IS_INF:

.. _class_VisualShaderNodeIs_constant_FUNC_IS_NAN:

.. _class_VisualShaderNodeIs_constant_FUNC_MAX:

enum **Function**:

- **FUNC_IS_INF** = **0** --- Comparison with ``INF`` (Infinity).

- **FUNC_IS_NAN** = **1** --- Comparison with ``NaN`` (Not a Number; denotes invalid numeric results, e.g. division by zero).

- **FUNC_MAX** = **2** --- Represents the size of the :ref:`Function<enum_VisualShaderNodeIs_Function>` enum.

Property Descriptions
---------------------

.. _class_VisualShaderNodeIs_property_function:

- :ref:`Function<enum_VisualShaderNodeIs_Function>` **function**

+-----------+---------------------+
| *Default* | ``0``               |
+-----------+---------------------+
| *Setter*  | set_function(value) |
+-----------+---------------------+
| *Getter*  | get_function()      |
+-----------+---------------------+

The comparison function. See :ref:`Function<enum_VisualShaderNodeIs_Function>` for options.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
