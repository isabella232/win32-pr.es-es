---
description: La \_ clase WMI de bus Win32 representa un bus físico tal como lo muestra un equipo que ejecuta un sistema operativo Windows. Cualquier instancia de un bus Windows es un descendiente (o miembro) de esta clase.
ms.assetid: 76ba15f4-8c7b-4713-b5a2-e444fbab064a
ms.tgt_platform: multiple
title: Win32_Bus (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Bus
- Win32_Bus.Reset
- Win32_Bus.SetPowerState
- Win32_Bus.Availability
- Win32_Bus.BusNum
- Win32_Bus.BusType
- Win32_Bus.Caption
- Win32_Bus.ConfigManagerErrorCode
- Win32_Bus.ConfigManagerUserConfig
- Win32_Bus.CreationClassName
- Win32_Bus.Description
- Win32_Bus.DeviceID
- Win32_Bus.ErrorCleared
- Win32_Bus.ErrorDescription
- Win32_Bus.InstallDate
- Win32_Bus.LastErrorCode
- Win32_Bus.Name
- Win32_Bus.PNPDeviceID
- Win32_Bus.PowerManagementCapabilities
- Win32_Bus.PowerManagementSupported
- Win32_Bus.Status
- Win32_Bus.StatusInfo
- Win32_Bus.SystemCreationClassName
- Win32_Bus.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac31a2187ee7e4974e1ddedbf084efd482748753
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907080"
---
# <a name="win32_bus-class"></a><span data-ttu-id="7e747-104">\_Clase de bus Win32</span><span class="sxs-lookup"><span data-stu-id="7e747-104">Win32\_Bus class</span></span>

<span data-ttu-id="7e747-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ bus Win32** representa un bus físico tal como lo muestra un equipo que ejecuta un sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="7e747-105">The **Win32\_Bus** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a physical bus as seen by a computer running a Windows operating system.</span></span> <span data-ttu-id="7e747-106">Cualquier instancia de un bus Windows es un descendiente (o miembro) de esta clase.</span><span class="sxs-lookup"><span data-stu-id="7e747-106">Any instance of a Windows bus is a descendant (or member) of this class.</span></span>

<span data-ttu-id="7e747-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7e747-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e747-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e747-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Bus : CIM_LogicalDevice
{
  uint16   Availability;
  uint32   BusNum;
  uint32   BusType;
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

## <a name="members"></a><span data-ttu-id="7e747-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e747-109">Members</span></span>

<span data-ttu-id="7e747-110">La clase de **\_ bus Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7e747-110">The **Win32\_Bus** class has these types of members:</span></span>

-   [<span data-ttu-id="7e747-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e747-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7e747-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e747-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7e747-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e747-113">Methods</span></span>

<span data-ttu-id="7e747-114">La clase de **\_ bus Win32** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7e747-114">The **Win32\_Bus** class has these methods.</span></span>



| <span data-ttu-id="7e747-115">Método</span><span class="sxs-lookup"><span data-stu-id="7e747-115">Method</span></span>            | <span data-ttu-id="7e747-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e747-116">Description</span></span>                                                                                                                                                                                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e747-117">**Reset**</span><span class="sxs-lookup"><span data-stu-id="7e747-117">**Reset**</span></span>         | <span data-ttu-id="7e747-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="7e747-118">Not implemented.</span></span> <span data-ttu-id="7e747-119">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**el \_ LogicalDevice de CIM**](cim-logicaldevice.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="7e747-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="7e747-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7e747-120">**SetPowerState**</span></span> | <span data-ttu-id="7e747-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="7e747-121">Not implemented.</span></span> <span data-ttu-id="7e747-122">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**el \_ LogicalDevice de CIM**](cim-logicaldevice.md) para obtener documentación.</span><span class="sxs-lookup"><span data-stu-id="7e747-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7e747-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e747-123">Properties</span></span>

<span data-ttu-id="7e747-124">La clase de **\_ bus Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7e747-124">The **Win32\_Bus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e747-125">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="7e747-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e747-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="7e747-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-129">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-129">Availability and status of the device.</span></span>

<span data-ttu-id="7e747-130">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7e747-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7e747-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e747-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7e747-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7e747-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="7e747-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-134">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="7e747-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7e747-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="7e747-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7e747-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="7e747-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7e747-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="7e747-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7e747-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="7e747-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7e747-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="7e747-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7e747-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="7e747-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7e747-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="7e747-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7e747-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="7e747-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7e747-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="7e747-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7e747-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="7e747-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-145">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="7e747-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7e747-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="7e747-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-147">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="7e747-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7e747-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="7e747-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-149">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="7e747-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7e747-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="7e747-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7e747-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="7e747-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-152">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="7e747-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7e747-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="7e747-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-154">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="7e747-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7e747-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="7e747-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-156">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="7e747-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7e747-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="7e747-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-158">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="7e747-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7e747-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="7e747-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-160">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="7e747-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7e747-161">**BusNum**</span><span class="sxs-lookup"><span data-stu-id="7e747-161">**BusNum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e747-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-164">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7e747-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-165">Número lógico asignado al bus físico.</span><span class="sxs-lookup"><span data-stu-id="7e747-165">Logical number assigned to the physical bus.</span></span>

<span data-ttu-id="7e747-166">Ejemplo: 1</span><span class="sxs-lookup"><span data-stu-id="7e747-166">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="7e747-167">**BusType**</span><span class="sxs-lookup"><span data-stu-id="7e747-167">**BusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-168">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e747-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-170">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| cHwRes \| tipo de interfaz \_ ")</span><span class="sxs-lookup"><span data-stu-id="7e747-170">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|cHwRes\|INTERFACE\_TYPE")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-171">Tipo del bus físico.</span><span class="sxs-lookup"><span data-stu-id="7e747-171">Type of the physical bus.</span></span> <span data-ttu-id="7e747-172">Este valor será uno de los valores de la enumeración de **\_ tipo de interfaz** definida en bus. h.</span><span class="sxs-lookup"><span data-stu-id="7e747-172">This value will be one of the values in the **INTERFACE\_TYPE** enumeration defined in Bus.h.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="7e747-173">**Undefined** (-1)</span><span class="sxs-lookup"><span data-stu-id="7e747-173">**Undefined** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="7e747-174">**Interno** (0)</span><span class="sxs-lookup"><span data-stu-id="7e747-174">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="7e747-175">**ISA** (1)</span><span class="sxs-lookup"><span data-stu-id="7e747-175">**ISA** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="7e747-176">**EISA** (2)</span><span class="sxs-lookup"><span data-stu-id="7e747-176">**EISA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MicroChannel"></span><span id="microchannel"></span><span id="MICROCHANNEL"></span>

<span data-ttu-id="7e747-177">**Microcanal** (3)</span><span class="sxs-lookup"><span data-stu-id="7e747-177">**MicroChannel** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboChannel"></span><span id="turbochannel"></span><span id="TURBOCHANNEL"></span>

<span data-ttu-id="7e747-178">**TurboChannel** (4)</span><span class="sxs-lookup"><span data-stu-id="7e747-178">**TurboChannel** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Bus"></span><span id="pci_bus"></span><span id="PCI_BUS"></span>

<span data-ttu-id="7e747-179">**Bus PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="7e747-179">**PCI Bus** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="7e747-180">**Bus VME** (6)</span><span class="sxs-lookup"><span data-stu-id="7e747-180">**VME Bus** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="7e747-181">**Nubus** (7)</span><span class="sxs-lookup"><span data-stu-id="7e747-181">**NuBus** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Bus"></span><span id="pcmcia_bus"></span><span id="PCMCIA_BUS"></span>

<span data-ttu-id="7e747-182">**Bus PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="7e747-182">**PCMCIA Bus** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="C_Bus"></span><span id="c_bus"></span><span id="C_BUS"></span>

<span data-ttu-id="7e747-183">**Bus C** (9)</span><span class="sxs-lookup"><span data-stu-id="7e747-183">**C Bus** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MPI_Bus"></span><span id="mpi_bus"></span><span id="MPI_BUS"></span>

<span data-ttu-id="7e747-184">**Bus MPI** (10)</span><span class="sxs-lookup"><span data-stu-id="7e747-184">**MPI Bus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MPSA_Bus"></span><span id="mpsa_bus"></span><span id="MPSA_BUS"></span>

<span data-ttu-id="7e747-185">**Bus MPSA** (11)</span><span class="sxs-lookup"><span data-stu-id="7e747-185">**MPSA Bus** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Processor"></span><span id="internal_processor"></span><span id="INTERNAL_PROCESSOR"></span>

<span data-ttu-id="7e747-186">**Procesador interno** (12)</span><span class="sxs-lookup"><span data-stu-id="7e747-186">**Internal Processor** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Power_Bus"></span><span id="internal_power_bus"></span><span id="INTERNAL_POWER_BUS"></span>

<span data-ttu-id="7e747-187">**Bus de alimentación interno** (13)</span><span class="sxs-lookup"><span data-stu-id="7e747-187">**Internal Power Bus** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_ISA_Bus"></span><span id="pnp_isa_bus"></span><span id="PNP_ISA_BUS"></span>

<span data-ttu-id="7e747-188">**Bus ISA de PNP** (14)</span><span class="sxs-lookup"><span data-stu-id="7e747-188">**PNP ISA Bus** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PNP_Bus"></span><span id="pnp_bus"></span><span id="PNP_BUS"></span>

<span data-ttu-id="7e747-189">**Bus PnP** (15)</span><span class="sxs-lookup"><span data-stu-id="7e747-189">**PNP Bus** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum_Interface_Type"></span><span id="maximum_interface_type"></span><span id="MAXIMUM_INTERFACE_TYPE"></span>

<span data-ttu-id="7e747-190">**Tipo de interfaz máximo** (16)</span><span class="sxs-lookup"><span data-stu-id="7e747-190">**Maximum Interface Type** (16)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e747-191">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7e747-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-194">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7e747-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-195">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="7e747-195">Short description of the object a one-line string.</span></span>

<span data-ttu-id="7e747-196">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-197">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7e747-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-198">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e747-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-200">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7e747-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-201">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="7e747-201">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7e747-202">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7e747-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="7e747-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="7e747-204"> (0)</span><span class="sxs-lookup"><span data-stu-id="7e747-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-205">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e747-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7e747-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="7e747-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="7e747-207">(1)</span><span class="sxs-lookup"><span data-stu-id="7e747-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-208">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e747-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7e747-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7e747-210">(2)</span><span class="sxs-lookup"><span data-stu-id="7e747-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7e747-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="7e747-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7e747-212">(3)</span><span class="sxs-lookup"><span data-stu-id="7e747-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-213">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="7e747-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7e747-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="7e747-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7e747-215">(4)</span><span class="sxs-lookup"><span data-stu-id="7e747-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-216">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e747-216">Device is not working properly.</span></span> <span data-ttu-id="7e747-217">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="7e747-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7e747-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="7e747-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7e747-219">(5)</span><span class="sxs-lookup"><span data-stu-id="7e747-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-220">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="7e747-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7e747-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="7e747-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7e747-222"> (6)</span><span class="sxs-lookup"><span data-stu-id="7e747-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-223">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7e747-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7e747-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="7e747-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="7e747-225">(7)</span><span class="sxs-lookup"><span data-stu-id="7e747-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7e747-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7e747-227">(8)</span><span class="sxs-lookup"><span data-stu-id="7e747-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-228">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7e747-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="7e747-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7e747-230">(9)</span><span class="sxs-lookup"><span data-stu-id="7e747-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-231">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e747-231">Device is not working properly.</span></span> <span data-ttu-id="7e747-232">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-232">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7e747-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="7e747-233"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="7e747-234">(10)</span><span class="sxs-lookup"><span data-stu-id="7e747-234">(10)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-235">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="7e747-235">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7e747-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-236"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="7e747-237">(11)</span><span class="sxs-lookup"><span data-stu-id="7e747-237">(11)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-238">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-238">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7e747-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="7e747-239"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7e747-240">(12)</span><span class="sxs-lookup"><span data-stu-id="7e747-240">(12)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-241">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="7e747-241">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7e747-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-242"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7e747-243">(13)</span><span class="sxs-lookup"><span data-stu-id="7e747-243">(13)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-244">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-244">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7e747-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-245"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7e747-246">(14)</span><span class="sxs-lookup"><span data-stu-id="7e747-246">(14)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-247">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="7e747-247">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7e747-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="7e747-248"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7e747-249">(15)</span><span class="sxs-lookup"><span data-stu-id="7e747-249">(15)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-250">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="7e747-250">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7e747-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-251"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7e747-252">(16)</span><span class="sxs-lookup"><span data-stu-id="7e747-252">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-253">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-253">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7e747-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="7e747-254"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7e747-255">(17)</span><span class="sxs-lookup"><span data-stu-id="7e747-255">(17)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-256">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="7e747-256">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7e747-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-257"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7e747-258">(18)</span><span class="sxs-lookup"><span data-stu-id="7e747-258">(18)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-259">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="7e747-259">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7e747-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="7e747-260"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="7e747-261">(19)</span><span class="sxs-lookup"><span data-stu-id="7e747-261">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7e747-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="7e747-262"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="7e747-263">(20)</span><span class="sxs-lookup"><span data-stu-id="7e747-263">(20)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-264">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="7e747-264">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7e747-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7e747-266">(21)</span><span class="sxs-lookup"><span data-stu-id="7e747-266">(21)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-267">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="7e747-267">System failure.</span></span> <span data-ttu-id="7e747-268">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="7e747-268">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="7e747-269">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-269">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7e747-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="7e747-270"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="7e747-271">(22)</span><span class="sxs-lookup"><span data-stu-id="7e747-271">(22)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-272">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7e747-272">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7e747-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="7e747-273"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7e747-274">(23)</span><span class="sxs-lookup"><span data-stu-id="7e747-274">(23)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-275">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="7e747-275">System failure.</span></span> <span data-ttu-id="7e747-276">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="7e747-276">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7e747-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="7e747-277"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7e747-278">(24)</span><span class="sxs-lookup"><span data-stu-id="7e747-278">(24)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-279">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="7e747-279">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7e747-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-280"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7e747-281">(25)</span><span class="sxs-lookup"><span data-stu-id="7e747-281">(25)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-282">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-282">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7e747-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-283"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="7e747-284">(26)</span><span class="sxs-lookup"><span data-stu-id="7e747-284">(26)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-285">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e747-285">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7e747-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="7e747-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7e747-287">(27)</span><span class="sxs-lookup"><span data-stu-id="7e747-287">(27)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-288">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="7e747-288">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7e747-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="7e747-289"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7e747-290">(28)</span><span class="sxs-lookup"><span data-stu-id="7e747-290">(28)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-291">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="7e747-291">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7e747-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="7e747-292"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7e747-293">(29)</span><span class="sxs-lookup"><span data-stu-id="7e747-293">(29)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-294">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="7e747-294">Device is disabled.</span></span> <span data-ttu-id="7e747-295">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7e747-295">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7e747-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="7e747-296"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7e747-297">(30)</span><span class="sxs-lookup"><span data-stu-id="7e747-297">(30)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-298">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="7e747-298">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7e747-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="7e747-299"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7e747-300">31</span><span class="sxs-lookup"><span data-stu-id="7e747-300">(31)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-301">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e747-301">Device is not working properly.</span></span> <span data-ttu-id="7e747-302">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7e747-302">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7e747-303">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="7e747-303">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-304">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7e747-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-306">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7e747-306">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-307">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7e747-307">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7e747-308">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-309">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7e747-309">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-310">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-312">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7e747-312">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7e747-313">Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="7e747-313">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="7e747-314">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="7e747-314">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="7e747-315">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-316">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7e747-316">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-319">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="7e747-319">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-320">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7e747-320">Description of the object.</span></span>

<span data-ttu-id="7e747-321">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-321">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-322">**ID**</span><span class="sxs-lookup"><span data-stu-id="7e747-322">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-323">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-325">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="7e747-325">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-326">Nombre único que identifica el bus.</span><span class="sxs-lookup"><span data-stu-id="7e747-326">Unique name that identifies the bus.</span></span>

<span data-ttu-id="7e747-327">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-328">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7e747-328">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-329">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7e747-329">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e747-331">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="7e747-331">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="7e747-332">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-333">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7e747-333">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e747-336">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="7e747-336">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="7e747-337">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7e747-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-339">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7e747-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-341">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="7e747-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-342">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e747-342">Date and time the object was installed.</span></span> <span data-ttu-id="7e747-343">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="7e747-343">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="7e747-344">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-345">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7e747-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-346">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e747-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e747-348">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7e747-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7e747-349">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-350">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7e747-350">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-351">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-352">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-353">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7e747-353">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-354">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e747-354">Label by which the object is known.</span></span> <span data-ttu-id="7e747-355">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="7e747-355">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7e747-356">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-357">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7e747-357">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-358">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-360">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7e747-360">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-361">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7e747-361">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7e747-362">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-362">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="7e747-363">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7e747-363">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="7e747-364">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7e747-364">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-365">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e747-365">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7e747-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e747-367">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7e747-367">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="7e747-368">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="7e747-368">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e747-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7e747-369"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7e747-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="7e747-370"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7e747-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="7e747-371"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7e747-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7e747-372"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-373">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="7e747-373">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7e747-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="7e747-374"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-375">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="7e747-375">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7e747-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="7e747-376"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-377">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="7e747-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="7e747-378">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="7e747-378">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="7e747-379">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7e747-379">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7e747-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="7e747-380"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-381">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="7e747-381">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7e747-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="7e747-382"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7e747-383">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="7e747-383">Timed Power-On Supported</span></span>

<span data-ttu-id="7e747-384">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="7e747-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7e747-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7e747-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-386">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7e747-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7e747-388">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="7e747-388">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="7e747-389">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="7e747-389">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="7e747-390">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-390">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-391">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7e747-391">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-392">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-394">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7e747-394">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-395">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="7e747-395">Current status of the object.</span></span> <span data-ttu-id="7e747-396">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="7e747-396">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="7e747-397">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="7e747-397">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="7e747-398">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="7e747-398">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7e747-399">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="7e747-399">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7e747-400">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="7e747-400">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7e747-401">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7e747-402">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="7e747-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7e747-403">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="7e747-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7e747-404">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="7e747-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7e747-405">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7e747-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e747-406">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="7e747-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7e747-407">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="7e747-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7e747-408">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="7e747-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7e747-409">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="7e747-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7e747-410">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="7e747-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7e747-411">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="7e747-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7e747-412">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7e747-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7e747-413">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="7e747-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7e747-414">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="7e747-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e747-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7e747-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-416">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7e747-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-418">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7e747-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7e747-419">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7e747-419">State of the logical device.</span></span> <span data-ttu-id="7e747-420">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="7e747-420">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="7e747-421">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7e747-422">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7e747-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7e747-423">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="7e747-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7e747-424">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="7e747-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7e747-425">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="7e747-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7e747-426">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="7e747-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7e747-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7e747-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-428">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-429">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-430">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7e747-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7e747-431">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7e747-431">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="7e747-432">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e747-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7e747-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e747-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e747-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e747-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e747-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e747-436">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7e747-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7e747-437">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="7e747-437">Name of the scoping system.</span></span>

<span data-ttu-id="7e747-438">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e747-439">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e747-439">Remarks</span></span>

<span data-ttu-id="7e747-440">La clase de **\_ bus Win32** se deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="7e747-440">The **Win32\_Bus** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e747-441">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e747-441">Requirements</span></span>



| <span data-ttu-id="7e747-442">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e747-442">Requirement</span></span> | <span data-ttu-id="7e747-443">Value</span><span class="sxs-lookup"><span data-stu-id="7e747-443">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e747-444">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e747-444">Minimum supported client</span></span><br/> | <span data-ttu-id="7e747-445">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e747-445">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e747-446">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e747-446">Minimum supported server</span></span><br/> | <span data-ttu-id="7e747-447">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e747-447">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e747-448">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e747-448">Namespace</span></span><br/>                | <span data-ttu-id="7e747-449">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7e747-449">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e747-450">MOF</span><span class="sxs-lookup"><span data-stu-id="7e747-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e747-451"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e747-451"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e747-452">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e747-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e747-453"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e747-453"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e747-454">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e747-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e747-455">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7e747-455">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="7e747-456">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="7e747-456">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

