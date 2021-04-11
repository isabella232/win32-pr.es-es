---
description: La \_ clase WMI VoltageProbe de Win32 representa las propiedades de un detector de voltaje (voltímetro electrónico).
ms.assetid: ca27c1df-fb38-412d-b77c-d9ccf7941c66
ms.tgt_platform: multiple
title: Win32_VoltageProbe (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VoltageProbe
- Win32_VoltageProbe.Reset
- Win32_VoltageProbe.SetPowerState
- Win32_VoltageProbe.Accuracy
- Win32_VoltageProbe.Availability
- Win32_VoltageProbe.Caption
- Win32_VoltageProbe.ConfigManagerErrorCode
- Win32_VoltageProbe.ConfigManagerUserConfig
- Win32_VoltageProbe.CreationClassName
- Win32_VoltageProbe.CurrentReading
- Win32_VoltageProbe.Description
- Win32_VoltageProbe.DeviceID
- Win32_VoltageProbe.ErrorCleared
- Win32_VoltageProbe.ErrorDescription
- Win32_VoltageProbe.InstallDate
- Win32_VoltageProbe.IsLinear
- Win32_VoltageProbe.LastErrorCode
- Win32_VoltageProbe.LowerThresholdCritical
- Win32_VoltageProbe.LowerThresholdFatal
- Win32_VoltageProbe.LowerThresholdNonCritical
- Win32_VoltageProbe.MaxReadable
- Win32_VoltageProbe.MinReadable
- Win32_VoltageProbe.Name
- Win32_VoltageProbe.NominalReading
- Win32_VoltageProbe.NormalMax
- Win32_VoltageProbe.NormalMin
- Win32_VoltageProbe.PNPDeviceID
- Win32_VoltageProbe.PowerManagementCapabilities
- Win32_VoltageProbe.PowerManagementSupported
- Win32_VoltageProbe.Resolution
- Win32_VoltageProbe.Status
- Win32_VoltageProbe.StatusInfo
- Win32_VoltageProbe.SystemCreationClassName
- Win32_VoltageProbe.SystemName
- Win32_VoltageProbe.Tolerance
- Win32_VoltageProbe.UpperThresholdCritical
- Win32_VoltageProbe.UpperThresholdFatal
- Win32_VoltageProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: acb5fe56706ed55098443ad9667eb980a1fe6d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274853"
---
# <a name="win32_voltageprobe-class"></a><span data-ttu-id="d14d1-103">\_Clase Win32 VoltageProbe</span><span class="sxs-lookup"><span data-stu-id="d14d1-103">Win32\_VoltageProbe class</span></span>

<span data-ttu-id="d14d1-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ VoltageProbe de Win32** representa las propiedades de un detector de voltaje (voltímetro electrónico).</span><span class="sxs-lookup"><span data-stu-id="d14d1-104">The **Win32\_VoltageProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a voltage sensor (electronic voltmeter).</span></span>

<span data-ttu-id="d14d1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d14d1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d14d1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d14d1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d14d1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d14d1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB8-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_VoltageProbe : CIM_VoltageSensor
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

## <a name="members"></a><span data-ttu-id="d14d1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d14d1-108">Members</span></span>

<span data-ttu-id="d14d1-109">La **clase \_ VoltageProbe de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d14d1-109">The **Win32\_VoltageProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="d14d1-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d14d1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d14d1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d14d1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d14d1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d14d1-112">Methods</span></span>

<span data-ttu-id="d14d1-113">La clase **Win32 \_ VoltageProbe** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d14d1-113">The **Win32\_VoltageProbe** class has these methods.</span></span>



| <span data-ttu-id="d14d1-114">Método</span><span class="sxs-lookup"><span data-stu-id="d14d1-114">Method</span></span>            | <span data-ttu-id="d14d1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d14d1-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d14d1-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="d14d1-116">**Reset**</span></span>         | <span data-ttu-id="d14d1-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d14d1-117">Not implemented.</span></span> <span data-ttu-id="d14d1-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ VoltageSensor**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/>                 |
| <span data-ttu-id="d14d1-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d14d1-119">**SetPowerState**</span></span> | <span data-ttu-id="d14d1-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d14d1-120">Not implemented.</span></span> <span data-ttu-id="d14d1-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ VoltageSensor**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d14d1-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d14d1-122">Properties</span></span>

<span data-ttu-id="d14d1-123">La **clase \_ VoltageProbe de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d14d1-123">The **Win32\_VoltageProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d14d1-124">**Precisión**</span><span class="sxs-lookup"><span data-stu-id="d14d1-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-125">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-127">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Sonda de voltaje de DMTF \| \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-128">Precisión del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="d14d1-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="d14d1-129">El valor de precisión se registra como más o menos centésimas de un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="d14d1-129">The accuracy value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="d14d1-130">La precisión, junto con la resolución y la tolerancia, se usa para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="d14d1-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="d14d1-131">La precisión puede variar y depende de si el dispositivo es lineal o no en su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-131">The accuracy may vary and depends on whether or not the device is linear in its dynamic range.</span></span>

<span data-ttu-id="d14d1-132">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-133">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="d14d1-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-134">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d14d1-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-136">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-137">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-137">Availability and status of the device.</span></span>

<span data-ttu-id="d14d1-138">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d14d1-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d14d1-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d14d1-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d14d1-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d14d1-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d14d1-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d14d1-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="d14d1-142"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d14d1-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="d14d1-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d14d1-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d14d1-144"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d14d1-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="d14d1-145"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d14d1-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="d14d1-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d14d1-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="d14d1-147"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d14d1-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="d14d1-148"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d14d1-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="d14d1-149"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d14d1-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="d14d1-150"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d14d1-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="d14d1-151"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-152">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="d14d1-152">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d14d1-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="d14d1-153"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-154">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="d14d1-154">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d14d1-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="d14d1-155"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-156">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="d14d1-156">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d14d1-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="d14d1-157"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d14d1-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="d14d1-158"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-159">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="d14d1-159">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d14d1-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d14d1-160"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-161">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="d14d1-161">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d14d1-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="d14d1-162"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-163">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-163">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d14d1-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="d14d1-164"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-165">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="d14d1-165">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d14d1-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d14d1-166"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-167">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="d14d1-167">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d14d1-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d14d1-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-171">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d14d1-171">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-172">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="d14d1-172">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="d14d1-173">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d14d1-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-175">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-177">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d14d1-177">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-178">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="d14d1-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d14d1-179">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d14d1-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d14d1-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="d14d1-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-182">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d14d1-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d14d1-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d14d1-184">(1)</span><span class="sxs-lookup"><span data-stu-id="d14d1-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-185">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d14d1-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d14d1-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d14d1-187">(2)</span><span class="sxs-lookup"><span data-stu-id="d14d1-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d14d1-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d14d1-189">(3)</span><span class="sxs-lookup"><span data-stu-id="d14d1-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-190">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="d14d1-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d14d1-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d14d1-192">(4)</span><span class="sxs-lookup"><span data-stu-id="d14d1-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-193">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d14d1-193">Device is not working properly.</span></span> <span data-ttu-id="d14d1-194">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="d14d1-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d14d1-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d14d1-196">(5)</span><span class="sxs-lookup"><span data-stu-id="d14d1-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-197">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="d14d1-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d14d1-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d14d1-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="d14d1-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-200">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d14d1-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d14d1-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d14d1-202">(7)</span><span class="sxs-lookup"><span data-stu-id="d14d1-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d14d1-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d14d1-204">(8)</span><span class="sxs-lookup"><span data-stu-id="d14d1-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-205">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d14d1-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d14d1-207">(9)</span><span class="sxs-lookup"><span data-stu-id="d14d1-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-208">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d14d1-208">Device is not working properly.</span></span> <span data-ttu-id="d14d1-209">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d14d1-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d14d1-211">(10)</span><span class="sxs-lookup"><span data-stu-id="d14d1-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-212">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="d14d1-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d14d1-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d14d1-214">(11)</span><span class="sxs-lookup"><span data-stu-id="d14d1-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-215">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d14d1-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d14d1-217">(12)</span><span class="sxs-lookup"><span data-stu-id="d14d1-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-218">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="d14d1-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d14d1-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d14d1-220">(13)</span><span class="sxs-lookup"><span data-stu-id="d14d1-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-221">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d14d1-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d14d1-223">(14)</span><span class="sxs-lookup"><span data-stu-id="d14d1-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-224">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d14d1-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d14d1-226">(15)</span><span class="sxs-lookup"><span data-stu-id="d14d1-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-227">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="d14d1-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d14d1-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d14d1-229">(16)</span><span class="sxs-lookup"><span data-stu-id="d14d1-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-230">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d14d1-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d14d1-232">(17)</span><span class="sxs-lookup"><span data-stu-id="d14d1-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-233">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="d14d1-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d14d1-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d14d1-235">(18)</span><span class="sxs-lookup"><span data-stu-id="d14d1-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-236">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d14d1-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d14d1-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d14d1-238">(19)</span><span class="sxs-lookup"><span data-stu-id="d14d1-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d14d1-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d14d1-240">(20)</span><span class="sxs-lookup"><span data-stu-id="d14d1-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-241">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="d14d1-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d14d1-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d14d1-243">(21)</span><span class="sxs-lookup"><span data-stu-id="d14d1-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d14d1-244">System failure.</span></span> <span data-ttu-id="d14d1-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d14d1-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d14d1-246">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d14d1-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d14d1-248">(22)</span><span class="sxs-lookup"><span data-stu-id="d14d1-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-249">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d14d1-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d14d1-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d14d1-251">(23)</span><span class="sxs-lookup"><span data-stu-id="d14d1-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-252">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d14d1-252">System failure.</span></span> <span data-ttu-id="d14d1-253">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d14d1-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d14d1-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d14d1-255">(24)</span><span class="sxs-lookup"><span data-stu-id="d14d1-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-256">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="d14d1-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d14d1-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d14d1-258">(25)</span><span class="sxs-lookup"><span data-stu-id="d14d1-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-259">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d14d1-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d14d1-261">(26)</span><span class="sxs-lookup"><span data-stu-id="d14d1-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-262">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d14d1-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d14d1-264">(27)</span><span class="sxs-lookup"><span data-stu-id="d14d1-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-265">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="d14d1-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d14d1-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d14d1-267">(28)</span><span class="sxs-lookup"><span data-stu-id="d14d1-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-268">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="d14d1-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d14d1-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d14d1-270">(29)</span><span class="sxs-lookup"><span data-stu-id="d14d1-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-271">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d14d1-271">Device is disabled.</span></span> <span data-ttu-id="d14d1-272">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d14d1-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d14d1-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d14d1-274">(30)</span><span class="sxs-lookup"><span data-stu-id="d14d1-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-275">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="d14d1-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d14d1-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d14d1-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d14d1-277">31</span><span class="sxs-lookup"><span data-stu-id="d14d1-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-278">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d14d1-278">Device is not working properly.</span></span> <span data-ttu-id="d14d1-279">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d14d1-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d14d1-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d14d1-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-281">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d14d1-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-283">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d14d1-283">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-284">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d14d1-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d14d1-285">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d14d1-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-287">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-289">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d14d1-289">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-290">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="d14d1-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d14d1-291">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="d14d1-291">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d14d1-292">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-293">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="d14d1-293">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-294">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-294">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-296">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-297">Valor actual indicado por el sensor.</span><span class="sxs-lookup"><span data-stu-id="d14d1-297">Current value indicated by the sensor.</span></span>

<span data-ttu-id="d14d1-298">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-298">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-299">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d14d1-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-302">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="d14d1-302">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-303">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d14d1-303">Description of the object.</span></span>

<span data-ttu-id="d14d1-304">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-305">**ID**</span><span class="sxs-lookup"><span data-stu-id="d14d1-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-306">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-308">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d14d1-308">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-309">Identificador único del sondeo de voltaje.</span><span class="sxs-lookup"><span data-stu-id="d14d1-309">Unique identifier of the voltage probe.</span></span>

<span data-ttu-id="d14d1-310">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d14d1-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-312">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d14d1-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-314">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="d14d1-314">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d14d1-315">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d14d1-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-319">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="d14d1-319">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="d14d1-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d14d1-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-322">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d14d1-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-324">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-324">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-325">Fecha y hora de instalación del objeto.</span><span class="sxs-lookup"><span data-stu-id="d14d1-325">Date and time the object is installed.</span></span> <span data-ttu-id="d14d1-326">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d14d1-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d14d1-327">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-328">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="d14d1-328">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-329">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d14d1-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-331">Si es **true**, el sensor es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-331">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="d14d1-332">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-332">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-333">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d14d1-333">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-334">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-334">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-336">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-336">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d14d1-337">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-338">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="d14d1-338">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-339">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-341">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,13 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-341">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-342">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d14d1-342">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d14d1-343">Si **CurrentReading** está entre **LowerThresholdCritical** y **LowerThresholdFatal**, el estado actual es crítico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-343">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="d14d1-344">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-344">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-345">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="d14d1-345">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-346">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-348">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,15 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-349">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d14d1-349">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d14d1-350">Si **CurrentReading** está por debajo de **LowerThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="d14d1-350">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="d14d1-351">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-352">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="d14d1-352">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-353">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-355">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-356">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d14d1-356">Sensor threshold values specify the ranges (minimum and maximum values) to determine if the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d14d1-357">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="d14d1-357">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="d14d1-358">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **LowerThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="d14d1-359">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-359">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-360">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="d14d1-360">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-361">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-361">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-363">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,9 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-364">Valor mayor de la propiedad medida que puede leer el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-364">Largest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="d14d1-365">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-365">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-366">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="d14d1-366">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-367">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-367">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-369">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,10 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-370">Valor menor de la propiedad medida que el sensor numérico puede leer.</span><span class="sxs-lookup"><span data-stu-id="d14d1-370">Smallest value of the measured property that the numeric sensor can read.</span></span>

<span data-ttu-id="d14d1-371">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-371">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-372">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d14d1-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-375">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d14d1-375">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-376">Etiqueta para un objeto.</span><span class="sxs-lookup"><span data-stu-id="d14d1-376">Label for an object.</span></span> <span data-ttu-id="d14d1-377">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="d14d1-377">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d14d1-378">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-379">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="d14d1-379">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-380">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-380">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-382">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,6 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-382">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-383">Valor normal o esperado para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-383">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="d14d1-384">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-384">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-385">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="d14d1-385">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-386">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-386">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-388">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,7 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-389">Valor normal o esperado para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-389">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="d14d1-390">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-390">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-391">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="d14d1-391">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-392">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-392">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-394">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-394">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-395">Instrucciones para que el usuario indique el intervalo mínimo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-395">Guidance for the user to indicate the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="d14d1-396">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-396">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-397">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d14d1-397">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-398">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-400">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d14d1-400">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-401">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-401">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d14d1-402">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d14d1-403">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d14d1-403">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-404">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d14d1-404">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-405">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d14d1-405">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-407">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-407">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d14d1-408">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="d14d1-408">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d14d1-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d14d1-409"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d14d1-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d14d1-410"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d14d1-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d14d1-411"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d14d1-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d14d1-412"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-413">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d14d1-413">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d14d1-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d14d1-414"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-415">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="d14d1-415">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d14d1-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="d14d1-416"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-417">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d14d1-417">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d14d1-418">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="d14d1-418">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d14d1-419">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-419">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d14d1-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="d14d1-420"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-421">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="d14d1-421">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d14d1-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="d14d1-422"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d14d1-423">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="d14d1-423">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d14d1-424">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d14d1-424">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-425">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d14d1-425">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-427">Si **es true**, el dispositivo puede administrarse mediante energía, lo que significa que se puede poner en modo de suspensión, etc.</span><span class="sxs-lookup"><span data-stu-id="d14d1-427">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="d14d1-428">La propiedad no indica que las características de administración de energía están habilitadas actualmente, pero indica que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="d14d1-428">The property does not indicate that power management features are currently enabled, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="d14d1-429">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-429">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-430">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="d14d1-430">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-431">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-431">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-433">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,17 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-433">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-434">Capacidad del sensor para resolver las diferencias en la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="d14d1-434">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="d14d1-435">Este valor puede variar y depende de si el dispositivo es lineal en su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-435">This value may vary and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="d14d1-436">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-436">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-437">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d14d1-437">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-438">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-438">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-440">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="d14d1-440">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-441">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d14d1-441">Current status of the object.</span></span> <span data-ttu-id="d14d1-442">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="d14d1-442">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d14d1-443">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d14d1-443">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d14d1-444">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d14d1-444">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d14d1-445">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d14d1-445">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d14d1-446">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d14d1-446">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d14d1-447">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d14d1-448">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d14d1-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d14d1-449">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="d14d1-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d14d1-450">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="d14d1-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d14d1-451">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d14d1-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d14d1-452">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="d14d1-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d14d1-453">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d14d1-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d14d1-454">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="d14d1-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d14d1-455">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="d14d1-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d14d1-456">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="d14d1-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d14d1-457">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="d14d1-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d14d1-458">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d14d1-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d14d1-459">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="d14d1-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d14d1-460">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="d14d1-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d14d1-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d14d1-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-462">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d14d1-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-463">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-464">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-464">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-465">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-465">State of the logical device.</span></span> <span data-ttu-id="d14d1-466">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="d14d1-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d14d1-467">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d14d1-468">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d14d1-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d14d1-469">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d14d1-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d14d1-470">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d14d1-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d14d1-471">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="d14d1-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d14d1-472">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d14d1-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d14d1-473">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d14d1-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-474">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-476">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d14d1-476">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-477">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d14d1-477">Value for the **CreationClassName** property of the scoping computer.</span></span>

<span data-ttu-id="d14d1-478">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d14d1-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-480">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d14d1-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-482">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d14d1-482">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-483">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d14d1-483">Name of the scoping system.</span></span>

<span data-ttu-id="d14d1-484">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-485">**Tolerancia**</span><span class="sxs-lookup"><span data-stu-id="d14d1-485">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-486">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-486">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-488">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,18 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-488">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-489">Tolerancia del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="d14d1-489">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="d14d1-490">La tolerancia, junto con la resolución y la precisión, se usa para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="d14d1-490">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="d14d1-491">La tolerancia puede variar y depende de si el dispositivo es lineal en su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-491">Tolerance may vary, and depends on whether the device is linear in its dynamic range.</span></span>

<span data-ttu-id="d14d1-492">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-492">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-493">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="d14d1-493">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-494">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-494">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-496">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,14 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-496">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-497">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d14d1-497">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d14d1-498">Si **CurrentReading** está entre **UpperThresholdCritical** y **UpperThresholdFatal**, el estado actual es crítico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-498">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="d14d1-499">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-500">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="d14d1-500">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-501">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-502">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-503">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,16 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-504">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d14d1-504">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d14d1-505">Si **CurrentReading** está por encima de **UpperThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="d14d1-505">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="d14d1-506">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d14d1-507">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="d14d1-507">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d14d1-508">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d14d1-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-509">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d14d1-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d14d1-510">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de voltaje \| de DMTF 001,12 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="d14d1-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Voltage Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="d14d1-511">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d14d1-511">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d14d1-512">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="d14d1-512">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="d14d1-513">Si **CurrentReading** está entre **UpperThresholdNonCritical** y **UpperThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="d14d1-513">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="d14d1-514">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-514">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d14d1-515">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d14d1-515">Remarks</span></span>

<span data-ttu-id="d14d1-516">La **clase \_ VoltageProbe de Win32** se deriva de [**\_ VoltageSensor de CIM**](cim-voltagesensor.md).</span><span class="sxs-lookup"><span data-stu-id="d14d1-516">The **Win32\_VoltageProbe** class is derived from [**CIM\_VoltageSensor**](cim-voltagesensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d14d1-517">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d14d1-517">Requirements</span></span>



| <span data-ttu-id="d14d1-518">Requisito</span><span class="sxs-lookup"><span data-stu-id="d14d1-518">Requirement</span></span> | <span data-ttu-id="d14d1-519">Value</span><span class="sxs-lookup"><span data-stu-id="d14d1-519">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d14d1-520">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d14d1-520">Minimum supported client</span></span><br/> | <span data-ttu-id="d14d1-521">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d14d1-521">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d14d1-522">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d14d1-522">Minimum supported server</span></span><br/> | <span data-ttu-id="d14d1-523">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d14d1-523">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d14d1-524">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d14d1-524">Namespace</span></span><br/>                | <span data-ttu-id="d14d1-525">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d14d1-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d14d1-526">MOF</span><span class="sxs-lookup"><span data-stu-id="d14d1-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d14d1-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d14d1-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d14d1-528">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d14d1-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d14d1-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d14d1-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d14d1-530">Vea también</span><span class="sxs-lookup"><span data-stu-id="d14d1-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d14d1-531">**\_VOLTAGESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="d14d1-531">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dt>

[<span data-ttu-id="d14d1-532">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d14d1-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
