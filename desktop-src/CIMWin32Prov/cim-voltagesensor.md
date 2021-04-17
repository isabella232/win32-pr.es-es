---
description: La \_ clase VoltageSensor de CIM existe para la compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores. Con las adiciones al \_ sensor CIM y \_ las clases de CIM NumericSensor en la versión 2,2, ya no es necesario.
ms.assetid: a578c7a2-27d5-4bd8-86d7-3962d5091f14
ms.tgt_platform: multiple
title: CIM_VoltageSensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VoltageSensor
- CIM_VoltageSensor.Accuracy
- CIM_VoltageSensor.Availability
- CIM_VoltageSensor.Caption
- CIM_VoltageSensor.ConfigManagerErrorCode
- CIM_VoltageSensor.ConfigManagerUserConfig
- CIM_VoltageSensor.CreationClassName
- CIM_VoltageSensor.CurrentReading
- CIM_VoltageSensor.Description
- CIM_VoltageSensor.DeviceID
- CIM_VoltageSensor.ErrorCleared
- CIM_VoltageSensor.ErrorDescription
- CIM_VoltageSensor.InstallDate
- CIM_VoltageSensor.IsLinear
- CIM_VoltageSensor.LastErrorCode
- CIM_VoltageSensor.LowerThresholdCritical
- CIM_VoltageSensor.LowerThresholdFatal
- CIM_VoltageSensor.LowerThresholdNonCritical
- CIM_VoltageSensor.MaxReadable
- CIM_VoltageSensor.MinReadable
- CIM_VoltageSensor.Name
- CIM_VoltageSensor.NominalReading
- CIM_VoltageSensor.NormalMax
- CIM_VoltageSensor.NormalMin
- CIM_VoltageSensor.PNPDeviceID
- CIM_VoltageSensor.PowerManagementCapabilities
- CIM_VoltageSensor.PowerManagementSupported
- CIM_VoltageSensor.Resolution
- CIM_VoltageSensor.Status
- CIM_VoltageSensor.StatusInfo
- CIM_VoltageSensor.SystemCreationClassName
- CIM_VoltageSensor.SystemName
- CIM_VoltageSensor.Tolerance
- CIM_VoltageSensor.UpperThresholdCritical
- CIM_VoltageSensor.UpperThresholdFatal
- CIM_VoltageSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bd0f3d79415254d0af50429c8f1776d2eb451cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659410"
---
# <a name="cim_voltagesensor-class"></a><span data-ttu-id="491f0-104">\_Clase VoltageSensor de CIM</span><span class="sxs-lookup"><span data-stu-id="491f0-104">CIM\_VoltageSensor class</span></span>

<span data-ttu-id="491f0-105">La **clase \_ VoltageSensor de CIM** existe para la compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores.</span><span class="sxs-lookup"><span data-stu-id="491f0-105">The **CIM\_VoltageSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="491f0-106">Con las adiciones al [**\_ sensor CIM**](cim-sensor.md) y las clases de [**CIM \_ NumericSensor**](cim-numericsensor.md) en la versión 2,2, ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="491f0-106">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span> <span data-ttu-id="491f0-107">Un sensor de voltaje se puede definir estableciendo la propiedad **SensorType** , heredado [**del \_ sensor CIM**](cim-sensor.md), en 3 ("voltaje").</span><span class="sxs-lookup"><span data-stu-id="491f0-107">A voltage sensor can be defined by setting the **SensorType** property, inherited from [**CIM\_Sensor**](cim-sensor.md), to 3 ("Voltage").</span></span> <span data-ttu-id="491f0-108">Otras propiedades de esta clase están codificadas de forma rígida en valores constantes que se corresponden con las definiciones de la jerarquía del sensor.</span><span class="sxs-lookup"><span data-stu-id="491f0-108">Other properties of this class are hard-coded to constant values that correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="491f0-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="491f0-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="491f0-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="491f0-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="491f0-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="491f0-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="491f0-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="491f0-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="491f0-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="491f0-113">Syntax</span></span>

``` syntax
[UUID("{A998F9B4-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VoltageSensor : CIM_NumericSensor
{
  sint32   Accuracy;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  sint32   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLinear;
  uint32   LastErrorCode;
  sint32   LowerThresholdCritical;
  sint32   LowerThresholdFatal;
  sint32   LowerThresholdNonCritical;
  sint32   MaxReadable;
  sint32   MinReadable;
  string   Name;
  sint32   NominalReading;
  sint32   NormalMax;
  sint32   NormalMin;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   Resolution;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  sint32   Tolerance;
  sint32   UpperThresholdCritical;
  sint32   UpperThresholdFatal;
  sint32   UpperThresholdNonCritical;
};
```

