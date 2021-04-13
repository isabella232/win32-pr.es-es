---
description: Representa los atributos de los servicios básicos de entrada y salida (BIOS) del sistema del equipo que están instalados en un equipo.
ms.assetid: e4a5aaf0-0432-4517-97b7-ac05ffd10b5b
ms.tgt_platform: multiple
title: Win32_BIOS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BIOS
- Win32_BIOS.BiosCharacteristics
- Win32_BIOS.BIOSVersion
- Win32_BIOS.BuildNumber
- Win32_BIOS.Caption
- Win32_BIOS.CodeSet
- Win32_BIOS.CurrentLanguage
- Win32_BIOS.Description
- Win32_BIOS.EmbeddedControllerMajorVersion
- Win32_BIOS.EmbeddedControllerMinorVersion
- Win32_BIOS.IdentificationCode
- Win32_BIOS.InstallableLanguages
- Win32_BIOS.InstallDate
- Win32_BIOS.LanguageEdition
- Win32_BIOS.ListOfLanguages
- Win32_BIOS.Manufacturer
- Win32_BIOS.Name
- Win32_BIOS.OtherTargetOS
- Win32_BIOS.PrimaryBIOS
- Win32_BIOS.ReleaseDate
- Win32_BIOS.SerialNumber
- Win32_BIOS.SMBIOSBIOSVersion
- Win32_BIOS.SMBIOSMajorVersion
- Win32_BIOS.SMBIOSMinorVersion
- Win32_BIOS.SMBIOSPresent
- Win32_BIOS.SoftwareElementID
- Win32_BIOS.SoftwareElementState
- Win32_BIOS.Status
- Win32_BIOS.SystemBiosMajorVersion
- Win32_BIOS.SystemBiosMinorVersion
- Win32_BIOS.TargetOperatingSystem
- Win32_BIOS.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c1e953c9c1348a133cf4755ab04f6024c42034
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539237"
---
# <a name="win32_bios-class"></a><span data-ttu-id="41c61-103">\_Clase de BIOS Win32</span><span class="sxs-lookup"><span data-stu-id="41c61-103">Win32\_BIOS class</span></span>

<span data-ttu-id="41c61-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ BIOS de Win32** representa los atributos de los servicios básicos de entrada y salida (BIOS) del sistema del equipo que están instalados en un equipo.</span><span class="sxs-lookup"><span data-stu-id="41c61-104">The **Win32\_BIOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the attributes of the computer system's basic input/output services (BIOS) that are installed on a computer.</span></span>

<span data-ttu-id="41c61-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="41c61-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="41c61-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="41c61-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c61-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41c61-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BIOS : CIM_BIOSElement
{
  uint16   BiosCharacteristics[];
  string   BIOSVersion[];
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   CurrentLanguage;
  string   Description;
  uint8    EmbeddedControllerMajorVersion;
  uint8    EmbeddedControllerMinorVersion;
  string   IdentificationCode;
  uint16   InstallableLanguages;
  datetime InstallDate;
  string   LanguageEdition;
  String   ListOfLanguages[];
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  boolean  PrimaryBIOS;
  datetime ReleaseDate;
  string   SerialNumber;
  string   SMBIOSBIOSVersion;
  uint16   SMBIOSMajorVersion;
  uint16   SMBIOSMinorVersion;
  boolean  SMBIOSPresent;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint8    SystemBiosMajorVersion;
  uint8    SystemBiosMinorVersion;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="41c61-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="41c61-108">Members</span></span>

<span data-ttu-id="41c61-109">La **clase \_ BIOS de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="41c61-109">The **Win32\_BIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="41c61-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41c61-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41c61-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41c61-111">Properties</span></span>

<span data-ttu-id="41c61-112">La **clase \_ BIOS de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="41c61-112">The **Win32\_BIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41c61-113">**BiosCharacteristics**</span><span class="sxs-lookup"><span data-stu-id="41c61-113">**BiosCharacteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-114">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c61-114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41c61-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-116">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| características del BIOS del tipo de SMBIOS 0")</span><span class="sxs-lookup"><span data-stu-id="41c61-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Characteristics")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-117">Matriz de características del BIOS admitidas por el sistema tal y como se define en la especificación de referencia de BIOS de administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="41c61-117">Array of BIOS characteristics supported by the system as defined by the System Management BIOS Reference Specification.</span></span>

<span data-ttu-id="41c61-118">Este valor procede del miembro **características del BIOS** de la estructura de **información del BIOS** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-118">This value comes from the **BIOS Characteristics** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="41c61-119">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="41c61-119">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="41c61-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="41c61-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="41c61-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (1)</span><span class="sxs-lookup"><span data-stu-id="41c61-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c61-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="41c61-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>

