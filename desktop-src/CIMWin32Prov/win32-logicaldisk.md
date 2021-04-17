---
description: Representa un origen de datos que se resuelve en un dispositivo de almacenamiento local real en un equipo con Windows.
ms.assetid: 134a90cc-b2c3-4ade-a317-b96c4aabe63d
ms.tgt_platform: multiple
title: Win32_LogicalDisk (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk
- Win32_LogicalDisk.Reset
- Win32_LogicalDisk.SetPowerState
- Win32_LogicalDisk.Access
- Win32_LogicalDisk.Availability
- Win32_LogicalDisk.BlockSize
- Win32_LogicalDisk.Caption
- Win32_LogicalDisk.Compressed
- Win32_LogicalDisk.ConfigManagerErrorCode
- Win32_LogicalDisk.ConfigManagerUserConfig
- Win32_LogicalDisk.CreationClassName
- Win32_LogicalDisk.Description
- Win32_LogicalDisk.DeviceID
- Win32_LogicalDisk.DriveType
- Win32_LogicalDisk.ErrorCleared
- Win32_LogicalDisk.ErrorDescription
- Win32_LogicalDisk.ErrorMethodology
- Win32_LogicalDisk.FileSystem
- Win32_LogicalDisk.FreeSpace
- Win32_LogicalDisk.InstallDate
- Win32_LogicalDisk.LastErrorCode
- Win32_LogicalDisk.MaximumComponentLength
- Win32_LogicalDisk.MediaType
- Win32_LogicalDisk.Name
- Win32_LogicalDisk.NumberOfBlocks
- Win32_LogicalDisk.PNPDeviceID
- Win32_LogicalDisk.PowerManagementCapabilities
- Win32_LogicalDisk.PowerManagementSupported
- Win32_LogicalDisk.ProviderName
- Win32_LogicalDisk.Purpose
- Win32_LogicalDisk.QuotasDisabled
- Win32_LogicalDisk.QuotasIncomplete
- Win32_LogicalDisk.QuotasRebuilding
- Win32_LogicalDisk.Size
- Win32_LogicalDisk.Status
- Win32_LogicalDisk.StatusInfo
- Win32_LogicalDisk.SupportsDiskQuotas
- Win32_LogicalDisk.SupportsFileBasedCompression
- Win32_LogicalDisk.SystemCreationClassName
- Win32_LogicalDisk.SystemName
- Win32_LogicalDisk.VolumeDirty
- Win32_LogicalDisk.VolumeName
- Win32_LogicalDisk.VolumeSerialNumber
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad1472f14e73d06c19ccc0808794a47f7588cf9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659359"
---
# <a name="win32_logicaldisk-class"></a><span data-ttu-id="cafe1-103">Win32 \_ LogicalDisk (clase)</span><span class="sxs-lookup"><span data-stu-id="cafe1-103">Win32\_LogicalDisk class</span></span>

<span data-ttu-id="cafe1-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalDisk de Win32** representa un origen de datos que se resuelve en un dispositivo de almacenamiento local real en un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="cafe1-104">The **Win32\_LogicalDisk** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a data source that resolves to an actual local storage device on a computer system running Windows.</span></span>

<span data-ttu-id="cafe1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cafe1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cafe1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cafe1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cafe1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cafe1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDisk : CIM_LogicalDisk
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
  uint32   DriveType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  string   FileSystem;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaximumComponentLength;
  uint32   MediaType;
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
  string   Size;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsDiskQuotas;
  boolean  SupportsFileBasedCompression;
  string   SystemCreationClassName;
  string   SystemName;
  boolean  VolumeDirty;
  string   VolumeName;
  string   VolumeSerialNumber;
};
```

## <a name="members"></a><span data-ttu-id="cafe1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cafe1-108">Members</span></span>

<span data-ttu-id="cafe1-109">La clase **Win32 \_ LogicalDisk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cafe1-109">The **Win32\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="cafe1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="cafe1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cafe1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cafe1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cafe1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cafe1-112">Methods</span></span>

<span data-ttu-id="cafe1-113">La clase **Win32 \_ LogicalDisk** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="cafe1-113">The **Win32\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="cafe1-114">Método</span><span class="sxs-lookup"><span data-stu-id="cafe1-114">Method</span></span>                                                                             | <span data-ttu-id="cafe1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="cafe1-115">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cafe1-116">**Emprende**</span><span class="sxs-lookup"><span data-stu-id="cafe1-116">**Chkdsk**</span></span>](chkdsk-method-in-class-win32-logicaldisk.md)                         | <span data-ttu-id="cafe1-117">Invoca la operación [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) en el disco.</span><span class="sxs-lookup"><span data-stu-id="cafe1-117">Invokes the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation on the disk.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="cafe1-118">**ExcludeFromAutochk**</span><span class="sxs-lookup"><span data-stu-id="cafe1-118">**ExcludeFromAutochk**</span></span>](excludefromautochk-method-in-class-win32-logicaldisk.md) | <span data-ttu-id="cafe1-119">Excluye los discos de la operación [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) que se ejecutarán en el siguiente reinicio.</span><span class="sxs-lookup"><span data-stu-id="cafe1-119">Excludes disks from the [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) operation to be run at the next restart.</span></span><br/>                                                                                      |
| <span data-ttu-id="cafe1-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="cafe1-120">**Reset**</span></span>                                                                          | <span data-ttu-id="cafe1-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="cafe1-121">Not implemented.</span></span> <span data-ttu-id="cafe1-122">Para obtener más información sobre cómo implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ LogicalDisk**](cim-logicaldisk.md) for Documentation.</span><span class="sxs-lookup"><span data-stu-id="cafe1-122">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md) for documentation.</span></span><br/> |
| [<span data-ttu-id="cafe1-123">**ScheduleAutoChk**</span><span class="sxs-lookup"><span data-stu-id="cafe1-123">**ScheduleAutoChk**</span></span>](scheduleautochk-method-in-class-win32-logicaldisk.md)       | <span data-ttu-id="cafe1-124">Programa que se ejecute [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) en el siguiente reinicio si se ha establecido el bit de integridad.</span><span class="sxs-lookup"><span data-stu-id="cafe1-124">Schedules [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart if the dirty bit has been set.</span></span><br/>                                                                                |
| <span data-ttu-id="cafe1-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cafe1-125">**SetPowerState**</span></span>                                                                  | <span data-ttu-id="cafe1-126">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="cafe1-126">Not implemented.</span></span> <span data-ttu-id="cafe1-127">Para obtener más información sobre cómo implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ LogicalDisk**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-127">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="cafe1-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cafe1-128">Properties</span></span>

<span data-ttu-id="cafe1-129">La clase **Win32 \_ LogicalDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cafe1-129">The **Win32\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cafe1-130">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="cafe1-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cafe1-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-133">Tipo de acceso a medios disponible.</span><span class="sxs-lookup"><span data-stu-id="cafe1-133">Type of media access available.</span></span>

<span data-ttu-id="cafe1-134">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cafe1-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cafe1-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="cafe1-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="cafe1-136"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="cafe1-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="cafe1-137"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-138">Editable</span><span class="sxs-lookup"><span data-stu-id="cafe1-138">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="cafe1-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="cafe1-139"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="cafe1-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="cafe1-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe1-141">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="cafe1-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-142">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cafe1-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-144">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="cafe1-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-145">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-145">Availability and status of the device.</span></span>

<span data-ttu-id="cafe1-146">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cafe1-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="cafe1-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cafe1-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="cafe1-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="cafe1-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="cafe1-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-150">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="cafe1-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="cafe1-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="cafe1-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="cafe1-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="cafe1-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cafe1-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="cafe1-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="cafe1-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="cafe1-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="cafe1-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="cafe1-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-156">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="cafe1-156">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="cafe1-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="cafe1-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cafe1-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="cafe1-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="cafe1-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="cafe1-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="cafe1-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="cafe1-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="cafe1-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="cafe1-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-162">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="cafe1-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="cafe1-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="cafe1-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-164">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="cafe1-164">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="cafe1-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="cafe1-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-166">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="cafe1-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="cafe1-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="cafe1-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="cafe1-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="cafe1-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-169">El dispositivo está en un estado de advertencia, pero también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="cafe1-169">The device is in a warning state, but also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="cafe1-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="cafe1-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-171">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="cafe1-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="cafe1-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="cafe1-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-173">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="cafe1-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="cafe1-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-175">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="cafe1-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="cafe1-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="cafe1-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-177">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="cafe1-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe1-178">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="cafe1-178">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-179">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cafe1-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-181">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="cafe1-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-182">Tamaño, en bytes, de los bloques que forman esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="cafe1-182">Size, in bytes, of the blocks that form this storage extent.</span></span> <span data-ttu-id="cafe1-183">Si es desconocido o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1.</span><span class="sxs-lookup"><span data-stu-id="cafe1-183">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter 1.</span></span>

<span data-ttu-id="cafe1-184">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="cafe1-185">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cafe1-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-186">**Caption**</span><span class="sxs-lookup"><span data-stu-id="cafe1-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-189">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cafe1-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-190">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="cafe1-190">Short description of the object a one-line string.</span></span>

<span data-ttu-id="cafe1-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-192">**Compressed**</span><span class="sxs-lookup"><span data-stu-id="cafe1-192">**Compressed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-193">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-195">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api ( \| funciones del sistema de archivos) \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ Vol \_ \_ Compressed")</span><span class="sxs-lookup"><span data-stu-id="cafe1-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_VOL\_IS\_COMPRESSED")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-196">Si **es true**, el volumen lógico existe como una única entidad comprimida, como un volumen de DoubleSpace.</span><span class="sxs-lookup"><span data-stu-id="cafe1-196">If **True**, the logical volume exists as a single compressed entity, such as a DoubleSpace volume.</span></span> <span data-ttu-id="cafe1-197">Si se admite la compresión basada en archivos, como en NTFS, esta propiedad es **false**.</span><span class="sxs-lookup"><span data-stu-id="cafe1-197">If file based compression is supported, such as on NTFS, this property is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-198">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cafe1-198">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-199">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cafe1-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-201">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cafe1-201">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-202">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="cafe1-202">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="cafe1-203">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-203">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="cafe1-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-204"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="cafe1-205"> (0)</span><span class="sxs-lookup"><span data-stu-id="cafe1-205">(0)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-206">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="cafe1-206">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="cafe1-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-207"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="cafe1-208">(1)</span><span class="sxs-lookup"><span data-stu-id="cafe1-208">(1)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-209">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="cafe1-209">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cafe1-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-210"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="cafe1-211">(2)</span><span class="sxs-lookup"><span data-stu-id="cafe1-211">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="cafe1-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-212"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="cafe1-213">(3)</span><span class="sxs-lookup"><span data-stu-id="cafe1-213">(3)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-214">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="cafe1-214">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cafe1-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-215"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="cafe1-216">(4)</span><span class="sxs-lookup"><span data-stu-id="cafe1-216">(4)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-217">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="cafe1-217">Device is not working properly.</span></span> <span data-ttu-id="cafe1-218">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="cafe1-218">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="cafe1-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-219"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="cafe1-220">(5)</span><span class="sxs-lookup"><span data-stu-id="cafe1-220">(5)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-221">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="cafe1-221">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="cafe1-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-222"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="cafe1-223"> (6)</span><span class="sxs-lookup"><span data-stu-id="cafe1-223">(6)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-224">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cafe1-224">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="cafe1-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-225"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="cafe1-226">(7)</span><span class="sxs-lookup"><span data-stu-id="cafe1-226">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="cafe1-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-227"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="cafe1-228">(8)</span><span class="sxs-lookup"><span data-stu-id="cafe1-228">(8)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-229">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-229">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="cafe1-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-230"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="cafe1-231">(9)</span><span class="sxs-lookup"><span data-stu-id="cafe1-231">(9)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-232">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="cafe1-232">Device is not working properly.</span></span> <span data-ttu-id="cafe1-233">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-233">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="cafe1-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-234"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="cafe1-235">(10)</span><span class="sxs-lookup"><span data-stu-id="cafe1-235">(10)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-236">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="cafe1-236">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="cafe1-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-237"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="cafe1-238">(11)</span><span class="sxs-lookup"><span data-stu-id="cafe1-238">(11)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-239">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-239">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="cafe1-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-240"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="cafe1-241">(12)</span><span class="sxs-lookup"><span data-stu-id="cafe1-241">(12)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-242">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="cafe1-242">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="cafe1-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-243"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="cafe1-244">(13)</span><span class="sxs-lookup"><span data-stu-id="cafe1-244">(13)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-245">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-245">Windows cannot verify the device resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="cafe1-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-246"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="cafe1-247">(14)</span><span class="sxs-lookup"><span data-stu-id="cafe1-247">(14)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-248">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-248">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="cafe1-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-249"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="cafe1-250">(15)</span><span class="sxs-lookup"><span data-stu-id="cafe1-250">(15)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-251">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="cafe1-251">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="cafe1-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-252"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="cafe1-253">(16)</span><span class="sxs-lookup"><span data-stu-id="cafe1-253">(16)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-254">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-254">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="cafe1-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-255"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="cafe1-256">(17)</span><span class="sxs-lookup"><span data-stu-id="cafe1-256">(17)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-257">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="cafe1-257">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cafe1-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-258"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="cafe1-259">(18)</span><span class="sxs-lookup"><span data-stu-id="cafe1-259">(18)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-260">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="cafe1-260">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="cafe1-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-261"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="cafe1-262">(19)</span><span class="sxs-lookup"><span data-stu-id="cafe1-262">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="cafe1-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-263"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="cafe1-264">(20)</span><span class="sxs-lookup"><span data-stu-id="cafe1-264">(20)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-265">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="cafe1-265">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="cafe1-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-266"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="cafe1-267">(21)</span><span class="sxs-lookup"><span data-stu-id="cafe1-267">(21)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-268">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="cafe1-268">System failure.</span></span> <span data-ttu-id="cafe1-269">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="cafe1-269">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="cafe1-270">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-270">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="cafe1-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-271"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="cafe1-272">(22)</span><span class="sxs-lookup"><span data-stu-id="cafe1-272">(22)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-273">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="cafe1-273">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="cafe1-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="cafe1-275">(23)</span><span class="sxs-lookup"><span data-stu-id="cafe1-275">(23)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-276">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="cafe1-276">System failure.</span></span> <span data-ttu-id="cafe1-277">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="cafe1-277">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="cafe1-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-278"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="cafe1-279">(24)</span><span class="sxs-lookup"><span data-stu-id="cafe1-279">(24)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-280">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="cafe1-280">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cafe1-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cafe1-282">(25)</span><span class="sxs-lookup"><span data-stu-id="cafe1-282">(25)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-283">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="cafe1-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="cafe1-285">(26)</span><span class="sxs-lookup"><span data-stu-id="cafe1-285">(26)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-286">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-286">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="cafe1-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-287"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="cafe1-288">(27)</span><span class="sxs-lookup"><span data-stu-id="cafe1-288">(27)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-289">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="cafe1-289">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="cafe1-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-290"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="cafe1-291">(28)</span><span class="sxs-lookup"><span data-stu-id="cafe1-291">(28)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-292">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="cafe1-292">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="cafe1-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-293"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="cafe1-294">(29)</span><span class="sxs-lookup"><span data-stu-id="cafe1-294">(29)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-295">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="cafe1-295">Device is disabled.</span></span> <span data-ttu-id="cafe1-296">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="cafe1-296">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="cafe1-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-297"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="cafe1-298">(30)</span><span class="sxs-lookup"><span data-stu-id="cafe1-298">(30)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-299">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="cafe1-299">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="cafe1-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="cafe1-300"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="cafe1-301">31</span><span class="sxs-lookup"><span data-stu-id="cafe1-301">(31)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-302">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="cafe1-302">Device is not working properly.</span></span> <span data-ttu-id="cafe1-303">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="cafe1-303">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe1-304">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="cafe1-304">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-305">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-307">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cafe1-307">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-308">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cafe1-308">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="cafe1-309">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-310">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cafe1-310">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-311">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-313">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cafe1-313">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-314">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="cafe1-314">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="cafe1-315">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="cafe1-315">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="cafe1-316">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-317">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cafe1-317">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-320">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="cafe1-320">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-321">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="cafe1-321">Description of the object.</span></span>

<span data-ttu-id="cafe1-322">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-322">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-323">**ID**</span><span class="sxs-lookup"><span data-stu-id="cafe1-323">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-326">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="cafe1-326">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-327">Identificador único del disco lógico desde otros dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="cafe1-327">Unique identifier of the logical disk from other devices on the system.</span></span>

<span data-ttu-id="cafe1-328">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cafe1-329">Para obtener un ejemplo de código que recupera esta propiedad, vea la sección Comentarios, más adelante.</span><span class="sxs-lookup"><span data-stu-id="cafe1-329">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-330">**DriveType**</span><span class="sxs-lookup"><span data-stu-id="cafe1-330">**DriveType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-331">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cafe1-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-333">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| FileFunctions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="cafe1-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|FileFunctions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-334">Valor numérico que corresponde al tipo de unidad de disco que representa este disco lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-334">Numeric value that corresponds to the type of disk drive this logical disk represents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cafe1-335">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cafe1-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Root_Directory"></span><span id="no_root_directory"></span><span id="NO_ROOT_DIRECTORY"></span>

<span data-ttu-id="cafe1-336">**No hay directorio raíz** (1)</span><span class="sxs-lookup"><span data-stu-id="cafe1-336">**No Root Directory** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Disk"></span><span id="removable_disk"></span><span id="REMOVABLE_DISK"></span>

<span data-ttu-id="cafe1-337">**Disco extraíble** (2)</span><span class="sxs-lookup"><span data-stu-id="cafe1-337">**Removable Disk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Disk"></span><span id="local_disk"></span><span id="LOCAL_DISK"></span>

<span data-ttu-id="cafe1-338">**Disco local** (3)</span><span class="sxs-lookup"><span data-stu-id="cafe1-338">**Local Disk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Drive"></span><span id="network_drive"></span><span id="NETWORK_DRIVE"></span>

<span data-ttu-id="cafe1-339">**Unidad de red** (4)</span><span class="sxs-lookup"><span data-stu-id="cafe1-339">**Network Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Compact_Disc"></span><span id="compact_disc"></span><span id="COMPACT_DISC"></span>

<span data-ttu-id="cafe1-340">**Disco compacto** (5)</span><span class="sxs-lookup"><span data-stu-id="cafe1-340">**Compact Disc** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM_Disk"></span><span id="ram_disk"></span><span id="RAM_DISK"></span>

<span data-ttu-id="cafe1-341">**Disco RAM** (6)</span><span class="sxs-lookup"><span data-stu-id="cafe1-341">**RAM Disk** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe1-342">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="cafe1-342">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-343">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-345">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="cafe1-345">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="cafe1-346">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-347">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cafe1-347">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-348">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-350">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="cafe1-350">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="cafe1-351">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-352">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="cafe1-352">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-355">Tipo de detección y corrección de errores admitidos por esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="cafe1-355">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="cafe1-356">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-356">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-357">**Systems**</span><span class="sxs-lookup"><span data-stu-id="cafe1-357">**FileSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-360">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="cafe1-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-361">Sistema de archivos en el disco lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-361">File system on the logical disk.</span></span>

<span data-ttu-id="cafe1-362">Ejemplo: "NTFS"</span><span class="sxs-lookup"><span data-stu-id="cafe1-362">Example: "NTFS"</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-363">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="cafe1-363">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-364">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cafe1-364">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-366">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="cafe1-366">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-367">Espacio, en bytes, disponible en el disco lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-367">Space, in bytes, available on the logical disk.</span></span>

<span data-ttu-id="cafe1-368">Esta propiedad se hereda del [**\_ LogicalDisk de CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-368">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="cafe1-369">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cafe1-369">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cafe1-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-371">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cafe1-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-373">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="cafe1-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-374">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="cafe1-374">Date and time the object was installed.</span></span> <span data-ttu-id="cafe1-375">Esta propiedad no requiere un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="cafe1-375">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cafe1-376">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-377">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cafe1-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-378">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cafe1-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-379">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-380">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="cafe1-381">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-382">**MaximumComponentLength**</span><span class="sxs-lookup"><span data-stu-id="cafe1-382">**MaximumComponentLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-383">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cafe1-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-385">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="cafe1-385">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-386">Longitud máxima de un componente de nombre de archivo compatible con la unidad de Windows.</span><span class="sxs-lookup"><span data-stu-id="cafe1-386">Maximum length of a filename component supported by the Windows drive.</span></span> <span data-ttu-id="cafe1-387">Un componente de nombre de archivo es la parte de un nombre de archivo entre barras diagonales inversas.</span><span class="sxs-lookup"><span data-stu-id="cafe1-387">A filename component is that portion of a filename between backslashes.</span></span> <span data-ttu-id="cafe1-388">El valor se puede usar para indicar que el sistema de archivos especificado admite nombres largos.</span><span class="sxs-lookup"><span data-stu-id="cafe1-388">The value can be used to indicate that long names are supported by the specified file system.</span></span> <span data-ttu-id="cafe1-389">Por ejemplo, para un sistema de archivos FAT que admite nombres largos, la función almacena el valor 255, en lugar del indicador 8,3 anterior.</span><span class="sxs-lookup"><span data-stu-id="cafe1-389">For example, for a FAT file system supporting long names, the function stores the value 255, rather than the previous 8.3 indicator.</span></span> <span data-ttu-id="cafe1-390">También se pueden admitir nombres largos en los sistemas que usan el sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="cafe1-390">Long names can also be supported on systems that use the NTFS file system.</span></span>

<span data-ttu-id="cafe1-391">Ejemplo: 255</span><span class="sxs-lookup"><span data-stu-id="cafe1-391">Example: 255</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-392">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="cafe1-392">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-393">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cafe1-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-395">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Device INPUT and Output Functions \| DeviceIoControl")</span><span class="sxs-lookup"><span data-stu-id="cafe1-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Functions\|DeviceIoControl")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-396">Tipo de medio actualmente presente en la unidad lógica.</span><span class="sxs-lookup"><span data-stu-id="cafe1-396">Type of media currently present in the logical drive.</span></span> <span data-ttu-id="cafe1-397">Este valor será uno de los valores de la \_ enumeración de tipo de medio definido en Winioctl. h.</span><span class="sxs-lookup"><span data-stu-id="cafe1-397">This value will be one of the values of the MEDIA\_TYPE enumeration defined in Winioctl.h.</span></span> <span data-ttu-id="cafe1-398">Es posible que el valor no sea exacto para unidades extraíbles si actualmente no hay ningún medio en la unidad.</span><span class="sxs-lookup"><span data-stu-id="cafe1-398">The value may not be exact for removable drives if currently there is no media in the drive.</span></span>

<dt>

<span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>

<span data-ttu-id="cafe1-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>El **formato es desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cafe1-399"><span id="Format_is_unknown"></span><span id="format_is_unknown"></span><span id="FORMAT_IS_UNKNOWN"></span>**Format is unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (1)</span><span class="sxs-lookup"><span data-stu-id="cafe1-400"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (1)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-401">Disquete de 5 1/2 pulgadas; 1,2 MB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-401">5 1/4-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (2)</span><span class="sxs-lookup"><span data-stu-id="cafe1-402"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (2)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-403">Disquete de 3 1/2 pulgadas; 1,44 MB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-403">3 1/2-Inch Floppy Disk - 1.44 MB -512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (3)</span><span class="sxs-lookup"><span data-stu-id="cafe1-404"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-405">Disquete de 3 1/2 pulgadas; 2,88 MB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-405">3 1/2-Inch Floppy Disk - 2.88 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (4)</span><span class="sxs-lookup"><span data-stu-id="cafe1-406"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-407">Disquete de 3 1/2 pulgadas; 20,8 MB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-407">3 1/2-Inch Floppy Disk - 20.8 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (5)</span><span class="sxs-lookup"><span data-stu-id="cafe1-408"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-409">Disquete de 3 1/2 pulgadas-720 KB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-409">3 1/2-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (6)</span><span class="sxs-lookup"><span data-stu-id="cafe1-410"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-411">Disquete de 5 1/2 pulgadas-360 KB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-411">5 1/4-Inch Floppy Disk - 360 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (7)</span><span class="sxs-lookup"><span data-stu-id="cafe1-412"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-413">Disquete de 5 1/2 pulgadas-320 KB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-413">5 1/4-Inch Floppy Disk - 320 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (8)</span><span class="sxs-lookup"><span data-stu-id="cafe1-414"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (8)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-415">Disquete de 5 1/2 pulgadas-320 KB-1024 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-415">5 1/4-Inch Floppy Disk - 320 KB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (9)</span><span class="sxs-lookup"><span data-stu-id="cafe1-416"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (9)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-417">Disquete de 5 1/2 pulgadas-180 KB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-417">5 1/4-Inch Floppy Disk - 180 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (10)</span><span class="sxs-lookup"><span data-stu-id="cafe1-418"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (10)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-419">Disquete de 5 1/2 pulgadas-160 KB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-419">5 1/4-Inch Floppy Disk - 160 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>

<span data-ttu-id="cafe1-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Medio extraíble distinto de disquete** (11)</span><span class="sxs-lookup"><span data-stu-id="cafe1-420"><span id="Removable_media_other_than_floppy"></span><span id="removable_media_other_than_floppy"></span><span id="REMOVABLE_MEDIA_OTHER_THAN_FLOPPY"></span>**Removable media other than floppy** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>

<span data-ttu-id="cafe1-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Medio de disco duro fijo** (12)</span><span class="sxs-lookup"><span data-stu-id="cafe1-421"><span id="Fixed_hard_disk_media"></span><span id="fixed_hard_disk_media"></span><span id="FIXED_HARD_DISK_MEDIA"></span>**Fixed hard disk media** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (13)</span><span class="sxs-lookup"><span data-stu-id="cafe1-422"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (13)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-423">Disquete de 3 1/2 pulgadas; 120 MB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-423">3 1/2-Inch Floppy Disk - 120 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (14)</span><span class="sxs-lookup"><span data-stu-id="cafe1-424"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (14)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-425">Disquete de 3 1/2 pulgadas-640 KB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-425">3 1/2-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (15)</span><span class="sxs-lookup"><span data-stu-id="cafe1-426"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (15)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-427">Disquete de 5 1/2 pulgadas-640 KB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-427">5 1/4-Inch Floppy Disk - 640 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (16)</span><span class="sxs-lookup"><span data-stu-id="cafe1-428"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (16)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-429">Disquete de 5 1/2 pulgadas-720 KB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-429">5 1/4-Inch Floppy Disk - 720 KB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (17)</span><span class="sxs-lookup"><span data-stu-id="cafe1-430"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (17)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-431">Disquete de 3 1/2 pulgadas; 1,2 MB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-431">3 1/2-Inch Floppy Disk - 1.2 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (18)</span><span class="sxs-lookup"><span data-stu-id="cafe1-432"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (18)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-433">Disquete de 3 1/2 pulgadas; 1,23 MB-1024 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-433">3 1/2-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**disquete de 5 pulgadas** (19)</span><span class="sxs-lookup"><span data-stu-id="cafe1-434"><span id="5_-Inch_Floppy_Disk"></span><span id="5_-inch_floppy_disk"></span><span id="5_-INCH_FLOPPY_DISK"></span>**5 -Inch Floppy Disk** (19)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-435">Disquete de 5 1/2 pulgadas; 1,23 MB-1024 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-435">5 1/4-Inch Floppy Disk - 1.23 MB - 1024 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (20)</span><span class="sxs-lookup"><span data-stu-id="cafe1-436"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (20)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-437">Disquete de 3 1/2 pulgadas; 128 MB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-437">3 1/2-Inch Floppy Disk - 128 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**disquete de 3 pulgadas** (21)</span><span class="sxs-lookup"><span data-stu-id="cafe1-438"><span id="3_-Inch_Floppy_Disk"></span><span id="3_-inch_floppy_disk"></span><span id="3_-INCH_FLOPPY_DISK"></span>**3 -Inch Floppy Disk** (21)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-439">Disquete de 3 1/2 pulgadas; 230 MB-512 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-439">3 1/2-Inch Floppy Disk - 230 MB - 512 bytes/sector</span></span>

</dd> <dt>

<span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>

<span data-ttu-id="cafe1-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**disquete de 8 pulgadas** (22)</span><span class="sxs-lookup"><span data-stu-id="cafe1-440"><span id="8-Inch_Floppy_Disk"></span><span id="8-inch_floppy_disk"></span><span id="8-INCH_FLOPPY_DISK"></span>**8-Inch Floppy Disk** (22)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-441">Disquete de 8 pulgadas-256 KB-128 bytes/sector</span><span class="sxs-lookup"><span data-stu-id="cafe1-441">8-Inch Floppy Disk - 256 KB - 128 bytes/sector</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe1-442">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="cafe1-442">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-445">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cafe1-445">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-446">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="cafe1-446">Label by which the object is known.</span></span> <span data-ttu-id="cafe1-447">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="cafe1-447">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cafe1-448">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-448">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-449">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="cafe1-449">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-450">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cafe1-450">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-452">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="cafe1-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-453">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="cafe1-453">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="cafe1-454">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="cafe1-454">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="cafe1-455">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="cafe1-455">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="cafe1-456">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-456">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="cafe1-457">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="cafe1-457">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-458">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="cafe1-458">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-459">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-461">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="cafe1-461">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-462">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-462">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="cafe1-463">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cafe1-464">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="cafe1-464">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-465">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="cafe1-465">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-466">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cafe1-466">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-467">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-468">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-468">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="cafe1-469">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="cafe1-469">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cafe1-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cafe1-470"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="cafe1-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="cafe1-471"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cafe1-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="cafe1-472"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cafe1-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="cafe1-473"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-474">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="cafe1-474">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="cafe1-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="cafe1-475"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-476">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="cafe1-476">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="cafe1-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="cafe1-477"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-478">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="cafe1-478">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="cafe1-479">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="cafe1-479">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="cafe1-480">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="cafe1-480">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="cafe1-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="cafe1-481"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-482">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="cafe1-482">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="cafe1-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="cafe1-483"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="cafe1-484">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="cafe1-484">Timed Power-On Supported</span></span>

<span data-ttu-id="cafe1-485">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="cafe1-485">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe1-486">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="cafe1-486">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-487">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-487">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-488">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-489">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="cafe1-489">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="cafe1-490">Esta propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="cafe1-490">This property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="cafe1-491">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-492">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="cafe1-492">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-493">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-494">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-495">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| funciones de red de Windows \| WNetGetConnection")</span><span class="sxs-lookup"><span data-stu-id="cafe1-495">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows Networking Functions\|WNetGetConnection")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-496">Ruta de acceso de red al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-496">Network path to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-497">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="cafe1-497">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-498">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-500">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="cafe1-500">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="cafe1-501">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-501">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-502">**QuotasDisabled**</span><span class="sxs-lookup"><span data-stu-id="cafe1-502">**QuotasDisabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-503">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-504">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-505">Indica que la administración de cuotas no está habilitada (TRUE) en este sistema.</span><span class="sxs-lookup"><span data-stu-id="cafe1-505">Indicates that quota management is not enabled (TRUE) on this system.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-506">**QuotasIncomplete**</span><span class="sxs-lookup"><span data-stu-id="cafe1-506">**QuotasIncomplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-507">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-507">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-508">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-509">Indica que se ha utilizado la administración de cuotas pero se ha deshabilitado (**true**).</span><span class="sxs-lookup"><span data-stu-id="cafe1-509">Indicates that the quota management was used but has been disabled (**True**).</span></span> <span data-ttu-id="cafe1-510">Incompleto hace referencia a la información que queda en el sistema de archivos una vez deshabilitada la administración de cuotas.</span><span class="sxs-lookup"><span data-stu-id="cafe1-510">Incomplete refers to the information left in the file system after quota management was disabled.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-511">**QuotasRebuilding**</span><span class="sxs-lookup"><span data-stu-id="cafe1-511">**QuotasRebuilding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-512">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-512">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-514">Si es **true**, indica que el sistema de archivos está en el proceso activo de compilar información y configurar el disco para la administración de cuotas.</span><span class="sxs-lookup"><span data-stu-id="cafe1-514">If **True**, indicates that the file system is in the active process of compiling information and setting the disk up for quota management.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-515">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="cafe1-515">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-516">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-517">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-518">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="cafe1-518">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-519">Tamaño de la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="cafe1-519">Size of the disk drive.</span></span>

<span data-ttu-id="cafe1-520">Esta propiedad se hereda del [**\_ LogicalDisk de CIM**](cim-logicaldisk.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-520">This property is inherited from [**CIM\_LogicalDisk**](cim-logicaldisk.md).</span></span>

<span data-ttu-id="cafe1-521">Para obtener un ejemplo de código que recupera esta propiedad, vea la sección Comentarios, más adelante.</span><span class="sxs-lookup"><span data-stu-id="cafe1-521">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-522">**Estado**</span><span class="sxs-lookup"><span data-stu-id="cafe1-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-525">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cafe1-525">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-526">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="cafe1-526">Current status of the object.</span></span> <span data-ttu-id="cafe1-527">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="cafe1-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="cafe1-528">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="cafe1-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="cafe1-529">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="cafe1-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cafe1-530">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cafe1-531">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="cafe1-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cafe1-532">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cafe1-533">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cafe1-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cafe1-534">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="cafe1-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cafe1-535">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="cafe1-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cafe1-536">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="cafe1-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cafe1-537">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="cafe1-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cafe1-538">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="cafe1-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cafe1-539">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="cafe1-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cafe1-540">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="cafe1-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cafe1-541">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="cafe1-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cafe1-542">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="cafe1-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cafe1-543">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="cafe1-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cafe1-544">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="cafe1-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cafe1-545">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="cafe1-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe1-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cafe1-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-547">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cafe1-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-548">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-549">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="cafe1-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-550">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-550">State of the logical device.</span></span> <span data-ttu-id="cafe1-551">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="cafe1-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="cafe1-552">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cafe1-553">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="cafe1-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cafe1-554">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="cafe1-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="cafe1-555">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="cafe1-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="cafe1-556">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="cafe1-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="cafe1-557">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="cafe1-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cafe1-558">**SupportsDiskQuotas**</span><span class="sxs-lookup"><span data-stu-id="cafe1-558">**SupportsDiskQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-559">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-559">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-560">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-560">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-561">Si **es true**, este volumen admite cuotas de disco.</span><span class="sxs-lookup"><span data-stu-id="cafe1-561">If **True**, this volume supports disk quotas.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-562">**SupportsFileBasedCompression**</span><span class="sxs-lookup"><span data-stu-id="cafe1-562">**SupportsFileBasedCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-563">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-564">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-565">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions \| [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa) \| FS \_ file \_ compression")</span><span class="sxs-lookup"><span data-stu-id="cafe1-565">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions\|[**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa)\|FS\_FILE\_COMPRESSION")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-566">Si es **true**, la partición de disco lógico admite la compresión basada en archivos, como es el caso del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="cafe1-566">If **True**, the logical disk partition supports file-based compression, such as is the case with the NTFS file system.</span></span> <span data-ttu-id="cafe1-567">Esta propiedad es **false** cuando la propiedad **Compressed** es **true**.</span><span class="sxs-lookup"><span data-stu-id="cafe1-567">This property is **False** when the **Compressed** property is **True**.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-568">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cafe1-568">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-569">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-569">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-570">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-570">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-571">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cafe1-571">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-572">Valor de la propiedad de ámbito de equipo de **CreationClassName** .</span><span class="sxs-lookup"><span data-stu-id="cafe1-572">Value of the scoping computer **CreationClassName** property.</span></span>

<span data-ttu-id="cafe1-573">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-573">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-574">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cafe1-574">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-575">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-575">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-576">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-577">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cafe1-577">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-578">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="cafe1-578">Name of the scoping system.</span></span>

<span data-ttu-id="cafe1-579">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-579">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-580">**VolumeDirty**</span><span class="sxs-lookup"><span data-stu-id="cafe1-580">**VolumeDirty**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-581">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cafe1-581">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-582">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-582">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-583">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL \_ está \_ sucio por volumen \_ ")</span><span class="sxs-lookup"><span data-stu-id="cafe1-583">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FSCTL\_IS\_VOLUME\_DIRTY")</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-584">Si **es true**, el disco requiere que [**CHKDSK**](chkdsk-method-in-class-win32-logicaldisk.md) se ejecute en el siguiente reinicio.</span><span class="sxs-lookup"><span data-stu-id="cafe1-584">If **True**, the disk requires [**ChkDsk**](chkdsk-method-in-class-win32-logicaldisk.md) to be run at the next restart.</span></span> <span data-ttu-id="cafe1-585">Esta propiedad solo es aplicable a las instancias de disco lógico que representan un disco físico en el equipo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-585">This property is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="cafe1-586">No es aplicable a las unidades lógicas asignadas.</span><span class="sxs-lookup"><span data-stu-id="cafe1-586">It is not applicable to mapped logical drives.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-587">**VolumeName**</span><span class="sxs-lookup"><span data-stu-id="cafe1-587">**VolumeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-588">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-589">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cafe1-589">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-590">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="cafe1-590">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-591">Nombre del volumen del disco lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-591">Volume name of the logical disk.</span></span>

<span data-ttu-id="cafe1-592">Restricciones: máximo 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cafe1-592">Constraints: Maximum 32 characters.</span></span>

<span data-ttu-id="cafe1-593">Para obtener un ejemplo de código que recupera esta propiedad, vea la sección Comentarios, más adelante.</span><span class="sxs-lookup"><span data-stu-id="cafe1-593">For a code example that retrieves this property, see the Remarks section, below.</span></span>

</dd> <dt>

<span data-ttu-id="cafe1-594">**VolumeSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="cafe1-594">**VolumeSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cafe1-595">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cafe1-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-596">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cafe1-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cafe1-597">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span><span class="sxs-lookup"><span data-stu-id="cafe1-597">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File System Functions [**GetVolumeInformation**](/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa))</span></span>
</dt> </dl>

<span data-ttu-id="cafe1-598">Número de serie del volumen del disco lógico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-598">Volume serial number of the logical disk.</span></span>

<span data-ttu-id="cafe1-599">Restricciones: máximo de 11 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cafe1-599">Constraints: Maximum 11 characters.</span></span>

<span data-ttu-id="cafe1-600">Ejemplo: "A8C3-D032"</span><span class="sxs-lookup"><span data-stu-id="cafe1-600">Example: "A8C3-D032"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cafe1-601">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cafe1-601">Remarks</span></span>

<span data-ttu-id="cafe1-602">La clase **Win32 \_ LogicalDisk** se deriva del [**\_ LogicalDisk de CIM**](cim-logicaldisk.md) que deriva de [**CIM \_ StorageExtent**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-602">The **Win32\_LogicalDisk** class is derived from [**CIM\_LogicalDisk**](cim-logicaldisk.md) which derives from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="cafe1-603">La **clase \_ StorageExtent de CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="cafe1-603">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="cafe1-604">Una unidad de disco física es la piedra angular de cualquier sistema de administración de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="cafe1-604">A physical disk drive is the cornerstone of any storage management system.</span></span> <span data-ttu-id="cafe1-605">Sin embargo, una vez instalada una unidad de disco física, ni los usuarios ni los administradores del sistema suelen tratar directamente con el hardware.</span><span class="sxs-lookup"><span data-stu-id="cafe1-605">However, after a physical disk drive has been installed, neither users nor system administrators typically deal with the hardware directly.</span></span> <span data-ttu-id="cafe1-606">En su lugar, los usuarios y los administradores del sistema interactúan con las unidades lógicas que se han creado en el disco.</span><span class="sxs-lookup"><span data-stu-id="cafe1-606">Instead, both users and system administrators interact with the logical drives that have been created on the disk.</span></span>

<span data-ttu-id="cafe1-607">Una unidad lógica es una subdivisión de una partición a la que se le ha asignado su propia letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="cafe1-607">A logical drive is a subdivision of a partition that has been assigned its own drive letter.</span></span> <span data-ttu-id="cafe1-608">(Es posible tener una partición a la que no se le haya asignado una letra de unidad). Al hablar acerca de la unidad C o D, se hace referencia a una unidad lógica en lugar de a una unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="cafe1-608">(It is possible to have a partition that has not been assigned a drive letter.) When you talk about drive C or drive D, you are referring to a logical drive rather than to a physical disk drive.</span></span> <span data-ttu-id="cafe1-609">Del mismo modo, al guardar un documento en la unidad E, lo guarda en la unidad lógica.</span><span class="sxs-lookup"><span data-stu-id="cafe1-609">Likewise, when you save a document to drive E, you are saving it to the logical drive.</span></span> <span data-ttu-id="cafe1-610">Los discos físicos componen el hardware que conforma una unidad, incluidos tales componentes como cabezales, sectores y cilindros.</span><span class="sxs-lookup"><span data-stu-id="cafe1-610">Physical disks compose the hardware that makes up a drive, including such components as heads, sectors, and cylinders.</span></span> <span data-ttu-id="cafe1-611">Por el contrario, las unidades lógicas tienen propiedades como el espacio en disco, el espacio disponible en disco y las letras de unidad.</span><span class="sxs-lookup"><span data-stu-id="cafe1-611">Logical drives, by contrast, have properties such as disk space, available disk space, and drive letters.</span></span>

> [!Note]  
> <span data-ttu-id="cafe1-612">La clase **Win32 \_ LogicalDisk** solo se puede usar para enumerar las propiedades de las unidades de disco locales.</span><span class="sxs-lookup"><span data-stu-id="cafe1-612">The **Win32\_LogicalDisk** class can be used only to enumerate the properties of local disk drives.</span></span> <span data-ttu-id="cafe1-613">Sin embargo, puede usar la clase [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md) para enumerar las propiedades de las unidades de red asignadas.</span><span class="sxs-lookup"><span data-stu-id="cafe1-613">However, you can use the [**Win32\_MappedLogicalDisk**](win32-mappedlogicaldisk.md) class to enumerate the properties of mapped network drives.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cafe1-614">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cafe1-614">Examples</span></span>

<span data-ttu-id="cafe1-615">Puede encontrar otros ejemplos con el **\_ LogicalDisk de Win32** para obtener datos de disco o volumen en el tema [tareas de WMI: discos y sistemas de archivos](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) .</span><span class="sxs-lookup"><span data-stu-id="cafe1-615">You can find other examples using **Win32\_LogicalDisk** to obtain disk or volume data in the [WMI Tasks: Disks and File Systems](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems) topic.</span></span>

<span data-ttu-id="cafe1-616">El ejemplo de código VBScript del administrador de [información WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) de la galería de TechNet utiliza la clase **Win32 \_ LogicalDisk** para recuperar información de hardware de varios equipos remotos.</span><span class="sxs-lookup"><span data-stu-id="cafe1-616">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_LogicalDisk** class to retrieve hardware information from a number of remote computers.</span></span>

<span data-ttu-id="cafe1-617">La [información de obtención de disco mediante WMI/CIM..](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) . En el ejemplo de código de PowerShell de la galería de TechNet se usa el **\_ LogicalDisk de Win32** para recuperar **DeviceID**, **NombreDeVolumen** y **el tamaño** de un dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="cafe1-617">The [Get Disk info using wmi/cim...](https://Gallery.TechNet.Microsoft.Com/Get-Disk-info-using-wmicim-ff0bd352) PowerShell code example on the TechNet Gallery uses **Win32\_LogicalDisk** to retrieve **DeviceID**, **VolumeName**, and **Size** from a target device.</span></span> <span data-ttu-id="cafe1-618">En concreto, este ejemplo incluye un control riguroso de las excepciones y devuelve un solo objeto por equipo, en lugar de por disco.</span><span class="sxs-lookup"><span data-stu-id="cafe1-618">In particular, this sample includes rigorous exception handling, and returns a single object per computer, rather than per disk.</span></span>

<span data-ttu-id="cafe1-619">El scripting empresarial suele implicar la configuración de hardware y software en equipos remotos. a su vez, esto requiere que sepa, de antemano, el tipo de unidades de disco instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-619">Enterprise scripting often involves configuring hardware and software on remote computers; in turn, this requires you to know, in advance, the type of disk drives installed on a computer.</span></span> <span data-ttu-id="cafe1-620">Por ejemplo, un script que instala una aplicación en la unidad E solo funciona si la unidad E es un disco duro.</span><span class="sxs-lookup"><span data-stu-id="cafe1-620">For example, a script that installs an application on drive E works only if drive E is a hard disk.</span></span> <span data-ttu-id="cafe1-621">Si la unidad E representa un disquete o una unidad de CD-ROM, el script produce un error.</span><span class="sxs-lookup"><span data-stu-id="cafe1-621">If drive E happens to represent a floppy disk or a CD-ROM drive, the script fails.</span></span> <span data-ttu-id="cafe1-622">En el código siguiente se identifican las unidades y los tipos de unidad instalados en un equipo</span><span class="sxs-lookup"><span data-stu-id="cafe1-622">The following code identifies the drives and drive types installed on a computer</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk")
For Each objDisk in colDisks
 Wscript.Echo "DeviceID: "& objDisk.DeviceID 
 Select Case objDisk.DriveType
 Case 1
 Wscript.Echo "No root directory."
 Case 2
 Wscript.Echo "DriveType: Removable drive."
 Case 3
 Wscript.Echo "DriveType: Local hard disk."
 Case 4
 Wscript.Echo "DriveType: Network disk." 
 Case 5
 Wscript.Echo "DriveType: Compact disk." 
 Case 6
 Wscript.Echo "DriveType: RAM disk." 
 Case Else
 Wscript.Echo "Drive type could not be determined."
 End Select
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...
{
   string strComputer = &quot;.&quot;;
            
   ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
   ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk&quot;);
   ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
   ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

   foreach (ManagementObject objDisk in colDisks)
   {
      Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
                
      switch ((uint)(objDisk[&quot;DriveType&quot;]))
      {
         case 1: {   Console.WriteLine(&quot;No root directory.&quot;);
                     break;}
         case 2: {   Console.WriteLine(&quot;DriveType: Removable drive.&quot;); 
                     break;}
         case 3: {   Console.WriteLine(&quot;DriveType: Local hard disk.&quot;);
                     break;}
         case 4: {   Console.WriteLine(&quot;DriveType: Network disk.&quot;);
                     break;}
         case 5: {   Console.WriteLine(&quot;DriveType: Compact disk.&quot;);
                     break;}
         case 6: {   Console.WriteLine(&quot;DriveType: RAM disk.&quot;);
                     break;}
         default: {  Console.WriteLine(&quot;Drive type could not be determined.&quot;);
                     break;}
      }
      //Readline is in here so the user can see the result before the code exists
      Console.ReadLine();
   }
}
```