## <a name="members"></a><span data-ttu-id="491f0-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="491f0-114">Members</span></span>

<span data-ttu-id="491f0-115">La clase **CIM \_ VoltageSensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="491f0-115">The **CIM\_VoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="491f0-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="491f0-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="491f0-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="491f0-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="491f0-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="491f0-118">Methods</span></span>

<span data-ttu-id="491f0-119">La clase **CIM \_ VoltageSensor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="491f0-119">The **CIM\_VoltageSensor** class has these methods.</span></span>



| <span data-ttu-id="491f0-120">Método</span><span class="sxs-lookup"><span data-stu-id="491f0-120">Method</span></span>                                                                   | <span data-ttu-id="491f0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="491f0-121">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="491f0-122">**Reset**</span><span class="sxs-lookup"><span data-stu-id="491f0-122">**Reset**</span></span>](reset-method-in-class-cim-voltagesensor.md)                 | <span data-ttu-id="491f0-123">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="491f0-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="491f0-124">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="491f0-124">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="491f0-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="491f0-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-voltagesensor.md) | <span data-ttu-id="491f0-126">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="491f0-126">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="491f0-127">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="491f0-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="491f0-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="491f0-128">Properties</span></span>

<span data-ttu-id="491f0-129">La clase **CIM \_ VoltageSensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="491f0-129">The **CIM\_VoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="491f0-130">**Precisión**</span><span class="sxs-lookup"><span data-stu-id="491f0-130">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-133">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Sonda de voltaje de DMTF \| \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="491f0-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-134">Precisión del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="491f0-134">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="491f0-135">Su valor se registra como más o menos centésimas de un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="491f0-135">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="491f0-136">Esta propiedad, y las propiedades de **resolución** y **tolerancia** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="491f0-136">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="491f0-137">La precisión puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="491f0-137">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="491f0-138">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-138">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-139">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="491f0-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="491f0-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-142">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="491f0-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-143">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-143">Availability and status of the device.</span></span>

<span data-ttu-id="491f0-144">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="491f0-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="491f0-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="491f0-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="491f0-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="491f0-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="491f0-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-148">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="491f0-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="491f0-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="491f0-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="491f0-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="491f0-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="491f0-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="491f0-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="491f0-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="491f0-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="491f0-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="491f0-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="491f0-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="491f0-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="491f0-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="491f0-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="491f0-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="491f0-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="491f0-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="491f0-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="491f0-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="491f0-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-159">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="491f0-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="491f0-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="491f0-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-161">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="491f0-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="491f0-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="491f0-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-163">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="491f0-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="491f0-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="491f0-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="491f0-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="491f0-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-166">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="491f0-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="491f0-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="491f0-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-168">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="491f0-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="491f0-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="491f0-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-170">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="491f0-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="491f0-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="491f0-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-172">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="491f0-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="491f0-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="491f0-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-174">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="491f0-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="491f0-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="491f0-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-178">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="491f0-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-179">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="491f0-179">Short textual description of the object.</span></span>

