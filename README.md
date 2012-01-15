fancontroller
=============

Features
--------

- makes sure fancontrol starts (babysitter mode)
- controls fans on its own (rouge mode)
- controls until:
    - temp and speed is normal
    - fancontrol is running
    - indefinitely
- min and max PWM setting
- min and max TEMP setting
- switching between AC and battery config with a single command

Fancontroller is useful for those who are experiencing problems with
fancontrol starting at boot and/or for those who are annoyed by full-speed
fans when fancontrol stops or fails to run (e.g. at boot and shutdown).


Usage
-----

    fancontroller [babysitter | rouge [ | until-fancontrol | indefinite] | ac-speed | batt-speed]


Tips
----

1. Add 'fancontroller babysitter' to /etc/rc.local
2. Add 'fancontroller rouge until-fancontrol' to 'stop' function in
   /etc/rc.d/fancontrol (see file fancontrol.daemon-script)
3. Create fancontrol.ac and fancontrol.batt config in /etc to be able
   to switch between the two configs with 'fancontroll ac-speed' and
   'fancontrol batt-speed'