<span data-ttu-id="cafe1-623">Los ejemplos siguientes enumeran el espacio disponible en todas las unidades de disco duro de un equipo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-623">The following samples enumerate the free space on all the hard disk drives on a computer.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("SELECT * FROM Win32_LogicalDisk WHERE DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
 Wscript.Echo "Device ID: " & objDisk.DeviceID 
 Wscript.Echo "Free Disk Space: " & objDisk.FreeSpace
Next
```


```CSharp

//be sure to References->Add->System.Management to your project
using System.Management;
...

const int HARD_DISK = 3;
string strComputer = &quot;.&quot;;

ManagementScope namespaceScope = new ManagementScope(&quot;\\\\&quot; + strComputer + &quot;\\ROOT\\CIMV2&quot;);
ObjectQuery diskQuery = new ObjectQuery(&quot;SELECT * FROM Win32_LogicalDisk WHERE DriveType = &quot; + HARD_DISK + &quot;&quot;);
ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher(namespaceScope, diskQuery);
ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

foreach (ManagementObject objDisk in colDisks)
{
    Console.WriteLine(&quot;Device ID : {0}&quot;, objDisk[&quot;DeviceID&quot;]);
    Console.WriteLine(&quot;Free Disk Space : {0}&quot;, objDisk[&quot;FreeSpace&quot;]);
    Console.ReadLine();
}
```





<span data-ttu-id="cafe1-624">En el ejemplo de código siguiente se devuelve el tipo de sistema de archivos (FAT, NTFS, FAT32, etc.) que se usa en cada unidad de un equipo.</span><span class="sxs-lookup"><span data-stu-id="cafe1-624">The following code example returns the type of file system (FAT, NTFS, FAT32, and so on) used on each drive in a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
    Wscript.Echo "DeviceID: "& vbTab &  objDisk.DeviceID  
    Wscript.Echo "File System: "& vbTab & objDisk.FileSystem
Next
```


