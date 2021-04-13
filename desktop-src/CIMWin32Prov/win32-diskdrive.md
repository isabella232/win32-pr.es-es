---
description: Representa una unidad de disco física tal como la muestra un equipo que ejecuta el sistema operativo Windows.
ms.assetid: c1fc6a1e-e725-484b-aacf-279f777e9b19
ms.tgt_platform: multiple
title: Clase Win32_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDrive
- Win32_DiskDrive.Reset
- Win32_DiskDrive.SetPowerState
- Win32_DiskDrive.Availability
- Win32_DiskDrive.BytesPerSector
- Win32_DiskDrive.Capabilities
- Win32_DiskDrive.CapabilityDescriptions
- Win32_DiskDrive.Caption
- Win32_DiskDrive.CompressionMethod
- Win32_DiskDrive.ConfigManagerErrorCode
- Win32_DiskDrive.ConfigManagerUserConfig
- Win32_DiskDrive.CreationClassName
- Win32_DiskDrive.DefaultBlockSize
- Win32_DiskDrive.Description
- Win32_DiskDrive.DeviceID
- Win32_DiskDrive.ErrorCleared
- Win32_DiskDrive.ErrorDescription
- Win32_DiskDrive.ErrorMethodology
- Win32_DiskDrive.FirmwareRevision
- Win32_DiskDrive.Index
- Win32_DiskDrive.InstallDate
- Win32_DiskDrive.InterfaceType
- Win32_DiskDrive.LastErrorCode
- Win32_DiskDrive.Manufacturer
- Win32_DiskDrive.MaxBlockSize
- Win32_DiskDrive.MaxMediaSize
- Win32_DiskDrive.MediaLoaded
- Win32_DiskDrive.MediaType
- Win32_DiskDrive.MinBlockSize
- Win32_DiskDrive.Model
- Win32_DiskDrive.Name
- Win32_DiskDrive.NeedsCleaning
- Win32_DiskDrive.NumberOfMediaSupported
- Win32_DiskDrive.Partitions
- Win32_DiskDrive.PNPDeviceID
- Win32_DiskDrive.PowerManagementCapabilities
- Win32_DiskDrive.PowerManagementSupported
- Win32_DiskDrive.SCSIBus
- Win32_DiskDrive.SCSILogicalUnit
- Win32_DiskDrive.SCSIPort
- Win32_DiskDrive.SCSITargetId
- Win32_DiskDrive.SectorsPerTrack
- Win32_DiskDrive.SerialNumber
- Win32_DiskDrive.Signature
- Win32_DiskDrive.Size
- Win32_DiskDrive.Status
- Win32_DiskDrive.StatusInfo
- Win32_DiskDrive.SystemCreationClassName
- Win32_DiskDrive.SystemName
- Win32_DiskDrive.TotalCylinders
- Win32_DiskDrive.TotalHeads
- Win32_DiskDrive.TotalSectors
- Win32_DiskDrive.TotalTracks
- Win32_DiskDrive.TracksPerCylinder
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 751dee053574be417cb312f6b046ae6b7703d543
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539141"
---
# <a name="win32_diskdrive-class"></a><span data-ttu-id="aa7c4-103">\_Clase Win32 DiskDrive</span><span class="sxs-lookup"><span data-stu-id="aa7c4-103">Win32\_DiskDrive class</span></span>

<span data-ttu-id="aa7c4-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskDrive de Win32** representa una unidad de disco física tal como la muestra un equipo que ejecuta el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-104">The **Win32\_DiskDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical disk drive as seen by a computer running the Windows operating system.</span></span>

