# nut-zyxel-nas
Install and Configure The Network UPS Tools (NUT)  on Zyxel NAS-540 via SSH 

(UPS : EATON 3S 700 with USB port)
 


## Usage
```


login as: admin
admin@192.168.*.*'s password:
Could not chdir to home directory /home/shares: No such file or directory


BusyBox v1.19.4 (2022-08-11 16:13:10 CST) built-in shell (ash)
Enter 'help' for a list of built-in commands.

/ $ sudo
-sh: sudo: not found
/ $ su
Password:


BusyBox v1.19.4 (2022-08-11 16:13:10 CST) built-in shell (ash)
Enter 'help' for a list of built-in commands.

~ # upsdrvctl start
Network UPS Tools - UPS driver controller merge-with-ng-1491-g4a3ee6da
Network UPS Tools - Generic HID driver 0.41 (merge-with-ng-1491-g4a3ee6da)
USB communication driver 0.33
Using subdriver: MGE HID 1.39
using 'battery.charge' to set battery low state
~ # upsc
Error: invalid UPS definition.
Required format: upsname[@hostname[:port]]
~ # upsc eaton3s
Error: Connection failure: Connection refused
~ # upsd
Network UPS Tools upsd merge-with-ng-1491-g4a3ee6da
fopen /opt/var/run/upsd.pid: No such file or directory
listening on 127.0.0.1 port 3493
listening on ::1 port 3493
/opt/var/run is world readable
Connected to UPS [eaton3s]: usbhid-ups-eaton3s
~ # Communications with UPS eaton3s@localhost established

~ # upsc
Error: invalid UPS definition.
Required format: upsname[@hostname[:port]]
~ # upsd
Network UPS Tools upsd merge-with-ng-1491-g4a3ee6da
Fatal error: A previous upsd instance is already running!
Either stop the previous instance first, or use the 'reload' command.

~ # upsc -L
eaton3s: EATON UPS
~ # upsc eaton3s
battery.charge: 100
battery.charge.low: 40
battery.runtime: 1050
battery.type: PbAc
device.mfr: EATON
device.model: Eaton 3S 700
device.serial: 000000000
device.type: ups
driver.flag.ignorelb: enabled
driver.name: usbhid-ups
driver.parameter.pollfreq: 30
driver.parameter.pollinterval: 2
driver.parameter.port: auto
driver.parameter.synchronous: no
driver.version: merge-with-ng-1491-g4a3ee6da
driver.version.data: MGE HID 1.39
driver.version.internal: 0.41
input.transfer.high: 264
input.transfer.low: 184
outlet.1.desc: PowerShare Outlet 1
outlet.1.id: 2
outlet.1.status: on
outlet.1.switchable: yes
outlet.2.desc: PowerShare Outlet 2
outlet.2.id: 3
outlet.2.status: off
outlet.2.switchable: yes
outlet.desc: Main Outlet
outlet.id: 1
outlet.switchable: no
output.frequency.nominal: 50
output.voltage: 230.0
output.voltage.nominal: 230
ups.beeper.status: enabled
ups.delay.shutdown: 20
ups.delay.start: 30
ups.firmware: 02
ups.load: 19
ups.mfr: EATON
ups.model: Eaton 3S 700
ups.power.nominal: 700
ups.productid: ffff
ups.serial: 000000000
ups.status: OL
ups.timer.shutdown: -1
ups.timer.start: -1
ups.vendorid: 0463
~ #
```
