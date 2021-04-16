---
description: La \_ clase WMI PointingDevice de Win32 representa un dispositivo de entrada que se usa para señalar y seleccionar regiones en la visualización de un equipo que ejecuta Windows.
ms.assetid: ed81abe3-3d8f-48aa-ab64-9e6c87e44f64
ms.tgt_platform: multiple
title: Win32_PointingDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PointingDevice
- Win32_PointingDevice.Reset
- Win32_PointingDevice.SetPowerState
- Win32_PointingDevice.Availability
- Win32_PointingDevice.Caption
- Win32_PointingDevice.ConfigManagerErrorCode
- Win32_PointingDevice.ConfigManagerUserConfig
- Win32_PointingDevice.CreationClassName
- Win32_PointingDevice.Description
- Win32_PointingDevice.DeviceID
- Win32_PointingDevice.DeviceInterface
- Win32_PointingDevice.DoubleSpeedThreshold
- Win32_PointingDevice.ErrorCleared
- Win32_PointingDevice.ErrorDescription
- Win32_PointingDevice.Handedness
- Win32_PointingDevice.HardwareType
- Win32_PointingDevice.InfFileName
- Win32_PointingDevice.InfSection
- Win32_PointingDevice.InstallDate
- Win32_PointingDevice.IsLocked
- Win32_PointingDevice.LastErrorCode
- Win32_PointingDevice.Manufacturer
- Win32_PointingDevice.Name
- Win32_PointingDevice.NumberOfButtons
- Win32_PointingDevice.PNPDeviceID
- Win32_PointingDevice.PointingType
- Win32_PointingDevice.PowerManagementCapabilities
- Win32_PointingDevice.PowerManagementSupported
- Win32_PointingDevice.QuadSpeedThreshold
- Win32_PointingDevice.Resolution
- Win32_PointingDevice.SampleRate
- Win32_PointingDevice.Status
- Win32_PointingDevice.StatusInfo
- Win32_PointingDevice.Synch
- Win32_PointingDevice.SystemCreationClassName
- Win32_PointingDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e4f2359e19476dfae111fc361f48e6f73d8cfac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659387"
---
# <a name="win32_pointingdevice-class"></a><span data-ttu-id="2855d-103">\_Clase Win32 PointingDevice</span><span class="sxs-lookup"><span data-stu-id="2855d-103">Win32\_PointingDevice class</span></span>

<span data-ttu-id="2855d-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PointingDevice de Win32** representa un dispositivo de entrada que se usa para señalar y seleccionar regiones en la visualización de un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="2855d-104">The **Win32\_PointingDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents an input device used to point to and select regions on the display of a computer system running Windows.</span></span> <span data-ttu-id="2855d-105">Cualquier dispositivo usado para manipular un puntero o apuntar a la pantalla de un equipo que ejecuta Windows es miembro de esta clase.</span><span class="sxs-lookup"><span data-stu-id="2855d-105">Any device used to manipulate a pointer, or point to the display on a computer system running Windows is a member of this class.</span></span>

<span data-ttu-id="2855d-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2855d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2855d-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2855d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2855d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2855d-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PointingDevice : CIM_PointingDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DeviceInterface;
  uint32   DoubleSpeedThreshold;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint16   Handedness;
  string   HardwareType;
  string   InfFileName;
  string   InfSection;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  uint8    NumberOfButtons;
  string   PNPDeviceID;
  uint16   PointingType;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   QuadSpeedThreshold;
  uint32   Resolution;
  uint32   SampleRate;
  string   Status;
  uint16   StatusInfo;
  uint32   Synch;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="2855d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2855d-109">Members</span></span>

<span data-ttu-id="2855d-110">La **clase \_ PointingDevice de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2855d-110">The **Win32\_PointingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="2855d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2855d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2855d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2855d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2855d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2855d-113">Methods</span></span>

<span data-ttu-id="2855d-114">La clase **Win32 \_ PointingDevice** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2855d-114">The **Win32\_PointingDevice** class has these methods.</span></span>



| <span data-ttu-id="2855d-115">Método</span><span class="sxs-lookup"><span data-stu-id="2855d-115">Method</span></span>            | <span data-ttu-id="2855d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2855d-116">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2855d-117">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2855d-117">**Reset**</span></span>         | <span data-ttu-id="2855d-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="2855d-118">Not implemented.</span></span> <span data-ttu-id="2855d-119">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/>                 |
| <span data-ttu-id="2855d-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2855d-120">**SetPowerState**</span></span> | <span data-ttu-id="2855d-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="2855d-121">Not implemented.</span></span> <span data-ttu-id="2855d-122">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ PointingDevice**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2855d-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2855d-123">Properties</span></span>

