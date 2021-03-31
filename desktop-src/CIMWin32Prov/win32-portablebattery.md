---
description: La \_ clase WMI PortableBattery de Win32 contiene las propiedades relacionadas con una batería portátil, como una batería de equipo portátil.
ms.assetid: ca7d061f-8fc6-4a1e-aa75-2465ce5e2735
ms.tgt_platform: multiple
title: Win32_PortableBattery (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortableBattery
- Win32_PortableBattery.Reset
- Win32_PortableBattery.SetPowerState
- Win32_PortableBattery.Availability
- Win32_PortableBattery.BatteryStatus
- Win32_PortableBattery.CapacityMultiplier
- Win32_PortableBattery.Caption
- Win32_PortableBattery.Chemistry
- Win32_PortableBattery.ConfigManagerErrorCode
- Win32_PortableBattery.ConfigManagerUserConfig
- Win32_PortableBattery.CreationClassName
- Win32_PortableBattery.Description
- Win32_PortableBattery.DesignCapacity
- Win32_PortableBattery.DesignVoltage
- Win32_PortableBattery.DeviceID
- Win32_PortableBattery.ErrorCleared
- Win32_PortableBattery.ErrorDescription
- Win32_PortableBattery.EstimatedChargeRemaining
- Win32_PortableBattery.EstimatedRunTime
- Win32_PortableBattery.ExpectedBatteryLife
- Win32_PortableBattery.ExpectedLife
- Win32_PortableBattery.FullChargeCapacity
- Win32_PortableBattery.InstallDate
- Win32_PortableBattery.LastErrorCode
- Win32_PortableBattery.Location
- Win32_PortableBattery.ManufactureDate
- Win32_PortableBattery.Manufacturer
- Win32_PortableBattery.MaxBatteryError
- Win32_PortableBattery.MaxRechargeTime
- Win32_PortableBattery.Name
- Win32_PortableBattery.PNPDeviceID
- Win32_PortableBattery.PowerManagementCapabilities
- Win32_PortableBattery.PowerManagementSupported
- Win32_PortableBattery.SmartBatteryVersion
- Win32_PortableBattery.Status
- Win32_PortableBattery.StatusInfo
- Win32_PortableBattery.SystemCreationClassName
- Win32_PortableBattery.SystemName
- Win32_PortableBattery.TimeOnBattery
- Win32_PortableBattery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9db875e7e4d1736cf45945b53f2f20fec0490a47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807082"
---
# <a name="win32_portablebattery-class"></a><span data-ttu-id="7905c-103">\_Clase Win32 PortableBattery</span><span class="sxs-lookup"><span data-stu-id="7905c-103">Win32\_PortableBattery class</span></span>

<span data-ttu-id="7905c-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PortableBattery de Win32** contiene las propiedades relacionadas con una batería portátil, como una batería de equipo portátil.</span><span class="sxs-lookup"><span data-stu-id="7905c-104">The **Win32\_PortableBattery** [WMI class](../wmisdk/retrieving-a-class.md) contains the properties related to a portable battery, such as a notebook computer battery.</span></span>

<span data-ttu-id="7905c-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7905c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7905c-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7905c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7905c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7905c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortableBattery : CIM_Battery
{
  uint16   Availability;
  uint16   BatteryStatus;
  uint16   CapacityMultiplier;
  string   Caption;
  uint16   Chemistry;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedBatteryLife;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Location;
  string   ManufactureDate;
  string   Manufacturer;
  uint16   MaxBatteryError;
  uint32   MaxRechargeTime;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   SmartBatteryVersion;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="7905c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7905c-108">Members</span></span>

<span data-ttu-id="7905c-109">La **clase \_ PortableBattery de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7905c-109">The **Win32\_PortableBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="7905c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7905c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7905c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7905c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7905c-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="7905c-112">Methods</span></span>

<span data-ttu-id="7905c-113">La clase **Win32 \_ PortableBattery** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7905c-113">The **Win32\_PortableBattery** class has these methods.</span></span>



| <span data-ttu-id="7905c-114">Método</span><span class="sxs-lookup"><span data-stu-id="7905c-114">Method</span></span>            | <span data-ttu-id="7905c-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7905c-115">Description</span></span>                                                                                                                                                                        |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7905c-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="7905c-116">**Reset**</span></span>         | <span data-ttu-id="7905c-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="7905c-117">Not implemented.</span></span> <span data-ttu-id="7905c-118">Para implementar este método, consulte el método de [**restablecimiento**](reset-method-in-class-cim-controller.md) de la [**\_ batería de CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/>                 |
| <span data-ttu-id="7905c-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7905c-119">**SetPowerState**</span></span> | <span data-ttu-id="7905c-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="7905c-120">Not implemented.</span></span> <span data-ttu-id="7905c-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**la \_ batería de CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7905c-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7905c-122">Properties</span></span>

<span data-ttu-id="7905c-123">La **clase \_ PortableBattery de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7905c-123">The **Win32\_PortableBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7905c-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="7905c-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7905c-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-127">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="7905c-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-128">Availability and status of the device.</span></span>

<span data-ttu-id="7905c-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7905c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7905c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7905c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7905c-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7905c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="7905c-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="7905c-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7905c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="7905c-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7905c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="7905c-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7905c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="7905c-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7905c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="7905c-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7905c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="7905c-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7905c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="7905c-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7905c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="7905c-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7905c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="7905c-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7905c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="7905c-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7905c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="7905c-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="7905c-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7905c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="7905c-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="7905c-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7905c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="7905c-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="7905c-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7905c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="7905c-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7905c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="7905c-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="7905c-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7905c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="7905c-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="7905c-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7905c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="7905c-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="7905c-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7905c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="7905c-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="7905c-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7905c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="7905c-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="7905c-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7905c-160">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="7905c-160">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7905c-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-163">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batería portátil DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="7905c-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-164">Descripción del estado de los cargos de la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-164">Description of the battery's charge status.</span></span> <span data-ttu-id="7905c-165">El valor 10 (sin definir) no es válido en el esquema de Modelo de información común (CIM) porque en la interfaz de administración de escritorio (DMI) indica que no hay ninguna batería instalada.</span><span class="sxs-lookup"><span data-stu-id="7905c-165">The value 10 (Undefined) is not valid in the Common Information Model (CIM) schema because in Desktop Management Interface (DMI) it indicates that no battery is installed.</span></span> <span data-ttu-id="7905c-166">En este caso, no se debe crear una instancia de este objeto.</span><span class="sxs-lookup"><span data-stu-id="7905c-166">In this case, this object should not be instantiated.</span></span>

<span data-ttu-id="7905c-167">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-167">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7905c-168">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7905c-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7905c-169">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7905c-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="7905c-170">Con **cargos completos** (3)</span><span class="sxs-lookup"><span data-stu-id="7905c-170">**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="7905c-171">**Bajo** (4)</span><span class="sxs-lookup"><span data-stu-id="7905c-171">**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="7905c-172">**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="7905c-172">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="7905c-173">**Carga** (6)</span><span class="sxs-lookup"><span data-stu-id="7905c-173">**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="7905c-174">**Cargando y alto** (7)</span><span class="sxs-lookup"><span data-stu-id="7905c-174">**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="7905c-175">**Cargando y bajo** (8)</span><span class="sxs-lookup"><span data-stu-id="7905c-175">**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="7905c-176">**Carga y crítico** (9)</span><span class="sxs-lookup"><span data-stu-id="7905c-176">**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="7905c-177">**Sin definir** (10)</span><span class="sxs-lookup"><span data-stu-id="7905c-177">**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="7905c-178">**Cargado parcialmente** (11)</span><span class="sxs-lookup"><span data-stu-id="7905c-178">**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7905c-179">**CapacityMultiplier**</span><span class="sxs-lookup"><span data-stu-id="7905c-179">**CapacityMultiplier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-180">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7905c-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-182">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("multiplicador de capacidad de diseño de tipo de SMBIOS \| 22 \| ")</span><span class="sxs-lookup"><span data-stu-id="7905c-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Design Capacity Multiplier")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-183">Factor de multiplicación del valor de **designCapacity** para asegurarse de que el valor de hora de milivatios no se desborda en las implementaciones de especificación de datos de batería inteligente (SBDS).</span><span class="sxs-lookup"><span data-stu-id="7905c-183">Multiplication factor of the **DesignCapacity** value to ensure that the milliwatt hour value does not overflow for Smart Battery Data Specification (SBDS) implementations.</span></span>

</dd> <dt>

<span data-ttu-id="7905c-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7905c-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-187">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7905c-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-188">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="7905c-188">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="7905c-189">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-190">**Químicos**</span><span class="sxs-lookup"><span data-stu-id="7905c-190">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-191">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7905c-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-193">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batería portátil DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="7905c-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-194">Química de la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-194">Chemistry of the battery.</span></span>

<span data-ttu-id="7905c-195">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-195">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7905c-196">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7905c-196">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7905c-197">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7905c-197">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="7905c-198">**Acid inicial** (3)</span><span class="sxs-lookup"><span data-stu-id="7905c-198">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="7905c-199">**Níquel cadmio** (4)</span><span class="sxs-lookup"><span data-stu-id="7905c-199">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="7905c-200">**Hidruro de níquel metal** (5)</span><span class="sxs-lookup"><span data-stu-id="7905c-200">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="7905c-201">**Ion-** litio (6)</span><span class="sxs-lookup"><span data-stu-id="7905c-201">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="7905c-202">**Aire de zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="7905c-202">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="7905c-203">**Polímero de litio** (8)</span><span class="sxs-lookup"><span data-stu-id="7905c-203">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7905c-204">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7905c-204">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-205">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-207">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7905c-207">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-208">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="7905c-208">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7905c-209">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-209">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7905c-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="7905c-210"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7905c-211"> (0)</span><span class="sxs-lookup"><span data-stu-id="7905c-211">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-212">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7905c-212">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7905c-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="7905c-213"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7905c-214">(1)</span><span class="sxs-lookup"><span data-stu-id="7905c-214">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-215">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7905c-215">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7905c-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-216"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7905c-217">(2)</span><span class="sxs-lookup"><span data-stu-id="7905c-217">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7905c-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="7905c-218"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7905c-219">(3)</span><span class="sxs-lookup"><span data-stu-id="7905c-219">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-220">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="7905c-220">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7905c-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="7905c-221"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7905c-222">(4)</span><span class="sxs-lookup"><span data-stu-id="7905c-222">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-223">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7905c-223">Device is not working properly.</span></span> <span data-ttu-id="7905c-224">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="7905c-224">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7905c-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="7905c-225"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7905c-226">(5)</span><span class="sxs-lookup"><span data-stu-id="7905c-226">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-227">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="7905c-227">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7905c-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="7905c-228"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7905c-229"> (6)</span><span class="sxs-lookup"><span data-stu-id="7905c-229">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-230">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7905c-230">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7905c-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="7905c-231"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7905c-232">(7)</span><span class="sxs-lookup"><span data-stu-id="7905c-232">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7905c-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-233"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7905c-234">(8)</span><span class="sxs-lookup"><span data-stu-id="7905c-234">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-235">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-235">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7905c-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="7905c-236"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7905c-237">(9)</span><span class="sxs-lookup"><span data-stu-id="7905c-237">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-238">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7905c-238">Device is not working properly.</span></span> <span data-ttu-id="7905c-239">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-239">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7905c-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="7905c-240"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7905c-241">(10)</span><span class="sxs-lookup"><span data-stu-id="7905c-241">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-242">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="7905c-242">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7905c-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-243"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7905c-244">(11)</span><span class="sxs-lookup"><span data-stu-id="7905c-244">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-245">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-245">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7905c-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="7905c-246"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7905c-247">(12)</span><span class="sxs-lookup"><span data-stu-id="7905c-247">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-248">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="7905c-248">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7905c-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-249"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7905c-250">(13)</span><span class="sxs-lookup"><span data-stu-id="7905c-250">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-251">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-251">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7905c-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-252"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7905c-253">(14)</span><span class="sxs-lookup"><span data-stu-id="7905c-253">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-254">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="7905c-254">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7905c-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="7905c-255"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7905c-256">(15)</span><span class="sxs-lookup"><span data-stu-id="7905c-256">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-257">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="7905c-257">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7905c-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-258"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7905c-259">(16)</span><span class="sxs-lookup"><span data-stu-id="7905c-259">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-260">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-260">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7905c-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="7905c-261"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7905c-262">(17)</span><span class="sxs-lookup"><span data-stu-id="7905c-262">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-263">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="7905c-263">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7905c-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-264"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7905c-265">(18)</span><span class="sxs-lookup"><span data-stu-id="7905c-265">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-266">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7905c-266">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7905c-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="7905c-267"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7905c-268">(19)</span><span class="sxs-lookup"><span data-stu-id="7905c-268">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7905c-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="7905c-269"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7905c-270">(20)</span><span class="sxs-lookup"><span data-stu-id="7905c-270">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-271">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="7905c-271">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7905c-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7905c-273">(21)</span><span class="sxs-lookup"><span data-stu-id="7905c-273">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-274">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="7905c-274">System failure.</span></span> <span data-ttu-id="7905c-275">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="7905c-275">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7905c-276">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-276">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7905c-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="7905c-277"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7905c-278">(22)</span><span class="sxs-lookup"><span data-stu-id="7905c-278">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-279">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7905c-279">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7905c-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="7905c-280"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7905c-281">(23)</span><span class="sxs-lookup"><span data-stu-id="7905c-281">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-282">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="7905c-282">System failure.</span></span> <span data-ttu-id="7905c-283">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="7905c-283">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7905c-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="7905c-284"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7905c-285">(24)</span><span class="sxs-lookup"><span data-stu-id="7905c-285">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-286">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="7905c-286">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7905c-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-287"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7905c-288">(25)</span><span class="sxs-lookup"><span data-stu-id="7905c-288">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-289">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-289">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7905c-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-290"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7905c-291">(26)</span><span class="sxs-lookup"><span data-stu-id="7905c-291">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-292">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7905c-292">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7905c-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="7905c-293"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7905c-294">(27)</span><span class="sxs-lookup"><span data-stu-id="7905c-294">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-295">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="7905c-295">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7905c-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="7905c-296"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7905c-297">(28)</span><span class="sxs-lookup"><span data-stu-id="7905c-297">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-298">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="7905c-298">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7905c-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="7905c-299"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7905c-300">(29)</span><span class="sxs-lookup"><span data-stu-id="7905c-300">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-301">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7905c-301">Device is disabled.</span></span> <span data-ttu-id="7905c-302">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7905c-302">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7905c-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="7905c-303"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7905c-304">(30)</span><span class="sxs-lookup"><span data-stu-id="7905c-304">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-305">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="7905c-305">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7905c-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7905c-306"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7905c-307">31</span><span class="sxs-lookup"><span data-stu-id="7905c-307">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-308">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7905c-308">Device is not working properly.</span></span> <span data-ttu-id="7905c-309">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7905c-309">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7905c-310">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7905c-310">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-311">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7905c-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-313">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7905c-313">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-314">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7905c-314">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7905c-315">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-316">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7905c-316">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-319">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7905c-319">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7905c-320">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="7905c-320">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7905c-321">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="7905c-321">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7905c-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-323">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7905c-323">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-326">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7905c-326">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-327">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7905c-327">Description of the object.</span></span>

<span data-ttu-id="7905c-328">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-329">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="7905c-329">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-330">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-332">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batería portátil \| de DMTF 002,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivatios-horas ")</span><span class="sxs-lookup"><span data-stu-id="7905c-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-333">Diseño de la capacidad de la batería en milivatios-horas.</span><span class="sxs-lookup"><span data-stu-id="7905c-333">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="7905c-334">Si no se admite esta propiedad, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7905c-334">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="7905c-335">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-335">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-336">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="7905c-336">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-337">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7905c-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-339">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Unidad DMTF portátil \| 002,9 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="7905c-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](../wmisdk/standard-qualifiers.md) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-340">Tensión de diseño de la batería en milivoltios.</span><span class="sxs-lookup"><span data-stu-id="7905c-340">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="7905c-341">Si no se admite este atributo, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7905c-341">If this attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="7905c-342">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-342">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="7905c-343">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-344">**ID**</span><span class="sxs-lookup"><span data-stu-id="7905c-344">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-345">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-347">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7905c-347">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-348">Identificador de la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-348">Battery identifier.</span></span>

