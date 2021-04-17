---
description: La \_ clase WMI SCSIController de Win32 representa una controladora SCSI en un equipo que ejecuta Windows.
ms.assetid: 14ed523e-d505-40fa-81d5-3a71eb9f078e
ms.tgt_platform: multiple
title: Win32_SCSIController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIController
- Win32_SCSIController.Reset
- Win32_SCSIController.SetPowerState
- Win32_SCSIController.Availability
- Win32_SCSIController.Caption
- Win32_SCSIController.ConfigManagerErrorCode
- Win32_SCSIController.ConfigManagerUserConfig
- Win32_SCSIController.ControllerTimeouts
- Win32_SCSIController.CreationClassName
- Win32_SCSIController.Description
- Win32_SCSIController.DeviceID
- Win32_SCSIController.DeviceMap
- Win32_SCSIController.DriverName
- Win32_SCSIController.ErrorCleared
- Win32_SCSIController.ErrorDescription
- Win32_SCSIController.HardwareVersion
- Win32_SCSIController.Index
- Win32_SCSIController.InstallDate
- Win32_SCSIController.LastErrorCode
- Win32_SCSIController.Manufacturer
- Win32_SCSIController.MaxDataWidth
- Win32_SCSIController.MaxNumberControlled
- Win32_SCSIController.MaxTransferRate
- Win32_SCSIController.Name
- Win32_SCSIController.PNPDeviceID
- Win32_SCSIController.PowerManagementCapabilities
- Win32_SCSIController.PowerManagementSupported
- Win32_SCSIController.ProtectionManagement
- Win32_SCSIController.ProtocolSupported
- Win32_SCSIController.Status
- Win32_SCSIController.StatusInfo
- Win32_SCSIController.SystemCreationClassName
- Win32_SCSIController.SystemName
- Win32_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f8ba77d626ada787ed18fd9855333fa813f3ab7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659739"
---
# <a name="win32_scsicontroller-class"></a><span data-ttu-id="a43a9-103">\_Clase Win32 SCSIController</span><span class="sxs-lookup"><span data-stu-id="a43a9-103">Win32\_SCSIController class</span></span>

<span data-ttu-id="a43a9-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SCSIController de Win32** representa una controladora SCSI en un equipo que ejecuta Windows.</span><span class="sxs-lookup"><span data-stu-id="a43a9-104">The **Win32\_SCSIController** [WMI class](../wmisdk/retrieving-a-class.md) represents a SCSI controller on a computer system running Windows.</span></span>

<span data-ttu-id="a43a9-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a43a9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a43a9-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a43a9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a43a9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a43a9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SCSIController : CIM_SCSIController
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  string   DeviceMap;
  string   DriverName;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareVersion;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="a43a9-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a43a9-108">Members</span></span>

<span data-ttu-id="a43a9-109">La **clase \_ SCSIController de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a43a9-109">The **Win32\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="a43a9-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a43a9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a43a9-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a43a9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a43a9-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a43a9-112">Methods</span></span>

<span data-ttu-id="a43a9-113">La clase **Win32 \_ SCSIController** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a43a9-113">The **Win32\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="a43a9-114">Método</span><span class="sxs-lookup"><span data-stu-id="a43a9-114">Method</span></span>            | <span data-ttu-id="a43a9-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a43a9-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a43a9-116">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a43a9-116">**Reset**</span></span>         | <span data-ttu-id="a43a9-117">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="a43a9-117">Not implemented.</span></span> <span data-ttu-id="a43a9-118">Para implementar este método, consulte el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/>                 |
| <span data-ttu-id="a43a9-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a43a9-119">**SetPowerState**</span></span> | <span data-ttu-id="a43a9-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="a43a9-120">Not implemented.</span></span> <span data-ttu-id="a43a9-121">Para implementar este método, consulte el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ SCSIController**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a43a9-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a43a9-122">Properties</span></span>

<span data-ttu-id="a43a9-123">La **clase \_ SCSIController de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a43a9-123">The **Win32\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a43a9-124">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="a43a9-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a43a9-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-127">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="a43a9-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-128">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-128">Availability and status of the device.</span></span>

