---
description: Win32 \_ ParallelPort &\# 32; La clase WMI representa las propiedades de un puerto paralelo de un equipo que ejecuta Windows.
ms.assetid: 986bd27f-71b0-4a40-a421-a8bfc0f081be
ms.tgt_platform: multiple
title: Win32_ParallelPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ParallelPort
- Win32_ParallelPort.Reset
- Win32_ParallelPort.SetPowerState
- Win32_ParallelPort.Availability
- Win32_ParallelPort.Capabilities
- Win32_ParallelPort.CapabilityDescriptions
- Win32_ParallelPort.Caption
- Win32_ParallelPort.ConfigManagerErrorCode
- Win32_ParallelPort.ConfigManagerUserConfig
- Win32_ParallelPort.CreationClassName
- Win32_ParallelPort.Description
- Win32_ParallelPort.DeviceID
- Win32_ParallelPort.DMASupport
- Win32_ParallelPort.ErrorCleared
- Win32_ParallelPort.ErrorDescription
- Win32_ParallelPort.InstallDate
- Win32_ParallelPort.LastErrorCode
- Win32_ParallelPort.MaxNumberControlled
- Win32_ParallelPort.Name
- Win32_ParallelPort.OSAutoDiscovered
- Win32_ParallelPort.PNPDeviceID
- Win32_ParallelPort.PowerManagementCapabilities
- Win32_ParallelPort.PowerManagementSupported
- Win32_ParallelPort.ProtocolSupported
- Win32_ParallelPort.Status
- Win32_ParallelPort.StatusInfo
- Win32_ParallelPort.SystemCreationClassName
- Win32_ParallelPort.SystemName
- Win32_ParallelPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: da2ed3b34f3655067fd5ae41c31424e7599789c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153415"
---
# <a name="win32_parallelport-class"></a><span data-ttu-id="8812e-103">\_Clase Win32 ParallelPort</span><span class="sxs-lookup"><span data-stu-id="8812e-103">Win32\_ParallelPort class</span></span>

<span data-ttu-id="8812e-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ ParallelPort de Win32** representa las propiedades de un puerto paralelo en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="8812e-104">The **Win32\_ParallelPort** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a parallel port on a computer system running Windows.</span></span>

<span data-ttu-id="8812e-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8812e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8812e-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8812e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8812e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8812e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class  Win32_ParallelPort : CIM_ParallelController
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  DMASupport;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="8812e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8812e-108">Members</span></span>

<span data-ttu-id="8812e-109">La **clase \_ ParallelPort de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8812e-109">The **Win32\_ParallelPort** class has these types of members:</span></span>

