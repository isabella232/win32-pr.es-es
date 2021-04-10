---
description: Win32 \_ TemperatureProbe&\# 32; La clase WMI representa las propiedades de un sensor de temperatura (termómetro electrónico).
ms.assetid: 63ba1ae2-6abc-4d86-a7f6-f02536ebd8ac
ms.tgt_platform: multiple
title: Win32_TemperatureProbe (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TemperatureProbe
- Win32_TemperatureProbe.Reset
- Win32_TemperatureProbe.SetPowerState
- Win32_TemperatureProbe.Accuracy
- Win32_TemperatureProbe.Availability
- Win32_TemperatureProbe.Caption
- Win32_TemperatureProbe.ConfigManagerErrorCode
- Win32_TemperatureProbe.ConfigManagerUserConfig
- Win32_TemperatureProbe.CreationClassName
- Win32_TemperatureProbe.CurrentReading
- Win32_TemperatureProbe.Description
- Win32_TemperatureProbe.DeviceID
- Win32_TemperatureProbe.ErrorCleared
- Win32_TemperatureProbe.ErrorDescription
- Win32_TemperatureProbe.InstallDate
- Win32_TemperatureProbe.IsLinear
- Win32_TemperatureProbe.LastErrorCode
- Win32_TemperatureProbe.LowerThresholdCritical
- Win32_TemperatureProbe.LowerThresholdFatal
- Win32_TemperatureProbe.LowerThresholdNonCritical
- Win32_TemperatureProbe.MaxReadable
- Win32_TemperatureProbe.MinReadable
- Win32_TemperatureProbe.Name
- Win32_TemperatureProbe.NominalReading
- Win32_TemperatureProbe.NormalMax
- Win32_TemperatureProbe.NormalMin
- Win32_TemperatureProbe.PNPDeviceID
- Win32_TemperatureProbe.PowerManagementCapabilities
- Win32_TemperatureProbe.PowerManagementSupported
- Win32_TemperatureProbe.Resolution
- Win32_TemperatureProbe.Status
- Win32_TemperatureProbe.StatusInfo
- Win32_TemperatureProbe.SystemCreationClassName
- Win32_TemperatureProbe.SystemName
- Win32_TemperatureProbe.Tolerance
- Win32_TemperatureProbe.UpperThresholdCritical
- Win32_TemperatureProbe.UpperThresholdFatal
- Win32_TemperatureProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6de4ed6334747e8313098075bc916a1975f520c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907243"
---
# <a name="win32_temperatureprobe-class"></a><span data-ttu-id="5809c-103">\_Clase Win32 TemperatureProbe</span><span class="sxs-lookup"><span data-stu-id="5809c-103">Win32\_TemperatureProbe class</span></span>

<span data-ttu-id="5809c-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ TemperatureProbe de Win32** representa las propiedades de un sensor de temperatura (termómetro electrónico).</span><span class="sxs-lookup"><span data-stu-id="5809c-104">The **Win32\_TemperatureProbe** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a temperature sensor (electronic thermometer).</span></span>

<span data-ttu-id="5809c-105">La mayor parte de la información que proporciona la clase WMI **\_ TemperatureProbe de Win32** procede de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="5809c-105">Most of the information that the **Win32\_TemperatureProbe** WMI class provides comes from SMBIOS.</span></span> <span data-ttu-id="5809c-106">No se pueden extraer las lecturas en tiempo real de la propiedad **CurrentReading** de las tablas de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="5809c-106">Real-time readings for the **CurrentReading** property cannot be extracted from SMBIOS tables.</span></span> <span data-ttu-id="5809c-107">Por esta razón, las implementaciones actuales de WMI no rellenan la propiedad **CurrentReading** .</span><span class="sxs-lookup"><span data-stu-id="5809c-107">For this reason, current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="5809c-108">La presencia de la propiedad **CurrentReading** se reserva para un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5809c-108">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="5809c-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5809c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5809c-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5809c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5809c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5809c-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABB-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_TemperatureProbe : CIM_TemperatureSensor
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

## <a name="members"></a><span data-ttu-id="5809c-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5809c-112">Members</span></span>

<span data-ttu-id="5809c-113">La **clase \_ TemperatureProbe de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5809c-113">The **Win32\_TemperatureProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="5809c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5809c-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="5809c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5809c-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5809c-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5809c-116">Methods</span></span>

<span data-ttu-id="5809c-117">La clase **Win32 \_ TemperatureProbe** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5809c-117">The **Win32\_TemperatureProbe** class has these methods.</span></span>



| <span data-ttu-id="5809c-118">Método</span><span class="sxs-lookup"><span data-stu-id="5809c-118">Method</span></span>            | <span data-ttu-id="5809c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5809c-119">Description</span></span>                                                                                                                                                                                                                     |
|:------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5809c-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5809c-120">**Reset**</span></span>         | <span data-ttu-id="5809c-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="5809c-121">Not implemented.</span></span> <span data-ttu-id="5809c-122">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-temperaturesensor.md) en [**CIM \_ TemperatureSensor**](cim-temperaturesensor.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="5809c-122">To implement this method, see the [**Reset**](reset-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="5809c-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5809c-123">**SetPowerState**</span></span> | <span data-ttu-id="5809c-124">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="5809c-124">Not implemented.</span></span> <span data-ttu-id="5809c-125">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) en [**CIM \_ TemperatureSensor**](cim-temperaturesensor.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="5809c-125">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-temperaturesensor.md) method in [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5809c-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5809c-126">Properties</span></span>

<span data-ttu-id="5809c-127">La **clase \_ TemperatureProbe de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5809c-127">The **Win32\_TemperatureProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5809c-128">**Precisión**</span><span class="sxs-lookup"><span data-stu-id="5809c-128">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-131">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="5809c-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-132">Precisión del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="5809c-132">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="5809c-133">Su valor se registra como más o menos centésimas de un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="5809c-133">Its value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="5809c-134">La precisión, la resolución y la tolerancia se utilizan para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="5809c-134">Accuracy, resolution, and tolerance are used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="5809c-135">La precisión puede variar y depende de si el dispositivo es lineal o no sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="5809c-135">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="5809c-136">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-136">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-137">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="5809c-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-138">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5809c-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-140">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5809c-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-141">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-141">Availability and status of the device.</span></span>

<span data-ttu-id="5809c-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5809c-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5809c-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5809c-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5809c-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5809c-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5809c-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5809c-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="5809c-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5809c-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="5809c-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5809c-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="5809c-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5809c-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="5809c-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5809c-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="5809c-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-151">Sin conexión</span><span class="sxs-lookup"><span data-stu-id="5809c-151">Offline</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5809c-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="5809c-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5809c-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5809c-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5809c-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5809c-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5809c-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="5809c-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5809c-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="5809c-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-157">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="5809c-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5809c-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="5809c-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-159">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="5809c-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5809c-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5809c-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-161">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="5809c-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5809c-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="5809c-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5809c-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="5809c-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-164">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5809c-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5809c-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5809c-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-166">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="5809c-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5809c-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="5809c-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-168">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="5809c-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5809c-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5809c-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-170">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="5809c-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5809c-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="5809c-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-172">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="5809c-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5809c-173">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5809c-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-176">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5809c-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-177">Breve descripción de un objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="5809c-177">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="5809c-178">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-179">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5809c-179">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-180">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5809c-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-182">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5809c-182">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-183">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="5809c-183">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5809c-184">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-184">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5809c-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5809c-185"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5809c-186"> (0)</span><span class="sxs-lookup"><span data-stu-id="5809c-186">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-187">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5809c-187">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5809c-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5809c-188"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5809c-189">(1)</span><span class="sxs-lookup"><span data-stu-id="5809c-189">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-190">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5809c-190">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5809c-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-191"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5809c-192">(2)</span><span class="sxs-lookup"><span data-stu-id="5809c-192">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5809c-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5809c-193"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5809c-194">(3)</span><span class="sxs-lookup"><span data-stu-id="5809c-194">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-195">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="5809c-195">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5809c-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="5809c-196"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5809c-197">(4)</span><span class="sxs-lookup"><span data-stu-id="5809c-197">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-198">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5809c-198">Device is not working properly.</span></span> <span data-ttu-id="5809c-199">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="5809c-199">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5809c-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="5809c-200"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5809c-201">(5)</span><span class="sxs-lookup"><span data-stu-id="5809c-201">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-202">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="5809c-202">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5809c-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5809c-203"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5809c-204"> (6)</span><span class="sxs-lookup"><span data-stu-id="5809c-204">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-205">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5809c-205">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5809c-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5809c-206"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5809c-207">(7)</span><span class="sxs-lookup"><span data-stu-id="5809c-207">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5809c-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-208"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5809c-209">(8)</span><span class="sxs-lookup"><span data-stu-id="5809c-209">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-210">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-210">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5809c-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="5809c-211"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5809c-212">(9)</span><span class="sxs-lookup"><span data-stu-id="5809c-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-213">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5809c-213">Device is not working properly.</span></span> <span data-ttu-id="5809c-214">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-214">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5809c-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="5809c-215"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5809c-216">(10)</span><span class="sxs-lookup"><span data-stu-id="5809c-216">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-217">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="5809c-217">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5809c-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-218"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5809c-219">(11)</span><span class="sxs-lookup"><span data-stu-id="5809c-219">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-220">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-220">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5809c-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="5809c-221"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5809c-222">(12)</span><span class="sxs-lookup"><span data-stu-id="5809c-222">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-223">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="5809c-223">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5809c-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-224"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5809c-225">(13)</span><span class="sxs-lookup"><span data-stu-id="5809c-225">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-226">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-226">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5809c-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-227"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5809c-228">(14)</span><span class="sxs-lookup"><span data-stu-id="5809c-228">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-229">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="5809c-229">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5809c-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="5809c-230"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5809c-231">(15)</span><span class="sxs-lookup"><span data-stu-id="5809c-231">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-232">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="5809c-232">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5809c-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-233"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5809c-234">(16)</span><span class="sxs-lookup"><span data-stu-id="5809c-234">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-235">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-235">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5809c-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="5809c-236"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5809c-237">(17)</span><span class="sxs-lookup"><span data-stu-id="5809c-237">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-238">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="5809c-238">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5809c-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-239"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5809c-240">(18)</span><span class="sxs-lookup"><span data-stu-id="5809c-240">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-241">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5809c-241">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5809c-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="5809c-242"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5809c-243">(19)</span><span class="sxs-lookup"><span data-stu-id="5809c-243">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5809c-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="5809c-244"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5809c-245">(20)</span><span class="sxs-lookup"><span data-stu-id="5809c-245">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-246">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="5809c-246">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5809c-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5809c-248">(21)</span><span class="sxs-lookup"><span data-stu-id="5809c-248">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-249">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="5809c-249">System failure.</span></span> <span data-ttu-id="5809c-250">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="5809c-250">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5809c-251">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-251">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5809c-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5809c-252"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5809c-253">(22)</span><span class="sxs-lookup"><span data-stu-id="5809c-253">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-254">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5809c-254">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5809c-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="5809c-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5809c-256">(23)</span><span class="sxs-lookup"><span data-stu-id="5809c-256">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-257">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="5809c-257">System failure.</span></span> <span data-ttu-id="5809c-258">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="5809c-258">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5809c-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="5809c-259"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5809c-260">(24)</span><span class="sxs-lookup"><span data-stu-id="5809c-260">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-261">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="5809c-261">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5809c-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-262"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5809c-263">(25)</span><span class="sxs-lookup"><span data-stu-id="5809c-263">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-264">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-264">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5809c-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-265"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5809c-266">(26)</span><span class="sxs-lookup"><span data-stu-id="5809c-266">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-267">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5809c-267">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5809c-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="5809c-268"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5809c-269">(27)</span><span class="sxs-lookup"><span data-stu-id="5809c-269">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-270">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="5809c-270">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5809c-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="5809c-271"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5809c-272">(28)</span><span class="sxs-lookup"><span data-stu-id="5809c-272">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-273">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="5809c-273">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5809c-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="5809c-274"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5809c-275">(29)</span><span class="sxs-lookup"><span data-stu-id="5809c-275">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-276">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5809c-276">Device is disabled.</span></span> <span data-ttu-id="5809c-277">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5809c-277">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5809c-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5809c-278"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5809c-279">(30)</span><span class="sxs-lookup"><span data-stu-id="5809c-279">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-280">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="5809c-280">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5809c-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5809c-281"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5809c-282">31</span><span class="sxs-lookup"><span data-stu-id="5809c-282">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-283">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5809c-283">Device is not working properly.</span></span> <span data-ttu-id="5809c-284">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5809c-284">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5809c-285">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5809c-285">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-286">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5809c-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-288">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5809c-288">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-289">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5809c-289">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5809c-290">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-290">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-291">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5809c-291">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-294">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5809c-294">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5809c-295">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5809c-295">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5809c-296">Cuando se usa con las otras propiedades clave de una clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="5809c-296">When used with the other key properties of a class, this property allows all instances of the class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="5809c-297">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-298">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="5809c-298">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-299">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-299">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-301">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-302">Valor actual indicado por el sensor.</span><span class="sxs-lookup"><span data-stu-id="5809c-302">Current value indicated by the sensor.</span></span>

<span data-ttu-id="5809c-303">Las implementaciones actuales de WMI no rellenan la propiedad **CurrentReading** .</span><span class="sxs-lookup"><span data-stu-id="5809c-303">Current implementations of WMI do not populate the **CurrentReading** property.</span></span> <span data-ttu-id="5809c-304">La presencia de la propiedad **CurrentReading** se reserva para un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5809c-304">The **CurrentReading** property's presence is reserved for future use.</span></span>

<span data-ttu-id="5809c-305">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-305">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-306">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5809c-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-309">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="5809c-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-310">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5809c-310">Description of the object.</span></span>

<span data-ttu-id="5809c-311">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-312">**ID**</span><span class="sxs-lookup"><span data-stu-id="5809c-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-313">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-315">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="5809c-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-316">Identificador único del sondeo actual.</span><span class="sxs-lookup"><span data-stu-id="5809c-316">Unique identifier of the current probe.</span></span>

<span data-ttu-id="5809c-317">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-318">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5809c-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-319">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5809c-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5809c-321">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="5809c-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="5809c-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5809c-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5809c-326">Más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que puede realizar.</span><span class="sxs-lookup"><span data-stu-id="5809c-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that you can take.</span></span>

<span data-ttu-id="5809c-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-328">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5809c-328">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-329">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5809c-329">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-331">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="5809c-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-332">Fecha y hora de instalación del objeto.</span><span class="sxs-lookup"><span data-stu-id="5809c-332">Date and time the object is installed.</span></span> <span data-ttu-id="5809c-333">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5809c-333">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5809c-334">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-334">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-335">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="5809c-335">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-336">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5809c-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5809c-338">Si es **true**, el sensor es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="5809c-338">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="5809c-339">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-339">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-340">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5809c-340">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-341">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5809c-341">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5809c-343">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5809c-343">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5809c-344">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-345">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="5809c-345">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-346">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-346">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-348">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,13 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-348">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.13"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-349">Valor de umbral de sensor para especificar los intervalos (valores mínimo y máximo) que identifican las condiciones de funcionamiento del sensor, que pueden ser condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="5809c-349">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="5809c-350">Si **CurrentReading** está entre **LowerThresholdCritical** y **LowerThresholdFatal**, el estado actual es crítico.</span><span class="sxs-lookup"><span data-stu-id="5809c-350">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="5809c-351">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-351">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-352">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="5809c-352">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-353">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-353">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-354">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-355">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,15 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-356">Valor de umbral de sensor para especificar los intervalos (valores mínimo y máximo) que identifican las condiciones de funcionamiento del sensor, que pueden ser condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="5809c-356">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="5809c-357">Si **CurrentReading** está por debajo de **LowerThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="5809c-357">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="5809c-358">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-358">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-359">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="5809c-359">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-360">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-360">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-362">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-363">Valor de umbral de sensor para especificar los intervalos (valores mínimo y máximo) que identifican las condiciones de funcionamiento del sensor, que pueden ser condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="5809c-363">Sensor threshold value to specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="5809c-364">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="5809c-364">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="5809c-365">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **LowerThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="5809c-365">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="5809c-366">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-367">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="5809c-367">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-368">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-370">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,9 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-371">Valor mayor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="5809c-371">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="5809c-372">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-373">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="5809c-373">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-374">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-374">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-376">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,10 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.10"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-377">Valor menor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="5809c-377">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="5809c-378">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-378">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-379">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5809c-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-380">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-382">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5809c-382">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-383">Etiqueta del objeto.</span><span class="sxs-lookup"><span data-stu-id="5809c-383">Label for the object.</span></span> <span data-ttu-id="5809c-384">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="5809c-384">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5809c-385">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-386">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="5809c-386">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-387">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-389">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,6 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-390">Valor normal o esperado para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="5809c-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="5809c-391">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-392">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="5809c-392">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-393">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-395">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,7 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-396">Valor normal o esperado para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="5809c-396">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="5809c-397">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-398">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="5809c-398">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-399">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-399">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-401">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-402">Instrucciones para el usuario sobre el intervalo mínimo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="5809c-402">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="5809c-403">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-403">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-404">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5809c-404">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-405">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-406">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-407">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5809c-407">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-408">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5809c-408">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5809c-409">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5809c-409">Example: "\*PNP030b"</span></span>

<span data-ttu-id="5809c-410">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-411">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5809c-411">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-412">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5809c-412">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5809c-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5809c-414">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5809c-414">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5809c-415">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5809c-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5809c-416"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5809c-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="5809c-417"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5809c-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5809c-418"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5809c-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5809c-419"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-420">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5809c-420">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5809c-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5809c-421"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-422">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="5809c-422">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5809c-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="5809c-423"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-424">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="5809c-424">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5809c-425">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="5809c-425">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5809c-426">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-426">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5809c-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="5809c-427"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-428">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="5809c-428">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5809c-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="5809c-429"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5809c-430">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="5809c-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5809c-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5809c-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-432">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5809c-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-433">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5809c-434">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="5809c-434">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="5809c-435">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="5809c-435">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="5809c-436">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-436">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-437">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="5809c-437">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-438">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5809c-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-439">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-440">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,17 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" centésimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-440">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.17"), [**Units**](../wmisdk/standard-qualifiers.md) ("hundredths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-441">Capacidad del sensor para resolver las diferencias en la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="5809c-441">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="5809c-442">Este valor puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="5809c-442">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="5809c-443">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-443">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-444">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5809c-444">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-445">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-447">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="5809c-447">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-448">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5809c-448">Current status of the object.</span></span> <span data-ttu-id="5809c-449">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="5809c-449">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5809c-450">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="5809c-450">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5809c-451">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="5809c-451">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5809c-452">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="5809c-452">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5809c-453">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="5809c-453">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5809c-454">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5809c-455">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5809c-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5809c-456">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="5809c-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5809c-457">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5809c-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5809c-458">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5809c-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5809c-459">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="5809c-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5809c-460">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5809c-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5809c-461">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="5809c-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5809c-462">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="5809c-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5809c-463">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="5809c-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5809c-464">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="5809c-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5809c-465">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5809c-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5809c-466">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="5809c-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5809c-467">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="5809c-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5809c-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5809c-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-469">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5809c-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-471">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5809c-471">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-472">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5809c-472">State of the logical device.</span></span> <span data-ttu-id="5809c-473">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="5809c-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5809c-474">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5809c-475">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5809c-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5809c-476">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5809c-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5809c-477">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5809c-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5809c-478">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5809c-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5809c-479">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="5809c-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5809c-480">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5809c-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-483">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5809c-483">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5809c-484">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5809c-484">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="5809c-485">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5809c-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5809c-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-488">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-489">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5809c-489">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5809c-490">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5809c-490">Name of the scoping system.</span></span>

<span data-ttu-id="5809c-491">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-492">**Tolerancia**</span><span class="sxs-lookup"><span data-stu-id="5809c-492">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-493">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-493">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-494">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-495">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,18 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-495">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.18"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-496">Tolerancia del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="5809c-496">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="5809c-497">La tolerancia, junto con la resolución y la precisión, se usa para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="5809c-497">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="5809c-498">La tolerancia puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="5809c-498">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="5809c-499">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-499">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-500">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="5809c-500">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-501">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-501">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-502">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-503">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,14 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-503">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.14"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-504">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) que identifican las condiciones de funcionamiento del sensor, que pueden ser condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="5809c-504">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="5809c-505">Si **CurrentReading** está entre **UpperThresholdCritical** y **UpperThresholdFatal**, el estado actual es crítico.</span><span class="sxs-lookup"><span data-stu-id="5809c-505">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="5809c-506">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-506">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-507">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="5809c-507">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-508">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-508">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-509">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-510">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,16 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-511">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) que identifican las condiciones de funcionamiento del sensor, que pueden ser condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="5809c-511">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="5809c-512">Si **CurrentReading** está por encima de **UpperThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="5809c-512">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="5809c-513">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-513">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="5809c-514">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="5809c-514">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5809c-515">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5809c-515">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5809c-516">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5809c-516">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5809c-517">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Sonda de temperatura DMTF \| 001,12 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" décimas de grados centigrade ")</span><span class="sxs-lookup"><span data-stu-id="5809c-517">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Temperature Probe\|001.12"), [**Units**](../wmisdk/standard-qualifiers.md) ("tenths of degrees centigrade")</span></span>
</dt> </dl>

