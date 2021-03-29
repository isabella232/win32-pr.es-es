---
description: Representa una unidad de CD-ROM en un equipo con Windows.
ms.assetid: 08087976-ca88-4ac8-9456-0d8bd799e66c
ms.tgt_platform: multiple
title: Clase Win32_CDROMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CDROMDrive
- Win32_CDROMDrive.Reset
- Win32_CDROMDrive.SetPowerState
- Win32_CDROMDrive.Availability
- Win32_CDROMDrive.Capabilities
- Win32_CDROMDrive.CapabilityDescriptions
- Win32_CDROMDrive.Caption
- Win32_CDROMDrive.CompressionMethod
- Win32_CDROMDrive.ConfigManagerErrorCode
- Win32_CDROMDrive.ConfigManagerUserConfig
- Win32_CDROMDrive.CreationClassName
- Win32_CDROMDrive.DefaultBlockSize
- Win32_CDROMDrive.Description
- Win32_CDROMDrive.DeviceID
- Win32_CDROMDrive.Drive
- Win32_CDROMDrive.DriveIntegrity
- Win32_CDROMDrive.ErrorCleared
- Win32_CDROMDrive.ErrorDescription
- Win32_CDROMDrive.ErrorMethodology
- Win32_CDROMDrive.FileSystemFlags
- Win32_CDROMDrive.FileSystemFlagsEx
- Win32_CDROMDrive.Id
- Win32_CDROMDrive.InstallDate
- Win32_CDROMDrive.LastErrorCode
- Win32_CDROMDrive.Manufacturer
- Win32_CDROMDrive.MaxBlockSize
- Win32_CDROMDrive.MaximumComponentLength
- Win32_CDROMDrive.MaxMediaSize
- Win32_CDROMDrive.MediaLoaded
- Win32_CDROMDrive.MediaType
- Win32_CDROMDrive.MfrAssignedRevisionLevel
- Win32_CDROMDrive.MinBlockSize
- Win32_CDROMDrive.Name
- Win32_CDROMDrive.NeedsCleaning
- Win32_CDROMDrive.NumberOfMediaSupported
- Win32_CDROMDrive.PNPDeviceID
- Win32_CDROMDrive.PowerManagementCapabilities
- Win32_CDROMDrive.PowerManagementSupported
- Win32_CDROMDrive.RevisionLevel
- Win32_CDROMDrive.SCSIBus
- Win32_CDROMDrive.SCSILogicalUnit
- Win32_CDROMDrive.SCSIPort
- Win32_CDROMDrive.SCSITargetId
- Win32_CDROMDrive.SerialNumber
- Win32_CDROMDrive.Size
- Win32_CDROMDrive.Status
- Win32_CDROMDrive.StatusInfo
- Win32_CDROMDrive.SystemCreationClassName
- Win32_CDROMDrive.SystemName
- Win32_CDROMDrive.TransferRate
- Win32_CDROMDrive.VolumeName
- Win32_CDROMDrive.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c352d2ee717f5eb888b49d6e5e8ff456cc5a85f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000735"
---
# <a name="win32_cdromdrive-class"></a><span data-ttu-id="d2eaf-103">\_Clase Win32 CDROMDrive</span><span class="sxs-lookup"><span data-stu-id="d2eaf-103">Win32\_CDROMDrive class</span></span>

<span data-ttu-id="d2eaf-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CDROMDrive de Win32** representa una unidad de CD-ROM en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-104">The **Win32\_CDROMDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a CD-ROM drive on a computer system running Windows.</span></span>

> [!Note]  
> <span data-ttu-id="d2eaf-105">Tenga en cuenta que el nombre de la unidad no se corresponde con la letra de unidad lógica asignada al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-105">Be aware that the name of the drive does not correspond to the logical drive letter assigned to the device.</span></span>

 

<span data-ttu-id="d2eaf-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d2eaf-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2eaf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2eaf-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CDROMDrive : CIM_CDROMDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  string   Drive;
  boolean  DriveIntegrity;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint16   FileSystemFlags;
  uint32   FileSystemFlagsEx;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint32   MaximumComponentLength;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  string   MfrAssignedRevisionLevel;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   RevisionLevel;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  string   SerialNumber;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  real64   TransferRate;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="d2eaf-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2eaf-109">Members</span></span>

<span data-ttu-id="d2eaf-110">La **clase \_ CDROMDrive de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d2eaf-110">The **Win32\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="d2eaf-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2eaf-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d2eaf-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2eaf-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d2eaf-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2eaf-113">Methods</span></span>

