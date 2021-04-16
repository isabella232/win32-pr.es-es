---
description: La \_ clase CIM UninterruptiblePowerSupply representa las capacidades y la administración de un sistema de alimentación ininterrumpida (SAI).
ms.assetid: 27ddc955-906b-40b9-981b-96872356477c
ms.tgt_platform: multiple
title: CIM_UninterruptiblePowerSupply (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UninterruptiblePowerSupply
- CIM_UninterruptiblePowerSupply.ActiveInputVoltage
- CIM_UninterruptiblePowerSupply.Availability
- CIM_UninterruptiblePowerSupply.Caption
- CIM_UninterruptiblePowerSupply.ConfigManagerErrorCode
- CIM_UninterruptiblePowerSupply.ConfigManagerUserConfig
- CIM_UninterruptiblePowerSupply.CreationClassName
- CIM_UninterruptiblePowerSupply.Description
- CIM_UninterruptiblePowerSupply.DeviceID
- CIM_UninterruptiblePowerSupply.ErrorCleared
- CIM_UninterruptiblePowerSupply.ErrorDescription
- CIM_UninterruptiblePowerSupply.EstimatedChargeRemaining
- CIM_UninterruptiblePowerSupply.EstimatedRunTime
- CIM_UninterruptiblePowerSupply.InstallDate
- CIM_UninterruptiblePowerSupply.IsSwitchingSupply
- CIM_UninterruptiblePowerSupply.LastErrorCode
- CIM_UninterruptiblePowerSupply.Name
- CIM_UninterruptiblePowerSupply.PNPDeviceID
- CIM_UninterruptiblePowerSupply.PowerManagementCapabilities
- CIM_UninterruptiblePowerSupply.PowerManagementSupported
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range1InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range1InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range1InputVoltageLow
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyHigh
- CIM_UninterruptiblePowerSupply.Range2InputFrequencyLow
- CIM_UninterruptiblePowerSupply.Range2InputVoltageHigh
- CIM_UninterruptiblePowerSupply.Range2InputVoltageLow
- CIM_UninterruptiblePowerSupply.RemainingCapacityStatus
- CIM_UninterruptiblePowerSupply.Status
- CIM_UninterruptiblePowerSupply.StatusInfo
- CIM_UninterruptiblePowerSupply.SystemCreationClassName
- CIM_UninterruptiblePowerSupply.SystemName
- CIM_UninterruptiblePowerSupply.TimeOnBackup
- CIM_UninterruptiblePowerSupply.TotalOutputPower
- CIM_UninterruptiblePowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 214517fd6518cf2ca406523c61f522ae9c1adc46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659412"
---
# <a name="cim_uninterruptiblepowersupply-class"></a><span data-ttu-id="aea59-103">\_Clase UninterruptiblePowerSupply de CIM</span><span class="sxs-lookup"><span data-stu-id="aea59-103">CIM\_UninterruptiblePowerSupply class</span></span>

<span data-ttu-id="aea59-104">La clase **CIM \_ UninterruptiblePowerSupply** representa las capacidades y la administración de un sistema de alimentación ininterrumpida (SAI).</span><span class="sxs-lookup"><span data-stu-id="aea59-104">The **CIM\_UninterruptiblePowerSupply** class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span> <span data-ttu-id="aea59-105">Las propiedades del dispositivo UPS indican cuándo se recorta o aumenta la alimentación entrante y la información agregada de las baterías, los generadores, etc., que componen el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-105">The properties of the UPS device indicate when incoming power is trimmed or boosted, and the aggregated information of the batteries, generators, and so on, that make up the device.</span></span> <span data-ttu-id="aea59-106">Los componentes individuales (por ejemplo, varias baterías) también pueden modelarse de forma independiente y asociarse con el SAI.</span><span class="sxs-lookup"><span data-stu-id="aea59-106">The individual components (for example, multiple batteries) can also be independently modeled and associated with the UPS.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aea59-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="aea59-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aea59-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aea59-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aea59-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="aea59-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="aea59-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="aea59-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea59-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aea59-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UninterruptiblePowerSupply : CIM_PowerSupply
{
  uint16   ActiveInputVoltage;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  datetime InstallDate;
  boolean  IsSwitchingSupply;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Range1InputFrequencyHigh;
  uint32   Range1InputFrequencyLow;
  uint32   Range1InputVoltageHigh;
  uint32   Range1InputVoltageLow;
  uint32   Range2InputFrequencyHigh;
  uint32   Range2InputFrequencyLow;
  uint32   Range2InputVoltageHigh;
  uint32   Range2InputVoltageLow;
  uint16   RemainingCapacityStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBackup;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="aea59-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="aea59-112">Members</span></span>

<span data-ttu-id="aea59-113">La clase **CIM \_ UninterruptiblePowerSupply** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aea59-113">The **CIM\_UninterruptiblePowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="aea59-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="aea59-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="aea59-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aea59-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aea59-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="aea59-116">Methods</span></span>

<span data-ttu-id="aea59-117">La clase **CIM \_ UninterruptiblePowerSupply** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="aea59-117">The **CIM\_UninterruptiblePowerSupply** class has these methods.</span></span>



| <span data-ttu-id="aea59-118">Método</span><span class="sxs-lookup"><span data-stu-id="aea59-118">Method</span></span>                                                                                | <span data-ttu-id="aea59-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="aea59-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aea59-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="aea59-120">**Reset**</span></span>](reset-method-in-class-cim-uninterruptiblepowersupply.md)                 | <span data-ttu-id="aea59-121">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aea59-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="aea59-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="aea59-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="aea59-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="aea59-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-uninterruptiblepowersupply.md) | <span data-ttu-id="aea59-124">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="aea59-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="aea59-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="aea59-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="aea59-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aea59-126">Properties</span></span>

