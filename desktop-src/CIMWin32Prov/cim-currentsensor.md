---
description: La \_ clase CurrentSensor de CIM existe para la compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores.
ms.assetid: d1835b09-4286-4586-92ec-f5f77791aea6
ms.tgt_platform: multiple
title: CIM_CurrentSensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor
- CIM_CurrentSensor.Accuracy
- CIM_CurrentSensor.Availability
- CIM_CurrentSensor.Caption
- CIM_CurrentSensor.ConfigManagerErrorCode
- CIM_CurrentSensor.ConfigManagerUserConfig
- CIM_CurrentSensor.CreationClassName
- CIM_CurrentSensor.CurrentReading
- CIM_CurrentSensor.Description
- CIM_CurrentSensor.DeviceID
- CIM_CurrentSensor.ErrorCleared
- CIM_CurrentSensor.ErrorDescription
- CIM_CurrentSensor.InstallDate
- CIM_CurrentSensor.IsLinear
- CIM_CurrentSensor.LastErrorCode
- CIM_CurrentSensor.LowerThresholdCritical
- CIM_CurrentSensor.LowerThresholdFatal
- CIM_CurrentSensor.LowerThresholdNonCritical
- CIM_CurrentSensor.MaxReadable
- CIM_CurrentSensor.MinReadable
- CIM_CurrentSensor.Name
- CIM_CurrentSensor.NominalReading
- CIM_CurrentSensor.NormalMax
- CIM_CurrentSensor.NormalMin
- CIM_CurrentSensor.PNPDeviceID
- CIM_CurrentSensor.PowerManagementCapabilities
- CIM_CurrentSensor.PowerManagementSupported
- CIM_CurrentSensor.Resolution
- CIM_CurrentSensor.Status
- CIM_CurrentSensor.StatusInfo
- CIM_CurrentSensor.SystemCreationClassName
- CIM_CurrentSensor.SystemName
- CIM_CurrentSensor.Tolerance
- CIM_CurrentSensor.UpperThresholdCritical
- CIM_CurrentSensor.UpperThresholdFatal
- CIM_CurrentSensor.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1fe2a34e2e598d5c9655abbf84324dbf9982e416
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153186"
---
# <a name="cim_currentsensor-class"></a><span data-ttu-id="c98ec-103">\_Clase CurrentSensor de CIM</span><span class="sxs-lookup"><span data-stu-id="c98ec-103">CIM\_CurrentSensor class</span></span>

<span data-ttu-id="c98ec-104">La **clase \_ CurrentSensor de CIM** existe para la compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores.</span><span class="sxs-lookup"><span data-stu-id="c98ec-104">The **CIM\_CurrentSensor** class exists for backward compatibility to earlier CIM schema definitions.</span></span>

<span data-ttu-id="c98ec-105">Las adiciones [**al \_ sensor CIM**](cim-sensor.md) y [**CIM \_ NumericSensor**](cim-numericsensor.md) en la versión 2,2 hacen que ya no sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c98ec-105">Additions to [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) in version 2.2 make it no longer necessary.</span></span> <span data-ttu-id="c98ec-106">Se puede definir una clase **\_ CurrentSensor de CIM** estableciendo la propiedad **SensorType** , heredada **del \_ sensor CIM**, en 4 ("actual").</span><span class="sxs-lookup"><span data-stu-id="c98ec-106">A **CIM\_CurrentSensor** class can be defined by setting the **SensorType** property, inherited from **CIM\_Sensor**, to 4 ("Current").</span></span> <span data-ttu-id="c98ec-107">Otras propiedades de esta clase están codificadas de forma rígida en valores constantes, que corresponden a las definiciones de la jerarquía del sensor.</span><span class="sxs-lookup"><span data-stu-id="c98ec-107">Other properties of this class are hard-coded to constant values, which correspond to definitions in the sensor hierarchy.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c98ec-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c98ec-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c98ec-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c98ec-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c98ec-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c98ec-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c98ec-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c98ec-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c98ec-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c98ec-112">Syntax</span></span>