<span data-ttu-id="d2eaf-114">La clase **Win32 \_ CDROMDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-114">The **Win32\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="d2eaf-115">Método</span><span class="sxs-lookup"><span data-stu-id="d2eaf-115">Method</span></span>            | <span data-ttu-id="d2eaf-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2eaf-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2eaf-117">**Reset**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-117">**Reset**</span></span>         | <span data-ttu-id="d2eaf-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-118">Not implemented.</span></span> <span data-ttu-id="d2eaf-119">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ CDROMDrive**](cim-cdromdrive.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="d2eaf-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-120">**SetPowerState**</span></span> | <span data-ttu-id="d2eaf-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-121">Not implemented.</span></span> <span data-ttu-id="d2eaf-122">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ CDROMDrive**](cim-cdromdrive.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CDROMDrive**](cim-cdromdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d2eaf-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2eaf-123">Properties</span></span>

<span data-ttu-id="d2eaf-124">La **clase \_ CDROMDrive de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-124">The **Win32\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2eaf-125">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-129">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-129">Availability and status of the device.</span></span>

<span data-ttu-id="d2eaf-130">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d2eaf-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d2eaf-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d2eaf-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-134">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="d2eaf-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d2eaf-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d2eaf-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d2eaf-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d2eaf-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="d2eaf-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d2eaf-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="d2eaf-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d2eaf-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d2eaf-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d2eaf-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d2eaf-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d2eaf-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d2eaf-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d2eaf-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-149">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d2eaf-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d2eaf-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d2eaf-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d2eaf-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d2eaf-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d2eaf-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d2eaf-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-162">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-164">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-165">Matriz de funcionalidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-165">Array of capabilities of the media access device.</span></span> <span data-ttu-id="d2eaf-166">Por ejemplo, el dispositivo puede admitir el acceso aleatorio (3), el medio extraíble (7) y la limpieza automática (9).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-166">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="d2eaf-167">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d2eaf-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d2eaf-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="d2eaf-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="d2eaf-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="d2eaf-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="d2eaf-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="d2eaf-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="d2eaf-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-176">Admite medios extraíbles</span><span class="sxs-lookup"><span data-stu-id="d2eaf-176">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="d2eaf-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="d2eaf-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="d2eaf-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="d2eaf-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-181">Admite medios Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="d2eaf-181">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="d2eaf-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d2eaf-183">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-183">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-184">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-186">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-187">Matriz de explicaciones más detalladas para cualquiera de las características de dispositivos de acceso indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="d2eaf-187">Array of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="d2eaf-188">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-188">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="d2eaf-189">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-189">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-190">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-193">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-194">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-194">Short description of the object a one-line string.</span></span>

<span data-ttu-id="d2eaf-195">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-196">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-196">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-199">Algoritmo o herramienta que usa el dispositivo para admitir la compresión.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-199">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="d2eaf-200">Si no es posible o no desea describir el esquema de compresión (quizás porque no se conoce), use las siguientes palabras: "Unknown" para indicar que no se sabe si el dispositivo admite capacidades de compresión; "Compressed" para representar que el dispositivo admite capacidades de compresión, pero su esquema de compresión no se conoce o no se revela; y "no comprimido" para representar que el dispositivo no admite capacidades de compresión.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-200">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="d2eaf-201">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-201">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="d2eaf-202">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-202">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-203">El esquema de compresión es desconocido o no se ha descrito.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-203">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="d2eaf-204">("Comprimido")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-204">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-205">El archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito</span><span class="sxs-lookup"><span data-stu-id="d2eaf-205">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="d2eaf-206">("No comprimido")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-206">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-207">Si el archivo lógico no está comprimido</span><span class="sxs-lookup"><span data-stu-id="d2eaf-207">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d2eaf-208">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-208">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-209">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-211">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-211">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-212">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-212">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="d2eaf-213">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-213">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d2eaf-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-214"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d2eaf-215"> (0)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-215">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-216">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-216">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d2eaf-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-217"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d2eaf-218">(1)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-218">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-219">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-219">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d2eaf-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-220"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d2eaf-221">(2)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-221">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d2eaf-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-222"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d2eaf-223">(3)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-223">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-224">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-224">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d2eaf-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-225"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d2eaf-226">(4)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-226">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-227">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-227">Device is not working properly.</span></span> <span data-ttu-id="d2eaf-228">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-228">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d2eaf-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-229"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d2eaf-230">(5)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-230">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-231">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-231">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d2eaf-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-232"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d2eaf-233"> (6)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-233">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-234">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-234">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d2eaf-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-235"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d2eaf-236">(7)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-236">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d2eaf-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-237"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d2eaf-238">(8)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-238">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-239">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-239">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d2eaf-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-240"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d2eaf-241">(9)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-241">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-242">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-242">Device is not working properly.</span></span> <span data-ttu-id="d2eaf-243">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-243">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d2eaf-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-244"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d2eaf-245">(10)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-245">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-246">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-246">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d2eaf-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-247"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d2eaf-248">(11)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-248">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-249">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-249">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d2eaf-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-250"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d2eaf-251">(12)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-251">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-252">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-252">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d2eaf-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-253"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d2eaf-254">(13)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-254">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-255">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-255">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d2eaf-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-256"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d2eaf-257">(14)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-257">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-258">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-258">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d2eaf-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-259"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d2eaf-260">(15)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-260">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-261">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-261">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d2eaf-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-262"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d2eaf-263">(16)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-263">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-264">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-264">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d2eaf-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-265"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d2eaf-266">(17)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-266">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-267">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-267">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d2eaf-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d2eaf-269">(18)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-269">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-270">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-270">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d2eaf-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-271"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d2eaf-272">(19)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-272">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d2eaf-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-273"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d2eaf-274">(20)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-274">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-275">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-275">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d2eaf-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-276"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d2eaf-277">(21)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-277">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-278">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-278">System failure.</span></span> <span data-ttu-id="d2eaf-279">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-279">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d2eaf-280">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-280">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d2eaf-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-281"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d2eaf-282">(22)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-282">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-283">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-283">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d2eaf-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-284"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d2eaf-285">(23)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-285">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-286">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-286">System failure.</span></span> <span data-ttu-id="d2eaf-287">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-287">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d2eaf-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-288"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d2eaf-289">(24)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-289">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-290">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-290">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d2eaf-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-291"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d2eaf-292">(25)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-292">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-293">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-293">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d2eaf-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d2eaf-295">(26)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-295">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-296">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d2eaf-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-297"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d2eaf-298">(27)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-298">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-299">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-299">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d2eaf-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-300"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d2eaf-301">(28)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-301">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-302">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-302">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d2eaf-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-303"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d2eaf-304">(29)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-304">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-305">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-305">Device is disabled.</span></span> <span data-ttu-id="d2eaf-306">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-306">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d2eaf-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-307"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d2eaf-308">(30)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-308">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-309">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-309">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d2eaf-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-310"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d2eaf-311">31</span><span class="sxs-lookup"><span data-stu-id="d2eaf-311">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-312">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-312">Device is not working properly.</span></span> <span data-ttu-id="d2eaf-313">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-313">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d2eaf-314">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-314">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-315">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-317">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-317">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-318">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-318">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d2eaf-319">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-320">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-320">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-323">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-324">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-324">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d2eaf-325">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-325">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d2eaf-326">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-327">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-327">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-328">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-330">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-330">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-331">Tamaño de bloque predeterminado, en bytes, para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-331">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="d2eaf-332">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-332">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="d2eaf-333">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-333">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-334">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-335">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-337">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-337">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-338">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-338">Description of the object.</span></span>

<span data-ttu-id="d2eaf-339">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-340">**ID**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-340">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-341">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-343">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetLogicalDriveStrings")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-343">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetLogicalDriveStrings")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-344">Identificador único de una unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-344">Unique identifier for a CD-ROM drive.</span></span>

<span data-ttu-id="d2eaf-345">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-346">**Unidad**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-346">**Drive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-349">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-350">Letra de unidad de la unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-350">Drive letter of the CD-ROM drive.</span></span>

<span data-ttu-id="d2eaf-351">Ejemplo: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="d2eaf-351">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-352">**DriveIntegrity**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-352">**DriveIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-353">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-353">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-355">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-355">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-356">Si **es true**, los archivos se pueden leer con precisión desde el dispositivo de CD.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-356">If **True**, files can be accurately read from the CD device.</span></span> <span data-ttu-id="d2eaf-357">Esto se logra mediante la lectura de un bloque de datos dos veces y la comparación de los datos con él mismo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-357">This is achieved by reading a block of data twice and comparing the data against itself.</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-358">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-358">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-359">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-361">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-361">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d2eaf-362">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-363">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-363">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-364">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-366">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-366">More information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="d2eaf-367">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-368">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-368">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-369">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-371">Tipo de detección y corrección de errores admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-371">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="d2eaf-372">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-372">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-373">**FileSystemFlags**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-373">**FileSystemFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-374">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-376">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funciones del sistema de archivos inesperados win32api \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-376">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-377">Esta propiedad ha quedado obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-377">This property is obsolete.</span></span> <span data-ttu-id="d2eaf-378">En lugar de esta propiedad, use **FileSystemFlagsEx**.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-378">In place of this property, use **FileSystemFlagsEx**.</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-379">**FileSystemFlagsEx**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-379">**FileSystemFlagsEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-380">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-382">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-382">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-383">Marcas del sistema de archivos asociadas a la unidad de CD-ROM de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-383">File system flags associated with the Windows CD-ROM drive.</span></span> <span data-ttu-id="d2eaf-384">Este parámetro puede ser cualquier combinación de marcas, pero **la \_ \_ compresión de archivos de FS** y el vol de FS están **\_ \_ \_ comprimidos** y son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-384">This parameter can be any combination of flags, but **FS\_FILE\_COMPRESSION** and **FS\_VOL\_IS\_COMPRESSED** are mutually exclusive.</span></span>

<dt>

<span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>

<span data-ttu-id="d2eaf-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Búsqueda con distinción de mayúsculas y** minúsculas (1)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-385"><span id="Case_Sensitive_Search"></span><span id="case_sensitive_search"></span><span id="CASE_SENSITIVE_SEARCH"></span>**Case Sensitive Search** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-386">El sistema de archivos admite nombres de archivo que distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-386">The file system supports case-sensitive file names.</span></span>

</dd> <dt>

<span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>

<span data-ttu-id="d2eaf-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Nombres conservados de mayúsculas y minúsculas** (2)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-387"><span id="Case_Preserved_Names"></span><span id="case_preserved_names"></span><span id="CASE_PRESERVED_NAMES"></span>**Case Preserved Names** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-388">El sistema de archivos conserva el caso de los nombres de archivo cuando coloca un nombre en un disco.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-388">The file system preserves the case of file names when it places a name on a disk.</span></span>

</dd> <dt>

<span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>

<span data-ttu-id="d2eaf-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode en disco** (4)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-389"><span id="Unicode_On_Disk"></span><span id="unicode_on_disk"></span><span id="UNICODE_ON_DISK"></span>**Unicode On Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-390">El sistema de archivos admite Unicode en nombres de archivo tal y como aparecen en el disco.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-390">The file system supports Unicode in file names as they appear on the disk.</span></span>

</dd> <dt>

<span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>

<span data-ttu-id="d2eaf-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**ACL persistentes** (8)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-391"><span id="Persistent_ACLs"></span><span id="persistent_acls"></span><span id="PERSISTENT_ACLS"></span>**Persistent ACLs** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-392">El sistema de archivos conserva y aplica las listas de control de acceso (ACL).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-392">The file system preserves and enforces access control lists (ACLs).</span></span> <span data-ttu-id="d2eaf-393">Por ejemplo, el sistema de archivos NTFS conserva y aplica las ACL y el sistema de archivos FAT no.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-393">For example, the NTFS file system preserves and enforces ACLs and the FAT file system does not.</span></span>

</dd> <dt>

<span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>

<span data-ttu-id="d2eaf-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**Compresión de archivos** (16)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-394"><span id="File_Compression"></span><span id="file_compression"></span><span id="FILE_COMPRESSION"></span>**File Compression** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-395">El sistema de archivos admite la compresión basada en archivos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-395">The file system supports file-based compression.</span></span>

</dd> <dt>

<span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>

<span data-ttu-id="d2eaf-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Cuotas de volumen** (32)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-396"><span id="Volume_Quotas"></span><span id="volume_quotas"></span><span id="VOLUME_QUOTAS"></span>**Volume Quotas** (32)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-397">El sistema de archivos admite cuotas de disco.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-397">The file system supports disk quotas.</span></span>

</dd> <dt>

<span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>

<span data-ttu-id="d2eaf-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Admite archivos dispersos** (64)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-398"><span id="Supports_Sparse_Files"></span><span id="supports_sparse_files"></span><span id="SUPPORTS_SPARSE_FILES"></span>**Supports Sparse Files** (64)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-399">El sistema de archivos admite archivos de reserva.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-399">The file system supports spare files.</span></span>

</dd> <dt>

<span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>

<span data-ttu-id="d2eaf-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Admite puntos de reanálisis** (128)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-400"><span id="Supports_Reparse_Points"></span><span id="supports_reparse_points"></span><span id="SUPPORTS_REPARSE_POINTS"></span>**Supports Reparse Points** (128)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-401">El sistema de archivos admite puntos de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-401">The file system supports reparse points.</span></span>

</dd> <dt>

<span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>

<span data-ttu-id="d2eaf-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Admite el almacenamiento remoto** (256)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-402"><span id="Supports_Remote_Storage"></span><span id="supports_remote_storage"></span><span id="SUPPORTS_REMOTE_STORAGE"></span>**Supports Remote Storage** (256)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-403">El sistema de archivos admite el almacenamiento remoto de archivos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-403">The file system supports the remote storage of files.</span></span>

</dd> <dt>

<span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>

<span data-ttu-id="d2eaf-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Admite nombres largos** (16384)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-404"><span id="Supports_Long_Names"></span><span id="supports_long_names"></span><span id="SUPPORTS_LONG_NAMES"></span>**Supports Long Names** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-405">El sistema de archivos admite nombres de archivo de más de ocho caracteres.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-405">The file system supports file names that are longer than eight characters.</span></span>

</dd> <dt>

<span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>

<span data-ttu-id="d2eaf-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>El **volumen está comprimido** (32768)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-406"><span id="Volume_Is_Compressed"></span><span id="volume_is_compressed"></span><span id="VOLUME_IS_COMPRESSED"></span>**Volume Is Compressed** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-407">El volumen de disco especificado es un volumen comprimido, por ejemplo, un volumen de DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-407">The specified disk volume is a compressed volume, for example, a DoubleSpace volume.</span></span>

</dd> <dt>

<span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>

<span data-ttu-id="d2eaf-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Volumen de solo lectura** (524289)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-408"><span id="Read_Only_Volume"></span><span id="read_only_volume"></span><span id="READ_ONLY_VOLUME"></span>**Read Only Volume** (524289)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-409">El volumen especificado es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-409">The specified volume is read-only.</span></span>

</dd> <dt>

<span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>

<span data-ttu-id="d2eaf-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Admite identificadores de objeto** (65536)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-410"><span id="Supports_Object_IDS"></span><span id="supports_object_ids"></span><span id="SUPPORTS_OBJECT_IDS"></span>**Supports Object IDS** (65536)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-411">El sistema de archivos admite identificadores de objetos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-411">The file system supports object identifiers.</span></span>

</dd> <dt>

<span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>

<span data-ttu-id="d2eaf-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Admite el cifrado** (131072)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-412"><span id="Supports_Encryption"></span><span id="supports_encryption"></span><span id="SUPPORTS_ENCRYPTION"></span>**Supports Encryption** (131072)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-413">El sistema de archivos es compatible con el sistema de archivos cifrados (EFS).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-413">The file system supports the Encrypted File System (EFS).</span></span>

</dd> <dt>

<span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>

<span data-ttu-id="d2eaf-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Admite secuencias con nombre** (262144)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-414"><span id="Supports_Named_Streams"></span><span id="supports_named_streams"></span><span id="SUPPORTS_NAMED_STREAMS"></span>**Supports Named Streams** (262144)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-415">El sistema de archivos admite secuencias con nombre.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-415">The file system supports named streams.</span></span>

</dd> </dl>

<span data-ttu-id="d2eaf-416">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="d2eaf-416">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-417">**Id**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-417">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-418">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-420">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-421">Letra de unidad que identifica de forma única esta unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-421">Drive letter that uniquely identifies this CD-ROM drive.</span></span>

<span data-ttu-id="d2eaf-422">Ejemplo: "d: \\ "</span><span class="sxs-lookup"><span data-stu-id="d2eaf-422">Example: "d:\\"</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-423">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-423">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-424">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-424">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-426">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-427">Fecha y hora de instalación del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-427">Date and time the object is installed.</span></span> <span data-ttu-id="d2eaf-428">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-428">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d2eaf-429">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-429">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-430">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-430">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-431">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-433">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-433">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d2eaf-434">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-434">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-435">**Le**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-435">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-438">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-439">Fabricante de la unidad de CD-ROM de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-439">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="d2eaf-440">Ejemplo: "PLEXtor"</span><span class="sxs-lookup"><span data-stu-id="d2eaf-440">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-441">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-441">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-442">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-444">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-444">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-445">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-445">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="d2eaf-446">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-446">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="d2eaf-447">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-448">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-448">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-449">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-451">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-451">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-452">Longitud máxima de un componente de nombre de archivo compatible con la unidad de CD-ROM de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-452">Maximum length of a filename component supported by the Windows CD-ROM drive.</span></span> <span data-ttu-id="d2eaf-453">Componente de nombre de archivo la parte de un nombre de archivo entre barras diagonales inversas.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-453">A file name component the portion of a file name between backslashes.</span></span> <span data-ttu-id="d2eaf-454">El valor se puede usar para indicar que el sistema de archivos especificado admite nombres largos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-454">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="d2eaf-455">Por ejemplo, para un sistema de archivos FAT que admite nombres largos, la función almacena el valor 255, en lugar del indicador 8,3 anterior.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-455">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="d2eaf-456">También se pueden admitir nombres largos en los sistemas que usan el sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-456">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="d2eaf-457">Ejemplo: 255</span><span class="sxs-lookup"><span data-stu-id="d2eaf-457">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-458">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-458">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-459">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-459">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-461">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-461">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-462">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-462">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="d2eaf-463">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="d2eaf-464">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-464">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-465">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-465">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-466">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-466">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-467">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-468">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-468">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-469">Si es **true**, hay un CD-ROM en la unidad.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-469">If **True**, a CD-ROM is in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-470">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-470">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-471">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-473">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-474">Tipo de medio que este dispositivo puede usar o al que puede acceder.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-474">Type of media that can be used or accessed by this device.</span></span> <span data-ttu-id="d2eaf-475">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="d2eaf-475">Possible values are:</span></span>

<dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="d2eaf-476">**Acceso aleatorio** ("acceso aleatorio")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-476">**Random Access** ("Random Access")</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="d2eaf-477">**Admite escritura** ("admite escritura")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-477">**Supports Writing** ("Supports Writing")</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="d2eaf-478">**Medios extraíbles** ("medios extraíbles")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-478">**Removable Media** ("Removable Media")</span></span>


</dt> <dd></dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="d2eaf-479">**CD-ROM** ("CD-ROM")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-479">**CD-ROM** ("CD-ROM")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d2eaf-480">**MfrAssignedRevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-480">**MfrAssignedRevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-483">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK \| KernelModeDrivers \| [**\_ \_ descriptor de dispositivo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor) \| ProductRevisionOffset")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-483">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win2000DDK\|KernelModeDrivers\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-484">Nivel de revisión de firmware asignado por el fabricante.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-484">Firmware revision level that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-485">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-485">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-486">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-488">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-488">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-489">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-489">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="d2eaf-490">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-490">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="d2eaf-491">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-491">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-492">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-492">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-493">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-494">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-495">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-495">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-496">Etiqueta del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-496">Label for the object.</span></span> <span data-ttu-id="d2eaf-497">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-497">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d2eaf-498">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-498">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-499">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-499">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-500">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-500">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-501">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-502">Si **es true**, el dispositivo de acceso a medios necesita limpieza.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-502">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="d2eaf-503">Si la limpieza manual o automática es posible, se indica en la propiedad **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="d2eaf-503">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="d2eaf-504">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-504">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-505">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-505">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-506">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-508">Número máximo de medios que se pueden admitir o insertar cuando el dispositivo de acceso a medios admite varios medios individuales.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-508">Maximum number of media that can be supported or inserted, when the media access device supports multiple individual media.</span></span>

<span data-ttu-id="d2eaf-509">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-509">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-510">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-510">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-511">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-512">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-513">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-513">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-514">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-514">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d2eaf-515">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-515">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d2eaf-516">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d2eaf-516">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-517">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-517">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-518">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-518">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-520">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-520">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d2eaf-521">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-521">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d2eaf-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-522"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d2eaf-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-523"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-524">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-524">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d2eaf-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-525"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d2eaf-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-526"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-527">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-527">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d2eaf-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-528"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-529">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-529">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d2eaf-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-530"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-531">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d2eaf-531">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d2eaf-532">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-532">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d2eaf-533">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-533">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d2eaf-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-534"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-535">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-535">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d2eaf-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-536"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d2eaf-537">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="d2eaf-537">Timed Power-On Supported</span></span>

<span data-ttu-id="d2eaf-538">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-538">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d2eaf-539">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-539">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-540">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-540">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-541">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-541">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-542">Si **es true**, el dispositivo puede administrarse mediante energía, lo que significa que se puede poner en modo de suspensión, etc.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-542">If **True**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="d2eaf-543">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-543">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d2eaf-544">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-544">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-545">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-545">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-546">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-547">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-548">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| RevisionLevel")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-548">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|RevisionLevel")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-549">Nivel de revisión de firmware de la unidad de CD-ROM de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-549">Firmware revision level of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-550">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-550">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-551">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-551">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-552">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-553">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| SCSI Structures SCSI \| [**\_ request \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| PathId")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-554">Número de bus SCSI de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-554">SCSI bus number for the disk drive.</span></span>

<span data-ttu-id="d2eaf-555">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="d2eaf-555">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-556">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-556">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-557">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-557">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-558">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-559">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| LUN de \| [**bloque de \_ solicitud \_ SCSI**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)de estructuras SCSI de inesperados win32api \| ")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-559">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-560">Número de unidad lógica (LUN) SCSI de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-560">SCSI logical unit number (LUN) of the disk drive.</span></span> <span data-ttu-id="d2eaf-561">El LUN se usa para designar a qué controladora SCSI se tiene acceso en un sistema con más de un controlador que se está usando.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-561">The LUN is used to designate which SCSI controller is being accessed in a system with more than one controller being used.</span></span> <span data-ttu-id="d2eaf-562">El identificador de dispositivo SCSI es similar, pero es la designación de varios dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-562">The SCSI device identifier is similar, but is the designation for multiple devices on one controller.</span></span>

<span data-ttu-id="d2eaf-563">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="d2eaf-563">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-564">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-564">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-565">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-565">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-566">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-567">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| SCSI Structures SCSI \| [**\_ request \_ Block**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block) \| ScsiStatus")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SCSI Structures\|[**SCSI\_REQUEST\_BLOCK**](/windows-hardware/drivers/ddi/content/srb/ns-srb-_scsi_request_block)\|ScsiStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-568">Número de puerto SCSI de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-568">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="d2eaf-569">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="d2eaf-569">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-570">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-570">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-571">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-571">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-572">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-573">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| DeviceIoControl \| ioctl \_ SCSI \_ Get \_ Address")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|DeviceIoControl\|IOCTL\_SCSI\_GET\_ADDRESS")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-574">Número de identificación SCSI de la unidad de CD-ROM de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-574">SCSI identifier number of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="d2eaf-575">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="d2eaf-575">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-576">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-576">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-577">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-578">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-579">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| [**\_ \_ descriptor de dispositivo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)de inesperados win32api de entrada y salida de dispositivo \| SerialNumberOffset")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-579">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-580">Número proporcionado por el fabricante que identifica el medio físico.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-580">Number supplied by the manufacturer that identifies the physical media.</span></span> <span data-ttu-id="d2eaf-581">Ejemplo: WD-WM3493798728.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-581">Example: WD-WM3493798728.</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-582">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-582">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-583">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-583">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-584">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-584">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-585">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| GetDiskFreeSpace"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-585">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDiskFreeSpace"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-586">Tamaño de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-586">Size of the disk drive.</span></span>

