
# Hi!

🇲🇽   [Spanish](http://google.com "Spanish")

This is a solution for the ACPI Error on dual boot ( W10 & Ubuntu ) in a Laptop ASUS TUF GAMING con NVMe SSD M.2


------------

#### Specs

- ASUS TUF FX505DY-BQ002T 15.6-inch FHD Gaming Laptop
- AMD Ryzen 5-3550H/16GB
- 256GB NVMe SSD M.2
- Windows 10
- Radeon RX 560X 4GB Graphics


------------




#### Requirements

* Pendrive Booteable with Ubuntu.

 `File sistem - Fat32`

 `Partition scheme - MBR`


> Make a Pendrive Booteable with [RUFUS](https://rufus.ie/es/ "RUFUS")


* Secure Boot.

	`disabled`


------------


#### Start

* In the pendrive go to:

 `cd   /Boot /grub`


* Edit the next file:

	`grub.cfg`

* Find the line that starts with : 


   `linux	/casper/vmlinuz  file=/cdrom/preseed/ubuntu.seed boot=casper only-ubiquity quiet splash      ***HERE**`

* Add the following instruction.


   `--- nvme_core.default_ps_max_latency_us=5500`




* Like This.



![](https://raw.githubusercontent.com/Artured/Asusu-ACPI-Error-Ubuntu/main/images/code-snapshot-2.png)

