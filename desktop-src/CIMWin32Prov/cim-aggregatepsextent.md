---
description: La \_ clase CIM AggregatePSExtent define el número de bloques lógicos direccionables en un único dispositivo de almacenamiento, excluidos los bloques lógicos asignados como datos de comprobación.
ms.assetid: 6c188955-a963-414d-94f9-b7e1cb5960ed
ms.tgt_platform: multiple
title: CIM_AggregatePSExtent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent
- CIM_AggregatePSExtent.Caption
- CIM_AggregatePSExtent.Description
- CIM_AggregatePSExtent.InstallDate
- CIM_AggregatePSExtent.Name
- CIM_AggregatePSExtent.Status
- CIM_AggregatePSExtent.Availability
- CIM_AggregatePSExtent.ConfigManagerErrorCode
- CIM_AggregatePSExtent.ConfigManagerUserConfig
- CIM_AggregatePSExtent.CreationClassName
- CIM_AggregatePSExtent.DeviceID
- CIM_AggregatePSExtent.PowerManagementCapabilities
- CIM_AggregatePSExtent.ErrorCleared
- CIM_AggregatePSExtent.ErrorDescription
- CIM_AggregatePSExtent.LastErrorCode
- CIM_AggregatePSExtent.PNPDeviceID
- CIM_AggregatePSExtent.PowerManagementSupported
- CIM_AggregatePSExtent.StatusInfo
- CIM_AggregatePSExtent.SystemCreationClassName
- CIM_AggregatePSExtent.SystemName
- CIM_AggregatePSExtent.Access
- CIM_AggregatePSExtent.BlockSize
- CIM_AggregatePSExtent.ErrorMethodology
- CIM_AggregatePSExtent.NumberOfBlocks
- CIM_AggregatePSExtent.Purpose
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: edc3f5b91bc39e18321778dbfdbc53446c6c27d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807688"
---
# <a name="cim_aggregatepsextent-class"></a><span data-ttu-id="5556a-103">\_Clase AggregatePSExtent de CIM</span><span class="sxs-lookup"><span data-stu-id="5556a-103">CIM\_AggregatePSExtent class</span></span>

<span data-ttu-id="5556a-104">La clase **CIM \_ AggregatePSExtent** define el número de bloques lógicos direccionables en un único dispositivo de almacenamiento, excluidos los bloques lógicos asignados como datos de comprobación.</span><span class="sxs-lookup"><span data-stu-id="5556a-104">The **CIM\_AggregatePSExtent** class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="5556a-105">Si se definen conjuntos de volúmenes, los bloques lógicos se incluyen en un único conjunto de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="5556a-105">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="5556a-106">Se trata de una agrupación alternativa para [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md), cuando solo se necesita información de resumen o cuando se usa la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="5556a-106">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