<span data-ttu-id="2855d-124">La **clase \_ PointingDevice de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2855d-124">The **Win32\_PointingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2855d-125">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="2855d-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2855d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-128">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2855d-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-129">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-129">Availability and status of the device.</span></span>

<span data-ttu-id="2855d-130">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2855d-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2855d-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2855d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2855d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2855d-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="2855d-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-134">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="2855d-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2855d-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="2855d-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2855d-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="2855d-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2855d-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="2855d-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2855d-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="2855d-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2855d-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="2855d-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2855d-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="2855d-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2855d-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="2855d-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2855d-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="2855d-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2855d-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="2855d-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2855d-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="2855d-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="2855d-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2855d-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="2855d-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="2855d-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2855d-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="2855d-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-149">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2855d-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2855d-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="2855d-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2855d-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="2855d-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="2855d-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2855d-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="2855d-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="2855d-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2855d-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="2855d-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="2855d-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2855d-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="2855d-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="2855d-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2855d-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="2855d-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="2855d-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2855d-161">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2855d-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-164">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2855d-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-165">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2855d-165">Short description of the object.</span></span>

<span data-ttu-id="2855d-166">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-167">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2855d-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2855d-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-170">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2855d-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-171">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="2855d-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2855d-172">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2855d-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="2855d-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2855d-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="2855d-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-175">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2855d-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2855d-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="2855d-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2855d-177">(1)</span><span class="sxs-lookup"><span data-stu-id="2855d-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-178">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2855d-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2855d-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2855d-180">(2)</span><span class="sxs-lookup"><span data-stu-id="2855d-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2855d-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="2855d-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2855d-182">(3)</span><span class="sxs-lookup"><span data-stu-id="2855d-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-183">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="2855d-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2855d-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="2855d-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2855d-185">(4)</span><span class="sxs-lookup"><span data-stu-id="2855d-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-186">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2855d-186">Device is not working properly.</span></span> <span data-ttu-id="2855d-187">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="2855d-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2855d-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="2855d-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2855d-189">(5)</span><span class="sxs-lookup"><span data-stu-id="2855d-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-190">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="2855d-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2855d-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="2855d-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2855d-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="2855d-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-193">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2855d-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2855d-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="2855d-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2855d-195">(7)</span><span class="sxs-lookup"><span data-stu-id="2855d-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2855d-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2855d-197">(8)</span><span class="sxs-lookup"><span data-stu-id="2855d-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-198">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2855d-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="2855d-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2855d-200">(9)</span><span class="sxs-lookup"><span data-stu-id="2855d-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-201">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2855d-201">Device is not working properly.</span></span> <span data-ttu-id="2855d-202">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2855d-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="2855d-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2855d-204">(10)</span><span class="sxs-lookup"><span data-stu-id="2855d-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-205">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="2855d-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2855d-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2855d-207">(11)</span><span class="sxs-lookup"><span data-stu-id="2855d-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-208">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2855d-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="2855d-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2855d-210">(12)</span><span class="sxs-lookup"><span data-stu-id="2855d-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-211">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="2855d-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2855d-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2855d-213">(13)</span><span class="sxs-lookup"><span data-stu-id="2855d-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-214">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2855d-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2855d-216">(14)</span><span class="sxs-lookup"><span data-stu-id="2855d-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-217">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="2855d-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2855d-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="2855d-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2855d-219">(15)</span><span class="sxs-lookup"><span data-stu-id="2855d-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-220">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="2855d-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2855d-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2855d-222">(16)</span><span class="sxs-lookup"><span data-stu-id="2855d-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-223">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2855d-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="2855d-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2855d-225">(17)</span><span class="sxs-lookup"><span data-stu-id="2855d-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-226">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="2855d-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2855d-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2855d-228">(18)</span><span class="sxs-lookup"><span data-stu-id="2855d-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-229">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2855d-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2855d-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="2855d-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2855d-231">(19)</span><span class="sxs-lookup"><span data-stu-id="2855d-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2855d-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="2855d-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2855d-233">(20)</span><span class="sxs-lookup"><span data-stu-id="2855d-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-234">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="2855d-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2855d-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2855d-236">(21)</span><span class="sxs-lookup"><span data-stu-id="2855d-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-237">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="2855d-237">System failure.</span></span> <span data-ttu-id="2855d-238">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="2855d-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2855d-239">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2855d-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="2855d-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2855d-241">(22)</span><span class="sxs-lookup"><span data-stu-id="2855d-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-242">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2855d-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2855d-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="2855d-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2855d-244">(23)</span><span class="sxs-lookup"><span data-stu-id="2855d-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-245">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="2855d-245">System failure.</span></span> <span data-ttu-id="2855d-246">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="2855d-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2855d-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="2855d-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2855d-248">(24)</span><span class="sxs-lookup"><span data-stu-id="2855d-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-249">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="2855d-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2855d-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2855d-251">(25)</span><span class="sxs-lookup"><span data-stu-id="2855d-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-252">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2855d-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2855d-254">(26)</span><span class="sxs-lookup"><span data-stu-id="2855d-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-255">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2855d-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2855d-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="2855d-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2855d-257">(27)</span><span class="sxs-lookup"><span data-stu-id="2855d-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-258">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="2855d-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2855d-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="2855d-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2855d-260">(28)</span><span class="sxs-lookup"><span data-stu-id="2855d-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-261">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="2855d-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2855d-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="2855d-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2855d-263">(29)</span><span class="sxs-lookup"><span data-stu-id="2855d-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-264">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2855d-264">Device is disabled.</span></span> <span data-ttu-id="2855d-265">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="2855d-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2855d-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="2855d-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2855d-267">(30)</span><span class="sxs-lookup"><span data-stu-id="2855d-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-268">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="2855d-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2855d-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2855d-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2855d-270">31</span><span class="sxs-lookup"><span data-stu-id="2855d-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-271">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2855d-271">Device is not working properly.</span></span> <span data-ttu-id="2855d-272">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="2855d-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2855d-273">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2855d-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-274">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2855d-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-276">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2855d-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-277">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2855d-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2855d-278">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2855d-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-280">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-282">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2855d-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2855d-283">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="2855d-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="2855d-284">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="2855d-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2855d-285">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-286">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2855d-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-287">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-289">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="2855d-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-290">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2855d-290">Description of the object.</span></span>