<span data-ttu-id="aa7c4-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="aa7c4-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa7c4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa7c4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDrive : CIM_DiskDrive
{
  uint16   Availability;
  uint32   BytesPerSector;
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
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FirmwareRevision;
  uint32   Index;
  datetime InstallDate;
  string   InterfaceType;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  boolean  MediaLoaded;
  string   MediaType;
  uint64   MinBlockSize;
  string   Model;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Partitions;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   SCSIBus;
  uint16   SCSILogicalUnit;
  uint16   SCSIPort;
  uint16   SCSITargetId;
  uint32   SectorsPerTrack;
  string   SerialNumber;
  uint32   Signature;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   TotalCylinders;
  uint32   TotalHeads;
  uint64   TotalSectors;
  uint64   TotalTracks;
  uint32   TracksPerCylinder;
};
```

## <a name="members"></a><span data-ttu-id="aa7c4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa7c4-108">Members</span></span>

<span data-ttu-id="aa7c4-109">La **clase \_ DiskDrive de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aa7c4-109">The **Win32\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="aa7c4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa7c4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="aa7c4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa7c4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aa7c4-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa7c4-112">Methods</span></span>

<span data-ttu-id="aa7c4-113">La clase **Win32 \_ DiskDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-113">The **Win32\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="aa7c4-114">Método</span><span class="sxs-lookup"><span data-stu-id="aa7c4-114">Method</span></span>            | <span data-ttu-id="aa7c4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa7c4-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7c4-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-116">**Reset**</span></span>         | <span data-ttu-id="aa7c4-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-117">Not implemented.</span></span> <span data-ttu-id="aa7c4-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ DiskDrive**](cim-diskdrive.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="aa7c4-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-119">**SetPowerState**</span></span> | <span data-ttu-id="aa7c4-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-120">Not implemented.</span></span> <span data-ttu-id="aa7c4-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ DiskDrive**](cim-diskdrive.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DiskDrive**](cim-diskdrive.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="aa7c4-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aa7c4-122">Properties</span></span>

<span data-ttu-id="aa7c4-123">La **clase \_ DiskDrive de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-123">The **Win32\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa7c4-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-127">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-128">Availability and status of the device.</span></span>

<span data-ttu-id="aa7c4-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa7c4-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa7c4-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="aa7c4-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="aa7c4-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="aa7c4-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="aa7c4-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aa7c4-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="aa7c4-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="aa7c4-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="aa7c4-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="aa7c4-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="aa7c4-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aa7c4-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="aa7c4-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="aa7c4-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="aa7c4-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="aa7c4-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="aa7c4-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="aa7c4-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="aa7c4-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="aa7c4-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="aa7c4-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-153"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="aa7c4-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-154"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="aa7c4-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-155"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-156">La unidad de disco no está disponible.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-156">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa7c4-157">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-157">**BytesPerSector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-158">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-160">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de \| [**\_ disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| BytesPerSector"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|BytesPerSector"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-161">Número de bytes de cada sector para la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-161">Number of bytes in each sector for the physical disk drive.</span></span>

<span data-ttu-id="aa7c4-162">Ejemplo: 512</span><span class="sxs-lookup"><span data-stu-id="aa7c4-162">Example: 512</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-164">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-166">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-166">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-167">Matriz de funcionalidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-167">Array of capabilities of the media access device.</span></span> <span data-ttu-id="aa7c4-168">Por ejemplo, el dispositivo puede admitir el acceso aleatorio (3), el medio extraíble (7) y la limpieza automática (9).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-168">For example, the device may support random access (3), removable media (7), and automatic cleaning (9).</span></span>

<span data-ttu-id="aa7c4-169">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa7c4-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa7c4-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="aa7c4-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="aa7c4-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="aa7c4-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="aa7c4-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="aa7c4-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="aa7c4-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-178">Admite medios extraíbles</span><span class="sxs-lookup"><span data-stu-id="aa7c4-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="aa7c4-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="aa7c4-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="aa7c4-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="aa7c4-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-183">Admite medios Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="aa7c4-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="aa7c4-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-185">Expulsión antes de desmontar la unidad no necesaria</span><span class="sxs-lookup"><span data-stu-id="aa7c4-185">Ejection Prior to Drive Dismount Not Required</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa7c4-186">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-186">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-187">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-189">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-189">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-190">Lista de explicaciones más detalladas para cualquiera de las características de dispositivos de acceso indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="aa7c4-190">List of more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="aa7c4-191">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-191">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="aa7c4-192">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-192">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-193">**Caption**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-196">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-197">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-197">Short description of the object.</span></span>

<span data-ttu-id="aa7c4-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-199">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-199">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-202">Algoritmo o herramienta que usa el dispositivo para admitir la compresión.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-202">Algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="aa7c4-203">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-203">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="aa7c4-204">Nombre del algoritmo de compresión o de uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-204">The name of the compression algorithm or one of the following values.</span></span>

<dt>



 <span data-ttu-id="aa7c4-205">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-206">Si el dispositivo admite capacidades de compresión o no, no se conoce.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-206">Whether the device supports compression capabilities or not is not known.</span></span>

</dd> <dt>



 <span data-ttu-id="aa7c4-207">("Comprimido")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-208">El dispositivo admite capacidades de compresión, pero su esquema de compresión no se conoce o no se revela.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-208">The device supports compression capabilities but its compression scheme is not known or not disclosed.</span></span>

</dd> <dt>



 <span data-ttu-id="aa7c4-209">("No comprimido")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-210">El dispositivo no admite la compresión.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-210">The device does not support compression.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa7c4-211">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-212">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-214">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-215">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="aa7c4-216">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="aa7c4-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="aa7c4-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-219">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="aa7c4-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="aa7c4-221">(1)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-222">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa7c4-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="aa7c4-224">(2)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="aa7c4-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="aa7c4-226">(3)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-227">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aa7c4-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="aa7c4-229">(4)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-230">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-230">Device is not working properly.</span></span> <span data-ttu-id="aa7c4-231">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="aa7c4-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="aa7c4-233">(5)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-234">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="aa7c4-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="aa7c4-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-237">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="aa7c4-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="aa7c4-239">(7)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="aa7c4-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="aa7c4-241">(8)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-242">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="aa7c4-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="aa7c4-244">(9)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-245">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-245">Device is not working properly.</span></span> <span data-ttu-id="aa7c4-246">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="aa7c4-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="aa7c4-248">(10)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-249">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="aa7c4-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="aa7c4-251">(11)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-252">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="aa7c4-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="aa7c4-254">(12)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-255">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="aa7c4-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="aa7c4-257">(13)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-258">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="aa7c4-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="aa7c4-260">(14)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-261">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="aa7c4-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="aa7c4-263">(15)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-264">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="aa7c4-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="aa7c4-266">(16)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-267">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="aa7c4-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="aa7c4-269">(17)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-270">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa7c4-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="aa7c4-272">(18)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-273">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="aa7c4-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="aa7c4-275">(19)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aa7c4-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="aa7c4-277">(20)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-278">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="aa7c4-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="aa7c4-280">(21)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-281">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-281">System failure.</span></span> <span data-ttu-id="aa7c4-282">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="aa7c4-283">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="aa7c4-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="aa7c4-285">(22)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-286">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="aa7c4-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="aa7c4-288">(23)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-289">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-289">System failure.</span></span> <span data-ttu-id="aa7c4-290">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="aa7c4-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="aa7c4-292">(24)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-293">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aa7c4-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aa7c4-295">(25)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-296">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aa7c4-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aa7c4-298">(26)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-299">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="aa7c4-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="aa7c4-301">(27)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-302">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="aa7c4-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="aa7c4-304">(28)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-305">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="aa7c4-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="aa7c4-307">(29)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-308">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-308">Device is disabled.</span></span> <span data-ttu-id="aa7c4-309">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="aa7c4-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="aa7c4-311">(30)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-312">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa7c4-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="aa7c4-314">31</span><span class="sxs-lookup"><span data-stu-id="aa7c4-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-315">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-315">Device is not working properly.</span></span> <span data-ttu-id="aa7c4-316">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa7c4-317">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-318">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-320">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-321">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-321">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="aa7c4-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-326">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-327">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-327">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="aa7c4-328">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-328">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="aa7c4-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-330">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-331">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-333">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-334">Tamaño de bloque predeterminado, en bytes, para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-334">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="aa7c4-335">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="aa7c4-336">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-337">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-340">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-341">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-341">Description of the object.</span></span>

<span data-ttu-id="aa7c4-342">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-343">**ID**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-344">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-346">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-346">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-347">Identificador único de la unidad de disco con otros dispositivos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-347">Unique identifier of the disk drive with other devices on the system.</span></span>

<span data-ttu-id="aa7c4-348">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-349">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-350">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-352">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-352">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="aa7c4-353">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-357">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-357">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="aa7c4-358">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-359">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-362">Tipo de detección y corrección de errores admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-362">Type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="aa7c4-363">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-364">**FirmwareRevision**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-364">**FirmwareRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-365">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-367">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| [**\_ \_ descriptor de dispositivo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)de inesperados win32api de entrada y salida de dispositivo \| ProductRevisionOffset")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|ProductRevisionOffset")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-368">Revisión para el firmware de la unidad de disco que asigna el fabricante.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-368">Revision for the disk drive firmware that is assigned by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-369">**Index**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-369">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-370">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-372">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Windows 95/98 Functions \| \_ \_ info Map info \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows 95/98 Functions\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-373">Número de unidad física de la unidad especificada.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-373">Physical drive number of the given drive.</span></span> <span data-ttu-id="aa7c4-374">Esta propiedad se rellena con la estructura de [**\_ \_ número de dispositivo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) devuelta desde el código de control [**\_ \_ obtener \_ \_ número de dispositivo de almacenamiento de ioctl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .</span><span class="sxs-lookup"><span data-stu-id="aa7c4-374">This property is filled by the [**STORAGE\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_number) structure returned from the [**IOCTL\_STORAGE\_GET\_DEVICE\_NUMBER**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) control code.</span></span> <span data-ttu-id="aa7c4-375">Un valor de 0xFFFFFFFF indica que la unidad especificada no se asigna a una unidad física.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-375">A value of 0xffffffff indicates that the given drive does not map to a physical drive.</span></span>

<span data-ttu-id="aa7c4-376">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="aa7c4-376">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-377">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-377">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-378">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-378">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-379">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-380">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-381">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-381">Date and time the object was installed.</span></span> <span data-ttu-id="aa7c4-382">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-382">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aa7c4-383">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-383">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-384">**InterfaceType**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-384">**InterfaceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-385">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-386">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-387">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Device INPUT and Output Functions \| [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-387">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-388">Tipo de interfaz de la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-388">Interface type of physical disk drive.</span></span>

<span data-ttu-id="aa7c4-389">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="aa7c4-389">The values are:</span></span>

<span data-ttu-id="aa7c4-390">SCSI</span><span class="sxs-lookup"><span data-stu-id="aa7c4-390">SCSI</span></span>

<span data-ttu-id="aa7c4-391">CÁMARAS</span><span class="sxs-lookup"><span data-stu-id="aa7c4-391">HDC</span></span>

<span data-ttu-id="aa7c4-392">IDE</span><span class="sxs-lookup"><span data-stu-id="aa7c4-392">IDE</span></span>

<span data-ttu-id="aa7c4-393">USB</span><span class="sxs-lookup"><span data-stu-id="aa7c4-393">USB</span></span>

<span data-ttu-id="aa7c4-394">1394</span><span class="sxs-lookup"><span data-stu-id="aa7c4-394">1394</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-395">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-395">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-396">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-398">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-398">Last error code reported by the logical device.</span></span>

<span data-ttu-id="aa7c4-399">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-400">**Le**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-400">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-403">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ hardware máquina local \\ \\ \\ \\ DEVICEMAP \\ \\ SCSI SCSI puerto SCSI \\ \\ bus SCSI identificador identificador \\ \\ \\ \\ \\ \\ de unidad lógica \\ \\ ", "Win32Registry \| manufacturer")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-404">Nombre del fabricante de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-404">Name of the disk drive manufacturer.</span></span>

<span data-ttu-id="aa7c4-405">Ejemplo: "Seagate"</span><span class="sxs-lookup"><span data-stu-id="aa7c4-405">Example: "Seagate"</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-406">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-406">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-407">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-407">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-409">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-409">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-410">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-410">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="aa7c4-411">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="aa7c4-412">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-413">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-413">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-414">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-416">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-417">Tamaño máximo del medio, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-417">Maximum media size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="aa7c4-418">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="aa7c4-419">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-420">**MediaLoaded**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-420">**MediaLoaded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-421">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-423">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| mediatype \| FixedMedia")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType\|FixedMedia")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-424">Si es **true**, se cargan los medios de una unidad de disco, lo que significa que el dispositivo tiene un sistema de archivos legible y es accesible.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-424">If **True**, the media for a disk drive is loaded, which means that the device has a readable file system and is accessible.</span></span> <span data-ttu-id="aa7c4-425">En el caso de las unidades de disco fijas, esta propiedad siempre será **true**.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-425">For fixed disk drives, this property will always be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-426">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-426">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-429">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| mediatype")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-429">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|MediaType")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-430">Tipo de medio utilizado o al que este dispositivo tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-430">Type of media used or accessed by this device.</span></span>

<span data-ttu-id="aa7c4-431">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="aa7c4-431">Possible values are:</span></span>

<dt>

<span id="External_hard_disk_media"></span><span id="external_hard_disk_media"></span><span id="EXTERNAL_HARD_DISK_MEDIA"></span>

<span data-ttu-id="aa7c4-432">**Medio de disco duro externo**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-432">**External hard disk media**</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_media"></span><span id="removable_media"></span><span id="REMOVABLE_MEDIA"></span>

<span data-ttu-id="aa7c4-433">**Medios extraíbles** ("medios extraíbles distintos de disquete")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-433">**Removable media** ("Removable media other than floppy")</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk"></span><span id="fixed_hard_disk"></span><span id="FIXED_HARD_DISK"></span>

<span data-ttu-id="aa7c4-434">**Disco duro fijo** ("medio de disco duro fijo")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-434">**Fixed hard disk** ("Fixed hard disk media")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa7c4-435">**Desconocido** ("el formato es desconocido")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-435">**Unknown** ("Format is unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa7c4-436">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-436">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-437">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-438">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-439">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-439">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-440">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-440">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="aa7c4-441">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-441">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="aa7c4-442">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-442">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-443">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-443">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-444">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-446">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ \_ hardware máquina local \\ \\ \\ \\ DEVICEMAP \\ \\ SCSI SCSI puerto SCSI \\ \\ bus SCSI identificador identificador \\ \\ \\ \\ \\ \\ de unidad lógica \\ \\ ", "Win32Registry \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-446">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DEVICEMAP\\\\Scsi\\\\Scsi Port\\\\Scsi Bus\\\\Target Id\\\\Logical Unit Id\\\\Identifier", "Win32Registry\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-447">Número de modelo del fabricante de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-447">Manufacturer's model number of the disk drive.</span></span>

<span data-ttu-id="aa7c4-448">Ejemplo: "ST32171W"</span><span class="sxs-lookup"><span data-stu-id="aa7c4-448">Example: "ST32171W"</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-449">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-449">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-450">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-452">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-452">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-453">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-453">Label by which the object is known.</span></span> <span data-ttu-id="aa7c4-454">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-454">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="aa7c4-455">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-455">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-456">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-456">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-457">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-459">Si **es true**, el dispositivo de acceso a medios necesita limpieza.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-459">If **True**, the media access device needs cleaning.</span></span> <span data-ttu-id="aa7c4-460">Si la limpieza manual o automática es posible, se indica en la propiedad **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="aa7c4-460">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="aa7c4-461">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-461">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-462">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-462">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-463">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-464">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-465">Número máximo de elementos multimedia que se admiten o insertan (cuando el dispositivo de acceso a medios admite varios medios individuales).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-465">Maximum number of media which can be supported or inserted (when the media access device supports multiple individual media).</span></span>

<span data-ttu-id="aa7c4-466">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-466">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-467">**Particiones**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-467">**Partitions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-468">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-468">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-470">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo \ \| [**\_ información de partición**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RecognizedPartition")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-470">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RecognizedPartition")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-471">Número de particiones en esta unidad de disco físico que reconoce el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-471">Number of partitions on this physical disk drive that are recognized by the operating system.</span></span>

<span data-ttu-id="aa7c4-472">Ejemplo: 2</span><span class="sxs-lookup"><span data-stu-id="aa7c4-472">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-473">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-473">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-474">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-476">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-476">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-477">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-477">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="aa7c4-478">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="aa7c4-479">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="aa7c4-479">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-480">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-480">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-481">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-481">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-483">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-483">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="aa7c4-484">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-484">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa7c4-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-485"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="aa7c4-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-486"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-487">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-487">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa7c4-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aa7c4-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-490">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="aa7c4-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-492">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="aa7c4-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-494">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="aa7c4-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="aa7c4-495">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-495">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="aa7c4-496">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-496">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="aa7c4-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-498">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="aa7c4-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aa7c4-500">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="aa7c4-500">Timed Power-On Supported</span></span>

<span data-ttu-id="aa7c4-501">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa7c4-502">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-503">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-504">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-505">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-505">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="aa7c4-506">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="aa7c4-507">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-508">**SCSIBus**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-508">**SCSIBus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-509">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-509">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-510">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-510">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-511">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo \| [**\_ Dirección SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| PathId")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-511">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PathId")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-512">Número de bus SCSI de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-512">SCSI bus number of the disk drive.</span></span>

<span data-ttu-id="aa7c4-513">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="aa7c4-513">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-514">**SCSILogicalUnit**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-514">**SCSILogicalUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-515">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-516">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-517">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras LUN de \| [**\_ Dirección SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| ")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-517">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|Lun")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-518">Número de unidad lógica (LUN) SCSI de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-518">SCSI logical unit number (LUN) of the disk drive.</span></span>

<span data-ttu-id="aa7c4-519">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="aa7c4-519">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-520">**SCSIPort**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-520">**SCSIPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-521">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-521">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-522">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-523">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo de \| [**\_ Dirección SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| númeroDePuerto")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|PortNumber")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-524">Número de puerto SCSI de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-524">SCSI port number of the disk drive.</span></span>

<span data-ttu-id="aa7c4-525">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="aa7c4-525">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-526">**SCSITargetId**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-526">**SCSITargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-527">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-527">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-528">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-529">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo \| [**\_ Dirección SCSI**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address) \| TargetId")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-529">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**SCSI\_ADDRESS**](/windows-hardware/drivers/ddi/content/ntddscsi/ns-ntddscsi-_scsi_address)\|TargetId")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-530">Número de identificador SCSI de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-530">SCSI identifier number of the disk drive.</span></span>

<span data-ttu-id="aa7c4-531">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="aa7c4-531">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-532">**SectorsPerTrack**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-532">**SectorsPerTrack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-533">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-533">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-534">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-535">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-535">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-536">Número de sectores de cada pista para esta unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-536">Number of sectors in each track for this physical disk drive.</span></span>

<span data-ttu-id="aa7c4-537">Ejemplo: 63</span><span class="sxs-lookup"><span data-stu-id="aa7c4-537">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-538">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-538">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-539">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-539">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-540">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-541">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| [**\_ \_ descriptor de dispositivo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)de inesperados win32api de entrada y salida de dispositivo \| SerialNumberOffset")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**STORAGE\_DEVICE\_DESCRIPTOR**](/windows/desktop/api/winioctl/ns-winioctl-storage_device_descriptor)\|SerialNumberOffset")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-542">Número asignado por el fabricante para identificar el medio físico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-542">Number allocated by the manufacturer to identify the physical media.</span></span>

<span data-ttu-id="aa7c4-543">Ejemplo: WD-WM3493798728</span><span class="sxs-lookup"><span data-stu-id="aa7c4-543">Example: WD-WM3493798728</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-544">**Signature**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-544">**Signature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-545">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-545">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-546">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-547">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras firma de \| [**\_ \_ información de diseño de unidad**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information) \| ")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-547">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DRIVE\_LAYOUT\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-drive_layout_information)\|Signature")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-548">Identificación del disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-548">Disk identification.</span></span> <span data-ttu-id="aa7c4-549">Esta propiedad se puede usar para identificar un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-549">This property can be used to identify a shared resource.</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-550">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-550">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-551">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-551">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-552">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-553">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructura \| [**\_ geométrica del disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-553">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-554">Tamaño de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-554">Size of the disk drive.</span></span> <span data-ttu-id="aa7c4-555">Se calcula multiplicando el número total de cilindros, pistas en cada cilindro, sectores de cada pista y bytes de cada sector.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-555">It is calculated by multiplying the total number of cylinders, tracks in each cylinder, sectors in each track, and bytes in each sector.</span></span>

<span data-ttu-id="aa7c4-556">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-556">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-557">**Estado**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-558">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-559">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-560">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-561">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-561">Current status of the object.</span></span> <span data-ttu-id="aa7c4-562">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-562">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="aa7c4-563">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-563">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="aa7c4-564">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="aa7c4-564">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aa7c4-565">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-565">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aa7c4-566">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-566">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aa7c4-567">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-567">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aa7c4-568">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="aa7c4-568">Values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aa7c4-569">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-569">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aa7c4-570">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-570">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aa7c4-571">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-571">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa7c4-572">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-572">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aa7c4-573">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-573">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aa7c4-574">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-574">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aa7c4-575">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-575">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aa7c4-576">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-576">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aa7c4-577">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-577">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aa7c4-578">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-578">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aa7c4-579">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-579">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aa7c4-580">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-580">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa7c4-581">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-581">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-582">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-583">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-583">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-584">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-584">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-585">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-585">State of the logical device.</span></span> <span data-ttu-id="aa7c4-586">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-586">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="aa7c4-587">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-587">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa7c4-588">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-588">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa7c4-589">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-589">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aa7c4-590">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-590">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa7c4-591">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-591">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aa7c4-592">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-592">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa7c4-593">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-593">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-594">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-594">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-595">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-595">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-596">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-596">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-597">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-597">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="aa7c4-598">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-598">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-599">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-599">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-600">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-600">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-601">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-601">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-602">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aa7c4-602">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-603">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-603">Name of the scoping system.</span></span>

<span data-ttu-id="aa7c4-604">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-604">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-605">**TotalCylinders**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-605">**TotalCylinders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-606">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-606">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-607">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-608">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| ")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|Cylinders")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-609">Número total de cilindros en la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-609">Total number of cylinders on the physical disk drive.</span></span> <span data-ttu-id="aa7c4-610">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-610">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aa7c4-611">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-611">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="aa7c4-612">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-612">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="aa7c4-613">Ejemplo: 657</span><span class="sxs-lookup"><span data-stu-id="aa7c4-613">Example: 657</span></span>

<span data-ttu-id="aa7c4-614">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-614">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-615">**TotalHeads**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-615">**TotalHeads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-616">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-616">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-617">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-618">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-618">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-619">Número total de cabezas en la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-619">Total number of heads on the disk drive.</span></span> <span data-ttu-id="aa7c4-620">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-620">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aa7c4-621">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-621">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="aa7c4-622">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-622">Consult the manufacturer for accurate drive specifications.</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-623">**TotalSectors**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-623">**TotalSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-624">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-624">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-625">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-626">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| SectorsPerTrack")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-626">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|SectorsPerTrack")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-627">Número total de sectores de la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-627">Total number of sectors on the physical disk drive.</span></span> <span data-ttu-id="aa7c4-628">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-628">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aa7c4-629">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-629">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="aa7c4-630">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-630">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="aa7c4-631">Ejemplo: 2649024</span><span class="sxs-lookup"><span data-stu-id="aa7c4-631">Example: 2649024</span></span>

<span data-ttu-id="aa7c4-632">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-632">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-633">**TotalTracks**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-633">**TotalTracks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-634">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-634">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-635">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-636">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-637">Número total de pistas en la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-637">Total number of tracks on the physical disk drive.</span></span> <span data-ttu-id="aa7c4-638">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-638">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aa7c4-639">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-639">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="aa7c4-640">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-640">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="aa7c4-641">Ejemplo: 42048</span><span class="sxs-lookup"><span data-stu-id="aa7c4-641">Example: 42048</span></span>

<span data-ttu-id="aa7c4-642">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-642">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="aa7c4-643">**TracksPerCylinder**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-643">**TracksPerCylinder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa7c4-644">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-644">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-645">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aa7c4-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa7c4-646">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo estructuras de la \| [**\_ geometría de disco**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry) \| TracksPerCylinder")</span><span class="sxs-lookup"><span data-stu-id="aa7c4-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**DISK\_GEOMETRY**](/windows/desktop/api/winioctl/ns-winioctl-disk_geometry)\|TracksPerCylinder")</span></span>
</dt> </dl>

<span data-ttu-id="aa7c4-647">Número de pistas en cada cilindro de la unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-647">Number of tracks in each cylinder on the physical disk drive.</span></span> <span data-ttu-id="aa7c4-648">Nota: el valor de esta propiedad se obtiene a través de funciones extendidas de la interrupción 13h del BIOS.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-648">Note: the value for this property is obtained through extended functions of BIOS interrupt 13h.</span></span> <span data-ttu-id="aa7c4-649">El valor puede ser incorrecto si la unidad utiliza un esquema de traducción para admitir tamaños de disco de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-649">The value may be inaccurate if the drive uses a translation scheme to support high-capacity disk sizes.</span></span> <span data-ttu-id="aa7c4-650">Consulte al fabricante para conocer las especificaciones de unidad precisas.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-650">Consult the manufacturer for accurate drive specifications.</span></span>

<span data-ttu-id="aa7c4-651">Ejemplo: 64</span><span class="sxs-lookup"><span data-stu-id="aa7c4-651">Example: 64</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa7c4-652">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa7c4-652">Remarks</span></span>

<span data-ttu-id="aa7c4-653">Las unidades de disco duro físico son el medio de almacenamiento principal para la información en cualquier entorno informático.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-653">Physical hard disk drives are the primary storage medium for information in any computing environment.</span></span> <span data-ttu-id="aa7c4-654">Aunque las organizaciones suelen usar dispositivos como unidades de cinta y unidades de disco compacto para archivar datos, estos dispositivos no son adecuados para el almacenamiento diario de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-654">Although organizations often use devices such as tape drives and compact disc drives for archiving data, these devices are not suited for day-to-day storage of user data.</span></span> <span data-ttu-id="aa7c4-655">Solo los discos duros físicos ofrecen la velocidad y la facilidad de uso necesaria para almacenar datos y para ejecutar aplicaciones y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-655">Only physical hard disks offer the speed and ease of use required for storing data and for running applications and the operating system.</span></span>

<span data-ttu-id="aa7c4-656">Para administrar los datos de forma eficaz, es importante tener un inventario detallado de todos los discos físicos, sus capacidades y sus capacidades.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-656">To efficiently manage data, it is important to have a detailed inventory of all your physical disks, their capabilities, and their capacities.</span></span> <span data-ttu-id="aa7c4-657">Puede usar la clase **Win32 \_ DiskDrive** para derivar este tipo de inventario.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-657">You can use the **Win32\_DiskDrive** class to derive this type of inventory.</span></span>

<span data-ttu-id="aa7c4-658">Cualquier interfaz a una unidad de disco físico de Windows es un descendiente (o miembro) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-658">Any interface to a Windows physical disk drive is a descendant (or member) of this class.</span></span> <span data-ttu-id="aa7c4-659">Las características de la unidad de disco que se muestran a través de este objeto corresponden a las características lógicas y de administración de la unidad.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-659">The features of the disk drive seen through this object correspond to the logical and management characteristics of the drive.</span></span> <span data-ttu-id="aa7c4-660">En algunos casos, es posible que esto no refleje las características físicas reales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-660">In some cases, this may not reflect the actual physical characteristics of the device.</span></span> <span data-ttu-id="aa7c4-661">Cualquier objeto basado en otro dispositivo lógico no sería un miembro de esta clase.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-661">Any object based on another logical device would not be a member of this class.</span></span>

<span data-ttu-id="aa7c4-662">Por motivos de seguridad, los usuarios que se conectan desde un equipo remoto deben tener el privilegio de **\_ \_ conexión SC Manager** habilitado para poder enumerar esta clase.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-662">For security reasons, a user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="aa7c4-663">Para obtener más información, consulte [seguridad del servicio y derechos de acceso](/windows/desktop/Services/service-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-663">For more information, see [Service Security and Access Rights](/windows/desktop/Services/service-security-and-access-rights).</span></span>

<span data-ttu-id="aa7c4-664">La **clase \_ DiskDrive de Win32** se deriva [**de \_ DiskDrive de CIM**](cim-diskdrive.md) que deriva [**de \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-664">The **Win32\_DiskDrive** class is derived from [**CIM\_DiskDrive**](cim-diskdrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="aa7c4-665">La **clase \_ MediaAccessDevice de CIM** deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aa7c4-665">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="aa7c4-666">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="aa7c4-666">Examples</span></span>

<span data-ttu-id="aa7c4-667">El ejemplo de código de PowerShell [Informe de inventario de servidores-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) en la galería de TechNet usa una serie de clases, incluido **Win32 \_ DiskDrive**, para devolver información sobre el estado del servidor.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-667">The [Servers Inventory report-WMI & CIM](https://Gallery.TechNet.Microsoft.Com/Servers-Inventory-report-e79e2b24) PowerShell code example on TechNet Gallery uses a number of classes, including **Win32\_DiskDrive**, to return information about server status.</span></span>

<span data-ttu-id="aa7c4-668">La [unidad de asignación a la letra de unidad con la \_ propiedad de tipo de interfaz DiskDrive de Win32](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) el ejemplo de código de PowerShell asigna una unidad a una letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="aa7c4-668">The [Map Drive to Drive Letter Using the Win32\_DiskDrive Interface Type Property](https://Gallery.TechNet.Microsoft.Com/Map-Drive-to-Drive-Letter-1fff91ad) PowerShell code sample maps a drive to a drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa7c4-669">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa7c4-669">Requirements</span></span>



| <span data-ttu-id="aa7c4-670">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa7c4-670">Requirement</span></span> | <span data-ttu-id="aa7c4-671">Value</span><span class="sxs-lookup"><span data-stu-id="aa7c4-671">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7c4-672">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa7c4-672">Minimum supported client</span></span><br/> | <span data-ttu-id="aa7c4-673">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa7c4-673">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa7c4-674">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa7c4-674">Minimum supported server</span></span><br/> | <span data-ttu-id="aa7c4-675">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa7c4-675">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa7c4-676">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aa7c4-676">Namespace</span></span><br/>                | <span data-ttu-id="aa7c4-677">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aa7c4-677">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa7c4-678">MOF</span><span class="sxs-lookup"><span data-stu-id="aa7c4-678">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa7c4-679"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa7c4-679"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa7c4-680">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa7c4-680">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa7c4-681"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa7c4-681"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa7c4-682">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa7c4-682">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa7c4-683">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="aa7c4-683">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="aa7c4-684">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="aa7c4-684">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="aa7c4-685">Tareas de WMI: discos y sistemas de archivos</span><span class="sxs-lookup"><span data-stu-id="aa7c4-685">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