<span data-ttu-id="aea59-127">La clase **CIM \_ UninterruptiblePowerSupply** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="aea59-127">The **CIM\_UninterruptiblePowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aea59-128">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="aea59-128">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aea59-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-131">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="aea59-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-132">El intervalo de voltaje de entrada está en uso actualmente.</span><span class="sxs-lookup"><span data-stu-id="aea59-132">Input voltage range is currently in use.</span></span> <span data-ttu-id="aea59-133">Si el suministro no está dibujando la energía actualmente, se puede especificar el valor 6 ("ninguno").</span><span class="sxs-lookup"><span data-stu-id="aea59-133">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="aea59-134">Esta información es necesaria en el caso de un SAI, una subclase de sistema de alimentación [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-134">This information is necessary in the case of a UPS, a subclass of [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="aea59-135">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-135">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aea59-136">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aea59-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aea59-137">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="aea59-137">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="aea59-138">**Intervalo 1** (3)</span><span class="sxs-lookup"><span data-stu-id="aea59-138">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="aea59-139">**Intervalo 2** (4)</span><span class="sxs-lookup"><span data-stu-id="aea59-139">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="aea59-140">**Ambos** (5)</span><span class="sxs-lookup"><span data-stu-id="aea59-140">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="aea59-141">**Ninguno** (6)</span><span class="sxs-lookup"><span data-stu-id="aea59-141">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aea59-142">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="aea59-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aea59-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-145">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="aea59-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-146">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-146">Availability and status of the device.</span></span>

<span data-ttu-id="aea59-147">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aea59-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aea59-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aea59-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="aea59-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="aea59-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="aea59-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-151">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="aea59-151">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="aea59-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="aea59-152"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="aea59-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="aea59-153"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aea59-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="aea59-154"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="aea59-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="aea59-155"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="aea59-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="aea59-156"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="aea59-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="aea59-157"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aea59-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="aea59-158"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="aea59-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="aea59-159"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="aea59-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="aea59-160"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="aea59-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="aea59-161"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-162">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="aea59-162">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="aea59-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="aea59-163"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-164">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="aea59-164">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="aea59-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="aea59-165"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-166">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="aea59-166">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="aea59-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="aea59-167"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="aea59-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="aea59-168"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-169">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="aea59-169">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="aea59-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="aea59-170"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-171">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="aea59-171">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="aea59-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="aea59-172"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-173">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="aea59-173">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="aea59-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="aea59-174"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-175">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="aea59-175">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="aea59-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="aea59-176"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-177">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="aea59-177">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aea59-178">**Caption**</span><span class="sxs-lookup"><span data-stu-id="aea59-178">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-181">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aea59-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-182">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="aea59-182">Short textual description of the object.</span></span>

<span data-ttu-id="aea59-183">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-184">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aea59-184">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-185">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-185">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-187">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aea59-187">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-188">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="aea59-188">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="aea59-189">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-189">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="aea59-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="aea59-190"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="aea59-191"> (0)</span><span class="sxs-lookup"><span data-stu-id="aea59-191">(0)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-192">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aea59-192">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="aea59-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="aea59-193"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="aea59-194">(1)</span><span class="sxs-lookup"><span data-stu-id="aea59-194">(1)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-195">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="aea59-195">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aea59-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-196"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="aea59-197">(2)</span><span class="sxs-lookup"><span data-stu-id="aea59-197">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="aea59-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="aea59-198"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="aea59-199">(3)</span><span class="sxs-lookup"><span data-stu-id="aea59-199">(3)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-200">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="aea59-200">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aea59-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="aea59-201"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="aea59-202">(4)</span><span class="sxs-lookup"><span data-stu-id="aea59-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-203">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aea59-203">Device is not working properly.</span></span> <span data-ttu-id="aea59-204">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="aea59-204">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="aea59-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="aea59-205"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="aea59-206">(5)</span><span class="sxs-lookup"><span data-stu-id="aea59-206">(5)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-207">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="aea59-207">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="aea59-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="aea59-208"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="aea59-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="aea59-209">(6)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-210">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aea59-210">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="aea59-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="aea59-211"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="aea59-212">(7)</span><span class="sxs-lookup"><span data-stu-id="aea59-212">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="aea59-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-213"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="aea59-214">(8)</span><span class="sxs-lookup"><span data-stu-id="aea59-214">(8)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-215">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-215">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="aea59-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="aea59-216"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="aea59-217">(9)</span><span class="sxs-lookup"><span data-stu-id="aea59-217">(9)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-218">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aea59-218">Device is not working properly.</span></span> <span data-ttu-id="aea59-219">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-219">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="aea59-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="aea59-220"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="aea59-221">(10)</span><span class="sxs-lookup"><span data-stu-id="aea59-221">(10)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-222">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="aea59-222">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="aea59-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-223"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="aea59-224">(11)</span><span class="sxs-lookup"><span data-stu-id="aea59-224">(11)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-225">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-225">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="aea59-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="aea59-226"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="aea59-227">(12)</span><span class="sxs-lookup"><span data-stu-id="aea59-227">(12)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-228">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="aea59-228">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="aea59-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-229"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="aea59-230">(13)</span><span class="sxs-lookup"><span data-stu-id="aea59-230">(13)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-231">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-231">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="aea59-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-232"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="aea59-233">(14)</span><span class="sxs-lookup"><span data-stu-id="aea59-233">(14)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-234">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="aea59-234">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="aea59-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="aea59-235"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="aea59-236">(15)</span><span class="sxs-lookup"><span data-stu-id="aea59-236">(15)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-237">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="aea59-237">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="aea59-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-238"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="aea59-239">(16)</span><span class="sxs-lookup"><span data-stu-id="aea59-239">(16)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-240">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-240">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="aea59-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="aea59-241"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="aea59-242">(17)</span><span class="sxs-lookup"><span data-stu-id="aea59-242">(17)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-243">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="aea59-243">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aea59-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-244"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="aea59-245">(18)</span><span class="sxs-lookup"><span data-stu-id="aea59-245">(18)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-246">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aea59-246">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="aea59-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="aea59-247"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="aea59-248">(19)</span><span class="sxs-lookup"><span data-stu-id="aea59-248">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aea59-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="aea59-249"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="aea59-250">(20)</span><span class="sxs-lookup"><span data-stu-id="aea59-250">(20)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-251">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="aea59-251">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="aea59-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-252"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="aea59-253">(21)</span><span class="sxs-lookup"><span data-stu-id="aea59-253">(21)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-254">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="aea59-254">System failure.</span></span> <span data-ttu-id="aea59-255">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="aea59-255">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="aea59-256">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-256">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="aea59-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="aea59-257"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="aea59-258">(22)</span><span class="sxs-lookup"><span data-stu-id="aea59-258">(22)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-259">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="aea59-259">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="aea59-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="aea59-260"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="aea59-261">(23)</span><span class="sxs-lookup"><span data-stu-id="aea59-261">(23)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-262">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="aea59-262">System failure.</span></span> <span data-ttu-id="aea59-263">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="aea59-263">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="aea59-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="aea59-264"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="aea59-265">(24)</span><span class="sxs-lookup"><span data-stu-id="aea59-265">(24)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-266">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="aea59-266">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aea59-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aea59-268">(25)</span><span class="sxs-lookup"><span data-stu-id="aea59-268">(25)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-269">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aea59-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aea59-271">(26)</span><span class="sxs-lookup"><span data-stu-id="aea59-271">(26)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-272">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aea59-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="aea59-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="aea59-273"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="aea59-274">(27)</span><span class="sxs-lookup"><span data-stu-id="aea59-274">(27)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-275">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="aea59-275">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="aea59-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="aea59-276"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="aea59-277">(28)</span><span class="sxs-lookup"><span data-stu-id="aea59-277">(28)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-278">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="aea59-278">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="aea59-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="aea59-279"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="aea59-280">(29)</span><span class="sxs-lookup"><span data-stu-id="aea59-280">(29)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-281">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="aea59-281">Device is disabled.</span></span> <span data-ttu-id="aea59-282">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="aea59-282">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="aea59-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="aea59-283"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="aea59-284">(30)</span><span class="sxs-lookup"><span data-stu-id="aea59-284">(30)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-285">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="aea59-285">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aea59-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="aea59-286"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="aea59-287">31</span><span class="sxs-lookup"><span data-stu-id="aea59-287">(31)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-288">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="aea59-288">Device is not working properly.</span></span> <span data-ttu-id="aea59-289">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="aea59-289">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aea59-290">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="aea59-290">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-291">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aea59-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-293">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aea59-293">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-294">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="aea59-294">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="aea59-295">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-296">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aea59-296">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-299">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aea59-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aea59-300">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="aea59-300">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="aea59-301">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="aea59-301">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="aea59-302">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-303">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="aea59-303">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-306">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="aea59-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-307">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="aea59-307">Textual description of the object.</span></span>

<span data-ttu-id="aea59-308">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-308">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-309">**ID**</span><span class="sxs-lookup"><span data-stu-id="aea59-309">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-312">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aea59-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aea59-313">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aea59-313">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="aea59-314">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-315">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="aea59-315">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-316">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aea59-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aea59-318">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="aea59-318">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="aea59-319">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-320">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="aea59-320">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aea59-323">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="aea59-323">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="aea59-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-325">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="aea59-325">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-326">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aea59-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-328">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|001,4 de la batería de alimentación DMTF \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" porcentaje ")</span><span class="sxs-lookup"><span data-stu-id="aea59-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-329">Estimación porcentual del importe total restante para un UPS que usa la tecnología de batería.</span><span class="sxs-lookup"><span data-stu-id="aea59-329">Percentage estimate of the remaining full charge for a UPS that uses battery technology.</span></span>

