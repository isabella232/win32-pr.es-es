---
description: La \_ clase WMI CurrentProbe de Win32 representa las propiedades de un sensor de supervisión actual (ammeter).
ms.assetid: 2e1da856-b787-404b-ac4b-080c4950bad8
ms.tgt_platform: multiple
title: Win32_CurrentProbe (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CurrentProbe
- Win32_CurrentProbe.Reset
- Win32_CurrentProbe.SetPowerState
- Win32_CurrentProbe.Accuracy
- Win32_CurrentProbe.Availability
- Win32_CurrentProbe.Caption
- Win32_CurrentProbe.ConfigManagerErrorCode
- Win32_CurrentProbe.ConfigManagerUserConfig
- Win32_CurrentProbe.CreationClassName
- Win32_CurrentProbe.CurrentReading
- Win32_CurrentProbe.Description
- Win32_CurrentProbe.DeviceID
- Win32_CurrentProbe.ErrorCleared
- Win32_CurrentProbe.ErrorDescription
- Win32_CurrentProbe.InstallDate
- Win32_CurrentProbe.IsLinear
- Win32_CurrentProbe.LastErrorCode
- Win32_CurrentProbe.LowerThresholdCritical
- Win32_CurrentProbe.LowerThresholdFatal
- Win32_CurrentProbe.LowerThresholdNonCritical
- Win32_CurrentProbe.MaxReadable
- Win32_CurrentProbe.MinReadable
- Win32_CurrentProbe.Name
- Win32_CurrentProbe.NominalReading
- Win32_CurrentProbe.NormalMax
- Win32_CurrentProbe.NormalMin
- Win32_CurrentProbe.PNPDeviceID
- Win32_CurrentProbe.PowerManagementCapabilities
- Win32_CurrentProbe.PowerManagementSupported
- Win32_CurrentProbe.Resolution
- Win32_CurrentProbe.Status
- Win32_CurrentProbe.StatusInfo
- Win32_CurrentProbe.SystemCreationClassName
- Win32_CurrentProbe.SystemName
- Win32_CurrentProbe.Tolerance
- Win32_CurrentProbe.UpperThresholdCritical
- Win32_CurrentProbe.UpperThresholdFatal
- Win32_CurrentProbe.UpperThresholdNonCritical
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be834e56eb3d958a8cd6ee653dc9a248c14ae3bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907526"
---
# <a name="win32_currentprobe-class"></a><span data-ttu-id="d4236-103">\_Clase Win32 CurrentProbe</span><span class="sxs-lookup"><span data-stu-id="d4236-103">Win32\_CurrentProbe class</span></span>

<span data-ttu-id="d4236-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CurrentProbe de Win32** representa las propiedades de un sensor de supervisión actual (ammeter).</span><span class="sxs-lookup"><span data-stu-id="d4236-104">The **Win32\_CurrentProbe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a current monitoring sensor (ammeter).</span></span>

<span data-ttu-id="d4236-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d4236-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d4236-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d4236-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4236-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4236-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFABA-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_CurrentProbe : CIM_CurrentSensor
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

## <a name="members"></a><span data-ttu-id="d4236-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4236-108">Members</span></span>

<span data-ttu-id="d4236-109">La **clase \_ CurrentProbe de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d4236-109">The **Win32\_CurrentProbe** class has these types of members:</span></span>

-   [<span data-ttu-id="d4236-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4236-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="d4236-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4236-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d4236-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4236-112">Methods</span></span>

<span data-ttu-id="d4236-113">La clase **Win32 \_ CurrentProbe** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d4236-113">The **Win32\_CurrentProbe** class has these methods.</span></span>



| <span data-ttu-id="d4236-114">Método</span><span class="sxs-lookup"><span data-stu-id="d4236-114">Method</span></span>            | <span data-ttu-id="d4236-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4236-115">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4236-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="d4236-116">**Reset**</span></span>         | <span data-ttu-id="d4236-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d4236-117">Not implemented.</span></span> <span data-ttu-id="d4236-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ CurrentSensor**](cim-currentsensor.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="d4236-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="d4236-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d4236-119">**SetPowerState**</span></span> | <span data-ttu-id="d4236-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="d4236-120">Not implemented.</span></span> <span data-ttu-id="d4236-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ CurrentSensor**](cim-currentsensor.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="d4236-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CurrentSensor**](cim-currentsensor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d4236-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4236-122">Properties</span></span>

<span data-ttu-id="d4236-123">La **clase \_ CurrentProbe de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d4236-123">The **Win32\_CurrentProbe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4236-124">**Precisión**</span><span class="sxs-lookup"><span data-stu-id="d4236-124">**Accuracy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-125">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-127">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,19 ")</span><span class="sxs-lookup"><span data-stu-id="d4236-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.19")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-128">Precisión del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="d4236-128">Accuracy of the sensor for the measured property.</span></span> <span data-ttu-id="d4236-129">El valor se registra como más o menos centésimas de un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="d4236-129">The value is recorded as plus or minus hundredths of a percent.</span></span> <span data-ttu-id="d4236-130">La precisión, junto con la resolución y la tolerancia, se usa para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="d4236-130">Accuracy, along with resolution and tolerance, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="d4236-131">La precisión puede variar y depende de si el dispositivo es lineal o no sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d4236-131">Accuracy may vary and depends on whether or not the device is linear over its dynamic range.</span></span>

<span data-ttu-id="d4236-132">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-132">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-133">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="d4236-133">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-134">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4236-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-136">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d4236-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-137">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-137">Availability and status of the device.</span></span>

<span data-ttu-id="d4236-138">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-138">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d4236-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d4236-139"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4236-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d4236-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d4236-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d4236-141"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-142">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="d4236-142">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d4236-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="d4236-143"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d4236-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="d4236-144"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d4236-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="d4236-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d4236-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="d4236-146"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d4236-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="d4236-147"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d4236-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="d4236-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d4236-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="d4236-149"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d4236-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="d4236-150"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d4236-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="d4236-151"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d4236-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="d4236-152"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-153">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="d4236-153">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d4236-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="d4236-154"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-155">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="d4236-155">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d4236-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="d4236-156"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-157">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="d4236-157">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d4236-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="d4236-158"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d4236-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="d4236-159"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-160">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="d4236-160">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d4236-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d4236-161"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-162">En pausa.</span><span class="sxs-lookup"><span data-stu-id="d4236-162">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d4236-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="d4236-163"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-164">No está listo.</span><span class="sxs-lookup"><span data-stu-id="d4236-164">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d4236-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="d4236-165"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-166">No configurado.</span><span class="sxs-lookup"><span data-stu-id="d4236-166">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d4236-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d4236-167"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-168">El sensor actual no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d4236-168">Current sensor is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d4236-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d4236-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-172">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d4236-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-173">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="d4236-173">Short description of the object a one-line string.</span></span>

<span data-ttu-id="d4236-174">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-175">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d4236-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-176">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4236-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-178">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d4236-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-179">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="d4236-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d4236-180">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d4236-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d4236-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d4236-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="d4236-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-183">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4236-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d4236-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="d4236-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d4236-185">(1)</span><span class="sxs-lookup"><span data-stu-id="d4236-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-186">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4236-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d4236-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d4236-188">(2)</span><span class="sxs-lookup"><span data-stu-id="d4236-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d4236-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="d4236-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d4236-190">(3)</span><span class="sxs-lookup"><span data-stu-id="d4236-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-191">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="d4236-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d4236-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="d4236-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d4236-193">(4)</span><span class="sxs-lookup"><span data-stu-id="d4236-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-194">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4236-194">Device is not working properly.</span></span> <span data-ttu-id="d4236-195">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="d4236-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d4236-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="d4236-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d4236-197">(5)</span><span class="sxs-lookup"><span data-stu-id="d4236-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-198">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="d4236-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d4236-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="d4236-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d4236-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="d4236-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-201">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d4236-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d4236-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="d4236-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d4236-203">(7)</span><span class="sxs-lookup"><span data-stu-id="d4236-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d4236-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d4236-205">(8)</span><span class="sxs-lookup"><span data-stu-id="d4236-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-206">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d4236-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="d4236-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d4236-208">(9)</span><span class="sxs-lookup"><span data-stu-id="d4236-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-209">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4236-209">Device is not working properly.</span></span> <span data-ttu-id="d4236-210">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d4236-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="d4236-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d4236-212">(10)</span><span class="sxs-lookup"><span data-stu-id="d4236-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-213">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="d4236-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d4236-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d4236-215">(11)</span><span class="sxs-lookup"><span data-stu-id="d4236-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-216">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d4236-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="d4236-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d4236-218">(12)</span><span class="sxs-lookup"><span data-stu-id="d4236-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-219">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="d4236-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d4236-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d4236-221">(13)</span><span class="sxs-lookup"><span data-stu-id="d4236-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-222">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d4236-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d4236-224">(14)</span><span class="sxs-lookup"><span data-stu-id="d4236-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-225">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="d4236-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d4236-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="d4236-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d4236-227">(15)</span><span class="sxs-lookup"><span data-stu-id="d4236-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-228">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="d4236-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d4236-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d4236-230">(16)</span><span class="sxs-lookup"><span data-stu-id="d4236-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-231">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d4236-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="d4236-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d4236-233">(17)</span><span class="sxs-lookup"><span data-stu-id="d4236-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-234">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="d4236-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d4236-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d4236-236">(18)</span><span class="sxs-lookup"><span data-stu-id="d4236-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-237">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d4236-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d4236-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="d4236-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d4236-239">(19)</span><span class="sxs-lookup"><span data-stu-id="d4236-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d4236-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="d4236-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d4236-241">(20)</span><span class="sxs-lookup"><span data-stu-id="d4236-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-242">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="d4236-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d4236-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d4236-244">(21)</span><span class="sxs-lookup"><span data-stu-id="d4236-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-245">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d4236-245">System failure.</span></span> <span data-ttu-id="d4236-246">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d4236-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d4236-247">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d4236-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="d4236-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d4236-249">(22)</span><span class="sxs-lookup"><span data-stu-id="d4236-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-250">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d4236-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d4236-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="d4236-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d4236-252">(23)</span><span class="sxs-lookup"><span data-stu-id="d4236-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-253">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="d4236-253">System failure.</span></span> <span data-ttu-id="d4236-254">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="d4236-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d4236-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="d4236-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d4236-256">(24)</span><span class="sxs-lookup"><span data-stu-id="d4236-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-257">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="d4236-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d4236-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d4236-259">(25)</span><span class="sxs-lookup"><span data-stu-id="d4236-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-260">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d4236-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d4236-262">(26)</span><span class="sxs-lookup"><span data-stu-id="d4236-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-263">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d4236-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d4236-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="d4236-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d4236-265">(27)</span><span class="sxs-lookup"><span data-stu-id="d4236-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-266">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="d4236-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d4236-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="d4236-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d4236-268">(28)</span><span class="sxs-lookup"><span data-stu-id="d4236-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-269">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="d4236-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d4236-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="d4236-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d4236-271">(29)</span><span class="sxs-lookup"><span data-stu-id="d4236-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-272">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d4236-272">Device is disabled.</span></span> <span data-ttu-id="d4236-273">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d4236-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d4236-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="d4236-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d4236-275">(30)</span><span class="sxs-lookup"><span data-stu-id="d4236-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-276">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="d4236-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d4236-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d4236-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d4236-278">31</span><span class="sxs-lookup"><span data-stu-id="d4236-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-279">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4236-279">Device is not working properly.</span></span> <span data-ttu-id="d4236-280">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d4236-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d4236-281">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d4236-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-282">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d4236-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-284">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d4236-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-285">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="d4236-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d4236-286">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d4236-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-290">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d4236-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d4236-291">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="d4236-291">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d4236-292">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="d4236-292">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d4236-293">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-294">**CurrentReading**</span><span class="sxs-lookup"><span data-stu-id="d4236-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-295">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-295">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-297">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,5 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-297">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-298">Valor actual indicado por el sensor.</span><span class="sxs-lookup"><span data-stu-id="d4236-298">Current value indicated by the sensor.</span></span>

<span data-ttu-id="d4236-299">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-299">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-300">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d4236-300">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-303">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="d4236-303">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-304">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d4236-304">Description of the object.</span></span>

<span data-ttu-id="d4236-305">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-305">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-306">**ID**</span><span class="sxs-lookup"><span data-stu-id="d4236-306">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-309">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d4236-309">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-310">Identificador único del sondeo actual.</span><span class="sxs-lookup"><span data-stu-id="d4236-310">Unique identifier of the current probe.</span></span>

<span data-ttu-id="d4236-311">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-312">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d4236-312">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-313">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d4236-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4236-315">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="d4236-315">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d4236-316">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-316">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-317">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d4236-317">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-318">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4236-320">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="d4236-320">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="d4236-321">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d4236-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-323">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d4236-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-325">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="d4236-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-326">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="d4236-326">Date and time the object was installed.</span></span> <span data-ttu-id="d4236-327">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="d4236-327">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d4236-328">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-329">**IsLinear**</span><span class="sxs-lookup"><span data-stu-id="d4236-329">**IsLinear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-330">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d4236-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4236-332">Si es **true**, el sensor es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d4236-332">If **TRUE**, the sensor is linear over its dynamic range.</span></span>

<span data-ttu-id="d4236-333">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-333">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d4236-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-335">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4236-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4236-337">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d4236-337">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d4236-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-339">**LowerThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="d4236-339">**LowerThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-340">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-340">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-342">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,13 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-342">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.13"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-343">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d4236-343">Sensor threshold values specify the ranges (minimum and maximum values) to determine whether or not the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d4236-344">Si **CurrentReading** está entre **LowerThresholdCritical** y **LowerThresholdFatal**, el estado actual es crítico.</span><span class="sxs-lookup"><span data-stu-id="d4236-344">If **CurrentReading** is between **LowerThresholdCritical** and **LowerThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="d4236-345">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-345">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-346">**LowerThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="d4236-346">**LowerThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-347">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-347">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-348">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-349">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-350">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d4236-350">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d4236-351">Si **CurrentReading** está por debajo de **LowerThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="d4236-351">If **CurrentReading** is below **LowerThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="d4236-352">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-352">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-353">**LowerThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="d4236-353">**LowerThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-354">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-354">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-356">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-357">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d4236-357">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d4236-358">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="d4236-358">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="d4236-359">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **LowerThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="d4236-359">If **CurrentReading** is between **LowerThresholdNonCritical** and **LowerThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="d4236-360">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-360">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-361">**MaxReadable**</span><span class="sxs-lookup"><span data-stu-id="d4236-361">**MaxReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-362">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-362">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-364">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-365">Valor mayor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d4236-365">Largest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="d4236-366">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-366">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-367">**MinReadable**</span><span class="sxs-lookup"><span data-stu-id="d4236-367">**MinReadable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-368">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-368">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-370">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,10 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-371">Valor menor de la propiedad medida que puede ser leída por el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d4236-371">Smallest value of the measured property that can be read by the numeric sensor.</span></span>

<span data-ttu-id="d4236-372">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-372">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-373">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d4236-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-376">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d4236-376">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-377">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="d4236-377">Label by which the object is known.</span></span> <span data-ttu-id="d4236-378">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="d4236-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d4236-379">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-380">**NominalReading**</span><span class="sxs-lookup"><span data-stu-id="d4236-380">**NominalReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-381">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-381">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-383">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-384">Valor normal o esperado para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d4236-384">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="d4236-385">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-385">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-386">**NormalMax**</span><span class="sxs-lookup"><span data-stu-id="d4236-386">**NormalMax**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-387">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-387">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-389">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-390">Valor normal o esperado para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d4236-390">Normal or expected value for the numeric sensor.</span></span>

<span data-ttu-id="d4236-391">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-391">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-392">**NormalMin**</span><span class="sxs-lookup"><span data-stu-id="d4236-392">**NormalMin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-393">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-393">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-395">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-396">Instrucciones para el usuario sobre el intervalo mínimo normal para el sensor numérico.</span><span class="sxs-lookup"><span data-stu-id="d4236-396">Guidance for the user as to the normal minimum range for the numeric sensor.</span></span>

<span data-ttu-id="d4236-397">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-397">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-398">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d4236-398">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-399">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-401">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d4236-401">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-402">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d4236-402">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d4236-403">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d4236-404">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d4236-404">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="d4236-405">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d4236-405">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-406">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4236-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d4236-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4236-408">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d4236-408">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d4236-409">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="d4236-409">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4236-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d4236-410"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d4236-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d4236-411"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d4236-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="d4236-412"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d4236-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d4236-413"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-414">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d4236-414">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d4236-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d4236-415"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-416">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="d4236-416">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d4236-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="d4236-417"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-418">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d4236-418">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d4236-419">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="d4236-419">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d4236-420">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d4236-420">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d4236-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="d4236-421"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-422">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="d4236-422">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d4236-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="d4236-423"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d4236-424">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="d4236-424">Timed Power-On Supported</span></span>

<span data-ttu-id="d4236-425">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="d4236-425">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d4236-426">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d4236-426">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-427">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d4236-427">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4236-429">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="d4236-429">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="d4236-430">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="d4236-430">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d4236-431">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-432">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="d4236-432">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-433">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4236-433">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-435">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" décimas de miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("tenths of milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-436">Capacidad del sensor para resolver las diferencias en la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="d4236-436">Ability of the sensor to resolve differences in the measured property.</span></span> <span data-ttu-id="d4236-437">Este valor puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d4236-437">This value may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="d4236-438">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-438">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-439">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d4236-439">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-440">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-441">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-442">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d4236-442">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-443">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="d4236-443">Current status of the object.</span></span> <span data-ttu-id="d4236-444">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="d4236-444">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d4236-445">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="d4236-445">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d4236-446">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="d4236-446">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d4236-447">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="d4236-447">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d4236-448">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="d4236-448">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d4236-449">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-449">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d4236-450">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d4236-450">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d4236-451">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="d4236-451">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d4236-452">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="d4236-452">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d4236-453">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d4236-453">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4236-454">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="d4236-454">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d4236-455">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="d4236-455">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d4236-456">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="d4236-456">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d4236-457">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="d4236-457">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d4236-458">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="d4236-458">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d4236-459">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="d4236-459">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d4236-460">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d4236-460">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d4236-461">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="d4236-461">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d4236-462">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="d4236-462">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d4236-463">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d4236-463">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-464">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4236-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-466">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d4236-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-467">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d4236-467">State of the logical device.</span></span> <span data-ttu-id="d4236-468">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="d4236-468">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d4236-469">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d4236-470">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="d4236-470">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4236-471">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="d4236-471">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d4236-472">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="d4236-472">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d4236-473">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="d4236-473">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d4236-474">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="d4236-474">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d4236-475">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d4236-475">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-476">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-478">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d4236-478">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d4236-479">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d4236-479">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d4236-480">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-481">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d4236-481">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-482">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d4236-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-483">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-483">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-484">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d4236-484">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d4236-485">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="d4236-485">Name of the scoping system.</span></span>

<span data-ttu-id="d4236-486">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-486">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-487">**Tolerancia**</span><span class="sxs-lookup"><span data-stu-id="d4236-487">**Tolerance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-488">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-488">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-489">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-490">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,18 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-490">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.18"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-491">Tolerancia del sensor para la propiedad medida.</span><span class="sxs-lookup"><span data-stu-id="d4236-491">Tolerance of the sensor for the measured property.</span></span> <span data-ttu-id="d4236-492">La tolerancia, junto con la resolución y la precisión, se usa para calcular el valor real de la propiedad física medida.</span><span class="sxs-lookup"><span data-stu-id="d4236-492">Tolerance, along with resolution and accuracy, is used to calculate the actual value of the measured physical property.</span></span> <span data-ttu-id="d4236-493">La tolerancia puede variar en función de si el dispositivo es lineal sobre su intervalo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d4236-493">Tolerance may vary depending on whether the device is linear over its dynamic range.</span></span>

<span data-ttu-id="d4236-494">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-494">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-495">**UpperThresholdCritical**</span><span class="sxs-lookup"><span data-stu-id="d4236-495">**UpperThresholdCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-496">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-496">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-497">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-498">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,14 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-499">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d4236-499">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d4236-500">Si **CurrentReading** está entre **UpperThresholdCritical** y **UpperThresholdFatal**, el estado actual es crítico.</span><span class="sxs-lookup"><span data-stu-id="d4236-500">If **CurrentReading** is between **UpperThresholdCritical** and **UpperThresholdFatal**, the current state is critical.</span></span>

<span data-ttu-id="d4236-501">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-501">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-502">**UpperThresholdFatal**</span><span class="sxs-lookup"><span data-stu-id="d4236-502">**UpperThresholdFatal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-503">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-503">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-504">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-505">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-506">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d4236-506">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d4236-507">Si **CurrentReading** está por encima de **UpperThresholdFatal**, el estado actual es fatal.</span><span class="sxs-lookup"><span data-stu-id="d4236-507">If **CurrentReading** is above **UpperThresholdFatal**, the current state is fatal.</span></span>

<span data-ttu-id="d4236-508">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-508">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4236-509">**UpperThresholdNonCritical**</span><span class="sxs-lookup"><span data-stu-id="d4236-509">**UpperThresholdNonCritical**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4236-510">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d4236-510">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4236-511">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d4236-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4236-512">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sondeo actual eléctrico DMTF \| 001,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliamperios ")</span><span class="sxs-lookup"><span data-stu-id="d4236-512">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Electrical Current Probe\|001.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliamps")</span></span>
</dt> </dl>

<span data-ttu-id="d4236-513">Los valores de umbral del sensor especifican los intervalos (valores mínimo y máximo) para determinar si el sensor está funcionando en condiciones normales, no críticas, críticas o graves.</span><span class="sxs-lookup"><span data-stu-id="d4236-513">Sensor's threshold values specify the ranges (minimum and maximum values) for determining whether the sensor is operating under normal, noncritical, critical, or fatal conditions.</span></span> <span data-ttu-id="d4236-514">Si **CurrentReading** está entre **LowerThresholdNonCritical** y **UpperThresholdNonCritical**, el sensor informa de un valor normal.</span><span class="sxs-lookup"><span data-stu-id="d4236-514">If **CurrentReading** is between **LowerThresholdNonCritical** and **UpperThresholdNonCritical**, the sensor is reporting a normal value.</span></span> <span data-ttu-id="d4236-515">Si **CurrentReading** está entre **UpperThresholdNonCritical** y **UpperThresholdCritical**, el estado actual es no crítico.</span><span class="sxs-lookup"><span data-stu-id="d4236-515">If **CurrentReading** is between **UpperThresholdNonCritical** and **UpperThresholdCritical**, the current state is noncritical.</span></span>

<span data-ttu-id="d4236-516">Esta propiedad se hereda de [**CIM \_ NumericSensor**](cim-numericsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-516">This property is inherited from [**CIM\_NumericSensor**](cim-numericsensor.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4236-517">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4236-517">Remarks</span></span>

<span data-ttu-id="d4236-518">La **clase \_ CurrentProbe de Win32** se deriva de [**\_ CurrentSensor de CIM**](cim-currentsensor.md).</span><span class="sxs-lookup"><span data-stu-id="d4236-518">The **Win32\_CurrentProbe** class is derived from [**CIM\_CurrentSensor**](cim-currentsensor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4236-519">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4236-519">Requirements</span></span>



| <span data-ttu-id="d4236-520">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4236-520">Requirement</span></span> | <span data-ttu-id="d4236-521">Value</span><span class="sxs-lookup"><span data-stu-id="d4236-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4236-522">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4236-522">Minimum supported client</span></span><br/> | <span data-ttu-id="d4236-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4236-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d4236-524">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4236-524">Minimum supported server</span></span><br/> | <span data-ttu-id="d4236-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4236-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d4236-526">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d4236-526">Namespace</span></span><br/>                | <span data-ttu-id="d4236-527">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d4236-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d4236-528">MOF</span><span class="sxs-lookup"><span data-stu-id="d4236-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4236-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4236-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4236-530">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4236-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4236-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4236-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4236-532">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4236-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4236-533">**\_CURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="d4236-533">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dt>

[<span data-ttu-id="d4236-534">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d4236-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

