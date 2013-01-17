acers3fand
==========

acers3fand is a script which controls your Acer Aspire S3 Ultrabook fan speed by cpu temperature.
It is designed to work with Intel Core i5 CPU but might work with other cpus as well.

IT IS POSSIBLE THAT YOUR LAPTOP WARRANTY WILL BE VOID AFTER USING THIS SCRIPT!
BE ALWAYS OBSERVANT AND ACT IF YOUR LAPTOP BEGINS TO BE TOO HOT OR THE FAN IS NOT SPINNING!

"sudo killall acers3fand" will restore your fan to state AUTO
but will not remove the auto-start script so it is running again after bootup

----------------------------------------

acers3fand is a script which controls your Acer Aspire S3 Ultrabook
fan speed by cpu temperature. It is designed to work with Intel Core i5 CPU
but might work with other cpus as well.

For Ubuntu (Gnome) users we would also recommend using Jupiter indicator
application (in addition with acers3fand) to manage cpu frequency
and power stages to get lower temperatures and allow acers3fand to
make your laptop even more quiet!

Kernel versions 3.x and above (Ubuntu 11.10 and newer) are also recommended.

#### Pre-requirements ####

- perl
- acer_ec.pl (http://code.google.com/p/aceracpi/)
- acers3fand
- acers3fand_init

#### Installation:####

- Copy `acer_ec.pl` and `acers3fand` to `/usr/local/bin/`
- Make sure both are executable (chmod +x) and owned by the root user
- Copy `acers3fand_init` to `/etc/init.d/`
- Make sure it is executable (chmod +x) and owned by the root user
- Run: `sudo ln -s /etc/init.d/acers3fand_init /etc/rc2.d/S99acers3fand`
- Reboot and check `/var/log/syslog` for lines "acers3fand"

#### Usage ####

- This is maintainance-free appplication, should work out of the box
- See acers3fand -file for changelog and limitations (bios versions etc.)
