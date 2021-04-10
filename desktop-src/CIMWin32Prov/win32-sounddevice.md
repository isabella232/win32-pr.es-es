---
description: Representa las propiedades de un dispositivo de sonido de un equipo que ejecuta Windows.
ms.assetid: 5471ffe9-60a3-466f-a608-e6268ba73c2b
ms.tgt_platform: multiple
title: Win32_SoundDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SoundDevice
- Win32_SoundDevice.Reset
- Win32_SoundDevice.SetPowerState
- Win32_SoundDevice.Availability
- Win32_SoundDevice.Caption
- Win32_SoundDevice.ConfigManagerErrorCode
- Win32_SoundDevice.ConfigManagerUserConfig
- Win32_SoundDevice.CreationClassName
- Win32_SoundDevice.Description
- Win32_SoundDevice.DeviceID
- Win32_SoundDevice.DMABufferSize
- Win32_SoundDevice.ErrorCleared
- Win32_SoundDevice.ErrorDescription
- Win32_SoundDevice.InstallDate
- Win32_SoundDevice.LastErrorCode
- Win32_SoundDevice.Manufacturer
- Win32_SoundDevice.MPU401Address
- Win32_SoundDevice.Name
- Win32_SoundDevice.PNPDeviceID
- Win32_SoundDevice.PowerManagementCapabilities
- Win32_SoundDevice.PowerManagementSupported
- Win32_SoundDevice.ProductName
- Win32_SoundDevice.Status
- Win32_SoundDevice.StatusInfo
- Win32_SoundDevice.SystemCreationClassName
- Win32_SoundDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73e0ef7cbc71872d26f75311b6d72ac48bbfae8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153487"
---
# <a name="win32_sounddevice-class"></a><span data-ttu-id="a6cf5-103">\_Clase Win32 SoundDevice</span><span class="sxs-lookup"><span data-stu-id="a6cf5-103">Win32\_SoundDevice class</span></span>

<span data-ttu-id="a6cf5-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SoundDevice de Win32** representa las propiedades de un dispositivo de sonido en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-104">The **Win32\_SoundDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a sound device on a computer system running Windows.</span></span>

<span data-ttu-id="a6cf5-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a6cf5-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6cf5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6cf5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SoundDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DMABufferSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MPU401Address;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="a6cf5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6cf5-108">Members</span></span>

<span data-ttu-id="a6cf5-109">La **clase \_ SoundDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a6cf5-109">The **Win32\_SoundDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="a6cf5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6cf5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a6cf5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6cf5-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a6cf5-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6cf5-112">Methods</span></span>

<span data-ttu-id="a6cf5-113">La clase **Win32 \_ SoundDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-113">The **Win32\_SoundDevice** class has these methods.</span></span>



| <span data-ttu-id="a6cf5-114">Método</span><span class="sxs-lookup"><span data-stu-id="a6cf5-114">Method</span></span>            | <span data-ttu-id="a6cf5-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6cf5-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cf5-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-116">**Reset**</span></span>         | <span data-ttu-id="a6cf5-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-117">Not implemented.</span></span> <span data-ttu-id="a6cf5-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**el \_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="a6cf5-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-119">**SetPowerState**</span></span> | <span data-ttu-id="a6cf5-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-120">Not implemented.</span></span> <span data-ttu-id="a6cf5-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**el \_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a6cf5-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6cf5-122">Properties</span></span>

<span data-ttu-id="a6cf5-123">La **clase \_ SoundDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-123">The **Win32\_SoundDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6cf5-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-127">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-128">Availability and status of the device.</span></span>

<span data-ttu-id="a6cf5-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a6cf5-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6cf5-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a6cf5-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="a6cf5-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a6cf5-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a6cf5-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a6cf5-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a6cf5-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="a6cf5-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a6cf5-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="a6cf5-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a6cf5-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a6cf5-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a6cf5-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a6cf5-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a6cf5-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a6cf5-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a6cf5-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a6cf5-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a6cf5-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a6cf5-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a6cf5-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a6cf5-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a6cf5-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a6cf5-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-163">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-164">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-164">Short description of the object.</span></span>

