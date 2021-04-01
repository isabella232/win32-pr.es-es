---
description: Win32 \_ MappedLogicalDisk &\# 32; La clase WMI representa los dispositivos de almacenamiento de red que se asignan como discos lógicos en el sistema del equipo.
ms.assetid: 5dd4b0eb-7872-4f2d-9c8b-ea03f7e2c16d
ms.tgt_platform: multiple
title: Win32_MappedLogicalDisk (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MappedLogicalDisk
- Win32_MappedLogicalDisk.Reset
- Win32_MappedLogicalDisk.SetPowerState
- Win32_MappedLogicalDisk.Access
- Win32_MappedLogicalDisk.Availability
- Win32_MappedLogicalDisk.BlockSize
- Win32_MappedLogicalDisk.Caption
- Win32_MappedLogicalDisk.Compressed
- Win32_MappedLogicalDisk.ConfigManagerErrorCode
- Win32_MappedLogicalDisk.ConfigManagerUserConfig
- Win32_MappedLogicalDisk.CreationClassName
- Win32_MappedLogicalDisk.Description
- Win32_MappedLogicalDisk.DeviceID
- Win32_MappedLogicalDisk.ErrorCleared
- Win32_MappedLogicalDisk.ErrorDescription
- Win32_MappedLogicalDisk.ErrorMethodology
- Win32_MappedLogicalDisk.FileSystem
- Win32_MappedLogicalDisk.FreeSpace
- Win32_MappedLogicalDisk.InstallDate
- Win32_MappedLogicalDisk.LastErrorCode
- Win32_MappedLogicalDisk.MaximumComponentLength
- Win32_MappedLogicalDisk.Name
- Win32_MappedLogicalDisk.NumberOfBlocks
- Win32_MappedLogicalDisk.PNPDeviceID
- Win32_MappedLogicalDisk.PowerManagementCapabilities
- Win32_MappedLogicalDisk.PowerManagementSupported
- Win32_MappedLogicalDisk.ProviderName
- Win32_MappedLogicalDisk.Purpose
- Win32_MappedLogicalDisk.QuotasDisabled
- Win32_MappedLogicalDisk.QuotasIncomplete
- Win32_MappedLogicalDisk.QuotasRebuilding
- Win32_MappedLogicalDisk.SessionID
- Win32_MappedLogicalDisk.Size
- Win32_MappedLogicalDisk.Status
- Win32_MappedLogicalDisk.StatusInfo
- Win32_MappedLogicalDisk.SupportsDiskQuotas
- Win32_MappedLogicalDisk.SupportsFileBasedCompression
- Win32_MappedLogicalDisk.SystemCreationClassName
- Win32_MappedLogicalDisk.SystemName
- Win32_MappedLogicalDisk.VolumeName
- Win32_MappedLogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75c3dfee876c34f36fd0b4cf0b59d3a61afcd75c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153489"
---
# <a name="win32_mappedlogicaldisk-class"></a><span data-ttu-id="d346c-103">\_Clase Win32 MappedLogicalDisk</span><span class="sxs-lookup"><span data-stu-id="d346c-103">Win32\_MappedLogicalDisk class</span></span>

<span data-ttu-id="d346c-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MappedLogicalDisk de Win32** representa los dispositivos de almacenamiento de red que se asignan como discos lógicos en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="d346c-104">The **Win32\_MappedLogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents network storage devices that are mapped as logical disks on the computer system.</span></span>

<span data-ttu-id="d346c-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d346c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d346c-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d346c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d346c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d346c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{BCF02FFE-5560-4de2-B419-272918693426}"), AMENDMENT]
class Win32_MappedLogicalDisk : CIM_LogicalDisk
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  boolean  Compressed;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProviderName;
  string   Purpose;
  boolean  QuotasDisabled;
  boolean  QuotasIncomplete;
  boolean  QuotasRebuilding;
  string   SessionID;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="d346c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d346c-108">Members</span></span>

<span data-ttu-id="d346c-109">La **clase \_ MappedLogicalDisk de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d346c-109">The **Win32\_MappedLogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="d346c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d346c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d346c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d346c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d346c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d346c-112">Methods</span></span>

