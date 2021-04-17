---
description: La \_ clase WMI TapeDrive de Win32 representa una unidad de cinta en un equipo con Windows. Las unidades de cinta se distinguen principalmente por el hecho de que solo se puede tener acceso a ellas de forma secuencial.
ms.assetid: ceefec7b-a904-4b2f-a6b6-b84917a33023
ms.tgt_platform: multiple
title: Win32_TapeDrive (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TapeDrive
- Win32_TapeDrive.Reset
- Win32_TapeDrive.SetPowerState
- Win32_TapeDrive.Availability
- Win32_TapeDrive.Capabilities
- Win32_TapeDrive.CapabilityDescriptions
- Win32_TapeDrive.Caption
- Win32_TapeDrive.Compression
- Win32_TapeDrive.CompressionMethod
- Win32_TapeDrive.ConfigManagerErrorCode
- Win32_TapeDrive.ConfigManagerUserConfig
- Win32_TapeDrive.CreationClassName
- Win32_TapeDrive.DefaultBlockSize
- Win32_TapeDrive.Description
- Win32_TapeDrive.DeviceID
- Win32_TapeDrive.ECC
- Win32_TapeDrive.EOTWarningZoneSize
- Win32_TapeDrive.ErrorCleared
- Win32_TapeDrive.ErrorDescription
- Win32_TapeDrive.ErrorMethodology
- Win32_TapeDrive.FeaturesHigh
- Win32_TapeDrive.FeaturesLow
- Win32_TapeDrive.Id
- Win32_TapeDrive.InstallDate
- Win32_TapeDrive.LastErrorCode
- Win32_TapeDrive.Manufacturer
- Win32_TapeDrive.MaxBlockSize
- Win32_TapeDrive.MaxMediaSize
- Win32_TapeDrive.MaxPartitionCount
- Win32_TapeDrive.MediaType
- Win32_TapeDrive.MinBlockSize
- Win32_TapeDrive.Name
- Win32_TapeDrive.NeedsCleaning
- Win32_TapeDrive.NumberOfMediaSupported
- Win32_TapeDrive.Padding
- Win32_TapeDrive.PNPDeviceID
- Win32_TapeDrive.PowerManagementCapabilities
- Win32_TapeDrive.PowerManagementSupported
- Win32_TapeDrive.ReportSetMarks
- Win32_TapeDrive.Status
- Win32_TapeDrive.StatusInfo
- Win32_TapeDrive.SystemCreationClassName
- Win32_TapeDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c7e7d3b754a0399acb152dba043da269f67a06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659559"
---
# <a name="win32_tapedrive-class"></a><span data-ttu-id="bb9c8-104">Win32 \_ TapeDrive (clase)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-104">Win32\_TapeDrive class</span></span>

<span data-ttu-id="bb9c8-105">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ TapeDrive de Win32** representa una unidad de cinta en un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-105">The **Win32\_TapeDrive** [WMI class](../wmisdk/retrieving-a-class.md) represents a tape drive on a computer system running Windows.</span></span> <span data-ttu-id="bb9c8-106">Las unidades de cinta se distinguen principalmente por el hecho de que solo se puede tener acceso a ellas de forma secuencial.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-106">Tape drives are primarily distinguished by the fact that they can only be accessed sequentially.</span></span>

<span data-ttu-id="bb9c8-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bb9c8-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb9c8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb9c8-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TapeDrive : CIM_TapeDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   Compression;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  uint32   ECC;
  uint32   EOTWarningZoneSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   FeaturesHigh;
  uint32   FeaturesLow;
  string   Id;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint32   MaxPartitionCount;
  string   MediaType;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  uint32   Padding;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint32   ReportSetMarks;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="bb9c8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="bb9c8-110">Members</span></span>

<span data-ttu-id="bb9c8-111">La clase **Win32 \_ TapeDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bb9c8-111">The **Win32\_TapeDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="bb9c8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb9c8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bb9c8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb9c8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bb9c8-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb9c8-114">Methods</span></span>

<span data-ttu-id="bb9c8-115">La clase **Win32 \_ TapeDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-115">The **Win32\_TapeDrive** class has these methods.</span></span>



| <span data-ttu-id="bb9c8-116">Método</span><span class="sxs-lookup"><span data-stu-id="bb9c8-116">Method</span></span>            | <span data-ttu-id="bb9c8-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb9c8-117">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9c8-118">**Reset**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-118">**Reset**</span></span>         | <span data-ttu-id="bb9c8-119">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-119">Not implemented.</span></span> <span data-ttu-id="bb9c8-120">Para implementar este método, vea el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/>                 |
| <span data-ttu-id="bb9c8-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-121">**SetPowerState**</span></span> | <span data-ttu-id="bb9c8-122">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-122">Not implemented.</span></span> <span data-ttu-id="bb9c8-123">Para implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bb9c8-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb9c8-124">Properties</span></span>

<span data-ttu-id="bb9c8-125">La clase **Win32 \_ TapeDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-125">The **Win32\_TapeDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb9c8-126">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-129">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-130">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-130">Availability and status of the device.</span></span>

<span data-ttu-id="bb9c8-131">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb9c8-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb9c8-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="bb9c8-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-135">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="bb9c8-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="bb9c8-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="bb9c8-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bb9c8-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="bb9c8-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="bb9c8-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="bb9c8-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="bb9c8-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="bb9c8-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bb9c8-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="bb9c8-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="bb9c8-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="bb9c8-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-146">Se sabe que el dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="bb9c8-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-148">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="bb9c8-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-150">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="bb9c8-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="bb9c8-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-153">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="bb9c8-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-155">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="bb9c8-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-157">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="bb9c8-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-159">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="bb9c8-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-161">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-163">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-165">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-165">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-166">Matriz de funcionalidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-166">Array of capabilities of the media access device.</span></span> <span data-ttu-id="bb9c8-167">Por ejemplo, el dispositivo puede admitir el acceso aleatorio, medios extraíbles y limpieza automática.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-167">For example, the device may support Random Access, removable media and Automatic Cleaning.</span></span> <span data-ttu-id="bb9c8-168">En este caso, los valores 3, 7 y 9 se escribirían en la matriz.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-168">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="bb9c8-169">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-169">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb9c8-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb9c8-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-171"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="bb9c8-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="bb9c8-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="bb9c8-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-174"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="bb9c8-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-175"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="bb9c8-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-176"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="bb9c8-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-177"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-178">Admite medios extraíbles</span><span class="sxs-lookup"><span data-stu-id="bb9c8-178">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="bb9c8-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-179"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="bb9c8-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-180"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="bb9c8-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-181"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="bb9c8-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-182"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-183">Admite medios Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="bb9c8-183">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="bb9c8-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-184"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-186">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-188">Calificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-188">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-189">Matriz de cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de las características de dispositivos de acceso indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="bb9c8-189">Array of free-form strings providing more detailed explanations for any of the access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="bb9c8-190">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-190">Note that each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="bb9c8-191">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-191">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-192">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-192">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-195">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-195">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-196">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-196">Short description of the object.</span></span>

<span data-ttu-id="bb9c8-197">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-197">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-198">**Compresión**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-198">**Compression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-199">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-201">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tape backup Structures \| [**Tape \_ Get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| compression")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-201">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|Compression")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-202">Si es **true**, la compresión de datos de hardware está habilitada.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-202">If **TRUE**, hardware data compression is enabled.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="bb9c8-203"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-203"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-204">false</span><span class="sxs-lookup"><span data-stu-id="bb9c8-204">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="bb9c8-205"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-205"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-206">TRUE</span><span class="sxs-lookup"><span data-stu-id="bb9c8-206">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-207">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-210">Cadena de forma libre que indica el algoritmo o la herramienta que usa el dispositivo para admitir la compresión.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-210">Free-form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="bb9c8-211">Si no es posible o no desea describir el esquema de compresión (quizás porque no se conoce), use las siguientes palabras: "Unknown" para indicar que no se sabe si el dispositivo admite o no capacidades de compresión. "Compressed" para representar que el dispositivo admite capacidades de compresión, pero su esquema de compresión no se conoce o no se revela; y "no comprimido" para representar que el dispositivo no admite capacidades de compresión.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-211">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use the following words: "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="bb9c8-212">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-212">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="bb9c8-213">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-213">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-214">El esquema de compresión es desconocido o no se ha descrito.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-214">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="bb9c8-215">("Comprimido")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-215">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-216">El archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito</span><span class="sxs-lookup"><span data-stu-id="bb9c8-216">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="bb9c8-217">("No comprimido")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-217">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-218">Si el archivo lógico no está comprimido</span><span class="sxs-lookup"><span data-stu-id="bb9c8-218">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-219">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-219">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-220">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-222">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-222">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-223">Código de error de Configuration Manager de Win32.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-223">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="bb9c8-224">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-224">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="bb9c8-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-225"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="bb9c8-226"> (0)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-226">(0)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-227">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-227">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="bb9c8-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-228"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="bb9c8-229">(1)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-229">(1)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-230">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-230">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bb9c8-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-231"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="bb9c8-232">(2)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="bb9c8-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-233"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="bb9c8-234">(3)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-234">(3)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-235">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-235">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bb9c8-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-236"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="bb9c8-237">(4)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-237">(4)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-238">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-238">Device is not working properly.</span></span> <span data-ttu-id="bb9c8-239">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-239">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="bb9c8-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-240"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="bb9c8-241">(5)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-241">(5)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-242">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-242">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="bb9c8-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-243"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="bb9c8-244"> (6)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-244">(6)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-245">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-245">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="bb9c8-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="bb9c8-247">(7)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="bb9c8-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="bb9c8-249">(8)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-249">(8)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-250">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-250">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="bb9c8-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-251"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="bb9c8-252">(9)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-252">(9)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-253">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-253">Device is not working properly.</span></span> <span data-ttu-id="bb9c8-254">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-254">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="bb9c8-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="bb9c8-256">(10)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-257">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="bb9c8-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="bb9c8-259">(11)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-260">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="bb9c8-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="bb9c8-262">(12)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-263">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="bb9c8-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="bb9c8-265">(13)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-266">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="bb9c8-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="bb9c8-268">(14)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-269">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="bb9c8-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="bb9c8-271">(15)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-272">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="bb9c8-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="bb9c8-274">(16)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-275">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="bb9c8-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="bb9c8-277">(17)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-278">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bb9c8-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="bb9c8-280">(18)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-281">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="bb9c8-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="bb9c8-283">(19)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="bb9c8-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="bb9c8-285">(20)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-286">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="bb9c8-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="bb9c8-288">(21)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-289">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-289">System failure.</span></span> <span data-ttu-id="bb9c8-290">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="bb9c8-291">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="bb9c8-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="bb9c8-293">(22)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-294">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="bb9c8-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="bb9c8-296">(23)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-297">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-297">System failure.</span></span> <span data-ttu-id="bb9c8-298">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="bb9c8-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="bb9c8-300">(24)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-301">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bb9c8-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bb9c8-303">(25)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-304">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="bb9c8-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="bb9c8-306">(26)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-307">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="bb9c8-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="bb9c8-309">(27)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-310">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="bb9c8-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="bb9c8-312">(28)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-313">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="bb9c8-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="bb9c8-315">(29)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-316">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-316">Device is disabled.</span></span> <span data-ttu-id="bb9c8-317">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-317">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="bb9c8-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-318"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="bb9c8-319">(30)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-319">(30)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-320">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-320">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="bb9c8-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-321"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="bb9c8-322">31</span><span class="sxs-lookup"><span data-stu-id="bb9c8-322">(31)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-323">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-323">Device is not working properly.</span></span> <span data-ttu-id="bb9c8-324">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-324">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-325">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-325">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-326">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-328">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-328">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-329">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-329">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="bb9c8-330">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-331">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-331">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-332">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-334">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-334">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-335">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-335">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="bb9c8-336">Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-336">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="bb9c8-337">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-338">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-338">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-339">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-339">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-341">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-341">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-342">Tamaño de bloque predeterminado, en bytes, para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-342">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="bb9c8-343">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-343">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bb9c8-344">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-345">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-345">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-348">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-348">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-349">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-349">Description of the object.</span></span>