<span data-ttu-id="491f0-180">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="491f0-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-182">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="491f0-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-184">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="491f0-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-185">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="491f0-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="491f0-186">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="491f0-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="491f0-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="491f0-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="491f0-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-189">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="491f0-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="491f0-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="491f0-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="491f0-191">(1)</span><span class="sxs-lookup"><span data-stu-id="491f0-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-192">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="491f0-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="491f0-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="491f0-194">(2)</span><span class="sxs-lookup"><span data-stu-id="491f0-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="491f0-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="491f0-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="491f0-196">(3)</span><span class="sxs-lookup"><span data-stu-id="491f0-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-197">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="491f0-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="491f0-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="491f0-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="491f0-199">(4)</span><span class="sxs-lookup"><span data-stu-id="491f0-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-200">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="491f0-200">Device is not working properly.</span></span> <span data-ttu-id="491f0-201">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="491f0-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="491f0-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="491f0-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="491f0-203">(5)</span><span class="sxs-lookup"><span data-stu-id="491f0-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-204">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="491f0-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="491f0-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="491f0-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="491f0-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="491f0-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-207">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="491f0-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="491f0-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="491f0-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="491f0-209">(7)</span><span class="sxs-lookup"><span data-stu-id="491f0-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="491f0-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="491f0-211">(8)</span><span class="sxs-lookup"><span data-stu-id="491f0-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-212">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="491f0-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="491f0-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="491f0-214">(9)</span><span class="sxs-lookup"><span data-stu-id="491f0-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-215">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="491f0-215">Device is not working properly.</span></span> <span data-ttu-id="491f0-216">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="491f0-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="491f0-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="491f0-218">(10)</span><span class="sxs-lookup"><span data-stu-id="491f0-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-219">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="491f0-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="491f0-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="491f0-221">(11)</span><span class="sxs-lookup"><span data-stu-id="491f0-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-222">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="491f0-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="491f0-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="491f0-224">(12)</span><span class="sxs-lookup"><span data-stu-id="491f0-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-225">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="491f0-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="491f0-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="491f0-227">(13)</span><span class="sxs-lookup"><span data-stu-id="491f0-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-228">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="491f0-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="491f0-230">(14)</span><span class="sxs-lookup"><span data-stu-id="491f0-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-231">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="491f0-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="491f0-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="491f0-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="491f0-233">(15)</span><span class="sxs-lookup"><span data-stu-id="491f0-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-234">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="491f0-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="491f0-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="491f0-236">(16)</span><span class="sxs-lookup"><span data-stu-id="491f0-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-237">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="491f0-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="491f0-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="491f0-239">(17)</span><span class="sxs-lookup"><span data-stu-id="491f0-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-240">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="491f0-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="491f0-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="491f0-242">(18)</span><span class="sxs-lookup"><span data-stu-id="491f0-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-243">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="491f0-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="491f0-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="491f0-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="491f0-245">(19)</span><span class="sxs-lookup"><span data-stu-id="491f0-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="491f0-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="491f0-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="491f0-247">(20)</span><span class="sxs-lookup"><span data-stu-id="491f0-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-248">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="491f0-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="491f0-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="491f0-250">(21)</span><span class="sxs-lookup"><span data-stu-id="491f0-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-251">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="491f0-251">System failure.</span></span> <span data-ttu-id="491f0-252">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="491f0-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="491f0-253">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="491f0-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="491f0-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="491f0-255">(22)</span><span class="sxs-lookup"><span data-stu-id="491f0-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-256">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="491f0-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="491f0-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="491f0-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="491f0-258">(23)</span><span class="sxs-lookup"><span data-stu-id="491f0-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-259">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="491f0-259">System failure.</span></span> <span data-ttu-id="491f0-260">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="491f0-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="491f0-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="491f0-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="491f0-262">(24)</span><span class="sxs-lookup"><span data-stu-id="491f0-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-263">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="491f0-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="491f0-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="491f0-265">(25)</span><span class="sxs-lookup"><span data-stu-id="491f0-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-266">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="491f0-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="491f0-268">(26)</span><span class="sxs-lookup"><span data-stu-id="491f0-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-269">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="491f0-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="491f0-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="491f0-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="491f0-271">(27)</span><span class="sxs-lookup"><span data-stu-id="491f0-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-272">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="491f0-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="491f0-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="491f0-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="491f0-274">(28)</span><span class="sxs-lookup"><span data-stu-id="491f0-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-275">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="491f0-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="491f0-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="491f0-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="491f0-277">(29)</span><span class="sxs-lookup"><span data-stu-id="491f0-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-278">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="491f0-278">Device is disabled.</span></span> <span data-ttu-id="491f0-279">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="491f0-279">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="491f0-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="491f0-280"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="491f0-281">(30)</span><span class="sxs-lookup"><span data-stu-id="491f0-281">(30)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-282">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="491f0-282">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="491f0-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="491f0-283"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="491f0-284">31</span><span class="sxs-lookup"><span data-stu-id="491f0-284">(31)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-285">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="491f0-285">Device is not working properly.</span></span> <span data-ttu-id="491f0-286">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="491f0-286">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="491f0-287">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="491f0-287">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-288">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="491f0-288">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-290">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="491f0-290">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-291">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="491f0-291">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="491f0-292">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-293">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="491f0-293">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-296">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="491f0-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="491f0-297">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="491f0-297">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="491f0-298">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="491f0-298">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="491f0-299">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-300">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="491f0-300">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-301">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-301">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-303">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-303">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-304">Valor actual indicado por el sensor.</span><span class="sxs-lookup"><span data-stu-id="491f0-304">Current value indicated by the sensor.</span></span>