<span data-ttu-id="41c61-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**Características del BIOS no admitidas** (3)</span><span class="sxs-lookup"><span data-stu-id="41c61-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**BIOS Characteristics Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA compatible** (4)</span><span class="sxs-lookup"><span data-stu-id="41c61-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**Se admite MCA** (5)</span><span class="sxs-lookup"><span data-stu-id="41c61-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**MCA is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**Se admite EISA** (6)</span><span class="sxs-lookup"><span data-stu-id="41c61-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**Se admite PCI** (7)</span><span class="sxs-lookup"><span data-stu-id="41c61-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="41c61-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Se admite la tarjeta PC (PCMCIA)** (8)</span><span class="sxs-lookup"><span data-stu-id="41c61-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**PC Card (PCMCIA) is supported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Se admite plug and Play** (9)</span><span class="sxs-lookup"><span data-stu-id="41c61-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug and Play is supported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**Se admite APM** (10)</span><span class="sxs-lookup"><span data-stu-id="41c61-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM is supported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>

<span data-ttu-id="41c61-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS es actualizable (Flash)** (11)</span><span class="sxs-lookup"><span data-stu-id="41c61-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS is Upgradeable (Flash)** (11)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-132">BIOS actualizable (Flash)</span><span class="sxs-lookup"><span data-stu-id="41c61-132">BIOS is Upgradable (Flash)</span></span>

</dd> <dt>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>

<span data-ttu-id="41c61-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**Se permite la sombra del BIOS** (12)</span><span class="sxs-lookup"><span data-stu-id="41c61-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**BIOS shadowing is allowed** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA es compatible** (13)</span><span class="sxs-lookup"><span data-stu-id="41c61-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA is supported** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>

<span data-ttu-id="41c61-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>La **compatibilidad con ESCD está disponible** (14)</span><span class="sxs-lookup"><span data-stu-id="41c61-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**ESCD support is available** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Se admite el arranque desde el CD** (15)</span><span class="sxs-lookup"><span data-stu-id="41c61-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Boot from CD is supported** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Se admite el arranque seleccionable** (16)</span><span class="sxs-lookup"><span data-stu-id="41c61-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Selectable Boot is supported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>

<span data-ttu-id="41c61-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>La **ROM del BIOS está socket** (17)</span><span class="sxs-lookup"><span data-stu-id="41c61-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM is socketed** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="41c61-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Se admite el arranque desde PC Card (PCMCIA)** (18)</span><span class="sxs-lookup"><span data-stu-id="41c61-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Boot From PC Card (PCMCIA) is supported** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**Se admite la especificación EDD (unidad de disco mejorada)** (19)</span><span class="sxs-lookup"><span data-stu-id="41c61-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**EDD (Enhanced Disk Drive) Specification is supported** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="41c61-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h: se admite el disquete japonés para NEC 9800 1.2 MB (3,5 \\ ", 1 k bytes/Sector, 360 rpm)** (20)</span><span class="sxs-lookup"><span data-stu-id="41c61-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5\\", 1k Bytes/Sector, 360 RPM) is supported** (20)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-142">Int 13h: se admite el disquete japonés para NEC 9800 1.2 MB (3,5, 1 k bytes/sector, 360 RPM)</span><span class="sxs-lookup"><span data-stu-id="41c61-142">Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="41c61-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h: se admite el disquete japonés para Toshiba 1.2 MB (3,5 \\ ", 360 rpm)** (21)</span><span class="sxs-lookup"><span data-stu-id="41c61-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5\\", 360 RPM) is supported** (21)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-144">Int 13h: se admite el disquete japonés para Toshiba 1.2 MB (3,5, 360 RPM)</span><span class="sxs-lookup"><span data-stu-id="41c61-144">Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="41c61-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "/360 KB se admiten los servicios de disquete** (22)</span><span class="sxs-lookup"><span data-stu-id="41c61-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" / 360 KB Floppy Services are supported** (22)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-146">Int 13h-5,25/360 se admiten los servicios de disquete de KB</span><span class="sxs-lookup"><span data-stu-id="41c61-146">Int 13h - 5.25 / 360 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="41c61-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "se admiten los servicios de disquete/1.2Mb** (23)</span><span class="sxs-lookup"><span data-stu-id="41c61-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" /1.2MB Floppy Services are supported** (23)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-148">Int 13h-5,25/1.2MB se admiten los servicios de disquete</span><span class="sxs-lookup"><span data-stu-id="41c61-148">Int 13h - 5.25 /1.2MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>

<span data-ttu-id="41c61-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h-3,5 \\ "/720 KB se admiten los servicios de disquete** (24)</span><span class="sxs-lookup"><span data-stu-id="41c61-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h - 3.5\\" / 720 KB Floppy Services are supported** (24)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-150">Int 13h-3,5/720 se admiten los servicios de disquete de KB</span><span class="sxs-lookup"><span data-stu-id="41c61-150">Int 13h - 3.5 / 720 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="41c61-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-3,5 \\ "/2,88 MB se admiten los servicios de disquete** (25)</span><span class="sxs-lookup"><span data-stu-id="41c61-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 3.5\\" / 2.88 MB Floppy Services are supported** (25)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-152">Se admiten los servicios de disquete int 13h-3,5/2,88 MB</span><span class="sxs-lookup"><span data-stu-id="41c61-152">Int 13h - 3.5 / 2.88 MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, se admite el servicio de pantalla de impresión** (26)</span><span class="sxs-lookup"><span data-stu-id="41c61-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, Print Screen Service is supported** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="41c61-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, se admiten los servicios de teclado 8042** (27)</span><span class="sxs-lookup"><span data-stu-id="41c61-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 Keyboard services are supported** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="41c61-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, se admiten los servicios en serie** (28)</span><span class="sxs-lookup"><span data-stu-id="41c61-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, Serial Services are supported** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="41c61-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, se admiten los servicios de impresora** (29)</span><span class="sxs-lookup"><span data-stu-id="41c61-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, printer services are supported** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="41c61-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, se admiten los servicios de vídeo CGA/mono** (30)</span><span class="sxs-lookup"><span data-stu-id="41c61-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, CGA/Mono Video Services are supported** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>

