---
description: La \_ clase de LogicalDisk de CIM representa un intervalo contiguo de bloques lógicos que un sistema de archivos identifica mediante el campo de DeviceID (clave) del disco.
ms.assetid: 1c2fd0bf-a1e3-4706-9f84-5dd4d371a167
ms.tgt_platform: multiple
title: CIM_LogicalDisk (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.Access
- CIM_LogicalDisk.Availability
- CIM_LogicalDisk.BlockSize
- CIM_LogicalDisk.Caption
- CIM_LogicalDisk.ConfigManagerErrorCode
- CIM_LogicalDisk.ConfigManagerUserConfig
- CIM_LogicalDisk.CreationClassName
- CIM_LogicalDisk.Description
- CIM_LogicalDisk.DeviceID
- CIM_LogicalDisk.ErrorCleared
- CIM_LogicalDisk.ErrorDescription
- CIM_LogicalDisk.ErrorMethodology
- CIM_LogicalDisk.FreeSpace
- CIM_LogicalDisk.InstallDate
- CIM_LogicalDisk.LastErrorCode
- CIM_LogicalDisk.Name
- CIM_LogicalDisk.NumberOfBlocks
- CIM_LogicalDisk.PNPDeviceID
- CIM_LogicalDisk.PowerManagementCapabilities
- CIM_LogicalDisk.PowerManagementSupported
- CIM_LogicalDisk.Purpose
- CIM_LogicalDisk.Size
- CIM_LogicalDisk.Status
- CIM_LogicalDisk.StatusInfo
- CIM_LogicalDisk.SystemCreationClassName
- CIM_LogicalDisk.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd28ab0b9982606278e65705273a9965cfb9b396
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807118"
---
# <a name="cim_logicaldisk-class-cimwin32-wmi-providers"></a><span data-ttu-id="91329-103">CIM_LogicalDisk (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="91329-103">CIM_LogicalDisk class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="91329-104">La clase de **\_ LogicalDisk de CIM** representa un intervalo contiguo de bloques lógicos que un sistema de archivos identifica mediante el campo de **DeviceID** (clave) del disco.</span><span class="sxs-lookup"><span data-stu-id="91329-104">The **CIM\_LogicalDisk** class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="91329-105">Por ejemplo, en un entorno de Windows, el campo **DeviceID** contiene una letra de unidad; en un entorno de UNIX, contiene la ruta de acceso; y en un entorno de NetWare, contiene el nombre del volumen.</span><span class="sxs-lookup"><span data-stu-id="91329-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91329-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="91329-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="91329-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="91329-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="91329-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="91329-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="91329-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="91329-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="91329-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91329-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C539-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="91329-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="91329-111">Members</span></span>

<span data-ttu-id="91329-112">La clase de **\_ LogicalDisk de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="91329-112">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="91329-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="91329-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="91329-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="91329-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="91329-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="91329-115">Methods</span></span>

<span data-ttu-id="91329-116">La clase de **\_ LogicalDisk de CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="91329-116">The **CIM\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="91329-117">Método</span><span class="sxs-lookup"><span data-stu-id="91329-117">Method</span></span>                                                                 | <span data-ttu-id="91329-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="91329-118">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91329-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="91329-119">**Reset**</span></span>](reset-method-in-class-cim-logicaldisk.md)                 | <span data-ttu-id="91329-120">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="91329-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="91329-121">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="91329-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="91329-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="91329-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldisk.md) | <span data-ttu-id="91329-123">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="91329-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="91329-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="91329-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="91329-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="91329-125">Properties</span></span>

<span data-ttu-id="91329-126">La clase de **\_ LogicalDisk de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="91329-126">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91329-127">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="91329-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91329-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91329-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91329-130">Describe si el medio es legible, grabable o ambos, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="91329-130">Describes whether the media is readable, writable, or both, for example.</span></span> <span data-ttu-id="91329-131">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91329-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91329-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="91329-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="91329-133">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="91329-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="91329-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="91329-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="91329-135">Puedan.</span><span class="sxs-lookup"><span data-stu-id="91329-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="91329-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="91329-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="91329-137">Edita.</span><span class="sxs-lookup"><span data-stu-id="91329-137">Writable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="91329-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="91329-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91329-139">Compatibilidad con lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="91329-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="91329-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="91329-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="91329-141">Escribir una vez.</span><span class="sxs-lookup"><span data-stu-id="91329-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91329-142">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="91329-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91329-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91329-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-145">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="91329-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="91329-146">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-146">Availability and status of the device.</span></span>

<span data-ttu-id="91329-147">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91329-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="91329-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91329-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="91329-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="91329-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="91329-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="91329-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="91329-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="91329-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="91329-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="91329-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="91329-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="91329-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="91329-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="91329-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="91329-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="91329-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="91329-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="91329-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="91329-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="91329-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="91329-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="91329-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="91329-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="91329-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="91329-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="91329-161">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="91329-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="91329-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="91329-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="91329-163">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="91329-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="91329-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="91329-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="91329-165">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="91329-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="91329-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="91329-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="91329-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="91329-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="91329-168">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="91329-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="91329-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="91329-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="91329-170">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="91329-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="91329-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="91329-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="91329-172">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="91329-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="91329-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="91329-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="91329-174">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="91329-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="91329-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="91329-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="91329-176">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="91329-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91329-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="91329-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-178">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91329-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91329-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-180">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="91329-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="91329-181">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="91329-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="91329-182">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="91329-182">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="91329-183">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1.</span><span class="sxs-lookup"><span data-stu-id="91329-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="91329-184">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91329-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="91329-185">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="91329-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="91329-186">**Caption**</span><span class="sxs-lookup"><span data-stu-id="91329-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-189">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="91329-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="91329-190">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="91329-190">Short textual description of the object.</span></span>

<span data-ttu-id="91329-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91329-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-192">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="91329-192">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-193">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91329-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91329-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-195">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91329-195">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91329-196">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="91329-196">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="91329-197">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-197">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="91329-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="91329-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="91329-199"> (0)</span><span class="sxs-lookup"><span data-stu-id="91329-199">(0)</span></span>


</dt> <dd>

<span data-ttu-id="91329-200">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="91329-200">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="91329-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="91329-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="91329-202">(1)</span><span class="sxs-lookup"><span data-stu-id="91329-202">(1)</span></span>


</dt> <dd>

<span data-ttu-id="91329-203">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="91329-203">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91329-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="91329-205">(2)</span><span class="sxs-lookup"><span data-stu-id="91329-205">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="91329-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="91329-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="91329-207">(3)</span><span class="sxs-lookup"><span data-stu-id="91329-207">(3)</span></span>


</dt> <dd>

<span data-ttu-id="91329-208">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="91329-208">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="91329-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="91329-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="91329-210">(4)</span><span class="sxs-lookup"><span data-stu-id="91329-210">(4)</span></span>


</dt> <dd>

<span data-ttu-id="91329-211">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="91329-211">Device is not working properly.</span></span> <span data-ttu-id="91329-212">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="91329-212">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="91329-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="91329-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="91329-214">(5)</span><span class="sxs-lookup"><span data-stu-id="91329-214">(5)</span></span>


</dt> <dd>

<span data-ttu-id="91329-215">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="91329-215">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="91329-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="91329-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="91329-217"> (6)</span><span class="sxs-lookup"><span data-stu-id="91329-217">(6)</span></span>


</dt> <dd>

<span data-ttu-id="91329-218">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="91329-218">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="91329-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="91329-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="91329-220">(7)</span><span class="sxs-lookup"><span data-stu-id="91329-220">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="91329-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="91329-222">(8)</span><span class="sxs-lookup"><span data-stu-id="91329-222">(8)</span></span>


</dt> <dd>

<span data-ttu-id="91329-223">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-223">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="91329-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="91329-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="91329-225">(9)</span><span class="sxs-lookup"><span data-stu-id="91329-225">(9)</span></span>


</dt> <dd>

<span data-ttu-id="91329-226">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-226">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="91329-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="91329-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="91329-228">(10)</span><span class="sxs-lookup"><span data-stu-id="91329-228">(10)</span></span>


</dt> <dd>

<span data-ttu-id="91329-229">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="91329-229">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="91329-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="91329-231">(11)</span><span class="sxs-lookup"><span data-stu-id="91329-231">(11)</span></span>


</dt> <dd>

<span data-ttu-id="91329-232">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-232">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="91329-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="91329-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="91329-234">(12)</span><span class="sxs-lookup"><span data-stu-id="91329-234">(12)</span></span>


</dt> <dd>

<span data-ttu-id="91329-235">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="91329-235">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="91329-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="91329-237">(13)</span><span class="sxs-lookup"><span data-stu-id="91329-237">(13)</span></span>


</dt> <dd>

<span data-ttu-id="91329-238">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-238">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="91329-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="91329-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="91329-240">(14)</span><span class="sxs-lookup"><span data-stu-id="91329-240">(14)</span></span>


</dt> <dd>

<span data-ttu-id="91329-241">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="91329-241">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="91329-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="91329-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="91329-243">(15)</span><span class="sxs-lookup"><span data-stu-id="91329-243">(15)</span></span>


</dt> <dd>

<span data-ttu-id="91329-244">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="91329-244">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="91329-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="91329-246">(16)</span><span class="sxs-lookup"><span data-stu-id="91329-246">(16)</span></span>


</dt> <dd>

<span data-ttu-id="91329-247">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-247">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="91329-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="91329-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="91329-249">(17)</span><span class="sxs-lookup"><span data-stu-id="91329-249">(17)</span></span>


</dt> <dd>

<span data-ttu-id="91329-250">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="91329-250">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91329-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="91329-252">(18)</span><span class="sxs-lookup"><span data-stu-id="91329-252">(18)</span></span>


</dt> <dd>

<span data-ttu-id="91329-253">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="91329-253">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="91329-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="91329-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="91329-255">(19)</span><span class="sxs-lookup"><span data-stu-id="91329-255">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="91329-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="91329-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="91329-257">(20)</span><span class="sxs-lookup"><span data-stu-id="91329-257">(20)</span></span>


</dt> <dd>

<span data-ttu-id="91329-258">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="91329-258">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="91329-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="91329-260">(21)</span><span class="sxs-lookup"><span data-stu-id="91329-260">(21)</span></span>


</dt> <dd>

<span data-ttu-id="91329-261">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="91329-261">System failure.</span></span> <span data-ttu-id="91329-262">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="91329-262">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="91329-263">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-263">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="91329-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="91329-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="91329-265">(22)</span><span class="sxs-lookup"><span data-stu-id="91329-265">(22)</span></span>


</dt> <dd>

<span data-ttu-id="91329-266">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="91329-266">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="91329-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="91329-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="91329-268">(23)</span><span class="sxs-lookup"><span data-stu-id="91329-268">(23)</span></span>


</dt> <dd>

<span data-ttu-id="91329-269">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="91329-269">System failure.</span></span> <span data-ttu-id="91329-270">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="91329-270">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="91329-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="91329-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="91329-272">(24)</span><span class="sxs-lookup"><span data-stu-id="91329-272">(24)</span></span>


</dt> <dd>

<span data-ttu-id="91329-273">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="91329-273">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="91329-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="91329-275">(25)</span><span class="sxs-lookup"><span data-stu-id="91329-275">(25)</span></span>


</dt> <dd>

<span data-ttu-id="91329-276">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="91329-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="91329-278">(26)</span><span class="sxs-lookup"><span data-stu-id="91329-278">(26)</span></span>


</dt> <dd>

<span data-ttu-id="91329-279">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91329-279">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="91329-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="91329-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="91329-281">(27)</span><span class="sxs-lookup"><span data-stu-id="91329-281">(27)</span></span>


</dt> <dd>

<span data-ttu-id="91329-282">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="91329-282">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="91329-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="91329-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="91329-284">(28)</span><span class="sxs-lookup"><span data-stu-id="91329-284">(28)</span></span>


</dt> <dd>

<span data-ttu-id="91329-285">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="91329-285">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="91329-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="91329-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="91329-287">(29)</span><span class="sxs-lookup"><span data-stu-id="91329-287">(29)</span></span>


</dt> <dd>

<span data-ttu-id="91329-288">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="91329-288">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="91329-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="91329-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="91329-290">(30)</span><span class="sxs-lookup"><span data-stu-id="91329-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="91329-291">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="91329-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91329-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="91329-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="91329-293">31</span><span class="sxs-lookup"><span data-stu-id="91329-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="91329-294">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="91329-294">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91329-295">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="91329-295">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-296">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="91329-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91329-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-298">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91329-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91329-299">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="91329-299">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="91329-300">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-301">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91329-301">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-304">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91329-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91329-305">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="91329-305">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="91329-306">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="91329-306">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="91329-307">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-308">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="91329-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-311">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="91329-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="91329-312">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="91329-312">Textual description of the object.</span></span>

<span data-ttu-id="91329-313">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91329-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-314">**ID**</span><span class="sxs-lookup"><span data-stu-id="91329-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-317">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91329-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91329-318">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="91329-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="91329-319">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="91329-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-321">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="91329-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91329-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91329-323">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="91329-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="91329-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="91329-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91329-328">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="91329-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="91329-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-330">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="91329-330">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91329-333">Cadena de forma libre que describe el tipo de detección y corrección de errores admitidos por la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="91329-333">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="91329-334">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91329-334">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-335">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="91329-335">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-336">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91329-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91329-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-338">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="91329-338">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="91329-339">Espacio libre disponible, en bytes, en el disco lógico.</span><span class="sxs-lookup"><span data-stu-id="91329-339">Available free space, in bytes, on the logical disk.</span></span>

<span data-ttu-id="91329-340">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="91329-340">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="91329-341">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="91329-341">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-342">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="91329-342">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="91329-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-344">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="91329-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="91329-345">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="91329-345">Date and time the object was installed.</span></span> <span data-ttu-id="91329-346">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="91329-346">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="91329-347">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91329-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-348">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="91329-348">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-349">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91329-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91329-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91329-351">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="91329-351">Last error code reported by the logical device.</span></span>

<span data-ttu-id="91329-352">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-353">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="91329-353">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-354">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-356">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="91329-356">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="91329-357">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="91329-357">Label by which the object is known.</span></span> <span data-ttu-id="91329-358">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="91329-358">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="91329-359">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91329-359">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-360">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="91329-360">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-361">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91329-361">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91329-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-363">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="91329-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="91329-364">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="91329-364">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form the storage extent.</span></span> <span data-ttu-id="91329-365">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="91329-365">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="91329-366">Si el valor de la propiedad **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="91329-366">If the value of the **BlockSize** property is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="91329-367">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91329-367">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="91329-368">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="91329-368">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="91329-369">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="91329-369">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-370">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-372">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91329-372">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91329-373">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="91329-373">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="91329-374">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="91329-375">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="91329-375">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="91329-376">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="91329-376">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-377">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91329-377">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="91329-378">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91329-379">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="91329-379">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="91329-380">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="91329-380">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91329-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="91329-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="91329-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="91329-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="91329-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="91329-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="91329-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="91329-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91329-385">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="91329-385">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="91329-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="91329-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="91329-387">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="91329-387">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="91329-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="91329-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="91329-389">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="91329-389">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="91329-390">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="91329-390">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="91329-391">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="91329-391">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="91329-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="91329-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="91329-393">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="91329-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="91329-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="91329-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="91329-395">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="91329-395">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91329-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="91329-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-397">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="91329-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91329-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91329-399">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="91329-399">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="91329-400">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="91329-400">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="91329-401">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="91329-401">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="91329-402">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="91329-402">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="91329-403">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-404">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="91329-404">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-405">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91329-407">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="91329-407">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="91329-408">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91329-408">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-409">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="91329-409">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-410">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91329-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91329-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-412">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="91329-412">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="91329-413">Tamaño del disco lógico, en bytes.</span><span class="sxs-lookup"><span data-stu-id="91329-413">Size of the logical disk, in bytes.</span></span>

<span data-ttu-id="91329-414">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="91329-414">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="91329-415">**Estado**</span><span class="sxs-lookup"><span data-stu-id="91329-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-416">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-418">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="91329-418">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="91329-419">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="91329-419">Current status of the object.</span></span>

<span data-ttu-id="91329-420">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91329-420">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="91329-421">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="91329-421">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="91329-422">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="91329-422">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="91329-423">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="91329-423">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="91329-424">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="91329-424">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91329-425">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="91329-425">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="91329-426">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="91329-426">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="91329-427">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="91329-427">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="91329-428">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="91329-428">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="91329-429">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="91329-429">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="91329-430">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="91329-430">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="91329-431">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="91329-431">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="91329-432">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="91329-432">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="91329-433">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="91329-433">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91329-434">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="91329-434">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-435">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91329-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91329-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-437">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="91329-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="91329-438">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="91329-438">State of the logical device.</span></span> <span data-ttu-id="91329-439">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="91329-439">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="91329-440">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91329-441">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="91329-441">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91329-442">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="91329-442">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="91329-443">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="91329-443">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="91329-444">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="91329-444">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="91329-445">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="91329-445">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91329-446">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91329-446">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-447">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-449">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91329-449">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91329-450">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="91329-450">Scoping system's creation class name.</span></span>

<span data-ttu-id="91329-451">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91329-452">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="91329-452">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91329-453">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="91329-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91329-454">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="91329-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91329-455">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="91329-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="91329-456">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="91329-456">Scoping system's name.</span></span>

<span data-ttu-id="91329-457">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="91329-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91329-458">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91329-458">Remarks</span></span>

<span data-ttu-id="91329-459">La clase de **\_ LogicalDisk de CIM** se deriva de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91329-459">The **CIM\_LogicalDisk** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="91329-460">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="91329-460">WMI does not implement this class.</span></span> <span data-ttu-id="91329-461">Para las clases derivadas de la **\_ DiscoLógico de CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="91329-461">For classes derived from **CIM\_LogicalDisk**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="91329-462">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="91329-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="91329-463">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="91329-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="91329-464">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91329-464">Requirements</span></span>



| <span data-ttu-id="91329-465">Requisito</span><span class="sxs-lookup"><span data-stu-id="91329-465">Requirement</span></span> | <span data-ttu-id="91329-466">Value</span><span class="sxs-lookup"><span data-stu-id="91329-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91329-467">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91329-467">Minimum supported client</span></span><br/> | <span data-ttu-id="91329-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91329-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91329-469">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91329-469">Minimum supported server</span></span><br/> | <span data-ttu-id="91329-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91329-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91329-471">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="91329-471">Namespace</span></span><br/>                | <span data-ttu-id="91329-472">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="91329-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91329-473">MOF</span><span class="sxs-lookup"><span data-stu-id="91329-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91329-474"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91329-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91329-475">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91329-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91329-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91329-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91329-477">Vea también</span><span class="sxs-lookup"><span data-stu-id="91329-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91329-478">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="91329-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