<span data-ttu-id="2855d-291">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-292">**ID**</span><span class="sxs-lookup"><span data-stu-id="2855d-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-295">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2855d-295">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-296">Identificador único del dispositivo señalador con otros dispositivos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="2855d-296">Unique identifier of the pointing device with other devices on the system.</span></span>

<span data-ttu-id="2855d-297">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-298">**DeviceInterface**</span><span class="sxs-lookup"><span data-stu-id="2855d-298">**DeviceInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-299">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2855d-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-301">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| interfaz de tipo SMBIOS 21 \| ")</span><span class="sxs-lookup"><span data-stu-id="2855d-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 21\|Interface")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-302">Tipo de interfaz que se usa para el dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="2855d-302">Type of interface used for the pointing device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2855d-303">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2855d-303">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2855d-304">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2855d-304">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial"></span><span id="serial"></span><span id="SERIAL"></span>

<span data-ttu-id="2855d-305">**Serie** (3)</span><span class="sxs-lookup"><span data-stu-id="2855d-305">**Serial** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="2855d-306">**PS/2** (4)</span><span class="sxs-lookup"><span data-stu-id="2855d-306">**PS/2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="2855d-307">**Infrarrojos** (5)</span><span class="sxs-lookup"><span data-stu-id="2855d-307">**Infrared** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="2855d-308">**HP-Hil** (6)</span><span class="sxs-lookup"><span data-stu-id="2855d-308">**HP-HIL** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="2855d-309">**Mouse de bus** (7)</span><span class="sxs-lookup"><span data-stu-id="2855d-309">**Bus mouse** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB__Apple_Desktop_Bus_"></span><span id="adb__apple_desktop_bus_"></span><span id="ADB__APPLE_DESKTOP_BUS_"></span>

<span data-ttu-id="2855d-310">**ADB (bus de escritorio de Apple)** (8)</span><span class="sxs-lookup"><span data-stu-id="2855d-310">**ADB (Apple Desktop Bus)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_DB-9"></span><span id="bus_mouse_db-9"></span><span id="BUS_MOUSE_DB-9"></span>