<span data-ttu-id="d2eaf-587">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-587">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-588">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-588">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-589">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-590">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-591">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-591">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-592">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-592">Current status of the object.</span></span> <span data-ttu-id="d2eaf-593">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-593">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d2eaf-594">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-594">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d2eaf-595">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d2eaf-595">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d2eaf-596">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-596">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d2eaf-597">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-597">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d2eaf-598">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-598">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d2eaf-599">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d2eaf-599">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d2eaf-600">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-600">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d2eaf-601">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-601">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d2eaf-602">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-602">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d2eaf-603">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-603">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d2eaf-604">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-604">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d2eaf-605">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-605">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d2eaf-606">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-606">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d2eaf-607">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-607">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d2eaf-608">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-608">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d2eaf-609">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-609">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d2eaf-610">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-610">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d2eaf-611">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-611">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d2eaf-612">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-612">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-613">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-614">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-615">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-615">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-616">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-616">State of the logical device.</span></span> <span data-ttu-id="d2eaf-617">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-617">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d2eaf-618">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-618">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d2eaf-619">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-619">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d2eaf-620">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-620">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d2eaf-621">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-621">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d2eaf-622">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-622">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d2eaf-623">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-623">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d2eaf-624">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-624">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-625">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-626">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-626">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-627">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-627">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-628">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-628">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d2eaf-629">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-629">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-630">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-630">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-631">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-632">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-632">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-633">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d2eaf-633">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-634">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-634">Name of the scoping system.</span></span>

