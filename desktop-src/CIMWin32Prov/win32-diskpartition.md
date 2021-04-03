---
description: Representa las capacidades y la capacidad de administración de un área con particiones de un disco físico en un equipo que ejecuta Windows.
ms.assetid: 7e78be3f-bae4-4374-abbf-7c4e63ba7593
ms.tgt_platform: multiple
title: Win32_DiskPartition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition
- Win32_DiskPartition.AdditionalAvailability
- Win32_DiskPartition.Availability
- Win32_DiskPartition.PowerManagementCapabilities
- Win32_DiskPartition.IdentifyingDescriptions
- Win32_DiskPartition.MaxQuiesceTime
- Win32_DiskPartition.OtherIdentifyingInfo
- Win32_DiskPartition.StatusInfo
- Win32_DiskPartition.PowerOnHours
- Win32_DiskPartition.TotalPowerOnHours
- Win32_DiskPartition.Access
- Win32_DiskPartition.BlockSize
- Win32_DiskPartition.Bootable
- Win32_DiskPartition.BootPartition
- Win32_DiskPartition.Caption
- Win32_DiskPartition.ConfigManagerErrorCode
- Win32_DiskPartition.ConfigManagerUserConfig
- Win32_DiskPartition.CreationClassName
- Win32_DiskPartition.Description
- Win32_DiskPartition.DeviceID
- Win32_DiskPartition.DiskIndex
- Win32_DiskPartition.ErrorCleared
- Win32_DiskPartition.ErrorDescription
- Win32_DiskPartition.ErrorMethodology
- Win32_DiskPartition.HiddenSectors
- Win32_DiskPartition.Index
- Win32_DiskPartition.InstallDate
- Win32_DiskPartition.LastErrorCode
- Win32_DiskPartition.Name
- Win32_DiskPartition.NumberOfBlocks
- Win32_DiskPartition.PNPDeviceID
- Win32_DiskPartition.PowerManagementSupported
- Win32_DiskPartition.PrimaryPartition
- Win32_DiskPartition.Purpose
- Win32_DiskPartition.RewritePartition
- Win32_DiskPartition.Size
- Win32_DiskPartition.StartingOffset
- Win32_DiskPartition.Status
- Win32_DiskPartition.SystemCreationClassName
- Win32_DiskPartition.SystemName
- Win32_DiskPartition.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4f9a9c16f58d0119c8027848c481479985e7505e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907420"
---
# <a name="win32_diskpartition-class"></a><span data-ttu-id="26d10-103">\_Clase Win32 DiskPartition</span><span class="sxs-lookup"><span data-stu-id="26d10-103">Win32\_DiskPartition class</span></span>

<span data-ttu-id="26d10-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskPartition de Win32** representa las capacidades y la capacidad de administración de un área con particiones de un disco físico en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="26d10-104">The **Win32\_DiskPartition** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a partitioned area of a physical disk on a computer system running Windows.</span></span> <span data-ttu-id="26d10-105">Ejemplo: disco \# 0, partición \# 1.</span><span class="sxs-lookup"><span data-stu-id="26d10-105">Example: Disk \#0, Partition \#1.</span></span>

