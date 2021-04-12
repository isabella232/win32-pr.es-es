---
description: La \_ clase WMI InfraredDevice de Win32 representa las capacidades y la administración de un dispositivo de infrarrojos.
ms.assetid: f129e7ce-4d50-44d0-877c-968f4865b781
ms.tgt_platform: multiple
title: Win32_InfraredDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_InfraredDevice
- Win32_InfraredDevice.Reset
- Win32_InfraredDevice.SetPowerState
- Win32_InfraredDevice.Availability
- Win32_InfraredDevice.Caption
- Win32_InfraredDevice.ConfigManagerErrorCode
- Win32_InfraredDevice.ConfigManagerUserConfig
- Win32_InfraredDevice.CreationClassName
- Win32_InfraredDevice.Description
- Win32_InfraredDevice.DeviceID
- Win32_InfraredDevice.ErrorCleared
- Win32_InfraredDevice.ErrorDescription
- Win32_InfraredDevice.InstallDate
- Win32_InfraredDevice.LastErrorCode
- Win32_InfraredDevice.Manufacturer
- Win32_InfraredDevice.MaxNumberControlled
- Win32_InfraredDevice.Name
- Win32_InfraredDevice.PNPDeviceID
- Win32_InfraredDevice.PowerManagementCapabilities
- Win32_InfraredDevice.PowerManagementSupported
- Win32_InfraredDevice.ProtocolSupported
- Win32_InfraredDevice.Status
- Win32_InfraredDevice.StatusInfo
- Win32_InfraredDevice.SystemCreationClassName
- Win32_InfraredDevice.SystemName
- Win32_InfraredDevice.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a71946eeda3a8c304e1a6dda0ab2cc92e7b4489
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152915"
---
# <a name="win32_infrareddevice-class"></a><span data-ttu-id="5382b-103">\_Clase Win32 InfraredDevice</span><span class="sxs-lookup"><span data-stu-id="5382b-103">Win32\_InfraredDevice class</span></span>

<span data-ttu-id="5382b-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ InfraredDevice de Win32** representa las capacidades y la administración de un dispositivo de infrarrojos.</span><span class="sxs-lookup"><span data-stu-id="5382b-104">The **Win32\_InfraredDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management of an infrared device.</span></span>

<span data-ttu-id="5382b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5382b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5382b-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5382b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5382b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5382b-107">Syntax</span></span>

