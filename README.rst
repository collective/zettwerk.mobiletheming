======================
zettwerk.mobiletheming
======================

Switching mobile themes based on urls using the `MobileESP`_ library.


Features
========

The ``zettwerk.mobiletheming`` package includes:

- A Mobile theming control panel
- The GenericSetup import/export profiles
- Also provides some mobile themes packages
- Provides the ``me.redirect.min.js`` resource based on *MobileESP* library.


Themes
======

This add-on provides the following mobile themes packages:

- https://github.com/espenmn/medialog.mobilethemeOne
- https://github.com/espenmn/medialog.mobilethemeTwo
- https://github.com/espenmn/medialog.mobilethemeThree


Documentation
=============

- Full **documentation for developers** can be found in the "docs" folder.
- A video example about **documentation for end users** at https://www.youtube.com/watch?v=Q2ID86XkiQQ


Translations
============

This product has been translated into

- Spanish (thanks, Leonardo J. Caballero G. aka macagua)


Installation
============


Buildout
--------

If you are a developer, you might enjoy installing it via buildout.

For install ``zettwerk.mobiletheming`` package add it to your ``buildout`` section's 
*eggs* parameter e.g.: ::

   [buildout]
    ...
    eggs =
        ...
        zettwerk.mobiletheming


and then running ``bin/buildout``.

Or, you can add it as a dependency on your own product ``setup.py`` file: ::

    install_requires=[
        ...
        'zettwerk.mobiletheming',
    ],


Enabling
--------

Select and enable the ``zettwerk.mobiletheming`` package from the ``Add-ons`` 
control panel. That's it!


Usage
=====

Install ``zettwerk.mobiletheming`` via ``portal_quickinstaller`` tool.

A new control panel entry makes it possible to change settings as the following:

.. image:: https://github.com/collective/zettwerk.mobiletheming/raw/master/docs/screenshot1.png
  :alt: Mobile theming control panel
  :align: center

Enter the hostnames on which the mobile theme should be applied.
Choose the diazo theme to use for selected URL.

There is also some settings for "redirecting urls", it works like this:

1) A javascript is installed in ``portal_javascript``
2) This javascript redirects urls to the url set in the control panel.
3) Redirects works for mobile devices.
4) You can choose if you want to redirect **iPads** and **tablets**, too.
5) There is a setting

See this example with the ``zettwerk.mobile`` theme: https://www.youtube.com/watch?v=Q2ID86XkiQQ


Generic Setup
=============

This product also provides a GenericSetup extension for integrators to set 
these settings via a xml profile file. Place the ``mobiletheming.xml`` file 
in your (default) generic setup profile and change it as you need. You can 
also export your current settings via ``portal_setup -> Export``. The export 
step is called ``Mobiletheming Settings``.

Example content, taken from `zettwerk.mobile <https://github.com/collective/zettwerk.mobile/tree/master/zettwerk/mobile/profiles/default/mobiletheming.xml>`_:

::

    <?xml version="1.0"?>
    <settings>
      <themename>zettwerk.mobile</themename>
      <hostnames>
        <element>http://localhost:8080</element>
      </hostnames>
      <ipad>False</ipad>
      <tablets>False</tablets>
    </settings>


Contribute
==========

- Issue Tracker: https://github.com/collective/zettwerk.mobiletheming/issues
- Source Code: https://github.com/collective/zettwerk.mobiletheming


License
=======

- The project is licensed under the GPLv2.
- The *MobileESP* library is licensed under the Apache License, Version 2.0.


Credits
-------

Really thanks to :

- Jörg Kubaile at zettwerk GmbH. (jk at zettwerk dot com).


Amazing contributions
---------------------

- Leonardo J. Caballero G. aka macagua (leonardocaballero at gmail dot com).

You can find an updated list of package contributors on https://github.com/collective/zettwerk.mobiletheming/contributors

.. _`MobileESP`: https://github.com/ahand/mobileesp
