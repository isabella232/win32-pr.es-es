---
description: La \_ clase de batería CIM representa las capacidades y la administración del dispositivo lógico de batería. Esta clase se aplica a las baterías de los sistemas portátiles y a otras baterías internas y externas.
ms.assetid: af127b7a-021b-4cd8-af1b-176aff760858
ms.tgt_platform: multiple
title: CIM_Battery (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Battery
- CIM_Battery.Caption
- CIM_Battery.Description
- CIM_Battery.InstallDate
- CIM_Battery.Name
- CIM_Battery.Status
- CIM_Battery.Availability
- CIM_Battery.ConfigManagerErrorCode
- CIM_Battery.ConfigManagerUserConfig
- CIM_Battery.CreationClassName
- CIM_Battery.DeviceID
- CIM_Battery.PowerManagementCapabilities
- CIM_Battery.ErrorCleared
- CIM_Battery.ErrorDescription
- CIM_Battery.LastErrorCode
- CIM_Battery.PNPDeviceID
- CIM_Battery.PowerManagementSupported
- CIM_Battery.StatusInfo
- CIM_Battery.SystemCreationClassName
- CIM_Battery.SystemName
- CIM_Battery.BatteryStatus
- CIM_Battery.Chemistry
- CIM_Battery.DesignCapacity
- CIM_Battery.DesignVoltage
- CIM_Battery.EstimatedChargeRemaining
- CIM_Battery.EstimatedRunTime
- CIM_Battery.ExpectedLife
- CIM_Battery.FullChargeCapacity
- CIM_Battery.MaxRechargeTime
- CIM_Battery.SmartBatteryVersion
- CIM_Battery.TimeOnBattery
- CIM_Battery.TimeToFullCharge
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3719b2700c69cfa58921bed1242aa8a6de158466
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659654"
---
# <a name="cim_battery-class"></a><span data-ttu-id="79554-104">\_Clase de batería CIM</span><span class="sxs-lookup"><span data-stu-id="79554-104">CIM\_Battery class</span></span>

<span data-ttu-id="79554-105">La clase de **\_ batería CIM** representa las capacidades y la administración del dispositivo lógico de batería.</span><span class="sxs-lookup"><span data-stu-id="79554-105">The **CIM\_Battery** class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="79554-106">Esta clase se aplica a las baterías de los sistemas portátiles y a otras baterías internas y externas.</span><span class="sxs-lookup"><span data-stu-id="79554-106">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79554-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="79554-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="79554-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="79554-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="79554-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="79554-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="79554-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="79554-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="79554-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79554-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C548-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Battery : CIM_LogicalDevice
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
  uint16   BatteryStatus;
  uint16   Chemistry;
  uint32   DesignCapacity;
  uint64   DesignVoltage;
  uint16   EstimatedChargeRemaining;
  uint32   EstimatedRunTime;
  uint32   ExpectedLife;
  uint32   FullChargeCapacity;
  uint32   MaxRechargeTime;
  string   SmartBatteryVersion;
  uint32   TimeOnBattery;
  uint32   TimeToFullCharge;
};
```

## <a name="members"></a><span data-ttu-id="79554-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="79554-112">Members</span></span>

<span data-ttu-id="79554-113">La clase de **\_ batería CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="79554-113">The **CIM\_Battery** class has these types of members:</span></span>

-   [<span data-ttu-id="79554-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="79554-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="79554-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79554-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="79554-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="79554-116">Methods</span></span>

<span data-ttu-id="79554-117">La clase de **\_ batería CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="79554-117">The **CIM\_Battery** class has these methods.</span></span>



| <span data-ttu-id="79554-118">Método</span><span class="sxs-lookup"><span data-stu-id="79554-118">Method</span></span>                                                             | <span data-ttu-id="79554-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="79554-119">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79554-120">**Reset**</span><span class="sxs-lookup"><span data-stu-id="79554-120">**Reset**</span></span>](reset-method-in-class-cim-battery.md)                 | <span data-ttu-id="79554-121">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79554-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="79554-122">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="79554-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="79554-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="79554-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-battery.md) | <span data-ttu-id="79554-124">Define el estado de energía deseado para un dispositivo lógico y el momento en que el dispositivo debe ponerse en ese estado.</span><span class="sxs-lookup"><span data-stu-id="79554-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="79554-125">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="79554-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="79554-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79554-126">Properties</span></span>

<span data-ttu-id="79554-127">La clase de **\_ batería CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="79554-127">The **CIM\_Battery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79554-128">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="79554-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79554-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79554-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-131">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="79554-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="79554-132">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79554-132">Availability and status of the device.</span></span>

<span data-ttu-id="79554-133">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79554-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="79554-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79554-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="79554-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="79554-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="79554-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="79554-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="79554-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="79554-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="79554-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="79554-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="79554-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="79554-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="79554-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="79554-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="79554-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="79554-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="79554-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="79554-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="79554-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="79554-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="79554-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="79554-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="79554-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="79554-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="79554-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="79554-147">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="79554-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="79554-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="79554-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="79554-149">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="79554-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="79554-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="79554-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="79554-151">El dispositivo no funciona, pero podría pasar rápidamente a pleno consumo de energía.</span><span class="sxs-lookup"><span data-stu-id="79554-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="79554-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="79554-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="79554-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="79554-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="79554-154">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="79554-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="79554-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="79554-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="79554-156">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="79554-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="79554-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="79554-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="79554-158">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="79554-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="79554-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="79554-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="79554-160">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="79554-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="79554-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="79554-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="79554-162">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="79554-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79554-163">**BatteryStatus**</span><span class="sxs-lookup"><span data-stu-id="79554-163">**BatteryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-164">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79554-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79554-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-166">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,14 ")</span><span class="sxs-lookup"><span data-stu-id="79554-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.14")</span></span>
</dt> </dl>

<span data-ttu-id="79554-167">Descripción del estado de los cargos de la batería.</span><span class="sxs-lookup"><span data-stu-id="79554-167">Description of the battery's charge status.</span></span> <span data-ttu-id="79554-168">El valor 10 no es válido en el esquema CIM, que no representa ninguna batería instalada en la interfaz de administración de escritorio (DMI).</span><span class="sxs-lookup"><span data-stu-id="79554-168">The value 10 is not valid in the CIM schema, which represents no battery being installed in Desktop Management Interface (DMI).</span></span> <span data-ttu-id="79554-169">En este caso, no se debe crear una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="79554-169">In this case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79554-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="79554-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="79554-171">Otros.</span><span class="sxs-lookup"><span data-stu-id="79554-171">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79554-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="79554-172"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="79554-173">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="79554-173">Unknown.</span></span>

</dd> <dt>

<span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>

<span data-ttu-id="79554-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>Con **cargos completos** (3)</span><span class="sxs-lookup"><span data-stu-id="79554-174"><span id="Fully_Charged"></span><span id="fully_charged"></span><span id="FULLY_CHARGED"></span>**Fully Charged** (3)</span></span>


</dt> <dd>

<span data-ttu-id="79554-175">Totalmente cargado.</span><span class="sxs-lookup"><span data-stu-id="79554-175">Fully charged.</span></span>

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="79554-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Bajo** (4)</span><span class="sxs-lookup"><span data-stu-id="79554-176"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (4)</span></span>


</dt> <dd>

<span data-ttu-id="79554-177">Baja.</span><span class="sxs-lookup"><span data-stu-id="79554-177">Low.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="79554-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="79554-178"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd>

<span data-ttu-id="79554-179">Crítico.</span><span class="sxs-lookup"><span data-stu-id="79554-179">Critical.</span></span>

</dd> <dt>

<span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>

<span data-ttu-id="79554-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Carga** (6)</span><span class="sxs-lookup"><span data-stu-id="79554-180"><span id="Charging"></span><span id="charging"></span><span id="CHARGING"></span>**Charging** (6)</span></span>


</dt> <dd>

<span data-ttu-id="79554-181">Cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="79554-181">Charging.</span></span>

</dd> <dt>

<span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>

<span data-ttu-id="79554-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Cargando y alto** (7)</span><span class="sxs-lookup"><span data-stu-id="79554-182"><span id="Charging_and_High"></span><span id="charging_and_high"></span><span id="CHARGING_AND_HIGH"></span>**Charging and High** (7)</span></span>


</dt> <dd>

<span data-ttu-id="79554-183">Carga y alta.</span><span class="sxs-lookup"><span data-stu-id="79554-183">Charging and high.</span></span>

</dd> <dt>

<span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>

<span data-ttu-id="79554-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Cargando y bajo** (8)</span><span class="sxs-lookup"><span data-stu-id="79554-184"><span id="Charging_and_Low"></span><span id="charging_and_low"></span><span id="CHARGING_AND_LOW"></span>**Charging and Low** (8)</span></span>


</dt> <dd>

<span data-ttu-id="79554-185">Cargando y bajo.</span><span class="sxs-lookup"><span data-stu-id="79554-185">Charging and low.</span></span>

</dd> <dt>

<span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>

<span data-ttu-id="79554-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Carga y crítico** (9)</span><span class="sxs-lookup"><span data-stu-id="79554-186"><span id="Charging_and_Critical"></span><span id="charging_and_critical"></span><span id="CHARGING_AND_CRITICAL"></span>**Charging and Critical** (9)</span></span>


</dt> <dd>

<span data-ttu-id="79554-187">Carga y crítico.</span><span class="sxs-lookup"><span data-stu-id="79554-187">Charging and critical.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="79554-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Sin definir** (10)</span><span class="sxs-lookup"><span data-stu-id="79554-188"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (10)</span></span>


</dt> <dd>

<span data-ttu-id="79554-189">Sin definir.</span><span class="sxs-lookup"><span data-stu-id="79554-189">Undefined.</span></span>

</dd> <dt>

<span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>

<span data-ttu-id="79554-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Cargado parcialmente** (11)</span><span class="sxs-lookup"><span data-stu-id="79554-190"><span id="Partially_Charged"></span><span id="partially_charged"></span><span id="PARTIALLY_CHARGED"></span>**Partially Charged** (11)</span></span>


</dt> <dd>

<span data-ttu-id="79554-191">Cargado parcialmente.</span><span class="sxs-lookup"><span data-stu-id="79554-191">Partially charged.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79554-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="79554-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-195">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="79554-195">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="79554-196">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="79554-196">A short textual description of the object.</span></span>

<span data-ttu-id="79554-197">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79554-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-198">**Químicos**</span><span class="sxs-lookup"><span data-stu-id="79554-198">**Chemistry**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-199">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79554-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79554-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-201">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,7 ")</span><span class="sxs-lookup"><span data-stu-id="79554-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="79554-202">Enumeración que describe la química de la batería.</span><span class="sxs-lookup"><span data-stu-id="79554-202">Enumeration that describes the battery's chemistry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79554-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="79554-203"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="79554-204">Otros.</span><span class="sxs-lookup"><span data-stu-id="79554-204">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79554-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="79554-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="79554-206">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="79554-206">Unknown.</span></span>

</dd> <dt>

<span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>

<span data-ttu-id="79554-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Acid inicial** (3)</span><span class="sxs-lookup"><span data-stu-id="79554-207"><span id="Lead_Acid"></span><span id="lead_acid"></span><span id="LEAD_ACID"></span>**Lead Acid** (3)</span></span>


</dt> <dd>

<span data-ttu-id="79554-208">Acid plomo.</span><span class="sxs-lookup"><span data-stu-id="79554-208">Lead acid.</span></span>

</dd> <dt>

<span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>

<span data-ttu-id="79554-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Níquel cadmio** (4)</span><span class="sxs-lookup"><span data-stu-id="79554-209"><span id="Nickel_Cadmium"></span><span id="nickel_cadmium"></span><span id="NICKEL_CADMIUM"></span>**Nickel Cadmium** (4)</span></span>


</dt> <dd>

<span data-ttu-id="79554-210">Níquel cadmio.</span><span class="sxs-lookup"><span data-stu-id="79554-210">Nickel cadmium.</span></span>

</dd> <dt>

<span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>

<span data-ttu-id="79554-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Hidruro de níquel metal** (5)</span><span class="sxs-lookup"><span data-stu-id="79554-211"><span id="Nickel_Metal_Hydride"></span><span id="nickel_metal_hydride"></span><span id="NICKEL_METAL_HYDRIDE"></span>**Nickel Metal Hydride** (5)</span></span>


</dt> <dd>

<span data-ttu-id="79554-212">Hidruro de níquel metal.</span><span class="sxs-lookup"><span data-stu-id="79554-212">Nickel metal hydride.</span></span>

</dd> <dt>

<span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>

<span data-ttu-id="79554-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Ion-** litio (6)</span><span class="sxs-lookup"><span data-stu-id="79554-213"><span id="Lithium-ion"></span><span id="lithium-ion"></span><span id="LITHIUM-ION"></span>**Lithium-ion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="79554-214">Ión de litio.</span><span class="sxs-lookup"><span data-stu-id="79554-214">Lithium ion.</span></span>

</dd> <dt>

<span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>

<span data-ttu-id="79554-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Aire de zinc** (7)</span><span class="sxs-lookup"><span data-stu-id="79554-215"><span id="Zinc_air"></span><span id="zinc_air"></span><span id="ZINC_AIR"></span>**Zinc air** (7)</span></span>


</dt> <dd>

<span data-ttu-id="79554-216">Aire de cinc.</span><span class="sxs-lookup"><span data-stu-id="79554-216">Zinc air.</span></span>

</dd> <dt>

<span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>

<span data-ttu-id="79554-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Polímero de litio** (8)</span><span class="sxs-lookup"><span data-stu-id="79554-217"><span id="Lithium_Polymer"></span><span id="lithium_polymer"></span><span id="LITHIUM_POLYMER"></span>**Lithium Polymer** (8)</span></span>


</dt> <dd>

<span data-ttu-id="79554-218">Polímero de litio.</span><span class="sxs-lookup"><span data-stu-id="79554-218">Lithium polymer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79554-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="79554-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-220">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-222">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="79554-222">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="79554-223">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="79554-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="79554-224">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="79554-225">**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="79554-225">**This device is working properly.**</span></span> <span data-ttu-id="79554-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="79554-226">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="79554-227">**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="79554-227">**This device is not configured correctly.**</span></span> <span data-ttu-id="79554-228">(1)</span><span class="sxs-lookup"><span data-stu-id="79554-228">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="79554-229">**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-229">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="79554-230">(2)</span><span class="sxs-lookup"><span data-stu-id="79554-230">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="79554-231">**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="79554-231">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="79554-232">(3)</span><span class="sxs-lookup"><span data-stu-id="79554-232">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="79554-233">**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="79554-233">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="79554-234">(4)</span><span class="sxs-lookup"><span data-stu-id="79554-234">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="79554-235">**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="79554-235">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="79554-236">(5)</span><span class="sxs-lookup"><span data-stu-id="79554-236">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="79554-237">**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="79554-237">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="79554-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="79554-238">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="79554-239">**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="79554-239">**Cannot filter.**</span></span> <span data-ttu-id="79554-240">(7)</span><span class="sxs-lookup"><span data-stu-id="79554-240">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="79554-241">**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-241">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="79554-242">(8)</span><span class="sxs-lookup"><span data-stu-id="79554-242">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="79554-243">**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="79554-243">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="79554-244">(9)</span><span class="sxs-lookup"><span data-stu-id="79554-244">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="79554-245">**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="79554-245">**This device cannot start.**</span></span> <span data-ttu-id="79554-246">(10)</span><span class="sxs-lookup"><span data-stu-id="79554-246">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="79554-247">**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-247">**This device failed.**</span></span> <span data-ttu-id="79554-248">(11)</span><span class="sxs-lookup"><span data-stu-id="79554-248">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="79554-249">**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="79554-249">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="79554-250">(12)</span><span class="sxs-lookup"><span data-stu-id="79554-250">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="79554-251">**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-251">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="79554-252">(13)</span><span class="sxs-lookup"><span data-stu-id="79554-252">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="79554-253">**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="79554-253">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="79554-254">(14)</span><span class="sxs-lookup"><span data-stu-id="79554-254">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="79554-255">**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="79554-255">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="79554-256">(15)</span><span class="sxs-lookup"><span data-stu-id="79554-256">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="79554-257">**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-257">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="79554-258">(16)</span><span class="sxs-lookup"><span data-stu-id="79554-258">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="79554-259">**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="79554-259">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="79554-260">(17)</span><span class="sxs-lookup"><span data-stu-id="79554-260">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="79554-261">**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-261">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="79554-262">(18)</span><span class="sxs-lookup"><span data-stu-id="79554-262">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="79554-263">**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="79554-263">**Failure using the VxD loader.**</span></span> <span data-ttu-id="79554-264">(19)</span><span class="sxs-lookup"><span data-stu-id="79554-264">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="79554-265">**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="79554-265">**Your registry might be corrupted.**</span></span> <span data-ttu-id="79554-266">(20)</span><span class="sxs-lookup"><span data-stu-id="79554-266">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="79554-267">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-267">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="79554-268">(21)</span><span class="sxs-lookup"><span data-stu-id="79554-268">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="79554-269">**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="79554-269">**This device is disabled.**</span></span> <span data-ttu-id="79554-270">(22)</span><span class="sxs-lookup"><span data-stu-id="79554-270">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="79554-271">**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="79554-271">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="79554-272">(23)</span><span class="sxs-lookup"><span data-stu-id="79554-272">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="79554-273">**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="79554-273">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="79554-274">(24)</span><span class="sxs-lookup"><span data-stu-id="79554-274">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="79554-275">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-275">**Windows is still setting up this device.**</span></span> <span data-ttu-id="79554-276">(25)</span><span class="sxs-lookup"><span data-stu-id="79554-276">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="79554-277">**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="79554-278">(26)</span><span class="sxs-lookup"><span data-stu-id="79554-278">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="79554-279">**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="79554-279">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="79554-280">(27)</span><span class="sxs-lookup"><span data-stu-id="79554-280">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="79554-281">**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="79554-281">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="79554-282">(28)</span><span class="sxs-lookup"><span data-stu-id="79554-282">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="79554-283">**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="79554-283">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="79554-284">(29)</span><span class="sxs-lookup"><span data-stu-id="79554-284">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="79554-285">**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="79554-285">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="79554-286">(30)</span><span class="sxs-lookup"><span data-stu-id="79554-286">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="79554-287">**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="79554-287">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="79554-288">31</span><span class="sxs-lookup"><span data-stu-id="79554-288">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79554-289">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="79554-289">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-290">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="79554-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79554-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-292">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="79554-292">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="79554-293">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="79554-293">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="79554-294">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-295">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79554-295">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-298">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79554-298">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79554-299">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="79554-299">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="79554-300">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="79554-300">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="79554-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-302">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="79554-302">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-305">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="79554-305">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="79554-306">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="79554-306">A textual description of the object.</span></span>

<span data-ttu-id="79554-307">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79554-307">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-308">**DesignCapacity**</span><span class="sxs-lookup"><span data-stu-id="79554-308">**DesignCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-309">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-309">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-311">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil \| de DMTF 002,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivatios-horas ")</span><span class="sxs-lookup"><span data-stu-id="79554-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="79554-312">Capacidad diseñada de la batería en milivatios-horas.</span><span class="sxs-lookup"><span data-stu-id="79554-312">Designed capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="79554-313">Si no se admite esta propiedad, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="79554-313">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="79554-314">**DesignVoltage**</span><span class="sxs-lookup"><span data-stu-id="79554-314">**DesignVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-315">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="79554-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="79554-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-317">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Unidad DMTF portátil \| 002,9 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="79554-317">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.9"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="79554-318">Voltaje diseñado de la batería en milivoltios.</span><span class="sxs-lookup"><span data-stu-id="79554-318">Designed voltage of the battery in millivolts.</span></span> <span data-ttu-id="79554-319">Si no se admite este atributo, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="79554-319">If this attribute is not supported, enter 0.</span></span>

<span data-ttu-id="79554-320">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="79554-320">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="79554-321">**ID**</span><span class="sxs-lookup"><span data-stu-id="79554-321">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-324">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79554-324">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79554-325">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79554-325">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="79554-326">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-326">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-327">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="79554-327">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-328">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="79554-328">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79554-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79554-330">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="79554-330">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="79554-331">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-332">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="79554-332">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-333">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79554-335">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="79554-335">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="79554-336">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-337">**EstimatedChargeRemaining**</span><span class="sxs-lookup"><span data-stu-id="79554-337">**EstimatedChargeRemaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-338">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79554-338">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79554-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-340">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("porcentaje")</span><span class="sxs-lookup"><span data-stu-id="79554-340">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="79554-341">Porcentaje estimado del importe total restante.</span><span class="sxs-lookup"><span data-stu-id="79554-341">Estimated percentage of the remaining full charge.</span></span>

</dd> <dt>

<span data-ttu-id="79554-342">**EstimatedRunTime**</span><span class="sxs-lookup"><span data-stu-id="79554-342">**EstimatedRunTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-343">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-345">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="79554-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="79554-346">Tiempo estimado, en minutos, hasta que se agota la carga de la batería bajo las condiciones de carga presentes si la utilidad de alimentación está apagada, se pierde y permanece desactivada, o si un equipo portátil se desconecta de una fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="79554-346">Estimated time, in minutes, until the battery charge is depleted under the present load conditions if the utility power is off, is lost and remains off, or if a laptop is disconnected from a power source.</span></span>

</dd> <dt>

<span data-ttu-id="79554-347">**ExpectedLife**</span><span class="sxs-lookup"><span data-stu-id="79554-347">**ExpectedLife**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-348">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-350">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="79554-350">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="79554-351">La duración esperada de la batería, en minutos, suponiendo que la batería está totalmente cargada.</span><span class="sxs-lookup"><span data-stu-id="79554-351">Battery's expected lifetime, in minutes, assuming that the battery is fully charged.</span></span> <span data-ttu-id="79554-352">Esta propiedad representa la vida total esperada de la batería, no su vida restante actual, que se indica mediante la propiedad **EstimatedRunTime** .</span><span class="sxs-lookup"><span data-stu-id="79554-352">This property represents the total expected life of the battery, not its current remaining life, which is indicated by the **EstimatedRunTime** property.</span></span>

</dd> <dt>

<span data-ttu-id="79554-353">**FullChargeCapacity**</span><span class="sxs-lookup"><span data-stu-id="79554-353">**FullChargeCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-354">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-356">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil \| de DMTF 002,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivatios-horas ")</span><span class="sxs-lookup"><span data-stu-id="79554-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatt-hours")</span></span>
</dt> </dl>

<span data-ttu-id="79554-357">La capacidad de carga completa de la batería en milivatios-horas.</span><span class="sxs-lookup"><span data-stu-id="79554-357">The full charge capacity of the battery in milliwatt-hours.</span></span> <span data-ttu-id="79554-358">Compare este valor con la propiedad **designCapacity** para determinar cuándo es necesario reemplazar la batería.</span><span class="sxs-lookup"><span data-stu-id="79554-358">Compare this value to the **DesignCapacity** property to determine when the battery requires replacement.</span></span> <span data-ttu-id="79554-359">La duración de la batería es normalmente cuando la propiedad **FullChargeCapacity** cae por debajo del 80 por ciento de la propiedad **designCapacity** .</span><span class="sxs-lookup"><span data-stu-id="79554-359">A battery's end-life is typically when the **FullChargeCapacity** property falls below 80 percent of the **DesignCapacity** property.</span></span> <span data-ttu-id="79554-360">Si no se admite esta propiedad, escriba 0.</span><span class="sxs-lookup"><span data-stu-id="79554-360">If this property is not supported, enter 0.</span></span>

</dd> <dt>

<span data-ttu-id="79554-361">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="79554-361">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-362">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="79554-362">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="79554-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-364">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="79554-364">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="79554-365">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="79554-365">Indicates when the object was installed.</span></span> <span data-ttu-id="79554-366">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="79554-366">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="79554-367">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79554-367">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-368">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="79554-368">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-369">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79554-371">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79554-371">Last error code reported by the logical device.</span></span>

<span data-ttu-id="79554-372">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-373">**MaxRechargeTime**</span><span class="sxs-lookup"><span data-stu-id="79554-373">**MaxRechargeTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-374">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-376">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="79554-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="79554-377">Tiempo máximo, en minutos, para cargar por completo la batería.</span><span class="sxs-lookup"><span data-stu-id="79554-377">Maximum time, in minutes, to fully charge the battery.</span></span> <span data-ttu-id="79554-378">Esta propiedad representa el tiempo para recargar una batería totalmente agotada, no el tiempo de carga restante actual, que se indica en la propiedad **TimeToFullCharge** .</span><span class="sxs-lookup"><span data-stu-id="79554-378">This property represents the time to recharge a fully depleted battery, not the current remaining charging time, which is indicated in the **TimeToFullCharge** property.</span></span>

</dd> <dt>

<span data-ttu-id="79554-379">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="79554-379">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-380">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-380">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-382">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="79554-382">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="79554-383">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="79554-383">Label by which the object is known.</span></span> <span data-ttu-id="79554-384">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="79554-384">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="79554-385">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79554-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="79554-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-387">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-389">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="79554-389">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="79554-390">Indica el identificador de dispositivo Plug and Play Win32 del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79554-390">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="79554-391">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="79554-391">Example: "\*PNP030b"</span></span>

<span data-ttu-id="79554-392">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-393">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="79554-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-394">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79554-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="79554-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79554-396">Indica las capacidades de energía específicas relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79554-396">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="79554-397">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79554-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="79554-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="79554-399">Las capacidades relacionadas con la energía son desconocidas.</span><span class="sxs-lookup"><span data-stu-id="79554-399">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="79554-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="79554-400"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="79554-401">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79554-401">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79554-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="79554-402"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="79554-403">Se han deshabilitado las capacidades relacionadas con la energía.</span><span class="sxs-lookup"><span data-stu-id="79554-403">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79554-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="79554-404"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="79554-405">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="79554-405">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="79554-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="79554-406"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="79554-407">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="79554-407">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="79554-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="79554-408"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="79554-409">Se admite el método **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="79554-409">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="79554-410">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="79554-410">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="79554-411">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="79554-411">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="79554-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="79554-412"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="79554-413">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía").</span><span class="sxs-lookup"><span data-stu-id="79554-413">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="79554-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="79554-414"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="79554-415">El método **SetPowerState** se puede invocar con el parámetro *PowerState* establecido en 5 ("ciclo de energía") y el parámetro *Time* establecido en una fecha y hora específicas, o Interval, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="79554-415">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="79554-416">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="79554-416">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-417">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="79554-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="79554-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="79554-419">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="79554-419">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="79554-420">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="79554-420">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="79554-421">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="79554-421">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="79554-422">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="79554-422">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="79554-423">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-423">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-424">**SmartBatteryVersion**</span><span class="sxs-lookup"><span data-stu-id="79554-424">**SmartBatteryVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-425">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-426">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-427">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,10 ")</span><span class="sxs-lookup"><span data-stu-id="79554-427">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.10")</span></span>
</dt> </dl>

<span data-ttu-id="79554-428">Número de versión de especificación de datos de batería inteligente compatible con esta batería.</span><span class="sxs-lookup"><span data-stu-id="79554-428">Smart battery data-specification version number that is supported by this battery.</span></span> <span data-ttu-id="79554-429">Si la batería no admite esta función, el valor debe dejarse vacío.</span><span class="sxs-lookup"><span data-stu-id="79554-429">If the battery does not support this function, the value should be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="79554-430">**Estado**</span><span class="sxs-lookup"><span data-stu-id="79554-430">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-431">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-432">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-433">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="79554-433">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="79554-434">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="79554-434">String that indicates the current status of the object.</span></span> <span data-ttu-id="79554-435">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="79554-435">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="79554-436">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="79554-436">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="79554-437">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="79554-437">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="79554-438">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="79554-438">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="79554-439">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="79554-439">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="79554-440">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="79554-440">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="79554-441">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="79554-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="79554-442">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="79554-442">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="79554-443">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="79554-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="79554-444">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="79554-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="79554-445">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="79554-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79554-446">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="79554-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="79554-447">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="79554-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="79554-448">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="79554-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="79554-449">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="79554-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="79554-450">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="79554-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="79554-451">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="79554-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="79554-452">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="79554-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="79554-453">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="79554-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="79554-454">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="79554-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79554-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="79554-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-456">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="79554-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="79554-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-458">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="79554-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="79554-459">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="79554-459">State of the logical device.</span></span> <span data-ttu-id="79554-460">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="79554-460">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="79554-461">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="79554-462">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="79554-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="79554-463">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="79554-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="79554-464">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="79554-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="79554-465">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="79554-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="79554-466">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="79554-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="79554-467">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="79554-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-468">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-470">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79554-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79554-471">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="79554-471">The scoping system's creation class name.</span></span>

<span data-ttu-id="79554-472">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="79554-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-474">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="79554-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79554-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-476">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="79554-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="79554-477">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="79554-477">The scoping system's name.</span></span>

<span data-ttu-id="79554-478">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="79554-479">**TimeOnBattery**</span><span class="sxs-lookup"><span data-stu-id="79554-479">**TimeOnBattery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-480">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-482">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")</span><span class="sxs-lookup"><span data-stu-id="79554-482">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="79554-483">Tiempo transcurrido, en segundos, desde la última vez que el sistema del equipo cambió a la energía de la batería, o la cantidad de tiempo transcurrido desde la última vez que se reinició el sistema o SAI, lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="79554-483">Elapsed time, in seconds, since the computer system's UPS last switched to battery power, or the amount of time since the system or UPS was last restarted, whichever is less.</span></span> <span data-ttu-id="79554-484">Se devuelve el valor 0 si la batería está "en línea".</span><span class="sxs-lookup"><span data-stu-id="79554-484">A value of 0 is returned if the battery is "online."</span></span>

</dd> <dt>

<span data-ttu-id="79554-485">**TimeToFullCharge**</span><span class="sxs-lookup"><span data-stu-id="79554-485">**TimeToFullCharge**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79554-486">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79554-486">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79554-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79554-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79554-488">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Batería portátil DMTF \| 002,16 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" minutos ")</span><span class="sxs-lookup"><span data-stu-id="79554-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Portable Battery\|002.16"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="79554-489">Tiempo restante, en minutos, para cargar la batería por completo a la tarifa de carga actual y usar.</span><span class="sxs-lookup"><span data-stu-id="79554-489">Remaining time, in minutes, to charge the battery fully at the current charging rate and use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79554-490">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79554-490">Remarks</span></span>

<span data-ttu-id="79554-491">La clase de **\_ batería CIM** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="79554-491">The **CIM\_Battery** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="79554-492">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="79554-492">WMI does not implement this class.</span></span> <span data-ttu-id="79554-493">Para obtener más información sobre las clases derivadas de la **\_ batería CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="79554-493">For more information about classes derived from **CIM\_Battery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="79554-494">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="79554-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="79554-495">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="79554-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="79554-496">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79554-496">Requirements</span></span>



| <span data-ttu-id="79554-497">Requisito</span><span class="sxs-lookup"><span data-stu-id="79554-497">Requirement</span></span> | <span data-ttu-id="79554-498">Value</span><span class="sxs-lookup"><span data-stu-id="79554-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79554-499">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79554-499">Minimum supported client</span></span><br/> | <span data-ttu-id="79554-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79554-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79554-501">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79554-501">Minimum supported server</span></span><br/> | <span data-ttu-id="79554-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79554-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79554-503">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="79554-503">Namespace</span></span><br/>                | <span data-ttu-id="79554-504">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="79554-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="79554-505">MOF</span><span class="sxs-lookup"><span data-stu-id="79554-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79554-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79554-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="79554-507">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="79554-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79554-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79554-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79554-509">Vea también</span><span class="sxs-lookup"><span data-stu-id="79554-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79554-510">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="79554-510">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