<span data-ttu-id="2855d-311">**Base de mouse de bus DB-9** (160)</span><span class="sxs-lookup"><span data-stu-id="2855d-311">**Bus mouse DB-9** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_mouse_micro-DIN"></span><span id="bus_mouse_micro-din"></span><span id="BUS_MOUSE_MICRO-DIN"></span>

<span data-ttu-id="2855d-312">**Micro-DIN de mouse de bus** (161)</span><span class="sxs-lookup"><span data-stu-id="2855d-312">**Bus mouse micro-DIN** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="2855d-313">**USB** (162)</span><span class="sxs-lookup"><span data-stu-id="2855d-313">**USB** (162)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2855d-314">**DoubleSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="2855d-314">**DoubleSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-315">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2855d-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-317">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Functions \| SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="2855d-317">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-318">Uno de los dos valores de aceleración.</span><span class="sxs-lookup"><span data-stu-id="2855d-318">One of two acceleration values.</span></span> <span data-ttu-id="2855d-319">La confidencialidad del dispositivo señalador se duplica (alterna entre el primero y el segundo valor) cuando el dispositivo señalador mueve una distancia mayor que este valor de umbral.</span><span class="sxs-lookup"><span data-stu-id="2855d-319">The sensitivity of the pointing device doubles (toggles from the first to the second value) when the pointing device moves a distance greater than this threshold value.</span></span>

</dd> <dt>

<span data-ttu-id="2855d-320">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2855d-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-321">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2855d-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2855d-323">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="2855d-323">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="2855d-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2855d-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2855d-328">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="2855d-328">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="2855d-329">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-330">**Situación**</span><span class="sxs-lookup"><span data-stu-id="2855d-330">**Handedness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-331">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2855d-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2855d-333">Configuración del dispositivo señalador para la operación de la izquierda o la derecha.</span><span class="sxs-lookup"><span data-stu-id="2855d-333">Configuration of the pointing device for left-hand or right-hand operation.</span></span>

<span data-ttu-id="2855d-334">Esta propiedad se hereda de [**\_ PointingDevice CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-334">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2855d-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2855d-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2855d-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (1)</span><span class="sxs-lookup"><span data-stu-id="2855d-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>

<span data-ttu-id="2855d-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Operación de mano derecha** (2)</span><span class="sxs-lookup"><span data-stu-id="2855d-337"><span id="Right_Handed_Operation"></span><span id="right_handed_operation"></span><span id="RIGHT_HANDED_OPERATION"></span>**Right Handed Operation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-338">Right-Handed operación</span><span class="sxs-lookup"><span data-stu-id="2855d-338">Right-Handed Operation</span></span>

</dd> <dt>

<span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>

<span data-ttu-id="2855d-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Operación de mano izquierda** (3)</span><span class="sxs-lookup"><span data-stu-id="2855d-339"><span id="Left_Handed_Operation"></span><span id="left_handed_operation"></span><span id="LEFT_HANDED_OPERATION"></span>**Left Handed Operation** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-340">Left-Handed operación</span><span class="sxs-lookup"><span data-stu-id="2855d-340">Left-Handed Operation</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2855d-341">**HardwareType**</span><span class="sxs-lookup"><span data-stu-id="2855d-341">**HardwareType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-342">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-344">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ ControlSet001 \\ \\ control \\ \\ Class \| DriverDesc")</span><span class="sxs-lookup"><span data-stu-id="2855d-344">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\ControlSet001\\\\Control\\\\Class\|DriverDesc")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-345">Tipo de hardware usado para el dispositivo señalador de Windows.</span><span class="sxs-lookup"><span data-stu-id="2855d-345">Type of hardware used for the Windows pointing device.</span></span>

<span data-ttu-id="2855d-346">Ejemplo: "MOUSE PS2 de MICROSOFT"</span><span class="sxs-lookup"><span data-stu-id="2855d-346">Example: "MICROSOFT PS2 MOUSE"</span></span>

</dd> <dt>

<span data-ttu-id="2855d-347">**InfFileName**</span><span class="sxs-lookup"><span data-stu-id="2855d-347">**InfFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-348">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-350">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| InfPath")</span><span class="sxs-lookup"><span data-stu-id="2855d-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-351">Nombre del archivo. inf para el dispositivo señalador de Windows.</span><span class="sxs-lookup"><span data-stu-id="2855d-351">Name of the .inf file for the Windows pointing device.</span></span>