<span data-ttu-id="491f0-305">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-306">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="491f0-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-309">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="491f0-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-310">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="491f0-310">Textual description of the object.</span></span>

<span data-ttu-id="491f0-311">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-312">**ID**</span><span class="sxs-lookup"><span data-stu-id="491f0-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-315">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="491f0-315">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="491f0-316">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="491f0-316">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="491f0-317">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="491f0-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-319">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="491f0-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491f0-321">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="491f0-321">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="491f0-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="491f0-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491f0-326">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="491f0-326">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="491f0-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="491f0-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-329">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="491f0-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-331">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="491f0-331">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-332">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="491f0-332">Date and time the object was installed.</span></span> <span data-ttu-id="491f0-333">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="491f0-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="491f0-334">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-335">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="491f0-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-336">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="491f0-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491f0-338">Si es **true**, el sensor es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="491f0-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="491f0-339">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="491f0-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-341">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="491f0-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491f0-343">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="491f0-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="491f0-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="491f0-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-346">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-348">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,13 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-348">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-349">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="491f0-349">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="491f0-350">Si la propiedad **CurrentReading** está entre **LowerThresholdCritical** y **LowerThresholdFatal**, el estado actual es Critical.</span><span class="sxs-lookup"><span data-stu-id="491f0-350">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="491f0-351">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="491f0-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-353">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-355">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-355">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-356">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="491f0-356">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, non-critical, critical, or fatal conditions.</span></span> <span data-ttu-id="491f0-357">Si la propiedad **CurrentReading** está por debajo de **LowerThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="491f0-357">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="491f0-358">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="491f0-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-360">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-362">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-362">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-363">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="491f0-363">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="491f0-364">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="491f0-364">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="491f0-365">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **LowerThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="491f0-365">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="491f0-366">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="491f0-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-368">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-370">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-371">Valor mayor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="491f0-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="491f0-372">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="491f0-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-374">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-376">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-376">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-377">Valor menor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="491f0-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="491f0-378">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-379">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="491f0-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-380">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-382">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="491f0-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-383">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="491f0-383">Label by which the object is known.</span></span> <span data-ttu-id="491f0-384">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="491f0-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="491f0-385">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="491f0-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-387">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-389">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-390">Valor esperado o normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="491f0-390">Expected or normal value for the numeric sensor.</span></span>

<span data-ttu-id="491f0-391">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="491f0-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-393">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-395">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-395">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-396">Intervalo máximo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="491f0-396">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="491f0-397">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="491f0-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-399">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-401">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-401">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-402">Intervalo mínimo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="491f0-402">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="491f0-403">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="491f0-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-405">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-407">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="491f0-407">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-408">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="491f0-408">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="491f0-409">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="491f0-410">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="491f0-410">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="491f0-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="491f0-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-412">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="491f0-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="491f0-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491f0-414">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="491f0-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="491f0-415">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="491f0-415">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="491f0-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="491f0-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="491f0-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="491f0-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="491f0-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="491f0-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="491f0-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="491f0-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-420">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="491f0-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="491f0-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="491f0-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-422">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="491f0-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="491f0-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="491f0-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-424">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="491f0-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="491f0-425">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="491f0-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="491f0-426">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="491f0-426">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="491f0-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="491f0-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-428">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="491f0-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="491f0-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="491f0-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="491f0-430">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="491f0-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="491f0-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="491f0-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-432">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="491f0-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-433">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="491f0-434">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="491f0-434">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="491f0-435">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="491f0-435">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="491f0-436">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="491f0-436">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="491f0-437">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="491f0-437">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="491f0-438">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-439">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="491f0-439">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-440">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="491f0-440">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-442">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-443">Capacidad del sensor para resolver las diferencias en la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="491f0-443">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="491f0-444">Esta propiedad, y las propiedades de **precisión** y **tolerancia** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="491f0-444">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="491f0-445">Este valor puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="491f0-445">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="491f0-446">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-446">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-447">**Estado**</span><span class="sxs-lookup"><span data-stu-id="491f0-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-448">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-450">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="491f0-450">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-451">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="491f0-451">Current status of the object.</span></span>