``` syntax
[UUID("{DCA1D084-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_CurrentSensor : CIM_NumericSensor
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

## <a name="members"></a><span data-ttu-id="c98ec-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="c98ec-113">Members</span></span>

<span data-ttu-id="c98ec-114">La clase **CIM \_ CurrentSensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c98ec-114">The **CIM\_CurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="c98ec-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="c98ec-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="c98ec-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c98ec-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c98ec-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="c98ec-117">Methods</span></span>

<span data-ttu-id="c98ec-118">La clase **CIM \_ CurrentSensor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c98ec-118">The **CIM\_CurrentSensor** class has these methods.</span></span>



| <span data-ttu-id="c98ec-119">Método</span><span class="sxs-lookup"><span data-stu-id="c98ec-119">Method</span></span>                                                                   | <span data-ttu-id="c98ec-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c98ec-120">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c98ec-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="c98ec-121">**Reset**</span></span>](reset-method-in-class-cim-currentsensor.md)                 | <span data-ttu-id="c98ec-122">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="c98ec-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c98ec-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c98ec-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c98ec-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-currentsensor.md) | <span data-ttu-id="c98ec-125">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="c98ec-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c98ec-126">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="c98ec-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c98ec-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c98ec-127">Properties</span></span>

<span data-ttu-id="c98ec-128">La clase **CIM \_ CurrentSensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c98ec-128">The **CIM\_CurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c98ec-129">**Precisión**</span><span class="sxs-lookup"><span data-stu-id="c98ec-129">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-130">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-132">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Accuracy"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-133">Precisión del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="c98ec-133">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="c98ec-134">Su valor se registra como más o menos centésimas de un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="c98ec-134">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="c98ec-135">Esta propiedad, y las propiedades de **resolución** y **tolerancia** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="c98ec-135">This property, and the **Resolution** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="c98ec-136">La precisión puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-136">Accuracy can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="c98ec-137">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-137">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-138">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="c98ec-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c98ec-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-141">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-142">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-142">Availability and status of the device.</span></span>

<span data-ttu-id="c98ec-143">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c98ec-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c98ec-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c98ec-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="c98ec-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c98ec-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="c98ec-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c98ec-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="c98ec-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c98ec-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="c98ec-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c98ec-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="c98ec-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c98ec-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="c98ec-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c98ec-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="c98ec-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c98ec-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="c98ec-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c98ec-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="c98ec-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c98ec-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="c98ec-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c98ec-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="c98ec-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c98ec-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="c98ec-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-157">Ahorro de energía desconocido.</span><span class="sxs-lookup"><span data-stu-id="c98ec-157">Power save   unknown.</span></span>

<span data-ttu-id="c98ec-158">El dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="c98ec-158">Device is in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c98ec-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="c98ec-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-160">Ahorro de energía: modo de baja energía.</span><span class="sxs-lookup"><span data-stu-id="c98ec-160">Power save   low-power mode.</span></span>

<span data-ttu-id="c98ec-161">El dispositivo está en modo de ahorro de energía y sigue funcionando, pero puede presentar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="c98ec-161">Device is in a power-save mode and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c98ec-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="c98ec-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-163">Ahorro de energía en espera.</span><span class="sxs-lookup"><span data-stu-id="c98ec-163">Power save   standby.</span></span>

<span data-ttu-id="c98ec-164">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="c98ec-164">Device is not functioning, but it could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c98ec-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="c98ec-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c98ec-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="c98ec-166"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-167">ADVERTENCIA de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="c98ec-167">Power save   warning.</span></span>

<span data-ttu-id="c98ec-168">El dispositivo se encuentra en estado de advertencia y en modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="c98ec-168">Device is in a warning state and a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c98ec-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="c98ec-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c98ec-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="c98ec-170"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c98ec-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="c98ec-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c98ec-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="c98ec-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-173">El sensor actual no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c98ec-173">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c98ec-174">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c98ec-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-177">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c98ec-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-178">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c98ec-178">Short textual description of the object.</span></span>

<span data-ttu-id="c98ec-179">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-180">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c98ec-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-181">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-183">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c98ec-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-184">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="c98ec-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c98ec-185">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c98ec-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c98ec-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="c98ec-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-188">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="c98ec-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c98ec-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c98ec-190">(1)</span><span class="sxs-lookup"><span data-stu-id="c98ec-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-191">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c98ec-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c98ec-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c98ec-193">(2)</span><span class="sxs-lookup"><span data-stu-id="c98ec-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c98ec-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c98ec-195">(3)</span><span class="sxs-lookup"><span data-stu-id="c98ec-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-196">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="c98ec-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c98ec-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c98ec-198">(4)</span><span class="sxs-lookup"><span data-stu-id="c98ec-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-199">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="c98ec-199">Device is not working properly.</span></span> <span data-ttu-id="c98ec-200">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="c98ec-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c98ec-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c98ec-202">(5)</span><span class="sxs-lookup"><span data-stu-id="c98ec-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-203">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="c98ec-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c98ec-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c98ec-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="c98ec-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-206">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c98ec-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c98ec-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c98ec-208">(7)</span><span class="sxs-lookup"><span data-stu-id="c98ec-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c98ec-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c98ec-210">(8)</span><span class="sxs-lookup"><span data-stu-id="c98ec-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-211">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c98ec-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c98ec-213">(9)</span><span class="sxs-lookup"><span data-stu-id="c98ec-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-214">El dispositivo no funciona correctamente. el firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-214">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c98ec-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c98ec-216">(10)</span><span class="sxs-lookup"><span data-stu-id="c98ec-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-217">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="c98ec-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c98ec-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c98ec-219">(11)</span><span class="sxs-lookup"><span data-stu-id="c98ec-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-220">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c98ec-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c98ec-222">(12)</span><span class="sxs-lookup"><span data-stu-id="c98ec-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-223">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="c98ec-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c98ec-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c98ec-225">(13)</span><span class="sxs-lookup"><span data-stu-id="c98ec-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-226">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c98ec-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c98ec-228">(14)</span><span class="sxs-lookup"><span data-stu-id="c98ec-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-229">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c98ec-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c98ec-231">(15)</span><span class="sxs-lookup"><span data-stu-id="c98ec-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-232">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="c98ec-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c98ec-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c98ec-234">(16)</span><span class="sxs-lookup"><span data-stu-id="c98ec-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-235">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c98ec-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c98ec-237">(17)</span><span class="sxs-lookup"><span data-stu-id="c98ec-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-238">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="c98ec-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c98ec-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c98ec-240">(18)</span><span class="sxs-lookup"><span data-stu-id="c98ec-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-241">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c98ec-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c98ec-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c98ec-243">(19)</span><span class="sxs-lookup"><span data-stu-id="c98ec-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c98ec-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c98ec-245">(20)</span><span class="sxs-lookup"><span data-stu-id="c98ec-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-246">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="c98ec-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c98ec-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c98ec-248">(21)</span><span class="sxs-lookup"><span data-stu-id="c98ec-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-249">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="c98ec-249">System failure.</span></span> <span data-ttu-id="c98ec-250">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="c98ec-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c98ec-251">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c98ec-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c98ec-253">(22)</span><span class="sxs-lookup"><span data-stu-id="c98ec-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-254">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="c98ec-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c98ec-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c98ec-256">(23)</span><span class="sxs-lookup"><span data-stu-id="c98ec-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-257">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="c98ec-257">System failure.</span></span> <span data-ttu-id="c98ec-258">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="c98ec-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c98ec-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c98ec-260">(24)</span><span class="sxs-lookup"><span data-stu-id="c98ec-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-261">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="c98ec-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c98ec-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c98ec-263">(25)</span><span class="sxs-lookup"><span data-stu-id="c98ec-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-264">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c98ec-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c98ec-266">(26)</span><span class="sxs-lookup"><span data-stu-id="c98ec-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-267">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c98ec-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c98ec-269">(27)</span><span class="sxs-lookup"><span data-stu-id="c98ec-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-270">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="c98ec-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c98ec-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c98ec-272">(28)</span><span class="sxs-lookup"><span data-stu-id="c98ec-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-273">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="c98ec-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c98ec-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c98ec-275">(29)</span><span class="sxs-lookup"><span data-stu-id="c98ec-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-276">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="c98ec-276">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c98ec-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-277"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c98ec-278">(30)</span><span class="sxs-lookup"><span data-stu-id="c98ec-278">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-279">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="c98ec-279">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c98ec-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="c98ec-280"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c98ec-281">31</span><span class="sxs-lookup"><span data-stu-id="c98ec-281">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-282">El dispositivo no funciona correctamente. Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="c98ec-282">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c98ec-283">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="c98ec-283">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-284">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c98ec-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-286">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c98ec-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-287">Indica si el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c98ec-287">Indicates whether the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c98ec-288">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-289">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c98ec-289">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-290">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-292">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c98ec-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-293">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="c98ec-293">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c98ec-294">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="c98ec-294">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c98ec-295">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-296">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="c98ec-296">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-297">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-297">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-299">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-299">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CurrentReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-300">Valor actual indicado por el sensor.</span><span class="sxs-lookup"><span data-stu-id="c98ec-300">Current value indicated by the sensor.</span></span>

<span data-ttu-id="c98ec-301">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-301">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-302">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c98ec-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-305">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="c98ec-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-306">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c98ec-306">Textual description of the object.</span></span>

<span data-ttu-id="c98ec-307">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-308">**ID**</span><span class="sxs-lookup"><span data-stu-id="c98ec-308">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-311">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c98ec-311">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-312">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-312">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c98ec-313">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-314">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c98ec-314">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-315">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c98ec-315">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-317">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="c98ec-317">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c98ec-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-319">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c98ec-319">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-322">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="c98ec-322">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c98ec-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-324">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c98ec-324">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-325">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c98ec-325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-327">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-328">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c98ec-328">Date and time when the object was installed.</span></span> <span data-ttu-id="c98ec-329">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c98ec-329">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c98ec-330">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-331">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="c98ec-331">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-332">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c98ec-332">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-334">Si es **true**, el sensor es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-334">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="c98ec-335">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-335">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-336">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c98ec-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-337">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-339">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c98ec-340">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-341">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="c98ec-341">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-342">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-342">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-344">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,13 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-344">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-345">Valor de umbral que especifica si el sensor está funcionando en condiciones críticas.</span><span class="sxs-lookup"><span data-stu-id="c98ec-345">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="c98ec-346">Si la propiedad **CurrentReading** está entre **LowerThresholdCritical** y **LowerThresholdFatal**, el estado actual es Critical.</span><span class="sxs-lookup"><span data-stu-id="c98ec-346">If the **CurrentReading** property is between **LowerThresholdCritical** and **LowerThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="c98ec-347">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-347">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-348">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="c98ec-348">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-349">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-349">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-351">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-351">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-352">Valor de umbral que especifica si el sensor está funcionando en condiciones irrecuperables.</span><span class="sxs-lookup"><span data-stu-id="c98ec-352">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="c98ec-353">Si la propiedad **CurrentReading** está por debajo de **LowerThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="c98ec-353">If the **CurrentReading** property is below **LowerThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="c98ec-354">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-354">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-355">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="c98ec-355">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-356">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-356">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-358">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-358">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("LowerThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-359">Valor de umbral que especifica si el sensor está funcionando en condiciones normales o no críticas.</span><span class="sxs-lookup"><span data-stu-id="c98ec-359">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="c98ec-360">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="c98ec-360">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="c98ec-361">Sin embargo, si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **LowerThresholdCritical**, el estado actual no es crítico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-361">If the **CurrentReading** property, however, is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="c98ec-362">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-362">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-363">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="c98ec-363">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-364">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-364">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-366">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-366">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-367">Valor mayor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-367">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="c98ec-368">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-368">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-369">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="c98ec-369">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-370">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-370">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-372">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-372">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MinReadable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-373">Valor menor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-373">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="c98ec-374">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-374">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-375">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c98ec-375">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-378">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="c98ec-378">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-379">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c98ec-379">Label by which the object is known.</span></span> <span data-ttu-id="c98ec-380">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="c98ec-380">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c98ec-381">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-381">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-382">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="c98ec-382">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-383">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-383">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-385">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-385">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NominalReading"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-386">Valor esperado para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-386">Expected value for the numeric sensor.</span></span>

<span data-ttu-id="c98ec-387">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-387">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-388">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="c98ec-388">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-389">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-389">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-391">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-391">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMax"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-392">Intervalo máximo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-392">Normal maximum range for the numeric sensor.</span></span>

<span data-ttu-id="c98ec-393">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-393">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-394">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="c98ec-394">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-395">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-395">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-397">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-397">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NormalMin"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-398">Intervalo mínimo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-398">Normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="c98ec-399">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-399">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-400">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c98ec-400">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-403">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c98ec-403">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-404">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-404">Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c98ec-405">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c98ec-405">Example: "\*PNP030b"</span></span>

<span data-ttu-id="c98ec-406">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-407">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c98ec-407">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-408">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c98ec-408">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-410">Capacidades específicas relacionadas con la energía del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-410">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="c98ec-411">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c98ec-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c98ec-412"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c98ec-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="c98ec-413"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c98ec-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="c98ec-414"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c98ec-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c98ec-415"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-416">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="c98ec-416">Power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c98ec-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="c98ec-417"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-418">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="c98ec-418">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c98ec-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="c98ec-419"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-420">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) .</span><span class="sxs-lookup"><span data-stu-id="c98ec-420">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c98ec-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="c98ec-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-422">El método [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="c98ec-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c98ec-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="c98ec-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c98ec-424">El método [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="c98ec-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-currentsensor.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c98ec-425">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c98ec-425">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-426">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c98ec-426">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-427">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-428">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="c98ec-428">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c98ec-429">Esta propiedad no indica que las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="c98ec-429">This property does not indicate that power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c98ec-430">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c98ec-430">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c98ec-431">Si **es false**, el valor entero 1, para la cadena "no compatible", debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="c98ec-431">If **FALSE**, the integer value 1, for the string "Not Supported", should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c98ec-432">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-433">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="c98ec-433">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-434">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-436">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-436">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Resolution"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-437">Capacidad del sensor para resolver las diferencias en la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="c98ec-437">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="c98ec-438">Esta propiedad, y las propiedades de **precisión** y **tolerancia** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="c98ec-438">This property, and the **Accuracy** and **Tolerance** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="c98ec-439">Este valor puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-439">This value can vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="c98ec-440">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-440">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-441">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c98ec-441">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-444">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c98ec-444">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-445">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c98ec-445">String that indicates the current status of the object.</span></span> <span data-ttu-id="c98ec-446">Se puede definir el estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-446">Operational and nonoperational status can be defined.</span></span> <span data-ttu-id="c98ec-447">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="c98ec-447">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c98ec-448">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="c98ec-448">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c98ec-449">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="c98ec-449">Nonoperational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c98ec-450">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="c98ec-450">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c98ec-451">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="c98ec-451">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c98ec-452">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-452">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c98ec-453">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c98ec-453">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c98ec-454">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="c98ec-454">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c98ec-455">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="c98ec-455">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c98ec-456">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c98ec-456">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c98ec-457">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="c98ec-457">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c98ec-458">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c98ec-458">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c98ec-459">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="c98ec-459">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c98ec-460">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="c98ec-460">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c98ec-461">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="c98ec-461">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c98ec-462">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="c98ec-462">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c98ec-463">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c98ec-463">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c98ec-464">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="c98ec-464">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c98ec-465">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="c98ec-465">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c98ec-466">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c98ec-466">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-467">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c98ec-467">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-468">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-469">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-470">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-470">State of the logical device.</span></span> <span data-ttu-id="c98ec-471">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="c98ec-471">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c98ec-472">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c98ec-473">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="c98ec-473">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c98ec-474">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="c98ec-474">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c98ec-475">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="c98ec-475">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c98ec-476">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="c98ec-476">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c98ec-477">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="c98ec-477">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c98ec-478">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c98ec-478">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-479">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-480">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-481">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c98ec-481">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-482">Propiedad **CreationClassName** del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c98ec-482">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="c98ec-483">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-484">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c98ec-484">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-485">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c98ec-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-486">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-487">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c98ec-487">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-488">Propiedad de **nombre** del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="c98ec-488">Scoping system's **Name** property.</span></span>

<span data-ttu-id="c98ec-489">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-489">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-490">**Tolerancia**</span><span class="sxs-lookup"><span data-stu-id="c98ec-490">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-491">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-491">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-492">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-493">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,18 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-493">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tolerance"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-494">Tolerancia del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="c98ec-494">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="c98ec-495">Esta propiedad, y las propiedades de **resolución** y **precisión** , se usan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="c98ec-495">This property, and the **Resolution** and **Accuracy** properties, are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="c98ec-496">La tolerancia puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-496">Tolerance can vary depending on whether the device is linear over its dynamic range.</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-497">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="c98ec-497">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-498">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-498">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-500">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-500">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-501">Valor de umbral que especifica si el sensor está funcionando en condiciones críticas.</span><span class="sxs-lookup"><span data-stu-id="c98ec-501">Threshold value that specifies whether the sensor is operating under critical conditions.</span></span> <span data-ttu-id="c98ec-502">Si la propiedad **CurrentReading** está entre **UpperThresholdCritical** y **UpperThresholdFatal**, el estado actual es Critical.</span><span class="sxs-lookup"><span data-stu-id="c98ec-502">If the **CurrentReading** property is between **UpperThresholdCritical** and **UpperThresholdFatal**, then the current state is critical.</span></span>

<span data-ttu-id="c98ec-503">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-503">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-504">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="c98ec-504">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-505">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-505">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-506">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-507">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-507">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdFatal"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-508">Valor de umbral que especifica si el sensor está funcionando en condiciones irrecuperables.</span><span class="sxs-lookup"><span data-stu-id="c98ec-508">Threshold value that specifies whether the sensor is operating under fatal conditions.</span></span> <span data-ttu-id="c98ec-509">Si la propiedad **CurrentReading** está por encima de **UpperThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="c98ec-509">If the **CurrentReading** property is above **UpperThresholdFatal**, then the current state is fatal.</span></span>

<span data-ttu-id="c98ec-510">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-510">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="c98ec-511">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="c98ec-511">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c98ec-512">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="c98ec-512">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c98ec-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98ec-514">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="c98ec-514">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("UpperThresholdNonCritical"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="c98ec-515">Valor de umbral que especifica si el sensor está funcionando en condiciones normales o no críticas.</span><span class="sxs-lookup"><span data-stu-id="c98ec-515">Threshold value that specifies whether the sensor is operating under normal or non-critical conditions.</span></span> <span data-ttu-id="c98ec-516">Si la propiedad **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="c98ec-516">If the **CurrentReading** property is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, then the sensor is reporting a normal value.</span></span> <span data-ttu-id="c98ec-517">Sin embargo, si la propiedad **CurrentReading** está entre **UpperThresholdNonCritical** y **UpperThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="c98ec-517">If the **CurrentReading** property, however, is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, then the current state is non-critical.</span></span>

<span data-ttu-id="c98ec-518">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-518">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c98ec-519">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c98ec-519">Remarks</span></span>

<span data-ttu-id="c98ec-520">La clase **CIM \_ CurrentSensor** se deriva de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-520">The **CIM\_CurrentSensor** class is derived from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

<span data-ttu-id="c98ec-521">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c98ec-521">WMI does not implement this class.</span></span> <span data-ttu-id="c98ec-522">Para obtener más información sobre las clases WMI derivadas de **CIM \_ CurrentSensor**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c98ec-522">For more information about WMI classes derived from **CIM\_CurrentSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c98ec-523">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c98ec-523">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c98ec-524">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c98ec-524">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c98ec-525">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c98ec-525">Requirements</span></span>



| <span data-ttu-id="c98ec-526">Requisito</span><span class="sxs-lookup"><span data-stu-id="c98ec-526">Requirement</span></span> | <span data-ttu-id="c98ec-527">Value</span><span class="sxs-lookup"><span data-stu-id="c98ec-527">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c98ec-528">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c98ec-528">Minimum supported client</span></span><br/> | <span data-ttu-id="c98ec-529">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c98ec-529">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c98ec-530">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c98ec-530">Minimum supported server</span></span><br/> | <span data-ttu-id="c98ec-531">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c98ec-531">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c98ec-532">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c98ec-532">Namespace</span></span><br/>                | <span data-ttu-id="c98ec-533">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c98ec-533">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c98ec-534">MOF</span><span class="sxs-lookup"><span data-stu-id="c98ec-534">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c98ec-535"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c98ec-535"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c98ec-536">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c98ec-536">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c98ec-537"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c98ec-537"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c98ec-538">Vea también</span><span class="sxs-lookup"><span data-stu-id="c98ec-538">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c98ec-539">**NumericSensor de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c98ec-539">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> </dl>

 