-   [<span data-ttu-id="8812e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8812e-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="8812e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8812e-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8812e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8812e-112">Methods</span></span>

<span data-ttu-id="8812e-113">La clase **Win32 \_ ParallelPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8812e-113">The **Win32\_ParallelPort** class has these methods.</span></span>



| <span data-ttu-id="8812e-114">Método</span><span class="sxs-lookup"><span data-stu-id="8812e-114">Method</span></span>            | <span data-ttu-id="8812e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="8812e-115">Description</span></span>                                                                                                                                                                                              |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8812e-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="8812e-116">**Reset**</span></span>         | <span data-ttu-id="8812e-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="8812e-117">Not implemented.</span></span> <span data-ttu-id="8812e-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="8812e-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8812e-119">**SetPowerState**</span></span> | <span data-ttu-id="8812e-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="8812e-120">Not implemented.</span></span> <span data-ttu-id="8812e-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ ParallelController**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8812e-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8812e-122">Properties</span></span>

<span data-ttu-id="8812e-123">La **clase \_ ParallelPort de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8812e-123">The **Win32\_ParallelPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8812e-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="8812e-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8812e-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-127">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="8812e-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-128">Availability and status of the device.</span></span>

<span data-ttu-id="8812e-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8812e-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8812e-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8812e-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8812e-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8812e-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="8812e-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="8812e-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8812e-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="8812e-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8812e-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="8812e-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8812e-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="8812e-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8812e-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="8812e-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8812e-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="8812e-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8812e-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="8812e-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8812e-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="8812e-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8812e-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="8812e-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8812e-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="8812e-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8812e-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="8812e-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="8812e-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8812e-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="8812e-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="8812e-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8812e-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="8812e-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="8812e-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8812e-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="8812e-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8812e-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="8812e-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="8812e-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8812e-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="8812e-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="8812e-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8812e-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="8812e-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="8812e-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8812e-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="8812e-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="8812e-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8812e-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="8812e-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="8812e-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8812e-160">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8812e-160">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-161">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8812e-161">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8812e-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-163">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puertos paralelos \| de DMTF 003,8 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="8812e-163">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.8"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-164">Matriz de las capacidades del controlador paralelo.</span><span class="sxs-lookup"><span data-stu-id="8812e-164">Array of the capabilities of the parallel controller.</span></span>

<span data-ttu-id="8812e-165">Esta propiedad se hereda de [**\_ ParallelController CIM**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-165">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8812e-166">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8812e-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8812e-167">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8812e-167">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="8812e-168">**XT/at compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="8812e-168">**XT/AT Compatible** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2_Compatible"></span><span id="ps_2_compatible"></span><span id="PS_2_COMPATIBLE"></span>

<span data-ttu-id="8812e-169">**Compatible con PS/2** (3)</span><span class="sxs-lookup"><span data-stu-id="8812e-169">**PS/2 Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ECP"></span><span id="ecp"></span>

<span data-ttu-id="8812e-170">**ECP** (4)</span><span class="sxs-lookup"><span data-stu-id="8812e-170">**ECP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EPP"></span><span id="epp"></span>

<span data-ttu-id="8812e-171">**EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="8812e-171">**EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="8812e-172">**PC-98** (6)</span><span class="sxs-lookup"><span data-stu-id="8812e-172">**PC-98** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="8812e-173">**PC-98-Hireso** (7)</span><span class="sxs-lookup"><span data-stu-id="8812e-173">**PC-98-Hireso** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="8812e-174">**PC-H98** (8)</span><span class="sxs-lookup"><span data-stu-id="8812e-174">**PC-H98** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8812e-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8812e-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-176">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8812e-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8812e-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-178">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ParallelController**](cim-parallelcontroller.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="8812e-178">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ParallelController**](cim-parallelcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-179">Matriz de explicaciones más detalladas para cualquiera de las características del controlador paralelo indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="8812e-179">Array of more detailed explanations for any of the parallel controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="8812e-180">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="8812e-180">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="8812e-181">Esta propiedad se hereda de [**\_ ParallelController CIM**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-181">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-182">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8812e-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-185">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8812e-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-186">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="8812e-186">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="8812e-187">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-188">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8812e-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-189">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8812e-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-191">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8812e-191">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-192">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="8812e-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="8812e-193">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8812e-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="8812e-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8812e-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="8812e-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-196">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="8812e-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8812e-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="8812e-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8812e-198">(1)</span><span class="sxs-lookup"><span data-stu-id="8812e-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-199">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8812e-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8812e-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8812e-201">(2)</span><span class="sxs-lookup"><span data-stu-id="8812e-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8812e-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="8812e-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8812e-203">(3)</span><span class="sxs-lookup"><span data-stu-id="8812e-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-204">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="8812e-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8812e-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="8812e-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8812e-206">(4)</span><span class="sxs-lookup"><span data-stu-id="8812e-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-207">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="8812e-207">Device is not working properly.</span></span> <span data-ttu-id="8812e-208">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="8812e-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8812e-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="8812e-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8812e-210">(5)</span><span class="sxs-lookup"><span data-stu-id="8812e-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-211">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="8812e-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8812e-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="8812e-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8812e-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="8812e-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-214">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8812e-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8812e-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="8812e-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8812e-216">(7)</span><span class="sxs-lookup"><span data-stu-id="8812e-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8812e-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8812e-218">(8)</span><span class="sxs-lookup"><span data-stu-id="8812e-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-219">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8812e-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="8812e-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8812e-221">(9)</span><span class="sxs-lookup"><span data-stu-id="8812e-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-222">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="8812e-222">Device is not working properly.</span></span> <span data-ttu-id="8812e-223">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8812e-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="8812e-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8812e-225">(10)</span><span class="sxs-lookup"><span data-stu-id="8812e-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-226">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="8812e-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8812e-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8812e-228">(11)</span><span class="sxs-lookup"><span data-stu-id="8812e-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-229">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8812e-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="8812e-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8812e-231">(12)</span><span class="sxs-lookup"><span data-stu-id="8812e-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-232">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="8812e-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8812e-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8812e-234">(13)</span><span class="sxs-lookup"><span data-stu-id="8812e-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-235">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8812e-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8812e-237">(14)</span><span class="sxs-lookup"><span data-stu-id="8812e-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-238">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="8812e-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8812e-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="8812e-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8812e-240">(15)</span><span class="sxs-lookup"><span data-stu-id="8812e-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-241">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="8812e-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8812e-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8812e-243">(16)</span><span class="sxs-lookup"><span data-stu-id="8812e-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-244">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8812e-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="8812e-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8812e-246">(17)</span><span class="sxs-lookup"><span data-stu-id="8812e-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-247">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="8812e-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8812e-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8812e-249">(18)</span><span class="sxs-lookup"><span data-stu-id="8812e-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-250">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="8812e-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8812e-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="8812e-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8812e-252">(19)</span><span class="sxs-lookup"><span data-stu-id="8812e-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8812e-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="8812e-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8812e-254">(20)</span><span class="sxs-lookup"><span data-stu-id="8812e-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-255">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="8812e-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8812e-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8812e-257">(21)</span><span class="sxs-lookup"><span data-stu-id="8812e-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-258">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="8812e-258">System failure.</span></span> <span data-ttu-id="8812e-259">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="8812e-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8812e-260">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8812e-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="8812e-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8812e-262">(22)</span><span class="sxs-lookup"><span data-stu-id="8812e-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-263">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8812e-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8812e-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="8812e-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8812e-265">(23)</span><span class="sxs-lookup"><span data-stu-id="8812e-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-266">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="8812e-266">System failure.</span></span> <span data-ttu-id="8812e-267">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="8812e-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8812e-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="8812e-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8812e-269">(24)</span><span class="sxs-lookup"><span data-stu-id="8812e-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-270">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="8812e-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8812e-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8812e-272">(25)</span><span class="sxs-lookup"><span data-stu-id="8812e-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-273">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8812e-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8812e-275">(26)</span><span class="sxs-lookup"><span data-stu-id="8812e-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-276">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8812e-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8812e-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="8812e-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8812e-278">(27)</span><span class="sxs-lookup"><span data-stu-id="8812e-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-279">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="8812e-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8812e-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="8812e-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8812e-281">(28)</span><span class="sxs-lookup"><span data-stu-id="8812e-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-282">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="8812e-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8812e-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="8812e-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8812e-284">(29)</span><span class="sxs-lookup"><span data-stu-id="8812e-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-285">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8812e-285">Device is disabled.</span></span> <span data-ttu-id="8812e-286">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="8812e-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8812e-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="8812e-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8812e-288">(30)</span><span class="sxs-lookup"><span data-stu-id="8812e-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-289">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="8812e-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8812e-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="8812e-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8812e-291">31</span><span class="sxs-lookup"><span data-stu-id="8812e-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-292">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="8812e-292">Device is not working properly.</span></span> <span data-ttu-id="8812e-293">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="8812e-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8812e-294">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="8812e-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-295">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8812e-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-297">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8812e-297">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-298">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8812e-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8812e-299">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8812e-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-303">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8812e-303">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8812e-304">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="8812e-304">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="8812e-305">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="8812e-305">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="8812e-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-307">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8812e-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-310">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="8812e-310">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-311">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8812e-311">Description of the object.</span></span>

<span data-ttu-id="8812e-312">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-313">**ID**</span><span class="sxs-lookup"><span data-stu-id="8812e-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-314">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-316">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8812e-316">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-317">Identificador del puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="8812e-317">Identifier of the parallel port.</span></span>

<span data-ttu-id="8812e-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-319">**DMASupport**</span><span class="sxs-lookup"><span data-stu-id="8812e-319">**DMASupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-320">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8812e-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-322">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puertos paralelos de DMTF \| 003,7 ")</span><span class="sxs-lookup"><span data-stu-id="8812e-322">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Parallel Ports\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-323">Si **es true**, el puerto paralelo admite DMA.</span><span class="sxs-lookup"><span data-stu-id="8812e-323">If **TRUE**, the parallel port supports DMA.</span></span>

<span data-ttu-id="8812e-324">Esta propiedad se hereda de [**\_ ParallelController CIM**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-324">This property is inherited from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-325">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8812e-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-326">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8812e-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8812e-328">Si es **true**, el error comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="8812e-328">If **TRUE**, the error reported in **LastErrorCode** is cleared.</span></span>

<span data-ttu-id="8812e-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8812e-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8812e-333">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="8812e-333">More information about the error recorded in **LastErrorCode**, and information about corrective actions that might be taken.</span></span>

<span data-ttu-id="8812e-334">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8812e-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-336">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8812e-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-338">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="8812e-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-339">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="8812e-339">Date and time the object was installed.</span></span> <span data-ttu-id="8812e-340">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="8812e-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8812e-341">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8812e-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-343">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8812e-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8812e-345">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8812e-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8812e-346">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-347">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="8812e-347">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-348">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8812e-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-350">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="8812e-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-351">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="8812e-351">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="8812e-352">Se debe utilizar un valor de 0 (cero) si se desconoce el número.</span><span class="sxs-lookup"><span data-stu-id="8812e-352">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="8812e-353">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-353">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-354">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8812e-354">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-355">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-357">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8812e-357">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-358">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="8812e-358">Label by which the object is known.</span></span> <span data-ttu-id="8812e-359">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="8812e-359">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="8812e-360">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-360">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-361">**OSAutoDiscovered**</span><span class="sxs-lookup"><span data-stu-id="8812e-361">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-362">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8812e-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-364">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="8812e-364">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-365">Si **es true**, el sistema operativo detecta automáticamente el puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="8812e-365">If **TRUE**, the parallel port was automatically detected by the operating system.</span></span> <span data-ttu-id="8812e-366">Si **es false**, el puerto fue detectado por otros medios (por ejemplo, se ha agregado manualmente a través del panel de control).</span><span class="sxs-lookup"><span data-stu-id="8812e-366">If **FALSE**, the port was detected by other means (such as being manually added through the Control Panel).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-367">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8812e-367">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-368">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-370">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8812e-370">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-371">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8812e-371">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="8812e-372">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8812e-373">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="8812e-373">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="8812e-374">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8812e-374">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-375">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8812e-375">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8812e-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8812e-377">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8812e-377">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8812e-378">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="8812e-378">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8812e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8812e-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8812e-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="8812e-380"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8812e-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="8812e-381"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8812e-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8812e-382"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-383">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="8812e-383">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8812e-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="8812e-384"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-385">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="8812e-385">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8812e-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="8812e-386"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-387">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="8812e-387">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8812e-388">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="8812e-388">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="8812e-389">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-389">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8812e-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="8812e-390"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-391">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="8812e-391">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8812e-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="8812e-392"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8812e-393">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="8812e-393">Timed Power-On Supported</span></span>

<span data-ttu-id="8812e-394">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="8812e-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8812e-395">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8812e-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-396">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8812e-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8812e-398">Si **es true**, el dispositivo puede administrarse mediante energía, lo que significa que se puede poner en modo de suspensión, etc.</span><span class="sxs-lookup"><span data-stu-id="8812e-398">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="8812e-399">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="8812e-399">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="8812e-400">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-401">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="8812e-401">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-402">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8812e-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-404">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8812e-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-405">Protocolo usado por el controlador para tener acceso a dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="8812e-405">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="8812e-406">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-406">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="8812e-407">Los valores se muestran en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="8812e-407">Values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8812e-408">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8812e-408">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8812e-409">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8812e-409">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="8812e-410">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="8812e-410">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="8812e-411">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="8812e-411">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="8812e-412">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="8812e-412">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="8812e-413">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="8812e-413">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="8812e-414">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="8812e-414">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="8812e-415">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="8812e-415">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="8812e-416">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="8812e-416">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="8812e-417">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="8812e-417">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="8812e-418">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="8812e-418">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="8812e-419">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="8812e-419">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="8812e-420">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="8812e-420">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="8812e-421">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="8812e-421">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="8812e-422">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="8812e-422">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="8812e-423">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="8812e-423">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="8812e-424">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="8812e-424">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="8812e-425">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="8812e-425">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="8812e-426">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="8812e-426">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="8812e-427">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="8812e-427">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="8812e-428">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="8812e-428">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="8812e-429">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="8812e-429">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="8812e-430">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="8812e-430">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="8812e-431">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="8812e-431">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="8812e-432">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="8812e-432">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="8812e-433">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="8812e-433">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="8812e-434">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="8812e-434">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="8812e-435">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="8812e-435">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="8812e-436">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="8812e-436">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="8812e-437">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="8812e-437">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="8812e-438">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="8812e-438">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="8812e-439">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="8812e-439">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="8812e-440">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="8812e-440">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="8812e-441">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="8812e-441">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="8812e-442">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="8812e-442">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="8812e-443">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="8812e-443">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="8812e-444">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="8812e-444">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="8812e-445">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="8812e-445">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="8812e-446">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="8812e-446">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="8812e-447">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="8812e-447">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="8812e-448">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="8812e-448">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="8812e-449">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="8812e-449">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="8812e-450">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="8812e-450">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="8812e-451">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="8812e-451">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="8812e-452">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="8812e-452">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="8812e-453">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="8812e-453">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="8812e-454">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="8812e-454">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8812e-455">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8812e-455">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-456">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-458">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="8812e-458">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-459">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8812e-459">Current status of the object.</span></span> <span data-ttu-id="8812e-460">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="8812e-460">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8812e-461">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8812e-461">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8812e-462">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="8812e-462">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8812e-463">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="8812e-463">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8812e-464">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="8812e-464">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8812e-465">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8812e-466">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8812e-466">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8812e-467">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="8812e-467">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8812e-468">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="8812e-468">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8812e-469">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8812e-469">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8812e-470">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="8812e-470">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8812e-471">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="8812e-471">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8812e-472">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="8812e-472">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8812e-473">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="8812e-473">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8812e-474">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="8812e-474">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8812e-475">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="8812e-475">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8812e-476">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8812e-476">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8812e-477">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="8812e-477">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8812e-478">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="8812e-478">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8812e-479">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8812e-479">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-480">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8812e-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-482">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8812e-482">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8812e-483">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8812e-483">State of the logical device.</span></span> <span data-ttu-id="8812e-484">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="8812e-484">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8812e-485">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8812e-486">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8812e-486">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8812e-487">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="8812e-487">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8812e-488">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="8812e-488">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8812e-489">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="8812e-489">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8812e-490">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="8812e-490">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8812e-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8812e-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-492">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-493">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-494">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8812e-494">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8812e-495">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8812e-495">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="8812e-496">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-496">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-497">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8812e-497">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-498">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8812e-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8812e-500">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8812e-500">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8812e-501">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8812e-501">Name of the scoping system.</span></span>

<span data-ttu-id="8812e-502">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8812e-503">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="8812e-503">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8812e-504">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8812e-504">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8812e-505">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8812e-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8812e-506">Fecha y hora de la última vez que se restableció el controlador.</span><span class="sxs-lookup"><span data-stu-id="8812e-506">Date and time the controller was last reset.</span></span> <span data-ttu-id="8812e-507">Esto podría significar que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="8812e-507">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="8812e-508">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-508">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8812e-509">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8812e-509">Remarks</span></span>

<span data-ttu-id="8812e-510">La **clase \_ ParallelPort de Win32** se deriva de [**\_ ParallelController de CIM**](cim-parallelcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="8812e-510">The **Win32\_ParallelPort** class is derived from [**CIM\_ParallelController**](cim-parallelcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8812e-511">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8812e-511">Requirements</span></span>



| <span data-ttu-id="8812e-512">Requisito</span><span class="sxs-lookup"><span data-stu-id="8812e-512">Requirement</span></span> | <span data-ttu-id="8812e-513">Value</span><span class="sxs-lookup"><span data-stu-id="8812e-513">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8812e-514">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8812e-514">Minimum supported client</span></span><br/> | <span data-ttu-id="8812e-515">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8812e-515">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8812e-516">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8812e-516">Minimum supported server</span></span><br/> | <span data-ttu-id="8812e-517">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8812e-517">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8812e-518">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8812e-518">Namespace</span></span><br/>                | <span data-ttu-id="8812e-519">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8812e-519">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8812e-520">MOF</span><span class="sxs-lookup"><span data-stu-id="8812e-520">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8812e-521"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8812e-521"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8812e-522">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8812e-522">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8812e-523"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8812e-523"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8812e-524">Vea también</span><span class="sxs-lookup"><span data-stu-id="8812e-524">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8812e-525">**\_PARALLELCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="8812e-525">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dt>

[<span data-ttu-id="8812e-526">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="8812e-526">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
