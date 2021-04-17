---
description: La \_ clase CIM AggregatePExtent proporciona información de resumen sobre los bloques lógicos direccionables, que están en el mismo grupo de redundancia de almacenamiento y se encuentran en el mismo medio físico.
ms.assetid: c8def347-e8d7-48d5-94d0-f6e704e7b40e
ms.tgt_platform: multiple
title: CIM_AggregatePExtent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent
- CIM_AggregatePExtent.Caption
- CIM_AggregatePExtent.Description
- CIM_AggregatePExtent.InstallDate
- CIM_AggregatePExtent.Name
- CIM_AggregatePExtent.Status
- CIM_AggregatePExtent.Availability
- CIM_AggregatePExtent.ConfigManagerErrorCode
- CIM_AggregatePExtent.ConfigManagerUserConfig
- CIM_AggregatePExtent.CreationClassName
- CIM_AggregatePExtent.DeviceID
- CIM_AggregatePExtent.PowerManagementCapabilities
- CIM_AggregatePExtent.ErrorCleared
- CIM_AggregatePExtent.ErrorDescription
- CIM_AggregatePExtent.LastErrorCode
- CIM_AggregatePExtent.PNPDeviceID
- CIM_AggregatePExtent.PowerManagementSupported
- CIM_AggregatePExtent.StatusInfo
- CIM_AggregatePExtent.SystemCreationClassName
- CIM_AggregatePExtent.SystemName
- CIM_AggregatePExtent.Access
- CIM_AggregatePExtent.BlockSize
- CIM_AggregatePExtent.ErrorMethodology
- CIM_AggregatePExtent.Purpose
- CIM_AggregatePExtent.NumberOfBlocks
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2f1b2b5b7e08876317888d02d4830cd72659bc0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539081"
---
# <a name="cim_aggregatepextent-class"></a><span data-ttu-id="2e0ee-103">\_Clase AggregatePExtent de CIM</span><span class="sxs-lookup"><span data-stu-id="2e0ee-103">CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="2e0ee-104">La clase **CIM \_ AggregatePExtent** proporciona información de resumen sobre los bloques lógicos direccionables, que están en el mismo grupo de redundancia de almacenamiento y se encuentran en el mismo medio físico.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-104">The **CIM\_AggregatePExtent** class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