<span data-ttu-id="a43a9-129">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a43a9-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a43a9-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a43a9-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a43a9-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a43a9-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="a43a9-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-133">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="a43a9-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a43a9-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="a43a9-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a43a9-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="a43a9-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a43a9-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="a43a9-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a43a9-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="a43a9-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a43a9-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="a43a9-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a43a9-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="a43a9-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a43a9-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="a43a9-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a43a9-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="a43a9-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a43a9-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="a43a9-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a43a9-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="a43a9-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-144">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="a43a9-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a43a9-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="a43a9-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-146">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="a43a9-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a43a9-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="a43a9-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-148">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="a43a9-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a43a9-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="a43a9-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a43a9-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="a43a9-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-151">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="a43a9-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a43a9-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="a43a9-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-153">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="a43a9-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a43a9-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="a43a9-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-155">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a43a9-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="a43a9-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-157">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="a43a9-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a43a9-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="a43a9-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-159">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="a43a9-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a43a9-160">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a43a9-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-163">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a43a9-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-164">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a43a9-164">Short description of the object.</span></span>

<span data-ttu-id="a43a9-165">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-166">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a43a9-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-167">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a43a9-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-169">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a43a9-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-170">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="a43a9-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a43a9-171">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a43a9-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a43a9-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="a43a9-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-174">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a43a9-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a43a9-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a43a9-176">(1)</span><span class="sxs-lookup"><span data-stu-id="a43a9-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-177">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a43a9-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a43a9-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a43a9-179">(2)</span><span class="sxs-lookup"><span data-stu-id="a43a9-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a43a9-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a43a9-181">(3)</span><span class="sxs-lookup"><span data-stu-id="a43a9-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-182">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="a43a9-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a43a9-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a43a9-184">(4)</span><span class="sxs-lookup"><span data-stu-id="a43a9-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-185">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a43a9-185">Device is not working properly.</span></span> <span data-ttu-id="a43a9-186">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="a43a9-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a43a9-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a43a9-188">(5)</span><span class="sxs-lookup"><span data-stu-id="a43a9-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-189">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="a43a9-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a43a9-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a43a9-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="a43a9-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-192">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a43a9-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a43a9-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a43a9-194">(7)</span><span class="sxs-lookup"><span data-stu-id="a43a9-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a43a9-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a43a9-196">(8)</span><span class="sxs-lookup"><span data-stu-id="a43a9-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-197">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a43a9-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a43a9-199">(9)</span><span class="sxs-lookup"><span data-stu-id="a43a9-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-200">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a43a9-200">Device is not working properly.</span></span> <span data-ttu-id="a43a9-201">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a43a9-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a43a9-203">(10)</span><span class="sxs-lookup"><span data-stu-id="a43a9-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-204">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="a43a9-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a43a9-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a43a9-206">(11)</span><span class="sxs-lookup"><span data-stu-id="a43a9-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-207">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a43a9-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a43a9-209">(12)</span><span class="sxs-lookup"><span data-stu-id="a43a9-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-210">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="a43a9-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a43a9-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a43a9-212">(13)</span><span class="sxs-lookup"><span data-stu-id="a43a9-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-213">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a43a9-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a43a9-215">(14)</span><span class="sxs-lookup"><span data-stu-id="a43a9-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-216">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a43a9-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a43a9-218">(15)</span><span class="sxs-lookup"><span data-stu-id="a43a9-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-219">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="a43a9-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a43a9-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a43a9-221">(16)</span><span class="sxs-lookup"><span data-stu-id="a43a9-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-222">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a43a9-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a43a9-224">(17)</span><span class="sxs-lookup"><span data-stu-id="a43a9-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-225">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="a43a9-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a43a9-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a43a9-227">(18)</span><span class="sxs-lookup"><span data-stu-id="a43a9-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-228">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a43a9-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a43a9-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a43a9-230">(19)</span><span class="sxs-lookup"><span data-stu-id="a43a9-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a43a9-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a43a9-232">(20)</span><span class="sxs-lookup"><span data-stu-id="a43a9-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-233">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="a43a9-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a43a9-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a43a9-235">(21)</span><span class="sxs-lookup"><span data-stu-id="a43a9-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-236">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="a43a9-236">System failure.</span></span> <span data-ttu-id="a43a9-237">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="a43a9-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a43a9-238">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a43a9-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a43a9-240">(22)</span><span class="sxs-lookup"><span data-stu-id="a43a9-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-241">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="a43a9-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a43a9-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a43a9-243">(23)</span><span class="sxs-lookup"><span data-stu-id="a43a9-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-244">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="a43a9-244">System failure.</span></span> <span data-ttu-id="a43a9-245">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="a43a9-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a43a9-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a43a9-247">(24)</span><span class="sxs-lookup"><span data-stu-id="a43a9-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-248">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="a43a9-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a43a9-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a43a9-250">(25)</span><span class="sxs-lookup"><span data-stu-id="a43a9-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-251">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a43a9-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a43a9-253">(26)</span><span class="sxs-lookup"><span data-stu-id="a43a9-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-254">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a43a9-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a43a9-256">(27)</span><span class="sxs-lookup"><span data-stu-id="a43a9-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-257">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="a43a9-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a43a9-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a43a9-259">(28)</span><span class="sxs-lookup"><span data-stu-id="a43a9-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-260">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="a43a9-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a43a9-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a43a9-262">(29)</span><span class="sxs-lookup"><span data-stu-id="a43a9-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-263">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="a43a9-263">Device is disabled.</span></span> <span data-ttu-id="a43a9-264">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a43a9-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a43a9-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a43a9-266">(30)</span><span class="sxs-lookup"><span data-stu-id="a43a9-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-267">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="a43a9-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a43a9-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="a43a9-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a43a9-269">31</span><span class="sxs-lookup"><span data-stu-id="a43a9-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-270">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="a43a9-270">Device is not working properly.</span></span> <span data-ttu-id="a43a9-271">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a43a9-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a43a9-272">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="a43a9-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-273">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a43a9-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-275">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a43a9-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-276">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a43a9-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a43a9-277">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-278">**ControllerTimeouts**</span><span class="sxs-lookup"><span data-stu-id="a43a9-278">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-279">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a43a9-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-281">Número de tiempos de espera que se han producido después del valor de **TimeOfLastReset** .</span><span class="sxs-lookup"><span data-stu-id="a43a9-281">Number of time-outs that have occurred after the **TimeOfLastReset** value.</span></span>

