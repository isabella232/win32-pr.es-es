---
description: La \_ clase WMI FloppyDrive de Win32 administra las funciones de una unidad de disquete.
ms.assetid: 41823eeb-4831-4deb-a798-7b3589ebf3e2
ms.tgt_platform: multiple
title: Win32_FloppyDrive (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyDrive
- Win32_FloppyDrive.Reset
- Win32_FloppyDrive.SetPowerState
- Win32_FloppyDrive.Availability
- Win32_FloppyDrive.Capabilities
- Win32_FloppyDrive.CapabilityDescriptions
- Win32_FloppyDrive.Caption
- Win32_FloppyDrive.CompressionMethod
- Win32_FloppyDrive.ConfigManagerErrorCode
- Win32_FloppyDrive.ConfigManagerUserConfig
- Win32_FloppyDrive.CreationClassName
- Win32_FloppyDrive.DefaultBlockSize
- Win32_FloppyDrive.Description
- Win32_FloppyDrive.DeviceID
- Win32_FloppyDrive.ErrorCleared
- Win32_FloppyDrive.ErrorDescription
- Win32_FloppyDrive.ErrorMethodology
- Win32_FloppyDrive.InstallDate
- Win32_FloppyDrive.LastErrorCode
- Win32_FloppyDrive.Manufacturer
- Win32_FloppyDrive.MaxBlockSize
- Win32_FloppyDrive.MaxMediaSize
- Win32_FloppyDrive.MinBlockSize
- Win32_FloppyDrive.Name
- Win32_FloppyDrive.NeedsCleaning
- Win32_FloppyDrive.NumberOfMediaSupported
- Win32_FloppyDrive.PNPDeviceID
- Win32_FloppyDrive.PowerManagementCapabilities
- Win32_FloppyDrive.PowerManagementSupported
- Win32_FloppyDrive.Status
- Win32_FloppyDrive.StatusInfo
- Win32_FloppyDrive.SystemCreationClassName
- Win32_FloppyDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 832b5fad0ce54d1436fd6b2e47765af0fabfd2bb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153353"
---
# <a name="win32_floppydrive-class"></a><span data-ttu-id="41d9d-103">\_Clase Win32 FloppyDrive</span><span class="sxs-lookup"><span data-stu-id="41d9d-103">Win32\_FloppyDrive class</span></span>

<span data-ttu-id="41d9d-104">\[**Win32 \_ FloppyDrive** ya no está disponible para su uso a partir de Windows 10 y Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="41d9d-104">\[**Win32\_FloppyDrive** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="41d9d-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ FloppyDrive de Win32** administra las funciones de una unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="41d9d-105">The **Win32\_FloppyDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) manages the functions of a floppy disk drive.</span></span>

<span data-ttu-id="41d9d-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="41d9d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="41d9d-107">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="41d9d-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d9d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41d9d-108">Syntax</span></span>

``` syntax
[Dynamic, provider("CIMWin32"), UUID("{FB1F3A64-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyDrive : CIM_DisketteDrive
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="41d9d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="41d9d-109">Members</span></span>

<span data-ttu-id="41d9d-110">La **clase \_ FloppyDrive de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="41d9d-110">The **Win32\_FloppyDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="41d9d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="41d9d-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="41d9d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41d9d-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="41d9d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="41d9d-113">Methods</span></span>

<span data-ttu-id="41d9d-114">La clase **Win32 \_ FloppyDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="41d9d-114">The **Win32\_FloppyDrive** class has these methods.</span></span>



| <span data-ttu-id="41d9d-115">Método</span><span class="sxs-lookup"><span data-stu-id="41d9d-115">Method</span></span>            | <span data-ttu-id="41d9d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="41d9d-116">Description</span></span>                                                                                                                                                                                                                   |
|:------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41d9d-117">**Reset**</span><span class="sxs-lookup"><span data-stu-id="41d9d-117">**Reset**</span></span>         | <span data-ttu-id="41d9d-118">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="41d9d-118">Not implemented.</span></span> <span data-ttu-id="41d9d-119">Para obtener más información sobre cómo implementar este método, vea el método [**RESET**](reset-method-in-class-cim-controller.md) en [**CIM \_ DisketteDrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-119">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/>                 |
| <span data-ttu-id="41d9d-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="41d9d-120">**SetPowerState**</span></span> | <span data-ttu-id="41d9d-121">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="41d9d-121">Not implemented.</span></span> <span data-ttu-id="41d9d-122">Para obtener más información sobre cómo implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ DisketteDrive**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-122">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="41d9d-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41d9d-123">Properties</span></span>

<span data-ttu-id="41d9d-124">La **clase \_ FloppyDrive de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="41d9d-124">The **Win32\_FloppyDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41d9d-125">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="41d9d-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d9d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-128">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="41d9d-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-129">Estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-129">Status of the device.</span></span>

<span data-ttu-id="41d9d-130">Esta propiedad se hereda del [ **\_ LogicalDevice de CIM**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="41d9d-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41d9d-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="41d9d-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41d9d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="41d9d-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="41d9d-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="41d9d-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-134">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="41d9d-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="41d9d-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="41d9d-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="41d9d-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="41d9d-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="41d9d-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="41d9d-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="41d9d-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="41d9d-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="41d9d-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="41d9d-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="41d9d-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="41d9d-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="41d9d-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="41d9d-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="41d9d-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="41d9d-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="41d9d-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="41d9d-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="41d9d-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="41d9d-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-145">Ahorro de energía: desconocido</span><span class="sxs-lookup"><span data-stu-id="41d9d-145">Power Save - Unknown</span></span>

<span data-ttu-id="41d9d-146">El dispositivo está en modo de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="41d9d-146">The device in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="41d9d-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="41d9d-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-148">Ahorro de energía: modo de baja energía</span><span class="sxs-lookup"><span data-stu-id="41d9d-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="41d9d-149">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="41d9d-149">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="41d9d-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="41d9d-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-151">Ahorro de energía: en espera</span><span class="sxs-lookup"><span data-stu-id="41d9d-151">Power Save - Standby</span></span>

<span data-ttu-id="41d9d-152">El dispositivo no funciona, pero se puede restaurar rápidamente a pleno rendimiento.</span><span class="sxs-lookup"><span data-stu-id="41d9d-152">The device is not functioning, but can be quickly restored to full-power.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="41d9d-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="41d9d-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="41d9d-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="41d9d-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-155">Ahorro de energía: ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="41d9d-155">Power Save - Warning</span></span>

<span data-ttu-id="41d9d-156">El dispositivo está en un estado de advertencia, aunque también en el modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="41d9d-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="41d9d-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="41d9d-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-158">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="41d9d-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="41d9d-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="41d9d-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-160">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="41d9d-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="41d9d-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-162">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="41d9d-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="41d9d-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="41d9d-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-164">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="41d9d-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41d9d-165">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="41d9d-165">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-166">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d9d-166">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-168">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de almacenamiento DMTF \| 001,9 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,11 "," MIF. \|Dispositivos de almacenamiento DMTF \| 001,12 "," MIF. \|Discos DMTF \| 003,7 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="41d9d-168">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-169">Matriz de funcionalidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="41d9d-169">Array of capabilities of the media access device.</span></span> <span data-ttu-id="41d9d-170">Por ejemplo, el dispositivo puede admitir el acceso aleatorio, el medio extraíble y la limpieza automática.</span><span class="sxs-lookup"><span data-stu-id="41d9d-170">For example, the device may support Random Access, Removable Media, and Automatic Cleaning.</span></span> <span data-ttu-id="41d9d-171">En este caso, los valores 3, 7 y 9 se escribirían en la matriz.</span><span class="sxs-lookup"><span data-stu-id="41d9d-171">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="41d9d-172">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-172">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41d9d-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="41d9d-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41d9d-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="41d9d-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="41d9d-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Acceso secuencial** (2)</span><span class="sxs-lookup"><span data-stu-id="41d9d-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="41d9d-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Acceso aleatorio** (3)</span><span class="sxs-lookup"><span data-stu-id="41d9d-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="41d9d-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Admite escritura** (4)</span><span class="sxs-lookup"><span data-stu-id="41d9d-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="41d9d-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Cifrado** (5)</span><span class="sxs-lookup"><span data-stu-id="41d9d-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="41d9d-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compresión** (6)</span><span class="sxs-lookup"><span data-stu-id="41d9d-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="41d9d-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Admite medios** extraíbles (7)</span><span class="sxs-lookup"><span data-stu-id="41d9d-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-181">Admite medios extraíbles</span><span class="sxs-lookup"><span data-stu-id="41d9d-181">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="41d9d-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Limpieza manual** (8)</span><span class="sxs-lookup"><span data-stu-id="41d9d-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="41d9d-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Limpieza automática** (9)</span><span class="sxs-lookup"><span data-stu-id="41d9d-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="41d9d-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Notificación inteligente** (10)</span><span class="sxs-lookup"><span data-stu-id="41d9d-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="41d9d-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Admite medios de doble cara** (11)</span><span class="sxs-lookup"><span data-stu-id="41d9d-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-186">Admite medios Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="41d9d-186">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="41d9d-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount EJECT no requerido** (12)</span><span class="sxs-lookup"><span data-stu-id="41d9d-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41d9d-188">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="41d9d-188">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-189">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="41d9d-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-191">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md).**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="41d9d-191">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-192">Matriz de cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de las características de controlador serie indicadas en la matriz de **funcionalidades** .</span><span class="sxs-lookup"><span data-stu-id="41d9d-192">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="41d9d-193">Tenga en cuenta que cada entrada de esta matriz está relacionada con la entrada de la matriz de **capacidades** que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="41d9d-193">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="41d9d-194">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-194">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-195">**Caption**</span><span class="sxs-lookup"><span data-stu-id="41d9d-195">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-198">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="41d9d-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-199">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="41d9d-199">Short description of the object.</span></span>

<span data-ttu-id="41d9d-200">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-201">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="41d9d-201">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-204">Cadena de forma libre que indica el algoritmo o la herramienta que usa el dispositivo para admitir la compresión.</span><span class="sxs-lookup"><span data-stu-id="41d9d-204">Free form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="41d9d-205">Si no es posible o no desea describir el esquema de compresión (quizás porque no se conoce), use "Unknown" para indicar que no se sabe si el dispositivo admite o no las capacidades de compresión. "Compressed" para representar que el dispositivo admite capacidades de compresión, pero su esquema de compresión no se conoce o no se revela; y "no comprimido" para representar que el dispositivo no admite capacidades de compresión.</span><span class="sxs-lookup"><span data-stu-id="41d9d-205">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="41d9d-206">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-206">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="41d9d-207">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="41d9d-207">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-208">El esquema de compresión es desconocido o no se ha descrito.</span><span class="sxs-lookup"><span data-stu-id="41d9d-208">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="41d9d-209">("Comprimido")</span><span class="sxs-lookup"><span data-stu-id="41d9d-209">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-210">El archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito</span><span class="sxs-lookup"><span data-stu-id="41d9d-210">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="41d9d-211">("No comprimido")</span><span class="sxs-lookup"><span data-stu-id="41d9d-211">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-212">Si el archivo lógico no está comprimido</span><span class="sxs-lookup"><span data-stu-id="41d9d-212">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41d9d-213">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="41d9d-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-214">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41d9d-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-216">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="41d9d-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-217">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="41d9d-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="41d9d-218">Esta propiedad se hereda del [ **\_ LogicalDevice de CIM**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="41d9d-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="41d9d-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="41d9d-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="41d9d-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-221">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="41d9d-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="41d9d-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="41d9d-223">(1)</span><span class="sxs-lookup"><span data-stu-id="41d9d-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-224">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="41d9d-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="41d9d-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="41d9d-226">(2)</span><span class="sxs-lookup"><span data-stu-id="41d9d-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="41d9d-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="41d9d-228">(3)</span><span class="sxs-lookup"><span data-stu-id="41d9d-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-229">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="41d9d-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="41d9d-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="41d9d-231">(4)</span><span class="sxs-lookup"><span data-stu-id="41d9d-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-232">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="41d9d-232">Device is not working properly.</span></span> <span data-ttu-id="41d9d-233">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="41d9d-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="41d9d-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="41d9d-235">(5)</span><span class="sxs-lookup"><span data-stu-id="41d9d-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-236">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="41d9d-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="41d9d-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="41d9d-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="41d9d-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-239">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="41d9d-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="41d9d-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="41d9d-241">(7)</span><span class="sxs-lookup"><span data-stu-id="41d9d-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="41d9d-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="41d9d-243">(8)</span><span class="sxs-lookup"><span data-stu-id="41d9d-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-244">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="41d9d-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="41d9d-246">(9)</span><span class="sxs-lookup"><span data-stu-id="41d9d-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-247">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="41d9d-247">Device is not working properly.</span></span> <span data-ttu-id="41d9d-248">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="41d9d-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="41d9d-250">(10)</span><span class="sxs-lookup"><span data-stu-id="41d9d-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-251">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="41d9d-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="41d9d-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="41d9d-253">(11)</span><span class="sxs-lookup"><span data-stu-id="41d9d-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-254">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="41d9d-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="41d9d-256">(12)</span><span class="sxs-lookup"><span data-stu-id="41d9d-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-257">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="41d9d-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="41d9d-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="41d9d-259">(13)</span><span class="sxs-lookup"><span data-stu-id="41d9d-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-260">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="41d9d-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="41d9d-262">(14)</span><span class="sxs-lookup"><span data-stu-id="41d9d-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-263">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="41d9d-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="41d9d-265">(15)</span><span class="sxs-lookup"><span data-stu-id="41d9d-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-266">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="41d9d-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="41d9d-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="41d9d-268">(16)</span><span class="sxs-lookup"><span data-stu-id="41d9d-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-269">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="41d9d-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="41d9d-271">(17)</span><span class="sxs-lookup"><span data-stu-id="41d9d-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-272">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="41d9d-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="41d9d-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="41d9d-274">(18)</span><span class="sxs-lookup"><span data-stu-id="41d9d-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-275">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="41d9d-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="41d9d-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="41d9d-277">(19)</span><span class="sxs-lookup"><span data-stu-id="41d9d-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="41d9d-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="41d9d-279">(20)</span><span class="sxs-lookup"><span data-stu-id="41d9d-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-280">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="41d9d-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="41d9d-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="41d9d-282">(21)</span><span class="sxs-lookup"><span data-stu-id="41d9d-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-283">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="41d9d-283">System failure.</span></span> <span data-ttu-id="41d9d-284">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="41d9d-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="41d9d-285">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="41d9d-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="41d9d-287">(22)</span><span class="sxs-lookup"><span data-stu-id="41d9d-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-288">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="41d9d-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="41d9d-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="41d9d-290">(23)</span><span class="sxs-lookup"><span data-stu-id="41d9d-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-291">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="41d9d-291">System failure.</span></span> <span data-ttu-id="41d9d-292">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="41d9d-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="41d9d-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="41d9d-294">(24)</span><span class="sxs-lookup"><span data-stu-id="41d9d-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-295">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="41d9d-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="41d9d-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="41d9d-297">(25)</span><span class="sxs-lookup"><span data-stu-id="41d9d-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-298">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="41d9d-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="41d9d-300">(26)</span><span class="sxs-lookup"><span data-stu-id="41d9d-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-301">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="41d9d-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="41d9d-303">(27)</span><span class="sxs-lookup"><span data-stu-id="41d9d-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-304">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="41d9d-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="41d9d-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="41d9d-306">(28)</span><span class="sxs-lookup"><span data-stu-id="41d9d-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-307">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="41d9d-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="41d9d-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="41d9d-309">(29)</span><span class="sxs-lookup"><span data-stu-id="41d9d-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-310">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="41d9d-310">Device is disabled.</span></span> <span data-ttu-id="41d9d-311">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="41d9d-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="41d9d-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="41d9d-313">(30)</span><span class="sxs-lookup"><span data-stu-id="41d9d-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-314">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="41d9d-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="41d9d-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="41d9d-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="41d9d-316">31</span><span class="sxs-lookup"><span data-stu-id="41d9d-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-317">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="41d9d-317">Device is not working properly.</span></span> <span data-ttu-id="41d9d-318">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="41d9d-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41d9d-319">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="41d9d-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-320">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="41d9d-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-322">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="41d9d-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-323">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="41d9d-323">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="41d9d-324">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-325">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41d9d-325">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-328">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41d9d-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-329">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="41d9d-329">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="41d9d-330">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="41d9d-330">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="41d9d-331">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-332">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="41d9d-332">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-333">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="41d9d-333">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-335">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="41d9d-335">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-336">Tamaño de bloque predeterminado, en bytes, para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-336">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="41d9d-337">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="41d9d-338">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="41d9d-338">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-339">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="41d9d-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-342">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="41d9d-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-343">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="41d9d-343">Description of the object.</span></span>

<span data-ttu-id="41d9d-344">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-345">**ID**</span><span class="sxs-lookup"><span data-stu-id="41d9d-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-346">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-347">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-348">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41d9d-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-349">Identificador único de la unidad de disquete con otros dispositivos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="41d9d-349">Unique identifier of the floppy disk drive with other devices on the system.</span></span>

<span data-ttu-id="41d9d-350">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-351">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="41d9d-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-352">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="41d9d-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-354">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="41d9d-354">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="41d9d-355">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="41d9d-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-357">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-359">Cadena de forma libre que proporciona más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="41d9d-359">Free-form string that supplies more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="41d9d-360">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-361">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="41d9d-361">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-362">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-364">Cadena de forma libre que describe el tipo de detección de errores y la corrección que admite este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-364">Free-form string that describes the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="41d9d-365">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-365">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-366">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="41d9d-366">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-367">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="41d9d-367">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-369">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="41d9d-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-370">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="41d9d-370">Date and time the object was installed.</span></span> <span data-ttu-id="41d9d-371">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="41d9d-371">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="41d9d-372">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-373">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="41d9d-373">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-374">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41d9d-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-376">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="41d9d-376">Last error code reported by the logical device.</span></span>

<span data-ttu-id="41d9d-377">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-378">**Le**</span><span class="sxs-lookup"><span data-stu-id="41d9d-378">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-379">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-381">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="41d9d-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-382">Nombre del fabricante de la unidad de disquete.</span><span class="sxs-lookup"><span data-stu-id="41d9d-382">Name of the manufacturer of the floppy disk drive.</span></span>

<span data-ttu-id="41d9d-383">Ejemplo: "Acme"</span><span class="sxs-lookup"><span data-stu-id="41d9d-383">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-384">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="41d9d-384">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-385">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="41d9d-385">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-386">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-387">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="41d9d-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-388">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-388">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="41d9d-389">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="41d9d-390">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="41d9d-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-391">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="41d9d-391">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-392">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="41d9d-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-394">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivos de acceso secuencial DMTF \| 001,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" kilobytes ")</span><span class="sxs-lookup"><span data-stu-id="41d9d-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-395">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-395">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="41d9d-396">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="41d9d-397">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="41d9d-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-398">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="41d9d-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-399">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="41d9d-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-401">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="41d9d-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-402">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-402">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="41d9d-403">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="41d9d-404">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="41d9d-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-405">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="41d9d-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-406">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-408">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="41d9d-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-409">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="41d9d-409">Label by which the object is known.</span></span> <span data-ttu-id="41d9d-410">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="41d9d-410">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="41d9d-411">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-412">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="41d9d-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-413">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="41d9d-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-414">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-415">Si **es true**, el dispositivo de acceso a medios requiere limpieza.</span><span class="sxs-lookup"><span data-stu-id="41d9d-415">If **True**, the media access device requires cleaning.</span></span> <span data-ttu-id="41d9d-416">Si la limpieza manual o automática es posible, se indica en la propiedad **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="41d9d-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="41d9d-417">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-418">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="41d9d-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-419">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="41d9d-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-421">Número máximo de medios individuales que se pueden admitir o insertar en el dispositivo de acceso a medios (si se admite).</span><span class="sxs-lookup"><span data-stu-id="41d9d-421">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="41d9d-422">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="41d9d-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-426">Calificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="41d9d-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-427">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="41d9d-427">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="41d9d-428">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="41d9d-429">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="41d9d-429">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="41d9d-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-431">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d9d-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-433">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="41d9d-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="41d9d-434">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="41d9d-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41d9d-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="41d9d-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="41d9d-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="41d9d-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="41d9d-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="41d9d-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="41d9d-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="41d9d-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-439">habilitado</span><span class="sxs-lookup"><span data-stu-id="41d9d-439">Enabled</span></span>

<span data-ttu-id="41d9d-440">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="41d9d-440">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="41d9d-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="41d9d-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-442">Modos de ahorro de energía introducidos automáticamente</span><span class="sxs-lookup"><span data-stu-id="41d9d-442">Power Saving Modes Entered Automatically</span></span>

<span data-ttu-id="41d9d-443">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="41d9d-443">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="41d9d-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="41d9d-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-445">Estado de energía configurable</span><span class="sxs-lookup"><span data-stu-id="41d9d-445">Power State Settable</span></span>

<span data-ttu-id="41d9d-446">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="41d9d-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="41d9d-447">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="41d9d-447">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="41d9d-448">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="41d9d-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="41d9d-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="41d9d-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-450">Ciclo de energía admitido</span><span class="sxs-lookup"><span data-stu-id="41d9d-450">Power Cycling Supported</span></span>

<span data-ttu-id="41d9d-451">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="41d9d-451">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="41d9d-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="41d9d-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="41d9d-453">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="41d9d-453">Timed Power-On Supported</span></span>

<span data-ttu-id="41d9d-454">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="41d9d-454">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="41d9d-455">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="41d9d-455">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-456">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="41d9d-456">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-458">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="41d9d-458">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="41d9d-459">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="41d9d-459">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="41d9d-460">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-461">**Estado**</span><span class="sxs-lookup"><span data-stu-id="41d9d-461">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-462">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-463">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-464">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="41d9d-464">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-465">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="41d9d-465">Current status of the object.</span></span> <span data-ttu-id="41d9d-466">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="41d9d-466">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="41d9d-467">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente, pero predecir un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="41d9d-467">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly, but predicting a failure in the near future).</span></span> <span data-ttu-id="41d9d-468">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="41d9d-468">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="41d9d-469">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="41d9d-469">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="41d9d-470">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="41d9d-470">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="41d9d-471">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="41d9d-472">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="41d9d-472">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="41d9d-473">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="41d9d-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="41d9d-474">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="41d9d-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="41d9d-475">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="41d9d-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41d9d-476">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="41d9d-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="41d9d-477">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="41d9d-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="41d9d-478">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="41d9d-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="41d9d-479">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="41d9d-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="41d9d-480">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="41d9d-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="41d9d-481">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="41d9d-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="41d9d-482">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="41d9d-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="41d9d-483">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="41d9d-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="41d9d-484">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="41d9d-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41d9d-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="41d9d-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-486">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41d9d-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-488">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="41d9d-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-489">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="41d9d-489">State of the logical device.</span></span> <span data-ttu-id="41d9d-490">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 ("no aplicable").</span><span class="sxs-lookup"><span data-stu-id="41d9d-490">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="41d9d-491">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="41d9d-492">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="41d9d-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="41d9d-493">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="41d9d-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="41d9d-494">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="41d9d-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="41d9d-495">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="41d9d-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="41d9d-496">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="41d9d-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="41d9d-497">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="41d9d-497">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-498">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-500">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41d9d-500">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-501">Valor de la propiedad de ámbito de equipo de **CreationClassName** .</span><span class="sxs-lookup"><span data-stu-id="41d9d-501">Value of the scoping computer **CreationClassName** property.</span></span> <span data-ttu-id="41d9d-502">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="41d9d-503">Esta propiedad se hereda del [ **\_ LogicalDevice de CIM**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="41d9d-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

</dd> <dt>

<span data-ttu-id="41d9d-504">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="41d9d-504">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41d9d-505">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="41d9d-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-506">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41d9d-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41d9d-507">Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41d9d-507">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41d9d-508">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="41d9d-508">Name of the scoping system.</span></span>

<span data-ttu-id="41d9d-509">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41d9d-510">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41d9d-510">Remarks</span></span>

<span data-ttu-id="41d9d-511">La **clase \_ FloppyDrive de Win32** se deriva [**de \_ DisketteDrive de CIM**](cim-diskettedrive.md) que deriva [**de \_ CIM MediaAccessDevice**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-511">The **Win32\_FloppyDrive** class is derived from [**CIM\_DisketteDrive**](cim-diskettedrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="41d9d-512">La **clase \_ MediaAccessDevice de CIM** deriva del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="41d9d-512">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41d9d-513">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41d9d-513">Requirements</span></span>



| <span data-ttu-id="41d9d-514">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d9d-514">Requirement</span></span> | <span data-ttu-id="41d9d-515">Value</span><span class="sxs-lookup"><span data-stu-id="41d9d-515">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d9d-516">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41d9d-516">Minimum supported client</span></span><br/> | <span data-ttu-id="41d9d-517">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41d9d-517">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41d9d-518">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41d9d-518">Minimum supported server</span></span><br/> | <span data-ttu-id="41d9d-519">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41d9d-519">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41d9d-520">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="41d9d-520">End of client support</span></span><br/>    | <span data-ttu-id="41d9d-521">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="41d9d-521">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="41d9d-522">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="41d9d-522">End of server support</span></span><br/>    | <span data-ttu-id="41d9d-523">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="41d9d-523">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="41d9d-524">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41d9d-524">Namespace</span></span><br/>                | <span data-ttu-id="41d9d-525">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="41d9d-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41d9d-526">MOF</span><span class="sxs-lookup"><span data-stu-id="41d9d-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41d9d-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41d9d-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41d9d-528">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41d9d-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41d9d-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d9d-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d9d-530">Vea también</span><span class="sxs-lookup"><span data-stu-id="41d9d-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d9d-531">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="41d9d-531">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="41d9d-532">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="41d9d-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