<span data-ttu-id="2e0ee-105">La **clase \_ AggregatePExtent de CIM** es una agrupación alternativa de extensiones físicas cuando solo se necesita información de resumen o cuando se utiliza la configuración automática.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-105">The **CIM\_AggregatePExtent** class is an alternative grouping for physical extents when only summary information is needed, or when automatic configuration is used.</span></span> <span data-ttu-id="2e0ee-106">La configuración automática puede dar lugar a que se definan miles de extensiones físicas.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-106">Automatic configuration can result in thousands of physical extents being defined.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e0ee-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e0ee-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e0ee-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2e0ee-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0ee-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e0ee-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979F-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AggregatePExtent : CIM_StorageExtent
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
  string   Purpose;
  uint64   NumberOfBlocks;
};
```

## <a name="members"></a><span data-ttu-id="2e0ee-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e0ee-112">Members</span></span>

<span data-ttu-id="2e0ee-113">La clase **CIM \_ AggregatePExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2e0ee-113">The **CIM\_AggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="2e0ee-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e0ee-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e0ee-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2e0ee-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e0ee-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="2e0ee-116">Methods</span></span>

<span data-ttu-id="2e0ee-117">La clase **CIM \_ AggregatePExtent** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-117">The **CIM\_AggregatePExtent** class has these methods.</span></span>



| <span data-ttu-id="2e0ee-118">Método</span><span class="sxs-lookup"><span data-stu-id="2e0ee-118">Method</span></span>                                                                      | <span data-ttu-id="2e0ee-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e0ee-119">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e0ee-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-120">**Reset**</span></span>](reset-method-in-class-cim-aggregatepextent.md)                 | <span data-ttu-id="2e0ee-121">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="2e0ee-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="2e0ee-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md) | <span data-ttu-id="2e0ee-124">Define el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="2e0ee-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2e0ee-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2e0ee-126">Properties</span></span>

<span data-ttu-id="2e0ee-127">La clase **CIM \_ AggregatePExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-127">The **CIM\_AggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e0ee-128">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-131">Describe las propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-131">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="2e0ee-132">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e0ee-133">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="2e0ee-134">**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="2e0ee-135">**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="2e0ee-136">**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="2e0ee-137">**Escribir una vez** (4)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e0ee-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-141">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-142">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-142">Availability and status of the device.</span></span>

<span data-ttu-id="2e0ee-143">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e0ee-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e0ee-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2e0ee-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2e0ee-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2e0ee-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2e0ee-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2e0ee-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="2e0ee-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2e0ee-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="2e0ee-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2e0ee-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2e0ee-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2e0ee-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2e0ee-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2e0ee-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-157">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2e0ee-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-159">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2e0ee-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-161">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-161">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2e0ee-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2e0ee-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-164">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2e0ee-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-166">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2e0ee-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-168">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2e0ee-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-170">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2e0ee-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-172">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e0ee-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-174">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-176">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-177">Tamaño, en bytes, de los bloques que forman la extensión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="2e0ee-178">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="2e0ee-179">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="2e0ee-180">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2e0ee-181">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-185">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-186">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-186">A short textual description of the object.</span></span>

<span data-ttu-id="2e0ee-187">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-189">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-191">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-192">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2e0ee-193">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2e0ee-194">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-194">**This device is working properly.**</span></span> <span data-ttu-id="2e0ee-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-195">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2e0ee-196">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-196">**This device is not configured correctly.**</span></span> <span data-ttu-id="2e0ee-197">(1)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-197">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e0ee-198">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-198">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2e0ee-199">(2)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2e0ee-200">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-200">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2e0ee-201">(3)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-201">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2e0ee-202">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-202">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2e0ee-203">(4)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-203">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2e0ee-204">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-204">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2e0ee-205">(5)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-205">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2e0ee-206">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-206">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2e0ee-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-207">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2e0ee-208">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-208">**Cannot filter.**</span></span> <span data-ttu-id="2e0ee-209">(7)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2e0ee-210">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-210">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2e0ee-211">(8)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-211">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2e0ee-212">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-212">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2e0ee-213">(9)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-213">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2e0ee-214">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-214">**This device cannot start.**</span></span> <span data-ttu-id="2e0ee-215">(10)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-215">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2e0ee-216">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-216">**This device failed.**</span></span> <span data-ttu-id="2e0ee-217">(11)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-217">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2e0ee-218">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-218">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2e0ee-219">(12)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-219">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2e0ee-220">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-220">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2e0ee-221">(13)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-221">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2e0ee-222">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-222">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2e0ee-223">(14)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-223">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2e0ee-224">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-224">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2e0ee-225">(15)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-225">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2e0ee-226">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-226">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2e0ee-227">(16)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-227">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2e0ee-228">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-228">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2e0ee-229">(17)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-229">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e0ee-230">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-230">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2e0ee-231">(18)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-231">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2e0ee-232">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-232">**Failure using the VxD loader.**</span></span> <span data-ttu-id="2e0ee-233">(19)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-233">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2e0ee-234">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-234">**Your registry might be corrupted.**</span></span> <span data-ttu-id="2e0ee-235">(20)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-235">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2e0ee-236">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-236">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2e0ee-237">(21)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-237">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2e0ee-238">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-238">**This device is disabled.**</span></span> <span data-ttu-id="2e0ee-239">(22)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-239">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2e0ee-240">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-240">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2e0ee-241">(23)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-241">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2e0ee-242">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-242">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2e0ee-243">(24)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-243">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2e0ee-244">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-244">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2e0ee-245">(25)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-245">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2e0ee-246">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="2e0ee-247">(26)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-247">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2e0ee-248">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-248">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2e0ee-249">(27)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-249">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2e0ee-250">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-250">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2e0ee-251">(28)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-251">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2e0ee-252">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-252">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2e0ee-253">(29)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-253">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2e0ee-254">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-254">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2e0ee-255">(30)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-255">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2e0ee-256">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-256">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2e0ee-257">31</span><span class="sxs-lookup"><span data-stu-id="2e0ee-257">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e0ee-258">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-258">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-259">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-259">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-261">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-261">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-262">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-262">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2e0ee-263">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-263">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-264">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-264">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-265">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-267">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-267">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-268">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-268">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2e0ee-269">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-269">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2e0ee-270">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-271">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-271">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-272">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-274">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-275">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-275">A textual description of the object.</span></span>

<span data-ttu-id="2e0ee-276">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-277">**ID**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-277">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-280">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-281">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-281">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="2e0ee-282">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-283">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-283">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-284">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-286">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-286">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="2e0ee-287">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-288">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-288">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-289">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-291">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-291">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="2e0ee-292">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-293">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-293">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-296">Cadena de forma libre que describe el tipo de detección y corrección de errores admitidos por la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-296">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="2e0ee-297">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-297">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-299">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-301">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-302">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-302">Indicates when the object was installed.</span></span> <span data-ttu-id="2e0ee-303">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-303">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2e0ee-304">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-305">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-305">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-306">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-308">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-308">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2e0ee-309">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-310">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-311">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-313">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-313">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-314">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-314">Label by which the object is known.</span></span> <span data-ttu-id="2e0ee-315">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-315">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2e0ee-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-317">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-317">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-318">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-318">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-320">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Extensión física de agregado DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-320">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Aggregate Physical Extent\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-321">Número total de bloques (incluidos los bloques de datos de comprobación) contenidos en esta extensión física de agregado.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-321">Total number of blocks (including the check data blocks) contained in this aggregate physical extent.</span></span> <span data-ttu-id="2e0ee-322">El tamaño del bloque (una propiedad heredada) debe establecerse en el mismo valor que para el dispositivo de acceso a medios asociado a esta extensión.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-322">The block size (an inherited property) should be set to the same value as for the media access device associated with this extent.</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-323">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-323">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-326">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-327">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-327">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2e0ee-328">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2e0ee-328">Example: "\*PNP030b"</span></span>

<span data-ttu-id="2e0ee-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-330">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-330">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-331">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-333">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-333">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="2e0ee-334">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e0ee-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-336">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-336">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2e0ee-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-338">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-338">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2e0ee-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-340">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-340">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2e0ee-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-342">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2e0ee-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-344">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2e0ee-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-346">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="2e0ee-346">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="2e0ee-347">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-347">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="2e0ee-348">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2e0ee-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-350">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="2e0ee-350">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2e0ee-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2e0ee-352">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-352">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2e0ee-353">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-353">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-354">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-356">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-356">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="2e0ee-357">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2e0ee-357">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2e0ee-358">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-358">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="2e0ee-359">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="2e0ee-359">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="2e0ee-360">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-361">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-361">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-362">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-364">Cadena de forma libre que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-364">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="2e0ee-365">Esta propiedad se hereda de [**\_ StorageExtent CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-365">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-366">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-367">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-369">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-369">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-370">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-370">String that indicates the current status of the object.</span></span> <span data-ttu-id="2e0ee-371">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-371">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2e0ee-372">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="2e0ee-372">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2e0ee-373">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-373">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2e0ee-374">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="2e0ee-374">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2e0ee-375">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-375">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2e0ee-376">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-376">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2e0ee-377">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-377">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2e0ee-378">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2e0ee-378">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2e0ee-379">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-379">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2e0ee-380">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-380">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2e0ee-381">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-381">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e0ee-382">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-382">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2e0ee-383">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-383">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2e0ee-384">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-384">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2e0ee-385">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-385">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2e0ee-386">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-386">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2e0ee-387">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-387">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2e0ee-388">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-388">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2e0ee-389">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-389">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2e0ee-390">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-390">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e0ee-391">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-391">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-392">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-394">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2e0ee-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-395">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-395">State of the logical device.</span></span> <span data-ttu-id="2e0ee-396">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="2e0ee-396">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="2e0ee-397">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2e0ee-398">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2e0ee-399">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2e0ee-400">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-400">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2e0ee-401">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-401">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2e0ee-402">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-402">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2e0ee-403">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-403">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-404">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-406">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-406">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-407">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-407">The scoping system's creation class name.</span></span>

<span data-ttu-id="2e0ee-408">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2e0ee-409">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-409">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e0ee-410">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e0ee-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e0ee-412">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-412">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e0ee-413">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-413">The scoping system's name.</span></span>

<span data-ttu-id="2e0ee-414">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e0ee-415">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e0ee-415">Remarks</span></span>

<span data-ttu-id="2e0ee-416">La clase **CIM \_ AggregatePExtent** se deriva de [**\_ StorageExtent de CIM**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="2e0ee-416">The **CIM\_AggregatePExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="2e0ee-417">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-417">WMI does not implement this class.</span></span>

<span data-ttu-id="2e0ee-418">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-418">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e0ee-419">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-419">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e0ee-420">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e0ee-420">Requirements</span></span>



| <span data-ttu-id="2e0ee-421">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e0ee-421">Requirement</span></span> | <span data-ttu-id="2e0ee-422">Value</span><span class="sxs-lookup"><span data-stu-id="2e0ee-422">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e0ee-423">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e0ee-423">Minimum supported client</span></span><br/> | <span data-ttu-id="2e0ee-424">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e0ee-424">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e0ee-425">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e0ee-425">Minimum supported server</span></span><br/> | <span data-ttu-id="2e0ee-426">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e0ee-426">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e0ee-427">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e0ee-427">Namespace</span></span><br/>                | <span data-ttu-id="2e0ee-428">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2e0ee-428">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e0ee-429">MOF</span><span class="sxs-lookup"><span data-stu-id="2e0ee-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e0ee-430"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e0ee-430"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e0ee-431">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e0ee-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e0ee-432"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e0ee-432"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e0ee-433">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e0ee-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0ee-434">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2e0ee-434">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="2e0ee-435">Clases CIM</span><span class="sxs-lookup"><span data-stu-id="2e0ee-435">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