<span data-ttu-id="d346c-113">La clase **Win32 \_ MappedLogicalDisk** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d346c-113">The **Win32\_MappedLogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="d346c-114">Método</span><span class="sxs-lookup"><span data-stu-id="d346c-114">Method</span></span>            | <span data-ttu-id="d346c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d346c-115">Description</span></span>                                                                                                                                                                                |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d346c-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="d346c-116">**Reset**</span></span>         | <span data-ttu-id="d346c-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d346c-117">Not implemented.</span></span> <span data-ttu-id="d346c-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>                 |
| <span data-ttu-id="d346c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d346c-119">**SetPowerState**</span></span> | <span data-ttu-id="d346c-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d346c-120">Not implemented.</span></span> <span data-ttu-id="d346c-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d346c-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d346c-122">Properties</span></span>

<span data-ttu-id="d346c-123">La **clase \_ MappedLogicalDisk de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d346c-123">The **Win32\_MappedLogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d346c-124">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="d346c-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d346c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-127">Estado de acceso del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-127">Device access state.</span></span>

<span data-ttu-id="d346c-128">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d346c-129">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d346c-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="d346c-130">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="d346c-130">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="d346c-131">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="d346c-131">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="d346c-132">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="d346c-132">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="d346c-133">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="d346c-133">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d346c-134">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="d346c-134">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d346c-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-137">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d346c-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-138">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-138">Availability and status of the device.</span></span>

<span data-ttu-id="d346c-139">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d346c-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d346c-140"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d346c-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d346c-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d346c-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d346c-142"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-143">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="d346c-143">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d346c-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="d346c-144"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d346c-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="d346c-145"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d346c-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d346c-146"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d346c-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="d346c-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d346c-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="d346c-148"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-149">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="d346c-149">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d346c-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="d346c-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d346c-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="d346c-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d346c-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="d346c-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d346c-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="d346c-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d346c-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="d346c-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-155">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="d346c-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d346c-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="d346c-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-157">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="d346c-157">The device is in a power save state but still functioning and can exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d346c-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="d346c-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-159">El dispositivo no funciona, pero se puede volver rápidamente a la alimentación completa.</span><span class="sxs-lookup"><span data-stu-id="d346c-159">The device is not functioning, but can be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d346c-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="d346c-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d346c-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="d346c-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-162">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="d346c-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d346c-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d346c-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-164">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d346c-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d346c-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="d346c-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-166">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="d346c-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d346c-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="d346c-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-168">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="d346c-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d346c-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d346c-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-170">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="d346c-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d346c-171">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="d346c-171">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-172">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d346c-172">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-174">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="d346c-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-175">Tamaño, en bytes, de los bloques que forman esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d346c-175">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="d346c-176">Si este concepto no es válido para el tipo de dispositivo, el valor es 1.</span><span class="sxs-lookup"><span data-stu-id="d346c-176">If this concept is not valid for the device type, the value is 1.</span></span>

<span data-ttu-id="d346c-177">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-177">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d346c-178">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d346c-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-179">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d346c-179">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-182">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d346c-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-183">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d346c-183">Short description of the object.</span></span>