</dd> <dt>

<span data-ttu-id="aea59-330">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="aea59-330">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-331">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-333">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Baterú de la batería \| 001,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="aea59-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-334">Tiempo estimado, en minutos, hasta que la batería, el generador u otra fuente de alimentación se agota bajo las condiciones de carga presentes si la utilidad de energía está apagada o se pierde y permanece desactivada.</span><span class="sxs-lookup"><span data-stu-id="aea59-334">Estimated time, in minutes, until the battery, generator, or other power source is depleted under the present load conditions if the utility power is off, or is lost and remains off.</span></span>

</dd> <dt>

<span data-ttu-id="aea59-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aea59-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-336">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aea59-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-338">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="aea59-338">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-339">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="aea59-339">Date and time the object was installed.</span></span> <span data-ttu-id="aea59-340">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="aea59-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aea59-341">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-342">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="aea59-342">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-343">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aea59-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aea59-345">Si es **true**, la fuente de alimentación es una fuente de conmutación (en lugar de lineal).</span><span class="sxs-lookup"><span data-stu-id="aea59-345">If **TRUE**, the power supply is a switching (rather than linear) supply.</span></span>

<span data-ttu-id="aea59-346">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-346">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-347">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="aea59-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-348">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aea59-350">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aea59-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="aea59-351">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-352">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="aea59-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-353">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-355">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="aea59-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-356">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="aea59-356">Label by which the object is known.</span></span> <span data-ttu-id="aea59-357">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="aea59-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="aea59-358">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-359">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="aea59-359">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-362">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aea59-362">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-363">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aea59-363">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="aea59-364">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="aea59-365">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="aea59-365">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="aea59-366">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="aea59-366">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-367">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aea59-367">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aea59-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aea59-369">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aea59-369">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="aea59-370">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="aea59-370">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aea59-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="aea59-371"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="aea59-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="aea59-372"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aea59-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="aea59-373"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aea59-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="aea59-374"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-375">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="aea59-375">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="aea59-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="aea59-376"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-377">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="aea59-377">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="aea59-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="aea59-378"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-379">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="aea59-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="aea59-380">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="aea59-380">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="aea59-381">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="aea59-381">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="aea59-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="aea59-382"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-383">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="aea59-383">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="aea59-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="aea59-384"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-385">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="aea59-385">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aea59-386">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="aea59-386">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-387">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="aea59-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aea59-389">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="aea59-389">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="aea59-390">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="aea59-390">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="aea59-391">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="aea59-391">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="aea59-392">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="aea59-392">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="aea59-393">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-394">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="aea59-394">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-395">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-395">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-397">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios")</span><span class="sxs-lookup"><span data-stu-id="aea59-397">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-398">Frecuencia, en hercios, en el extremo superior del intervalo de frecuencia de entrada de la fuente de alimentación 1.</span><span class="sxs-lookup"><span data-stu-id="aea59-398">Frequency, in hertz, at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="aea59-399">Un valor de 0 (cero) implica DC.</span><span class="sxs-lookup"><span data-stu-id="aea59-399">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="aea59-400">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-400">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-401">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="aea59-401">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-402">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-404">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="aea59-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-405">Frecuencia, en hercios, en el extremo inferior del intervalo de frecuencia de entrada de la fuente de alimentación 1.</span><span class="sxs-lookup"><span data-stu-id="aea59-405">Frequency, in hertz, at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="aea59-406">Un valor de 0 (cero) implica DC.</span><span class="sxs-lookup"><span data-stu-id="aea59-406">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="aea59-407">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-407">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-408">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="aea59-408">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-409">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-411">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivoltios")</span><span class="sxs-lookup"><span data-stu-id="aea59-411">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-412">Si el voltaje, en milivoltios, supera el valor especificado por la propiedad **Range1InputVoltageHigh** , el SAI se compensará recortando la tensión.</span><span class="sxs-lookup"><span data-stu-id="aea59-412">If the voltage, in millivolts, rises above the value specified by the **Range1InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="aea59-413">Un valor de 0 (cero) indica que se desconoce el voltaje en el que se produce el recorte.</span><span class="sxs-lookup"><span data-stu-id="aea59-413">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="aea59-414">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-414">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-415">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="aea59-415">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-416">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-418">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivoltios")</span><span class="sxs-lookup"><span data-stu-id="aea59-418">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range1InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-419">Si el voltaje, en milivoltios, cae por debajo del valor especificado por la propiedad **Range1InputVoltageLow** , el UPS se compensará aumentando el voltaje usando sus fuentes de alimentación.</span><span class="sxs-lookup"><span data-stu-id="aea59-419">If the voltage, in millivolts, drops below the value specified by the **Range1InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="aea59-420">Un valor de 0 indica que se desconoce el voltaje en el que se produce el aumento.</span><span class="sxs-lookup"><span data-stu-id="aea59-420">A value of 0 indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="aea59-421">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-421">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-422">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="aea59-422">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-423">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-423">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-424">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-425">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,20 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="aea59-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-426">Frecuencia, en hercios, en el extremo superior del intervalo de frecuencia de entrada de la fuente de alimentación 2.</span><span class="sxs-lookup"><span data-stu-id="aea59-426">Frequency, in hertz, at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="aea59-427">Un valor de 0 (cero) implica DC.</span><span class="sxs-lookup"><span data-stu-id="aea59-427">A value of 0 (zero) implies DC.</span></span>