<span data-ttu-id="a6cf5-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-169">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-170">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a6cf5-171">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a6cf5-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a6cf5-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-174">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a6cf5-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a6cf5-176">(1)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-177">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a6cf5-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a6cf5-179">(2)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a6cf5-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a6cf5-181">(3)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-182">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a6cf5-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a6cf5-184">(4)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-185">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-185">Device is not working properly.</span></span> <span data-ttu-id="a6cf5-186">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a6cf5-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a6cf5-188">(5)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-189">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a6cf5-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a6cf5-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-192">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a6cf5-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a6cf5-194">(7)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a6cf5-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a6cf5-196">(8)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-197">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a6cf5-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a6cf5-199">(9)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-200">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-200">Device is not working properly.</span></span> <span data-ttu-id="a6cf5-201">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a6cf5-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a6cf5-203">(10)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-204">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a6cf5-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a6cf5-206">(11)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-207">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a6cf5-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a6cf5-209">(12)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-210">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a6cf5-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a6cf5-212">(13)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-213">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a6cf5-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a6cf5-215">(14)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-216">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a6cf5-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a6cf5-218">(15)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-219">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a6cf5-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a6cf5-221">(16)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-222">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a6cf5-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a6cf5-224">(17)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-225">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a6cf5-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a6cf5-227">(18)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-228">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a6cf5-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a6cf5-230">(19)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a6cf5-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a6cf5-232">(20)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-233">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a6cf5-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a6cf5-235">(21)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-236">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-236">System failure.</span></span> <span data-ttu-id="a6cf5-237">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a6cf5-238">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a6cf5-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a6cf5-240">(22)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-241">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a6cf5-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a6cf5-243">(23)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-244">System failure.</span></span> <span data-ttu-id="a6cf5-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a6cf5-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a6cf5-247">(24)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-248">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a6cf5-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a6cf5-250">(25)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-251">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a6cf5-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a6cf5-253">(26)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-254">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a6cf5-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a6cf5-256">(27)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-257">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a6cf5-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a6cf5-259">(28)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-260">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a6cf5-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a6cf5-262">(29)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-263">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-263">Device is disabled.</span></span> <span data-ttu-id="a6cf5-264">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a6cf5-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a6cf5-266">(30)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-267">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a6cf5-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a6cf5-269">31</span><span class="sxs-lookup"><span data-stu-id="a6cf5-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-270">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-270">Device is not working properly.</span></span> <span data-ttu-id="a6cf5-271">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a6cf5-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-273">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-275">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-276">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a6cf5-277">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-279">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-281">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-281">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-282">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-282">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a6cf5-283">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a6cf5-284">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-285">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-288">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-288">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-289">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-289">Description of the object.</span></span>

<span data-ttu-id="a6cf5-290">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-291">**ID**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-294">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ MediaResources \\ \\ Wave \| DeviceId")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-294">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\wave\|DeviceID")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-295">Identificador único del dispositivo de sonido.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-295">Unique identifier of the sound device.</span></span>

<span data-ttu-id="a6cf5-296">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-297">**DMABufferSize**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-297">**DMABufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-298">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-300">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-300">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-301">Tamaño del búfer de acceso directo a memoria.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-301">Size of the Direct Memory Access buffer.</span></span>

<span data-ttu-id="a6cf5-302">Ejemplo: 4</span><span class="sxs-lookup"><span data-stu-id="a6cf5-302">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-303">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-303">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-304">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-306">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-306">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="a6cf5-307">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-308">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-308">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-311">Cadena de forma libre que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-311">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="a6cf5-312">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-314">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-316">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-317">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-317">Date and time the object was installed.</span></span> <span data-ttu-id="a6cf5-318">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-318">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a6cf5-319">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-320">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-321">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-323">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a6cf5-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-325">**Le**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-328">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-328">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-329">Fabricante del dispositivo de sonido.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-329">Manufacturer of the sound device.</span></span>

<span data-ttu-id="a6cf5-330">Ejemplo: "Creative Labs"</span><span class="sxs-lookup"><span data-stu-id="a6cf5-330">Example: "Creative Labs"</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-331">**MPU401Address**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-331">**MPU401Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-332">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-334">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-335">Dirección de e/s de inicio asignada al puerto MPU-401 del dispositivo de sonido.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-335">Starting I/O address assigned to the MPU-401 port of the sound device.</span></span>

<span data-ttu-id="a6cf5-336">Ejemplo: 300</span><span class="sxs-lookup"><span data-stu-id="a6cf5-336">Example: 300</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-337">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-338">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-340">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-340">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-341">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-341">Label by which the object is known.</span></span> <span data-ttu-id="a6cf5-342">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-342">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a6cf5-343">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-345">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-347">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-347">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-348">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-348">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a6cf5-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a6cf5-350">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a6cf5-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-351">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-352">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-354">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a6cf5-355">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6cf5-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a6cf5-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a6cf5-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a6cf5-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-360">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a6cf5-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-362">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a6cf5-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-364">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="a6cf5-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a6cf5-365">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a6cf5-366">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-366">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a6cf5-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-368">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a6cf5-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a6cf5-370">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="a6cf5-370">Timed Power-On Supported</span></span>

