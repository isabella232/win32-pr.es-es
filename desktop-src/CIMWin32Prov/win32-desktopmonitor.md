---
description: Representa el tipo de monitor o dispositivo de pantalla conectado al sistema del equipo.
ms.assetid: 922be3c1-3c7b-4418-a72f-ab5ada91a7a4
ms.tgt_platform: multiple
title: Win32_DesktopMonitor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DesktopMonitor
- Win32_DesktopMonitor.Reset
- Win32_DesktopMonitor.SetPowerState
- Win32_DesktopMonitor.Availability
- Win32_DesktopMonitor.Bandwidth
- Win32_DesktopMonitor.Caption
- Win32_DesktopMonitor.ConfigManagerErrorCode
- Win32_DesktopMonitor.ConfigManagerUserConfig
- Win32_DesktopMonitor.CreationClassName
- Win32_DesktopMonitor.Description
- Win32_DesktopMonitor.DeviceID
- Win32_DesktopMonitor.DisplayType
- Win32_DesktopMonitor.ErrorCleared
- Win32_DesktopMonitor.ErrorDescription
- Win32_DesktopMonitor.InstallDate
- Win32_DesktopMonitor.IsLocked
- Win32_DesktopMonitor.LastErrorCode
- Win32_DesktopMonitor.MonitorManufacturer
- Win32_DesktopMonitor.MonitorType
- Win32_DesktopMonitor.Name
- Win32_DesktopMonitor.PixelsPerXLogicalInch
- Win32_DesktopMonitor.PixelsPerYLogicalInch
- Win32_DesktopMonitor.PNPDeviceID
- Win32_DesktopMonitor.PowerManagementCapabilities
- Win32_DesktopMonitor.PowerManagementSupported
- Win32_DesktopMonitor.ScreenHeight
- Win32_DesktopMonitor.ScreenWidth
- Win32_DesktopMonitor.Status
- Win32_DesktopMonitor.StatusInfo
- Win32_DesktopMonitor.SystemCreationClassName
- Win32_DesktopMonitor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccf986957d73dd93837b0ab7a1e10b50aec5e8f9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539370"
---
# <a name="win32_desktopmonitor-class"></a><span data-ttu-id="6ba47-103">\_Clase Win32 DesktopMonitor</span><span class="sxs-lookup"><span data-stu-id="6ba47-103">Win32\_DesktopMonitor class</span></span>

<span data-ttu-id="6ba47-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DesktopMonitor de Win32** representa el tipo de monitor o dispositivo de pantalla conectado al sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-104">The **Win32\_DesktopMonitor** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the type of monitor or display device attached to the computer system.</span></span>

<span data-ttu-id="6ba47-105">El hardware que no es compatible con Windows Display Driver Model (WDDM) devuelve valores de propiedad inexactos para las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="6ba47-105">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