<span data-ttu-id="41c61-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span><span class="sxs-lookup"><span data-stu-id="41c61-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>

<span data-ttu-id="41c61-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**Compatible con ACPI** (32)</span><span class="sxs-lookup"><span data-stu-id="41c61-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI supported** (32)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-160">Se admite ACPI</span><span class="sxs-lookup"><span data-stu-id="41c61-160">ACPI is supported</span></span>

</dd> <dt>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**Se admite USB Legacy** (33)</span><span class="sxs-lookup"><span data-stu-id="41c61-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**USB Legacy is supported** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**Se admite AGP** (34)</span><span class="sxs-lookup"><span data-stu-id="41c61-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP is supported** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**Se admite el arranque de I2O** (35)</span><span class="sxs-lookup"><span data-stu-id="41c61-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**I2O boot is supported** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120 se admite el arranque** (36)</span><span class="sxs-lookup"><span data-stu-id="41c61-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120 boot is supported** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**Se admite el arranque de unidad Zip ATAPI** (37)</span><span class="sxs-lookup"><span data-stu-id="41c61-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**ATAPI ZIP Drive boot is supported** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="41c61-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**se admite el arranque 1394** (38)</span><span class="sxs-lookup"><span data-stu-id="41c61-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 boot is supported** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>

<span data-ttu-id="41c61-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Compatibilidad con batería inteligente** (39)</span><span class="sxs-lookup"><span data-stu-id="41c61-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Smart Battery supported** (39)</span></span>


</dt> <dd>

<span data-ttu-id="41c61-168">Se admite la batería inteligente</span><span class="sxs-lookup"><span data-stu-id="41c61-168">Smart Battery is supported</span></span>

</dd> <dt>

<span data-ttu-id="41c61-169">40 47</span><span class="sxs-lookup"><span data-stu-id="41c61-169">40 47</span></span>
</dt> <dd>

<span data-ttu-id="41c61-170">Reservado para el proveedor de BIOS</span><span class="sxs-lookup"><span data-stu-id="41c61-170">Reserved for BIOS vendor</span></span>

</dd> <dt>

<span data-ttu-id="41c61-171">48 63</span><span class="sxs-lookup"><span data-stu-id="41c61-171">48 63</span></span>
</dt> <dd>

<span data-ttu-id="41c61-172">Reservado para el proveedor del sistema</span><span class="sxs-lookup"><span data-stu-id="41c61-172">Reserved for system vendor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41c61-173">**BIOSVersion**</span><span class="sxs-lookup"><span data-stu-id="41c61-173">**BIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-174">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="41c61-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41c61-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c61-176">Matriz de la información completa del BIOS del sistema.</span><span class="sxs-lookup"><span data-stu-id="41c61-176">Array of the complete system BIOS information.</span></span> <span data-ttu-id="41c61-177">En muchos equipos puede haber varias cadenas de versión que se almacenan en el registro y que representan la información del BIOS del sistema.</span><span class="sxs-lookup"><span data-stu-id="41c61-177">In many computers there can be several version strings that are stored in the registry and represent the system BIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-178">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="41c61-178">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-181">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="41c61-181">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-182">Identificador interno de esta compilación de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="41c61-182">Internal identifier for this compilation of this software element.</span></span>

<span data-ttu-id="41c61-183">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-183">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="41c61-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-187">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="41c61-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-188">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="41c61-188">Short description of the object a one-line string.</span></span>

<span data-ttu-id="41c61-189">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-190">**Dese**</span><span class="sxs-lookup"><span data-stu-id="41c61-190">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-193">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="41c61-193">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="41c61-194">Conjunto de código utilizado por este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="41c61-194">Code set used by this software element.</span></span>

<span data-ttu-id="41c61-195">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-195">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-196">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="41c61-196">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-199">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 13 \| idioma actual")</span><span class="sxs-lookup"><span data-stu-id="41c61-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Current Language")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-200">Nombre del idioma actual del BIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-200">Name of the current BIOS language.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-201">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41c61-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-204">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="41c61-204">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-205">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="41c61-205">Description of the object.</span></span>

<span data-ttu-id="41c61-206">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-207">**EmbeddedControllerMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="41c61-207">**EmbeddedControllerMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-208">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="41c61-208">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-210">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| versión principal de firmware del controlador incrustado de tipo SMBIOS 0")</span><span class="sxs-lookup"><span data-stu-id="41c61-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-211">La versión principal del firmware del controlador insertado.</span><span class="sxs-lookup"><span data-stu-id="41c61-211">The major release of the embedded controller firmware.</span></span>

