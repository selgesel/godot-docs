:github_url: hide

.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the bool.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_bool:

bool
====

Boolean built-in type.

Description
-----------

Boolean is a built-in type. There are two boolean values: ``true`` and ``false``. You can think of it as a switch with on or off (1 or 0) setting. Booleans are used in programming for logic in condition statements, like ``if`` statements.

Booleans can be directly used in ``if`` statements. The code below demonstrates this on the ``if can_shoot:`` line. You don't need to use ``== true``, you only need ``if can_shoot:``. Similarly, use ``if not can_shoot:`` rather than ``== false``.


.. tabs::

 .. code-tab:: gdscript

    var _can_shoot = true
    
    func shoot():
        if _can_shoot:
            pass # Perform shooting actions here.

 .. code-tab:: csharp

    private bool _canShoot = true;
    
    public void Shoot()
    {
        if (_canShoot)
        {
            // Perform shooting actions here.
        }
    }



The following code will only create a bullet if both conditions are met: action "shoot" is pressed and if ``can_shoot`` is ``true``.

**Note:** ``Input.is_action_pressed("shoot")`` is also a boolean that is ``true`` when "shoot" is pressed and ``false`` when "shoot" isn't pressed.


.. tabs::

 .. code-tab:: gdscript

    var _can_shoot = true
    
    func shoot():
        if _can_shoot and Input.is_action_pressed("shoot"):
            create_bullet()

 .. code-tab:: csharp

    private bool _canShoot = true;
    
    public void Shoot()
    {
        if (_canShoot && Input.IsActionPressed("shoot"))
        {
            CreateBullet();
        }
    }



The following code will set ``can_shoot`` to ``false`` and start a timer. This will prevent player from shooting until the timer runs out. Next ``can_shoot`` will be set to ``true`` again allowing player to shoot once again.


.. tabs::

 .. code-tab:: gdscript

    var _can_shoot = true
    onready var _cool_down = $CoolDownTimer
    
    func shoot():
        if _can_shoot and Input.is_action_pressed("shoot"):
            create_bullet()
            _can_shoot = false
            _cool_down.start()
    
    func _on_CoolDownTimer_timeout():
        _can_shoot = true

 .. code-tab:: csharp

    private bool _canShoot = true;
    private Timer _coolDown;
    
    public override void _Ready()
    {
        _coolDown = GetNode<Timer>("CoolDownTimer");
    }
    
    public void Shoot()
    {
        if (_canShoot && Input.IsActionPressed("shoot"))
        {
            CreateBullet();
            _canShoot = false;
            _coolDown.Start();
        }
    }
    
    public void OnCoolDownTimerTimeout()
    {
        _canShoot = true;
    }



Methods
-------

+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | :ref:`bool<class_bool_method_bool>` **(** **)** |constructor|                                |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | :ref:`bool<class_bool_method_bool>` **(** :ref:`bool<class_bool>` from **)** |constructor|   |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | :ref:`bool<class_bool_method_bool>` **(** :ref:`float<class_float>` from **)** |constructor| |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | :ref:`bool<class_bool_method_bool>` **(** :ref:`int<class_int>` from **)** |constructor|     |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | **operator !=** **(** **)** |operator|                                                       |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | **operator !=** **(** :ref:`bool<class_bool>` right **)** |operator|                         |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | **operator <** **(** :ref:`bool<class_bool>` right **)** |operator|                          |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | **operator ==** **(** **)** |operator|                                                       |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | **operator ==** **(** :ref:`bool<class_bool>` right **)** |operator|                         |
+-------------------------+----------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>` | **operator >** **(** :ref:`bool<class_bool>` right **)** |operator|                          |
+-------------------------+----------------------------------------------------------------------------------------------+

Method Descriptions
-------------------

.. _class_bool_method_bool:

- :ref:`bool<class_bool>` **bool** **(** **)** |constructor|

Constructs a default-initialized ``bool`` set to ``false``.

----

- :ref:`bool<class_bool>` **bool** **(** :ref:`bool<class_bool>` from **)** |constructor|

Constructs a ``bool`` as a copy of the given ``bool``.

----

- :ref:`bool<class_bool>` **bool** **(** :ref:`float<class_float>` from **)** |constructor|

Cast a :ref:`float<class_float>` value to a boolean value, this method will return ``false`` if ``0.0`` is passed in, and ``true`` for all other floats.

----

- :ref:`bool<class_bool>` **bool** **(** :ref:`int<class_int>` from **)** |constructor|

Cast an :ref:`int<class_int>` value to a boolean value, this method will return ``false`` if ``0`` is passed in, and ``true`` for all other ints.

----

.. _class_bool_method_operator !=:

- :ref:`bool<class_bool>` **operator !=** **(** **)** |operator|

----

- :ref:`bool<class_bool>` **operator !=** **(** :ref:`bool<class_bool>` right **)** |operator|

Returns ``true`` if two bools are different, i.e. one is ``true`` and the other is ``false``.

----

.. _class_bool_method_operator <:

- :ref:`bool<class_bool>` **operator <** **(** :ref:`bool<class_bool>` right **)** |operator|

Returns ``true`` if left operand is ``false`` and right operand is ``true``.

----

.. _class_bool_method_operator ==:

- :ref:`bool<class_bool>` **operator ==** **(** **)** |operator|

----

- :ref:`bool<class_bool>` **operator ==** **(** :ref:`bool<class_bool>` right **)** |operator|

Returns ``true`` if two bools are equal, i.e. both are ``true`` or both are ``false``.

----

.. _class_bool_method_operator >:

- :ref:`bool<class_bool>` **operator >** **(** :ref:`bool<class_bool>` right **)** |operator|

Returns ``true`` if left operand is ``true`` and right operand is ``false``.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
