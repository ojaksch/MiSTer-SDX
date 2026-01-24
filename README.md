## These are tools for the famous [SpartaDOS X](https://sdx.atari8.info/index.php), intended for use with the wonderful [MiSTer FPGA](https://github.com/MiSTer-devel/Wiki_MiSTer/wiki) and the magnificent [Atari800 Core](https://github.com/MiSTer-devel/Atari800_MiSTer)

Have a read of the [documentation](https://github.com/MiSTer-devel/Atari800_MiSTer/tree/VBXE), especially about the boot3.rom file and [about handling the PBI BIOS](https://github.com/MiSTer-devel/Atari800_MiSTer/tree/VBXE?tab=readme-ov-file#pbi-bios-atari800).  

Settings to be made in the Core:

- Set SIO drive speed to "Fast-1" (Pokey Divisor 1) or whatever you like, but not "Fast-0"!
- Mount a hard disk image as drive 4
- PBI BIOS: enabled
- PBI Splash: whatever you prefer
- PBI boot drive: APT
- Load Cart SDX450_ult320.rom
- Have fun!

The files (7z'd):
<table>
    <tr><td>CONFIG.SYS</td><td>An example config.sys including driver for VBXE(*)</td></tr>
    <tr><td>SDX450_ult320.rom</td><td>The original SpartaDOS X ROM file</td></tr>
    <tr><td>SDX_hdd.img</td><td>A 16MB bootable SDFS(*) hard disk including CONFIG.SYS</td></tr>
    <tr><td>SDX_hdd-VBXE.img</td><td>As before plus driver for VBXE(*).</td></tr>
    <tr><td>SDX_hdd-FAT.img</td><td>A 256MB bootable SDFS(*) hard disk including CONFIG.SYS and driver for FATFS(*). A 128MB FAT partition is available for data exchange, set to drive 3</td></tr>
    <tr><td>SDX_hdd-FAT-VBXE.img</td><td>As before plus driver for VBXE(*).</td></tr>
    <tr><td>SDX_hdd-empty.img</td><td>An empty 16MB hard disk</td></tr>
    <tr><td>SDX_megatoolkit.atr</td><td>The SpartaDOS SDFS(*) Tooldisk floppy, almost all tools and drivers unpacked for direct access</td></tr>
    <tr><td>SDX_empty.atr</td><td>A big empty SpartaDOS SDFS(*) floppy disk</td></tr>
    <tr><td>boot3.rom</td><td>The PBI ROM file for the MiSTer FPGA and its Atari800 Core</td></tr>
</table>

(\*) SDFS: SpartaDOS File System  
(\*) FATFS: A lightweight software library that implements FAT file system support (all modern OS'es)  
(\*) VBXE: Videoboard XE, a video enhancement upgrade board

All files and drivers are unpatched, unmodified and taken from the original SpartaDOS X tooldisk (but extracted from their archives).

---

## Changelog
- 2026-01-24: Added INIDOS, DISSDX, SD6502, VBFIX/VBFIX816, VPRINT, FSEL, UNIXTIME, PCLINK, CON, CON64, RC_VBXE, VBXE, VBXEFXS, CAD, CPMFS/USER, INDUS, XEPSET  
omitted: drivers/turbobrd  
DOSKEY added to config.sys  
config.sys loads drivers from CAR: or "the booted drive"  
Added an empty 1.4MB SDFS formatted floppy disk  
Reorganizised disk's layout and adjusted the paths in config.sys
- 2026-01-13: Initial commmit

---

## License
[The right to use, modify and republish has been kindly granted](https://forums.atariage.com/index.php?app=core&module=system&controller=redirect&url=https://forums.atariage.com/topic/378023-spartados-x-450/?do=findComment%26comment=5779930&key=2181e3c3ca0f619e8793139f27524f99b2863ec2a750faf07dd7a5065c3876c4&email=1&type=notification_new_comment)

<a href="https://sdx.atari8.info/index.php" rel="SpartaDOS X homepage">![Foo](images/sdx-new.gif)</a>