<span data-ttu-id="2855d-352">Ejemplo: "AB. inf"</span><span class="sxs-lookup"><span data-stu-id="2855d-352">Example: "ab.inf"</span></span>

</dd> <dt>

<span data-ttu-id="2855d-353">**InfSection**</span><span class="sxs-lookup"><span data-stu-id="2855d-353">**InfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-354">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-356">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \| InfSection")</span><span class="sxs-lookup"><span data-stu-id="2855d-356">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-357">Sección del archivo. inf que contiene información de configuración del dispositivo señalador de Windows.</span><span class="sxs-lookup"><span data-stu-id="2855d-357">Section of the .inf file that holds configuration information for the Windows pointing device.</span></span>

</dd> <dt>

<span data-ttu-id="2855d-358">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2855d-358">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-359">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2855d-359">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-361">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="2855d-361">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-362">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="2855d-362">Date and time the object was installed.</span></span> <span data-ttu-id="2855d-363">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="2855d-363">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2855d-364">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-365">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="2855d-365">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-366">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2855d-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2855d-368">Si es **true**, el dispositivo está bloqueado, lo que impide la entrada o salida del usuario.</span><span class="sxs-lookup"><span data-stu-id="2855d-368">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="2855d-369">Esta propiedad se hereda de [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-369">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-370">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2855d-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-371">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2855d-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2855d-373">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2855d-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2855d-374">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-375">**Le**</span><span class="sxs-lookup"><span data-stu-id="2855d-375">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-378">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2855d-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-379">Nombre del fabricante del procesador.</span><span class="sxs-lookup"><span data-stu-id="2855d-379">Name of the processor's manufacturer.</span></span>

<span data-ttu-id="2855d-380">Ejemplo: "GenuineSilicon"</span><span class="sxs-lookup"><span data-stu-id="2855d-380">Example: "GenuineSilicon"</span></span>

</dd> <dt>

<span data-ttu-id="2855d-381">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2855d-381">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-382">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-384">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2855d-384">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-385">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="2855d-385">Label by which the object is known.</span></span> <span data-ttu-id="2855d-386">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="2855d-386">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="2855d-387">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-387">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-388">**NumberOfButtons**</span><span class="sxs-lookup"><span data-stu-id="2855d-388">**NumberOfButtons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-389">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2855d-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2855d-391">Número de botones del dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="2855d-391">Number of buttons on the pointing device.</span></span>