<span data-ttu-id="aea59-428">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-428">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-429">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="aea59-429">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-430">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-431">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-432">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,19 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="aea59-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-433">Frecuencia, en hercios, en el extremo inferior del intervalo de frecuencia de entrada de la fuente de alimentación 2.</span><span class="sxs-lookup"><span data-stu-id="aea59-433">Frequency, in hertz, at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="aea59-434">Un valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="aea59-434">A value of 0 implies DC.</span></span>

<span data-ttu-id="aea59-435">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-435">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-436">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="aea59-436">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-437">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-437">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-438">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-439">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivoltios")</span><span class="sxs-lookup"><span data-stu-id="aea59-439">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageHigh"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-440">Si el voltaje, en milivoltios, supera el valor especificado por la propiedad **Range2InputVoltageHigh** , el SAI se compensará recortando la tensión.</span><span class="sxs-lookup"><span data-stu-id="aea59-440">If the voltage, in millivolts, rises above the value specified by the **Range2InputVoltageHigh** property, the UPS will compensate by trimming the voltage.</span></span> <span data-ttu-id="aea59-441">Un valor de 0 (cero) indica que se desconoce el voltaje en el que se produce el recorte.</span><span class="sxs-lookup"><span data-stu-id="aea59-441">A value of 0 (zero) indicates that the voltage at which trimming occurs is unknown.</span></span>

