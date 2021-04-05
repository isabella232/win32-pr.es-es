---
description: La \_ clase WMI HeatPipe de Win32 representa las propiedades de un dispositivo de refrigeración de canalización térmica.
ms.assetid: c6e24cb2-e29a-4cd5-af62-b8e48a5936f9
ms.tgt_platform: multiple
title: Win32_HeatPipe (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_HeatPipe
- Win32_HeatPipe.Reset
- Win32_HeatPipe.SetPowerState
- Win32_HeatPipe.ActiveCooling
- Win32_HeatPipe.Availability
- Win32_HeatPipe.Caption
- Win32_HeatPipe.ConfigManagerErrorCode
- Win32_HeatPipe.ConfigManagerUserConfig
- Win32_HeatPipe.CreationClassName
- Win32_HeatPipe.Description
- Win32_HeatPipe.DeviceID
- Win32_HeatPipe.ErrorCleared
- Win32_HeatPipe.ErrorDescription
- Win32_HeatPipe.InstallDate
- Win32_HeatPipe.LastErrorCode
- Win32_HeatPipe.Name
- Win32_HeatPipe.PNPDeviceID
- Win32_HeatPipe.PowerManagementCapabilities
- Win32_HeatPipe.PowerManagementSupported
- Win32_HeatPipe.Status
- Win32_HeatPipe.StatusInfo
- Win32_HeatPipe.SystemCreationClassName
- Win32_HeatPipe.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f89b8f059a5c80f4d40c70007d8870211e79f93f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080252"
---
# <a name="win32_heatpipe-class"></a><span data-ttu-id="72389-103">\_Clase Win32 HeatPipe</span><span class="sxs-lookup"><span data-stu-id="72389-103">Win32\_HeatPipe class</span></span>

<span data-ttu-id="72389-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ HeatPipe de Win32** representa las propiedades de un dispositivo de refrigeración de canalización térmica.</span><span class="sxs-lookup"><span data-stu-id="72389-104">The **Win32\_HeatPipe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a heat pipe cooling device.</span></span>

<span data-ttu-id="72389-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="72389-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="72389-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72389-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB7-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_HeatPipe : CIM_HeatPipe
{
  boolean  ActiveCooling;
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
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="72389-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="72389-107">Members</span></span>

<span data-ttu-id="72389-108">La **clase \_ HeatPipe de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="72389-108">The **Win32\_HeatPipe** class has these types of members:</span></span>

-   [<span data-ttu-id="72389-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="72389-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="72389-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72389-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="72389-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="72389-111">Methods</span></span>

<span data-ttu-id="72389-112">La clase **Win32 \_ HeatPipe** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="72389-112">The **Win32\_HeatPipe** class has these methods.</span></span>



| <span data-ttu-id="72389-113">Método</span><span class="sxs-lookup"><span data-stu-id="72389-113">Method</span></span>            | <span data-ttu-id="72389-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="72389-114">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72389-115">**Reset**</span><span class="sxs-lookup"><span data-stu-id="72389-115">**Reset**</span></span>         | <span data-ttu-id="72389-116">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72389-116">Not implemented.</span></span> <span data-ttu-id="72389-117">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ HeatPipe**](cim-heatpipe.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="72389-117">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_HeatPipe**](cim-heatpipe.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="72389-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="72389-118">**SetPowerState**</span></span> | <span data-ttu-id="72389-119">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="72389-119">Not implemented.</span></span> <span data-ttu-id="72389-120">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ HeatPipe**](cim-heatpipe.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="72389-120">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_HeatPipe**](cim-heatpipe.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="72389-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72389-121">Properties</span></span>

<span data-ttu-id="72389-122">La **clase \_ HeatPipe de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="72389-122">The **Win32\_HeatPipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72389-123">**ActiveCooling**</span><span class="sxs-lookup"><span data-stu-id="72389-123">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-124">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="72389-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72389-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72389-126">Si **es true**, el dispositivo de enfriamiento proporciona enfriamiento activo no pasivo.</span><span class="sxs-lookup"><span data-stu-id="72389-126">If **TRUE**, the cooling device provides active cooling not passive.</span></span>

<span data-ttu-id="72389-127">Esta propiedad se hereda de [**\_ CoolingDevice CIM**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-127">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-128">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="72389-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72389-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72389-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-131">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="72389-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="72389-132">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-132">Availability and status of the device.</span></span>

<span data-ttu-id="72389-133">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="72389-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="72389-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72389-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="72389-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="72389-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="72389-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="72389-137">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="72389-137">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="72389-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="72389-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="72389-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="72389-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="72389-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="72389-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="72389-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="72389-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="72389-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="72389-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="72389-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="72389-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="72389-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="72389-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="72389-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="72389-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="72389-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="72389-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="72389-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="72389-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="72389-148">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="72389-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="72389-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="72389-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="72389-150">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="72389-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="72389-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="72389-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="72389-152">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="72389-152">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="72389-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="72389-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="72389-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="72389-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="72389-155">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="72389-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="72389-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="72389-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="72389-157">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="72389-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="72389-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="72389-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="72389-159">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="72389-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="72389-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="72389-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="72389-161">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="72389-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="72389-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="72389-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="72389-163">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="72389-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72389-164">**Caption**</span><span class="sxs-lookup"><span data-stu-id="72389-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-167">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="72389-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="72389-168">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="72389-168">Short description of the object a one-line string.</span></span>

<span data-ttu-id="72389-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="72389-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-170">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="72389-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-171">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72389-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72389-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-173">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="72389-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="72389-174">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="72389-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="72389-175">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="72389-176"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="72389-176"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="72389-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="72389-177">(0)</span></span>


</dt> <dd>

<span data-ttu-id="72389-178">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="72389-178">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="72389-179"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="72389-179"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="72389-180">(1)</span><span class="sxs-lookup"><span data-stu-id="72389-180">(1)</span></span>


</dt> <dd>

<span data-ttu-id="72389-181">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="72389-181">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="72389-182"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-182"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="72389-183">(2)</span><span class="sxs-lookup"><span data-stu-id="72389-183">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="72389-184"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="72389-184"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="72389-185">(3)</span><span class="sxs-lookup"><span data-stu-id="72389-185">(3)</span></span>


</dt> <dd>

<span data-ttu-id="72389-186">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="72389-186">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="72389-187"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="72389-187"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="72389-188">(4)</span><span class="sxs-lookup"><span data-stu-id="72389-188">(4)</span></span>


</dt> <dd>

<span data-ttu-id="72389-189">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="72389-189">Device is not working properly.</span></span> <span data-ttu-id="72389-190">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="72389-190">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="72389-191"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="72389-191"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="72389-192">(5)</span><span class="sxs-lookup"><span data-stu-id="72389-192">(5)</span></span>


</dt> <dd>

<span data-ttu-id="72389-193">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="72389-193">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="72389-194"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="72389-194"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="72389-195"> (6)</span><span class="sxs-lookup"><span data-stu-id="72389-195">(6)</span></span>


</dt> <dd>

<span data-ttu-id="72389-196">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="72389-196">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="72389-197"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="72389-197"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="72389-198">(7)</span><span class="sxs-lookup"><span data-stu-id="72389-198">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="72389-199"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-199"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="72389-200">(8)</span><span class="sxs-lookup"><span data-stu-id="72389-200">(8)</span></span>


</dt> <dd>

<span data-ttu-id="72389-201">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-201">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="72389-202"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="72389-202"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="72389-203">(9)</span><span class="sxs-lookup"><span data-stu-id="72389-203">(9)</span></span>


</dt> <dd>

<span data-ttu-id="72389-204">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="72389-204">Device is not working properly.</span></span> <span data-ttu-id="72389-205">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-205">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="72389-206"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="72389-206"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="72389-207">(10)</span><span class="sxs-lookup"><span data-stu-id="72389-207">(10)</span></span>


</dt> <dd>

<span data-ttu-id="72389-208">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="72389-208">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="72389-209"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-209"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="72389-210">(11)</span><span class="sxs-lookup"><span data-stu-id="72389-210">(11)</span></span>


</dt> <dd>

<span data-ttu-id="72389-211">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-211">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="72389-212"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="72389-212"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="72389-213">(12)</span><span class="sxs-lookup"><span data-stu-id="72389-213">(12)</span></span>


</dt> <dd>

<span data-ttu-id="72389-214">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="72389-214">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="72389-215"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-215"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="72389-216">(13)</span><span class="sxs-lookup"><span data-stu-id="72389-216">(13)</span></span>


</dt> <dd>

<span data-ttu-id="72389-217">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-217">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="72389-218"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="72389-218"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="72389-219">(14)</span><span class="sxs-lookup"><span data-stu-id="72389-219">(14)</span></span>


</dt> <dd>

<span data-ttu-id="72389-220">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="72389-220">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="72389-221"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="72389-221"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="72389-222">(15)</span><span class="sxs-lookup"><span data-stu-id="72389-222">(15)</span></span>


</dt> <dd>

<span data-ttu-id="72389-223">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="72389-223">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="72389-224"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-224"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="72389-225">(16)</span><span class="sxs-lookup"><span data-stu-id="72389-225">(16)</span></span>


</dt> <dd>

<span data-ttu-id="72389-226">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-226">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="72389-227"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="72389-227"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="72389-228">(17)</span><span class="sxs-lookup"><span data-stu-id="72389-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="72389-229">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="72389-229">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="72389-230"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-230"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="72389-231">(18)</span><span class="sxs-lookup"><span data-stu-id="72389-231">(18)</span></span>


</dt> <dd>

<span data-ttu-id="72389-232">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="72389-232">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="72389-233"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="72389-233"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="72389-234">(19)</span><span class="sxs-lookup"><span data-stu-id="72389-234">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="72389-235"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="72389-235"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="72389-236">(20)</span><span class="sxs-lookup"><span data-stu-id="72389-236">(20)</span></span>


</dt> <dd>

<span data-ttu-id="72389-237">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="72389-237">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="72389-238"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-238"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="72389-239">(21)</span><span class="sxs-lookup"><span data-stu-id="72389-239">(21)</span></span>


</dt> <dd>

<span data-ttu-id="72389-240">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="72389-240">System failure.</span></span> <span data-ttu-id="72389-241">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="72389-241">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="72389-242">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-242">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="72389-243"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="72389-243"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="72389-244">(22)</span><span class="sxs-lookup"><span data-stu-id="72389-244">(22)</span></span>


</dt> <dd>

<span data-ttu-id="72389-245">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="72389-245">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="72389-246"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="72389-246"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="72389-247">(23)</span><span class="sxs-lookup"><span data-stu-id="72389-247">(23)</span></span>


</dt> <dd>

<span data-ttu-id="72389-248">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="72389-248">System failure.</span></span> <span data-ttu-id="72389-249">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="72389-249">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="72389-250"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="72389-250"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="72389-251">(24)</span><span class="sxs-lookup"><span data-stu-id="72389-251">(24)</span></span>


</dt> <dd>

<span data-ttu-id="72389-252">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="72389-252">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="72389-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="72389-254">(25)</span><span class="sxs-lookup"><span data-stu-id="72389-254">(25)</span></span>


</dt> <dd>

<span data-ttu-id="72389-255">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="72389-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="72389-257">(26)</span><span class="sxs-lookup"><span data-stu-id="72389-257">(26)</span></span>


</dt> <dd>

<span data-ttu-id="72389-258">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="72389-259"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="72389-259"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="72389-260">(27)</span><span class="sxs-lookup"><span data-stu-id="72389-260">(27)</span></span>


</dt> <dd>

<span data-ttu-id="72389-261">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="72389-261">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="72389-262"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="72389-262"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="72389-263">(28)</span><span class="sxs-lookup"><span data-stu-id="72389-263">(28)</span></span>


</dt> <dd>

<span data-ttu-id="72389-264">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="72389-264">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="72389-265"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="72389-265"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="72389-266">(29)</span><span class="sxs-lookup"><span data-stu-id="72389-266">(29)</span></span>


</dt> <dd>

<span data-ttu-id="72389-267">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="72389-267">Device is disabled.</span></span> <span data-ttu-id="72389-268">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="72389-268">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="72389-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="72389-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="72389-270">(30)</span><span class="sxs-lookup"><span data-stu-id="72389-270">(30)</span></span>


</dt> <dd>

<span data-ttu-id="72389-271">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="72389-271">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="72389-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="72389-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="72389-273">31</span><span class="sxs-lookup"><span data-stu-id="72389-273">(31)</span></span>


</dt> <dd>

<span data-ttu-id="72389-274">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="72389-274">Device is not working properly.</span></span> <span data-ttu-id="72389-275">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="72389-275">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72389-276">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="72389-276">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-277">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="72389-277">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72389-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-279">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="72389-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="72389-280">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="72389-280">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="72389-281">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-281">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-282">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="72389-282">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-283">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-285">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="72389-285">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="72389-286">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="72389-286">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="72389-287">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="72389-287">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="72389-288">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-289">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72389-289">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-290">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-292">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="72389-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="72389-293">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="72389-293">Description of the object.</span></span>

<span data-ttu-id="72389-294">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="72389-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-295">**ID**</span><span class="sxs-lookup"><span data-stu-id="72389-295">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-296">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-297">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-298">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="72389-298">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="72389-299">Identificador único de la canalización térmica.</span><span class="sxs-lookup"><span data-stu-id="72389-299">Unique identifier of the heat pipe.</span></span>

<span data-ttu-id="72389-300">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-301">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="72389-301">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-302">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="72389-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72389-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72389-304">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="72389-304">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="72389-305">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-306">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="72389-306">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72389-309">Más información sobre el error que se registra en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="72389-309">More information about the error that is recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="72389-310">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="72389-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-312">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="72389-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="72389-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-314">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="72389-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="72389-315">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="72389-315">Date and time the object was installed.</span></span> <span data-ttu-id="72389-316">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="72389-316">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="72389-317">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="72389-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-318">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="72389-318">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-319">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72389-319">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72389-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72389-321">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="72389-321">Last error code reported by the logical device.</span></span>

<span data-ttu-id="72389-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-323">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="72389-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-326">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="72389-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="72389-327">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="72389-327">Label by which the object is known.</span></span> <span data-ttu-id="72389-328">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="72389-328">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="72389-329">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="72389-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-330">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="72389-330">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-331">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-333">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="72389-333">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="72389-334">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="72389-334">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="72389-335">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="72389-336">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="72389-336">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="72389-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="72389-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-338">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72389-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="72389-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72389-340">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="72389-340">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="72389-341">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="72389-341">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72389-342"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="72389-342"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="72389-343"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="72389-343"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="72389-344">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72389-344">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="72389-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="72389-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="72389-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="72389-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="72389-347">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="72389-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="72389-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="72389-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="72389-349">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="72389-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="72389-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="72389-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="72389-351">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="72389-351">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="72389-352">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="72389-352">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="72389-353">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="72389-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="72389-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="72389-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="72389-355">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="72389-355">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="72389-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="72389-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="72389-357">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="72389-357">Timed Power-On Supported</span></span>

<span data-ttu-id="72389-358">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="72389-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="72389-359">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="72389-359">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-360">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="72389-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72389-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72389-362">Si **es true**, el dispositivo puede administrarse con energía en modo de suspensión, etc.</span><span class="sxs-lookup"><span data-stu-id="72389-362">If **TRUE**, the device can be power-managed put into suspend mode, and so on.</span></span> <span data-ttu-id="72389-363">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="72389-363">The property does not indicate that power management features are enabled currently, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="72389-364">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-365">**Estado**</span><span class="sxs-lookup"><span data-stu-id="72389-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-366">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-368">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="72389-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="72389-369">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="72389-369">Current status of the object.</span></span> <span data-ttu-id="72389-370">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="72389-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="72389-371">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="72389-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="72389-372">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="72389-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="72389-373">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="72389-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="72389-374">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="72389-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="72389-375">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="72389-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="72389-376">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="72389-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="72389-377">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="72389-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="72389-378">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="72389-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="72389-379">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="72389-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72389-380">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="72389-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="72389-381">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="72389-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="72389-382">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="72389-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="72389-383">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="72389-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="72389-384">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="72389-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="72389-385">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="72389-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="72389-386">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="72389-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="72389-387">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="72389-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="72389-388">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="72389-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="72389-389">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="72389-389">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-390">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72389-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72389-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-392">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="72389-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="72389-393">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="72389-393">State of the logical device.</span></span> <span data-ttu-id="72389-394">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="72389-394">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="72389-395">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-395">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="72389-396">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="72389-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72389-397">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="72389-397">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="72389-398">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="72389-398">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="72389-399">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="72389-399">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="72389-400">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="72389-400">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="72389-401">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="72389-401">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-402">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-404">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="72389-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="72389-405">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="72389-405">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="72389-406">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="72389-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="72389-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72389-408">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72389-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72389-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72389-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72389-410">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="72389-410">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="72389-411">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="72389-411">Name of the scoping system.</span></span>

<span data-ttu-id="72389-412">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="72389-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72389-413">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72389-413">Remarks</span></span>

<span data-ttu-id="72389-414">La **clase \_ HeatPipe de Win32** se deriva de [**\_ HeatPipe de CIM**](cim-heatpipe.md).</span><span class="sxs-lookup"><span data-stu-id="72389-414">The **Win32\_HeatPipe** class is derived from [**CIM\_HeatPipe**](cim-heatpipe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72389-415">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72389-415">Requirements</span></span>



| <span data-ttu-id="72389-416">Requisito</span><span class="sxs-lookup"><span data-stu-id="72389-416">Requirement</span></span> | <span data-ttu-id="72389-417">Value</span><span class="sxs-lookup"><span data-stu-id="72389-417">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72389-418">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72389-418">Minimum supported client</span></span><br/> | <span data-ttu-id="72389-419">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72389-419">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72389-420">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72389-420">Minimum supported server</span></span><br/> | <span data-ttu-id="72389-421">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72389-421">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72389-422">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72389-422">Namespace</span></span><br/>                | <span data-ttu-id="72389-423">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="72389-423">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72389-424">MOF</span><span class="sxs-lookup"><span data-stu-id="72389-424">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72389-425"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72389-425"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72389-426">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72389-426">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72389-427"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72389-427"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72389-428">Vea también</span><span class="sxs-lookup"><span data-stu-id="72389-428">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72389-429">**\_HEATPIPE CIM**</span><span class="sxs-lookup"><span data-stu-id="72389-429">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dt>

[<span data-ttu-id="72389-430">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="72389-430">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