<span data-ttu-id="2855d-392">Esta propiedad se hereda de [**\_ PointingDevice CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-392">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="2855d-393">Ejemplo: 2</span><span class="sxs-lookup"><span data-stu-id="2855d-393">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="2855d-394">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2855d-394">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-395">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-397">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2855d-397">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-398">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2855d-398">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2855d-399">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2855d-400">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2855d-400">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2855d-401">**PointingType**</span><span class="sxs-lookup"><span data-stu-id="2855d-401">**PointingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-402">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2855d-402">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-404">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo señalador DMTF \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="2855d-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Pointing Device\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-405">Tipo de dispositivo señalador.</span><span class="sxs-lookup"><span data-stu-id="2855d-405">Type of pointing device.</span></span>

<span data-ttu-id="2855d-406">Esta propiedad se hereda de [**\_ PointingDevice CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-406">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2855d-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2855d-407"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2855d-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2855d-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>

<span data-ttu-id="2855d-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span><span class="sxs-lookup"><span data-stu-id="2855d-409"><span id="Mouse"></span><span id="mouse"></span><span id="MOUSE"></span>**Mouse** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>

<span data-ttu-id="2855d-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Bola de seguimiento** (4)</span><span class="sxs-lookup"><span data-stu-id="2855d-410"><span id="Track_Ball"></span><span id="track_ball"></span><span id="TRACK_BALL"></span>**Track Ball** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-411">Trackball</span><span class="sxs-lookup"><span data-stu-id="2855d-411">Trackball</span></span>

</dd> <dt>

<span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>

<span data-ttu-id="2855d-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Punto de seguimiento** (5)</span><span class="sxs-lookup"><span data-stu-id="2855d-412"><span id="Track_Point"></span><span id="track_point"></span><span id="TRACK_POINT"></span>**Track Point** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>

<span data-ttu-id="2855d-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Punto de deslizamiento** (6)</span><span class="sxs-lookup"><span data-stu-id="2855d-413"><span id="Glide_Point"></span><span id="glide_point"></span><span id="GLIDE_POINT"></span>**Glide Point** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>

<span data-ttu-id="2855d-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Teclado táctil** (7)</span><span class="sxs-lookup"><span data-stu-id="2855d-414"><span id="Touch_Pad"></span><span id="touch_pad"></span><span id="TOUCH_PAD"></span>**Touch Pad** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>

<span data-ttu-id="2855d-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Pantalla táctil** (8)</span><span class="sxs-lookup"><span data-stu-id="2855d-415"><span id="Touch_Screen"></span><span id="touch_screen"></span><span id="TOUCH_SCREEN"></span>**Touch Screen** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>

<span data-ttu-id="2855d-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse-sensor óptico** (9)</span><span class="sxs-lookup"><span data-stu-id="2855d-416"><span id="Mouse_-_Optical_Sensor"></span><span id="mouse_-_optical_sensor"></span><span id="MOUSE_-_OPTICAL_SENSOR"></span>**Mouse - Optical Sensor** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2855d-417">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2855d-417">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-418">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2855d-418">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2855d-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2855d-420">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2855d-420">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2855d-421">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="2855d-421">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2855d-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2855d-422"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2855d-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2855d-423"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2855d-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="2855d-424"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2855d-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2855d-425"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-426">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2855d-426">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2855d-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2855d-427"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-428">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="2855d-428">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2855d-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="2855d-429"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-430">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="2855d-430">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2855d-431">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="2855d-431">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2855d-432">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-432">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2855d-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="2855d-433"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-434">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="2855d-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2855d-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="2855d-435"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2855d-436">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="2855d-436">Timed Power-On Supported</span></span>

<span data-ttu-id="2855d-437">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="2855d-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2855d-438">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2855d-438">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-439">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2855d-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2855d-441">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="2855d-441">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="2855d-442">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="2855d-442">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="2855d-443">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-444">**QuadSpeedThreshold**</span><span class="sxs-lookup"><span data-stu-id="2855d-444">**QuadSpeedThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-445">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2855d-445">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-447">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| System Information Functions \| SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("Mickeys")</span><span class="sxs-lookup"><span data-stu-id="2855d-447">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|SystemParametersInfo"), [**Units**](../wmisdk/standard-qualifiers.md) ("mickeys")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-448">Uno de los dos valores de umbral de aceleración.</span><span class="sxs-lookup"><span data-stu-id="2855d-448">One of two acceleration threshold values.</span></span> <span data-ttu-id="2855d-449">El sistema duplica la velocidad del movimiento del puntero cuando el dispositivo de puntero mueve una distancia mayor que este valor.</span><span class="sxs-lookup"><span data-stu-id="2855d-449">The system doubles the speed of the pointer movement when the pointer device moves a distance greater than this value.</span></span> <span data-ttu-id="2855d-450">Dado que este aumento de velocidad se produce una vez que se ha alcanzado el valor de **DoubleSpeedThreshold** , el puntero se mueve realmente cuatro veces a la velocidad original.</span><span class="sxs-lookup"><span data-stu-id="2855d-450">Because this speed increase occurs after the **DoubleSpeedThreshold** value has been met, the pointer effectively moves at four times its original speed.</span></span>

</dd> <dt>

<span data-ttu-id="2855d-451">**Resolución**</span><span class="sxs-lookup"><span data-stu-id="2855d-451">**Resolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-452">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2855d-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-454">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("recuentos por pulgada")</span><span class="sxs-lookup"><span data-stu-id="2855d-454">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("counts per inch")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-455">Resolución de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="2855d-455">Tracking resolution.</span></span>

<span data-ttu-id="2855d-456">Esta propiedad se hereda de [**\_ PointingDevice CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-456">This property is inherited from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

<span data-ttu-id="2855d-457">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="2855d-457">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="2855d-458">**SampleRate**</span><span class="sxs-lookup"><span data-stu-id="2855d-458">**SampleRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-459">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2855d-459">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-461">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SampleRate"), [**unidades**](../wmisdk/standard-qualifiers.md) ("hercios")</span><span class="sxs-lookup"><span data-stu-id="2855d-461">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SampleRate"), [**Units**](../wmisdk/standard-qualifiers.md) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-462">Velocidad a la que se sondea el dispositivo señalador en busca de información de entrada.</span><span class="sxs-lookup"><span data-stu-id="2855d-462">Rate at which the pointing device is polled for input information.</span></span>

</dd> <dt>

<span data-ttu-id="2855d-463">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2855d-463">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-464">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-464">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-466">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="2855d-466">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-467">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2855d-467">Current status of the object.</span></span> <span data-ttu-id="2855d-468">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="2855d-468">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2855d-469">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="2855d-469">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2855d-470">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="2855d-470">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2855d-471">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="2855d-471">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2855d-472">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="2855d-472">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2855d-473">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-473">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2855d-474">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2855d-474">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2855d-475">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="2855d-475">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2855d-476">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="2855d-476">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2855d-477">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2855d-477">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2855d-478">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="2855d-478">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2855d-479">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="2855d-479">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2855d-480">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="2855d-480">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2855d-481">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="2855d-481">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2855d-482">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="2855d-482">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2855d-483">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="2855d-483">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2855d-484">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2855d-484">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2855d-485">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="2855d-485">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2855d-486">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="2855d-486">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2855d-487">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2855d-487">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-488">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2855d-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-489">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-490">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2855d-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-491">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2855d-491">State of the logical device.</span></span> <span data-ttu-id="2855d-492">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="2855d-492">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2855d-493">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-493">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2855d-494">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2855d-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2855d-495">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2855d-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2855d-496">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2855d-496">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2855d-497">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="2855d-497">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2855d-498">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="2855d-498">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2855d-499">**Synch**</span><span class="sxs-lookup"><span data-stu-id="2855d-499">**Synch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-500">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2855d-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-501">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-501">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-502">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| MouseSynchIn100ns"), [**unidades**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")</span><span class="sxs-lookup"><span data-stu-id="2855d-502">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|MouseSynchIn100ns"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="2855d-503">Período de tiempo después del cual se supone que la siguiente interrupción indica el inicio de un nuevo paquete de dispositivo (los paquetes parciales se descartan).</span><span class="sxs-lookup"><span data-stu-id="2855d-503">Length of time after which the next interrupt is assumed to indicate the start of a new device packet (partial packets are discarded).</span></span> <span data-ttu-id="2855d-504">En caso de que se pierda una interrupción, esto permite que el controlador del dispositivo señalador Sincronice su representación interna del estado del paquete con el estado del hardware.</span><span class="sxs-lookup"><span data-stu-id="2855d-504">In the event that an interrupt is lost, this allows the pointing device driver to synchronize its internal representation of the packet state with the hardware state.</span></span>