<span data-ttu-id="aea59-442">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-442">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-443">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="aea59-443">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-444">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-444">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-446">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milivoltios")</span><span class="sxs-lookup"><span data-stu-id="aea59-446">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Range2InputVoltageLow"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-447">Si el voltaje, en milivoltios, cae por debajo del valor especificado por la propiedad **Range2InputVoltageLow** , el UPS se compensará aumentando el voltaje usando sus fuentes de alimentación.</span><span class="sxs-lookup"><span data-stu-id="aea59-447">If the voltage, in millivolts, drops below the value specified by the **Range2InputVoltageLow** property, the UPS will compensate by boosting the voltage using its power sources.</span></span> <span data-ttu-id="aea59-448">Un valor de 0 (cero) indica que se desconoce el voltaje en el que se produce el aumento.</span><span class="sxs-lookup"><span data-stu-id="aea59-448">A value of 0 (zero) indicates that the voltage at which boosting occurs is unknown.</span></span>

<span data-ttu-id="aea59-449">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-449">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-450">**RemainingCapacityStatus**</span><span class="sxs-lookup"><span data-stu-id="aea59-450">**RemainingCapacityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-451">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aea59-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-453">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería 001,1 de DMTF (SAI \| )</span><span class="sxs-lookup"><span data-stu-id="aea59-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-454">Indicación de la capacidad restante en las baterías, el generador u otro origen del SAI.</span><span class="sxs-lookup"><span data-stu-id="aea59-454">Indication of the capacity remaining in the UPS's batteries, generator, or other source.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aea59-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (1)</span><span class="sxs-lookup"><span data-stu-id="aea59-455"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="aea59-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span><span class="sxs-lookup"><span data-stu-id="aea59-456"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-457">Los minutos estimados restantes de tiempo de ejecución son mayores que el estado de baja energía definido por el SAI (normalmente, dos minutos).</span><span class="sxs-lookup"><span data-stu-id="aea59-457">Remaining estimated minutes of run-time is greater than the UPS's defined low-power state (typically, two minutes).</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="aea59-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bajo** (3)</span><span class="sxs-lookup"><span data-stu-id="aea59-458"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-459">Los minutos estimados restantes de tiempo de ejecución son menores o iguales que el estado de baja energía definido por el SAI.</span><span class="sxs-lookup"><span data-stu-id="aea59-459">Remaining estimated minutes of run-time is less than or equal to the UPS's defined low-power state.</span></span>

