## alternative unofficial napalm ios driver

Due the purpose of NAPALM the included IOS Drivers are designed to require Privilege Exec Mode(aka Privilege Level 15)<br>
to ensure the full feature-set is always available.<br>
If this privilege level is not available the driver will not work.<br>
This limits it's use for certain purposes where priv exec is not required. (like using the getters() or sending show commands)

This driver is a fork of the original driver, it changes the behavior of the driver and implements privilege level checking.
It will allow to connect without privilege level 15 and instead raise permission-errors<br>
if a function is called and the necessary privileges are not available. <br>
It will neither change function arguments or return values nor implement new functions.

## Authors:

While the privilege patches are maintained by me the rest(the largest part) of the codebase  is sync'd from and belongs to the [NAPALM Project](https://github.com/napalm-automation/napalm/).

Privilege Patches
  * Daniel Schlifka <remingu@techturn.de>

Original Authors(NAPALM Project)
 * David Barroso ([dbarrosop@dravetech.com](mailto:dbarrosop@dravetech.com))
 * Elisa Jasinska ([elisa@bigwaveit.org](mailto:elisa@bigwaveit.org))
 * Many others, check the [napalm contributors](https://github.com/napalm-automation/napalm/graphs/contributors) page for details.