<span data-ttu-id="41c61-212">Este valor procede del miembro de la **versión principal del firmware del controlador insertado** de la estructura de **información del BIOS** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-212">This value comes from the **Embedded Controller Firmware Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="41c61-213">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="41c61-213">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-214">**EmbeddedControllerMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="41c61-214">**EmbeddedControllerMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-215">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="41c61-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-217">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| versión secundaria del firmware del controlador incrustado de tipo SMBIOS 0")</span><span class="sxs-lookup"><span data-stu-id="41c61-217">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-218">Versión secundaria del firmware del controlador insertado.</span><span class="sxs-lookup"><span data-stu-id="41c61-218">The minor release of the embedded controller firmware.</span></span>

<span data-ttu-id="41c61-219">Este valor procede del miembro de **versión secundaria del firmware del controlador incrustado** de la estructura de **información del BIOS** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-219">This value comes from the **Embedded Controller Firmware Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="41c61-220">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="41c61-220">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-221">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="41c61-221">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-224">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="41c61-224">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-225">Identificador del fabricante para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="41c61-225">Manufacturer's identifier for this software element.</span></span> <span data-ttu-id="41c61-226">A menudo, se trata de una referencia de almacén (SKU) o un número de pieza.</span><span class="sxs-lookup"><span data-stu-id="41c61-226">Often this will be a stock keeping unit (SKU) or a part number.</span></span>

<span data-ttu-id="41c61-227">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-227">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-228">**InstallableLanguages**</span><span class="sxs-lookup"><span data-stu-id="41c61-228">**InstallableLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-229">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c61-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-231">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) de tipo ("SMBIOS \| Type 13 \| idiomas instalables")</span><span class="sxs-lookup"><span data-stu-id="41c61-231">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Installable Languages")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-232">Número de idiomas disponibles para la instalación en este sistema.</span><span class="sxs-lookup"><span data-stu-id="41c61-232">Number of languages available for installation on this system.</span></span> <span data-ttu-id="41c61-233">El lenguaje puede determinar propiedades como la necesidad de texto Unicode y bidireccional.</span><span class="sxs-lookup"><span data-stu-id="41c61-233">Language may determine properties such as the need for Unicode and bidirectional text.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="41c61-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-235">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41c61-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-237">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="41c61-237">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-238">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="41c61-238">Date and time the object was installed.</span></span> <span data-ttu-id="41c61-239">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="41c61-239">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="41c61-240">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-241">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="41c61-241">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-244">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información del componente de software de DMTF \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="41c61-244">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-245">Edición de idioma de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="41c61-245">Language edition of this software element.</span></span> <span data-ttu-id="41c61-246">Se deben usar los códigos de idioma definidos en ISO 639.</span><span class="sxs-lookup"><span data-stu-id="41c61-246">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="41c61-247">Cuando el elemento de software representa una versión multilingüe o internacional de un producto, se debe usar la cadena "multilingüe".</span><span class="sxs-lookup"><span data-stu-id="41c61-247">Where the software element represents a multilingual or international version of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="41c61-248">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-248">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-249">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="41c61-249">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-250">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="41c61-250">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="41c61-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-252">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| cadenas de lenguaje de tipo SMBIOS 13 \| ")</span><span class="sxs-lookup"><span data-stu-id="41c61-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Language Strings")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-253">Matriz de nombres de los idiomas disponibles para instalar BIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-253">Array of names of available BIOS-installable languages.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-254">**Le**</span><span class="sxs-lookup"><span data-stu-id="41c61-254">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-255">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-257">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="41c61-257">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-258">Fabricante de este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="41c61-258">Manufacturer of this software element.</span></span>

<span data-ttu-id="41c61-259">Este valor procede del miembro del **proveedor** de la estructura de **información del BIOS** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-259">This value comes from the **Vendor** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="41c61-260">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-260">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-261">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="41c61-261">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-262">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-264">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41c61-264">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41c61-265">Nombre usado para identificar este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="41c61-265">Name used to identify this software element.</span></span>

<span data-ttu-id="41c61-266">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-266">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-267">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="41c61-267">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-268">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-270">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="41c61-270">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-271">Registra el fabricante y el tipo de sistema operativo para un elemento de software cuando la propiedad **TargetOperatingSystem** tiene un valor de 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="41c61-271">Records the manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 (Other).</span></span> <span data-ttu-id="41c61-272">Cuando **TargetOperatingSystem** tiene un valor de 1, **OtherTargetOS** debe tener un valor que no sea NULL.</span><span class="sxs-lookup"><span data-stu-id="41c61-272">When **TargetOperatingSystem** has a value of 1, **OtherTargetOS** must have a nonnull value.</span></span> <span data-ttu-id="41c61-273">Para todos los demás valores de **TargetOperatingSystem**, **OtherTargetOS** es **null**.</span><span class="sxs-lookup"><span data-stu-id="41c61-273">For all other values of **TargetOperatingSystem**, **OtherTargetOS** is **NULL**.</span></span>

<span data-ttu-id="41c61-274">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-274">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-275">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="41c61-275">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-276">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="41c61-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-278">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS del sistema DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="41c61-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-279">Si es **true**, se trata del BIOS principal del equipo.</span><span class="sxs-lookup"><span data-stu-id="41c61-279">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

