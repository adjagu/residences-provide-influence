-------------------------------------------------------------------------------
Technician Shelters Provide Influence
-------------------------------------------------------------------------------

Technician shelters now provide influence. Each technician shelter will provide
influence equal to the amount that <InfluenceAmount> is set to.

Technicians do not provide influence.
Technician shelters provide influence.

To change the amount of influence technician shelters provide alter
<InfluenceAmount>'s number in /data/config/export/main/asset/assets.xml

---------------------------------------
Author : adjagu
License: GPL-2.0-only
Version: 0.1.3
Source : https://github.com/adjagu/residences-provide-influence
---------------------------------------


-------------------------------------------------------------------------------
Modding and Anno 1800
-------------------------------------------------------------------------------

Since game update 17, Anno 1800 now supports loading mods without the need for
an external mod loader. To use mods with Anno 1800 a "mods" directory must be
created in Anno 1800's install directory.

Below is the default install directories for various stores:

Windows:
  Epic : C:\Program Files\Epic Games\Anno 1800\
  Steam: C:\Program Files (x86)\Steam\steamapps\common\Anno 1800\
  Uplay: C:\Program Files (x86)\Ubisoft\Ubisoft Game Launcher\games\Anno 1800\

Linux:
  Steam: ~/.local/share/Steam/steamapps/common/Anno 1800/


-------------------------------------------------------------------------------
How to Install This Mod
-------------------------------------------------------------------------------

Copy "[Gameplay] Technician Shelters Provide Influence" folder into
Anno 1800's "mods" directory.


-------------------------------------------------------------------------------
Mod Overview
-------------------------------------------------------------------------------

[Gameplay] Technician Shelters Provide Influence
  /data/config/export/main/asset/assets.xml
    /LICENSE.txt
    /modinfo.json
    /README.txt

assets.xml
  The actual modification.

LICENSE.txt
  The license for this modification. This modification uses and is released
  as "GPL 2.0 only".

modinfo.json
  A file used by Anno 1800's modloader and third-party mod managers. More
  information is available at the following url:

  https://github.com/anno-mods/Modinfo

README.txt
  This file.


-------------------------------------------------------------------------------
How to Edit This Mod
-------------------------------------------------------------------------------

By default this modification enables each technician shelter to produce
two (2) influence. This is shown in the following code:

---------------------------------------
<?xml version="1.0" encoding="utf-8"?>

<ModOps>

  <ModOp GUID="112652" Path="/Values" Type="Merge">
    <InfluenceSource>
      <InfluenceAmount>2</InfluenceAmount>
      <InfluenceSource>Culture</InfluenceSource>
    </InfluenceSource>
  </ModOp>

</ModOps>
---------------------------------------

If you would like each technician shelter to produce one hundred (100)
influence each you could use the following code:

---------------------------------------
<?xml version="1.0" encoding="utf-8"?>

<ModOps>

  <ModOp GUID="112652" Path="/Values" Type="Merge">
    <InfluenceSource>
      <InfluenceAmount>100</InfluenceAmount>
      <InfluenceSource>Culture</InfluenceSource>
    </InfluenceSource>
  </ModOp>

</ModOps>