<span data-ttu-id="a43a9-282">Esta propiedad se hereda de [**\_ SCSIController CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-282">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a43a9-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-284">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-286">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a43a9-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-287">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="a43a9-287">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a43a9-288">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="a43a9-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="a43a9-289">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-290">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a43a9-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-291">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-293">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="a43a9-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-294">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a43a9-294">Description of the object.</span></span>

<span data-ttu-id="a43a9-295">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-296">**ID**</span><span class="sxs-lookup"><span data-stu-id="a43a9-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-297">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-299">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| hardware \\ \\ DeviceMap \\ \\ SCSI")</span><span class="sxs-lookup"><span data-stu-id="a43a9-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-300">Identificador único de la controladora SCSI con otros dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="a43a9-300">Unique identifier of the SCSI controller with other devices on the system.</span></span>

<span data-ttu-id="a43a9-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-302">**DeviceMap**</span><span class="sxs-lookup"><span data-stu-id="a43a9-302">**DeviceMap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-305">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| hardware \\ \\ DeviceMap \\ \\ SCSI \| ScsiPort")</span><span class="sxs-lookup"><span data-stu-id="a43a9-305">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-306">Orden en que se enumeran los dispositivos con este controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="a43a9-306">Order in which the devices are listed with this SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-307">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="a43a9-307">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-308">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-310">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| PortDriver")</span><span class="sxs-lookup"><span data-stu-id="a43a9-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|PortDriver")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-311">Nombre del archivo del controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="a43a9-311">Driver file name of the SCSI controller.</span></span>

<span data-ttu-id="a43a9-312">Ejemplo: "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="a43a9-312">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-313">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="a43a9-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-314">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a43a9-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-316">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="a43a9-316">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="a43a9-317">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a43a9-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-321">Cadena de forma libre que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="a43a9-321">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="a43a9-322">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-323">**HardwareVersion**</span><span class="sxs-lookup"><span data-stu-id="a43a9-323">**HardwareVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-326">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ enum \\ \\ root \| HWRevision")</span><span class="sxs-lookup"><span data-stu-id="a43a9-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|HWRevision")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-327">Número de versión de hardware de la controladora SCSI.</span><span class="sxs-lookup"><span data-stu-id="a43a9-327">Hardware version number of the SCSI controller.</span></span>

<span data-ttu-id="a43a9-328">Ejemplo: "1,25"</span><span class="sxs-lookup"><span data-stu-id="a43a9-328">Example: "1.25"</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-329">**Index**</span><span class="sxs-lookup"><span data-stu-id="a43a9-329">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-330">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a43a9-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-332">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| hardware \\ \\ DeviceMap \\ \\ SCSI \| ScsiPort")</span><span class="sxs-lookup"><span data-stu-id="a43a9-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-333">Número de índice de la controladora SCSI en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="a43a9-333">Index number of the SCSI controller in the system registry.</span></span>