</dd> <dt>

<span data-ttu-id="2855d-505">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2855d-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-506">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-508">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2855d-508">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2855d-509">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2855d-509">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="2855d-510">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2855d-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2855d-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2855d-512">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2855d-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2855d-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2855d-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2855d-514">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2855d-514">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2855d-515">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2855d-515">Name of the scoping system.</span></span>

<span data-ttu-id="2855d-516">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2855d-517">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2855d-517">Remarks</span></span>

<span data-ttu-id="2855d-518">La **clase \_ PointingDevice de Win32** se deriva de [**\_ PointingDevice de CIM**](cim-pointingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2855d-518">The **Win32\_PointingDevice** class is derived from [**CIM\_PointingDevice**](cim-pointingdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2855d-519">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2855d-519">Requirements</span></span>



| <span data-ttu-id="2855d-520">Requisito</span><span class="sxs-lookup"><span data-stu-id="2855d-520">Requirement</span></span> | <span data-ttu-id="2855d-521">Value</span><span class="sxs-lookup"><span data-stu-id="2855d-521">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2855d-522">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2855d-522">Minimum supported client</span></span><br/> | <span data-ttu-id="2855d-523">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2855d-523">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2855d-524">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2855d-524">Minimum supported server</span></span><br/> | <span data-ttu-id="2855d-525">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2855d-525">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2855d-526">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2855d-526">Namespace</span></span><br/>                | <span data-ttu-id="2855d-527">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2855d-527">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2855d-528">MOF</span><span class="sxs-lookup"><span data-stu-id="2855d-528">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2855d-529"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2855d-529"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2855d-530">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2855d-530">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2855d-531"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2855d-531"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2855d-532">Vea también</span><span class="sxs-lookup"><span data-stu-id="2855d-532">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2855d-533">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2855d-533">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dt>

[<span data-ttu-id="2855d-534">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="2855d-534">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