<span data-ttu-id="a6cf5-371">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a6cf5-372">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-373">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-375">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-375">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="a6cf5-376">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="a6cf5-377">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-378">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-378">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-381">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api de \| estructuras multimedia \| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) \| szPname")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-381">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Multimedia Structures\|[**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)\|szPname")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-382">Nombre del producto del dispositivo de sonido.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-382">Product name of the sound device.</span></span>

<span data-ttu-id="a6cf5-383">Ejemplo: "Creative Labs SoundBlaster AWE64PNP"</span><span class="sxs-lookup"><span data-stu-id="a6cf5-383">Example: "Creative Labs SoundBlaster AWE64PNP"</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-384">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-385">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-386">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-387">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-387">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-388">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-388">Current status of the object.</span></span> <span data-ttu-id="a6cf5-389">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-389">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a6cf5-390">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-390">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a6cf5-391">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="a6cf5-391">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a6cf5-392">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-392">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a6cf5-393">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-393">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a6cf5-394">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-394">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a6cf5-395">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a6cf5-395">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a6cf5-396">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-396">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a6cf5-397">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-397">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a6cf5-398">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-398">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6cf5-399">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-399">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a6cf5-400">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-400">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a6cf5-401">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-401">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a6cf5-402">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-402">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a6cf5-403">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-403">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a6cf5-404">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-404">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a6cf5-405">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-405">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a6cf5-406">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-406">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a6cf5-407">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-407">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6cf5-408">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-408">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-409">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-411">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a6cf5-411">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-412">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-412">State of the logical device.</span></span> <span data-ttu-id="a6cf5-413">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-413">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a6cf5-414">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a6cf5-415">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-415">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6cf5-416">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-416">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a6cf5-417">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-417">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a6cf5-418">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-418">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a6cf5-419">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-419">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6cf5-420">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-420">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-421">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-423">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-423">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-424">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-424">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="a6cf5-425">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6cf5-426">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-426">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6cf5-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6cf5-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6cf5-429">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a6cf5-429">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a6cf5-430">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-430">Name of the scoping system.</span></span>

<span data-ttu-id="a6cf5-431">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6cf5-432">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6cf5-432">Remarks</span></span>

<span data-ttu-id="a6cf5-433">La **clase \_ SoundDevice de Win32** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a6cf5-433">The **Win32\_SoundDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a6cf5-434">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a6cf5-434">Examples</span></span>

<span data-ttu-id="a6cf5-435">El ejemplo de PowerShell [lista de propiedades de tarjeta de sonido](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) recupera información acerca de todas las tarjetas de sonido instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-435">The [List Sound Card Properties](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) PowerShell sample retrieves information about all the sound cards installed in a computer.</span></span>

<span data-ttu-id="a6cf5-436">El siguiente ejemplo de VBScript recupera información acerca de todas las tarjetas de sonido instaladas en un equipo.</span><span class="sxs-lookup"><span data-stu-id="a6cf5-436">The following VBScript sample retrieves information about all the sound cards installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SoundDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "DMA Buffer Size: " & objItem.DMABufferSize 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "MPU 401 Address: " & objItem.MPU401Address 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Product Name: " & objItem.ProductName 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="a6cf5-437">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6cf5-437">Requirements</span></span>



| <span data-ttu-id="a6cf5-438">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6cf5-438">Requirement</span></span> | <span data-ttu-id="a6cf5-439">Value</span><span class="sxs-lookup"><span data-stu-id="a6cf5-439">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cf5-440">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6cf5-440">Minimum supported client</span></span><br/> | <span data-ttu-id="a6cf5-441">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6cf5-441">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a6cf5-442">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6cf5-442">Minimum supported server</span></span><br/> | <span data-ttu-id="a6cf5-443">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6cf5-443">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a6cf5-444">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a6cf5-444">Namespace</span></span><br/>                | <span data-ttu-id="a6cf5-445">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a6cf5-445">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a6cf5-446">MOF</span><span class="sxs-lookup"><span data-stu-id="a6cf5-446">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6cf5-447"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6cf5-447"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6cf5-448">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6cf5-448">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6cf5-449"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6cf5-449"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6cf5-450">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6cf5-450">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6cf5-451">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a6cf5-451">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="a6cf5-452">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="a6cf5-452">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