<span data-ttu-id="7905c-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7905c-350">Ejemplo: "batería interna"</span><span class="sxs-lookup"><span data-stu-id="7905c-350">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="7905c-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7905c-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-352">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7905c-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7905c-354">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="7905c-354">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="7905c-355">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7905c-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-357">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7905c-359">Más información sobre el error registrado en **LastErrorCode** y las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="7905c-359">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="7905c-360">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-361">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="7905c-361">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-362">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7905c-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-364">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("porcentaje")</span><span class="sxs-lookup"><span data-stu-id="7905c-364">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-365">Estimación del porcentaje de carga completa restante.</span><span class="sxs-lookup"><span data-stu-id="7905c-365">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="7905c-366">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-366">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-367">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="7905c-367">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-368">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-370">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batería portátil DMTF \| 002,15 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="7905c-370">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-371">Estime en minutos el agotamiento del tiempo de la carga de la batería en las condiciones actuales de carga si la utilidad de energía está apagada, perdida y permanece apagada, o si un equipo portátil está desconectado de una fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="7905c-371">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="7905c-372">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-372">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-373">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="7905c-373">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-374">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7905c-376">No se admite.</span><span class="sxs-lookup"><span data-stu-id="7905c-376">Not supported.</span></span>

<span data-ttu-id="7905c-377">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-378">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="7905c-378">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-379">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-381">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="7905c-381">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-382">La duración esperada de la batería en minutos, suponiendo que la batería está totalmente cargada.</span><span class="sxs-lookup"><span data-stu-id="7905c-382">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="7905c-383">Esta propiedad representa la vida total esperada de la batería, no su vida restante actual, que se indica mediante la propiedad **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="7905c-383">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="7905c-384">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-384">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-385">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="7905c-385">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-386">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-388">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batería portátil \| de DMTF 002,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" milivatios-horas ")</span><span class="sxs-lookup"><span data-stu-id="7905c-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-389">Capacidad de carga completa de la batería en milivatios-horas.</span><span class="sxs-lookup"><span data-stu-id="7905c-389">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="7905c-390">La comparación de este valor con la propiedad **designCapacity** determina cuándo es necesario reemplazar la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-390">Comparison of this value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="7905c-391">El final de la vida de una batería suele ser cuando la propiedad **FullChargeCapacity** cae por debajo del 80% de la propiedad **designCapacity** .</span><span class="sxs-lookup"><span data-stu-id="7905c-391">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="7905c-392">Si no se admite esta propiedad, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7905c-392">If this property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="7905c-393">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-393">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-394">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7905c-394">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-395">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7905c-395">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-397">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7905c-397">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-398">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7905c-398">Date and time the object was installed.</span></span> <span data-ttu-id="7905c-399">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="7905c-399">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7905c-400">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-400">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-401">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7905c-401">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-402">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7905c-404">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7905c-404">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7905c-405">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-406">**Ubicación**</span><span class="sxs-lookup"><span data-stu-id="7905c-406">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-407">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-409">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 22 \| Location")</span><span class="sxs-lookup"><span data-stu-id="7905c-409">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-410">Ubicación física de la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-410">Physical location of the battery.</span></span> <span data-ttu-id="7905c-411">Esta propiedad la rellena el fabricante del equipo.</span><span class="sxs-lookup"><span data-stu-id="7905c-411">This property is filled by the computer manufacturer.</span></span>

