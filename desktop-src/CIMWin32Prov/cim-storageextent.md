---
description: La \_ clase CIM StorageExtent representa las capacidades y la administración de los distintos medios que existen para almacenar datos y permitir la recuperación de datos.
ms.assetid: 3895e00e-1a80-4d45-be0a-b159f8f335e8
ms.tgt_platform: multiple
title: CIM_StorageExtent (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.Access
- CIM_StorageExtent.Availability
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.Caption
- CIM_StorageExtent.ConfigManagerErrorCode
- CIM_StorageExtent.ConfigManagerUserConfig
- CIM_StorageExtent.CreationClassName
- CIM_StorageExtent.Description
- CIM_StorageExtent.DeviceID
- CIM_StorageExtent.ErrorCleared
- CIM_StorageExtent.ErrorDescription
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.InstallDate
- CIM_StorageExtent.LastErrorCode
- CIM_StorageExtent.Name
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.PNPDeviceID
- CIM_StorageExtent.PowerManagementCapabilities
- CIM_StorageExtent.PowerManagementSupported
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Status
- CIM_StorageExtent.StatusInfo
- CIM_StorageExtent.SystemCreationClassName
- CIM_StorageExtent.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f2d83386822d0994cc3acf68b97acc2841b77d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659589"
---
# <a name="cim_storageextent-class-cimwin32-wmi-providers"></a><span data-ttu-id="db4aa-103">CIM_StorageExtent (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="db4aa-103">CIM_StorageExtent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="db4aa-104">La clase **CIM \_ StorageExtent** representa las capacidades y la administración de los distintos medios que existen para almacenar datos y permitir la recuperación de datos.</span><span class="sxs-lookup"><span data-stu-id="db4aa-104">The **CIM\_StorageExtent** class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="db4aa-105">Esta clase primaria puede representar los distintos componentes de RAID (hardware o software) o una extensión lógica sin procesar sobre medios físicos.</span><span class="sxs-lookup"><span data-stu-id="db4aa-105">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db4aa-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="db4aa-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="db4aa-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="db4aa-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="db4aa-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="db4aa-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="db4aa-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="db4aa-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="db4aa-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db4aa-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C538-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
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
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="db4aa-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="db4aa-111">Members</span></span>

<span data-ttu-id="db4aa-112">La clase **CIM \_ StorageExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="db4aa-112">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="db4aa-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="db4aa-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="db4aa-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="db4aa-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="db4aa-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="db4aa-115">Methods</span></span>

<span data-ttu-id="db4aa-116">La clase **CIM \_ StorageExtent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="db4aa-116">The **CIM\_StorageExtent** class has these methods.</span></span>



| <span data-ttu-id="db4aa-117">Método</span><span class="sxs-lookup"><span data-stu-id="db4aa-117">Method</span></span>                                                                   | <span data-ttu-id="db4aa-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="db4aa-118">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db4aa-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="db4aa-119">**Reset**</span></span>](reset-method-in-class-cim-storageextent.md)                 | <span data-ttu-id="db4aa-120">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="db4aa-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="db4aa-121">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="db4aa-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="db4aa-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="db4aa-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-storageextent.md) | <span data-ttu-id="db4aa-123">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="db4aa-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="db4aa-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="db4aa-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="db4aa-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="db4aa-125">Properties</span></span>

<span data-ttu-id="db4aa-126">La clase **CIM \_ StorageExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="db4aa-126">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db4aa-127">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="db4aa-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db4aa-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-130">Describe las propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="db4aa-130">Describes the read/write properties of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db4aa-131">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="db4aa-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="db4aa-132">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="db4aa-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="db4aa-133">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="db4aa-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="db4aa-134">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="db4aa-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="db4aa-135">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="db4aa-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="db4aa-136">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="db4aa-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db4aa-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-139">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="db4aa-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-140">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-140">Availability and status of the device.</span></span>

<span data-ttu-id="db4aa-141">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db4aa-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="db4aa-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db4aa-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="db4aa-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="db4aa-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="db4aa-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="db4aa-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="db4aa-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="db4aa-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="db4aa-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="db4aa-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="db4aa-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="db4aa-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="db4aa-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="db4aa-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="db4aa-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="db4aa-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="db4aa-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="db4aa-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="db4aa-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="db4aa-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="db4aa-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="db4aa-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="db4aa-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="db4aa-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="db4aa-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-155">Ahorro de energía: desconocido</span><span class="sxs-lookup"><span data-stu-id="db4aa-155">Power Save - Unknown</span></span>

<span data-ttu-id="db4aa-156">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="db4aa-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="db4aa-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="db4aa-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-158">Ahorro de energía: modo de baja energía</span><span class="sxs-lookup"><span data-stu-id="db4aa-158">Power Save - Low Power Mode</span></span>

<span data-ttu-id="db4aa-159">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="db4aa-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="db4aa-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="db4aa-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-161">Ahorro de energía: en espera</span><span class="sxs-lookup"><span data-stu-id="db4aa-161">Power Save - Standby</span></span>

<span data-ttu-id="db4aa-162">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="db4aa-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="db4aa-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="db4aa-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="db4aa-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="db4aa-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-165">Ahorro de energía: ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="db4aa-165">Power Save - Warning</span></span>

<span data-ttu-id="db4aa-166">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="db4aa-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="db4aa-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="db4aa-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-168">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="db4aa-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="db4aa-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="db4aa-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-170">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="db4aa-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="db4aa-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-172">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="db4aa-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="db4aa-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="db4aa-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-174">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="db4aa-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db4aa-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="db4aa-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-176">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="db4aa-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-178">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="db4aa-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-179">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="db4aa-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="db4aa-180">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="db4aa-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="db4aa-181">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="db4aa-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="db4aa-182">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="db4aa-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-183">**Caption**</span><span class="sxs-lookup"><span data-stu-id="db4aa-183">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-186">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="db4aa-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-187">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="db4aa-187">Short textual description of the object.</span></span>

<span data-ttu-id="db4aa-188">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-189">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="db4aa-189">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-190">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db4aa-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-192">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="db4aa-192">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-193">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="db4aa-193">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="db4aa-194">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="db4aa-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="db4aa-196"> (0)</span><span class="sxs-lookup"><span data-stu-id="db4aa-196">(0)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-197">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="db4aa-197">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="db4aa-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="db4aa-199">(1)</span><span class="sxs-lookup"><span data-stu-id="db4aa-199">(1)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-200">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="db4aa-200">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="db4aa-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="db4aa-202">(2)</span><span class="sxs-lookup"><span data-stu-id="db4aa-202">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="db4aa-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="db4aa-204">(3)</span><span class="sxs-lookup"><span data-stu-id="db4aa-204">(3)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-205">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="db4aa-205">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="db4aa-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="db4aa-207">(4)</span><span class="sxs-lookup"><span data-stu-id="db4aa-207">(4)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-208">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="db4aa-208">Device is not working properly.</span></span> <span data-ttu-id="db4aa-209">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="db4aa-209">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="db4aa-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="db4aa-211">(5)</span><span class="sxs-lookup"><span data-stu-id="db4aa-211">(5)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-212">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="db4aa-212">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="db4aa-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="db4aa-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="db4aa-214">(6)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-215">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="db4aa-215">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="db4aa-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="db4aa-217">(7)</span><span class="sxs-lookup"><span data-stu-id="db4aa-217">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="db4aa-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="db4aa-219">(8)</span><span class="sxs-lookup"><span data-stu-id="db4aa-219">(8)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-220">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-220">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="db4aa-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="db4aa-222">(9)</span><span class="sxs-lookup"><span data-stu-id="db4aa-222">(9)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-223">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="db4aa-223">Device is not working properly.</span></span> <span data-ttu-id="db4aa-224">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-224">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="db4aa-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="db4aa-226">(10)</span><span class="sxs-lookup"><span data-stu-id="db4aa-226">(10)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-227">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="db4aa-227">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="db4aa-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="db4aa-229">(11)</span><span class="sxs-lookup"><span data-stu-id="db4aa-229">(11)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-230">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-230">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="db4aa-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="db4aa-232">(12)</span><span class="sxs-lookup"><span data-stu-id="db4aa-232">(12)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-233">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="db4aa-233">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="db4aa-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="db4aa-235">(13)</span><span class="sxs-lookup"><span data-stu-id="db4aa-235">(13)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-236">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-236">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="db4aa-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="db4aa-238">(14)</span><span class="sxs-lookup"><span data-stu-id="db4aa-238">(14)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-239">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-239">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="db4aa-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="db4aa-241">(15)</span><span class="sxs-lookup"><span data-stu-id="db4aa-241">(15)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-242">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="db4aa-242">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="db4aa-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="db4aa-244">(16)</span><span class="sxs-lookup"><span data-stu-id="db4aa-244">(16)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-245">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-245">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="db4aa-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="db4aa-247">(17)</span><span class="sxs-lookup"><span data-stu-id="db4aa-247">(17)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-248">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="db4aa-248">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="db4aa-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="db4aa-250">(18)</span><span class="sxs-lookup"><span data-stu-id="db4aa-250">(18)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-251">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="db4aa-251">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="db4aa-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="db4aa-253">(19)</span><span class="sxs-lookup"><span data-stu-id="db4aa-253">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="db4aa-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="db4aa-255">(20)</span><span class="sxs-lookup"><span data-stu-id="db4aa-255">(20)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-256">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="db4aa-256">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="db4aa-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="db4aa-258">(21)</span><span class="sxs-lookup"><span data-stu-id="db4aa-258">(21)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-259">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="db4aa-259">System failure.</span></span> <span data-ttu-id="db4aa-260">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="db4aa-260">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="db4aa-261">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-261">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="db4aa-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="db4aa-263">(22)</span><span class="sxs-lookup"><span data-stu-id="db4aa-263">(22)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-264">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="db4aa-264">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="db4aa-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="db4aa-266">(23)</span><span class="sxs-lookup"><span data-stu-id="db4aa-266">(23)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-267">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="db4aa-267">System failure.</span></span> <span data-ttu-id="db4aa-268">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="db4aa-268">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="db4aa-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="db4aa-270">(24)</span><span class="sxs-lookup"><span data-stu-id="db4aa-270">(24)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-271">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="db4aa-271">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="db4aa-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="db4aa-273">(25)</span><span class="sxs-lookup"><span data-stu-id="db4aa-273">(25)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-274">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="db4aa-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="db4aa-276">(26)</span><span class="sxs-lookup"><span data-stu-id="db4aa-276">(26)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-277">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db4aa-277">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="db4aa-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="db4aa-279">(27)</span><span class="sxs-lookup"><span data-stu-id="db4aa-279">(27)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-280">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="db4aa-280">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="db4aa-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="db4aa-282">(28)</span><span class="sxs-lookup"><span data-stu-id="db4aa-282">(28)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-283">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="db4aa-283">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="db4aa-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="db4aa-285">(29)</span><span class="sxs-lookup"><span data-stu-id="db4aa-285">(29)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-286">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="db4aa-286">Device is disabled.</span></span> <span data-ttu-id="db4aa-287">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="db4aa-287">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="db4aa-288"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-288"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="db4aa-289">(30)</span><span class="sxs-lookup"><span data-stu-id="db4aa-289">(30)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-290">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="db4aa-290">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="db4aa-291"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="db4aa-291"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="db4aa-292">31</span><span class="sxs-lookup"><span data-stu-id="db4aa-292">(31)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-293">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="db4aa-293">Device is not working properly.</span></span> <span data-ttu-id="db4aa-294">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="db4aa-294">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db4aa-295">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="db4aa-295">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-296">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="db4aa-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-298">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="db4aa-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-299">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="db4aa-299">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="db4aa-300">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-301">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="db4aa-301">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-304">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="db4aa-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-305">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="db4aa-305">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="db4aa-306">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="db4aa-306">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="db4aa-307">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-308">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="db4aa-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-311">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="db4aa-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-312">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="db4aa-312">Textual description of the object.</span></span>

<span data-ttu-id="db4aa-313">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-314">**ID**</span><span class="sxs-lookup"><span data-stu-id="db4aa-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-317">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="db4aa-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-318">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="db4aa-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="db4aa-319">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="db4aa-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-321">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="db4aa-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-323">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="db4aa-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="db4aa-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="db4aa-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-328">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="db4aa-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="db4aa-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-330">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="db4aa-330">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-333">Cadena de forma libre que describe el tipo de detección y corrección de errores admitidos por la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="db4aa-333">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="db4aa-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-335">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="db4aa-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="db4aa-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-338">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="db4aa-338">Date and time the object was installed.</span></span> <span data-ttu-id="db4aa-339">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="db4aa-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="db4aa-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="db4aa-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-342">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db4aa-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-344">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="db4aa-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="db4aa-345">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-346">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="db4aa-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-349">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="db4aa-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-350">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="db4aa-350">Label by which the object is known.</span></span> <span data-ttu-id="db4aa-351">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="db4aa-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="db4aa-352">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="db4aa-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-354">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="db4aa-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-356">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="db4aa-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-357">Número de bloques consecutivos, cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="db4aa-357">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="db4aa-358">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="db4aa-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="db4aa-359">Si el valor de **blocksize** es 1 (uno), esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="db4aa-359">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="db4aa-360">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="db4aa-360">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-361">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="db4aa-361">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-362">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-364">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="db4aa-364">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-365">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="db4aa-365">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="db4aa-366">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="db4aa-367">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="db4aa-367">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-368">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="db4aa-368">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-369">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db4aa-369">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-371">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="db4aa-371">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="db4aa-372">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db4aa-373"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="db4aa-373"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="db4aa-374"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="db4aa-374"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="db4aa-375"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="db4aa-375"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="db4aa-376"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="db4aa-376"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-377">habilitado</span><span class="sxs-lookup"><span data-stu-id="db4aa-377">Enabled</span></span>

<span data-ttu-id="db4aa-378">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="db4aa-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="db4aa-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="db4aa-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-380">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="db4aa-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="db4aa-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="db4aa-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-382">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="db4aa-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="db4aa-383">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="db4aa-383">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="db4aa-384">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="db4aa-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="db4aa-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="db4aa-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-386">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="db4aa-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="db4aa-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="db4aa-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="db4aa-388">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="db4aa-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="db4aa-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="db4aa-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-390">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="db4aa-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-392">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="db4aa-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="db4aa-393">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="db4aa-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="db4aa-394">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="db4aa-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="db4aa-395">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="db4aa-395">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="db4aa-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-397">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="db4aa-397">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-398">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-400">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="db4aa-400">Free form string that describes the media and its use.</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-401">**Estado**</span><span class="sxs-lookup"><span data-stu-id="db4aa-401">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-402">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-404">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="db4aa-404">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-405">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="db4aa-405">Current status of the object.</span></span>

<span data-ttu-id="db4aa-406">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="db4aa-407">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="db4aa-407">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="db4aa-408">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="db4aa-408">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="db4aa-409">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="db4aa-409">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="db4aa-410">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="db4aa-410">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db4aa-411">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="db4aa-411">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="db4aa-412">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="db4aa-412">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="db4aa-413">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="db4aa-413">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="db4aa-414">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="db4aa-414">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="db4aa-415">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="db4aa-415">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="db4aa-416">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="db4aa-416">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="db4aa-417">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="db4aa-417">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="db4aa-418">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="db4aa-418">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="db4aa-419">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="db4aa-419">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="db4aa-420">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="db4aa-420">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-421">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="db4aa-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-423">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="db4aa-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-424">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="db4aa-424">State of the logical device.</span></span> <span data-ttu-id="db4aa-425">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="db4aa-425">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="db4aa-426">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="db4aa-427">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="db4aa-427">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="db4aa-428">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="db4aa-428">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="db4aa-429">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="db4aa-429">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="db4aa-430">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="db4aa-430">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="db4aa-431">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="db4aa-431">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="db4aa-432">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="db4aa-432">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-433">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-435">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="db4aa-435">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-436">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="db4aa-436">Scoping system's creation class name.</span></span>

<span data-ttu-id="db4aa-437">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="db4aa-438">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="db4aa-438">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db4aa-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="db4aa-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="db4aa-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db4aa-441">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="db4aa-441">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="db4aa-442">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="db4aa-442">Scoping system's name.</span></span>

<span data-ttu-id="db4aa-443">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db4aa-444">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db4aa-444">Remarks</span></span>

<span data-ttu-id="db4aa-445">La **clase \_ StorageExtent de CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-445">The **CIM\_StorageExtent** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="db4aa-446">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="db4aa-446">WMI does not implement this class.</span></span> <span data-ttu-id="db4aa-447">Para las clases WMI derivadas de **CIM \_ StorageExtent**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="db4aa-447">For WMI classes derived from **CIM\_StorageExtent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="db4aa-448">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="db4aa-448">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="db4aa-449">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="db4aa-449">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="db4aa-450">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db4aa-450">Requirements</span></span>



| <span data-ttu-id="db4aa-451">Requisito</span><span class="sxs-lookup"><span data-stu-id="db4aa-451">Requirement</span></span> | <span data-ttu-id="db4aa-452">Value</span><span class="sxs-lookup"><span data-stu-id="db4aa-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db4aa-453">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db4aa-453">Minimum supported client</span></span><br/> | <span data-ttu-id="db4aa-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db4aa-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db4aa-455">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db4aa-455">Minimum supported server</span></span><br/> | <span data-ttu-id="db4aa-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db4aa-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db4aa-457">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="db4aa-457">Namespace</span></span><br/>                | <span data-ttu-id="db4aa-458">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="db4aa-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="db4aa-459">MOF</span><span class="sxs-lookup"><span data-stu-id="db4aa-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db4aa-460"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db4aa-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="db4aa-461">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db4aa-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db4aa-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db4aa-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db4aa-463">Vea también</span><span class="sxs-lookup"><span data-stu-id="db4aa-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4aa-464">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="db4aa-464">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