<span data-ttu-id="a43a9-334">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="a43a9-334">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a43a9-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-336">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a43a9-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-338">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="a43a9-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-339">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a43a9-339">Date and time the object was installed.</span></span> <span data-ttu-id="a43a9-340">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a43a9-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a43a9-341">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-342">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="a43a9-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-343">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a43a9-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-345">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a43a9-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a43a9-346">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-347">**Le**</span><span class="sxs-lookup"><span data-stu-id="a43a9-347">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-348">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-350">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ enum \\ \\ root \| Mfg")</span><span class="sxs-lookup"><span data-stu-id="a43a9-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-351">Nombre del fabricante del controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="a43a9-351">Name of the SCSI controller manufacturer.</span></span>

<span data-ttu-id="a43a9-352">Ejemplo: "Adaptec"</span><span class="sxs-lookup"><span data-stu-id="a43a9-352">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-353">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="a43a9-353">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-354">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a43a9-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-356">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits")</span><span class="sxs-lookup"><span data-stu-id="a43a9-356">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-357">Ancho de datos máximo (en bits) admitido por la controladora SCSI.</span><span class="sxs-lookup"><span data-stu-id="a43a9-357">Maximum data width (in bits) supported by the SCSI controller.</span></span>

<span data-ttu-id="a43a9-358">Esta propiedad se hereda de [**\_ SCSIController CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-358">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-359">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="a43a9-359">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-360">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a43a9-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-362">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="a43a9-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-363">Número máximo de entidades directamente direccionables admitidas por este controlador.</span><span class="sxs-lookup"><span data-stu-id="a43a9-363">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="a43a9-364">Se debe utilizar un valor de 0 (cero) si se desconoce el número.</span><span class="sxs-lookup"><span data-stu-id="a43a9-364">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="a43a9-365">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-365">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-366">**MaxTransferRate**</span><span class="sxs-lookup"><span data-stu-id="a43a9-366">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-367">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a43a9-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-369">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="a43a9-369">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-370">Velocidad de transferencia máxima (en bits por segundo) admitida por el controlador SCSI.</span><span class="sxs-lookup"><span data-stu-id="a43a9-370">Maximum transfer rate (in bits per second) supported by the SCSI controller.</span></span>

<span data-ttu-id="a43a9-371">Esta propiedad se hereda de [**\_ SCSIController CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-371">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<span data-ttu-id="a43a9-372">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-373">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a43a9-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-376">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="a43a9-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-377">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a43a9-377">Label by which the object is known.</span></span> <span data-ttu-id="a43a9-378">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="a43a9-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a43a9-379">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a43a9-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-383">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a43a9-383">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-384">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a43a9-384">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a43a9-385">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a43a9-386">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a43a9-386">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-387">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a43a9-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-388">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a43a9-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-390">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a43a9-390">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a43a9-391">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="a43a9-391">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a43a9-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a43a9-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a43a9-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="a43a9-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a43a9-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="a43a9-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a43a9-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a43a9-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-396">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="a43a9-396">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a43a9-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="a43a9-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-398">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="a43a9-398">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a43a9-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="a43a9-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-400">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="a43a9-400">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a43a9-401">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="a43a9-401">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a43a9-402">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-402">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a43a9-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="a43a9-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-404">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="a43a9-404">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a43a9-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="a43a9-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a43a9-406">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="a43a9-406">Timed Power-On Supported</span></span>

<span data-ttu-id="a43a9-407">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="a43a9-407">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a43a9-408">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="a43a9-408">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-409">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a43a9-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-411">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="a43a9-411">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="a43a9-412">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="a43a9-412">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="a43a9-413">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-414">**ProtectionManagement**</span><span class="sxs-lookup"><span data-stu-id="a43a9-414">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-415">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a43a9-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-417">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Controlador de almacenamiento DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a43a9-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-418">Compatibilidad de la controladora SCSI para la redundancia o la protección frente a errores de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-418">Support of the SCSI controller for redundancy or protection against device failures.</span></span>

<span data-ttu-id="a43a9-419">Esta propiedad se hereda de [**\_ SCSIController CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-419">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a43a9-420">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a43a9-420">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a43a9-421">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a43a9-421">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="a43a9-422">Sin **protección** (3)</span><span class="sxs-lookup"><span data-stu-id="a43a9-422">**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="a43a9-423">**Protegido** (4)</span><span class="sxs-lookup"><span data-stu-id="a43a9-423">**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="a43a9-424">**Protegido a través de SCC (comando del controlador SCSI-3)** (5)</span><span class="sxs-lookup"><span data-stu-id="a43a9-424">**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="a43a9-425">**Protegido a través de SCC-2 (comando de controlador SCSI-3)** (6)</span><span class="sxs-lookup"><span data-stu-id="a43a9-425">**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a43a9-426">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="a43a9-426">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-427">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a43a9-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-429">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,2 "," MIF. \|Discos DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a43a9-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-430">Protocolo usado por el controlador para tener acceso a dispositivos "controlados".</span><span class="sxs-lookup"><span data-stu-id="a43a9-430">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="a43a9-431">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-431">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="a43a9-432">En la lista siguiente se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a43a9-432">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a43a9-433">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a43a9-433">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a43a9-434">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a43a9-434">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="a43a9-435">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="a43a9-435">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="a43a9-436">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="a43a9-436">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="a43a9-437">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="a43a9-437">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="a43a9-438">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="a43a9-438">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="a43a9-439">**Disco flexible** (7)</span><span class="sxs-lookup"><span data-stu-id="a43a9-439">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="a43a9-440">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="a43a9-440">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="a43a9-441">**Interfaz paralela SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="a43a9-441">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="a43a9-442">**Protocolo SCSI canal de fibra** (10)</span><span class="sxs-lookup"><span data-stu-id="a43a9-442">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="a43a9-443">**Protocolo de bus serie SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="a43a9-443">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="a43a9-444">**Protocolo de bus serie SCSI: 2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="a43a9-444">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="a43a9-445">**Arquitectura de almacenamiento en serie SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="a43a9-445">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="a43a9-446">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="a43a9-446">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="a43a9-447">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="a43a9-447">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="a43a9-448">**Bus serie universal** (16)</span><span class="sxs-lookup"><span data-stu-id="a43a9-448">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="a43a9-449">**Protocolo paralelo** (17)</span><span class="sxs-lookup"><span data-stu-id="a43a9-449">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="a43a9-450">**ESCON** (18)</span><span class="sxs-lookup"><span data-stu-id="a43a9-450">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="a43a9-451">**Diagnóstico** (19)</span><span class="sxs-lookup"><span data-stu-id="a43a9-451">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="a43a9-452">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="a43a9-452">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="a43a9-453">**Potencia** (21)</span><span class="sxs-lookup"><span data-stu-id="a43a9-453">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="a43a9-454">**HIPPI** (22)</span><span class="sxs-lookup"><span data-stu-id="a43a9-454">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="a43a9-455">**MultiBus** (23)</span><span class="sxs-lookup"><span data-stu-id="a43a9-455">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="a43a9-456">**VME** (24)</span><span class="sxs-lookup"><span data-stu-id="a43a9-456">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="a43a9-457">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="a43a9-457">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="a43a9-458">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="a43a9-458">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="a43a9-459">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="a43a9-459">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="a43a9-460">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="a43a9-460">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="a43a9-461">**IEEE 802,3 10Base2** (29)</span><span class="sxs-lookup"><span data-stu-id="a43a9-461">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="a43a9-462">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="a43a9-462">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="a43a9-463">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="a43a9-463">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="a43a9-464">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="a43a9-464">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="a43a9-465">**Token-ring IEEE 802,5** (33)</span><span class="sxs-lookup"><span data-stu-id="a43a9-465">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="a43a9-466">**FDDI ANSI x3t 9.5** (34)</span><span class="sxs-lookup"><span data-stu-id="a43a9-466">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="a43a9-467">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="a43a9-467">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="a43a9-468">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="a43a9-468">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="a43a9-469">**IDE** (37)</span><span class="sxs-lookup"><span data-stu-id="a43a9-469">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="a43a9-470">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="a43a9-470">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="a43a9-471">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="a43a9-471">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="a43a9-472">**DSSI** (40)</span><span class="sxs-lookup"><span data-stu-id="a43a9-472">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="a43a9-473">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="a43a9-473">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="a43a9-474">**ATA/IDE mejorado** (42)</span><span class="sxs-lookup"><span data-stu-id="a43a9-474">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="a43a9-475">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="a43a9-475">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="a43a9-476">**TWIRP (infrarrojo bidireccional)** (44)</span><span class="sxs-lookup"><span data-stu-id="a43a9-476">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="a43a9-477">**FIR (infrarrojo rápido)** (45)</span><span class="sxs-lookup"><span data-stu-id="a43a9-477">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="a43a9-478">**Sir (infrarrojos serie)** (46)</span><span class="sxs-lookup"><span data-stu-id="a43a9-478">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="a43a9-479">**IrBus** (47)</span><span class="sxs-lookup"><span data-stu-id="a43a9-479">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a43a9-480">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a43a9-480">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-481">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-483">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="a43a9-483">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-484">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a43a9-484">Current status of the object.</span></span> <span data-ttu-id="a43a9-485">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="a43a9-485">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a43a9-486">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a43a9-486">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a43a9-487">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="a43a9-487">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a43a9-488">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a43a9-488">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a43a9-489">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="a43a9-489">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a43a9-490">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-490">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a43a9-491">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a43a9-491">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a43a9-492">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="a43a9-492">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a43a9-493">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="a43a9-493">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a43a9-494">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a43a9-494">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a43a9-495">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="a43a9-495">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a43a9-496">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a43a9-496">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a43a9-497">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="a43a9-497">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a43a9-498">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="a43a9-498">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a43a9-499">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="a43a9-499">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a43a9-500">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="a43a9-500">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a43a9-501">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a43a9-501">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a43a9-502">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="a43a9-502">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a43a9-503">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="a43a9-503">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a43a9-504">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a43a9-504">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-505">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a43a9-505">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-506">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-507">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a43a9-507">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-508">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a43a9-508">State of the logical device.</span></span> <span data-ttu-id="a43a9-509">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="a43a9-509">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a43a9-510">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a43a9-511">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a43a9-511">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a43a9-512">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a43a9-512">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a43a9-513">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="a43a9-513">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a43a9-514">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="a43a9-514">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a43a9-515">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="a43a9-515">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a43a9-516">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a43a9-516">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-517">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-518">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-518">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-519">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a43a9-519">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-520">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a43a9-520">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="a43a9-521">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-522">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a43a9-522">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a43a9-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-525">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a43a9-525">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-526">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="a43a9-526">Name of the scoping system.</span></span>

<span data-ttu-id="a43a9-527">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a43a9-528">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="a43a9-528">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a9-529">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a43a9-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a43a9-530">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a43a9-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a43a9-531">Fecha y hora en que se restableció por última vez este controlador.</span><span class="sxs-lookup"><span data-stu-id="a43a9-531">Date and time this controller was last reset.</span></span> <span data-ttu-id="a43a9-532">Esto podría significar que el controlador se apagó o reinicializó.</span><span class="sxs-lookup"><span data-stu-id="a43a9-532">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="a43a9-533">Esta propiedad se hereda del [**\_ controlador CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-533">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a43a9-534">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a43a9-534">Remarks</span></span>

<span data-ttu-id="a43a9-535">La **clase \_ SCSIController de Win32** se deriva de [**\_ SCSIController de CIM**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="a43a9-535">The **Win32\_SCSIController** class is derived from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a43a9-536">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a43a9-536">Requirements</span></span>



| <span data-ttu-id="a43a9-537">Requisito</span><span class="sxs-lookup"><span data-stu-id="a43a9-537">Requirement</span></span> | <span data-ttu-id="a43a9-538">Value</span><span class="sxs-lookup"><span data-stu-id="a43a9-538">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a43a9-539">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a43a9-539">Minimum supported client</span></span><br/> | <span data-ttu-id="a43a9-540">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a43a9-540">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a43a9-541">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a43a9-541">Minimum supported server</span></span><br/> | <span data-ttu-id="a43a9-542">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a43a9-542">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a43a9-543">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a43a9-543">Namespace</span></span><br/>                | <span data-ttu-id="a43a9-544">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a43a9-544">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a43a9-545">MOF</span><span class="sxs-lookup"><span data-stu-id="a43a9-545">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a43a9-546"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a43a9-546"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a43a9-547">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a43a9-547">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a43a9-548"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a43a9-548"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a43a9-549">Vea también</span><span class="sxs-lookup"><span data-stu-id="a43a9-549">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43a9-550">**\_SCSICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="a43a9-550">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dt>

[<span data-ttu-id="a43a9-551">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="a43a9-551">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