<span data-ttu-id="7905c-412">Ejemplo: "en el fondo, a la izquierda"</span><span class="sxs-lookup"><span data-stu-id="7905c-412">Example: "In the back, on the left"</span></span>

</dd> <dt>

<span data-ttu-id="7905c-413">**ManufactureDate**</span><span class="sxs-lookup"><span data-stu-id="7905c-413">**ManufactureDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-414">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-416">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 22 \| fecha de fabricación")</span><span class="sxs-lookup"><span data-stu-id="7905c-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacture Date")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-417">Fecha en la que se fabricó la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-417">Date when the battery was manufactured.</span></span>

</dd> <dt>

<span data-ttu-id="7905c-418">**Le**</span><span class="sxs-lookup"><span data-stu-id="7905c-418">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-419">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-421">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| fabricante de tipo 22 de SMBIOS \| ")</span><span class="sxs-lookup"><span data-stu-id="7905c-421">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-422">Fabricante de la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-422">Manufacturer of the battery.</span></span>

</dd> <dt>

<span data-ttu-id="7905c-423">**MaxBatteryError**</span><span class="sxs-lookup"><span data-stu-id="7905c-423">**MaxBatteryError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-424">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7905c-424">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-426">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("el \| tipo de SMBIOS 22 \| error máximo en los datos de la batería"), [**unidades**](../wmisdk/standard-qualifiers.md) ("porcentaje")</span><span class="sxs-lookup"><span data-stu-id="7905c-426">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 22\|Maximum Error in Battery Data"), [**Units**](../wmisdk/standard-qualifiers.md) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-427">Diferencia entre la mayor cantidad de energía estimada que se ha dejado en la batería y la cantidad actual indicada por la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-427">Difference between the highest estimated amount of energy left in the battery and the current amount reported by the battery.</span></span>

