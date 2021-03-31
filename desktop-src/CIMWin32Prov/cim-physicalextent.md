---
description: La \_ clase CIM PhysicalExtent representa una implementación RAID de SCC.
ms.assetid: d1950464-e17a-4651-aa53-6385659994ff
ms.tgt_platform: multiple
title: CIM_PhysicalExtent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalExtent
- CIM_PhysicalExtent.Access
- CIM_PhysicalExtent.Availability
- CIM_PhysicalExtent.BlockSize
- CIM_PhysicalExtent.Caption
- CIM_PhysicalExtent.ConfigManagerErrorCode
- CIM_PhysicalExtent.ConfigManagerUserConfig
- CIM_PhysicalExtent.CreationClassName
- CIM_PhysicalExtent.Description
- CIM_PhysicalExtent.DeviceID
- CIM_PhysicalExtent.ErrorCleared
- CIM_PhysicalExtent.ErrorDescription
- CIM_PhysicalExtent.ErrorMethodology
- CIM_PhysicalExtent.InstallDate
- CIM_PhysicalExtent.LastErrorCode
- CIM_PhysicalExtent.Name
- CIM_PhysicalExtent.NumberOfBlocks
- CIM_PhysicalExtent.PNPDeviceID
- CIM_PhysicalExtent.PowerManagementCapabilities
- CIM_PhysicalExtent.PowerManagementSupported
- CIM_PhysicalExtent.Purpose
- CIM_PhysicalExtent.Status
- CIM_PhysicalExtent.StatusInfo
- CIM_PhysicalExtent.SystemCreationClassName
- CIM_PhysicalExtent.SystemName
- CIM_PhysicalExtent.UnitsBeforeCheckDataInterleave
- CIM_PhysicalExtent.UnitsOfCheckData
- CIM_PhysicalExtent.UnitsOfUserData
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 31e05d3b339d64fd640460716376c3d8b538fa95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807034"
---
# <a name="cim_physicalextent-class"></a><span data-ttu-id="55127-103">\_Clase PhysicalExtent de CIM</span><span class="sxs-lookup"><span data-stu-id="55127-103">CIM\_PhysicalExtent class</span></span>