<span data-ttu-id="5809c-518">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) que identifican las condiciones de funcionamiento del sensor, que pueden ser condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="5809c-518">Sensor's threshold values specify the ranges (minimum and maximum values) that identify the sensor operating conditions, which can be normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="5809c-519">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="5809c-519">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="5809c-520">Si **CurrentReading** está entre **UpperThresholdNonCritical** y **UpperThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="5809c-520">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="5809c-521">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-521">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5809c-522">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5809c-522">Remarks</span></span>

<span data-ttu-id="5809c-523">La **clase \_ TemperatureProbe de Win32** se deriva de [**\_ TemperatureSensor de CIM**](cim-temperaturesensor.md).</span><span class="sxs-lookup"><span data-stu-id="5809c-523">The **Win32\_TemperatureProbe** class is derived from [**CIM\_TemperatureSensor**](cim-temperaturesensor.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5809c-524">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5809c-524">Examples</span></span>

<span data-ttu-id="5809c-525">En el ejemplo siguiente se devuelven datos de sondeo de temperatura para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="5809c-525">The following example returns temperature probe data for the local computer.</span></span>


```VB
strComputer = "."
Set colTempProbe = GetObject("Winmgmts:"_
    & "{impersonationLevel=impersonate}!\\"_ 
    & strComputer & "\root\cimv2")._
    InstancesOf("Win32_TemperatureProbe")
Num = 0
For Each obj In colTempProbe      
    WScript.Echo   obj.Name & VBNewLine _
        & obj.DeviceID & VBNewLine _
        & obj.Status & VBNewLine _
        & obj.Resolution & VBNewLine _
        & obj.Tolerance & VBNewLine _
        & obj.Accuracy 
    Num = Num +1
Next
If Num = 0 Then
    WScript.Echo "No temperature probe data"
End If
```



## <a name="requirements"></a><span data-ttu-id="5809c-526">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5809c-526">Requirements</span></span>



| <span data-ttu-id="5809c-527">Requisito</span><span class="sxs-lookup"><span data-stu-id="5809c-527">Requirement</span></span> | <span data-ttu-id="5809c-528">Value</span><span class="sxs-lookup"><span data-stu-id="5809c-528">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5809c-529">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5809c-529">Minimum supported client</span></span><br/> | <span data-ttu-id="5809c-530">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5809c-530">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5809c-531">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5809c-531">Minimum supported server</span></span><br/> | <span data-ttu-id="5809c-532">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5809c-532">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5809c-533">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5809c-533">Namespace</span></span><br/>                | <span data-ttu-id="5809c-534">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5809c-534">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5809c-535">MOF</span><span class="sxs-lookup"><span data-stu-id="5809c-535">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5809c-536"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5809c-536"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5809c-537">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5809c-537">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5809c-538"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5809c-538"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5809c-539">Vea también</span><span class="sxs-lookup"><span data-stu-id="5809c-539">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5809c-540">**\_TEMPERATURESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="5809c-540">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dt>

[<span data-ttu-id="5809c-541">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="5809c-541">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
