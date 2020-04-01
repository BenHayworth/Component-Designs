# Design

3D printing and laser cutting designs used in the [Reiser Lab](https://www.janelia.org/lab/reiser-lab).


## Holder

Everything related to the tether between fly and robot.

- [Holder-cone_pointy](Holder/Holder-cone_pointy.scad) pointy cone, replaces earlier Holder-cone base design.
- [Holder-cone_pointy_tip-0.07](Holder/Holder-cone_pointy_tip-0.07.scad) additional cylindric tip (0.07mm diameter) on pointy cone.
- [Holder-cone_flat_hole-0.1](Holder/Holder-cone_flat_hole-0.1.scad) cone cut off, instead added a hole (0.1mm diameter) for a metal tether.
- [Holder-cone_flat_hole-0.2](Holder/Holder-cone_flat_hole-0.2.scad) cone cut off, instead added a hole (0.2mm diameter) for a metal tether.
- [Holder-cone_flat_hole-0.3](Holder/Holder-cone_flat_hole-0.3.scad) cone cut off, instead added a hole (0.3mm diameter) for a metal tether.
- [Holder-cone_flat_helical-cutout](Holder-cone_flat_helical-cutout.scad) cone cut off, the hole is constructed of overlapping semi-circles, trying to address the minimal production size of the printers.
- [Holder-Luer](Holder/Holder-Luer.FCStd) Magnetic holder to Luer lock
- [Flyplate](Holder/Flyplate5.md) head fixation plate for imaging experiments


## Camera

Camera related designs.

- [Adapter_PS3-PCB-to-lens-mount.scad](Camera/Adapter_PS3-PCB-to-lens-mount.scad) basic solid that connects to the PCB (the two pins) and can be used to connect to a standard M12 lens holder
- [PS3-lens-mount_M12.scad](Camera/PS3-lens-mount_M12.scad) the adapter from PS3-PCB including the lens mount


## Plate-Sarcophagus

Cooling plate and fly sarcophagus to hold the flies in place, usually under a microscope and during tethering.

- [Cooling_Plate](Plate-Sarcophagus/Cooling_plate.md) A cooling plate body with fly sarcophagus inlay
- [Sacrophagus_size-test](Plate-Sarcophagus/Sacrophagus_size-test.scad) Sarcophagus design for test prints (3D plastic prints on top of peltier element)
- [Sarcophagus_platform](Plate-Sarcophagus/Sarcophagus_platform.scad) Sarcophagus design used at CSHL workshop 2019


## Misc

Not fitting anywhere else.

- [Wells_3x3_optogenetics](Misc/RedPlate-Departments.svg) (and -cover) to observe individual flies on light plate
- [Adapter_metric-imperial_micro-manipulator_bottom](Misc/Adapter_metric-imperial_micro-manipulator_bottom.svg) adapt metric micro manipulator to imperial breadboard
- [Adapter_metric-imperial_micro-manipulator_top](Misc/Adapter_metric-imperial_micro-manipulator_top.svg) Add central crane mount to the top of a metric manipulator
- [Holder_Treadmill_Barb-adapter](Misc/Holder_Treadmill_Barb-adapter.stl) Ball holder for spherical treadmill with adapter for tubing
- [Case_JetsonNano_*](Misc/Case_JetsonNano_Bottom.FCStd) Case for Jetson Nano (from thingiverse)
- [Case_RaspberryPi3_*](Misc/Case_RaspberryPi3_Top.FCStd) Case for Raspberry Pi 3 (from thiniverse)
- [Holder_Magnet_Robot](Misc/Holder_Magnet_Robot.FCStd) magnet holder for robot
- [Adapter_fly-vial-to-5mm-tube](Misc/Adapter_fly-vial-to-5mm-tube.FCStd) Funnel to move flies from one vial to another
- [Wingbeat-analyzer_sensor_mask](Misc/Wingbeat-analyzer_sensor_mask.svg) Different masks to verify best shadow for Wingbeat analyzer


# Manufacturing

With the help of [jET](https://www.janelia.org/support-team/janelia-experimental-technology), we produce many of the designs in-house and on different machines. For best reproducibility we document some of the results in pictures. For those images, the 3D Printer shorthands in the file names stand for:

- form2: [Form 2](https://formlabs.com/3d-printers/form-2/) SLA printer, jET
- form3: [Form 3](https://formlabs.com/3d-printers/form-3/) SLA printer, jET
- connex: [Statsys Polyjet](https://www.stratasys.com/3d-printers/objet-260-500-connex1), jET
- f170: [Stratsys F170](https://www.stratasys.com/3d-printers/f123), W2


# Filetypes and applications

`*.FCStd` files are the native format of [FreeCAD](https://www.freecadweb.org/), an open-source 3D parametric modeller. It has a GUI to manipulate and parametrize models.

`*.scad` files are the native file format of [OpenSCAD](https://www.openscad.org/), "The Programmers Solid 3D CAD Modeller" – another open-source software (OSS). It uses a scripting language to build parametric models.

`*.[iam|ipt|idw]` files are the file format of [Autodesk Inventor](http://autodesk.com/inventor), a proprietary and commercial 3D CAD software. The extensions represent assembly, part, and drawing files respectively. 

`*.stl` are "stereolithography" files, containing unstructured triangulated surfaces of 3D models. This is the output format understood by our 3D printers, but not good for editing.

`*.svg` 2D Designs for laser cut, can be edited in the OSS [Inkscape](https://inkscape.org/). Sometimes `*.dxf` is used as an export format.

`*.md` with the same basename as other files contain additional information for that file. Usually that's related to licenses etc.

`*.[jpg|png]` pictures of the produced items. They usually follow the filename pattern `<design>_<printer>_<nr>_<date>`.

`*.pro` is a project file for the OSS [KiCad EDA](https://www.kicad-pcb.org/), an open-source electronics design automation suite. KiCad can produce `*.gbr` RS-274X gerber files for the manufacturers.


# Contribution

We welcome any kind of comments and corrections. You can either open an issue here on github or get in contact via the [Reiser Lab website](https://www.janelia.org/lab/reiser-lab). We are looking forward to your feedback.