</dd> <dt>

<span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>

<span data-ttu-id="aea59-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Agotado** (4)</span><span class="sxs-lookup"><span data-stu-id="aea59-460"><span id="Depleted"></span><span id="depleted"></span><span id="DEPLETED"></span>**Depleted** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aea59-461">El SAI (UPS) no podrá mantener la carga actual cuando se pierda la alimentación de la utilidad (incluida la posibilidad de que la utilidad de energía esté actualmente ausente).</span><span class="sxs-lookup"><span data-stu-id="aea59-461">The UPS will be unable to sustain the present load when the utility power is lost (including the possibility that the utility power is currently absent).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aea59-462">**Estado**</span><span class="sxs-lookup"><span data-stu-id="aea59-462">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-463">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-464">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-465">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="aea59-465">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-466">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="aea59-466">Current status of the object.</span></span> <span data-ttu-id="aea59-467">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-467">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aea59-468">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="aea59-468">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aea59-469">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="aea59-469">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aea59-470">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="aea59-470">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aea59-471">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="aea59-471">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aea59-472">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="aea59-472">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aea59-473">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="aea59-473">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aea59-474">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="aea59-474">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aea59-475">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="aea59-475">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aea59-476">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="aea59-476">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aea59-477">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="aea59-477">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aea59-478">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="aea59-478">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aea59-479">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="aea59-479">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aea59-480">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="aea59-480">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aea59-481">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="aea59-481">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-482">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aea59-482">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-483">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-484">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="aea59-484">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-485">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="aea59-485">State of the logical device.</span></span> <span data-ttu-id="aea59-486">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="aea59-486">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="aea59-487">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-487">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aea59-488">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aea59-488">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aea59-489">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="aea59-489">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aea59-490">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="aea59-490">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aea59-491">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="aea59-491">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aea59-492">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="aea59-492">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aea59-493">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aea59-493">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-494">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-496">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aea59-496">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aea59-497">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="aea59-497">Scoping system's creation class name.</span></span>