<span data-ttu-id="26d10-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="26d10-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="26d10-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="26d10-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d10-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26d10-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskPartition : CIM_DiskPartition
{
  unit16   AdditionalAvailability;
  uint16   Availability;
  uint16   PowerManagementCapabilities[];
  string   IdentifyingDescriptions[1];
  uint64   MaxQuiesceTime;
  uint64   OtherIdentifyingInfo;
  uint16   StatusInfo;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  uint16   Access;
  uint64   BlockSize;
  boolean  Bootable;
  boolean  BootPartition;
  string.  Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string.  CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DiskIndex;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   HiddenSectors;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  boolean  RewritePartition;
  uint64   Size;
  uint64   StartingOffset;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   Type;
};
```

## <a name="members"></a><span data-ttu-id="26d10-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="26d10-109">Members</span></span>

<span data-ttu-id="26d10-110">La **clase \_ DiskPartition de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="26d10-110">The **Win32\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="26d10-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="26d10-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="26d10-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26d10-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="26d10-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="26d10-113">Methods</span></span>

<span data-ttu-id="26d10-114">La clase **Win32 \_ DiskPartition** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="26d10-114">The **Win32\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="26d10-115">Método</span><span class="sxs-lookup"><span data-stu-id="26d10-115">Method</span></span>                                                     | <span data-ttu-id="26d10-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="26d10-116">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26d10-117">**Reset**</span><span class="sxs-lookup"><span data-stu-id="26d10-117">**Reset**</span></span>](win32-diskpartition-reset.md)                 | <span data-ttu-id="26d10-118">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="26d10-118">Requests a reset of the logical device.</span></span><br/>                                                            |
| [<span data-ttu-id="26d10-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="26d10-119">**SetPowerState**</span></span>](win32-diskpartition-setpowerstate.md) | <span data-ttu-id="26d10-120">Establece el estado de energía deseado para un dispositivo lógico y el momento en que se debe colocar un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="26d10-120">Sets the desired power state for a logical device and when a device should be put into that state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="26d10-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26d10-121">Properties</span></span>

<span data-ttu-id="26d10-122">La **clase \_ DiskPartition de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="26d10-122">The **Win32\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26d10-123">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="26d10-123">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-124">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26d10-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-126">Acceso a medios disponible.</span><span class="sxs-lookup"><span data-stu-id="26d10-126">Media access available.</span></span>

<span data-ttu-id="26d10-127">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-127">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26d10-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="26d10-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="26d10-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="26d10-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="26d10-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="26d10-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-131">Editable</span><span class="sxs-lookup"><span data-stu-id="26d10-131">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="26d10-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="26d10-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="26d10-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="26d10-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26d10-134">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="26d10-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-135">Tipo de datos: **unit16**</span><span class="sxs-lookup"><span data-stu-id="26d10-135">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-136">Tipo de acceso: solo escritura</span><span class="sxs-lookup"><span data-stu-id="26d10-136">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-137">Disponibilidad adicional y estado del dispositivo, más allá de lo especificado en la propiedad Availability.</span><span class="sxs-lookup"><span data-stu-id="26d10-137">Additional availability and status of the Device, beyond that specified in the Availability property.</span></span> <span data-ttu-id="26d10-138">La propiedad **Availability** denota el estado principal y la disponibilidad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26d10-138">The **Availability** property denotes the primary status and availability of the Device.</span></span> <span data-ttu-id="26d10-139">En algunos casos, esto no será suficiente para indicar el estado completo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26d10-139">In some cases, this will not be sufficient to denote the complete status of the Device.</span></span> <span data-ttu-id="26d10-140">En esos casos, la propiedad **AdditionalAvailability** se puede usar para proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="26d10-140">In those cases, the **AdditionalAvailability** property can be used to provide further information.</span></span> <span data-ttu-id="26d10-141">Por ejemplo, la **disponibilidad** principal de un dispositivo puede estar fuera de línea (valor = 8), pero también puede estar en un estado de baja energía (valor de **AdditonalAvailability** = 14) o el dispositivo puede estar ejecutando diagnósticos (valor de **AdditionalAvailability** = 5, en pruebas). "</span><span class="sxs-lookup"><span data-stu-id="26d10-141">For example, a Device's primary **Availability** may be Off line (value=8), but it may also be in a low power state (**AdditonalAvailability** value=14), or the Device could be running Diagnostics (**AdditionalAvailability** value=5, In Test)."</span></span>

<span data-ttu-id="26d10-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26d10-143">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="26d10-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26d10-144">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="26d10-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="26d10-145">En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="26d10-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="26d10-146">**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="26d10-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="26d10-147">**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="26d10-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="26d10-148">**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="26d10-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="26d10-149">**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="26d10-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="26d10-150">Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="26d10-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="26d10-151">**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="26d10-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="26d10-152">**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="26d10-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="26d10-153">**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="26d10-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="26d10-154">**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="26d10-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="26d10-155">Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="26d10-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="26d10-156">Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="26d10-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="26d10-157">Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="26d10-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="26d10-158">**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="26d10-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="26d10-159">Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="26d10-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="26d10-160">En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="26d10-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="26d10-161">**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="26d10-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="26d10-162">**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="26d10-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="26d10-163">Modo **inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="26d10-163">**Quiesce** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26d10-164">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="26d10-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26d10-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-167">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="26d10-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-168">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26d10-168">Availability and status of the device.</span></span>

<span data-ttu-id="26d10-169">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-169">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26d10-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="26d10-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26d10-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="26d10-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="26d10-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="26d10-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="26d10-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="26d10-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="26d10-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="26d10-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="26d10-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="26d10-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="26d10-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="26d10-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="26d10-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="26d10-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="26d10-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="26d10-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="26d10-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="26d10-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="26d10-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="26d10-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="26d10-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="26d10-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="26d10-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="26d10-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-183">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="26d10-183">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="26d10-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="26d10-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-185">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="26d10-185">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="26d10-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="26d10-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-187">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="26d10-187">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="26d10-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="26d10-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="26d10-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="26d10-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-190">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="26d10-190">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="26d10-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="26d10-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-192">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="26d10-192">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="26d10-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="26d10-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-194">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="26d10-194">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="26d10-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="26d10-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-196">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="26d10-196">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="26d10-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="26d10-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-198">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="26d10-198">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="26d10-199">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="26d10-199">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-200">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26d10-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-202">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="26d10-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-203">Tamaño en bytes de los bloques que forman esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="26d10-203">Size in bytes of the blocks which form this storage extent.</span></span> <span data-ttu-id="26d10-204">Si es desconocido o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1.</span><span class="sxs-lookup"><span data-stu-id="26d10-204">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="26d10-205">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="26d10-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="26d10-206">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-207">**Ejecutable**</span><span class="sxs-lookup"><span data-stu-id="26d10-207">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-208">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26d10-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-210">Indica si se puede arrancar el equipo desde esta partición.</span><span class="sxs-lookup"><span data-stu-id="26d10-210">Indicates whether the computer can be booted from this partition.</span></span>

<span data-ttu-id="26d10-211">Esta propiedad se hereda de [**\_ DiskPartition CIM**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-211">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-212">**BootPartition**</span><span class="sxs-lookup"><span data-stu-id="26d10-212">**BootPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-213">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26d10-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-215">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| readfile")</span><span class="sxs-lookup"><span data-stu-id="26d10-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-216">Partition es la partición activa.</span><span class="sxs-lookup"><span data-stu-id="26d10-216">Partition is the active partition.</span></span> <span data-ttu-id="26d10-217">El sistema operativo usa la partición activa al arrancar desde un disco duro.</span><span class="sxs-lookup"><span data-stu-id="26d10-217">The operating system uses the active partition when booting from a hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="26d10-218">**Caption**</span><span class="sxs-lookup"><span data-stu-id="26d10-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-219">Tipo de datos: **cadena.**</span><span class="sxs-lookup"><span data-stu-id="26d10-219">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-221">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="26d10-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-222">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="26d10-222">Short description of the object.</span></span>

<span data-ttu-id="26d10-223">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-224">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="26d10-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-225">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26d10-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-227">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="26d10-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-228">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="26d10-228">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="26d10-229">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="26d10-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="26d10-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="26d10-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="26d10-231">(0)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-232">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="26d10-232">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="26d10-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="26d10-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="26d10-234">(1)</span><span class="sxs-lookup"><span data-stu-id="26d10-234">(1)</span></span>


</dt> <dd>

<span data-ttu-id="26d10-235">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="26d10-235">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="26d10-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="26d10-237">(2)</span><span class="sxs-lookup"><span data-stu-id="26d10-237">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="26d10-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="26d10-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="26d10-239">(3)</span><span class="sxs-lookup"><span data-stu-id="26d10-239">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="26d10-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="26d10-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="26d10-241">(4)</span><span class="sxs-lookup"><span data-stu-id="26d10-241">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="26d10-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="26d10-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="26d10-243">(5)</span><span class="sxs-lookup"><span data-stu-id="26d10-243">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="26d10-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="26d10-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="26d10-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="26d10-245">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="26d10-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="26d10-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="26d10-247">(7)</span><span class="sxs-lookup"><span data-stu-id="26d10-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="26d10-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="26d10-249">(8)</span><span class="sxs-lookup"><span data-stu-id="26d10-249">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="26d10-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="26d10-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="26d10-251">(9)</span><span class="sxs-lookup"><span data-stu-id="26d10-251">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="26d10-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="26d10-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="26d10-253">(10)</span><span class="sxs-lookup"><span data-stu-id="26d10-253">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="26d10-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="26d10-255">(11)</span><span class="sxs-lookup"><span data-stu-id="26d10-255">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="26d10-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="26d10-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="26d10-257">(12)</span><span class="sxs-lookup"><span data-stu-id="26d10-257">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="26d10-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="26d10-259">(13)</span><span class="sxs-lookup"><span data-stu-id="26d10-259">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="26d10-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="26d10-261">(14)</span><span class="sxs-lookup"><span data-stu-id="26d10-261">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="26d10-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="26d10-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="26d10-263">(15)</span><span class="sxs-lookup"><span data-stu-id="26d10-263">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="26d10-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="26d10-265">(16)</span><span class="sxs-lookup"><span data-stu-id="26d10-265">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="26d10-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="26d10-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="26d10-267">(17)</span><span class="sxs-lookup"><span data-stu-id="26d10-267">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="26d10-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="26d10-269">(18)</span><span class="sxs-lookup"><span data-stu-id="26d10-269">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="26d10-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="26d10-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="26d10-271">(19)</span><span class="sxs-lookup"><span data-stu-id="26d10-271">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="26d10-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="26d10-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="26d10-273">(20)</span><span class="sxs-lookup"><span data-stu-id="26d10-273">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="26d10-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="26d10-275">(21)</span><span class="sxs-lookup"><span data-stu-id="26d10-275">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="26d10-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="26d10-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="26d10-277">(22)</span><span class="sxs-lookup"><span data-stu-id="26d10-277">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="26d10-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="26d10-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="26d10-279">(23)</span><span class="sxs-lookup"><span data-stu-id="26d10-279">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="26d10-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="26d10-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="26d10-281">(24)</span><span class="sxs-lookup"><span data-stu-id="26d10-281">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="26d10-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="26d10-283">(25)</span><span class="sxs-lookup"><span data-stu-id="26d10-283">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="26d10-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="26d10-285">(26)</span><span class="sxs-lookup"><span data-stu-id="26d10-285">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="26d10-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="26d10-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="26d10-287">(27)</span><span class="sxs-lookup"><span data-stu-id="26d10-287">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="26d10-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="26d10-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="26d10-289">(28)</span><span class="sxs-lookup"><span data-stu-id="26d10-289">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="26d10-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="26d10-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="26d10-291">(29)</span><span class="sxs-lookup"><span data-stu-id="26d10-291">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="26d10-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="26d10-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="26d10-293">(30)</span><span class="sxs-lookup"><span data-stu-id="26d10-293">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="26d10-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="26d10-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="26d10-295">31</span><span class="sxs-lookup"><span data-stu-id="26d10-295">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26d10-296">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="26d10-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-297">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26d10-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-299">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="26d10-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-300">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="26d10-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="26d10-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="26d10-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-303">Tipo de datos: **cadena.**</span><span class="sxs-lookup"><span data-stu-id="26d10-303">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-305">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="26d10-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="26d10-306">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="26d10-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="26d10-307">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="26d10-307">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="26d10-308">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-309">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="26d10-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-312">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="26d10-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-313">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="26d10-313">Description of the object.</span></span>

<span data-ttu-id="26d10-314">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-315">**ID**</span><span class="sxs-lookup"><span data-stu-id="26d10-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-316">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-318">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="26d10-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-319">Identificador único de la unidad de disco y la partición del resto del sistema.</span><span class="sxs-lookup"><span data-stu-id="26d10-319">Unique identifier of the disk drive and partition, from the rest of the system.</span></span>

</dd> <dt>

<span data-ttu-id="26d10-320">**DiskIndex**</span><span class="sxs-lookup"><span data-stu-id="26d10-320">**DiskIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-321">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26d10-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-323">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| readfile")</span><span class="sxs-lookup"><span data-stu-id="26d10-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-324">Número de índice del disco que contiene esta partición.</span><span class="sxs-lookup"><span data-stu-id="26d10-324">Index number of the disk containing this partition.</span></span>

<span data-ttu-id="26d10-325">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="26d10-325">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="26d10-326">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="26d10-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-327">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26d10-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-329">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="26d10-329">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="26d10-330">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="26d10-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-332">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-334">Información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="26d10-334">Information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="26d10-335">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-336">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="26d10-336">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-337">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-339">Tipo de detección y corrección de errores admitidos por esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="26d10-339">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="26d10-340">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-340">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-341">**HiddenSectors**</span><span class="sxs-lookup"><span data-stu-id="26d10-341">**HiddenSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-342">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26d10-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-344">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api")</span><span class="sxs-lookup"><span data-stu-id="26d10-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-345">Número de sectores ocultos en la partición.</span><span class="sxs-lookup"><span data-stu-id="26d10-345">Number of hidden sectors in the partition.</span></span>

<span data-ttu-id="26d10-346">Ejemplo: 63</span><span class="sxs-lookup"><span data-stu-id="26d10-346">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="26d10-347">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="26d10-347">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-348">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="26d10-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="26d10-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-350">Una matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz OtherIdentifyingInfo.</span><span class="sxs-lookup"><span data-stu-id="26d10-350">An array of free-form strings providing explanations and details behind the entries in the OtherIdentifyingInfo array.</span></span> <span data-ttu-id="26d10-351">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de OtherIdentifyingInfo que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="26d10-351">Note, each entry of this array is related to the entry in OtherIdentifyingInfo that is located at the same index.</span></span>

<span data-ttu-id="26d10-352">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-353">**Index**</span><span class="sxs-lookup"><span data-stu-id="26d10-353">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-354">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26d10-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-356">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="26d10-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-357">Número de índice de la partición.</span><span class="sxs-lookup"><span data-stu-id="26d10-357">Index number of the partition.</span></span>

<span data-ttu-id="26d10-358">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="26d10-358">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="26d10-359">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="26d10-359">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-360">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="26d10-360">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-362">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="26d10-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-363">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="26d10-363">Date the object was installed.</span></span> <span data-ttu-id="26d10-364">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="26d10-364">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="26d10-365">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-366">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="26d10-366">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-367">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26d10-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-369">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="26d10-369">Last error code reported by the logical device.</span></span>

<span data-ttu-id="26d10-370">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-371">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="26d10-371">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-372">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26d10-372">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-374">Calificadores: **en desuso**</span><span class="sxs-lookup"><span data-stu-id="26d10-374">Qualifiers: **Depricated**</span></span>
</dt> </dl>

<span data-ttu-id="26d10-375">Tiempo máximo en milisegundos, que un dispositivo puede ejecutarse en estado inactivo.</span><span class="sxs-lookup"><span data-stu-id="26d10-375">Maximum time in milliseconds, that a Device can run in a Quiesced state.</span></span> <span data-ttu-id="26d10-376">El estado de un dispositivo se define en sus propiedades Availability y AdditionalAvailability, donde el valor 21 lo transmite.</span><span class="sxs-lookup"><span data-stu-id="26d10-376">A Device's state is defined in its Availability and AdditionalAvailability properties, where Quiesced is conveyed by the value 21.</span></span> <span data-ttu-id="26d10-377">Lo que sucede al final del límite de tiempo es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26d10-377">What occurs at the end of the time limit is device-specific.</span></span> <span data-ttu-id="26d10-378">El dispositivo puede desactivar, puede estar sin conexión o realizar otras acciones.</span><span class="sxs-lookup"><span data-stu-id="26d10-378">The Device may unquiesce, may offline or take other action.</span></span> <span data-ttu-id="26d10-379">Un valor de 0 indica que un dispositivo puede permanecer inactivo indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="26d10-379">A value of 0 indicates that a Device can remain quiesced indefinitely.</span></span>

> [!Note]
>
> <span data-ttu-id="26d10-380">"La propiedad MaxQuiesceTime está en desuso.</span><span class="sxs-lookup"><span data-stu-id="26d10-380">"The MaxQuiesceTime property has been deprecated.</span></span> <span data-ttu-id="26d10-381">Al evaluar el uso del modo de reposo, se determinó que esta propiedad única no es adecuada para describir Cuándo un dispositivo abandonará automáticamente un estado de modo inactivo.</span><span class="sxs-lookup"><span data-stu-id="26d10-381">When evaluating the use of Quiesce, it was determine that this single property is not adequate for describing when a device will automatically exit a quiescent state.</span></span> <span data-ttu-id="26d10-382">De hecho, el escenario más probable para que un dispositivo salga de un estado inactivo se determinó que se basaba en el número de solicitudes pendientes en cola en lugar de en un tiempo máximo.</span><span class="sxs-lookup"><span data-stu-id="26d10-382">In fact, the most likely scenario for a device to exit a quiescent state was determined to be based on the number of outstanding requests queued rather than on a maximum time.</span></span> <span data-ttu-id="26d10-383">Se volverá a evaluar y a colocar más adelante.</span><span class="sxs-lookup"><span data-stu-id="26d10-383">This will be re-evaluated and repositioned later.</span></span> <span data-ttu-id="26d10-384">\\n</span><span class="sxs-lookup"><span data-stu-id="26d10-384">\\n</span></span>

 

<span data-ttu-id="26d10-385">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-386">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="26d10-386">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-387">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-389">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="26d10-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-390">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="26d10-390">Label by which the object is known.</span></span> <span data-ttu-id="26d10-391">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="26d10-391">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="26d10-392">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-393">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="26d10-393">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-394">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26d10-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-396">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="26d10-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-397">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="26d10-397">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="26d10-398">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="26d10-398">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="26d10-399">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="26d10-399">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="26d10-400">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="26d10-400">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="26d10-401">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="26d10-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-403">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26d10-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-405">Matriz que captura datos adicionales, más allá de la información de DeviceID, que se pueden usar para identificar un LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="26d10-405">Array that captures additional data, beyond DeviceID information, that could be used to identify a LogicalDevice.</span></span> <span data-ttu-id="26d10-406">Un ejemplo sería mantener el nombre descriptivo del sistema operativo del dispositivo en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="26d10-406">One example would be to hold the Operating System's user friendly name for the Device in this property.</span></span> <span data-ttu-id="26d10-407">La longitud máxima es 256.</span><span class="sxs-lookup"><span data-stu-id="26d10-407">Maximum length is 256.</span></span>

<span data-ttu-id="26d10-408">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-409">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="26d10-409">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-410">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-412">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="26d10-412">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-413">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="26d10-413">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="26d10-414">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="26d10-414">Example: "\*PNP030b"</span></span>

<span data-ttu-id="26d10-415">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-416">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="26d10-416">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-417">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26d10-417">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="26d10-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-419">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="26d10-419">Indicates the specific power-related capabilities of the logical device.</span></span> <span data-ttu-id="26d10-420">Los valores de matriz, 0 = "Unknown", 1 = "no compatible" y 2 = "deshabilitado" se explican por sí solos.</span><span class="sxs-lookup"><span data-stu-id="26d10-420">The array values, 0="Unknown", 1="Not Supported" and 2="Disabled" are self-explanatory.</span></span> <span data-ttu-id="26d10-421">El valor 3 = "habilitado" indica que las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="26d10-421">The value, 3="Enabled" indicates that the power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span> <span data-ttu-id="26d10-422">"Modos de ahorro de energía introducidos automáticamente" (4) describe que un dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="26d10-422">"Power Saving Modes Entered Automatically" (4) describes that a device can change its power state based on usage or other criteria.</span></span> <span data-ttu-id="26d10-423">"El estado de energía configurable" (5) indica que se admite el método SetPowerState.</span><span class="sxs-lookup"><span data-stu-id="26d10-423">"Power State Settable" (5) indicates that the SetPowerState method is supported.</span></span> <span data-ttu-id="26d10-424">"Se admite el ciclo de energía" (6) indica que el método SetPowerState se puede invocar con la variable de entrada PowerState establecida en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="26d10-424">"Power Cycling Supported" (6) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle").</span></span> <span data-ttu-id="26d10-425">"El tiempo de espera admitido" (7) indica que el método SetPowerState se puede invocar con la variable de entrada PowerState establecida en 5 ("ciclo de energía") y el parámetro de tiempo establecido en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="26d10-425">"Timed Power On Supported" (7) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle") and the Time parameter set to a specific date and time, or interval, for power-on.</span></span>

<span data-ttu-id="26d10-426">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26d10-427">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="26d10-427">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="26d10-428">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="26d10-428">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="26d10-429">**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="26d10-429">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="26d10-430">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="26d10-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="26d10-431">**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="26d10-431">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="26d10-432">**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="26d10-432">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="26d10-433">**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="26d10-433">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="26d10-434">Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="26d10-434">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26d10-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="26d10-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-436">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26d10-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-438">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="26d10-438">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="26d10-439">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="26d10-439">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="26d10-440">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-441">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="26d10-441">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-442">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26d10-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-444">El número de horas consecutivas que este dispositivo ha estado encendido desde su último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="26d10-444">The number of consecutive hours that this Device has been powered, since its last power cycle.</span></span>

<span data-ttu-id="26d10-445">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-446">**PrimaryPartition**</span><span class="sxs-lookup"><span data-stu-id="26d10-446">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-447">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26d10-447">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-449">Si es **true**, esta es la partición principal.</span><span class="sxs-lookup"><span data-stu-id="26d10-449">If **True**, this is the primary partition.</span></span>

<span data-ttu-id="26d10-450">Esta propiedad se hereda de [**\_ DiskPartition CIM**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-450">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-451">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="26d10-451">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-452">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-454">Descripción del medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="26d10-454">Description of the media and its use.</span></span>

<span data-ttu-id="26d10-455">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-455">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-456">**RewritePartition**</span><span class="sxs-lookup"><span data-stu-id="26d10-456">**RewritePartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-457">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26d10-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-459">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de entrada y salida de dispositivo \ \| [**\_ información de partición**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| RewritePartition")</span><span class="sxs-lookup"><span data-stu-id="26d10-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RewritePartition")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-460">Si **es true**, la información de la partición ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="26d10-460">If **True**, the partition information has changed.</span></span> <span data-ttu-id="26d10-461">Cuando se cambia una partición (con [**el \_ \_ diseño de \_ unidad \_ del conjunto de discos ioctl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), el sistema usa esta propiedad para determinar qué particiones han cambiado y es necesario volver a escribir su información.</span><span class="sxs-lookup"><span data-stu-id="26d10-461">When you change a partition (with [**IOCTL\_DISK\_SET\_DRIVE\_LAYOUT**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), the system uses this property to determine which partitions have changed and need their information rewritten.</span></span> <span data-ttu-id="26d10-462">Si **es true**, se debe volver a escribir la partición.</span><span class="sxs-lookup"><span data-stu-id="26d10-462">If **TRUE**, the partition must be rewritten.</span></span>

</dd> <dt>

<span data-ttu-id="26d10-463">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="26d10-463">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-464">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26d10-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-466">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| readfile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="26d10-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-467">Tamaño total de la partición.</span><span class="sxs-lookup"><span data-stu-id="26d10-467">Total size of the partition.</span></span>

<span data-ttu-id="26d10-468">Ejemplo: 1059045376</span><span class="sxs-lookup"><span data-stu-id="26d10-468">Example: 1059045376</span></span>

<span data-ttu-id="26d10-469">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="26d10-469">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-470">**StartingOffset**</span><span class="sxs-lookup"><span data-stu-id="26d10-470">**StartingOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-471">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26d10-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-473">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| File Functions \| readfile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="26d10-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-474">Desplazamiento inicial (en bytes) de la partición.</span><span class="sxs-lookup"><span data-stu-id="26d10-474">Starting offset (in bytes) of the partition.</span></span>

<span data-ttu-id="26d10-475">Ejemplo: 32256</span><span class="sxs-lookup"><span data-stu-id="26d10-475">Example: 32256</span></span>

<span data-ttu-id="26d10-476">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="26d10-476">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-477">**Estado**</span><span class="sxs-lookup"><span data-stu-id="26d10-477">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-478">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-479">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-480">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="26d10-480">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-481">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="26d10-481">Current status of the object.</span></span> <span data-ttu-id="26d10-482">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="26d10-482">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="26d10-483">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="26d10-483">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="26d10-484">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="26d10-484">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="26d10-485">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="26d10-485">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="26d10-486">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="26d10-486">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="26d10-487">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-487">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="26d10-488">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="26d10-488">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="26d10-489">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="26d10-489">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="26d10-490">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="26d10-490">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="26d10-491">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="26d10-491">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26d10-492">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="26d10-492">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="26d10-493">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="26d10-493">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="26d10-494">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="26d10-494">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="26d10-495">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="26d10-495">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="26d10-496">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="26d10-496">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="26d10-497">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="26d10-497">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="26d10-498">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="26d10-498">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="26d10-499">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="26d10-499">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="26d10-500">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="26d10-500">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26d10-501">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="26d10-501">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-502">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26d10-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-503">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-504">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="26d10-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-505">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="26d10-505">State of the logical device.</span></span> <span data-ttu-id="26d10-506">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="26d10-506">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="26d10-507">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="26d10-508">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="26d10-508">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26d10-509">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="26d10-509">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="26d10-510">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="26d10-510">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="26d10-511">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="26d10-511">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="26d10-512">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="26d10-512">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26d10-513">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="26d10-513">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-514">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-515">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-516">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="26d10-516">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="26d10-517">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="26d10-517">Creation class name of the scoping system.</span></span>

<span data-ttu-id="26d10-518">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-518">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-519">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="26d10-519">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-520">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-521">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-522">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="26d10-522">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="26d10-523">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="26d10-523">Name of the scoping system.</span></span>

<span data-ttu-id="26d10-524">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-525">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="26d10-525">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-526">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="26d10-526">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-527">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="26d10-528">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26d10-528">The total number of hours that this device has been powered.</span></span>

<span data-ttu-id="26d10-529">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-529">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="26d10-530">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="26d10-530">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d10-531">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26d10-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d10-532">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26d10-532">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d10-533">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| PartitionRecord \| dwPartitionType")</span><span class="sxs-lookup"><span data-stu-id="26d10-533">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|PartitionRecord\|dwPartitionType")</span></span>
</dt> </dl>

<span data-ttu-id="26d10-534">Tipo de la partición.</span><span class="sxs-lookup"><span data-stu-id="26d10-534">Type of the partition.</span></span>

<span data-ttu-id="26d10-535">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="26d10-535">The values are:</span></span>

<dl> <dd><span data-ttu-id="26d10-536">Sin usar</span><span class="sxs-lookup"><span data-stu-id="26d10-536">"Unused"</span></span></dd> <dd><span data-ttu-id="26d10-537">"FAT de 12 bits"</span><span class="sxs-lookup"><span data-stu-id="26d10-537">"12-bit FAT"</span></span></dd> <dd><span data-ttu-id="26d10-538">"Xenix tipo 1"</span><span class="sxs-lookup"><span data-stu-id="26d10-538">"Xenix Type 1"</span></span></dd> <dd><span data-ttu-id="26d10-539">"Xenix tipo 2"</span><span class="sxs-lookup"><span data-stu-id="26d10-539">"Xenix Type 2"</span></span></dd> <dd><span data-ttu-id="26d10-540">"FAT de 16 bits"</span><span class="sxs-lookup"><span data-stu-id="26d10-540">"16-bit FAT"</span></span></dd> <dd><span data-ttu-id="26d10-541">"Partición extendida"</span><span class="sxs-lookup"><span data-stu-id="26d10-541">"Extended Partition"</span></span></dd> <dd><span data-ttu-id="26d10-542">"MS-DOS V4 enorme"</span><span class="sxs-lookup"><span data-stu-id="26d10-542">"MS-DOS V4 Huge"</span></span></dd> <dd><span data-ttu-id="26d10-543">"Sistema de archivos instalables"</span><span class="sxs-lookup"><span data-stu-id="26d10-543">"Installable File System"</span></span></dd> <dd><span data-ttu-id="26d10-544">"Plataforma de referencia de PowerPC"</span><span class="sxs-lookup"><span data-stu-id="26d10-544">"PowerPC Reference Platform"</span></span></dd> <dd><span data-ttu-id="26d10-545">Unix</span><span class="sxs-lookup"><span data-stu-id="26d10-545">"UNIX"</span></span></dd> <dd><span data-ttu-id="26d10-546">NTFS</span><span class="sxs-lookup"><span data-stu-id="26d10-546">"NTFS"</span></span></dd> <dd><span data-ttu-id="26d10-547">"Win95 w/Extended int 13"</span><span class="sxs-lookup"><span data-stu-id="26d10-547">"Win95 w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="26d10-548">"Extended w/Extended int 13"</span><span class="sxs-lookup"><span data-stu-id="26d10-548">"Extended w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="26d10-549">"Administrador de discos lógicos"</span><span class="sxs-lookup"><span data-stu-id="26d10-549">"Logical Disk Manager"</span></span></dd> <dd><span data-ttu-id="26d10-550">Unknown</span><span class="sxs-lookup"><span data-stu-id="26d10-550">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Unused"></span><span id="unused"></span><span id="UNUSED"></span>

<span data-ttu-id="26d10-551">**Sin usar** ("sin usar")</span><span class="sxs-lookup"><span data-stu-id="26d10-551">**Unused** ("Unused")</span></span>


</dt> <dd></dd> <dt>

<span id="12-bit_FAT"></span><span id="12-bit_fat"></span><span id="12-BIT_FAT"></span>

<span data-ttu-id="26d10-552">**FAT de 12 bits** ("FAT de 12 bits")</span><span class="sxs-lookup"><span data-stu-id="26d10-552">**12-bit FAT** ("12-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_1"></span><span id="xenix_type_1"></span><span id="XENIX_TYPE_1"></span>

<span data-ttu-id="26d10-553">**Xenix tipo 1** ("Xenix tipo 1")</span><span class="sxs-lookup"><span data-stu-id="26d10-553">**Xenix Type 1** ("Xenix Type 1")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_2"></span><span id="xenix_type_2"></span><span id="XENIX_TYPE_2"></span>

<span data-ttu-id="26d10-554">**Xenix tipo 2** ("Xenix tipo 2")</span><span class="sxs-lookup"><span data-stu-id="26d10-554">**Xenix Type 2** ("Xenix Type 2")</span></span>


</dt> <dd></dd> <dt>

<span id="16-bit_FAT"></span><span id="16-bit_fat"></span><span id="16-BIT_FAT"></span>

<span data-ttu-id="26d10-555">**FAT de 16 bits** ("FAT de 16 bits")</span><span class="sxs-lookup"><span data-stu-id="26d10-555">**16-bit FAT** ("16-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Partition"></span><span id="extended_partition"></span><span id="EXTENDED_PARTITION"></span>

<span data-ttu-id="26d10-556">**Partición extendida** ("partición extendida")</span><span class="sxs-lookup"><span data-stu-id="26d10-556">**Extended Partition** ("Extended Partition")</span></span>


</dt> <dd></dd> <dt>

<span id="MS-DOS_V4_Huge"></span><span id="ms-dos_v4_huge"></span><span id="MS-DOS_V4_HUGE"></span>

<span data-ttu-id="26d10-557">**Ms-dos V4 enorme** ("ms-dos V4 enorme")</span><span class="sxs-lookup"><span data-stu-id="26d10-557">**MS-DOS V4 Huge** ("MS-DOS V4 Huge")</span></span>


</dt> <dd></dd> <dt>

<span id="Installable_File_System"></span><span id="installable_file_system"></span><span id="INSTALLABLE_FILE_SYSTEM"></span>

<span data-ttu-id="26d10-558">**Sistema de archivos instalables** ("sistema de archivos instalables")</span><span class="sxs-lookup"><span data-stu-id="26d10-558">**Installable File System** ("Installable File System")</span></span>


</dt> <dd></dd> <dt>

<span id="PowerPC_Reference_Platform"></span><span id="powerpc_reference_platform"></span><span id="POWERPC_REFERENCE_PLATFORM"></span>

<span data-ttu-id="26d10-559">**Plataforma de referencia de PowerPC** ("plataforma de referencia de PowerPC")</span><span class="sxs-lookup"><span data-stu-id="26d10-559">**PowerPC Reference Platform** ("PowerPC Reference Platform")</span></span>


</dt> <dd></dd> <dt>

<span id="UNIX"></span><span id="unix"></span>

<span data-ttu-id="26d10-560">**UNIX** ("UNIX")</span><span class="sxs-lookup"><span data-stu-id="26d10-560">**UNIX** ("UNIX")</span></span>


</dt> <dd></dd> <dt>

<span id="NTFS"></span><span id="ntfs"></span>

<span data-ttu-id="26d10-561">**NTFS** ("NTFS")</span><span class="sxs-lookup"><span data-stu-id="26d10-561">**NTFS** ("NTFS")</span></span>


</dt> <dd></dd> <dt>

<span id="Win95_w_Extended_Int_13"></span><span id="win95_w_extended_int_13"></span><span id="WIN95_W_EXTENDED_INT_13"></span>

<span data-ttu-id="26d10-562">**Win95 w/Extended int 13** ("Win95 w/Extended int 13")</span><span class="sxs-lookup"><span data-stu-id="26d10-562">**Win95 w/Extended Int 13** ("Win95 w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_w_Extended_Int_13"></span><span id="extended_w_extended_int_13"></span><span id="EXTENDED_W_EXTENDED_INT_13"></span>

<span data-ttu-id="26d10-563">**Extended w/Extended int 13** ("Extended w/Extended int 13")</span><span class="sxs-lookup"><span data-stu-id="26d10-563">**Extended w/Extended Int 13** ("Extended w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk_Manager"></span><span id="logical_disk_manager"></span><span id="LOGICAL_DISK_MANAGER"></span>

<span data-ttu-id="26d10-564">**Administrador de discos lógicos** ("Administrador de discos lógicos")</span><span class="sxs-lookup"><span data-stu-id="26d10-564">**Logical Disk Manager** ("Logical Disk Manager")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26d10-565">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="26d10-565">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="26d10-566"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="26d10-566"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="26d10-567">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26d10-567">Remarks</span></span>

<span data-ttu-id="26d10-568">La **clase \_ DiskPartition de Win32** se deriva de [**\_ DiskPartition de CIM**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="26d10-568">The **Win32\_DiskPartition** class is derived from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

<span data-ttu-id="26d10-569">Una partición es una división estructural de una unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="26d10-569">A partition is a structural division of a physical disk drive.</span></span> <span data-ttu-id="26d10-570">Aunque una unidad puede contener una sola partición, los volúmenes más grandes suelen dividirse en varias particiones.</span><span class="sxs-lookup"><span data-stu-id="26d10-570">Although a drive can contain a single partition, larger volumes are often divided into multiple partitions.</span></span> <span data-ttu-id="26d10-571">Este es el motivo por el que podría tener las unidades C, D y E incluso aunque el equipo solo tenga un disco duro físico.</span><span class="sxs-lookup"><span data-stu-id="26d10-571">This is why you might have drives C, D, and E even though your computer has only a single physical hard disk.</span></span>

<span data-ttu-id="26d10-572">Windows admite los siguientes tipos de partición:</span><span class="sxs-lookup"><span data-stu-id="26d10-572">Windows supports the following partition types:</span></span>

-   <span data-ttu-id="26d10-573">Partición principal.</span><span class="sxs-lookup"><span data-stu-id="26d10-573">Primary partition.</span></span> <span data-ttu-id="26d10-574">Este es el único tipo de partición que puede tener instalado un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="26d10-574">This is the only type of partition that can have an operating system installed.</span></span> <span data-ttu-id="26d10-575">Cada unidad puede tener hasta cuatro particiones primarias, cada una con una letra de unidad diferente.</span><span class="sxs-lookup"><span data-stu-id="26d10-575">Each drive can have as many as four primary partitions, each assigned a different drive letter.</span></span>
-   <span data-ttu-id="26d10-576">Partición extendida.</span><span class="sxs-lookup"><span data-stu-id="26d10-576">Extended partition.</span></span> <span data-ttu-id="26d10-577">Partición adicional que se puede subdividir en varias unidades lógicas, cada una de las cuales tiene asignada una letra de unidad única.</span><span class="sxs-lookup"><span data-stu-id="26d10-577">An additional partition that can be subdivided into multiple logical drives, each assigned a unique drive letter.</span></span> <span data-ttu-id="26d10-578">Una unidad solo puede tener una partición extendida; sin embargo, puede dividir esta partición en varias unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="26d10-578">A drive can have only one extended partition; however, you can divide this partition into multiple logical drives.</span></span> <span data-ttu-id="26d10-579">Esto permite que un disco tenga más de las cuatro particiones primarias permitidas.</span><span class="sxs-lookup"><span data-stu-id="26d10-579">This enables a disk to have more than just the four allowed primary partitions.</span></span>
-   <span data-ttu-id="26d10-580">Partición del sistema.</span><span class="sxs-lookup"><span data-stu-id="26d10-580">System partition.</span></span> <span data-ttu-id="26d10-581">Cualquier partición primaria que contenga un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="26d10-581">Any primary partition containing an operating system.</span></span>

<span data-ttu-id="26d10-582">Las particiones pueden indicar cómo se utiliza realmente una unidad de disco físico.</span><span class="sxs-lookup"><span data-stu-id="26d10-582">Partitions can tell you how a physical disk drive is actually being used.</span></span> <span data-ttu-id="26d10-583">Mediante el examen de las particiones físicas en un disco, puede determinar los siguientes tipos de cosas:</span><span class="sxs-lookup"><span data-stu-id="26d10-583">By examining the physical partitions on a disk, you can determine the following types of things:</span></span>

-   <span data-ttu-id="26d10-584">Cómo se ha dividido el disco en unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="26d10-584">How the disk has been divided into logical drives.</span></span>
-   <span data-ttu-id="26d10-585">Si hay espacio sin particiones disponible en el disco.</span><span class="sxs-lookup"><span data-stu-id="26d10-585">If there is unpartitioned space available on the disk.</span></span> <span data-ttu-id="26d10-586">Esto puede determinarse restando el tamaño de todas las particiones de un disco del tamaño del disco.</span><span class="sxs-lookup"><span data-stu-id="26d10-586">This can be determined by subtracting the size of all the partitions on a disk from the size of the disk itself.</span></span>
-   <span data-ttu-id="26d10-587">Si puede arrancar el equipo desde ese disco (es decir, si el disco contiene una partición de arranque).</span><span class="sxs-lookup"><span data-stu-id="26d10-587">If you can boot the computer from that disk (that is, does the disk contain a boot partition).</span></span>

<span data-ttu-id="26d10-588">Todas estas preguntas se pueden resolver mediante la clase **Win32 \_ DiskPartition** .</span><span class="sxs-lookup"><span data-stu-id="26d10-588">All these questions can be resolved by using the **Win32\_DiskPartition** class.</span></span>

## <a name="examples"></a><span data-ttu-id="26d10-589">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="26d10-589">Examples</span></span>

<span data-ttu-id="26d10-590">El siguiente ejemplo de código de PowerShell comprueba la alineación de los discos en un equipo: Si el desplazamiento es fraccionario, el disco no está alineado correctamente.</span><span class="sxs-lookup"><span data-stu-id="26d10-590">The following PowerShell code sample checks the alignment of disks on a computer: if the offset is fractional, the disk is not aligned correctly.</span></span>


```PowerShell
$wql = "SELECT DiskIndex,Index,StartingOffset FROM Win32_DiskPartition"
Get-WmiObject -Query $wql -ComputerName '.' | Select-Object DiskIndex,Index,@{Name='Offset (KB)';Expression={$_.StartingOffset / 1024}} | Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="26d10-591">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26d10-591">Requirements</span></span>



| <span data-ttu-id="26d10-592">Requisito</span><span class="sxs-lookup"><span data-stu-id="26d10-592">Requirement</span></span> | <span data-ttu-id="26d10-593">Value</span><span class="sxs-lookup"><span data-stu-id="26d10-593">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26d10-594">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26d10-594">Minimum supported client</span></span><br/> | <span data-ttu-id="26d10-595">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="26d10-595">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="26d10-596">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26d10-596">Minimum supported server</span></span><br/> | <span data-ttu-id="26d10-597">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="26d10-597">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="26d10-598">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26d10-598">Namespace</span></span><br/>                | <span data-ttu-id="26d10-599">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="26d10-599">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="26d10-600">MOF</span><span class="sxs-lookup"><span data-stu-id="26d10-600">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26d10-601"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26d10-601"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="26d10-602">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26d10-602">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d10-603"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d10-603"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26d10-604">Vea también</span><span class="sxs-lookup"><span data-stu-id="26d10-604">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d10-605">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="26d10-605">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

<span data-ttu-id="26d10-606">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26d10-606">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="26d10-607">Tareas de WMI: discos y sistemas de archivos</span><span class="sxs-lookup"><span data-stu-id="26d10-607">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

