---
description: La \_ clase CIM VolumeSet representa un intervalo contiguo de bloques lógicos que se presentan al entorno operativo para leer y escribir datos de usuario.
ms.assetid: f0350185-6210-4f95-a2a2-23de61b1af1f
ms.tgt_platform: multiple
title: CIM_VolumeSet (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolumeSet
- CIM_VolumeSet.Access
- CIM_VolumeSet.Availability
- CIM_VolumeSet.BlockSize
- CIM_VolumeSet.Caption
- CIM_VolumeSet.ConfigManagerErrorCode
- CIM_VolumeSet.ConfigManagerUserConfig
- CIM_VolumeSet.CreationClassName
- CIM_VolumeSet.Description
- CIM_VolumeSet.DeviceID
- CIM_VolumeSet.ErrorCleared
- CIM_VolumeSet.ErrorDescription
- CIM_VolumeSet.ErrorMethodology
- CIM_VolumeSet.InstallDate
- CIM_VolumeSet.LastErrorCode
- CIM_VolumeSet.Name
- CIM_VolumeSet.NumberOfBlocks
- CIM_VolumeSet.PNPDeviceID
- CIM_VolumeSet.PowerManagementCapabilities
- CIM_VolumeSet.PowerManagementSupported
- CIM_VolumeSet.PSExtentInterleaveDepth
- CIM_VolumeSet.PSExtentStripeLength
- CIM_VolumeSet.Purpose
- CIM_VolumeSet.Status
- CIM_VolumeSet.StatusInfo
- CIM_VolumeSet.SystemCreationClassName
- CIM_VolumeSet.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7ee8cd96381901250c9a15e544ee1963470565b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659409"
---
# <a name="cim_volumeset-class"></a><span data-ttu-id="d59d8-103">\_Clase VolumeSet de CIM</span><span class="sxs-lookup"><span data-stu-id="d59d8-103">CIM\_VolumeSet class</span></span>

<span data-ttu-id="d59d8-104">La clase **CIM \_ VolumeSet** representa un intervalo contiguo de bloques lógicos que se presentan al entorno operativo para leer y escribir datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="d59d8-104">The **CIM\_VolumeSet** class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span> <span data-ttu-id="d59d8-105">Los conjuntos de volúmenes no deben superponerse entre sí y se basan en una o varias extensiones físicas, extensiones de espacio protegido o extensiones de agregado (todo el mismo tipo).</span><span class="sxs-lookup"><span data-stu-id="d59d8-105">Volume sets should not overlap one another and are based on one or more physical extents, protected space extents, or aggregate extents (all of the same type).</span></span> <span data-ttu-id="d59d8-106">Se debe crear una instancia de las asociaciones basadas en o subclases según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d59d8-106">The based-on associations should be instantiated or subclassed as needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d59d8-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="d59d8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d59d8-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d59d8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d59d8-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d59d8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d59d8-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d59d8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d59d8-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d59d8-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{35E25AA5-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VolumeSet : CIM_StorageExtent
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
  uint64   PSExtentInterleaveDepth;
  uint64   PSExtentStripeLength;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="d59d8-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="d59d8-112">Members</span></span>

<span data-ttu-id="d59d8-113">La clase **CIM \_ VolumeSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d59d8-113">The **CIM\_VolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="d59d8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d59d8-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d59d8-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d59d8-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d59d8-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="d59d8-116">Methods</span></span>

<span data-ttu-id="d59d8-117">La clase **CIM \_ VolumeSet** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d59d8-117">The **CIM\_VolumeSet** class has these methods.</span></span>



| <span data-ttu-id="d59d8-118">Método</span><span class="sxs-lookup"><span data-stu-id="d59d8-118">Method</span></span>                                                               | <span data-ttu-id="d59d8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="d59d8-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d59d8-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="d59d8-120">**Reset**</span></span>](reset-method-in-class-cim-volumeset.md)                 | <span data-ttu-id="d59d8-121">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d59d8-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="d59d8-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="d59d8-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="d59d8-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d59d8-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volumeset.md) | <span data-ttu-id="d59d8-124">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="d59d8-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="d59d8-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="d59d8-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d59d8-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d59d8-126">Properties</span></span>

<span data-ttu-id="d59d8-127">La clase **CIM \_ VolumeSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d59d8-127">The **CIM\_VolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d59d8-128">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="d59d8-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d59d8-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-131">Propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="d59d8-131">Read/write properties of the media.</span></span>

<span data-ttu-id="d59d8-132">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d59d8-133">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d59d8-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="d59d8-134">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="d59d8-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="d59d8-135">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="d59d8-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="d59d8-136">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="d59d8-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="d59d8-137">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="d59d8-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d59d8-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="d59d8-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d59d8-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-141">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d59d8-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-142">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-142">Availability and status of the device.</span></span>

<span data-ttu-id="d59d8-143">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d59d8-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d59d8-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d59d8-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d59d8-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d59d8-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d59d8-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d59d8-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="d59d8-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d59d8-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="d59d8-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d59d8-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d59d8-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d59d8-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="d59d8-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d59d8-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="d59d8-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d59d8-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="d59d8-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d59d8-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="d59d8-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d59d8-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="d59d8-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d59d8-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="d59d8-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d59d8-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="d59d8-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-157">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="d59d8-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d59d8-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="d59d8-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-159">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="d59d8-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d59d8-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="d59d8-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-161">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="d59d8-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d59d8-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="d59d8-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d59d8-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="d59d8-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-164">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="d59d8-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d59d8-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d59d8-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-166">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d59d8-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d59d8-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="d59d8-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-168">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d59d8-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="d59d8-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-170">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="d59d8-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d59d8-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d59d8-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-172">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="d59d8-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d59d8-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="d59d8-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-174">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d59d8-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-176">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="d59d8-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-177">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d59d8-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="d59d8-178">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="d59d8-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="d59d8-179">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="d59d8-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="d59d8-180">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-180">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d59d8-181">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d59d8-181">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d59d8-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-185">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d59d8-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-186">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d59d8-186">Short textual description of the object.</span></span>

<span data-ttu-id="d59d8-187">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d59d8-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-189">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d59d8-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-191">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d59d8-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-192">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d59d8-192">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="d59d8-193">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d59d8-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d59d8-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="d59d8-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-196">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d59d8-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d59d8-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d59d8-198">(1)</span><span class="sxs-lookup"><span data-stu-id="d59d8-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-199">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d59d8-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d59d8-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d59d8-201">(2)</span><span class="sxs-lookup"><span data-stu-id="d59d8-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d59d8-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d59d8-203">(3)</span><span class="sxs-lookup"><span data-stu-id="d59d8-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-204">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="d59d8-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d59d8-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d59d8-206">(4)</span><span class="sxs-lookup"><span data-stu-id="d59d8-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-207">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d59d8-207">Device is not working properly.</span></span> <span data-ttu-id="d59d8-208">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="d59d8-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d59d8-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d59d8-210">(5)</span><span class="sxs-lookup"><span data-stu-id="d59d8-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-211">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="d59d8-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d59d8-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d59d8-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="d59d8-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-214">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d59d8-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d59d8-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d59d8-216">(7)</span><span class="sxs-lookup"><span data-stu-id="d59d8-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d59d8-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d59d8-218">(8)</span><span class="sxs-lookup"><span data-stu-id="d59d8-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-219">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d59d8-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d59d8-221">(9)</span><span class="sxs-lookup"><span data-stu-id="d59d8-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-222">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d59d8-222">Device is not working properly.</span></span> <span data-ttu-id="d59d8-223">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d59d8-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d59d8-225">(10)</span><span class="sxs-lookup"><span data-stu-id="d59d8-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-226">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="d59d8-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d59d8-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d59d8-228">(11)</span><span class="sxs-lookup"><span data-stu-id="d59d8-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-229">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d59d8-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d59d8-231">(12)</span><span class="sxs-lookup"><span data-stu-id="d59d8-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-232">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="d59d8-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d59d8-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d59d8-234">(13)</span><span class="sxs-lookup"><span data-stu-id="d59d8-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-235">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d59d8-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d59d8-237">(14)</span><span class="sxs-lookup"><span data-stu-id="d59d8-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-238">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d59d8-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d59d8-240">(15)</span><span class="sxs-lookup"><span data-stu-id="d59d8-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-241">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="d59d8-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d59d8-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d59d8-243">(16)</span><span class="sxs-lookup"><span data-stu-id="d59d8-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-244">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d59d8-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d59d8-246">(17)</span><span class="sxs-lookup"><span data-stu-id="d59d8-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-247">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="d59d8-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d59d8-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d59d8-249">(18)</span><span class="sxs-lookup"><span data-stu-id="d59d8-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-250">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d59d8-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d59d8-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d59d8-252">(19)</span><span class="sxs-lookup"><span data-stu-id="d59d8-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d59d8-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d59d8-254">(20)</span><span class="sxs-lookup"><span data-stu-id="d59d8-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-255">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="d59d8-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d59d8-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d59d8-257">(21)</span><span class="sxs-lookup"><span data-stu-id="d59d8-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-258">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d59d8-258">System failure.</span></span> <span data-ttu-id="d59d8-259">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d59d8-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d59d8-260">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d59d8-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d59d8-262">(22)</span><span class="sxs-lookup"><span data-stu-id="d59d8-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-263">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d59d8-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d59d8-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d59d8-265">(23)</span><span class="sxs-lookup"><span data-stu-id="d59d8-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-266">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d59d8-266">System failure.</span></span> <span data-ttu-id="d59d8-267">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d59d8-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d59d8-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d59d8-269">(24)</span><span class="sxs-lookup"><span data-stu-id="d59d8-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-270">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="d59d8-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d59d8-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d59d8-272">(25)</span><span class="sxs-lookup"><span data-stu-id="d59d8-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-273">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d59d8-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d59d8-275">(26)</span><span class="sxs-lookup"><span data-stu-id="d59d8-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-276">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d59d8-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d59d8-278">(27)</span><span class="sxs-lookup"><span data-stu-id="d59d8-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-279">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="d59d8-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d59d8-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d59d8-281">(28)</span><span class="sxs-lookup"><span data-stu-id="d59d8-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-282">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="d59d8-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d59d8-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d59d8-284">(29)</span><span class="sxs-lookup"><span data-stu-id="d59d8-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-285">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d59d8-285">Device is disabled.</span></span> <span data-ttu-id="d59d8-286">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d59d8-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d59d8-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d59d8-288">(30)</span><span class="sxs-lookup"><span data-stu-id="d59d8-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-289">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="d59d8-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d59d8-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d59d8-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d59d8-291">31</span><span class="sxs-lookup"><span data-stu-id="d59d8-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-292">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d59d8-292">Device is not working properly.</span></span> <span data-ttu-id="d59d8-293">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d59d8-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d59d8-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d59d8-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-295">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d59d8-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-297">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d59d8-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-298">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d59d8-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d59d8-299">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d59d8-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-303">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d59d8-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-304">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="d59d8-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d59d8-305">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="d59d8-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d59d8-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-307">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d59d8-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-310">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="d59d8-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-311">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d59d8-311">Textual description of the object.</span></span>

<span data-ttu-id="d59d8-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-313">**ID**</span><span class="sxs-lookup"><span data-stu-id="d59d8-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-314">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-316">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d59d8-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-317">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d59d8-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="d59d8-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d59d8-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-320">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d59d8-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-322">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="d59d8-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="d59d8-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d59d8-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-327">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="d59d8-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="d59d8-328">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="d59d8-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-332">Cadena de forma libre que describe el tipo de detección y corrección de errores admitidos por la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d59d8-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="d59d8-333">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d59d8-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-335">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d59d8-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="d59d8-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-338">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="d59d8-338">Date and time the object was installed.</span></span> <span data-ttu-id="d59d8-339">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d59d8-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d59d8-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d59d8-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-342">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d59d8-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-344">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d59d8-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d59d8-345">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-346">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d59d8-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-349">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d59d8-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-350">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="d59d8-350">Label by which the object is known.</span></span> <span data-ttu-id="d59d8-351">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="d59d8-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d59d8-352">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="d59d8-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-354">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d59d8-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-356">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="d59d8-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-357">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d59d8-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="d59d8-358">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="d59d8-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="d59d8-359">Si el valor de **blocksize** es 1 (uno), esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d59d8-359">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="d59d8-360">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d59d8-361">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d59d8-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d59d8-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-363">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-365">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d59d8-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-366">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d59d8-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="d59d8-367">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d59d8-368">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d59d8-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d59d8-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-370">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d59d8-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-372">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d59d8-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d59d8-373">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="d59d8-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d59d8-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d59d8-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d59d8-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d59d8-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d59d8-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d59d8-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d59d8-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d59d8-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-378">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d59d8-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d59d8-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d59d8-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-380">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="d59d8-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d59d8-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="d59d8-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-382">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d59d8-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d59d8-383">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="d59d8-383">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="d59d8-384">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d59d8-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d59d8-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="d59d8-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-386">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="d59d8-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d59d8-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="d59d8-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d59d8-388">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="d59d8-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d59d8-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d59d8-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-390">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d59d8-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-392">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="d59d8-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="d59d8-393">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d59d8-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d59d8-394">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="d59d8-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="d59d8-395">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="d59d8-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="d59d8-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-397">**PSExtentInterleaveDepth**</span><span class="sxs-lookup"><span data-stu-id="d59d8-397">**PSExtentInterleaveDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-398">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d59d8-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-400">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Conjunto de volúmenes de DMTF \| \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="d59d8-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-401">Número de extensiones de espacio protegido para seccionar como conjunto colectivo.</span><span class="sxs-lookup"><span data-stu-id="d59d8-401">Number of protected space extents to stripe as a collective set.</span></span> <span data-ttu-id="d59d8-402">En SCC, este valor se define como el número de franjas que se van a contar antes de continuar con la asignación en el siguiente conjunto contiguo de extensiones, más allá de la franja actual.</span><span class="sxs-lookup"><span data-stu-id="d59d8-402">In SCC, this value is defined as the number of stripes to count before continuing to map into the next contiguous set of extents, beyond the current stripe.</span></span>

<span data-ttu-id="d59d8-403">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d59d8-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-404">**PSExtentStripeLength**</span><span class="sxs-lookup"><span data-stu-id="d59d8-404">**PSExtentStripeLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-405">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d59d8-405">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-407">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Conjunto de volúmenes de DMTF \| \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="d59d8-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-408">Número de extensiones de espacio protegido contiguas que se han contado antes de volver a la primera extensión de espacio protegido de la franja actual.</span><span class="sxs-lookup"><span data-stu-id="d59d8-408">Number of contiguous protected space extents counted before looping back to the first protected space extent of the current stripe.</span></span> <span data-ttu-id="d59d8-409">Es el número de extensiones que forman la franja de datos del usuario.</span><span class="sxs-lookup"><span data-stu-id="d59d8-409">It is the number of extents forming the user data stripe.</span></span>

<span data-ttu-id="d59d8-410">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d59d8-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-411">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="d59d8-411">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-412">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-414">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="d59d8-414">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="d59d8-415">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-415">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-416">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d59d8-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-417">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-419">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d59d8-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-420">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d59d8-420">Current status of the object.</span></span> <span data-ttu-id="d59d8-421">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d59d8-422">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d59d8-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d59d8-423">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="d59d8-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d59d8-424">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="d59d8-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d59d8-425">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d59d8-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d59d8-426">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="d59d8-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d59d8-427">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d59d8-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d59d8-428">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="d59d8-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d59d8-429">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="d59d8-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d59d8-430">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="d59d8-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d59d8-431">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="d59d8-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d59d8-432">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d59d8-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d59d8-433">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="d59d8-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d59d8-434">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="d59d8-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d59d8-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d59d8-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-436">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d59d8-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-438">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d59d8-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-439">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d59d8-439">State of the logical device.</span></span> <span data-ttu-id="d59d8-440">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="d59d8-440">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d59d8-441">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d59d8-442">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d59d8-442">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d59d8-443">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d59d8-443">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d59d8-444">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d59d8-444">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d59d8-445">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="d59d8-445">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d59d8-446">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d59d8-446">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d59d8-447">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d59d8-447">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-450">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d59d8-450">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-451">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d59d8-451">Scoping system's creation class name.</span></span>

<span data-ttu-id="d59d8-452">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d59d8-453">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d59d8-453">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d59d8-454">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d59d8-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d59d8-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d59d8-456">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d59d8-456">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d59d8-457">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d59d8-457">Scoping system's name.</span></span>

<span data-ttu-id="d59d8-458">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d59d8-459">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d59d8-459">Remarks</span></span>

<span data-ttu-id="d59d8-460">La clase **CIM \_ VolumeSet** se deriva de [**\_ StorageExtent de CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d59d8-460">The **CIM\_VolumeSet** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d59d8-461">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="d59d8-461">WMI does not implement this class.</span></span>

<span data-ttu-id="d59d8-462">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d59d8-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d59d8-463">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d59d8-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d59d8-464">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d59d8-464">Requirements</span></span>



| <span data-ttu-id="d59d8-465">Requisito</span><span class="sxs-lookup"><span data-stu-id="d59d8-465">Requirement</span></span> | <span data-ttu-id="d59d8-466">Value</span><span class="sxs-lookup"><span data-stu-id="d59d8-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d59d8-467">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d59d8-467">Minimum supported client</span></span><br/> | <span data-ttu-id="d59d8-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d59d8-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d59d8-469">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d59d8-469">Minimum supported server</span></span><br/> | <span data-ttu-id="d59d8-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d59d8-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d59d8-471">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d59d8-471">Namespace</span></span><br/>                | <span data-ttu-id="d59d8-472">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d59d8-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d59d8-473">MOF</span><span class="sxs-lookup"><span data-stu-id="d59d8-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d59d8-474"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d59d8-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d59d8-475">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d59d8-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d59d8-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d59d8-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d59d8-477">Vea también</span><span class="sxs-lookup"><span data-stu-id="d59d8-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d59d8-478">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d59d8-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