<span data-ttu-id="bb9c8-350">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-351">**ID**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-351">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-352">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-354">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| File Functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-354">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-355">Identificador único de la unidad de cinta con otros dispositivos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-355">Unique identifier of the tape drive with other devices on the system.</span></span>

<span data-ttu-id="bb9c8-356">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-357">**ECC**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-357">**ECC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-358">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-360">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tape backup Structures \| [**Tape \_ Get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ECC")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-360">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ECC")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-361">Si **es true**, el dispositivo admite la corrección de errores de hardware.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-361">If **TRUE**, the device supports hardware error correction.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="bb9c8-362">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-362">**False** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="bb9c8-363">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-363">**True** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-364">**EOTWarningZoneSize**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-364">**EOTWarningZoneSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-365">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-365">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-367">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-367">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-368">Tamaño de zona para la advertencia de final de cinta (EOT).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-368">Zone size for the end of tape (EOT) warning.</span></span>

<span data-ttu-id="bb9c8-369">Esta propiedad se hereda de [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-369">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-370">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-370">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-371">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-373">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-373">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="bb9c8-374">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-375">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-375">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-378">Cadena de forma libre que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-378">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="bb9c8-379">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-380">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-380">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-381">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-383">Cadena de forma libre que describe el tipo de detección de errores y la corrección que admite este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-383">Free-form string describing the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="bb9c8-384">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-385">**FeaturesHigh**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-385">**FeaturesHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-386">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-388">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tape backup Structures \| [**Tape \_ Get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesHigh")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-388">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesHigh")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-389">32 bits de orden superior de la marca características del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-389">High-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-390">**FeaturesLow**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-390">**FeaturesLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-391">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-391">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-393">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tape backup Structures \| [**Tape \_ Get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| FeaturesLow")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|FeaturesLow")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-394">32 bits de orden inferior de la marca características del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-394">Low-order 32 bits of the device features flag.</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-395">**Id**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-395">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-396">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-398">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| File Functions")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-399">Nombre de identificación del fabricante de la unidad de CD-ROM de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-399">Manufacturer's identifying name of the Windows CD ROM drive.</span></span>