</dd> <dt>

<span data-ttu-id="7905c-428">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="7905c-428">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-429">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-431">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="7905c-431">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-432">Tiempo máximo, en minutos, para cargar por completo la batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-432">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="7905c-433">Esta propiedad representa el tiempo para recargar una batería totalmente agotada, no el tiempo de carga restante actual, que se indica en la propiedad **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="7905c-433">This property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="7905c-434">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-434">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-435">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7905c-435">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-438">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7905c-438">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-439">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="7905c-439">Label by which the object is known.</span></span> <span data-ttu-id="7905c-440">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="7905c-440">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="7905c-441">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-442">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7905c-442">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-443">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-445">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7905c-445">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-446">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7905c-446">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7905c-447">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7905c-448">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7905c-448">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7905c-449">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7905c-449">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-450">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7905c-450">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7905c-451">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7905c-452">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7905c-452">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7905c-453">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="7905c-453">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7905c-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7905c-454"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7905c-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="7905c-455"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7905c-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="7905c-456"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7905c-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7905c-457"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-458">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="7905c-458">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7905c-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="7905c-459"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-460">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="7905c-460">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7905c-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="7905c-461"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-462">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="7905c-462">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7905c-463">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="7905c-463">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7905c-464">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-464">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7905c-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="7905c-465"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-466">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="7905c-466">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7905c-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="7905c-467"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7905c-468">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="7905c-468">Timed Power-On Supported</span></span>