```PowerShell

Get-WMIObject Win32_LogicalDisk | Select DeviceID, FileSystem | Format=Table -AutoSize
```





<span data-ttu-id="cafe1-625">El siguiente ejemplo de código de PowerShell recupera información adicional sobre los discos locales lógicos.</span><span class="sxs-lookup"><span data-stu-id="cafe1-625">The following PowerShell code sample retrieves additional information about the logical local disks.</span></span>


```PowerShell
Write-Host "Drive information for $env:ComputerName"

Get-WmiObject -Class Win32_LogicalDisk |
    Where-Object {$_.DriveType -ne 5} |
    Sort-Object -Property Name | 
    Select-Object Name, VolumeName, FileSystem, Description, VolumeDirty, `
        @{"Label"="DiskSize(GB)";"Expression"={"{0:N}" -f ($_.Size/1GB) -as [float]}}, `
        @{"Label"="FreeSpace(GB)";"Expression"={"{0:N}" -f ($_.FreeSpace/1GB) -as [float]}}, `
        @{"Label"="%Free";"Expression"={"{0:N}" -f ($_.FreeSpace/$_.Size*100) -as [float]}} |
    Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="cafe1-626">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cafe1-626">Requirements</span></span>



| <span data-ttu-id="cafe1-627">Requisito</span><span class="sxs-lookup"><span data-stu-id="cafe1-627">Requirement</span></span> | <span data-ttu-id="cafe1-628">Value</span><span class="sxs-lookup"><span data-stu-id="cafe1-628">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cafe1-629">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cafe1-629">Minimum supported client</span></span><br/> | <span data-ttu-id="cafe1-630">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cafe1-630">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cafe1-631">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cafe1-631">Minimum supported server</span></span><br/> | <span data-ttu-id="cafe1-632">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cafe1-632">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cafe1-633">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cafe1-633">Namespace</span></span><br/>                | <span data-ttu-id="cafe1-634">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cafe1-634">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cafe1-635">MOF</span><span class="sxs-lookup"><span data-stu-id="cafe1-635">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cafe1-636"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cafe1-636"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cafe1-637">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cafe1-637">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cafe1-638"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cafe1-638"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cafe1-639">Vea también</span><span class="sxs-lookup"><span data-stu-id="cafe1-639">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cafe1-640">**LogicalDisk de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="cafe1-640">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="cafe1-641">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="cafe1-641">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cafe1-642">Tareas de WMI: discos y sistemas de archivos</span><span class="sxs-lookup"><span data-stu-id="cafe1-642">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