<span data-ttu-id="bb9c8-400">Ejemplo: "PLEXtor CD-ROM PX-12CS 1,01"</span><span class="sxs-lookup"><span data-stu-id="bb9c8-400">Example: "PLEXTOR CD-ROM PX-12CS 1.01"</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-401">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-401">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-402">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-402">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-404">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-405">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-405">Date and time the object was installed.</span></span> <span data-ttu-id="bb9c8-406">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-406">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bb9c8-407">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-408">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-408">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-409">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-409">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-411">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-411">Last error code reported by the logical device.</span></span>

<span data-ttu-id="bb9c8-412">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-413">**Le**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-413">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-414">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-416">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-416">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-417">Fabricante de la unidad de CD-ROM de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-417">Manufacturer of the Windows CD-ROM drive.</span></span>

<span data-ttu-id="bb9c8-418">Ejemplo: "PLEXtor"</span><span class="sxs-lookup"><span data-stu-id="bb9c8-418">Example: "PLEXTOR"</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-419">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-419">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-420">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-420">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-422">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-422">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-423">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-423">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="bb9c8-424">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-424">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bb9c8-425">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-426">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-426">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-427">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-427">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-429">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-430">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-430">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="bb9c8-431">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-431">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bb9c8-432">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-432">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-433">**MaxPartitionCount**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-433">**MaxPartitionCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-434">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-436">Recuento máximo de particiones para la unidad de cinta.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-436">Maximum partition count for the tape drive.</span></span>