<span data-ttu-id="d2eaf-635">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-635">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-636">**TransferRate**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-636">**TransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-637">Tipo de datos: **real64**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-637">Data type: **real64**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-638">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-638">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-639">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("referencia \| de archivo y referencia de tiempo"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes por segundo")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-639">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Reference and Time Reference"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes per second")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-640">Velocidad de transferencia de la unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-640">Transfer rate of the CD-ROM drive.</span></span> <span data-ttu-id="d2eaf-641">Un valor de-1 indica que no se puede determinar la tasa.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-641">A value of -1 indicates that the rate cannot be determined.</span></span> <span data-ttu-id="d2eaf-642">Cuando esto sucede, el CD no está en la unidad.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-642">When this happens, the CD is not in the drive.</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-643">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-643">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-644">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-644">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-645">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-646">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-647">Nombre del volumen de la unidad de CD-ROM de Windows.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-647">Volume name of the Windows CD-ROM drive.</span></span>

</dd> <dt>

<span data-ttu-id="d2eaf-648">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-648">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2eaf-649">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-650">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2eaf-650">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2eaf-651">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span><span class="sxs-lookup"><span data-stu-id="d2eaf-651">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)")</span></span>
</dt> </dl>

<span data-ttu-id="d2eaf-652">Número de serie del volumen del medio en la unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-652">Volume serial number of the media in the CD-ROM drive.</span></span>