<span data-ttu-id="41c61-280">Esta propiedad se hereda de [**\_ BIOSElement CIM**](cim-bioselement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-280">This property is inherited from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-281">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="41c61-281">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-282">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41c61-282">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41c61-284">Fecha de lanzamiento del BIOS de Windows con el formato de hora universal coordinada (UTC) de AAAAMMDDHHMMSS. MMMMMM (+-) OOO.</span><span class="sxs-lookup"><span data-stu-id="41c61-284">Release date of the Windows BIOS in the Coordinated Universal Time (UTC) format of YYYYMMDDHHMMSS.MMMMMM(+-)OOO.</span></span>

<span data-ttu-id="41c61-285">Este valor procede del miembro de **fecha de lanzamiento de BIOS** de la estructura de información de **BIOS** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-285">This value comes from the **BIOS Release Date** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-286">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="41c61-286">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-287">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-289">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="41c61-289">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-290">Número de serie asignado del elemento de software.</span><span class="sxs-lookup"><span data-stu-id="41c61-290">Assigned serial number of the software element.</span></span>

<span data-ttu-id="41c61-291">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-291">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-292">**SMBIOSBIOSVersion**</span><span class="sxs-lookup"><span data-stu-id="41c61-292">**SMBIOSBIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-295">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 0 \| BIOS versión")</span><span class="sxs-lookup"><span data-stu-id="41c61-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Version")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-296">Versión del BIOS tal como la ha indicado el SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-296">BIOS version as reported by SMBIOS.</span></span>

<span data-ttu-id="41c61-297">Este valor procede del miembro **versión del BIOS** de la estructura de **información del BIOS** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-297">This value comes from the **BIOS Version** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-298">**SMBIOSMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="41c61-298">**SMBIOSMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-299">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c61-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-301">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")</span><span class="sxs-lookup"><span data-stu-id="41c61-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-302">Número de versión principal de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-302">Major SMBIOS version number.</span></span> <span data-ttu-id="41c61-303">Esta propiedad es **null** si no se encuentra SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-303">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-304">**SMBIOSMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="41c61-304">**SMBIOSMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-305">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c61-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-307">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")</span><span class="sxs-lookup"><span data-stu-id="41c61-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-308">Número de versión secundaria de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-308">Minor SMBIOS version number.</span></span> <span data-ttu-id="41c61-309">Esta propiedad es **null** si no se encuentra SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-309">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-310">**SMBIOSPresent**</span><span class="sxs-lookup"><span data-stu-id="41c61-310">**SMBIOSPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-311">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="41c61-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-313">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| init")</span><span class="sxs-lookup"><span data-stu-id="41c61-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|Init")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-314">Si es **true**, el SMBIOS está disponible en este equipo.</span><span class="sxs-lookup"><span data-stu-id="41c61-314">If **true**, the SMBIOS is available on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-315">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="41c61-315">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-318">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="41c61-318">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="41c61-319">Identificador de este elemento de software; diseñado para usarse junto con otras claves para crear una representación única de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="41c61-319">Identifier for this software element; designed to be used in conjunction with other keys to create a unique representation of this instance.</span></span>

<span data-ttu-id="41c61-320">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-320">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41c61-321">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="41c61-321">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-322">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c61-322">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-324">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="41c61-324">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="41c61-325">Estado de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="41c61-325">State of a software element.</span></span>

<span data-ttu-id="41c61-326">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-326">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="41c61-327">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="41c61-327">The possible values are.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="41c61-328">Se pueden **implementar** (0)</span><span class="sxs-lookup"><span data-stu-id="41c61-328">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="41c61-329">**Instalable** (1)</span><span class="sxs-lookup"><span data-stu-id="41c61-329">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="41c61-330">**Archivo ejecutable** (2)</span><span class="sxs-lookup"><span data-stu-id="41c61-330">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="41c61-331">En **ejecución** (3)</span><span class="sxs-lookup"><span data-stu-id="41c61-331">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c61-332">**Estado**</span><span class="sxs-lookup"><span data-stu-id="41c61-332">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-335">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="41c61-335">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-336">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="41c61-336">Current status of the object.</span></span> <span data-ttu-id="41c61-337">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="41c61-337">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="41c61-338">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="41c61-338">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="41c61-339">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="41c61-339">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="41c61-340">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="41c61-340">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="41c61-341">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="41c61-341">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="41c61-342">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="41c61-343">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="41c61-343">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="41c61-344">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="41c61-344">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="41c61-345">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="41c61-345">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="41c61-346">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="41c61-346">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c61-347">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="41c61-347">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="41c61-348">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="41c61-348">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="41c61-349">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="41c61-349">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="41c61-350">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="41c61-350">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="41c61-351">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="41c61-351">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="41c61-352">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="41c61-352">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="41c61-353">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="41c61-353">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="41c61-354">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="41c61-354">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="41c61-355">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="41c61-355">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c61-356">**SystemBiosMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="41c61-356">**SystemBiosMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-357">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="41c61-357">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-359">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| System BIOS major release")</span><span class="sxs-lookup"><span data-stu-id="41c61-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-360">Versión principal del BIOS del sistema.</span><span class="sxs-lookup"><span data-stu-id="41c61-360">The major release of the System BIOS.</span></span>

