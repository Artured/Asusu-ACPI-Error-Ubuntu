
# Hola!



Esta es una solucion a los Errores de ACPI para dual boot ( W10 & Ubuntu )  en una Laptop ASUS TUF GAMING con NVMe SSD M.2


------------

#### Especificaciones

- ASUS TUF FX505DY-BQ002T 15.6-inch FHD Gaming Laptop
- AMD Ryzen 5-3550H/16GB
- 256GB NVMe SSD M.2
- Windows 10
- Radeon RX 560X 4GB Graphics


------------




#### Prerrequisitos

* Memoria USB Booteable con Ubuntu.

   `Sistema de archivos - Fat32`

   `Esquema de particion - MBR`


> Crear soportes USB de arranque con [RUFUS](https://rufus.ie/es/ "RUFUS")


* Secure Boot.

	`deshabilitado`


------------


####Inicio

* Dentro de la USB.

   `cd   /Boot /grub`


* Encontraras el archivo:

	`grub.cfg`

* En la linea que inicia : 


   `linux	/casper/vmlinuz  file=/cdrom/preseed/ubuntu.seed boot=casper only-ubiquity quiet splash      ***AQUI**`

* Añade la siguiente instruccion.


   `--- nvme_core.default_ps_max_latency_us=5500`




* Quedando así.



![](https://raw.githubusercontent.com/Artured/Asusu-ACPI-Error-Ubuntu/main/images/code-snapshot-2.png)



* Guardalo y correlo.