<span data-ttu-id="7905c-469">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="7905c-469">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7905c-470">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7905c-470">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-471">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7905c-471">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7905c-473">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="7905c-473">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="7905c-474">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="7905c-474">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="7905c-475">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-475">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-476">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="7905c-476">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-477">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-478">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-479">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batería portátil DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="7905c-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-480">Número de versión de especificación de datos de batería inteligente compatible con esta batería.</span><span class="sxs-lookup"><span data-stu-id="7905c-480">Smart Battery Data Specification version number supported by this battery.</span></span> <span data-ttu-id="7905c-481">Si la batería no admite esta función, el valor debe dejarse en blanco.</span><span class="sxs-lookup"><span data-stu-id="7905c-481">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="7905c-482">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-482">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-483">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7905c-483">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-484">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-485">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-486">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="7905c-486">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-487">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7905c-487">Current status of the object.</span></span> <span data-ttu-id="7905c-488">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="7905c-488">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7905c-489">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="7905c-489">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7905c-490">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7905c-490">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7905c-491">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7905c-491">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7905c-492">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7905c-492">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7905c-493">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-493">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7905c-494">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7905c-494">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7905c-495">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7905c-495">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7905c-496">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7905c-496">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7905c-497">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7905c-497">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7905c-498">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7905c-498">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7905c-499">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7905c-499">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7905c-500">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7905c-500">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7905c-501">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7905c-501">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7905c-502">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7905c-502">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7905c-503">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7905c-503">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7905c-504">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7905c-504">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7905c-505">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7905c-505">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7905c-506">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7905c-506">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7905c-507">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7905c-507">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-508">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7905c-508">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-509">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-510">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7905c-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-511">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7905c-511">State of the logical device.</span></span> <span data-ttu-id="7905c-512">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="7905c-512">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7905c-513">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-513">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7905c-514">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7905c-514">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7905c-515">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7905c-515">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7905c-516">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7905c-516">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7905c-517">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="7905c-517">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7905c-518">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="7905c-518">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7905c-519">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7905c-519">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-520">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-521">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-522">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7905c-522">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7905c-523">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7905c-523">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="7905c-524">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-525">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7905c-525">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-526">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7905c-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-527">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-528">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="7905c-528">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="7905c-529">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7905c-529">Name of the scoping system.</span></span>