<span data-ttu-id="491f0-452">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="491f0-453">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="491f0-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="491f0-454">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="491f0-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="491f0-455">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="491f0-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="491f0-456">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="491f0-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="491f0-457">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="491f0-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="491f0-458">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="491f0-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="491f0-459">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="491f0-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="491f0-460">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="491f0-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="491f0-461">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="491f0-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="491f0-462">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="491f0-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="491f0-463">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="491f0-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="491f0-464">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="491f0-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="491f0-465">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="491f0-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="491f0-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="491f0-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-467">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="491f0-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-469">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="491f0-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-470">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="491f0-470">State of the logical device.</span></span> <span data-ttu-id="491f0-471">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="491f0-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="491f0-472">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="491f0-473">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="491f0-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="491f0-474">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="491f0-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="491f0-475">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="491f0-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="491f0-476">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="491f0-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="491f0-477">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="491f0-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="491f0-478">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="491f0-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-479">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-480">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-481">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="491f0-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="491f0-482">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="491f0-482">Scoping system's creation class name.</span></span>

<span data-ttu-id="491f0-483">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="491f0-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-485">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="491f0-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-486">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-487">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="491f0-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="491f0-488">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="491f0-488">Scoping system's name.</span></span>

<span data-ttu-id="491f0-489">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-490">**Tolerancia**</span><span class="sxs-lookup"><span data-stu-id="491f0-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-491">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-492">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-493">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,18 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-494">Tolerancia del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="491f0-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="491f0-495">Esta propiedad, y las propiedades de **resolución** y **precisión** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="491f0-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="491f0-496">La tolerancia puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="491f0-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="491f0-497">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-497">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-498">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="491f0-498">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-499">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-499">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-500">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-501">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-501">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-502">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="491f0-502">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="491f0-503">Si la propiedad **CurrentReading** está entre **UpperThresholdCritical** y **UpperThresholdFatal**, el estado actual es Critical.</span><span class="sxs-lookup"><span data-stu-id="491f0-503">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="491f0-504">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-504">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-505">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="491f0-505">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-506">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-506">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-508">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-508">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-509">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="491f0-509">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="491f0-510">Si la propiedad **CurrentReading** está por encima de **UpperThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="491f0-510">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="491f0-511">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-511">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="491f0-512">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="491f0-512">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="491f0-513">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="491f0-513">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="491f0-514">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="491f0-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="491f0-515">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sonda de voltaje \| de DMTF 001,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="491f0-515">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="491f0-516">Valor de umbral que especifica los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="491f0-516">Threshold value that specifies the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="491f0-517">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="491f0-517">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="491f0-518">Si la propiedad **CurrentReading** está entre **UpperThresholdNonCritical** y **UpperThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="491f0-518">If the **CurrentReading** property is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is noncritical.</span></span>

<span data-ttu-id="491f0-519">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-519">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="491f0-520">Observaciones</span><span class="sxs-lookup"><span data-stu-id="491f0-520">Remarks</span></span>

<span data-ttu-id="491f0-521">La clase **CIM \_ VoltageSensor** se deriva de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-521">The **CIM\_VoltageSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="491f0-522">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="491f0-522">WMI does not implement this class.</span></span> <span data-ttu-id="491f0-523">Para las clases WMI derivadas de **CIM \_ VoltageSensor**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="491f0-523">For WMI classes derived from **CIM\_VoltageSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="491f0-524">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="491f0-524">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="491f0-525">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="491f0-525">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="491f0-526">Requisitos</span><span class="sxs-lookup"><span data-stu-id="491f0-526">Requirements</span></span>



| <span data-ttu-id="491f0-527">Requisito</span><span class="sxs-lookup"><span data-stu-id="491f0-527">Requirement</span></span> | <span data-ttu-id="491f0-528">Value</span><span class="sxs-lookup"><span data-stu-id="491f0-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="491f0-529">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="491f0-529">Minimum supported client</span></span><br/> | <span data-ttu-id="491f0-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="491f0-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="491f0-531">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="491f0-531">Minimum supported server</span></span><br/> | <span data-ttu-id="491f0-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="491f0-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="491f0-533">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="491f0-533">Namespace</span></span><br/>                | <span data-ttu-id="491f0-534">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="491f0-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="491f0-535">MOF</span><span class="sxs-lookup"><span data-stu-id="491f0-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="491f0-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="491f0-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="491f0-537">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="491f0-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="491f0-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="491f0-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="491f0-539">Vea también</span><span class="sxs-lookup"><span data-stu-id="491f0-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="491f0-540">**NumericSensor de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="491f0-540">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