<span data-ttu-id="d346c-184">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-185">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="d346c-185">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-186">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-188">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api ( \| funciones del sistema de archivos) \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ Vol \_ \_ Compressed")</span><span class="sxs-lookup"><span data-stu-id="d346c-188">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-189">Si es **true**, el archivo se comprime.</span><span class="sxs-lookup"><span data-stu-id="d346c-189">If **True**, the file is compressed.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d346c-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-191">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d346c-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-193">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d346c-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-194">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d346c-194">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="d346c-195">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d346c-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d346c-196"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d346c-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="d346c-197">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-198">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d346c-198">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d346c-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d346c-199"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d346c-200">(1)</span><span class="sxs-lookup"><span data-stu-id="d346c-200">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-201">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d346c-201">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d346c-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-202"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d346c-203">(2)</span><span class="sxs-lookup"><span data-stu-id="d346c-203">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d346c-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="d346c-204"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d346c-205">(3)</span><span class="sxs-lookup"><span data-stu-id="d346c-205">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-206">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="d346c-206">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d346c-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="d346c-207"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d346c-208">(4)</span><span class="sxs-lookup"><span data-stu-id="d346c-208">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-209">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d346c-209">Device is not working properly.</span></span> <span data-ttu-id="d346c-210">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="d346c-210">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d346c-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="d346c-211"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d346c-212">(5)</span><span class="sxs-lookup"><span data-stu-id="d346c-212">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-213">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="d346c-213">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d346c-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="d346c-214"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d346c-215"> (6)</span><span class="sxs-lookup"><span data-stu-id="d346c-215">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-216">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d346c-216">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d346c-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="d346c-217"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d346c-218">(7)</span><span class="sxs-lookup"><span data-stu-id="d346c-218">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d346c-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-219"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d346c-220">(8)</span><span class="sxs-lookup"><span data-stu-id="d346c-220">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-221">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-221">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d346c-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="d346c-222"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d346c-223">(9)</span><span class="sxs-lookup"><span data-stu-id="d346c-223">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-224">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d346c-224">Device is not working properly.</span></span> <span data-ttu-id="d346c-225">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-225">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d346c-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="d346c-226"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d346c-227">(10)</span><span class="sxs-lookup"><span data-stu-id="d346c-227">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-228">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="d346c-228">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d346c-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-229"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d346c-230">(11)</span><span class="sxs-lookup"><span data-stu-id="d346c-230">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-231">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-231">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d346c-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="d346c-232"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d346c-233">(12)</span><span class="sxs-lookup"><span data-stu-id="d346c-233">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-234">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="d346c-234">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d346c-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-235"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d346c-236">(13)</span><span class="sxs-lookup"><span data-stu-id="d346c-236">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-237">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-237">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d346c-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-238"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d346c-239">(14)</span><span class="sxs-lookup"><span data-stu-id="d346c-239">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-240">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="d346c-240">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d346c-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="d346c-241"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d346c-242">(15)</span><span class="sxs-lookup"><span data-stu-id="d346c-242">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-243">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="d346c-243">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d346c-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-244"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d346c-245">(16)</span><span class="sxs-lookup"><span data-stu-id="d346c-245">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-246">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-246">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d346c-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="d346c-247"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d346c-248">(17)</span><span class="sxs-lookup"><span data-stu-id="d346c-248">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-249">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="d346c-249">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d346c-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-250"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d346c-251">(18)</span><span class="sxs-lookup"><span data-stu-id="d346c-251">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-252">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d346c-252">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d346c-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="d346c-253"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d346c-254">(19)</span><span class="sxs-lookup"><span data-stu-id="d346c-254">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d346c-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="d346c-255"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d346c-256">(20)</span><span class="sxs-lookup"><span data-stu-id="d346c-256">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-257">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="d346c-257">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d346c-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-258"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d346c-259">(21)</span><span class="sxs-lookup"><span data-stu-id="d346c-259">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-260">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d346c-260">System failure.</span></span> <span data-ttu-id="d346c-261">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d346c-261">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d346c-262">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-262">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d346c-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="d346c-263"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d346c-264">(22)</span><span class="sxs-lookup"><span data-stu-id="d346c-264">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-265">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d346c-265">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d346c-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="d346c-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d346c-267">(23)</span><span class="sxs-lookup"><span data-stu-id="d346c-267">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-268">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d346c-268">System failure.</span></span> <span data-ttu-id="d346c-269">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d346c-269">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d346c-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="d346c-270"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d346c-271">(24)</span><span class="sxs-lookup"><span data-stu-id="d346c-271">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-272">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="d346c-272">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d346c-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d346c-274">(25)</span><span class="sxs-lookup"><span data-stu-id="d346c-274">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-275">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d346c-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-276"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d346c-277">(26)</span><span class="sxs-lookup"><span data-stu-id="d346c-277">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-278">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d346c-278">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d346c-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="d346c-279"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d346c-280">(27)</span><span class="sxs-lookup"><span data-stu-id="d346c-280">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-281">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="d346c-281">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d346c-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="d346c-282"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d346c-283">(28)</span><span class="sxs-lookup"><span data-stu-id="d346c-283">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-284">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="d346c-284">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d346c-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="d346c-285"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d346c-286">(29)</span><span class="sxs-lookup"><span data-stu-id="d346c-286">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-287">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d346c-287">Device is disabled.</span></span> <span data-ttu-id="d346c-288">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d346c-288">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d346c-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="d346c-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d346c-290">(30)</span><span class="sxs-lookup"><span data-stu-id="d346c-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-291">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="d346c-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d346c-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d346c-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d346c-293">31</span><span class="sxs-lookup"><span data-stu-id="d346c-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-294">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d346c-294">Device is not working properly.</span></span> <span data-ttu-id="d346c-295">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d346c-295">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d346c-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d346c-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-297">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-299">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d346c-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-300">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d346c-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d346c-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d346c-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-305">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d346c-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d346c-306">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="d346c-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d346c-307">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="d346c-307">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d346c-308">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-309">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d346c-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-312">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="d346c-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-313">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d346c-313">Description of the object.</span></span>