<span data-ttu-id="bb9c8-437">Esta propiedad se hereda de [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-437">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-438">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-438">**MediaType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-441">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ TapeDrive \| \| Tape Drive")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-441">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_TapeDrive\|MediaType\|Tape Drive")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-442">Tipo de medio que usa (o al que tiene acceso) este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-442">Media type used by (or accessed by) this device.</span></span> <span data-ttu-id="bb9c8-443">En este caso, se establece en "unidad de cinta".</span><span class="sxs-lookup"><span data-stu-id="bb9c8-443">In this case, it is set to "Tape Drive".</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-444">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-444">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-445">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-446">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-447">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-447">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-448">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-448">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="bb9c8-449">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-449">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="bb9c8-450">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-451">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-451">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-452">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-453">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-454">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-454">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-455">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-455">Label by which the object is known.</span></span> <span data-ttu-id="bb9c8-456">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-456">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="bb9c8-457">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-458">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-458">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-459">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-459">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-461">Si **es true**, el dispositivo de acceso a medios necesita limpieza.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-461">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="bb9c8-462">Si la limpieza manual o automática es posible, se indica en la propiedad **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="bb9c8-462">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="bb9c8-463">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-463">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-464">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-464">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-465">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-465">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-466">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-467">Número máximo de medios individuales que se pueden admitir o insertar en el dispositivo de acceso a medios (si se admite).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-467">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="bb9c8-468">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-468">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-469">**Relleno**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-469">**Padding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-470">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-470">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-471">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-472">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-472">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-473">Número de bytes insertados entre bloques en un medio de cinta.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-473">Number of bytes inserted between blocks on a tape media.</span></span>

<span data-ttu-id="bb9c8-474">Esta propiedad se hereda de [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-474">This property is inherited from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-475">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-475">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-476">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-478">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-478">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-479">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-479">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="bb9c8-480">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="bb9c8-481">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="bb9c8-481">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-482">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-482">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-483">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-483">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-484">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-484">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-485">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-485">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="bb9c8-486">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-486">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb9c8-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-487"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bb9c8-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-488"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-489">No se admiten capacidades relacionadas con la energía para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-489">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bb9c8-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-490"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bb9c8-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-491"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-492">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-492">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="bb9c8-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-493"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-494">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-494">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="bb9c8-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-495"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-496">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="bb9c8-496">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="bb9c8-497">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-497">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="bb9c8-498">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-498">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="bb9c8-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-499"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-500">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-500">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="bb9c8-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-501"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-502">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="bb9c8-502">Timed Power-On Supported</span></span>

<span data-ttu-id="bb9c8-503">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-503">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-504">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-504">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-505">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-505">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-506">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-507">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-507">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="bb9c8-508">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-508">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="bb9c8-509">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-510">**ReportSetMarks**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-510">**ReportSetMarks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-511">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-511">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-512">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-513">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tape backup Structures \| [**Tape \_ Get \_ Drive \_ Parameters**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters) \| ReportSetmarks")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Tape Backup Structures\|[**TAPE\_GET\_DRIVE\_PARAMETERS**](/windows/win32/api/winnt/ns-winnt-tape_get_drive_parameters)\|ReportSetmarks")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-514">Si es **true**, setmark Reporting está habilitado.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-514">If **TRUE**, setmark reporting is enabled.</span></span> <span data-ttu-id="bb9c8-515">Setmark Reporting hace uso de un elemento grabado especializado que no contiene datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-515">Setmark reporting makes use of a specialized recorded element that does not contain user data.</span></span> <span data-ttu-id="bb9c8-516">Este elemento grabado se utiliza para proporcionar un esquema de segmentación que sea jerárquicamente superior a filemarks.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-516">This recorded element is used to provide a segmentation scheme that is hierarchically superior to filemarks.</span></span> <span data-ttu-id="bb9c8-517">Setmarks proporcionan un posicionamiento más rápido en las cintas de alta capacidad.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-517">Setmarks provide faster positioning on high-capacity tapes.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="bb9c8-518"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-518"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-519">false</span><span class="sxs-lookup"><span data-stu-id="bb9c8-519">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="bb9c8-520"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-520"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="bb9c8-521">TRUE</span><span class="sxs-lookup"><span data-stu-id="bb9c8-521">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-522">**Estado**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-522">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-523">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-525">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-525">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-526">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-526">Current status of the object.</span></span> <span data-ttu-id="bb9c8-527">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-527">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bb9c8-528">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-528">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bb9c8-529">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="bb9c8-529">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bb9c8-530">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-530">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bb9c8-531">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-531">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bb9c8-532">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-532">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bb9c8-533">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="bb9c8-533">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bb9c8-534">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-534">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bb9c8-535">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-535">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bb9c8-536">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-536">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb9c8-537">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-537">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bb9c8-538">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-538">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bb9c8-539">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-539">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bb9c8-540">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-540">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bb9c8-541">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-541">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bb9c8-542">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-542">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bb9c8-543">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-543">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bb9c8-544">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-544">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bb9c8-545">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-545">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-546">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-546">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-547">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-548">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-549">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="bb9c8-549">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-550">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-550">State of the logical device.</span></span> <span data-ttu-id="bb9c8-551">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-551">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="bb9c8-552">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-552">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bb9c8-553">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-553">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bb9c8-554">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-554">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="bb9c8-555">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-555">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bb9c8-556">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-556">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="bb9c8-557">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-557">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb9c8-558">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-558">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-559">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-560">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-560">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-561">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-561">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-562">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-562">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="bb9c8-563">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-563">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb9c8-564">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-564">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb9c8-565">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-566">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bb9c8-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb9c8-567">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="bb9c8-567">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="bb9c8-568">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="bb9c8-568">Name of the scoping system.</span></span>

<span data-ttu-id="bb9c8-569">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-569">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb9c8-570">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb9c8-570">Remarks</span></span>

<span data-ttu-id="bb9c8-571">La clase **Win32 \_ TapeDrive** se deriva de [**CIM \_ TapeDrive**](cim-tapedrive.md).</span><span class="sxs-lookup"><span data-stu-id="bb9c8-571">The **Win32\_TapeDrive** class is derived from [**CIM\_TapeDrive**](cim-tapedrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb9c8-572">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb9c8-572">Requirements</span></span>



| <span data-ttu-id="bb9c8-573">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb9c8-573">Requirement</span></span> | <span data-ttu-id="bb9c8-574">Value</span><span class="sxs-lookup"><span data-stu-id="bb9c8-574">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb9c8-575">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb9c8-575">Minimum supported client</span></span><br/> | <span data-ttu-id="bb9c8-576">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb9c8-576">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb9c8-577">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bb9c8-577">Minimum supported server</span></span><br/> | <span data-ttu-id="bb9c8-578">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb9c8-578">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb9c8-579">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bb9c8-579">Namespace</span></span><br/>                | <span data-ttu-id="bb9c8-580">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bb9c8-580">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bb9c8-581">MOF</span><span class="sxs-lookup"><span data-stu-id="bb9c8-581">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb9c8-582"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb9c8-582"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb9c8-583">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb9c8-583">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb9c8-584"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb9c8-584"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb9c8-585">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb9c8-585">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb9c8-586">**CIM \_ TapeDrive**</span><span class="sxs-lookup"><span data-stu-id="bb9c8-586">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dt>

[<span data-ttu-id="bb9c8-587">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="bb9c8-587">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
