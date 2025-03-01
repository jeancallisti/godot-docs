:github_url: hide

.. Generated automatically by doc/tools/make_rst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the PhysicalBone2D.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_PhysicalBone2D:

PhysicalBone2D
==============

**Inherits:** :ref:`RigidDynamicBody2D<class_RigidDynamicBody2D>` **<** :ref:`PhysicsBody2D<class_PhysicsBody2D>` **<** :ref:`CollisionObject2D<class_CollisionObject2D>` **<** :ref:`Node2D<class_Node2D>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

A 2D node that can be used for physically aware bones in 2D.

Description
-----------

The ``PhysicalBone2D`` node is a :ref:`RigidDynamicBody2D<class_RigidDynamicBody2D>`-based node that can be used to make :ref:`Bone2D<class_Bone2D>` nodes in a :ref:`Skeleton2D<class_Skeleton2D>` react to physics. This node is very similar to the :ref:`PhysicalBone3D<class_PhysicalBone3D>` node, just for 2D instead of 3D.

\ **Note:** To have the Bone2D nodes visually follow the ``PhysicalBone2D`` node, use a :ref:`SkeletonModification2DPhysicalBones<class_SkeletonModification2DPhysicalBones>` modification on the :ref:`Skeleton2D<class_Skeleton2D>` node with the :ref:`Bone2D<class_Bone2D>` nodes.

\ **Note:** The PhysicalBone2D node does not automatically create a :ref:`Joint2D<class_Joint2D>` node to keep ``PhysicalBone2D`` nodes together. You will need to create these manually. For most cases, you want to use a :ref:`PinJoint2D<class_PinJoint2D>` node. The ``PhysicalBone2D`` node can automatically configure the :ref:`Joint2D<class_Joint2D>` node once it's been created as a child node.

Properties
----------

+---------------------------------+-----------------------------------------------------------------------------------------------+------------------+
| :ref:`bool<class_bool>`         | :ref:`auto_configure_joint<class_PhysicalBone2D_property_auto_configure_joint>`               | ``true``         |
+---------------------------------+-----------------------------------------------------------------------------------------------+------------------+
| :ref:`int<class_int>`           | :ref:`bone2d_index<class_PhysicalBone2D_property_bone2d_index>`                               | ``-1``           |
+---------------------------------+-----------------------------------------------------------------------------------------------+------------------+
| :ref:`NodePath<class_NodePath>` | :ref:`bone2d_nodepath<class_PhysicalBone2D_property_bone2d_nodepath>`                         | ``NodePath("")`` |
+---------------------------------+-----------------------------------------------------------------------------------------------+------------------+
| :ref:`bool<class_bool>`         | :ref:`follow_bone_when_simulating<class_PhysicalBone2D_property_follow_bone_when_simulating>` | ``false``        |
+---------------------------------+-----------------------------------------------------------------------------------------------+------------------+
| :ref:`bool<class_bool>`         | :ref:`simulate_physics<class_PhysicalBone2D_property_simulate_physics>`                       | ``false``        |
+---------------------------------+-----------------------------------------------------------------------------------------------+------------------+

Methods
-------

+-------------------------------+-----------------------------------------------------------------------------------------------------+
| :ref:`Joint2D<class_Joint2D>` | :ref:`get_joint<class_PhysicalBone2D_method_get_joint>` **(** **)** |const|                         |
+-------------------------------+-----------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`       | :ref:`is_simulating_physics<class_PhysicalBone2D_method_is_simulating_physics>` **(** **)** |const| |
+-------------------------------+-----------------------------------------------------------------------------------------------------+

Property Descriptions
---------------------

.. _class_PhysicalBone2D_property_auto_configure_joint:

- :ref:`bool<class_bool>` **auto_configure_joint**

+-----------+---------------------------------+
| *Default* | ``true``                        |
+-----------+---------------------------------+
| *Setter*  | set_auto_configure_joint(value) |
+-----------+---------------------------------+
| *Getter*  | get_auto_configure_joint()      |
+-----------+---------------------------------+

If ``true``, the ``PhysicalBone2D`` node will automatically configure the first :ref:`Joint2D<class_Joint2D>` child node. The automatic configuration is limited to setting up the node properties and positioning the :ref:`Joint2D<class_Joint2D>`.

----

.. _class_PhysicalBone2D_property_bone2d_index:

- :ref:`int<class_int>` **bone2d_index**

+-----------+-------------------------+
| *Default* | ``-1``                  |
+-----------+-------------------------+
| *Setter*  | set_bone2d_index(value) |
+-----------+-------------------------+
| *Getter*  | get_bone2d_index()      |
+-----------+-------------------------+

The index of the :ref:`Bone2D<class_Bone2D>` node that this ``PhysicalBone2D`` node is supposed to be simulating.

----

.. _class_PhysicalBone2D_property_bone2d_nodepath:

- :ref:`NodePath<class_NodePath>` **bone2d_nodepath**

+-----------+----------------------------+
| *Default* | ``NodePath("")``           |
+-----------+----------------------------+
| *Setter*  | set_bone2d_nodepath(value) |
+-----------+----------------------------+
| *Getter*  | get_bone2d_nodepath()      |
+-----------+----------------------------+

The :ref:`NodePath<class_NodePath>` to the :ref:`Bone2D<class_Bone2D>` node that this ``PhysicalBone2D`` node is supposed to be simulating.

----

.. _class_PhysicalBone2D_property_follow_bone_when_simulating:

- :ref:`bool<class_bool>` **follow_bone_when_simulating**

+-----------+----------------------------------------+
| *Default* | ``false``                              |
+-----------+----------------------------------------+
| *Setter*  | set_follow_bone_when_simulating(value) |
+-----------+----------------------------------------+
| *Getter*  | get_follow_bone_when_simulating()      |
+-----------+----------------------------------------+

If ``true``, the ``PhysicalBone2D`` will keep the transform of the bone it is bound to when simulating physics.

----

.. _class_PhysicalBone2D_property_simulate_physics:

- :ref:`bool<class_bool>` **simulate_physics**

+-----------+-----------------------------+
| *Default* | ``false``                   |
+-----------+-----------------------------+
| *Setter*  | set_simulate_physics(value) |
+-----------+-----------------------------+
| *Getter*  | get_simulate_physics()      |
+-----------+-----------------------------+

If ``true``, the ``PhysicalBone2D`` will start simulating using physics. If ``false``, the ``PhysicalBone2D`` will follow the transform of the :ref:`Bone2D<class_Bone2D>` node.

\ **Note:** To have the Bone2D nodes visually follow the ``PhysicalBone2D`` node, use a :ref:`SkeletonModification2DPhysicalBones<class_SkeletonModification2DPhysicalBones>` modification on the :ref:`Skeleton2D<class_Skeleton2D>` node with the :ref:`Bone2D<class_Bone2D>` nodes.

Method Descriptions
-------------------

.. _class_PhysicalBone2D_method_get_joint:

- :ref:`Joint2D<class_Joint2D>` **get_joint** **(** **)** |const|

Returns the first :ref:`Joint2D<class_Joint2D>` child node, if one exists. This is mainly a helper function to make it easier to get the :ref:`Joint2D<class_Joint2D>` that the ``PhysicalBone2D`` is autoconfiguring.

----

.. _class_PhysicalBone2D_method_is_simulating_physics:

- :ref:`bool<class_bool>` **is_simulating_physics** **(** **)** |const|

Returns a boolean that indicates whether the ``PhysicalBone2D`` node is running and simulating using the Godot 2D physics engine. When ``true``, the PhysicalBone2D node is using physics.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
