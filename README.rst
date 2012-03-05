Supervisord-Nagios-Plugin
-------------------------

Installation
-----------

Copy the file check_supv.py to your Nagios/Icinga plugin directory and make executable using `sudo chmod a+x`.


Configuration
-------------
Set the supervisorctl status command, default is

::

        SUPERV_STAT_CHECK='sudo supervisorctl status'

Please make sure nagios/icinga user can run the command without password.

Command
-------
Run the command with the name of the supervisord process as it appears in ``supervisorctl status``

::

        check_supv.py -p PROCESS_NAME

For example, running `./check_supv.py -p roamz_com:roamz_com_w1` should yield a response.