<span data-ttu-id="41c61-361">Este valor procede del miembro de la **versión principal del BIOS del sistema** de la estructura de **información del BIOS** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-361">This value comes from the **System BIOS Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="41c61-362">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="41c61-362">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-363">**SystemBiosMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="41c61-363">**SystemBiosMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-364">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="41c61-364">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-366">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| System BIOS Minor release")</span><span class="sxs-lookup"><span data-stu-id="41c61-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-367">Versión secundaria del BIOS del sistema.</span><span class="sxs-lookup"><span data-stu-id="41c61-367">The minor release of the System BIOS.</span></span>

<span data-ttu-id="41c61-368">Este valor procede del miembro de **versión secundaria BIOS del sistema** de la estructura de **información del BIOS** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-368">This value comes from the **System BIOS Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="41c61-369">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="41c61-369">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="41c61-370">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="41c61-370">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-371">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41c61-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-373">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información \| del componente de software de DMTF 002,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="41c61-373">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-374">Sistema operativo de destino del elemento de software propietario.</span><span class="sxs-lookup"><span data-stu-id="41c61-374">Target operating system of the owning software element.</span></span>

<span data-ttu-id="41c61-375">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-375">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="41c61-376">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="41c61-376">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41c61-377">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="41c61-377">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41c61-378">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="41c61-378">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="41c61-379">**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="41c61-379">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="41c61-380">**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="41c61-380">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="41c61-381">**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="41c61-381">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="41c61-382">**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="41c61-382">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="41c61-383">**UNIX digital** (6)</span><span class="sxs-lookup"><span data-stu-id="41c61-383">**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="41c61-384">**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="41c61-384">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="41c61-385">**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="41c61-385">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="41c61-386">**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="41c61-386">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="41c61-387">**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="41c61-387">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="41c61-388">**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="41c61-388">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="41c61-389">**Os/2** (12)</span><span class="sxs-lookup"><span data-stu-id="41c61-389">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="41c61-390">**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="41c61-390">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="41c61-391">**Msdos** (14)</span><span class="sxs-lookup"><span data-stu-id="41c61-391">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="41c61-392">**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="41c61-392">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="41c61-393">**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="41c61-393">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="41c61-394">**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="41c61-394">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="41c61-395">**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="41c61-395">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="41c61-396">**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="41c61-396">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="41c61-397">**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="41c61-397">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="41c61-398">**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="41c61-398">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="41c61-399">**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="41c61-399">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="41c61-400">**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="41c61-400">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="41c61-401">**UNIX que depende** de (24)</span><span class="sxs-lookup"><span data-stu-id="41c61-401">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="41c61-402">**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="41c61-402">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="41c61-403">**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="41c61-403">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="41c61-404">**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="41c61-404">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="41c61-405">**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="41c61-405">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="41c61-406">**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="41c61-406">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="41c61-407">**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="41c61-407">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="41c61-408">**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="41c61-408">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="41c61-409">**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="41c61-409">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="41c61-410">**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="41c61-410">**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="41c61-411">**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="41c61-411">**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="41c61-412">**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="41c61-412">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="41c61-413">**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="41c61-413">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="41c61-414">**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="41c61-414">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="41c61-415">**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="41c61-415">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="41c61-416">**VM/sec** (39)</span><span class="sxs-lookup"><span data-stu-id="41c61-416">**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="41c61-417">**UNIX interactivo** (40)</span><span class="sxs-lookup"><span data-stu-id="41c61-417">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="41c61-418">**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="41c61-418">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="41c61-419">**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="41c61-419">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="41c61-420">**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="41c61-420">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="41c61-421">**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="41c61-421">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="41c61-422">**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="41c61-422">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="41c61-423">**Kernel de Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="41c61-423">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="41c61-424">**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="41c61-424">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="41c61-425">**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="41c61-425">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="41c61-426">**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="41c61-426">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="41c61-427">**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="41c61-427">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="41c61-428">**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="41c61-428">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="41c61-429">**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="41c61-429">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="41c61-430">**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="41c61-430">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="41c61-431">**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="41c61-431">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="41c61-432">**NextStep** (55)</span><span class="sxs-lookup"><span data-stu-id="41c61-432">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="41c61-433">**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="41c61-433">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="41c61-434">**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="41c61-434">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="41c61-435">**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="41c61-435">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="41c61-436">**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="41c61-436">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="41c61-437">**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="41c61-437">**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="41c61-438">**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="41c61-438">**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41c61-439">**Versión**</span><span class="sxs-lookup"><span data-stu-id="41c61-439">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c61-440">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41c61-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41c61-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41c61-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c61-442">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hardware \\ \\ Description \\ \\ System \| SystemBiosVersion")</span><span class="sxs-lookup"><span data-stu-id="41c61-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HARDWARE\\\\Description\\\\System\|SystemBiosVersion")</span></span>
</dt> </dl>

<span data-ttu-id="41c61-443">Versión del BIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-443">Version of the BIOS.</span></span> <span data-ttu-id="41c61-444">Esta cadena la crea el fabricante del BIOS.</span><span class="sxs-lookup"><span data-stu-id="41c61-444">This string is created by the BIOS manufacturer.</span></span>

