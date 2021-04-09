---
description: Representa una batería conectada al sistema del equipo.
ms.assetid: b07ccb1d-008e-4bf1-8299-33706cbcbaee
ms.tgt_platform: multiple
title: Win32_Battery (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Battery
- Win32_Battery.Reset
- Win32_Battery.SetPowerState
- Win32_Battery.Availability
- Win32_Battery.BatteryRechargeTime
- Win32_Battery.BatteryStatus
- Win32_Battery.Caption
- Win32_Battery.Chemistry
- Win32_Battery.ConfigManagerErrorCode
- Win32_Battery.ConfigManagerUserConfig
- Win32_Battery.CreationClassName
- Win32_Battery.Description
- Win32_Battery.DesignCapacity
- Win32_Battery.DesignVoltage
- Win32_Battery.DeviceID
- Win32_Battery.ErrorCleared
- Win32_Battery.ErrorDescription
- Win32_Battery.EstimatedChargeRemaining
- Win32_Battery.EstimatedRunTime
- Win32_Battery.ExpectedBatteryLife
- Win32_Battery.ExpectedLife
- Win32_Battery.FullChargeCapacity
- Win32_Battery.InstallDate
- Win32_Battery.LastErrorCode
- Win32_Battery.MaxRechargeTime
- Win32_Battery.Name
- Win32_Battery.PNPDeviceID
- Win32_Battery.PowerManagementCapabilities
- Win32_Battery.PowerManagementSupported
- Win32_Battery.SmartBatteryVersion
- Win32_Battery.Status
- Win32_Battery.StatusInfo
- Win32_Battery.SystemCreationClassName
- Win32_Battery.SystemName
- Win32_Battery.TimeOnBattery
- Win32_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 75477bcf670bcc0cf16c63f130f95d4c38d7b783
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080278"
---
# <a name="win32_battery-class"></a><span data-ttu-id="3a248-103">\_Clase de batería Win32</span><span class="sxs-lookup"><span data-stu-id="3a248-103">Win32\_Battery class</span></span>

<span data-ttu-id="3a248-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de la **\_ batería de Win32** representa una batería conectada al sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="3a248-104">The **Win32\_Battery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a battery connected to the computer system.</span></span>

<span data-ttu-id="3a248-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3a248-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3a248-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3a248-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a248-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a248-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Battery : CIM_Battery
{
  uint16   Availability;
  uint32   BatteryRechargeTime;
  uint16   BatteryStatus;
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

## <a name="members"></a><span data-ttu-id="3a248-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a248-108">Members</span></span>

<span data-ttu-id="3a248-109">La clase de **\_ batería Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3a248-109">The **Win32\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="3a248-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a248-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3a248-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a248-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3a248-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3a248-112">Methods</span></span>

<span data-ttu-id="3a248-113">La clase de **\_ batería Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3a248-113">The **Win32\_Battery** class has these methods.</span></span>



| <span data-ttu-id="3a248-114">Método</span><span class="sxs-lookup"><span data-stu-id="3a248-114">Method</span></span>            | <span data-ttu-id="3a248-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3a248-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a248-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="3a248-116">**Reset**</span></span>         | <span data-ttu-id="3a248-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="3a248-117">Not implemented.</span></span> <span data-ttu-id="3a248-118">Para implementar este método, consulte la documentación sobre el método de [**restablecimiento**](reset-method-in-class-cim-controller.md) de la [**\_ batería de CIM**](cim-battery.md) .</span><span class="sxs-lookup"><span data-stu-id="3a248-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="3a248-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3a248-119">**SetPowerState**</span></span> | <span data-ttu-id="3a248-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="3a248-120">Not implemented.</span></span> <span data-ttu-id="3a248-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**la \_ batería de CIM**](cim-battery.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="3a248-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Battery**](cim-battery.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3a248-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a248-122">Properties</span></span>

<span data-ttu-id="3a248-123">La clase de **\_ batería Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3a248-123">The **Win32\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a248-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="3a248-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a248-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-127">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="3a248-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-128">Availability and status of the device.</span></span>

<span data-ttu-id="3a248-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a248-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a248-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a248-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="3a248-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3a248-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="3a248-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="3a248-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3a248-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="3a248-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3a248-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="3a248-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3a248-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="3a248-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3a248-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="3a248-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3a248-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="3a248-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3a248-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="3a248-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3a248-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="3a248-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3a248-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="3a248-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3a248-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="3a248-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3a248-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="3a248-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="3a248-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3a248-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="3a248-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="3a248-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3a248-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="3a248-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="3a248-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3a248-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="3a248-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3a248-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="3a248-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="3a248-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3a248-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="3a248-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="3a248-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3a248-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="3a248-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="3a248-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3a248-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="3a248-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="3a248-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3a248-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="3a248-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="3a248-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a248-160">**BatteryRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="3a248-160">**BatteryRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-161">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-163">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| RechargeRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="3a248-163">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|RechargeRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-164">Tiempo necesario para cargar por completo la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-164">Time required to fully charge the battery.</span></span> <span data-ttu-id="3a248-165">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="3a248-165">This property is not supported.</span></span> <span data-ttu-id="3a248-166">**BatteryRechargeTime** no tiene una propiedad de reemplazo y ahora se considera obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3a248-166">**BatteryRechargeTime** does not have a replacement property, and is now considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="3a248-167">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="3a248-167">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a248-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-170">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="3a248-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-171">Estado de la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-171">Status of the battery.</span></span> <span data-ttu-id="3a248-172">El valor 10 (sin definir) no es válido en el esquema CIM porque, en DMI, indica que no hay ninguna batería instalada.</span><span class="sxs-lookup"><span data-stu-id="3a248-172">The value 10 (Undefined) is not valid in the CIM schema because in DMI it represents that no battery is installed.</span></span> <span data-ttu-id="3a248-173">En este caso, no se debe crear una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a248-173">In this case, the object should not be instantiated.</span></span>

<span data-ttu-id="3a248-174">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-174">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a248-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a248-175"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-176">La batería se está descargando.</span><span class="sxs-lookup"><span data-stu-id="3a248-176">The battery is discharging.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a248-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="3a248-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-178">El sistema tiene acceso a AC, por lo que no se está descargado la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-178">The system has access to AC so no battery is being discharged.</span></span> <span data-ttu-id="3a248-179">Sin embargo, la batería no se está cargando necesariamente.</span><span class="sxs-lookup"><span data-stu-id="3a248-179">However, the battery is not necessarily charging.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="3a248-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>Con **cargos completos** (3)</span><span class="sxs-lookup"><span data-stu-id="3a248-180"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="3a248-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bajo** (4)</span><span class="sxs-lookup"><span data-stu-id="3a248-181"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="3a248-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="3a248-182"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="3a248-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Carga** (6)</span><span class="sxs-lookup"><span data-stu-id="3a248-183"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="3a248-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Cargando y alto** (7)</span><span class="sxs-lookup"><span data-stu-id="3a248-184"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="3a248-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Cargando y bajo** (8)</span><span class="sxs-lookup"><span data-stu-id="3a248-185"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="3a248-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Carga y crítico** (9)</span><span class="sxs-lookup"><span data-stu-id="3a248-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="3a248-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Sin definir** (10)</span><span class="sxs-lookup"><span data-stu-id="3a248-187"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="3a248-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Cargado parcialmente** (11)</span><span class="sxs-lookup"><span data-stu-id="3a248-188"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a248-189">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3a248-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-192">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3a248-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-193">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="3a248-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="3a248-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-195">**Químicos**</span><span class="sxs-lookup"><span data-stu-id="3a248-195">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a248-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-198">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="3a248-198">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-199">Enumeración que describe la química de la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-199">Enumeration that describes the battery's chemistry.</span></span>

<span data-ttu-id="3a248-200">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-200">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a248-201">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a248-201">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a248-202">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="3a248-202">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="3a248-203">**Acid inicial** (3)</span><span class="sxs-lookup"><span data-stu-id="3a248-203">**Lead Acid** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="3a248-204">**Níquel cadmio** (4)</span><span class="sxs-lookup"><span data-stu-id="3a248-204">**Nickel Cadmium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="3a248-205">**Hidruro de níquel metal** (5)</span><span class="sxs-lookup"><span data-stu-id="3a248-205">**Nickel Metal Hydride** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="3a248-206">**Ion-** litio (6)</span><span class="sxs-lookup"><span data-stu-id="3a248-206">**Lithium-ion** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="3a248-207">**Aire de zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="3a248-207">**Zinc air** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="3a248-208">**Polímero de litio** (8)</span><span class="sxs-lookup"><span data-stu-id="3a248-208">**Lithium Polymer** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a248-209">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3a248-209">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-210">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-212">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3a248-212">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-213">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3a248-213">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="3a248-214">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-214">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3a248-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="3a248-215"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3a248-216"> (0)</span><span class="sxs-lookup"><span data-stu-id="3a248-216">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-217">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a248-217">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3a248-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="3a248-218"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3a248-219">(1)</span><span class="sxs-lookup"><span data-stu-id="3a248-219">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-220">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a248-220">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3a248-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-221"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3a248-222">(2)</span><span class="sxs-lookup"><span data-stu-id="3a248-222">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3a248-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="3a248-223"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3a248-224">(3)</span><span class="sxs-lookup"><span data-stu-id="3a248-224">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-225">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="3a248-225">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3a248-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="3a248-226"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3a248-227">(4)</span><span class="sxs-lookup"><span data-stu-id="3a248-227">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-228">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a248-228">Device is not working properly.</span></span> <span data-ttu-id="3a248-229">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="3a248-229">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3a248-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="3a248-230"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3a248-231">(5)</span><span class="sxs-lookup"><span data-stu-id="3a248-231">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-232">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="3a248-232">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3a248-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="3a248-233"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3a248-234"> (6)</span><span class="sxs-lookup"><span data-stu-id="3a248-234">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-235">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3a248-235">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3a248-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="3a248-236"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3a248-237">(7)</span><span class="sxs-lookup"><span data-stu-id="3a248-237">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3a248-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-238"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3a248-239">(8)</span><span class="sxs-lookup"><span data-stu-id="3a248-239">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-240">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-240">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3a248-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="3a248-241"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3a248-242">(9)</span><span class="sxs-lookup"><span data-stu-id="3a248-242">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-243">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a248-243">Device is not working properly.</span></span> <span data-ttu-id="3a248-244">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-244">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3a248-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="3a248-245"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3a248-246">(10)</span><span class="sxs-lookup"><span data-stu-id="3a248-246">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-247">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="3a248-247">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3a248-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-248"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3a248-249">(11)</span><span class="sxs-lookup"><span data-stu-id="3a248-249">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-250">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-250">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3a248-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="3a248-251"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3a248-252">(12)</span><span class="sxs-lookup"><span data-stu-id="3a248-252">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-253">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="3a248-253">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3a248-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-254"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3a248-255">(13)</span><span class="sxs-lookup"><span data-stu-id="3a248-255">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-256">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-256">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3a248-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-257"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3a248-258">(14)</span><span class="sxs-lookup"><span data-stu-id="3a248-258">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-259">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="3a248-259">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3a248-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="3a248-260"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3a248-261">(15)</span><span class="sxs-lookup"><span data-stu-id="3a248-261">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-262">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="3a248-262">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3a248-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-263"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3a248-264">(16)</span><span class="sxs-lookup"><span data-stu-id="3a248-264">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-265">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-265">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3a248-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="3a248-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3a248-267">(17)</span><span class="sxs-lookup"><span data-stu-id="3a248-267">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-268">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="3a248-268">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3a248-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-269"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3a248-270">(18)</span><span class="sxs-lookup"><span data-stu-id="3a248-270">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-271">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3a248-271">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3a248-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="3a248-272"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3a248-273">(19)</span><span class="sxs-lookup"><span data-stu-id="3a248-273">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3a248-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="3a248-274"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3a248-275">(20)</span><span class="sxs-lookup"><span data-stu-id="3a248-275">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-276">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="3a248-276">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3a248-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-277"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3a248-278">(21)</span><span class="sxs-lookup"><span data-stu-id="3a248-278">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-279">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="3a248-279">System failure.</span></span> <span data-ttu-id="3a248-280">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="3a248-280">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3a248-281">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-281">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3a248-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="3a248-282"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3a248-283">(22)</span><span class="sxs-lookup"><span data-stu-id="3a248-283">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-284">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3a248-284">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3a248-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="3a248-285"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3a248-286">(23)</span><span class="sxs-lookup"><span data-stu-id="3a248-286">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-287">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="3a248-287">System failure.</span></span> <span data-ttu-id="3a248-288">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="3a248-288">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3a248-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="3a248-289"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3a248-290">(24)</span><span class="sxs-lookup"><span data-stu-id="3a248-290">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-291">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="3a248-291">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3a248-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-292"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3a248-293">(25)</span><span class="sxs-lookup"><span data-stu-id="3a248-293">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-294">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-294">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3a248-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-295"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3a248-296">(26)</span><span class="sxs-lookup"><span data-stu-id="3a248-296">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-297">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a248-297">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3a248-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="3a248-298"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3a248-299">(27)</span><span class="sxs-lookup"><span data-stu-id="3a248-299">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-300">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="3a248-300">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3a248-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="3a248-301"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3a248-302">(28)</span><span class="sxs-lookup"><span data-stu-id="3a248-302">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-303">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="3a248-303">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3a248-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="3a248-304"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3a248-305">(29)</span><span class="sxs-lookup"><span data-stu-id="3a248-305">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-306">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3a248-306">Device is disabled.</span></span> <span data-ttu-id="3a248-307">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="3a248-307">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3a248-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="3a248-308"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3a248-309">(30)</span><span class="sxs-lookup"><span data-stu-id="3a248-309">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-310">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="3a248-310">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3a248-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="3a248-311"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3a248-312">31</span><span class="sxs-lookup"><span data-stu-id="3a248-312">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-313">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a248-313">Device is not working properly.</span></span> <span data-ttu-id="3a248-314">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="3a248-314">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a248-315">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="3a248-315">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-316">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3a248-316">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-318">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3a248-318">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-319">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="3a248-319">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3a248-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-321">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3a248-321">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-324">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a248-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a248-325">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="3a248-325">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3a248-326">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="3a248-326">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="3a248-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-328">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a248-328">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-331">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="3a248-331">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-332">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a248-332">Description of the object.</span></span>

<span data-ttu-id="3a248-333">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-333">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-334">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="3a248-334">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-335">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-337">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil \| de DMTF 002,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivatios-horas ")</span><span class="sxs-lookup"><span data-stu-id="3a248-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-338">Diseño de la capacidad de la batería en milivatios-horas.</span><span class="sxs-lookup"><span data-stu-id="3a248-338">Design capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="3a248-339">Si no se admite la propiedad, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="3a248-339">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="3a248-340">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-340">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-341">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="3a248-341">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-342">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3a248-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-344">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Unidad DMTF portátil \| 002,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="3a248-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-345">Tensión de diseño de la batería en milivoltios.</span><span class="sxs-lookup"><span data-stu-id="3a248-345">Design voltage of the battery in millivolts.</span></span> <span data-ttu-id="3a248-346">Si no se admite el atributo, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="3a248-346">If the attribute is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="3a248-347">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-347">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

<span data-ttu-id="3a248-348">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3a248-348">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-349">**ID**</span><span class="sxs-lookup"><span data-stu-id="3a248-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-352">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="3a248-352">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-353">Identifica la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-353">Identifies the battery.</span></span>

<span data-ttu-id="3a248-354">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3a248-355">Ejemplo: "batería interna"</span><span class="sxs-lookup"><span data-stu-id="3a248-355">Example: "Internal Battery"</span></span>

</dd> <dt>

<span data-ttu-id="3a248-356">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3a248-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-357">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3a248-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a248-359">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="3a248-359">If **True**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="3a248-360">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3a248-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-362">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a248-364">Cadena de forma libre que proporciona más información sobre el error registrado en la propiedad **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="3a248-364">Free-form string that supplies more information about the error recorded in **LastErrorCode** property, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="3a248-365">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-366">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="3a248-366">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-367">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a248-367">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-369">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("porcentaje")</span><span class="sxs-lookup"><span data-stu-id="3a248-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-370">Estimación del porcentaje de carga completa restante.</span><span class="sxs-lookup"><span data-stu-id="3a248-370">Estimate of the percentage of full charge remaining.</span></span>

<span data-ttu-id="3a248-371">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-371">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-372">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="3a248-372">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-373">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-373">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-375">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="3a248-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-376">Estime en minutos el agotamiento del tiempo de la carga de la batería en las condiciones actuales de carga si la utilidad de energía está apagada, perdida y permanece apagada, o si un equipo portátil está desconectado de una fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="3a248-376">Estimate in minutes of the time to battery charge depletion under the present load conditions if the utility power is off, or lost and remains off, or a laptop is disconnected from a power source.</span></span>

<span data-ttu-id="3a248-377">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-377">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-378">**ExpectedBatteryLife**</span><span class="sxs-lookup"><span data-stu-id="3a248-378">**ExpectedBatteryLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-379">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-381">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ Services \| BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="3a248-381">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("HKEY\_LOCAL\_MACHINE\\\\System\\\\CurrentControlSet\\\\Services\|BatteryLife"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-382">Cantidad de tiempo que se tarda en agotar la batería por completo una vez que se ha cargado por completo.</span><span class="sxs-lookup"><span data-stu-id="3a248-382">Amount of time it takes to completely drain the battery after it is fully charged.</span></span> <span data-ttu-id="3a248-383">Esta propiedad ya no se utiliza y se considera obsoleta.</span><span class="sxs-lookup"><span data-stu-id="3a248-383">This property is no longer used and is considered obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="3a248-384">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="3a248-384">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-385">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-385">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-386">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-387">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="3a248-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-388">La duración esperada de la batería en minutos, suponiendo que la batería está totalmente cargada.</span><span class="sxs-lookup"><span data-stu-id="3a248-388">Battery's expected lifetime in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="3a248-389">La propiedad representa la vida total esperada de la batería, no su vida restante actual, que se indica mediante la propiedad **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="3a248-389">The property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

<span data-ttu-id="3a248-390">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-390">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-391">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="3a248-391">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-392">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-394">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil \| de DMTF 002,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivatios-horas ")</span><span class="sxs-lookup"><span data-stu-id="3a248-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-395">Capacidad de carga completa de la batería en milivatios-horas.</span><span class="sxs-lookup"><span data-stu-id="3a248-395">Full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="3a248-396">La comparación del valor con la propiedad **designCapacity** determina cuándo es necesario reemplazar la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-396">Comparison of the value to the **DesignCapacity** property determines when the battery requires replacement.</span></span> <span data-ttu-id="3a248-397">El final de la vida de una batería suele ser cuando la propiedad **FullChargeCapacity** cae por debajo del 80% de la propiedad **designCapacity** .</span><span class="sxs-lookup"><span data-stu-id="3a248-397">A battery's end of life is typically when the **FullChargeCapacity** property falls below 80% of the **DesignCapacity** property.</span></span> <span data-ttu-id="3a248-398">Si no se admite la propiedad, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="3a248-398">If the property is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="3a248-399">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-399">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-400">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3a248-400">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-401">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a248-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-403">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="3a248-403">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-404">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="3a248-404">Date and time the object was installed.</span></span> <span data-ttu-id="3a248-405">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3a248-405">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3a248-406">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-407">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3a248-407">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-408">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-408">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a248-410">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3a248-410">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3a248-411">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-412">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="3a248-412">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-413">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-413">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-415">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="3a248-415">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-416">Tiempo máximo, en minutos, para cargar por completo la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-416">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="3a248-417">La propiedad representa el tiempo para recargar una batería totalmente agotada, no el tiempo de carga restante actual, que se indica en la propiedad **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="3a248-417">The property represents the time to recharge a fully depleted battery, not the current remaining charge time, which is indicated in the **TimeToFullCharge** property.</span></span>

<span data-ttu-id="3a248-418">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-418">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-419">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3a248-419">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-420">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-422">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="3a248-422">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-423">Define la etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="3a248-423">Defines the label by which the object is known.</span></span> <span data-ttu-id="3a248-424">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="3a248-424">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="3a248-425">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-425">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-426">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3a248-426">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-429">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3a248-429">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-430">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3a248-430">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="3a248-431">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3a248-432">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3a248-432">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3a248-433">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3a248-433">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-434">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a248-434">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3a248-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a248-436">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3a248-436">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3a248-437">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="3a248-437">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a248-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3a248-438"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3a248-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="3a248-439"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3a248-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="3a248-440"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3a248-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3a248-441"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-442">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="3a248-442">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3a248-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="3a248-443"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-444">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="3a248-444">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3a248-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="3a248-445"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-446">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="3a248-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3a248-447">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="3a248-447">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="3a248-448">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="3a248-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3a248-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="3a248-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-450">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="3a248-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3a248-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="3a248-451"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3a248-452">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="3a248-452">Timed Power-On Supported</span></span>

<span data-ttu-id="3a248-453">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="3a248-453">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a248-454">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3a248-454">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-455">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3a248-455">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-456">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a248-457">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="3a248-457">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="3a248-458">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="3a248-458">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="3a248-459">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-460">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="3a248-460">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-461">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-461">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-462">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-463">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="3a248-463">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-464">Número de versión de especificación de datos compatible con la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-464">Data Specification version number supported by the battery.</span></span> <span data-ttu-id="3a248-465">Si la batería no admite esta función, el valor debe dejarse en blanco.</span><span class="sxs-lookup"><span data-stu-id="3a248-465">If the battery does not support this function, the value should be left blank.</span></span>

<span data-ttu-id="3a248-466">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-466">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-467">**Estado**</span><span class="sxs-lookup"><span data-stu-id="3a248-467">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-468">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-470">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="3a248-470">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-471">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a248-471">Current status of the object.</span></span> <span data-ttu-id="3a248-472">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="3a248-472">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3a248-473">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="3a248-473">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3a248-474">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="3a248-474">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3a248-475">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="3a248-475">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3a248-476">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="3a248-476">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3a248-477">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-477">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3a248-478">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="3a248-478">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3a248-479">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="3a248-479">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3a248-480">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="3a248-480">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3a248-481">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="3a248-481">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a248-482">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="3a248-482">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3a248-483">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="3a248-483">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3a248-484">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="3a248-484">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3a248-485">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="3a248-485">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3a248-486">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="3a248-486">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3a248-487">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="3a248-487">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3a248-488">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="3a248-488">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3a248-489">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="3a248-489">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3a248-490">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="3a248-490">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a248-491">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3a248-491">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-492">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a248-492">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-493">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-494">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="3a248-494">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-495">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3a248-495">State of the logical device.</span></span> <span data-ttu-id="3a248-496">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3a248-496">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="3a248-497">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3a248-498">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3a248-498">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3a248-499">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="3a248-499">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3a248-500">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3a248-500">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3a248-501">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="3a248-501">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3a248-502">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="3a248-502">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a248-503">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3a248-503">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-504">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-504">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-505">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-506">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a248-506">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a248-507">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3a248-507">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="3a248-508">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-508">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-509">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3a248-509">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-510">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a248-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-511">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-512">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="3a248-512">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="3a248-513">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3a248-513">Name of the scoping system.</span></span>

<span data-ttu-id="3a248-514">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-514">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-515">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="3a248-515">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-516">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-516">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-517">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-518">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="3a248-518">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-519">Tiempo transcurrido en segundos desde la última vez que el sistema del equipo cambió a la energía de la batería o desde la última vez que se reinició el sistema o SAI, lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="3a248-519">Elapsed time in seconds since the computer system's UPS last switched to battery power, or the time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="3a248-520">Si la batería está "en línea", se devuelve 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="3a248-520">If the battery is "on line", 0 (zero) is returned.</span></span>

<span data-ttu-id="3a248-521">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-521">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a248-522">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="3a248-522">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a248-523">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a248-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a248-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a248-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a248-525">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="3a248-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="3a248-526">Tiempo restante para cargar la batería por completo en minutos con la tarifa de carga actual y el uso.</span><span class="sxs-lookup"><span data-stu-id="3a248-526">Remaining time to charge the battery fully in minutes at the current charging rate and usage.</span></span>

<span data-ttu-id="3a248-527">Esta propiedad se hereda de [**la \_ batería CIM**](cim-battery.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-527">This property is inherited from [**CIM\_Battery**](cim-battery.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a248-528">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a248-528">Remarks</span></span>

<span data-ttu-id="3a248-529">La clase de **\_ batería de Win32** se deriva de la [**\_ batería de CIM**](cim-battery.md) , que se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="3a248-529">The **Win32\_Battery** class is derived from [**CIM\_Battery**](cim-battery.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3a248-530">Windows Server 2008 contiene los controladores de UPS (APC) en el sistema operativo, lo que le permite tratar el UPS como suministro de la batería.</span><span class="sxs-lookup"><span data-stu-id="3a248-530">Windows Server 2008 contains the (APC) UPS drivers in the OS, which allows you to treat the UPS as a battery supply.</span></span> <span data-ttu-id="3a248-531">Esto le permite supervisar el estado del SAI mediante un script y realizar acciones cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="3a248-531">This allows you to monitor the UPS status using a script and take actions when necessary.</span></span>

## <a name="examples"></a><span data-ttu-id="3a248-532">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3a248-532">Examples</span></span>

<span data-ttu-id="3a248-533">En el ejemplo de código de PowerShell de [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) se consulta la **\_ batería de Win32** para determinar si se debe o no activar o desactivar la red inalámbrica con el fin de ahorrar energía.</span><span class="sxs-lookup"><span data-stu-id="3a248-533">The [Toggle-Wireless.ps1](https://Gallery.TechNet.Microsoft.Com/Toggle-Wirelessps1-2d244a8f) PowerShell code sample queries **Win32\_Battery** to determine whether or not to toggle the wireless in order to save power.</span></span>

<span data-ttu-id="3a248-534">En el ejemplo de [información de SAI](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) de la lista Perl se muestra información acerca de las fuentes de alimentación ininterrumpidas conectadas a un equipo.</span><span class="sxs-lookup"><span data-stu-id="3a248-534">The [List UPS Information](https://Gallery.TechNet.Microsoft.Com/7196121e-97de-4290-9939-26d0ce266270) Perl sample Lists information about the uninterruptible power sources attached to a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a248-535">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a248-535">Requirements</span></span>



| <span data-ttu-id="3a248-536">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a248-536">Requirement</span></span> | <span data-ttu-id="3a248-537">Value</span><span class="sxs-lookup"><span data-stu-id="3a248-537">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a248-538">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a248-538">Minimum supported client</span></span><br/> | <span data-ttu-id="3a248-539">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a248-539">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a248-540">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a248-540">Minimum supported server</span></span><br/> | <span data-ttu-id="3a248-541">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a248-541">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a248-542">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a248-542">Namespace</span></span><br/>                | <span data-ttu-id="3a248-543">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3a248-543">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a248-544">MOF</span><span class="sxs-lookup"><span data-stu-id="3a248-544">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a248-545"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a248-545"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a248-546">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3a248-546">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a248-547"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a248-547"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a248-548">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a248-548">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a248-549">**\_Batería CIM**</span><span class="sxs-lookup"><span data-stu-id="3a248-549">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dt>

[<span data-ttu-id="3a248-550">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="3a248-550">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