<span data-ttu-id="55127-104">La clase **CIM \_ PhysicalExtent** representa una implementación RAID de SCC.</span><span class="sxs-lookup"><span data-stu-id="55127-104">The **CIM\_PhysicalExtent** class represents an SCC RAID implementation.</span></span> <span data-ttu-id="55127-105">Define las direcciones de bloque direccionables consecutivas en un único dispositivo de almacenamiento que se tratan como una única extensión de almacenamiento en la misma clase [**\_ StorageRedundancyGroup de CIM**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="55127-105">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="55127-106">Una alternativa, cuando se utiliza la configuración automática, es crear una instancia de la [**clase \_ AggregatePExtent de CIM**](cim-aggregatepextent.md) o extenderla.</span><span class="sxs-lookup"><span data-stu-id="55127-106">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55127-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="55127-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55127-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="55127-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55127-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="55127-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="55127-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="55127-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55127-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55127-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979E-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalExtent : CIM_StorageExtent
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
  uint64   UnitsBeforeCheckDataInterleave;
  uint64   UnitsOfCheckData;
  uint64   UnitsOfUserData;
};
```

## <a name="members"></a><span data-ttu-id="55127-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="55127-112">Members</span></span>

<span data-ttu-id="55127-113">La clase **CIM \_ PhysicalExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="55127-113">The **CIM\_PhysicalExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="55127-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="55127-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="55127-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55127-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="55127-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="55127-116">Methods</span></span>

<span data-ttu-id="55127-117">La clase **CIM \_ PhysicalExtent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="55127-117">The **CIM\_PhysicalExtent** class has these methods.</span></span>



| <span data-ttu-id="55127-118">Método</span><span class="sxs-lookup"><span data-stu-id="55127-118">Method</span></span>                                                                    | <span data-ttu-id="55127-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="55127-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55127-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="55127-120">**Reset**</span></span>](reset-method-in-class-cim-physicalextent.md)                 | <span data-ttu-id="55127-121">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="55127-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="55127-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="55127-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="55127-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="55127-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-physicalextent.md) | <span data-ttu-id="55127-124">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="55127-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="55127-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="55127-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="55127-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55127-126">Properties</span></span>

<span data-ttu-id="55127-127">La clase **CIM \_ PhysicalExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="55127-127">The **CIM\_PhysicalExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55127-128">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="55127-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55127-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55127-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55127-131">Propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="55127-131">Read/write properties of the media.</span></span>

<span data-ttu-id="55127-132">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="55127-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55127-133">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="55127-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="55127-134">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="55127-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="55127-135">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="55127-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="55127-136">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="55127-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="55127-137">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="55127-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55127-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="55127-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55127-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55127-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-141">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="55127-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="55127-142">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-142">Availability and status of the device.</span></span>

<span data-ttu-id="55127-143">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55127-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="55127-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55127-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="55127-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="55127-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="55127-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="55127-147">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="55127-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="55127-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="55127-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="55127-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="55127-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="55127-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="55127-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="55127-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="55127-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="55127-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="55127-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="55127-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="55127-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="55127-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="55127-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="55127-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="55127-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="55127-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="55127-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="55127-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="55127-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="55127-158">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="55127-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="55127-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="55127-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="55127-160">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="55127-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="55127-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="55127-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="55127-162">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="55127-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="55127-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="55127-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="55127-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="55127-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="55127-165">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="55127-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="55127-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="55127-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="55127-167">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="55127-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="55127-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="55127-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="55127-169">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="55127-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="55127-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="55127-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="55127-171">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="55127-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="55127-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="55127-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="55127-173">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="55127-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="55127-174">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="55127-174">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-175">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55127-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55127-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-177">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("blocksize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensión física de DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="55127-177">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BlockSize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="55127-178">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="55127-178">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="55127-179">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="55127-179">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="55127-180">Si el tamaño de bloque es desconocido o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="55127-180">If the block size is unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one) .</span></span>

<span data-ttu-id="55127-181">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="55127-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="55127-182">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55127-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="55127-183">**Caption**</span><span class="sxs-lookup"><span data-stu-id="55127-183">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-186">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="55127-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="55127-187">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="55127-187">Short textual description of the object.</span></span>

<span data-ttu-id="55127-188">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55127-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-189">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="55127-189">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-190">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55127-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55127-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-192">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="55127-192">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="55127-193">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="55127-193">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="55127-194">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="55127-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="55127-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="55127-196"> (0)</span><span class="sxs-lookup"><span data-stu-id="55127-196">(0)</span></span>


</dt> <dd>

<span data-ttu-id="55127-197">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="55127-197">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="55127-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="55127-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="55127-199">(1)</span><span class="sxs-lookup"><span data-stu-id="55127-199">(1)</span></span>


</dt> <dd>

<span data-ttu-id="55127-200">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="55127-200">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="55127-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="55127-202">(2)</span><span class="sxs-lookup"><span data-stu-id="55127-202">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="55127-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="55127-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="55127-204">(3)</span><span class="sxs-lookup"><span data-stu-id="55127-204">(3)</span></span>


</dt> <dd>

<span data-ttu-id="55127-205">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="55127-205">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="55127-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="55127-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="55127-207">(4)</span><span class="sxs-lookup"><span data-stu-id="55127-207">(4)</span></span>


</dt> <dd>

<span data-ttu-id="55127-208">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="55127-208">Device is not working properly.</span></span> <span data-ttu-id="55127-209">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="55127-209">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="55127-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="55127-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="55127-211">(5)</span><span class="sxs-lookup"><span data-stu-id="55127-211">(5)</span></span>


</dt> <dd>

<span data-ttu-id="55127-212">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="55127-212">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="55127-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="55127-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="55127-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="55127-214">(6)</span></span>


</dt> <dd>

<span data-ttu-id="55127-215">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="55127-215">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="55127-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="55127-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="55127-217">(7)</span><span class="sxs-lookup"><span data-stu-id="55127-217">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="55127-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="55127-219">(8)</span><span class="sxs-lookup"><span data-stu-id="55127-219">(8)</span></span>


</dt> <dd>

<span data-ttu-id="55127-220">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-220">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="55127-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="55127-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="55127-222">(9)</span><span class="sxs-lookup"><span data-stu-id="55127-222">(9)</span></span>


</dt> <dd>

<span data-ttu-id="55127-223">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="55127-223">Device is not working properly.</span></span> <span data-ttu-id="55127-224">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-224">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="55127-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="55127-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="55127-226">(10)</span><span class="sxs-lookup"><span data-stu-id="55127-226">(10)</span></span>


</dt> <dd>

<span data-ttu-id="55127-227">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="55127-227">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="55127-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="55127-229">(11)</span><span class="sxs-lookup"><span data-stu-id="55127-229">(11)</span></span>


</dt> <dd>

<span data-ttu-id="55127-230">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-230">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="55127-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="55127-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="55127-232">(12)</span><span class="sxs-lookup"><span data-stu-id="55127-232">(12)</span></span>


</dt> <dd>

<span data-ttu-id="55127-233">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="55127-233">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="55127-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="55127-235">(13)</span><span class="sxs-lookup"><span data-stu-id="55127-235">(13)</span></span>


</dt> <dd>

<span data-ttu-id="55127-236">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-236">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="55127-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="55127-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="55127-238">(14)</span><span class="sxs-lookup"><span data-stu-id="55127-238">(14)</span></span>


</dt> <dd>

<span data-ttu-id="55127-239">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="55127-239">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="55127-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="55127-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="55127-241">(15)</span><span class="sxs-lookup"><span data-stu-id="55127-241">(15)</span></span>


</dt> <dd>

<span data-ttu-id="55127-242">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="55127-242">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="55127-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="55127-244">(16)</span><span class="sxs-lookup"><span data-stu-id="55127-244">(16)</span></span>


</dt> <dd>

<span data-ttu-id="55127-245">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-245">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="55127-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="55127-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="55127-247">(17)</span><span class="sxs-lookup"><span data-stu-id="55127-247">(17)</span></span>


</dt> <dd>

<span data-ttu-id="55127-248">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="55127-248">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="55127-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="55127-250">(18)</span><span class="sxs-lookup"><span data-stu-id="55127-250">(18)</span></span>


</dt> <dd>

<span data-ttu-id="55127-251">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="55127-251">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="55127-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="55127-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="55127-253">(19)</span><span class="sxs-lookup"><span data-stu-id="55127-253">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="55127-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="55127-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="55127-255">(20)</span><span class="sxs-lookup"><span data-stu-id="55127-255">(20)</span></span>


</dt> <dd>

<span data-ttu-id="55127-256">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="55127-256">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="55127-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="55127-258">(21)</span><span class="sxs-lookup"><span data-stu-id="55127-258">(21)</span></span>


</dt> <dd>

<span data-ttu-id="55127-259">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="55127-259">System failure.</span></span> <span data-ttu-id="55127-260">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="55127-260">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="55127-261">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-261">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="55127-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="55127-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="55127-263">(22)</span><span class="sxs-lookup"><span data-stu-id="55127-263">(22)</span></span>


</dt> <dd>

<span data-ttu-id="55127-264">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="55127-264">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="55127-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="55127-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="55127-266">(23)</span><span class="sxs-lookup"><span data-stu-id="55127-266">(23)</span></span>


</dt> <dd>

<span data-ttu-id="55127-267">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="55127-267">System failure.</span></span> <span data-ttu-id="55127-268">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="55127-268">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="55127-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="55127-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="55127-270">(24)</span><span class="sxs-lookup"><span data-stu-id="55127-270">(24)</span></span>


</dt> <dd>

<span data-ttu-id="55127-271">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="55127-271">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="55127-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="55127-273">(25)</span><span class="sxs-lookup"><span data-stu-id="55127-273">(25)</span></span>


</dt> <dd>

<span data-ttu-id="55127-274">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="55127-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="55127-276">(26)</span><span class="sxs-lookup"><span data-stu-id="55127-276">(26)</span></span>


</dt> <dd>

<span data-ttu-id="55127-277">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="55127-277">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="55127-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="55127-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="55127-279">(27)</span><span class="sxs-lookup"><span data-stu-id="55127-279">(27)</span></span>


</dt> <dd>

<span data-ttu-id="55127-280">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="55127-280">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="55127-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="55127-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="55127-282">(28)</span><span class="sxs-lookup"><span data-stu-id="55127-282">(28)</span></span>


</dt> <dd>

<span data-ttu-id="55127-283">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="55127-283">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="55127-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="55127-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="55127-285">(29)</span><span class="sxs-lookup"><span data-stu-id="55127-285">(29)</span></span>


</dt> <dd>

<span data-ttu-id="55127-286">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="55127-286">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="55127-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="55127-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="55127-288">(30)</span><span class="sxs-lookup"><span data-stu-id="55127-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="55127-289">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="55127-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="55127-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="55127-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="55127-291">31</span><span class="sxs-lookup"><span data-stu-id="55127-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="55127-292">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="55127-292">Device is not working properly.</span></span> <span data-ttu-id="55127-293">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="55127-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="55127-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="55127-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-295">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="55127-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55127-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-297">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="55127-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="55127-298">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="55127-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="55127-299">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="55127-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-303">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="55127-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="55127-304">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="55127-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="55127-305">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="55127-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="55127-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-307">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="55127-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-310">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="55127-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="55127-311">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="55127-311">Textual description of the object.</span></span>

<span data-ttu-id="55127-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55127-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-313">**ID**</span><span class="sxs-lookup"><span data-stu-id="55127-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-314">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-316">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="55127-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="55127-317">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="55127-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="55127-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-319">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="55127-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-320">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="55127-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55127-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55127-322">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="55127-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="55127-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="55127-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55127-327">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="55127-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="55127-328">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-329">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="55127-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-330">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55127-332">Cadena de forma libre que describe el tipo de detección y corrección de errores admitidos por la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="55127-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="55127-333">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="55127-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="55127-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-335">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="55127-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="55127-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="55127-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="55127-338">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="55127-338">Date and time the object was installed.</span></span> <span data-ttu-id="55127-339">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="55127-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="55127-340">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55127-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-341">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="55127-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-342">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="55127-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="55127-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55127-344">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="55127-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="55127-345">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-346">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="55127-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-347">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-349">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="55127-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="55127-350">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="55127-350">Label by which the object is known.</span></span> <span data-ttu-id="55127-351">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="55127-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="55127-352">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55127-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="55127-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-354">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55127-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55127-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-356">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensión física de DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="55127-356">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="55127-357">Número total de bloques consecutivos; cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que constituye esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="55127-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="55127-358">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="55127-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="55127-359">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="55127-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="55127-360">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="55127-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="55127-361">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55127-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="55127-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="55127-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-363">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-365">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="55127-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="55127-366">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="55127-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="55127-367">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="55127-368">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="55127-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="55127-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="55127-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-370">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55127-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="55127-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55127-372">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="55127-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="55127-373">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="55127-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55127-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="55127-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="55127-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="55127-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="55127-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="55127-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="55127-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="55127-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="55127-378">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="55127-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="55127-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="55127-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="55127-380">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="55127-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="55127-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="55127-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="55127-382">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="55127-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="55127-383">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="55127-383">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="55127-384">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="55127-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="55127-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="55127-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="55127-386">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="55127-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="55127-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="55127-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="55127-388">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="55127-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="55127-389">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="55127-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-390">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="55127-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55127-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55127-392">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="55127-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="55127-393">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="55127-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="55127-394">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="55127-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="55127-395">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="55127-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="55127-396">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-397">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="55127-397">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-398">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55127-400">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="55127-400">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="55127-401">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="55127-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-402">**Estado**</span><span class="sxs-lookup"><span data-stu-id="55127-402">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-405">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="55127-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="55127-406">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="55127-406">Current status of the object.</span></span>

<span data-ttu-id="55127-407">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="55127-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="55127-408">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="55127-408">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="55127-409">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="55127-409">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="55127-410">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="55127-410">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="55127-411">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="55127-411">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55127-412">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="55127-412">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="55127-413">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="55127-413">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="55127-414">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="55127-414">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="55127-415">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="55127-415">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="55127-416">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="55127-416">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="55127-417">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="55127-417">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="55127-418">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="55127-418">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="55127-419">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="55127-419">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="55127-420">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="55127-420">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55127-421">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="55127-421">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-422">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55127-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55127-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-424">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="55127-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="55127-425">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="55127-425">State of the logical device.</span></span> <span data-ttu-id="55127-426">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="55127-426">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="55127-427">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55127-428">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="55127-428">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55127-429">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="55127-429">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="55127-430">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="55127-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="55127-431">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="55127-431">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="55127-432">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="55127-432">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55127-433">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="55127-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-436">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="55127-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="55127-437">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="55127-437">Scoping system's creation class name.</span></span>

<span data-ttu-id="55127-438">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="55127-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-440">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55127-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55127-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-442">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="55127-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="55127-443">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="55127-443">Scoping system's name.</span></span>

<span data-ttu-id="55127-444">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="55127-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="55127-445">**UnitsBeforeCheckDataInterleave**</span><span class="sxs-lookup"><span data-stu-id="55127-445">**UnitsBeforeCheckDataInterleave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-446">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55127-446">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55127-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-448">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensión física \| de DMTF 001,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="55127-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="55127-449">Número de bytes de datos de usuario que se omiten antes de iniciar la intercalación de datos de comprobación.</span><span class="sxs-lookup"><span data-stu-id="55127-449">Number of user data bytes to skip before starting the check-data interleave.</span></span>

<span data-ttu-id="55127-450">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55127-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="55127-451">**UnitsOfCheckData**</span><span class="sxs-lookup"><span data-stu-id="55127-451">**UnitsOfCheckData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-452">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55127-452">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55127-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-454">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensión física \| de DMTF 001,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="55127-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="55127-455">Número de bytes que se van a reservar para comprobar los datos.</span><span class="sxs-lookup"><span data-stu-id="55127-455">Number of bytes to be reserved for check data.</span></span>

<span data-ttu-id="55127-456">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55127-456">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="55127-457">**UnitsOfUserData**</span><span class="sxs-lookup"><span data-stu-id="55127-457">**UnitsOfUserData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55127-458">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55127-458">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55127-459">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55127-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55127-460">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensión física \| de DMTF 001,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="55127-460">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="55127-461">Número de bytes que se van a reservar para los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="55127-461">Number of bytes to be reserved for user data.</span></span>

<span data-ttu-id="55127-462">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55127-462">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55127-463">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55127-463">Remarks</span></span>

<span data-ttu-id="55127-464">La clase **CIM \_ PhysicalExtent** se deriva de [**\_ StorageExtent de CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="55127-464">The **CIM\_PhysicalExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="55127-465">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="55127-465">WMI does not implement this class.</span></span>

<span data-ttu-id="55127-466">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="55127-466">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55127-467">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="55127-467">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55127-468">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55127-468">Requirements</span></span>



| <span data-ttu-id="55127-469">Requisito</span><span class="sxs-lookup"><span data-stu-id="55127-469">Requirement</span></span> | <span data-ttu-id="55127-470">Value</span><span class="sxs-lookup"><span data-stu-id="55127-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55127-471">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55127-471">Minimum supported client</span></span><br/> | <span data-ttu-id="55127-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55127-472">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55127-473">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55127-473">Minimum supported server</span></span><br/> | <span data-ttu-id="55127-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55127-474">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55127-475">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="55127-475">Namespace</span></span><br/>                | <span data-ttu-id="55127-476">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="55127-476">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55127-477">MOF</span><span class="sxs-lookup"><span data-stu-id="55127-477">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55127-478"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55127-478"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55127-479">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55127-479">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55127-480"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55127-480"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55127-481">Vea también</span><span class="sxs-lookup"><span data-stu-id="55127-481">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55127-482">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="55127-482">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