<span data-ttu-id="5556a-107">La configuración automática puede dar lugar a que se definan miles de clases [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) .</span><span class="sxs-lookup"><span data-stu-id="5556a-107">Automatic configuration can result in thousands of [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) classes being defined.</span></span> <span data-ttu-id="5556a-108">La clase **CIM \_ AggregatePSExtent** se ha definido para que no sea necesario modelar las extensiones individuales.</span><span class="sxs-lookup"><span data-stu-id="5556a-108">The **CIM\_AggregatePSExtent** class was defined so that individual extents would not have to be modeled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5556a-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5556a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5556a-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5556a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5556a-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5556a-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5556a-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5556a-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5556a-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5556a-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D0E255C-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AggregatePSExtent : CIM_StorageExtent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  string   ErrorMethodology;
  uint64   NumberOfBlocks;
  string   Purpose;
};
```

## <a name="members"></a><span data-ttu-id="5556a-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="5556a-114">Members</span></span>

<span data-ttu-id="5556a-115">La clase **CIM \_ AggregatePSExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5556a-115">The **CIM\_AggregatePSExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="5556a-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5556a-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="5556a-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5556a-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5556a-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="5556a-118">Methods</span></span>

<span data-ttu-id="5556a-119">La clase **CIM \_ AggregatePSExtent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5556a-119">The **CIM\_AggregatePSExtent** class has these methods.</span></span>



| <span data-ttu-id="5556a-120">Método</span><span class="sxs-lookup"><span data-stu-id="5556a-120">Method</span></span>                                                                       | <span data-ttu-id="5556a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="5556a-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5556a-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5556a-122">**Reset**</span></span>](reset-method-in-class-cim-aggregatepsextent.md)                 | <span data-ttu-id="5556a-123">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5556a-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="5556a-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="5556a-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="5556a-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5556a-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepsextent.md) | <span data-ttu-id="5556a-126">Define el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.</span><span class="sxs-lookup"><span data-stu-id="5556a-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="5556a-127">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="5556a-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5556a-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5556a-128">Properties</span></span>

<span data-ttu-id="5556a-129">La clase **CIM \_ AggregatePSExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5556a-129">The **CIM\_AggregatePSExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5556a-130">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="5556a-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5556a-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5556a-133">Describe las propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="5556a-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="5556a-134">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5556a-135">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5556a-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="5556a-136">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="5556a-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="5556a-137">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="5556a-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="5556a-138">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="5556a-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="5556a-139">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="5556a-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5556a-140">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="5556a-140">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5556a-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-143">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5556a-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-144">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5556a-144">Availability and status of the device.</span></span>

<span data-ttu-id="5556a-145">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-145">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5556a-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5556a-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5556a-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5556a-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5556a-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5556a-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5556a-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="5556a-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5556a-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="5556a-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5556a-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="5556a-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5556a-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="5556a-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5556a-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="5556a-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5556a-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="5556a-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5556a-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5556a-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5556a-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5556a-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5556a-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="5556a-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5556a-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="5556a-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-159">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="5556a-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5556a-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="5556a-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-161">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="5556a-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5556a-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5556a-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-163">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="5556a-163">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5556a-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="5556a-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5556a-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="5556a-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-166">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5556a-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5556a-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5556a-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-168">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="5556a-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5556a-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="5556a-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-170">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="5556a-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5556a-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5556a-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-172">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="5556a-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5556a-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="5556a-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-174">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="5556a-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5556a-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="5556a-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-176">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5556a-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-178">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="5556a-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-179">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5556a-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="5556a-180">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="5556a-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="5556a-181">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="5556a-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="5556a-182">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5556a-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5556a-183">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-183">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5556a-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-187">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5556a-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-188">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5556a-188">A short textual description of the object.</span></span>

<span data-ttu-id="5556a-189">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-190">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5556a-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-191">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5556a-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-193">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5556a-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-194">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="5556a-194">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5556a-195">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5556a-196">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5556a-196">**This device is working properly.**</span></span> <span data-ttu-id="5556a-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="5556a-197">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5556a-198">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5556a-198">**This device is not configured correctly.**</span></span> <span data-ttu-id="5556a-199">(1)</span><span class="sxs-lookup"><span data-stu-id="5556a-199">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5556a-200">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-200">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5556a-201">(2)</span><span class="sxs-lookup"><span data-stu-id="5556a-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5556a-202">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5556a-202">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5556a-203">(3)</span><span class="sxs-lookup"><span data-stu-id="5556a-203">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5556a-204">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="5556a-204">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5556a-205">(4)</span><span class="sxs-lookup"><span data-stu-id="5556a-205">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5556a-206">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="5556a-206">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5556a-207">(5)</span><span class="sxs-lookup"><span data-stu-id="5556a-207">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5556a-208">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5556a-208">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5556a-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="5556a-209">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5556a-210">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5556a-210">**Cannot filter.**</span></span> <span data-ttu-id="5556a-211">(7)</span><span class="sxs-lookup"><span data-stu-id="5556a-211">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5556a-212">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-212">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5556a-213">(8)</span><span class="sxs-lookup"><span data-stu-id="5556a-213">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5556a-214">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="5556a-214">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5556a-215">(9)</span><span class="sxs-lookup"><span data-stu-id="5556a-215">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5556a-216">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="5556a-216">**This device cannot start.**</span></span> <span data-ttu-id="5556a-217">(10)</span><span class="sxs-lookup"><span data-stu-id="5556a-217">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5556a-218">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-218">**This device failed.**</span></span> <span data-ttu-id="5556a-219">(11)</span><span class="sxs-lookup"><span data-stu-id="5556a-219">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5556a-220">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="5556a-220">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5556a-221">(12)</span><span class="sxs-lookup"><span data-stu-id="5556a-221">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5556a-222">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-222">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5556a-223">(13)</span><span class="sxs-lookup"><span data-stu-id="5556a-223">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5556a-224">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-224">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5556a-225">(14)</span><span class="sxs-lookup"><span data-stu-id="5556a-225">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5556a-226">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="5556a-226">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5556a-227">(15)</span><span class="sxs-lookup"><span data-stu-id="5556a-227">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5556a-228">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-228">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5556a-229">(16)</span><span class="sxs-lookup"><span data-stu-id="5556a-229">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5556a-230">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="5556a-230">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5556a-231">(17)</span><span class="sxs-lookup"><span data-stu-id="5556a-231">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5556a-232">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-232">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5556a-233">(18)</span><span class="sxs-lookup"><span data-stu-id="5556a-233">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5556a-234">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="5556a-234">**Failure using the VxD loader.**</span></span> <span data-ttu-id="5556a-235">(19)</span><span class="sxs-lookup"><span data-stu-id="5556a-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5556a-236">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="5556a-236">**Your registry might be corrupted.**</span></span> <span data-ttu-id="5556a-237">(20)</span><span class="sxs-lookup"><span data-stu-id="5556a-237">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5556a-238">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-238">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5556a-239">(21)</span><span class="sxs-lookup"><span data-stu-id="5556a-239">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5556a-240">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5556a-240">**This device is disabled.**</span></span> <span data-ttu-id="5556a-241">(22)</span><span class="sxs-lookup"><span data-stu-id="5556a-241">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5556a-242">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="5556a-242">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5556a-243">(23)</span><span class="sxs-lookup"><span data-stu-id="5556a-243">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5556a-244">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="5556a-244">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5556a-245">(24)</span><span class="sxs-lookup"><span data-stu-id="5556a-245">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5556a-246">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="5556a-247">(25)</span><span class="sxs-lookup"><span data-stu-id="5556a-247">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5556a-248">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-248">**Windows is still setting up this device.**</span></span> <span data-ttu-id="5556a-249">(26)</span><span class="sxs-lookup"><span data-stu-id="5556a-249">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5556a-250">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="5556a-250">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5556a-251">(27)</span><span class="sxs-lookup"><span data-stu-id="5556a-251">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5556a-252">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="5556a-252">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5556a-253">(28)</span><span class="sxs-lookup"><span data-stu-id="5556a-253">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5556a-254">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="5556a-254">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5556a-255">(29)</span><span class="sxs-lookup"><span data-stu-id="5556a-255">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5556a-256">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5556a-256">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5556a-257">(30)</span><span class="sxs-lookup"><span data-stu-id="5556a-257">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5556a-258">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5556a-258">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5556a-259">31</span><span class="sxs-lookup"><span data-stu-id="5556a-259">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5556a-260">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5556a-260">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-261">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5556a-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-263">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5556a-263">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-264">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5556a-264">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5556a-265">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-266">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5556a-266">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-267">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-269">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5556a-269">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5556a-270">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5556a-270">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5556a-271">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="5556a-271">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5556a-272">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-273">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5556a-273">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-276">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="5556a-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-277">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5556a-277">A textual description of the object.</span></span>

<span data-ttu-id="5556a-278">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-278">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-279">**ID**</span><span class="sxs-lookup"><span data-stu-id="5556a-279">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-282">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5556a-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5556a-283">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5556a-283">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="5556a-284">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-285">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5556a-285">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-286">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5556a-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5556a-288">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="5556a-288">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="5556a-289">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-290">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5556a-290">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-291">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5556a-293">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="5556a-293">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="5556a-294">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-295">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="5556a-295">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5556a-298">Cadena de forma libre que describe el tipo de detección y corrección de errores admitidos por la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5556a-298">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="5556a-299">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-299">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5556a-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-301">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5556a-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-303">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="5556a-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-304">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5556a-304">Indicates when the object was installed.</span></span> <span data-ttu-id="5556a-305">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="5556a-305">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5556a-306">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-307">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5556a-307">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-308">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5556a-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5556a-310">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5556a-310">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5556a-311">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-312">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5556a-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-315">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5556a-315">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-316">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="5556a-316">Label by which the object is known.</span></span> <span data-ttu-id="5556a-317">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="5556a-317">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5556a-318">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-319">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="5556a-319">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-320">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5556a-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-322">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="5556a-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-323">Número de bloques consecutivos, cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5556a-323">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="5556a-324">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="5556a-324">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="5556a-325">Si el valor de **blocksize** es 1 (uno), esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5556a-325">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="5556a-326">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="5556a-326">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="5556a-327">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-327">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-328">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5556a-328">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-331">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5556a-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-332">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5556a-332">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5556a-333">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5556a-333">Example: "\*PNP030b"</span></span>

<span data-ttu-id="5556a-334">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-335">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5556a-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-336">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5556a-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5556a-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5556a-338">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5556a-338">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="5556a-339">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5556a-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5556a-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-341">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="5556a-341">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5556a-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="5556a-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-343">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5556a-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5556a-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5556a-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-345">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="5556a-345">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5556a-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5556a-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-347">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5556a-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5556a-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5556a-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-349">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="5556a-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5556a-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="5556a-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-351">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="5556a-351">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="5556a-352">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="5556a-352">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="5556a-353">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5556a-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5556a-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="5556a-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-355">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="5556a-355">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5556a-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="5556a-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5556a-357">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="5556a-357">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5556a-358">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5556a-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-359">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5556a-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5556a-361">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5556a-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="5556a-362">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5556a-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5556a-363">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="5556a-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="5556a-364">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="5556a-364">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="5556a-365">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-366">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="5556a-366">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5556a-369">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="5556a-369">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="5556a-370">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-370">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-371">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5556a-371">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-372">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-374">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5556a-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-375">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5556a-375">String that indicates the current status of the object.</span></span> <span data-ttu-id="5556a-376">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="5556a-376">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="5556a-377">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="5556a-377">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="5556a-378">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="5556a-378">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="5556a-379">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="5556a-379">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5556a-380">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="5556a-380">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5556a-381">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="5556a-381">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5556a-382">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-382">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5556a-383">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5556a-383">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5556a-384">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="5556a-384">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5556a-385">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5556a-385">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5556a-386">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5556a-386">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5556a-387">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="5556a-387">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5556a-388">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5556a-388">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5556a-389">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="5556a-389">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5556a-390">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="5556a-390">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5556a-391">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="5556a-391">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5556a-392">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="5556a-392">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5556a-393">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5556a-393">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5556a-394">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="5556a-394">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5556a-395">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="5556a-395">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5556a-396">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5556a-396">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-397">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5556a-397">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-399">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5556a-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5556a-400">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5556a-400">State of the logical device.</span></span> <span data-ttu-id="5556a-401">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="5556a-401">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="5556a-402">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5556a-403">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5556a-403">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5556a-404">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5556a-404">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5556a-405">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5556a-405">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5556a-406">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5556a-406">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5556a-407">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="5556a-407">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5556a-408">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5556a-408">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-409">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-411">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5556a-411">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5556a-412">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5556a-412">The scoping system's creation class name.</span></span>

<span data-ttu-id="5556a-413">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5556a-414">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5556a-414">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5556a-415">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5556a-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5556a-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5556a-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5556a-417">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5556a-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5556a-418">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5556a-418">The scoping system's name.</span></span>

<span data-ttu-id="5556a-419">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5556a-420">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5556a-420">Remarks</span></span>

<span data-ttu-id="5556a-421">La clase **CIM \_ AggregatePSExtent** se deriva de [**\_ StorageExtent de CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="5556a-421">The **CIM\_AggregatePSExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="5556a-422">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5556a-422">WMI does not implement this class.</span></span>

<span data-ttu-id="5556a-423">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5556a-423">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5556a-424">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5556a-424">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5556a-425">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5556a-425">Requirements</span></span>



| <span data-ttu-id="5556a-426">Requisito</span><span class="sxs-lookup"><span data-stu-id="5556a-426">Requirement</span></span> | <span data-ttu-id="5556a-427">Value</span><span class="sxs-lookup"><span data-stu-id="5556a-427">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5556a-428">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5556a-428">Minimum supported client</span></span><br/> | <span data-ttu-id="5556a-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5556a-429">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5556a-430">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5556a-430">Minimum supported server</span></span><br/> | <span data-ttu-id="5556a-431">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5556a-431">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5556a-432">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5556a-432">Namespace</span></span><br/>                | <span data-ttu-id="5556a-433">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5556a-433">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5556a-434">MOF</span><span class="sxs-lookup"><span data-stu-id="5556a-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5556a-435"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5556a-435"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5556a-436">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5556a-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5556a-437"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5556a-437"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5556a-438">Vea también</span><span class="sxs-lookup"><span data-stu-id="5556a-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5556a-439">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5556a-439">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="5556a-440">Clases CIM</span><span class="sxs-lookup"><span data-stu-id="5556a-440">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