<span data-ttu-id="7905c-530">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-530">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-531">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="7905c-531">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-532">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-532">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-533">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-533">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-534">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="7905c-534">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-535">Tiempo transcurrido en segundos desde la última vez que el sistema del equipo cambió a la energía de la batería o desde la última vez que se reinició el sistema o SAI, lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="7905c-535">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="7905c-536">Si la batería está en línea, se devuelve 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="7905c-536">If the battery is online, 0 (zero) is returned.</span></span>

<span data-ttu-id="7905c-537">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-537">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="7905c-538">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="7905c-538">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7905c-539">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7905c-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7905c-540">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7905c-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7905c-541">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Batería portátil DMTF \| 002,16 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="7905c-541">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="7905c-542">Tiempo restante en minutos para cargar la batería por completo a la tarifa de cargos actual y uso.</span><span class="sxs-lookup"><span data-stu-id="7905c-542">Remaining time in minutes to charge the battery fully at the current charge rate and usage.</span></span>

<span data-ttu-id="7905c-543">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-543">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7905c-544">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7905c-544">Remarks</span></span>

<span data-ttu-id="7905c-545">La clase **Win32 \_ PortableBattery** se deriva de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="7905c-545">The **Win32\_PortableBattery** class is derived from [**CIM\_Battery**](cim-battery.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7905c-546">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7905c-546">Requirements</span></span>



| <span data-ttu-id="7905c-547">Requisito</span><span class="sxs-lookup"><span data-stu-id="7905c-547">Requirement</span></span> | <span data-ttu-id="7905c-548">Value</span><span class="sxs-lookup"><span data-stu-id="7905c-548">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7905c-549">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7905c-549">Minimum supported client</span></span><br/> | <span data-ttu-id="7905c-550">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7905c-550">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7905c-551">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7905c-551">Minimum supported server</span></span><br/> | <span data-ttu-id="7905c-552">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7905c-552">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7905c-553">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7905c-553">Namespace</span></span><br/>                | <span data-ttu-id="7905c-554">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7905c-554">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7905c-555">MOF</span><span class="sxs-lookup"><span data-stu-id="7905c-555">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7905c-556"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7905c-556"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7905c-557">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7905c-557">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7905c-558"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7905c-558"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7905c-559">Vea también</span><span class="sxs-lookup"><span data-stu-id="7905c-559">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7905c-560">**\_Batería CIM**</span><span class="sxs-lookup"><span data-stu-id="7905c-560">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="7905c-561">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="7905c-561">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