<span data-ttu-id="41c61-445">Esta propiedad se hereda de [**\_ SoftwareElement CIM**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-445">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41c61-446">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41c61-446">Remarks</span></span>

<span data-ttu-id="41c61-447">La **clase \_ BIOS de Win32** se deriva [**del \_ BIOSElement CIM**](cim-bioselement.md).</span><span class="sxs-lookup"><span data-stu-id="41c61-447">The **Win32\_BIOS** class is derived from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

<span data-ttu-id="41c61-448">Las propiedades de la **clase \_ BIOS de Win32** pueden cambiar para un sistema de equipo específico con el mismo BIOS, por ejemplo, el arranque a través de un modo BIOS heredado y el arranque a través del modo de BIOS UEFI.</span><span class="sxs-lookup"><span data-stu-id="41c61-448">The properties in the **Win32\_BIOS** class may change for a specific computer system with the same BIOS, for example booting through a legacy BIOS mode vs. booting through UEFI BIOS mode.</span></span> <span data-ttu-id="41c61-449">Sin embargo, las propiedades recuperadas de las estructuras de SMBIOS deben ser las mismas.</span><span class="sxs-lookup"><span data-stu-id="41c61-449">However the properties retrieved from the SMBIOS structures should remain the same.</span></span>

## <a name="examples"></a><span data-ttu-id="41c61-450">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="41c61-450">Examples</span></span>

<span data-ttu-id="41c61-451">El ejemplo de PowerShell [Get-ComputerInfo-Query Computer info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) de PowerShell en la galería de TechNet utiliza varias llamadas a hardware y software, incluido **\_ BIOS de Win32**, para mostrar información acerca de un sistema local o remoto.</span><span class="sxs-lookup"><span data-stu-id="41c61-451">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to display information about a local or remote system.</span></span>

<span data-ttu-id="41c61-452">El ejemplo [generar información del sistema como jerarquía XML](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) de VBScript en la galería de TechNet utiliza varias llamadas a hardware y software, incluido **\_ BIOS Win32**, para generar una representación XML de un sistema mediante una salida XML manual.</span><span class="sxs-lookup"><span data-stu-id="41c61-452">The [Generate system information as XML hierarchy](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) VBScript sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to generate an XML representation of a system using a manual XML output.</span></span>

<span data-ttu-id="41c61-453">El siguiente ejemplo de código de PowerShell usa el **\_ BIOS Win32** para devolver características del BIOS</span><span class="sxs-lookup"><span data-stu-id="41c61-453">The following PowerShell code sample uses **Win32\_BIOS** to return characteristics of the BIOS</span></span>


```PowerShell
# wmi-win32_bios.ps1
# Demonstrates use of Win32_Bios WMI class
# Thomas Lee - tfl@psp.co.uk



# Helper function to return characterics of the BIOS
function get-WmiBiosCharacteristics {
param ([uint16] $char)

# parse and return values

If ($char -le 39) {

switch ($char) {
0   {"00-Reserved"}
1   {"01-Reserved"}
2   {"02-Unknown"}
3   {"03-BIOS Characteristics Not Supported"}
4   {"04-ISA is supported"}
5   {"05-MCA is supported"}
6   {"06-EISA is supported"}
7   {"07-PCI is supported"}
8   {"08-PC Card (PCMCIA) is supported"}
9   {"09-Plug and Play is supported"}
10  {"10-APM is supported"}
11  {"11-BIOS is Upgradable (Flash)"}
12  {"12-BIOS shadowing is allowed"}
13  {"13-VL-VESA is supported"}
14  {"14-ESCD support is available"}
15  {"15-Boot from CD is supported"}
16  {"16-Selectable Boot is supported"}
17  {"17-BIOS ROM is socketed"}
18  {"18-Boot From PC Card (PCMCIA) is supported"}
19  {"19-EDD (Enhanced Disk Drive) Specification is supported"}
20  {"20-Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported"}
21  {"21-Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported"}
22  {"22-Int 13h - 5.25 / 360 KB Floppy Services are supported"}
23  {"23-Int 13h - 5.25 /1.2MB Floppy Services are supported"}
24  {"24-Int 13h - 3.5 / 720 KB Floppy Services are supported"}
25  {"25-Int 13h - 3.5 / 2.88 MB Floppy Services are supported"}
26  {"26-Int 5h, Print Screen Service is supported"}
27  {"27-Int 9h, 8042 Keyboard services are supported"}
28  {"28-Int 14h, Serial Services are supported"}
29  {"29-Int 17h, printer services are supported"}
30  {"30-Int 10h, CGA/Mono Video Services are supported"}
31  {"31-NEC PC-98"}
32  {"32-ACPI supported"}
33  {"33-USB Legacy is supported"}
34  {"34-AGP is supported"}
35  {"35-I2O boot is supported"}
36  {"36-LS-120 boot is supported"}
37  {"37-ATAPI ZIP Drive boot is supported"}
38  {"38-1394 boot is supported"}
39  {"39-Smart Battery supported"}
}
Return
}

If ($char -ge 40 -and $char -le 45) {
          "{0}-Reserved for BIOS vendor" -f $char
return
}

If ($char -ge 48 -and $char -le 63) {
           "{0}-Reserved for system vendor" -f $char
return
}
"{0}-Unknown Value " -f $char
}

# Get BIOS information from WMI
$bios = Get-WMIObject Win32_Bios

# Display BIOS Details
"Win32_Bios WMI Information"
"Bios Characteristics"
foreach ($ch in $bios.BiosCharacteristics) {
"                      :  {0}" -f  (Get-WmiBiosCharacteristics($ch))
} 
"Bios Version          :  {0}" -f $bios.BiosVersion
"Codeset               :  {0}" -f $bios.Codeset
"CurrentLanguage       :  {0}" -f $bios.CurrentLanguage
"Description           :  {0}" -f $bios.Description
"IdentificatonCode     :  {0}" -f $bios.IdentificatonCode
"InstallableLanguages  :  {0}" -f $bios.InstallableLanguages
"InstallDate           :  {0}" -f $bios.InstallDate 
"LanguageEdition       :  {0}" -f $bios.LanguageEdition
"ListOfLanguages       :  {0}" -f $bios.ListOfLanguages
"Manufacturer          :  {0}" -f $bios.Manufacturer
"OtherTargetOS         :  {0}" -f $bios.OtherTargetOS
"PrimaryBIOS           :  {0}" -f $bios.PrimaryBIOS
"ReleaseDate           :  {0}" -f $bios.ReleaseDate
"SerialNumber          :  {0}" -f $bios.SerialNumber
"SMBIOSBIOSVersion     :  {0}" -f $bios.SMBIOSBIOSVersion
"SMBIOSMajorVersion    :  {0}" -f $bios.SMBIOSMajorVersion
"SMBIOSMinorVersion    :  {0}" -f $bios.SMBIOSMinorVersion
"SoftwareElementID     :  {0}" -f $bios.SoftwareElementID 
"SoftwareElementState  :  {0}" -f $bios.SoftwareElementState
"TargetOperatingSystem :  {0}" -f $bios.TargetOperatingSystem
"Version               :  {0}" -f $bios.Version 
```



<span data-ttu-id="41c61-454">El ejemplo de código anterior devuelve la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="41c61-454">The previous code sample returns the following information:</span></span>

``` syntax
Win32_Bios WMI Information
Bios Characteristics
                      :  04-ISA is supported
                      :  07-PCI is supported
                      :  08-PC Card (PCMCIA) is supported
                      :  09-Plug and Play is supported
                      :  11-BIOS is Upgradable (Flash)
                      :  12-BIOS shadowing is allowed
                      :  15-Boot from CD is supported
                      :  16-Selectable Boot is supported
                      :  24-Int 13h - 3.5 / 720 KB Floppy Services are supported
                      :  26-Int 5h, Print Screen Service is supported
                      :  27-Int 9h, 8042 Keyboard services are supported
                      :  28-Int 14h, Serial Services are supported
                      :  29-Int 17h, printer services are supported
                      :  30-Int 10h, CGA/Mono Video Services are supported
                      :  32-ACPI supported
                      :  33-USB Legacy is supported
                      :  34-AGP is supported
                      :  39-Smart Battery supported
                      :  40-Reserved for BIOS vendor
                      :  41-Reserved for BIOS vendor
                      :  42-Reserved for BIOS vendor
                      :  58-Reserved for system vendor
                      :  74-Unknown Value
Bios Version          :  DELL   - 27d60a0d
Codeset               :
CurrentLanguage       :  en|US|iso8859-1
Description           :  Phoenix ROM BIOS PLUS Version 1.10 A04
IdentificatonCode     :
InstallableLanguages  :  1
InstallDate           :
LanguageEdition       :
ListOfLanguages       :  en|US|iso8859-1
Manufacturer          :  Dell Inc.
OtherTargetOS         :
PrimaryBIOS           :  True
ReleaseDate           :  20061013000000.000000+000
SerialNumber          :  DDC2H2J
SMBIOSBIOSVersion     :  A04
SMBIOSMajorVersion    :  2
SMBIOSMinorVersion    :  4
SoftwareElementID     :  Phoenix ROM BIOS PLUS Version 1.10 A04
SoftwareElementState  :  3
TargetOperatingSystem :  0
Version               :  DELL   - 27d60a0d
```

## <a name="requirements"></a><span data-ttu-id="41c61-455">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c61-455">Requirements</span></span>



| <span data-ttu-id="41c61-456">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c61-456">Requirement</span></span> | <span data-ttu-id="41c61-457">Value</span><span class="sxs-lookup"><span data-stu-id="41c61-457">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c61-458">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c61-458">Minimum supported client</span></span><br/> | <span data-ttu-id="41c61-459">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41c61-459">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41c61-460">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c61-460">Minimum supported server</span></span><br/> | <span data-ttu-id="41c61-461">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41c61-461">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41c61-462">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41c61-462">Namespace</span></span><br/>                | <span data-ttu-id="41c61-463">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="41c61-463">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41c61-464">MOF</span><span class="sxs-lookup"><span data-stu-id="41c61-464">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41c61-465"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41c61-465"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41c61-466">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41c61-466">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c61-467"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c61-467"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c61-468">Vea también</span><span class="sxs-lookup"><span data-stu-id="41c61-468">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c61-469">**\_BIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="41c61-469">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="41c61-470">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="41c61-470">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