``` syntax
[dynamic, provider("CIMWin32"), UUID("{67F74295-BA42-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_InfraredDevice : CIM_InfraredController
{
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
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
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

## <a name="members"></a><span data-ttu-id="5382b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5382b-108">Members</span></span>

<span data-ttu-id="5382b-109">La **clase \_ InfraredDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5382b-109">The **Win32\_InfraredDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="5382b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5382b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5382b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5382b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5382b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="5382b-112">Methods</span></span>

<span data-ttu-id="5382b-113">La clase **Win32 \_ InfraredDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5382b-113">The **Win32\_InfraredDevice** class has these methods.</span></span>



| <span data-ttu-id="5382b-114">Método</span><span class="sxs-lookup"><span data-stu-id="5382b-114">Method</span></span>            | <span data-ttu-id="5382b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5382b-115">Description</span></span>                                                                                                                                                                                                                |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5382b-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5382b-116">**Reset**</span></span>         | <span data-ttu-id="5382b-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="5382b-117">Not implemented.</span></span> <span data-ttu-id="5382b-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ InfraredController**](cim-infraredcontroller.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="5382b-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_InfraredController**](cim-infraredcontroller.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="5382b-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5382b-119">**SetPowerState**</span></span> | <span data-ttu-id="5382b-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="5382b-120">Not implemented.</span></span> <span data-ttu-id="5382b-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ InfraredController**](cim-infraredcontroller.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="5382b-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_InfraredController**](cim-infraredcontroller.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5382b-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5382b-122">Properties</span></span>

<span data-ttu-id="5382b-123">La **clase \_ InfraredDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5382b-123">The **Win32\_InfraredDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5382b-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="5382b-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5382b-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-127">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="5382b-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-128">Availability and status of the device.</span></span>

<span data-ttu-id="5382b-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5382b-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5382b-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5382b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5382b-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="5382b-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="5382b-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="5382b-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="5382b-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="5382b-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="5382b-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="5382b-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5382b-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="5382b-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="5382b-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="5382b-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="5382b-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="5382b-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="5382b-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="5382b-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5382b-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="5382b-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="5382b-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="5382b-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="5382b-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="5382b-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="5382b-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="5382b-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="5382b-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="5382b-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="5382b-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="5382b-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="5382b-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="5382b-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="5382b-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="5382b-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="5382b-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="5382b-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="5382b-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="5382b-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="5382b-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="5382b-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="5382b-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="5382b-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="5382b-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="5382b-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="5382b-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="5382b-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="5382b-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="5382b-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="5382b-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="5382b-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5382b-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5382b-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-163">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5382b-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-164">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="5382b-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="5382b-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5382b-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5382b-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-169">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5382b-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-170">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="5382b-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="5382b-171">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="5382b-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5382b-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="5382b-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="5382b-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-174">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5382b-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="5382b-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="5382b-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="5382b-176">(1)</span><span class="sxs-lookup"><span data-stu-id="5382b-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-177">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5382b-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5382b-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="5382b-179">(2)</span><span class="sxs-lookup"><span data-stu-id="5382b-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="5382b-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="5382b-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="5382b-181">(3)</span><span class="sxs-lookup"><span data-stu-id="5382b-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-182">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="5382b-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5382b-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="5382b-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="5382b-184">(4)</span><span class="sxs-lookup"><span data-stu-id="5382b-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-185">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5382b-185">Device is not working properly.</span></span> <span data-ttu-id="5382b-186">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="5382b-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="5382b-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="5382b-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="5382b-188">(5)</span><span class="sxs-lookup"><span data-stu-id="5382b-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-189">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="5382b-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="5382b-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="5382b-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="5382b-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="5382b-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-192">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5382b-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="5382b-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="5382b-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="5382b-194">(7)</span><span class="sxs-lookup"><span data-stu-id="5382b-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="5382b-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="5382b-196">(8)</span><span class="sxs-lookup"><span data-stu-id="5382b-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-197">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="5382b-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="5382b-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="5382b-199">(9)</span><span class="sxs-lookup"><span data-stu-id="5382b-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-200">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5382b-200">Device is not working properly.</span></span> <span data-ttu-id="5382b-201">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="5382b-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="5382b-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="5382b-203">(10)</span><span class="sxs-lookup"><span data-stu-id="5382b-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-204">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="5382b-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="5382b-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="5382b-206">(11)</span><span class="sxs-lookup"><span data-stu-id="5382b-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-207">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="5382b-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="5382b-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="5382b-209">(12)</span><span class="sxs-lookup"><span data-stu-id="5382b-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-210">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="5382b-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="5382b-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="5382b-212">(13)</span><span class="sxs-lookup"><span data-stu-id="5382b-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-213">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="5382b-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="5382b-215">(14)</span><span class="sxs-lookup"><span data-stu-id="5382b-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-216">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="5382b-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="5382b-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="5382b-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="5382b-218">(15)</span><span class="sxs-lookup"><span data-stu-id="5382b-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-219">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="5382b-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="5382b-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="5382b-221">(16)</span><span class="sxs-lookup"><span data-stu-id="5382b-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-222">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="5382b-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="5382b-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="5382b-224">(17)</span><span class="sxs-lookup"><span data-stu-id="5382b-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-225">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="5382b-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5382b-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="5382b-227">(18)</span><span class="sxs-lookup"><span data-stu-id="5382b-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-228">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5382b-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="5382b-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="5382b-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="5382b-230">(19)</span><span class="sxs-lookup"><span data-stu-id="5382b-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="5382b-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="5382b-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="5382b-232">(20)</span><span class="sxs-lookup"><span data-stu-id="5382b-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-233">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="5382b-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="5382b-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="5382b-235">(21)</span><span class="sxs-lookup"><span data-stu-id="5382b-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-236">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="5382b-236">System failure.</span></span> <span data-ttu-id="5382b-237">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="5382b-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="5382b-238">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="5382b-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="5382b-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="5382b-240">(22)</span><span class="sxs-lookup"><span data-stu-id="5382b-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-241">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5382b-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="5382b-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="5382b-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="5382b-243">(23)</span><span class="sxs-lookup"><span data-stu-id="5382b-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="5382b-244">System failure.</span></span> <span data-ttu-id="5382b-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="5382b-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="5382b-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="5382b-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="5382b-247">(24)</span><span class="sxs-lookup"><span data-stu-id="5382b-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-248">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="5382b-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5382b-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5382b-250">(25)</span><span class="sxs-lookup"><span data-stu-id="5382b-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-251">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="5382b-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="5382b-253">(26)</span><span class="sxs-lookup"><span data-stu-id="5382b-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-254">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="5382b-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="5382b-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="5382b-256">(27)</span><span class="sxs-lookup"><span data-stu-id="5382b-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-257">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="5382b-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="5382b-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="5382b-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="5382b-259">(28)</span><span class="sxs-lookup"><span data-stu-id="5382b-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-260">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="5382b-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="5382b-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="5382b-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="5382b-262">(29)</span><span class="sxs-lookup"><span data-stu-id="5382b-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-263">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5382b-263">Device is disabled.</span></span> <span data-ttu-id="5382b-264">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5382b-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="5382b-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="5382b-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="5382b-266">(30)</span><span class="sxs-lookup"><span data-stu-id="5382b-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-267">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="5382b-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="5382b-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="5382b-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="5382b-269">31</span><span class="sxs-lookup"><span data-stu-id="5382b-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-270">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="5382b-270">Device is not working properly.</span></span> <span data-ttu-id="5382b-271">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="5382b-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5382b-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="5382b-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-273">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5382b-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-275">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5382b-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-276">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5382b-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="5382b-277">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5382b-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-281">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5382b-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5382b-282">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="5382b-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5382b-283">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="5382b-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="5382b-284">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-285">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5382b-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-288">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="5382b-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-289">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="5382b-289">Description of the object.</span></span>

<span data-ttu-id="5382b-290">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-291">**ID**</span><span class="sxs-lookup"><span data-stu-id="5382b-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-294">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="5382b-294">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-295">Identificador único del dispositivo de infrarrojos.</span><span class="sxs-lookup"><span data-stu-id="5382b-295">Unique identifier of the infrared device.</span></span>

<span data-ttu-id="5382b-296">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5382b-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-298">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5382b-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5382b-300">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="5382b-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="5382b-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5382b-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5382b-305">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="5382b-305">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="5382b-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5382b-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-308">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5382b-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-310">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="5382b-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-311">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="5382b-311">Date and time the object was installed.</span></span> <span data-ttu-id="5382b-312">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5382b-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5382b-313">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5382b-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-315">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5382b-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5382b-317">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5382b-317">Last error code reported by the logical device.</span></span>

<span data-ttu-id="5382b-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-319">**Le**</span><span class="sxs-lookup"><span data-stu-id="5382b-319">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-320">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-322">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="5382b-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-323">Fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-323">Manufacturer of the device.</span></span>

</dd> <dt>

<span data-ttu-id="5382b-324">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="5382b-324">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-325">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5382b-325">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-327">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="5382b-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-328">Número máximo de entidades directamente direccionables admitidas por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5382b-328">Maximum number of directly addressable entities supportable by this device.</span></span> <span data-ttu-id="5382b-329">Se debe utilizar un valor de 0 (cero) si se desconoce el número.</span><span class="sxs-lookup"><span data-stu-id="5382b-329">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="5382b-330">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-330">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-331">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="5382b-331">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-332">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-334">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5382b-334">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-335">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="5382b-335">Label by which the object is known.</span></span> <span data-ttu-id="5382b-336">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="5382b-336">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5382b-337">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-337">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-338">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="5382b-338">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-339">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-341">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="5382b-341">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-342">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5382b-342">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="5382b-343">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-343">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="5382b-344">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="5382b-344">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="5382b-345">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5382b-345">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-346">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5382b-346">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5382b-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5382b-348">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5382b-348">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="5382b-349">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="5382b-349">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5382b-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="5382b-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="5382b-351"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="5382b-351"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5382b-352"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="5382b-352"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5382b-353"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5382b-353"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-354">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5382b-354">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="5382b-355"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="5382b-355"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-356">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="5382b-356">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="5382b-357"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="5382b-357"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-358">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="5382b-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="5382b-359">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="5382b-359">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="5382b-360">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="5382b-360">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="5382b-361"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="5382b-361"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-362">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="5382b-362">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="5382b-363"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="5382b-363"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5382b-364">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="5382b-364">Timed Power-On Supported</span></span>

<span data-ttu-id="5382b-365">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="5382b-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5382b-366">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5382b-366">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-367">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5382b-367">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5382b-369">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="5382b-369">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="5382b-370">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="5382b-370">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="5382b-371">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-371">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-372">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="5382b-372">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-373">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5382b-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-375">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5382b-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-376">Protocolo usado por el controlador para tener acceso a dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="5382b-376">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="5382b-377">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-377">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="5382b-378">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="5382b-378">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5382b-379">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5382b-379">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5382b-380">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5382b-380">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="5382b-381">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="5382b-381">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="5382b-382">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="5382b-382">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="5382b-383">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="5382b-383">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="5382b-384">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="5382b-384">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="5382b-385">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="5382b-385">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="5382b-386">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="5382b-386">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="5382b-387">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="5382b-387">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="5382b-388">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="5382b-388">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="5382b-389">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="5382b-389">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="5382b-390">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="5382b-390">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="5382b-391">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="5382b-391">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="5382b-392">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="5382b-392">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="5382b-393">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="5382b-393">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="5382b-394">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="5382b-394">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="5382b-395">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="5382b-395">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="5382b-396">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="5382b-396">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="5382b-397">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="5382b-397">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="5382b-398">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="5382b-398">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="5382b-399">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="5382b-399">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="5382b-400">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="5382b-400">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="5382b-401">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="5382b-401">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="5382b-402">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="5382b-402">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="5382b-403">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="5382b-403">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="5382b-404">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="5382b-404">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="5382b-405">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="5382b-405">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="5382b-406">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="5382b-406">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="5382b-407">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="5382b-407">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="5382b-408">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="5382b-408">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="5382b-409">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="5382b-409">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="5382b-410">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="5382b-410">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="5382b-411">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="5382b-411">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="5382b-412">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="5382b-412">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="5382b-413">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="5382b-413">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="5382b-414">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="5382b-414">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="5382b-415">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="5382b-415">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="5382b-416">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="5382b-416">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="5382b-417">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="5382b-417">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="5382b-418">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="5382b-418">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="5382b-419">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="5382b-419">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="5382b-420">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="5382b-420">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="5382b-421">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="5382b-421">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="5382b-422">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="5382b-422">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="5382b-423">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="5382b-423">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="5382b-424">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="5382b-424">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="5382b-425">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="5382b-425">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5382b-426">**Estado**</span><span class="sxs-lookup"><span data-stu-id="5382b-426">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-429">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5382b-429">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-430">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="5382b-430">Current status of the object.</span></span> <span data-ttu-id="5382b-431">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="5382b-431">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5382b-432">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="5382b-432">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5382b-433">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="5382b-433">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5382b-434">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="5382b-434">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5382b-435">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="5382b-435">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5382b-436">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-436">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5382b-437">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5382b-437">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5382b-438">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="5382b-438">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5382b-439">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="5382b-439">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5382b-440">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5382b-440">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5382b-441">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="5382b-441">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5382b-442">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="5382b-442">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5382b-443">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="5382b-443">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5382b-444">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="5382b-444">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5382b-445">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="5382b-445">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5382b-446">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="5382b-446">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5382b-447">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5382b-447">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5382b-448">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="5382b-448">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5382b-449">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="5382b-449">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5382b-450">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5382b-450">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-451">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5382b-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-453">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="5382b-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="5382b-454">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5382b-454">State of the logical device.</span></span> <span data-ttu-id="5382b-455">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="5382b-455">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="5382b-456">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-456">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5382b-457">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="5382b-457">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5382b-458">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="5382b-458">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="5382b-459">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="5382b-459">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="5382b-460">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="5382b-460">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="5382b-461">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="5382b-461">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5382b-462">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5382b-462">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-463">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-464">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-465">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5382b-465">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5382b-466">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5382b-466">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="5382b-467">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-468">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5382b-468">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5382b-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5382b-471">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5382b-471">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5382b-472">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="5382b-472">Name of the scoping system.</span></span>

<span data-ttu-id="5382b-473">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="5382b-474">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="5382b-474">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5382b-475">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5382b-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5382b-476">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5382b-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5382b-477">Fecha y hora de la última vez que se restableció el controlador.</span><span class="sxs-lookup"><span data-stu-id="5382b-477">Date and time the controller was last reset.</span></span> <span data-ttu-id="5382b-478">Esto podría significar que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="5382b-478">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="5382b-479">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-479">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5382b-480">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5382b-480">Remarks</span></span>

<span data-ttu-id="5382b-481">La **clase \_ InfraredDevice de Win32** se deriva de [**\_ InfraredController de CIM**](cim-infraredcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-481">The **Win32\_InfraredDevice** class is derived from [**CIM\_InfraredController**](cim-infraredcontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5382b-482">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5382b-482">Requirements</span></span>



| <span data-ttu-id="5382b-483">Requisito</span><span class="sxs-lookup"><span data-stu-id="5382b-483">Requirement</span></span> | <span data-ttu-id="5382b-484">Value</span><span class="sxs-lookup"><span data-stu-id="5382b-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5382b-485">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5382b-485">Minimum supported client</span></span><br/> | <span data-ttu-id="5382b-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5382b-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5382b-487">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5382b-487">Minimum supported server</span></span><br/> | <span data-ttu-id="5382b-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5382b-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5382b-489">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5382b-489">Namespace</span></span><br/>                | <span data-ttu-id="5382b-490">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5382b-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5382b-491">MOF</span><span class="sxs-lookup"><span data-stu-id="5382b-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5382b-492"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5382b-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5382b-493">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5382b-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5382b-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5382b-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5382b-495">Vea también</span><span class="sxs-lookup"><span data-stu-id="5382b-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5382b-496">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="5382b-496">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dt>

[<span data-ttu-id="5382b-497">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="5382b-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