<span data-ttu-id="aea59-498">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-498">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-499">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="aea59-499">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-500">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="aea59-500">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-501">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-502">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aea59-502">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aea59-503">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="aea59-503">Scoping system's name.</span></span>

<span data-ttu-id="aea59-504">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-504">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-505">**TimeOnBackup**</span><span class="sxs-lookup"><span data-stu-id="aea59-505">**TimeOnBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-506">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-508">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|001,2 de la batería de alimentación DMTF \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="aea59-508">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|UPS Battery\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-509">Tiempo transcurrido, en segundos, desde que el SAI se cambió por última vez a la energía de la batería, el generador u otra fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="aea59-509">Elapsed time, in seconds, since the UPS last switched to battery power, generator, or other power source.</span></span> <span data-ttu-id="aea59-510">O bien, la hora desde la última vez que se reinició el SAI, lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="aea59-510">Or, the time since the UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="aea59-511">Si el SAI está en línea, se devolverá 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="aea59-511">If the UPS is online, 0 (zero) will be returned.</span></span>

</dd> <dt>

<span data-ttu-id="aea59-512">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="aea59-512">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-513">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aea59-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-514">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-515">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,21 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivatios ")</span><span class="sxs-lookup"><span data-stu-id="aea59-515">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-516">Potencia de salida total de la fuente de alimentación, en milivatios.</span><span class="sxs-lookup"><span data-stu-id="aea59-516">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="aea59-517">Un valor de 0 (cero) denota Unknown.</span><span class="sxs-lookup"><span data-stu-id="aea59-517">A value of 0 (zero) denotes unknown.</span></span>