<span data-ttu-id="d346c-314">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-315">**ID**</span><span class="sxs-lookup"><span data-stu-id="d346c-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-318">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d346c-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-319">Identificador único de la matriz de memoria.</span><span class="sxs-lookup"><span data-stu-id="d346c-319">Unique identifier of the memory array.</span></span>

<span data-ttu-id="d346c-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d346c-321">Ejemplo: "matriz de memoria 1"</span><span class="sxs-lookup"><span data-stu-id="d346c-321">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="d346c-322">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d346c-322">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-323">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-325">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="d346c-325">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d346c-326">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-327">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d346c-327">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-330">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="d346c-330">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span>

<span data-ttu-id="d346c-331">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-332">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="d346c-332">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-335">Tipos de comprobación de errores utilizados por el hardware.</span><span class="sxs-lookup"><span data-stu-id="d346c-335">Types of error checking used by the hardware.</span></span>

<span data-ttu-id="d346c-336">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-336">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-337">**Systems**</span><span class="sxs-lookup"><span data-stu-id="d346c-337">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-340">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="d346c-340">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="d346c-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-341">Access type: Read-only</span></span>

<span data-ttu-id="d346c-342">Sistema de archivos en el disco lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-342">File system on the logical disk.</span></span>

<span data-ttu-id="d346c-343">Ejemplo: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="d346c-343">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="d346c-344">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="d346c-344">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-345">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d346c-345">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-347">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d346c-347">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-348">Espacio disponible en el disco lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-348">Space available on the logical disk.</span></span>