<span data-ttu-id="6ba47-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6ba47-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6ba47-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6ba47-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba47-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ba47-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCF0-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_DesktopMonitor : CIM_DesktopMonitor
{
  uint16   Availability;
  uint32   Bandwidth;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="6ba47-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ba47-109">Members</span></span>

<span data-ttu-id="6ba47-110">La **clase \_ DesktopMonitor de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6ba47-110">The **Win32\_DesktopMonitor** class has these types of members:</span></span>

-   [<span data-ttu-id="6ba47-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ba47-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6ba47-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ba47-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6ba47-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ba47-113">Methods</span></span>

<span data-ttu-id="6ba47-114">La clase **Win32 \_ DesktopMonitor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6ba47-114">The **Win32\_DesktopMonitor** class has these methods.</span></span>



| <span data-ttu-id="6ba47-115">Método</span><span class="sxs-lookup"><span data-stu-id="6ba47-115">Method</span></span>            | <span data-ttu-id="6ba47-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba47-116">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba47-117">**Reset**</span><span class="sxs-lookup"><span data-stu-id="6ba47-117">**Reset**</span></span>         | <span data-ttu-id="6ba47-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="6ba47-118">Not implemented.</span></span> <span data-ttu-id="6ba47-119">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="6ba47-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="6ba47-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="6ba47-120">**SetPowerState**</span></span> | <span data-ttu-id="6ba47-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="6ba47-121">Not implemented.</span></span> <span data-ttu-id="6ba47-122">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="6ba47-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6ba47-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ba47-123">Properties</span></span>

<span data-ttu-id="6ba47-124">La **clase \_ DesktopMonitor de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6ba47-124">The **Win32\_DesktopMonitor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ba47-125">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="6ba47-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ba47-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="6ba47-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-129">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-129">Availability and status of the device.</span></span>

<span data-ttu-id="6ba47-130">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ba47-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="6ba47-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ba47-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="6ba47-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="6ba47-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="6ba47-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-134">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="6ba47-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="6ba47-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="6ba47-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="6ba47-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="6ba47-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6ba47-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="6ba47-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="6ba47-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="6ba47-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="6ba47-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="6ba47-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="6ba47-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="6ba47-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6ba47-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="6ba47-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="6ba47-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="6ba47-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="6ba47-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="6ba47-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="6ba47-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="6ba47-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="6ba47-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="6ba47-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="6ba47-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="6ba47-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="6ba47-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="6ba47-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-149">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="6ba47-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="6ba47-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="6ba47-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="6ba47-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="6ba47-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="6ba47-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="6ba47-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="6ba47-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="6ba47-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="6ba47-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="6ba47-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6ba47-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="6ba47-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="6ba47-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="6ba47-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="6ba47-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="6ba47-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ba47-161">**Ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="6ba47-161">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ba47-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-164">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahercios")</span><span class="sxs-lookup"><span data-stu-id="6ba47-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-165">Ancho de banda del monitor en megahercios.</span><span class="sxs-lookup"><span data-stu-id="6ba47-165">Monitor's bandwidth in megahertz.</span></span> <span data-ttu-id="6ba47-166">Si es desconocido, escriba 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="6ba47-166">If unknown, enter 0 (zero).</span></span>

<span data-ttu-id="6ba47-167">Esta propiedad se hereda de [**\_ DesktopMonitor CIM**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-167">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-168">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6ba47-168">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-171">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6ba47-171">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-172">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6ba47-172">Short description of the object.</span></span>

<span data-ttu-id="6ba47-173">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-174">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6ba47-174">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-175">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ba47-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-177">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6ba47-177">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-178">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="6ba47-178">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="6ba47-179">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-179">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="6ba47-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-180"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="6ba47-181"> (0)</span><span class="sxs-lookup"><span data-stu-id="6ba47-181">(0)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-182">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ba47-182">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="6ba47-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-183"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="6ba47-184">(1)</span><span class="sxs-lookup"><span data-stu-id="6ba47-184">(1)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-185">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ba47-185">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6ba47-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-186"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="6ba47-187">(2)</span><span class="sxs-lookup"><span data-stu-id="6ba47-187">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="6ba47-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-188"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="6ba47-189">(3)</span><span class="sxs-lookup"><span data-stu-id="6ba47-189">(3)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-190">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="6ba47-190">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6ba47-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-191"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="6ba47-192">(4)</span><span class="sxs-lookup"><span data-stu-id="6ba47-192">(4)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-193">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ba47-193">Device is not working properly.</span></span> <span data-ttu-id="6ba47-194">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="6ba47-194">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="6ba47-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-195"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="6ba47-196">(5)</span><span class="sxs-lookup"><span data-stu-id="6ba47-196">(5)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-197">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="6ba47-197">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="6ba47-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-198"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="6ba47-199"> (6)</span><span class="sxs-lookup"><span data-stu-id="6ba47-199">(6)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-200">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6ba47-200">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="6ba47-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-201"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="6ba47-202">(7)</span><span class="sxs-lookup"><span data-stu-id="6ba47-202">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="6ba47-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-203"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="6ba47-204">(8)</span><span class="sxs-lookup"><span data-stu-id="6ba47-204">(8)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-205">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-205">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="6ba47-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-206"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="6ba47-207">(9)</span><span class="sxs-lookup"><span data-stu-id="6ba47-207">(9)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-208">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ba47-208">Device is not working properly.</span></span> <span data-ttu-id="6ba47-209">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-209">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="6ba47-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-210"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="6ba47-211">(10)</span><span class="sxs-lookup"><span data-stu-id="6ba47-211">(10)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-212">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="6ba47-212">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="6ba47-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-213"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="6ba47-214">(11)</span><span class="sxs-lookup"><span data-stu-id="6ba47-214">(11)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-215">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-215">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="6ba47-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-216"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="6ba47-217">(12)</span><span class="sxs-lookup"><span data-stu-id="6ba47-217">(12)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-218">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="6ba47-218">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="6ba47-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-219"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="6ba47-220">(13)</span><span class="sxs-lookup"><span data-stu-id="6ba47-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-221">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-221">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="6ba47-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-222"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="6ba47-223">(14)</span><span class="sxs-lookup"><span data-stu-id="6ba47-223">(14)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-224">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-224">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="6ba47-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-225"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="6ba47-226">(15)</span><span class="sxs-lookup"><span data-stu-id="6ba47-226">(15)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-227">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="6ba47-227">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="6ba47-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-228"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="6ba47-229">(16)</span><span class="sxs-lookup"><span data-stu-id="6ba47-229">(16)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-230">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-230">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="6ba47-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-231"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="6ba47-232">(17)</span><span class="sxs-lookup"><span data-stu-id="6ba47-232">(17)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-233">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="6ba47-233">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6ba47-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-234"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="6ba47-235">(18)</span><span class="sxs-lookup"><span data-stu-id="6ba47-235">(18)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-236">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6ba47-236">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="6ba47-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-237"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="6ba47-238">(19)</span><span class="sxs-lookup"><span data-stu-id="6ba47-238">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="6ba47-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-239"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="6ba47-240">(20)</span><span class="sxs-lookup"><span data-stu-id="6ba47-240">(20)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-241">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="6ba47-241">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="6ba47-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="6ba47-243">(21)</span><span class="sxs-lookup"><span data-stu-id="6ba47-243">(21)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ba47-244">System failure.</span></span> <span data-ttu-id="6ba47-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="6ba47-245">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="6ba47-246">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-246">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="6ba47-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-247"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="6ba47-248">(22)</span><span class="sxs-lookup"><span data-stu-id="6ba47-248">(22)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-249">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="6ba47-249">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="6ba47-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-250"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="6ba47-251">(23)</span><span class="sxs-lookup"><span data-stu-id="6ba47-251">(23)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-252">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="6ba47-252">System failure.</span></span> <span data-ttu-id="6ba47-253">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="6ba47-253">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="6ba47-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-254"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="6ba47-255">(24)</span><span class="sxs-lookup"><span data-stu-id="6ba47-255">(24)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-256">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="6ba47-256">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6ba47-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6ba47-258">(25)</span><span class="sxs-lookup"><span data-stu-id="6ba47-258">(25)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-259">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="6ba47-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="6ba47-261">(26)</span><span class="sxs-lookup"><span data-stu-id="6ba47-261">(26)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-262">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="6ba47-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-263"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="6ba47-264">(27)</span><span class="sxs-lookup"><span data-stu-id="6ba47-264">(27)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-265">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="6ba47-265">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="6ba47-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-266"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="6ba47-267">(28)</span><span class="sxs-lookup"><span data-stu-id="6ba47-267">(28)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-268">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="6ba47-268">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="6ba47-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-269"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="6ba47-270">(29)</span><span class="sxs-lookup"><span data-stu-id="6ba47-270">(29)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-271">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="6ba47-271">Device is disabled.</span></span> <span data-ttu-id="6ba47-272">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="6ba47-272">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="6ba47-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-273"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="6ba47-274">(30)</span><span class="sxs-lookup"><span data-stu-id="6ba47-274">(30)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-275">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="6ba47-275">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="6ba47-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="6ba47-276"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="6ba47-277">31</span><span class="sxs-lookup"><span data-stu-id="6ba47-277">(31)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-278">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ba47-278">Device is not working properly.</span></span> <span data-ttu-id="6ba47-279">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="6ba47-279">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ba47-280">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="6ba47-280">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-281">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6ba47-281">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-283">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6ba47-283">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-284">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6ba47-284">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="6ba47-285">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-286">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6ba47-286">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-287">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-289">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6ba47-289">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-290">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="6ba47-290">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="6ba47-291">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="6ba47-291">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6ba47-292">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-293">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6ba47-293">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-294">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-296">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="6ba47-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-297">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6ba47-297">Description of the object.</span></span>

<span data-ttu-id="6ba47-298">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-298">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-299">**ID**</span><span class="sxs-lookup"><span data-stu-id="6ba47-299">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-300">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-301">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-302">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api de \| Windows GDI \| HMONITOR")</span><span class="sxs-lookup"><span data-stu-id="6ba47-302">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Windows GDI\|HMONITOR")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-303">Identificador único de un monitor de escritorio.</span><span class="sxs-lookup"><span data-stu-id="6ba47-303">Unique identifier of a desktop monitor.</span></span>

<span data-ttu-id="6ba47-304">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-305">**TipoDePresentación**</span><span class="sxs-lookup"><span data-stu-id="6ba47-305">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-306">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ba47-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-308">Tipo de monitor de escritorio o CRT.</span><span class="sxs-lookup"><span data-stu-id="6ba47-308">Type of desktop monitor or CRT.</span></span>

<span data-ttu-id="6ba47-309">Esta propiedad se hereda de [**\_ DesktopMonitor CIM**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-309">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ba47-310">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6ba47-310">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ba47-311">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="6ba47-311">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Color"></span><span id="multiscan_color"></span><span id="MULTISCAN_COLOR"></span>

<span data-ttu-id="6ba47-312">**Color de Multiscan** (2)</span><span class="sxs-lookup"><span data-stu-id="6ba47-312">**Multiscan Color** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiscan_Monochrome"></span><span id="multiscan_monochrome"></span><span id="MULTISCAN_MONOCHROME"></span>

<span data-ttu-id="6ba47-313">**Monocromo Multiscan** (3)</span><span class="sxs-lookup"><span data-stu-id="6ba47-313">**Multiscan Monochrome** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Color"></span><span id="fixed_frequency_color"></span><span id="FIXED_FREQUENCY_COLOR"></span>

<span data-ttu-id="6ba47-314">**Color de frecuencia fijo** (4)</span><span class="sxs-lookup"><span data-stu-id="6ba47-314">**Fixed Frequency Color** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Frequency_Monochrome"></span><span id="fixed_frequency_monochrome"></span><span id="FIXED_FREQUENCY_MONOCHROME"></span>

<span data-ttu-id="6ba47-315">**Monocromática de frecuencia fija** (5)</span><span class="sxs-lookup"><span data-stu-id="6ba47-315">**Fixed Frequency Monochrome** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6ba47-316">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="6ba47-316">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-317">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6ba47-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-319">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="6ba47-319">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="6ba47-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-321">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6ba47-321">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-324">Cadena de forma libre que proporciona más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="6ba47-324">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="6ba47-325">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-326">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6ba47-326">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-327">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6ba47-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-329">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="6ba47-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-330">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="6ba47-330">Date and time the object was installed.</span></span> <span data-ttu-id="6ba47-331">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="6ba47-331">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="6ba47-332">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-332">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-333">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="6ba47-333">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-334">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6ba47-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-336">Si es **true**, el dispositivo está bloqueado, lo que impide la entrada o salida del usuario.</span><span class="sxs-lookup"><span data-stu-id="6ba47-336">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="6ba47-337">Esta propiedad se hereda de [**\_ UserDevice CIM**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-337">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-338">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6ba47-338">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-339">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ba47-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-341">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6ba47-341">Last error code reported by the logical device.</span></span>

<span data-ttu-id="6ba47-342">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-343">**MonitorManufacturer**</span><span class="sxs-lookup"><span data-stu-id="6ba47-343">**MonitorManufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-344">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-345">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-346">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="6ba47-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-347">Nombre del fabricante del monitor.</span><span class="sxs-lookup"><span data-stu-id="6ba47-347">Name of the monitor manufacturer.</span></span>

<span data-ttu-id="6ba47-348">Ejemplo: "NEC"</span><span class="sxs-lookup"><span data-stu-id="6ba47-348">Example: "NEC"</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-349">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6ba47-349">**MonitorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-352">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="6ba47-352">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-353">Tipo de monitor.</span><span class="sxs-lookup"><span data-stu-id="6ba47-353">Type of monitor.</span></span>

<span data-ttu-id="6ba47-354">Ejemplo: "NEC 5FGp"</span><span class="sxs-lookup"><span data-stu-id="6ba47-354">Example: "NEC 5FGp"</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-355">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6ba47-355">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-356">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-358">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6ba47-358">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-359">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="6ba47-359">Label by which the object is known.</span></span> <span data-ttu-id="6ba47-360">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="6ba47-360">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="6ba47-361">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-361">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-362">**PixelsPerXLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="6ba47-362">**PixelsPerXLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-363">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ba47-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-365">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Device context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles por pulgada lógica")</span><span class="sxs-lookup"><span data-stu-id="6ba47-365">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-366">Resolución a lo largo del eje x (dirección horizontal) del monitor.</span><span class="sxs-lookup"><span data-stu-id="6ba47-366">Resolution along the x-axis (horizontal direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-367">**PixelsPerYLogicalInch**</span><span class="sxs-lookup"><span data-stu-id="6ba47-367">**PixelsPerYLogicalInch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-368">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ba47-368">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-370">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Device context Functions \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles por pulgada lógica")</span><span class="sxs-lookup"><span data-stu-id="6ba47-370">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Context Functions\|[**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps)"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per logical inch")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-371">Resolución a lo largo del eje y (dirección vertical) del monitor.</span><span class="sxs-lookup"><span data-stu-id="6ba47-371">Resolution along the y-axis (vertical direction) of the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-372">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="6ba47-372">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-375">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="6ba47-375">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-376">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6ba47-376">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="6ba47-377">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="6ba47-378">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="6ba47-378">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-379">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6ba47-379">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-380">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ba47-380">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-382">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6ba47-382">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="6ba47-383">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-383">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ba47-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6ba47-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="6ba47-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="6ba47-385"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-386">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-386">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6ba47-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="6ba47-387"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6ba47-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="6ba47-388"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-389">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="6ba47-389">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="6ba47-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="6ba47-390"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-391">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="6ba47-391">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="6ba47-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="6ba47-392"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-393">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="6ba47-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="6ba47-394">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="6ba47-394">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="6ba47-395">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="6ba47-395">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="6ba47-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="6ba47-396"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-397">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="6ba47-397">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="6ba47-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="6ba47-398"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6ba47-399">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="6ba47-399">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6ba47-400">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="6ba47-400">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-401">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6ba47-401">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-403">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="6ba47-403">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="6ba47-404">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="6ba47-404">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="6ba47-405">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-405">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-406">**ScreenHeight**</span><span class="sxs-lookup"><span data-stu-id="6ba47-406">**ScreenHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-407">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ba47-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-409">Alto lógico de la pantalla en las coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6ba47-409">Logical height of the display in screen coordinates.</span></span>

<span data-ttu-id="6ba47-410">Esta propiedad se hereda de [**\_ DesktopMonitor CIM**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-410">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-411">**ScreenWidth**</span><span class="sxs-lookup"><span data-stu-id="6ba47-411">**ScreenWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-412">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6ba47-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-414">Ancho lógico de la pantalla en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="6ba47-414">Logical width of the display in screen coordinates.</span></span>

<span data-ttu-id="6ba47-415">Esta propiedad se hereda de [**\_ DesktopMonitor CIM**](cim-desktopmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-415">This property is inherited from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-416">**Estado**</span><span class="sxs-lookup"><span data-stu-id="6ba47-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-417">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-419">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="6ba47-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-420">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6ba47-420">Current status of the object.</span></span> <span data-ttu-id="6ba47-421">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="6ba47-421">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6ba47-422">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="6ba47-422">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6ba47-423">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="6ba47-423">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6ba47-424">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="6ba47-424">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6ba47-425">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="6ba47-425">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6ba47-426">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6ba47-427">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="6ba47-427">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6ba47-428">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="6ba47-428">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6ba47-429">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="6ba47-429">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6ba47-430">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6ba47-430">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ba47-431">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="6ba47-431">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6ba47-432">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="6ba47-432">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6ba47-433">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="6ba47-433">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6ba47-434">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="6ba47-434">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6ba47-435">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="6ba47-435">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6ba47-436">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="6ba47-436">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6ba47-437">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6ba47-437">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6ba47-438">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="6ba47-438">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6ba47-439">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="6ba47-439">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6ba47-440">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="6ba47-440">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-441">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ba47-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-443">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="6ba47-443">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-444">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="6ba47-444">State of the logical device.</span></span> <span data-ttu-id="6ba47-445">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="6ba47-445">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="6ba47-446">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-446">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6ba47-447">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="6ba47-447">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ba47-448">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="6ba47-448">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="6ba47-449">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="6ba47-449">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="6ba47-450">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="6ba47-450">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="6ba47-451">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="6ba47-451">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6ba47-452">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6ba47-452">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-453">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-454">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-455">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6ba47-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-456">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="6ba47-456">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="6ba47-457">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ba47-458">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6ba47-458">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ba47-459">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ba47-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba47-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ba47-461">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6ba47-461">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6ba47-462">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="6ba47-462">Name of the scoping system.</span></span>

<span data-ttu-id="6ba47-463">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-463">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ba47-464">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ba47-464">Remarks</span></span>

<span data-ttu-id="6ba47-465">La **clase \_ DesktopMonitor de Win32** se deriva de [**\_ DesktopMonitor de CIM**](cim-desktopmonitor.md), que se deriva de la [**\_ presentación de CIM**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-465">The **Win32\_DesktopMonitor** class is derived from [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), which derives from [**CIM\_Display**](cim-display.md).</span></span> <span data-ttu-id="6ba47-466">**CIM \_ La presentación** se deriva de [**CIM \_ UserDevice**](cim-userdevice.md), que se deriva de un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="6ba47-466">**CIM\_Display** is derived from [**CIM\_UserDevice**](cim-userdevice.md), which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6ba47-467">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6ba47-467">Examples</span></span>

<span data-ttu-id="6ba47-468">En el ejemplo de [creación de un dibujo de configuración de equipo con Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell en la galería de TechNet se usa **Win32 \_ DesktopMonitor** para interactuar con el modelo de automatización de Visio con el fin de crear un dibujo de Visio.</span><span class="sxs-lookup"><span data-stu-id="6ba47-468">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_DesktopMonitor** to interact with the Visio automation model to create a Visio drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba47-469">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba47-469">Requirements</span></span>



| <span data-ttu-id="6ba47-470">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba47-470">Requirement</span></span> | <span data-ttu-id="6ba47-471">Value</span><span class="sxs-lookup"><span data-stu-id="6ba47-471">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba47-472">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ba47-472">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba47-473">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ba47-473">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ba47-474">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ba47-474">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba47-475">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ba47-475">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ba47-476">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6ba47-476">Namespace</span></span><br/>                | <span data-ttu-id="6ba47-477">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6ba47-477">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ba47-478">MOF</span><span class="sxs-lookup"><span data-stu-id="6ba47-478">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ba47-479"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ba47-479"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ba47-480">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ba47-480">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ba47-481"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ba47-481"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba47-482">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba47-482">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba47-483">**\_DESKTOPMONITOR CIM**</span><span class="sxs-lookup"><span data-stu-id="6ba47-483">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dt>

[<span data-ttu-id="6ba47-484">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="6ba47-484">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="6ba47-485">Tareas WMI: administración de escritorio</span><span class="sxs-lookup"><span data-stu-id="6ba47-485">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