<span data-ttu-id="d2eaf-653">Ejemplo: A8C3-D032</span><span class="sxs-lookup"><span data-stu-id="d2eaf-653">Example: A8C3-D032</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2eaf-654">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2eaf-654">Remarks</span></span>

<span data-ttu-id="d2eaf-655">La **clase \_ CDROMDrive de Win32** se deriva [**de \_ CDROMDrive de CIM**](cim-cdromdrive.md) que deriva [**de \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-655">The **Win32\_CDROMDrive** class is derived from [**CIM\_CDROMDrive**](cim-cdromdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="d2eaf-656">La **clase \_ MediaAccessDevice de CIM** deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d2eaf-656">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d2eaf-657">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2eaf-657">Examples</span></span>

<span data-ttu-id="d2eaf-658">El siguiente ejemplo de VBScript determina si un CD se encuentra en una unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="d2eaf-658">The following VBScript example determines if a CD is in a CDROM drive.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject(_
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery( _
    "Select * from Win32_CDROMDrive")
For Each objItem in colItems
    Wscript.Echo "Device ID: " _
        & objItem.DeviceID
    Wscript.Echo "Media Loaded: " _
        & objItem.MediaLoaded
Next
```



## <a name="requirements"></a><span data-ttu-id="d2eaf-659">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2eaf-659">Requirements</span></span>



| <span data-ttu-id="d2eaf-660">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2eaf-660">Requirement</span></span> | <span data-ttu-id="d2eaf-661">Value</span><span class="sxs-lookup"><span data-stu-id="d2eaf-661">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2eaf-662">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2eaf-662">Minimum supported client</span></span><br/> | <span data-ttu-id="d2eaf-663">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2eaf-663">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2eaf-664">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2eaf-664">Minimum supported server</span></span><br/> | <span data-ttu-id="d2eaf-665">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2eaf-665">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2eaf-666">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2eaf-666">Namespace</span></span><br/>                | <span data-ttu-id="d2eaf-667">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d2eaf-667">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2eaf-668">MOF</span><span class="sxs-lookup"><span data-stu-id="d2eaf-668">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2eaf-669"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2eaf-669"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2eaf-670">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2eaf-670">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2eaf-671"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2eaf-671"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2eaf-672">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2eaf-672">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2eaf-673">**\_CDROMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="d2eaf-673">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dt>

[<span data-ttu-id="d2eaf-674">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d2eaf-674">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d2eaf-675">Tareas WMI: hardware del equipo</span><span class="sxs-lookup"><span data-stu-id="d2eaf-675">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="d2eaf-676">Tareas de WMI: discos y sistemas de archivos</span><span class="sxs-lookup"><span data-stu-id="d2eaf-676">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