<span data-ttu-id="d346c-349">Esta propiedad se hereda del [**\_ LogicalDisk de CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-349">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="d346c-350">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d346c-350">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-351">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d346c-351">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-352">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d346c-352">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-354">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="d346c-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-355">Access type: Read-only</span></span>

<span data-ttu-id="d346c-356">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="d346c-356">Date and time the object was installed.</span></span> <span data-ttu-id="d346c-357">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d346c-357">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d346c-358">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-359">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d346c-359">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-360">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d346c-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-362">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-362">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d346c-363">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-364">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="d346c-364">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-365">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d346c-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-367">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="d346c-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="d346c-368">Contiene la longitud máxima de un componente de nombre de archivo compatible con la unidad de Windows.</span><span class="sxs-lookup"><span data-stu-id="d346c-368">Contains the maximum length of a file-name component supported by the Windows drive.</span></span>

<span data-ttu-id="d346c-369">Ejemplo: 255</span><span class="sxs-lookup"><span data-stu-id="d346c-369">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="d346c-370">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d346c-370">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-371">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-373">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d346c-373">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-374">Etiqueta del objeto.</span><span class="sxs-lookup"><span data-stu-id="d346c-374">Object label.</span></span>

<span data-ttu-id="d346c-375">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-376">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="d346c-376">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-377">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d346c-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-379">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="d346c-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-380">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d346c-380">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="d346c-381">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d346c-381">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="d346c-382">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d346c-382">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="d346c-383">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-383">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d346c-384">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d346c-384">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-385">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d346c-385">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-386">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-388">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d346c-388">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-389">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-389">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d346c-390">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d346c-391">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d346c-391">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d346c-392">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d346c-392">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-393">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d346c-393">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d346c-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-395">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-395">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d346c-396">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="d346c-396">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d346c-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d346c-397"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d346c-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d346c-398"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d346c-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d346c-399"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d346c-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d346c-400"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-401">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d346c-401">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d346c-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d346c-402"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-403">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="d346c-403">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d346c-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="d346c-404"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-405">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d346c-405">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d346c-406">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="d346c-406">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d346c-407">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d346c-407">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d346c-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="d346c-408"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-409">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="d346c-409">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d346c-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="d346c-410"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d346c-411">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="d346c-411">Timed Power-On Supported</span></span>

<span data-ttu-id="d346c-412">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="d346c-412">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d346c-413">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d346c-413">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-414">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-414">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-416">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="d346c-416">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="d346c-417">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="d346c-417">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d346c-418">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-418">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-419">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="d346c-419">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-420">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-422">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| funciones de red de Windows \| WNetGetConnection")</span><span class="sxs-lookup"><span data-stu-id="d346c-422">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-423">Nombre de la ruta de acceso de red al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-423">Network path name to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-424">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="d346c-424">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-425">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-427">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="d346c-427">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="d346c-428">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-429">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="d346c-429">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-430">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-430">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-432">Si es **true**, la administración de cuotas no está habilitada para este volumen.</span><span class="sxs-lookup"><span data-stu-id="d346c-432">If **True**, quota management is not enabled for this volume.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-433">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="d346c-433">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-434">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-434">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-436">Si **es true**, se usó la administración de cuotas pero se ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d346c-436">If **True**, quota management was used but has been disabled.</span></span> <span data-ttu-id="d346c-437">Incompleto hace referencia a la información que queda en el sistema de archivos después de que se haya deshabilitado la administración de cuotas.</span><span class="sxs-lookup"><span data-stu-id="d346c-437">Incomplete refers to the information left in the file system after quota management has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-438">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="d346c-438">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-439">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-441">Si es **true**, el sistema de archivos se está configurando para la administración de cuotas.</span><span class="sxs-lookup"><span data-stu-id="d346c-441">If **True**, the file system is setting up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-442">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="d346c-442">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-445">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d346c-445">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d346c-446">IDENTIFICADOR de la sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="d346c-446">ID of the user's session.</span></span> <span data-ttu-id="d346c-447">El usuario se puede conectar mediante un inicio de sesión local o una sesión de terminal.</span><span class="sxs-lookup"><span data-stu-id="d346c-447">The user may be connected using a local login or a terminal session.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-448">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="d346c-448">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-449">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d346c-449">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-451">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="d346c-451">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-452">Tamaño del disco lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-452">Size of the logical disk.</span></span>

<span data-ttu-id="d346c-453">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d346c-453">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d346c-454">Esta propiedad se hereda del [**\_ LogicalDisk de CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-454">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-455">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d346c-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-456">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-458">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d346c-458">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-459">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d346c-459">Current status of the object.</span></span> <span data-ttu-id="d346c-460">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="d346c-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d346c-461">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART puede funcionar correctamente, pero predice un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d346c-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="d346c-462">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d346c-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d346c-463">El estado del servicio se aplica a la tarea administrativa, como la reduplicación de reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d346c-463">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d346c-464">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d346c-464">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d346c-465">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d346c-466">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="d346c-466">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d346c-467">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="d346c-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d346c-468">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="d346c-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d346c-469">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d346c-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d346c-470">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="d346c-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d346c-471">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d346c-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d346c-472">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="d346c-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d346c-473">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="d346c-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d346c-474">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="d346c-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d346c-475">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="d346c-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d346c-476">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d346c-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d346c-477">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="d346c-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d346c-478">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="d346c-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d346c-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d346c-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-480">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d346c-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-482">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d346c-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-483">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-483">State of the logical device.</span></span> <span data-ttu-id="d346c-484">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="d346c-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d346c-485">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d346c-486">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d346c-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d346c-487">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d346c-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d346c-488">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d346c-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d346c-489">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="d346c-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d346c-490">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d346c-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d346c-491">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="d346c-491">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-492">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-492">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-493">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d346c-494">Si es **true**, el sistema de archivos en el que se asigna esta unidad de red es compatible con las cuotas de disco.</span><span class="sxs-lookup"><span data-stu-id="d346c-494">If **True**, then the file system on which this network drive is mapped supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-495">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="d346c-495">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-496">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d346c-496">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-497">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-498">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ file \_ compression")</span><span class="sxs-lookup"><span data-stu-id="d346c-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="d346c-499">Si es **true**, la partición de disco lógico admite la compresión basada en archivos, como es el caso de NTFS.</span><span class="sxs-lookup"><span data-stu-id="d346c-499">If **True**, the logical disk partition supports file-based compression, such as is the case with NTFS.</span></span> <span data-ttu-id="d346c-500">Esta propiedad es **false** cuando la propiedad **Compressed** es **true**.</span><span class="sxs-lookup"><span data-stu-id="d346c-500">This property is **False**, when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-501">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d346c-501">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-502">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-503">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-504">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d346c-504">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d346c-505">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d346c-505">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d346c-506">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-506">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-507">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d346c-507">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-508">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-509">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-510">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d346c-510">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d346c-511">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d346c-511">Name of the scoping system.</span></span>

<span data-ttu-id="d346c-512">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-512">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d346c-513">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="d346c-513">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-514">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-515">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d346c-515">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d346c-516">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="d346c-516">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="d346c-517">Nombre del volumen del disco lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-517">Volume name of the logical disk.</span></span> <span data-ttu-id="d346c-518">Este valor de propiedad puede tener un máximo de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d346c-518">This property value can have a maximum of 32 characters.</span></span>

</dd> <dt>

<span data-ttu-id="d346c-519">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="d346c-519">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d346c-520">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d346c-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d346c-521">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d346c-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d346c-522">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="d346c-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="d346c-523">Número de serie del volumen del disco lógico.</span><span class="sxs-lookup"><span data-stu-id="d346c-523">Volume serial number of the logical disk.</span></span> <span data-ttu-id="d346c-524">Este valor de propiedad puede tener un máximo de 11 caracteres.</span><span class="sxs-lookup"><span data-stu-id="d346c-524">This property value can have a maximum of 11 characters.</span></span>

<span data-ttu-id="d346c-525">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d346c-525">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d346c-526">Ejemplo: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="d346c-526">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d346c-527">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d346c-527">Remarks</span></span>

<span data-ttu-id="d346c-528">Las instancias devueltas para esta clase son las siguientes, suponiendo que el usuario A está enumerando las instancias:</span><span class="sxs-lookup"><span data-stu-id="d346c-528">The instances returned for this class are as follows, supposing that user A is enumerating the instances:</span></span>

-   <span data-ttu-id="d346c-529">El proveedor busca una sesión de inicio de sesión del usuario A en ese equipo:</span><span class="sxs-lookup"><span data-stu-id="d346c-529">The provider looks for a logon session of user A on that machine:</span></span>

    -   <span data-ttu-id="d346c-530">Si hay una sesión de inicio de sesión (y solo una), el proveedor devuelve las unidades asignadas de esa sesión.</span><span class="sxs-lookup"><span data-stu-id="d346c-530">If there is one (and only one) such logon session, then the provider returns the mapped drives of that session.</span></span>
    -   <span data-ttu-id="d346c-531">Si hay más de una sesión para el usuario A en el equipo, no se devuelve ninguna instancia de unidad asignada (porque el proveedor no tiene una forma razonable de decidir qué sesión usar).</span><span class="sxs-lookup"><span data-stu-id="d346c-531">If there is more than one session for user A on the machine, then no mapped drive instances are returned (because the provider has no reasonable way of deciding which session to use).</span></span>

-   <span data-ttu-id="d346c-532">Si no hay ninguna sesión de usuario A en ejecución, y hay un usuario que ha iniciado sesión localmente B:</span><span class="sxs-lookup"><span data-stu-id="d346c-532">If there are no sessions of user A running, and there is a locally logged on user B:</span></span>

    -   <span data-ttu-id="d346c-533">Si hay una sola sesión para el usuario B, el proveedor suplanta a y devuelve las unidades asignadas del usuario B. Este caso es compatible con el escenario de soporte técnico que quiere ver las instancias de un usuario que ha iniciado sesión localmente.</span><span class="sxs-lookup"><span data-stu-id="d346c-533">If there is a single session for user B, then the provider impersonates A and returns the mapped drives of user B. This case supports the scenario of Helpdesk wanting to see the instances of a locally logged on user.</span></span> <span data-ttu-id="d346c-534">Sin embargo, el hecho de que se devuelvan instancias dependerá de la configuración de la Directiva de seguridad local en las herramientas administrativas del panel de control.</span><span class="sxs-lookup"><span data-stu-id="d346c-534">However, whether instances are returned depends on the Local Security Policy settings in the Control Panel Administrative Tools.</span></span> <span data-ttu-id="d346c-535">Si la siguiente directiva se establece en "creador del objeto", no se devuelve ninguna instancia de unidad asignada, incluso si es miembro del grupo administradores:</span><span class="sxs-lookup"><span data-stu-id="d346c-535">If the following policy is set to "Object Creator", then no mapped drive instances are returned, even if A is a member of the Administrators group:</span></span>

        <span data-ttu-id="d346c-536">"Objeto de sistema: propietario predeterminado para los objetos creados por miembros del grupo de administradores".</span><span class="sxs-lookup"><span data-stu-id="d346c-536">"System object: default owner for objects created by members of the administrators group."</span></span>

    -   <span data-ttu-id="d346c-537">De nuevo, si hay más de una sesión de usuario B ejecutándose en el equipo, el proveedor no tiene forma de decidir cuál usar.</span><span class="sxs-lookup"><span data-stu-id="d346c-537">Again, if there is more than one session of user B running on the machine, then the provider has no way of deciding which to use.</span></span> <span data-ttu-id="d346c-538">En este caso, no se devuelve ninguna instancia de unidad asignada.</span><span class="sxs-lookup"><span data-stu-id="d346c-538">In this case, no mapped drive instances are returned.</span></span>

<span data-ttu-id="d346c-539">Para obtener más información sobre el uso de **Win32 \_ MappedLogicalDisk**, consulte [¿Cómo puedo determinar qué unidades están asignadas a recursos compartidos de red?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span><span class="sxs-lookup"><span data-stu-id="d346c-539">For more information on using **Win32\_MappedLogicalDisk**, see [How Can I Determine Which Drives are Mapped to Network Shares?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/10/27/how-can-i-determine-which-drives-are-mapped-to-network-shares.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="d346c-540">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d346c-540">Examples</span></span>

<span data-ttu-id="d346c-541">El siguiente fragmento de código de PowerShell muestra las unidades asignadas.</span><span class="sxs-lookup"><span data-stu-id="d346c-541">The following PowerShell snippet shows mapped drives.</span></span>


```PowerShell
Get-WmiObject Win32_MappedLogicalDisk | Select Name, ProviderName, FileSystem, Size, FreeSpace | Format-Table
```



## <a name="requirements"></a><span data-ttu-id="d346c-542">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d346c-542">Requirements</span></span>



| <span data-ttu-id="d346c-543">Requisito</span><span class="sxs-lookup"><span data-stu-id="d346c-543">Requirement</span></span> | <span data-ttu-id="d346c-544">Value</span><span class="sxs-lookup"><span data-stu-id="d346c-544">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d346c-545">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d346c-545">Minimum supported client</span></span><br/> | <span data-ttu-id="d346c-546">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d346c-546">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d346c-547">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d346c-547">Minimum supported server</span></span><br/> | <span data-ttu-id="d346c-548">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d346c-548">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d346c-549">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d346c-549">Namespace</span></span><br/>                | <span data-ttu-id="d346c-550">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d346c-550">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d346c-551">MOF</span><span class="sxs-lookup"><span data-stu-id="d346c-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d346c-552"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d346c-552"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d346c-553">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d346c-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d346c-554"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d346c-554"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d346c-555">Vea también</span><span class="sxs-lookup"><span data-stu-id="d346c-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d346c-556">**LogicalDisk de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d346c-556">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="d346c-557">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d346c-557">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d346c-558">Tareas de WMI: discos y sistemas de archivos</span><span class="sxs-lookup"><span data-stu-id="d346c-558">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

