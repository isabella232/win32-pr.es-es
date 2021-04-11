---
description: La \_ clase de energía CIM representa las capacidades y la administración del dispositivo lógico de fuente de alimentación.
ms.assetid: a9b79564-01d9-42a4-8586-782f179c179f
ms.tgt_platform: multiple
title: CIM_PowerSupply (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply
- CIM_PowerSupply.ActiveInputVoltage
- CIM_PowerSupply.Availability
- CIM_PowerSupply.Caption
- CIM_PowerSupply.ConfigManagerErrorCode
- CIM_PowerSupply.ConfigManagerUserConfig
- CIM_PowerSupply.CreationClassName
- CIM_PowerSupply.Description
- CIM_PowerSupply.DeviceID
- CIM_PowerSupply.ErrorCleared
- CIM_PowerSupply.ErrorDescription
- CIM_PowerSupply.InstallDate
- CIM_PowerSupply.IsSwitchingSupply
- CIM_PowerSupply.LastErrorCode
- CIM_PowerSupply.Name
- CIM_PowerSupply.PNPDeviceID
- CIM_PowerSupply.PowerManagementCapabilities
- CIM_PowerSupply.PowerManagementSupported
- CIM_PowerSupply.Range1InputFrequencyHigh
- CIM_PowerSupply.Range1InputFrequencyLow
- CIM_PowerSupply.Range1InputVoltageHigh
- CIM_PowerSupply.Range1InputVoltageLow
- CIM_PowerSupply.Range2InputFrequencyHigh
- CIM_PowerSupply.Range2InputFrequencyLow
- CIM_PowerSupply.Range2InputVoltageHigh
- CIM_PowerSupply.Range2InputVoltageLow
- CIM_PowerSupply.Status
- CIM_PowerSupply.StatusInfo
- CIM_PowerSupply.SystemCreationClassName
- CIM_PowerSupply.SystemName
- CIM_PowerSupply.TotalOutputPower
- CIM_PowerSupply.TypeOfRangeSwitching
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35a1eb73c258b800bb8b33ad7aa75ea86cd0ef4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274931"
---
# <a name="cim_powersupply-class"></a><span data-ttu-id="a0581-103">CIM ( \_ clase)</span><span class="sxs-lookup"><span data-stu-id="a0581-103">CIM\_PowerSupply class</span></span>

<span data-ttu-id="a0581-104">La clase de energía **CIM \_** representa las capacidades y la administración del dispositivo lógico de fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="a0581-104">The **CIM\_PowerSupply** class represents the capabilities and management of the power supply logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0581-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a0581-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a0581-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a0581-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a0581-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a0581-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a0581-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a0581-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0581-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0581-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C547-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_PowerSupply : CIM_LogicalDevice
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TotalOutputPower;
  uint16   TypeOfRangeSwitching;
};
```

## <a name="members"></a><span data-ttu-id="a0581-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0581-110">Members</span></span>

<span data-ttu-id="a0581-111">La clase de sistema de sistema **CIM \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a0581-111">The **CIM\_PowerSupply** class has these types of members:</span></span>

-   [<span data-ttu-id="a0581-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0581-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0581-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0581-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0581-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0581-114">Methods</span></span>

<span data-ttu-id="a0581-115">La clase de sistema de sistema **CIM \_** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a0581-115">The **CIM\_PowerSupply** class has these methods.</span></span>



| <span data-ttu-id="a0581-116">Método</span><span class="sxs-lookup"><span data-stu-id="a0581-116">Method</span></span>                                                                 | <span data-ttu-id="a0581-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0581-117">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0581-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a0581-118">**Reset**</span></span>](reset-method-in-class-cim-powersupply.md)                 | <span data-ttu-id="a0581-119">Solicita un restablecimiento del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0581-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="a0581-120">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="a0581-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="a0581-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a0581-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-powersupply.md) | <span data-ttu-id="a0581-122">Define el estado de energía deseado para un dispositivo lógico y cuándo debe colocarse un dispositivo en ese estado.</span><span class="sxs-lookup"><span data-stu-id="a0581-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="a0581-123">No implementado por WMI.</span><span class="sxs-lookup"><span data-stu-id="a0581-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a0581-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0581-124">Properties</span></span>

<span data-ttu-id="a0581-125">La clase de sistema de sistema **CIM \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a0581-125">The **CIM\_PowerSupply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0581-126">**ActiveInputVoltage**</span><span class="sxs-lookup"><span data-stu-id="a0581-126">**ActiveInputVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0581-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,15 ")</span><span class="sxs-lookup"><span data-stu-id="a0581-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.15")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-130">Intervalo de voltaje que está actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="a0581-130">Voltage range that is currently in use.</span></span> <span data-ttu-id="a0581-131">Si el suministro no está dibujando la energía actualmente, se puede especificar el valor 6 ("ninguno").</span><span class="sxs-lookup"><span data-stu-id="a0581-131">If the supply is not currently drawing power, the value 6 ("Neither") can be specified.</span></span> <span data-ttu-id="a0581-132">Esta información es necesaria en el caso de una fuente de alimentación ininterrumpida (SAI), una subclase de energía **CIM \_**.</span><span class="sxs-lookup"><span data-stu-id="a0581-132">This information is necessary in the case of an uninterruptible power supply (UPS), a subclass of **CIM\_PowerSupply**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0581-133">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a0581-133">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0581-134">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a0581-134">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="a0581-135">**Intervalo 1** (3)</span><span class="sxs-lookup"><span data-stu-id="a0581-135">**Range 1** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="a0581-136">**Intervalo 2** (4)</span><span class="sxs-lookup"><span data-stu-id="a0581-136">**Range 2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="a0581-137">**Ambos** (5)</span><span class="sxs-lookup"><span data-stu-id="a0581-137">**Both** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Neither"></span><span id="neither"></span><span id="NEITHER"></span>

<span data-ttu-id="a0581-138">**Ninguno** (6)</span><span class="sxs-lookup"><span data-stu-id="a0581-138">**Neither** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0581-139">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="a0581-139">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0581-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-142">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a0581-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-143">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-143">Availability and status of the device.</span></span>

<span data-ttu-id="a0581-144">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-144">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0581-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a0581-145"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0581-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a0581-146"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a0581-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a0581-147"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-148">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="a0581-148">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a0581-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="a0581-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a0581-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="a0581-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a0581-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="a0581-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a0581-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="a0581-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a0581-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="a0581-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a0581-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="a0581-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a0581-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="a0581-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a0581-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="a0581-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a0581-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="a0581-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a0581-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="a0581-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-159">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="a0581-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a0581-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="a0581-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-161">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="a0581-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a0581-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="a0581-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-163">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="a0581-163">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a0581-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="a0581-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a0581-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="a0581-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-166">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="a0581-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a0581-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a0581-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-168">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="a0581-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a0581-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="a0581-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-170">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="a0581-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a0581-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="a0581-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-172">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="a0581-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a0581-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="a0581-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-174">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="a0581-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0581-175">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a0581-175">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-178">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a0581-178">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-179">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0581-179">Short textual description of the object.</span></span>

<span data-ttu-id="a0581-180">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-181">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a0581-181">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-182">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-184">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0581-184">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-185">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="a0581-185">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a0581-186">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a0581-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="a0581-187"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a0581-188"> (0)</span><span class="sxs-lookup"><span data-stu-id="a0581-188">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-189">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0581-189">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a0581-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="a0581-190"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a0581-191">(1)</span><span class="sxs-lookup"><span data-stu-id="a0581-191">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-192">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0581-192">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0581-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-193"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a0581-194">(2)</span><span class="sxs-lookup"><span data-stu-id="a0581-194">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a0581-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="a0581-195"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a0581-196">(3)</span><span class="sxs-lookup"><span data-stu-id="a0581-196">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-197">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="a0581-197">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a0581-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="a0581-198"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a0581-199">(4)</span><span class="sxs-lookup"><span data-stu-id="a0581-199">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-200">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0581-200">Device is not working properly.</span></span> <span data-ttu-id="a0581-201">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="a0581-201">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a0581-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="a0581-202"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a0581-203">(5)</span><span class="sxs-lookup"><span data-stu-id="a0581-203">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-204">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="a0581-204">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a0581-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="a0581-205"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a0581-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="a0581-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-207">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a0581-207">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a0581-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="a0581-208"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a0581-209">(7)</span><span class="sxs-lookup"><span data-stu-id="a0581-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a0581-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-210"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a0581-211">(8)</span><span class="sxs-lookup"><span data-stu-id="a0581-211">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-212">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-212">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a0581-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="a0581-213"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a0581-214">(9)</span><span class="sxs-lookup"><span data-stu-id="a0581-214">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-215">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0581-215">Device is not working properly.</span></span> <span data-ttu-id="a0581-216">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-216">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a0581-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="a0581-217"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a0581-218">(10)</span><span class="sxs-lookup"><span data-stu-id="a0581-218">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-219">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="a0581-219">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a0581-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-220"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a0581-221">(11)</span><span class="sxs-lookup"><span data-stu-id="a0581-221">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-222">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-222">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a0581-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="a0581-223"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a0581-224">(12)</span><span class="sxs-lookup"><span data-stu-id="a0581-224">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-225">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="a0581-225">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a0581-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-226"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a0581-227">(13)</span><span class="sxs-lookup"><span data-stu-id="a0581-227">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-228">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-228">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a0581-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-229"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a0581-230">(14)</span><span class="sxs-lookup"><span data-stu-id="a0581-230">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-231">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="a0581-231">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a0581-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="a0581-232"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a0581-233">(15)</span><span class="sxs-lookup"><span data-stu-id="a0581-233">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-234">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="a0581-234">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a0581-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-235"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a0581-236">(16)</span><span class="sxs-lookup"><span data-stu-id="a0581-236">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-237">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-237">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a0581-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="a0581-238"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a0581-239">(17)</span><span class="sxs-lookup"><span data-stu-id="a0581-239">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-240">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="a0581-240">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0581-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-241"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a0581-242">(18)</span><span class="sxs-lookup"><span data-stu-id="a0581-242">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-243">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a0581-243">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a0581-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="a0581-244"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a0581-245">(19)</span><span class="sxs-lookup"><span data-stu-id="a0581-245">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a0581-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="a0581-246"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a0581-247">(20)</span><span class="sxs-lookup"><span data-stu-id="a0581-247">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-248">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="a0581-248">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a0581-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-249"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a0581-250">(21)</span><span class="sxs-lookup"><span data-stu-id="a0581-250">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-251">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="a0581-251">System failure.</span></span> <span data-ttu-id="a0581-252">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="a0581-252">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a0581-253">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-253">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a0581-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="a0581-254"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a0581-255">(22)</span><span class="sxs-lookup"><span data-stu-id="a0581-255">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-256">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="a0581-256">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a0581-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="a0581-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a0581-258">(23)</span><span class="sxs-lookup"><span data-stu-id="a0581-258">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-259">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="a0581-259">System failure.</span></span> <span data-ttu-id="a0581-260">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="a0581-260">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a0581-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="a0581-261"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a0581-262">(24)</span><span class="sxs-lookup"><span data-stu-id="a0581-262">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-263">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="a0581-263">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a0581-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-264"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a0581-265">(25)</span><span class="sxs-lookup"><span data-stu-id="a0581-265">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-266">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-266">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a0581-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-267"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a0581-268">(26)</span><span class="sxs-lookup"><span data-stu-id="a0581-268">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-269">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0581-269">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a0581-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="a0581-270"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a0581-271">(27)</span><span class="sxs-lookup"><span data-stu-id="a0581-271">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-272">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="a0581-272">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a0581-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="a0581-273"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a0581-274">(28)</span><span class="sxs-lookup"><span data-stu-id="a0581-274">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-275">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="a0581-275">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a0581-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="a0581-276"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a0581-277">(29)</span><span class="sxs-lookup"><span data-stu-id="a0581-277">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-278">El dispositivo está deshabilitado; el firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a0581-278">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a0581-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="a0581-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a0581-280">(30)</span><span class="sxs-lookup"><span data-stu-id="a0581-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-281">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="a0581-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a0581-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a0581-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a0581-283">31</span><span class="sxs-lookup"><span data-stu-id="a0581-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-284">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a0581-284">Device is not working properly.</span></span> <span data-ttu-id="a0581-285">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a0581-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0581-286">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a0581-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-287">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0581-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-289">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0581-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-290">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a0581-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a0581-291">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a0581-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-295">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0581-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0581-296">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="a0581-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a0581-297">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="a0581-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a0581-298">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-299">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0581-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-302">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="a0581-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-303">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0581-303">Textual description of the object.</span></span>

<span data-ttu-id="a0581-304">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-305">**ID**</span><span class="sxs-lookup"><span data-stu-id="a0581-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-306">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-308">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0581-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0581-309">Dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0581-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="a0581-310">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-311">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a0581-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-312">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0581-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0581-314">Si es **true**, el error que se ha comunicado en la propiedad **LastErrorCode** ahora está desactivado.</span><span class="sxs-lookup"><span data-stu-id="a0581-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="a0581-315">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a0581-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0581-319">Cadena de forma libre que proporciona información sobre el error registrado en la propiedad **LastErrorCode** y las acciones correctivas que se deben realizar.</span><span class="sxs-lookup"><span data-stu-id="a0581-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="a0581-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a0581-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-322">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a0581-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-324">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="a0581-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-325">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a0581-325">Date and time the object was installed.</span></span> <span data-ttu-id="a0581-326">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a0581-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a0581-327">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-328">**IsSwitchingSupply**</span><span class="sxs-lookup"><span data-stu-id="a0581-328">**IsSwitchingSupply**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-329">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0581-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0581-331">Si es **true**, la fuente de alimentación es un suministro de conmutación (frente a lineal).</span><span class="sxs-lookup"><span data-stu-id="a0581-331">If **TRUE**, the power supply is a switching (versus linear) supply.</span></span>

</dd> <dt>

<span data-ttu-id="a0581-332">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a0581-332">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-333">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-333">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0581-335">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0581-335">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a0581-336">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-337">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a0581-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-340">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a0581-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-341">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a0581-341">Label by which the object is known.</span></span> <span data-ttu-id="a0581-342">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="a0581-342">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a0581-343">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a0581-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-345">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-347">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a0581-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-348">Win32 Plug and Play el identificador de dispositivo del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0581-348">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="a0581-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a0581-350">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a0581-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a0581-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a0581-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-352">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0581-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a0581-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0581-354">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0581-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a0581-355">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="a0581-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0581-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a0581-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a0581-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="a0581-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a0581-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="a0581-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a0581-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a0581-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-360">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a0581-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a0581-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a0581-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-362">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="a0581-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a0581-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="a0581-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-364">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="a0581-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a0581-365">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="a0581-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a0581-366">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="a0581-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a0581-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="a0581-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-368">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="a0581-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a0581-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="a0581-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a0581-370">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="a0581-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a0581-371">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a0581-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-372">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a0581-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0581-374">Si **es true**, el dispositivo puede administrarse con energía, es decir, ponerse en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="a0581-374">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="a0581-375">Si **es false**, el valor entero 1 ("no compatible") debe ser la única entrada de la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a0581-375">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="a0581-376">Esta propiedad no indica si las características de administración de energía están habilitadas actualmente o si están habilitadas, qué características se admiten.</span><span class="sxs-lookup"><span data-stu-id="a0581-376">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="a0581-377">Para obtener más información, vea la matriz **PowerManagementCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="a0581-377">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="a0581-378">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-378">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-379">**Range1InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="a0581-379">**Range1InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-380">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-381">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-382">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios")</span><span class="sxs-lookup"><span data-stu-id="a0581-382">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-383">Frecuencia (en hercios) en el extremo superior del intervalo de frecuencia de entrada de la fuente de alimentación 1.</span><span class="sxs-lookup"><span data-stu-id="a0581-383">Frequency (in hertz) at the high-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="a0581-384">Un valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="a0581-384">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="a0581-385">**Range1InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="a0581-385">**Range1InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-386">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-388">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,17 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="a0581-388">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.17"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-389">Frecuencia (en hercios) en el extremo inferior del intervalo de frecuencia de entrada de la fuente de alimentación 1.</span><span class="sxs-lookup"><span data-stu-id="a0581-389">Frequency (in hertz) at the low-end of the power supply's input frequency range 1.</span></span> <span data-ttu-id="a0581-390">Un valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="a0581-390">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="a0581-391">**Range1InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="a0581-391">**Range1InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-392">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-392">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-394">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,8 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="a0581-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-395">Alto voltaje del intervalo de voltaje de entrada 1 para la fuente de alimentación, en milivoltios.</span><span class="sxs-lookup"><span data-stu-id="a0581-395">High voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="a0581-396">Un valor de 0 denota "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a0581-396">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a0581-397">**Range1InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="a0581-397">**Range1InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-398">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-398">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-400">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="a0581-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-401">Voltaje bajo del intervalo de voltaje de entrada 1 para la fuente de alimentación, en milivoltios.</span><span class="sxs-lookup"><span data-stu-id="a0581-401">Low voltage of input voltage range 1 for the power supply, in millivolts.</span></span> <span data-ttu-id="a0581-402">Un valor de 0 denota "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a0581-402">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a0581-403">**Range2InputFrequencyHigh**</span><span class="sxs-lookup"><span data-stu-id="a0581-403">**Range2InputFrequencyHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-404">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-405">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-406">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,20 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="a0581-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.20"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-407">Frecuencia (en hercios) en el extremo superior del intervalo de frecuencia de entrada de la fuente de alimentación 2.</span><span class="sxs-lookup"><span data-stu-id="a0581-407">Frequency (in hertz) at the high-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="a0581-408">Un valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="a0581-408">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="a0581-409">**Range2InputFrequencyLow**</span><span class="sxs-lookup"><span data-stu-id="a0581-409">**Range2InputFrequencyLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-410">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-412">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,19 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="a0581-412">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.19"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-413">Frecuencia (en hercios) en el extremo inferior del intervalo de frecuencia de entrada de la fuente de alimentación 2.</span><span class="sxs-lookup"><span data-stu-id="a0581-413">Frequency (in hertz) at the low-end of the power supply's input frequency range 2.</span></span> <span data-ttu-id="a0581-414">Un valor de 0 implica DC.</span><span class="sxs-lookup"><span data-stu-id="a0581-414">A value of 0 implies DC.</span></span>

</dd> <dt>

<span data-ttu-id="a0581-415">**Range2InputVoltageHigh**</span><span class="sxs-lookup"><span data-stu-id="a0581-415">**Range2InputVoltageHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-416">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-416">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-418">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,12 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="a0581-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.12"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-419">Alto voltaje del intervalo de voltaje de entrada 2 para la fuente de alimentación, en milivoltios.</span><span class="sxs-lookup"><span data-stu-id="a0581-419">High voltage of input voltage range 2 for the power supply, in millivolts.</span></span> <span data-ttu-id="a0581-420">Un valor de 0 denota "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a0581-420">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a0581-421">**Range2InputVoltageLow**</span><span class="sxs-lookup"><span data-stu-id="a0581-421">**Range2InputVoltageLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-422">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-422">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-424">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivoltios ")</span><span class="sxs-lookup"><span data-stu-id="a0581-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("millivolts")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-425">Bajo voltaje del intervalo 2 de voltaje de entrada para esta fuente de alimentación, en milivoltios.</span><span class="sxs-lookup"><span data-stu-id="a0581-425">Low voltage of input voltage range 2 for this power supply, in Millivolts.</span></span> <span data-ttu-id="a0581-426">Un valor de 0 denota "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a0581-426">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a0581-427">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a0581-427">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-430">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a0581-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-431">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a0581-431">Current status of the object.</span></span>

<span data-ttu-id="a0581-432">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a0581-433">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a0581-433">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a0581-434">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="a0581-434">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a0581-435">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a0581-435">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a0581-436">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a0581-436">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0581-437">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="a0581-437">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a0581-438">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a0581-438">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a0581-439">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="a0581-439">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a0581-440">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="a0581-440">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a0581-441">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="a0581-441">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a0581-442">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="a0581-442">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a0581-443">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a0581-443">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a0581-444">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="a0581-444">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a0581-445">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="a0581-445">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0581-446">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a0581-446">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-447">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0581-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-449">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a0581-449">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-450">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a0581-450">State of the logical device.</span></span> <span data-ttu-id="a0581-451">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="a0581-451">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a0581-452">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0581-453">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a0581-453">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0581-454">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a0581-454">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a0581-455">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a0581-455">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a0581-456">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="a0581-456">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a0581-457">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="a0581-457">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a0581-458">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a0581-458">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-459">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-461">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0581-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0581-462">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a0581-462">Scoping system's creation class name.</span></span>

<span data-ttu-id="a0581-463">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a0581-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-465">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0581-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-467">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a0581-467">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a0581-468">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a0581-468">Scoping system's name.</span></span>

<span data-ttu-id="a0581-469">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-469">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0581-470">**TotalOutputPower**</span><span class="sxs-lookup"><span data-stu-id="a0581-470">**TotalOutputPower**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-471">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0581-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-473">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,21 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" milivatios ")</span><span class="sxs-lookup"><span data-stu-id="a0581-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.21"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-474">Potencia de salida total de la fuente de alimentación, en milivatios.</span><span class="sxs-lookup"><span data-stu-id="a0581-474">Total output power of the power supply, in milliwatts.</span></span> <span data-ttu-id="a0581-475">Un valor de 0 denota "Unknown".</span><span class="sxs-lookup"><span data-stu-id="a0581-475">A value of 0 denotes "Unknown".</span></span>

</dd> <dt>

<span data-ttu-id="a0581-476">**TypeOfRangeSwitching**</span><span class="sxs-lookup"><span data-stu-id="a0581-476">**TypeOfRangeSwitching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0581-477">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a0581-477">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a0581-478">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0581-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0581-479">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Fuente de alimentación DMTF \| 002,16 ")</span><span class="sxs-lookup"><span data-stu-id="a0581-479">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Power Supply\|002.16")</span></span>
</dt> </dl>

<span data-ttu-id="a0581-480">Tipo de cambio de intervalo de voltaje de entrada implementado en la fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="a0581-480">Type of input voltage range switching implemented in the power supply.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a0581-481">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a0581-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a0581-482">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a0581-482">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="a0581-483">**Manual** (3)</span><span class="sxs-lookup"><span data-stu-id="a0581-483">**Manual** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Autoswitch"></span><span id="autoswitch"></span><span id="AUTOSWITCH"></span>

<span data-ttu-id="a0581-484">**AutoSwitch** (4)</span><span class="sxs-lookup"><span data-stu-id="a0581-484">**Autoswitch** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Range"></span><span id="wide_range"></span><span id="WIDE_RANGE"></span>

<span data-ttu-id="a0581-485">**Rango amplio** (5)</span><span class="sxs-lookup"><span data-stu-id="a0581-485">**Wide Range** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a0581-486">**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="a0581-486">**Not Applicable** (6)</span></span>


<span data-ttu-id="a0581-487"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a0581-487"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a0581-488">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0581-488">Remarks</span></span>

<span data-ttu-id="a0581-489">La clase de sistema de sistema **CIM \_** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-489">The **CIM\_PowerSupply** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a0581-490">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a0581-490">WMI does not implement this class.</span></span> <span data-ttu-id="a0581-491">En el caso de las clases de WMI derivadas de la sistema **CIM \_**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a0581-491">For WMI classed derived from **CIM\_PowerSupply**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a0581-492">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a0581-492">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a0581-493">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a0581-493">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0581-494">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0581-494">Requirements</span></span>



| <span data-ttu-id="a0581-495">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0581-495">Requirement</span></span> | <span data-ttu-id="a0581-496">Value</span><span class="sxs-lookup"><span data-stu-id="a0581-496">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0581-497">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0581-497">Minimum supported client</span></span><br/> | <span data-ttu-id="a0581-498">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0581-498">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0581-499">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0581-499">Minimum supported server</span></span><br/> | <span data-ttu-id="a0581-500">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0581-500">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0581-501">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a0581-501">Namespace</span></span><br/>                | <span data-ttu-id="a0581-502">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a0581-502">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a0581-503">MOF</span><span class="sxs-lookup"><span data-stu-id="a0581-503">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0581-504"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0581-504"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0581-505">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0581-505">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0581-506"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0581-506"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0581-507">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0581-507">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0581-508">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a0581-508">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

