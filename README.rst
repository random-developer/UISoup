UISoup
======

.. image:: https://img.shields.io/pypi/v/UISoup.svg
        :alt: Release Status
        :target: https://pypi.python.org/pypi/UISoup

**This library supports UI-related testing using Python on Windows and Mac OS. (Only Python x86 is supported)**


**How to use examples:**

* Calculator:

.. code:: python

 from uisoup import uisoup


 calculator = uisoup.get_window('Calculator')

 calculator.drag_to(50, 50, x_offset=30, y_offset=5)
 b1 = calculator.find(c_name='btn2')
 b1.click()
 ba = calculator.find(c_name='btnAdd')
 ba.click()
 b2 = calculator.find(c_name='btn3')
 b2.click()
 be = calculator.find(c_name='btnEquals')
 be.click()

* Notepad:

.. code:: python

 from uisoup import uisoup


 # You can use wildcard in names such as "?" and "*".
 notepad = uisoup.get_window('*Notepad')

 notepad.set_focus()
 kc = uisoup.keyboard.codes
 uisoup.keyboard.send(kc.SHIFT.modify(kc.KEY_H), kc.KEY_E, kc.KEY_L,
                      kc.KEY_L, kc.KEY_O, kc.SPACE, kc.KEY_W, kc.KEY_O,
                      kc.KEY_R, kc.KEY_L, kc.KEY_D,
                      kc.SHIFT.modify(kc.KEY_1))


Also adds :code:`ui-inspector` script that allows you to inspect UI elements. Just type it in terminal.

**Changelog:**

UISoup 2.5.7 (released 27 Apr 2018)

* Fixes: fix issue with pip.req in new version of pip.

UISoup 2.5.5 (released 01 Jun 2017)

* Fixes: fix issue #19 that blocks __str__ method of element.

UISoup 2.5.4 (released 14 Apr 2017)

* Additions: added support for Python3.
* Additions: docstrings were updated.

UISoup 2.4.3 (released 15 Apr 2015)

* Additions: fixed mouse double click.

UISoup 2.4.2 (released 8 Apr 2015)

* Additions: updated with smooth mouse move.
* Additions: updated with delay between key press in Keyboard.send() method.

UISoup 2.4.1 (released 4 Mar 2015)

* Mac OS Additions: added new element role "AXLink".
* Mac OS Additions: fixed issue when we getting fail on execution "get attribute "AXURL" of UI element" string.

UISoup 2.4 (released 5 Feb 2015)

* Mac OS Additions: fixed issue when we can't work with windows that have double quotes in name.

UISoup 2.2 (released 16 Dec 2014)

* Mac OS Additions: added ability to see AXDialog windows.
* Mac OS Additions: fixed issue when incorrect applescript specifier was constructed.

UISoup 2.0 (released 20 Jun 2014)

* Mac OS Additions: added version for Mac OS.

UISoup 1.0 (released 28 Mar 2014)

* Windows Additions: initial version for Windows.
