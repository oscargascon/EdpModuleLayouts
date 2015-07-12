EdpModuleLayouts
================
Created by Evan Coury. Version 1.1 improved by Oscar Gascón.

Introduction
------------

EdpModuleLayouts is a very simple ZF2 module (less than 20 lines) that simply
allows you to specify alternative layouts to use for each module.

Version 1.1
-----------

Now this module permits setup by config the different layouts for Module, Controllers an Action directly in the module.config.php file using an array config.

Usage
-----

Using EdpModuleLayouts is very, very simple. In any module config or autoloaded
config file simply specify the following:

```php
array(
    'module_layouts' => array(
        'ModuleName' => 'layout/some-layout',
    ),
    'controller_layouts' => array(
        'ModuleName/ControllerName' => 'layout/some-layout',
    ),
    'action_layouts' => array(
        'ModuleName/ControllerName/ActionName' => 'layout/some-layout',
    ),
);
```

Example
-------

```php
    'module_layouts' => array(
        'Admin' => 'admin/layout',
    ),
    'controller_layouts' => array(
        'Admin/Login' => 'login/layout',
    ),
    'àction_layouts' => array(
        'Admin/Login/logout' => 'logout/layout',
    ),
```

That's it!