<span data-ttu-id="aea59-518">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-518">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

</dd> <dt>

<span data-ttu-id="aea59-519">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="aea59-519">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aea59-520">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aea59-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aea59-521">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="aea59-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aea59-522">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="aea59-522">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="aea59-523">Tipo de cambio de intervalo de voltaje de entrada implementado en la fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="aea59-523">Type of input-voltage range switching implemented in the power supply.</span></span>

<span data-ttu-id="aea59-524">Esta propiedad se hereda del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-524">This property is inherited from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aea59-525">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="aea59-525">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aea59-526">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="aea59-526">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="aea59-527">**Manual** (3)</span><span class="sxs-lookup"><span data-stu-id="aea59-527">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="aea59-528">**AutoSwitch** (4)</span><span class="sxs-lookup"><span data-stu-id="aea59-528">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="aea59-529">**Rango amplio** (5)</span><span class="sxs-lookup"><span data-stu-id="aea59-529">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aea59-530">**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="aea59-530">**Not Applicable** (6)</span></span>


<span data-ttu-id="aea59-531"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="aea59-531"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="aea59-532">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aea59-532">Remarks</span></span>

<span data-ttu-id="aea59-533">La **clase \_ UninterruptiblePowerSupply de CIM** se deriva del sistema de sistema [**CIM \_**](cim-powersupply.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-533">The **CIM\_UninterruptiblePowerSupply** class is derived from [**CIM\_PowerSupply**](cim-powersupply.md).</span></span>

<span data-ttu-id="aea59-534">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="aea59-534">WMI does not implement this class.</span></span> <span data-ttu-id="aea59-535">Para las clases WMI derivadas de **CIM \_ UninterruptiblePowerSupply**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="aea59-535">For WMI classes derived from **CIM\_UninterruptiblePowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="aea59-536">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="aea59-536">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aea59-537">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="aea59-537">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea59-538">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aea59-538">Requirements</span></span>



| <span data-ttu-id="aea59-539">Requisito</span><span class="sxs-lookup"><span data-stu-id="aea59-539">Requirement</span></span> | <span data-ttu-id="aea59-540">Value</span><span class="sxs-lookup"><span data-stu-id="aea59-540">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aea59-541">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aea59-541">Minimum supported client</span></span><br/> | <span data-ttu-id="aea59-542">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aea59-542">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aea59-543">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aea59-543">Minimum supported server</span></span><br/> | <span data-ttu-id="aea59-544">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aea59-544">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aea59-545">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aea59-545">Namespace</span></span><br/>                | <span data-ttu-id="aea59-546">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aea59-546">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aea59-547">MOF</span><span class="sxs-lookup"><span data-stu-id="aea59-547">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aea59-548"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aea59-548"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aea59-549">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aea59-549">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aea59-550"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aea59-550"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea59-551">Vea también</span><span class="sxs-lookup"><span data-stu-id="aea59-551">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea59-552">**Sistema \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="aea59-552">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> </dl>

 

