---
description: Representa un equipo que ejecuta Windows.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Clase Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152920"
---
# <a name="win32_computersystem-class"></a><span data-ttu-id="2be80-103">\_Clase ComputerSystem de Win32</span><span class="sxs-lookup"><span data-stu-id="2be80-103">Win32\_ComputerSystem class</span></span>

<span data-ttu-id="2be80-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComputerSystem de Win32** representa un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="2be80-104">The **Win32\_ComputerSystem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a computer system running Windows.</span></span>

<span data-ttu-id="2be80-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2be80-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be80-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2be80-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a><span data-ttu-id="2be80-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2be80-107">Members</span></span>

<span data-ttu-id="2be80-108">La clase de **Win32 \_ ComputerSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2be80-108">The **Win32\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="2be80-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2be80-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2be80-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2be80-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2be80-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2be80-111">Methods</span></span>

<span data-ttu-id="2be80-112">La clase de **Win32 \_ ComputerSystem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2be80-112">The **Win32\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="2be80-113">Método</span><span class="sxs-lookup"><span data-stu-id="2be80-113">Method</span></span>                                                                                          | <span data-ttu-id="2be80-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2be80-114">Description</span></span>                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2be80-115">**JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="2be80-115">**JoinDomainOrWorkgroup**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | <span data-ttu-id="2be80-116">Agrega un equipo a un dominio o grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2be80-116">Adds a computer system to a domain or workgroup.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="2be80-117">**Cambiar el nombre**</span><span class="sxs-lookup"><span data-stu-id="2be80-117">**Rename**</span></span>](rename-method-in-class-win32-computersystem.md)                                   | <span data-ttu-id="2be80-118">Cambia el nombre de un equipo local.</span><span class="sxs-lookup"><span data-stu-id="2be80-118">Renames a local computer.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="2be80-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2be80-119">**SetPowerState**</span></span>                                                                               | <span data-ttu-id="2be80-120">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="2be80-120">Not implemented.</span></span> <span data-ttu-id="2be80-121">Para obtener más información sobre cómo implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-121">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span><br/> |
| [<span data-ttu-id="2be80-122">**UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="2be80-122">**UnjoinDomainOrWorkgroup**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | <span data-ttu-id="2be80-123">Quita un equipo de un dominio o un grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2be80-123">Removes a computer system from a domain or workgroup.</span></span><br/>                                                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="2be80-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2be80-124">Properties</span></span>

<span data-ttu-id="2be80-125">La clase de **Win32 \_ ComputerSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2be80-125">The **Win32\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2be80-126">**AdminPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="2be80-126">**AdminPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 24 \| configuración de seguridad de hardware \| AdminPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="2be80-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|AdminPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-130">Configuración de seguridad del hardware del sistema para el estado de la contraseña de administrador.</span><span class="sxs-lookup"><span data-stu-id="2be80-130">System hardware security settings for administrator password status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2be80-131">**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-131">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2be80-132">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-132">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2be80-133">**No implementado** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-133">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-134">**Desconocido** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-134">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-135">**AutomaticManagedPagefile**</span><span class="sxs-lookup"><span data-stu-id="2be80-135">**AutomaticManagedPagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-136">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2be80-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2be80-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-139">Si **es true**, el sistema administra el archivo de paginación.</span><span class="sxs-lookup"><span data-stu-id="2be80-139">If **True**, the system manages the page file.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-140">**AutomaticResetBootOption**</span><span class="sxs-lookup"><span data-stu-id="2be80-140">**AutomaticResetBootOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-141">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2be80-143">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ System \\ \\ CurrentControlSet \\ \\ control \\ \\ CrashControl \| AutoReboot")</span><span class="sxs-lookup"><span data-stu-id="2be80-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-144">Si es **true**, se habilita la opción de inicio de restablecimiento automático.</span><span class="sxs-lookup"><span data-stu-id="2be80-144">If **True**, the automatic reset boot option is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-145">**AutomaticResetCapability**</span><span class="sxs-lookup"><span data-stu-id="2be80-145">**AutomaticResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-148">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2be80-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-149">Si es **true**, el restablecimiento automático está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2be80-149">If **True**, the automatic reset is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-150">**BootOptionOnLimit**</span><span class="sxs-lookup"><span data-stu-id="2be80-150">**BootOptionOnLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-153">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| \| opción de arranque de tipo de SMBIOS 23 en límite")</span><span class="sxs-lookup"><span data-stu-id="2be80-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilites\|Boot Option on Limit")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-154">El límite de la opción de arranque es ON.</span><span class="sxs-lookup"><span data-stu-id="2be80-154">Boot option limit is ON.</span></span> <span data-ttu-id="2be80-155">Identifica la acción del sistema cuando se alcanza el valor de **ResetLimit** .</span><span class="sxs-lookup"><span data-stu-id="2be80-155">Identifies the system action when the **ResetLimit** value is reached.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="2be80-156">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-156">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="2be80-157">**Sistema operativo** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-157">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="2be80-158">**Utilidades del sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-158">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="2be80-159">**No reiniciar** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-159">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-160">**BootOptionOnWatchDog**</span><span class="sxs-lookup"><span data-stu-id="2be80-160">**BootOptionOnWatchDog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-163">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (opción de \| arranque de funcionalidades de tipo SMBIOS 23 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="2be80-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilities\|Boot Option")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-164">Tipo de acción de reinicio después de que transcurra el tiempo del temporizador de vigilante.</span><span class="sxs-lookup"><span data-stu-id="2be80-164">Type of reboot action after the time on the watchdog timer is elapsed.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="2be80-165">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-165">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="2be80-166">**Sistema operativo** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-166">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="2be80-167">**Utilidades del sistema** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-167">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="2be80-168">**No reiniciar** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-168">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-169">**BootROMSupported**</span><span class="sxs-lookup"><span data-stu-id="2be80-169">**BootROMSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-170">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-172">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2be80-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-173">Si es **true**, indica si se admite una ROM de arranque.</span><span class="sxs-lookup"><span data-stu-id="2be80-173">If **True**, indicates whether a boot ROM is supported.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-174">**BootStatus**</span><span class="sxs-lookup"><span data-stu-id="2be80-174">**BootStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-175">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2be80-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-177">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 32 estado de arranque de la información de arranque \| del sistema \| ")</span><span class="sxs-lookup"><span data-stu-id="2be80-177">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 32\|System Boot Information\|Boot Status")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-178">Estado y campos de datos adicionales que identifican el estado de arranque.</span><span class="sxs-lookup"><span data-stu-id="2be80-178">Status and Additional Data fields that identify the boot status.</span></span>

<span data-ttu-id="2be80-179">Este valor procede del miembro de **Estado de arranque** de la estructura de información de **arranque del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2be80-179">This value comes from the **Boot Status** member of the **System Boot Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2be80-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2be80-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-181">**BootupState**</span><span class="sxs-lookup"><span data-stu-id="2be80-181">**BootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-184">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ CLEANBOOT")</span><span class="sxs-lookup"><span data-stu-id="2be80-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)\|SM\_CLEANBOOT")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-185">El sistema se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="2be80-185">System is started.</span></span> <span data-ttu-id="2be80-186">El arranque a prueba de errores omite los archivos de inicio del usuario también denominados SafeBoot.</span><span class="sxs-lookup"><span data-stu-id="2be80-186">Fail-safe boot bypasses the user startup files also called SafeBoot.</span></span>

<span data-ttu-id="2be80-187">La lista siguiente contiene los valores necesarios:</span><span class="sxs-lookup"><span data-stu-id="2be80-187">The following list contains the required values:</span></span>

<dl> <dd><span data-ttu-id="2be80-188">"Arranque normal"</span><span class="sxs-lookup"><span data-stu-id="2be80-188">"Normal boot"</span></span></dd> <dd><span data-ttu-id="2be80-189">"Arranque a prueba de errores"</span><span class="sxs-lookup"><span data-stu-id="2be80-189">"Fail-safe boot"</span></span></dd> <dd><span data-ttu-id="2be80-190">"No seguro con arranque de red"</span><span class="sxs-lookup"><span data-stu-id="2be80-190">"Fail-safe with network boot"</span></span></dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

<span data-ttu-id="2be80-191">**Arranque normal** ("arranque normal")</span><span class="sxs-lookup"><span data-stu-id="2be80-191">**Normal boot** ("Normal boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

<span data-ttu-id="2be80-192">**Arranque a prueba de errores** ("arranque con error")</span><span class="sxs-lookup"><span data-stu-id="2be80-192">**Fail-safe boot** ("Fail-safe boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

<span data-ttu-id="2be80-193">**Error de seguridad con arranque de red** ("error de seguridad con arranque de red")</span><span class="sxs-lookup"><span data-stu-id="2be80-193">**Fail-safe with network boot** ("Fail-safe with network boot")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-194">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2be80-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-197">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2be80-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-198">Breve descripción del objeto de una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="2be80-198">Short description of the object a one-line string.</span></span>

<span data-ttu-id="2be80-199">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-200">**ChassisBootupState**</span><span class="sxs-lookup"><span data-stu-id="2be80-200">**ChassisBootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-201">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-203">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 3 \| Estado de arranque")</span><span class="sxs-lookup"><span data-stu-id="2be80-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Bootup State")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-204">Arranque el estado del chasis.</span><span class="sxs-lookup"><span data-stu-id="2be80-204">Boot up state of the chassis.</span></span>

<span data-ttu-id="2be80-205">Este valor procede del miembro de **Estado de arranque** del alojamiento del **sistema o** de la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2be80-205">This value comes from the **Boot-up State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2be80-206">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-206">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-207">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-207">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="2be80-208">**Safe** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-208">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2be80-209">**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-209">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2be80-210">**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-210">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="2be80-211">**No recuperable** (6)</span><span class="sxs-lookup"><span data-stu-id="2be80-211">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-212">**ChassisSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="2be80-212">**ChassisSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-215">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| número de SKU del chasis de tipo SMBIOS 3 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="2be80-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Chassis\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-216">El número de SKU del chasis o del gabinete como una cadena.</span><span class="sxs-lookup"><span data-stu-id="2be80-216">The chassis or enclosure SKU number as a string.</span></span>

<span data-ttu-id="2be80-217">Este valor procede del miembro del **número de SKU** del **alojamiento del sistema o** de la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2be80-217">This value comes from the **SKU Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2be80-218">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2be80-218">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-219">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2be80-219">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-220">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-222">Calificadores: [ **\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2be80-222">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2be80-223">Nombre de la primera clase concreta de la cadena de herencia de una instancia.</span><span class="sxs-lookup"><span data-stu-id="2be80-223">Name of the first concrete class in the inheritance chain of an instance.</span></span> <span data-ttu-id="2be80-224">Puede usar esta propiedad con otras propiedades de la clase para identificar todas las instancias de la clase y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="2be80-224">You can use this property with other properties of the class to identify all instances of the class and its subclasses.</span></span>

<span data-ttu-id="2be80-225">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-225">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-226">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="2be80-226">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-227">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2be80-227">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-228">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2be80-229">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| de hora estructuras de tiempo de la \| [**\_ \_ información de zona horaria**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="2be80-229">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-230">Cantidad de tiempo que el sistema del equipo unitario se desvía de la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="2be80-230">Amount of time the unitary computer system is offset from Coordinated Universal Time (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-231">**DaylightInEffect**</span><span class="sxs-lookup"><span data-stu-id="2be80-231">**DaylightInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-232">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-234">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Time Functions \| [**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span><span class="sxs-lookup"><span data-stu-id="2be80-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Functions\|[**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-235">Si es **true**, el modo de verano está activado.</span><span class="sxs-lookup"><span data-stu-id="2be80-235">If **True**, the daylight savings mode is ON.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-236">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2be80-236">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-239">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="2be80-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-240">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2be80-240">Description of the object.</span></span>

<span data-ttu-id="2be80-241">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-241">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-242">**ServicePrincipalName**</span><span class="sxs-lookup"><span data-stu-id="2be80-242">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-245">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| GetComputerNameEx \| ComputerNameDnsHostname")</span><span class="sxs-lookup"><span data-stu-id="2be80-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetComputerNameEx\|ComputerNameDnsHostname")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-246">Nombre del equipo local según el servidor de nombres de dominio (DNS).</span><span class="sxs-lookup"><span data-stu-id="2be80-246">Name of local computer according to the domain name server (DNS).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-247">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="2be80-247">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-250">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Structures \| [**WKSTA \_ info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ LANGROUP")</span><span class="sxs-lookup"><span data-stu-id="2be80-250">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**WKSTA\_INFO\_100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100)\|wki100\_langroup")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-251">Nombre del dominio al que pertenece un equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-251">Name of the domain to which a computer belongs.</span></span>

> [!Note]  
> <span data-ttu-id="2be80-252">Si el equipo no forma parte de un dominio, se devuelve el nombre del grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2be80-252">If the computer is not part of a domain, then the name of the workgroup is returned.</span></span>

 

</dd> <dt>

<span data-ttu-id="2be80-253">**DomainRole**</span><span class="sxs-lookup"><span data-stu-id="2be80-253">**DomainRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-254">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-256">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Directory Service (DS) Structures \| [**DSROLE \_ Primary \_ domain \_ info \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**DSROLE \_ \_ role**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| rol")</span><span class="sxs-lookup"><span data-stu-id="2be80-256">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Directory Service (Ds) Structures\| [**DSROLE\_PRIMARY\_DOMAIN\_INFO\_BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic)\|[**DSROLE\_MACHINE\_ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role)\| MachineRole")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-257">Rol de un equipo en un grupo de trabajo de dominio asignado.</span><span class="sxs-lookup"><span data-stu-id="2be80-257">Role of a computer in an assigned domain workgroup.</span></span> <span data-ttu-id="2be80-258">Un grupo de trabajo de dominio es una colección de equipos de la misma red.</span><span class="sxs-lookup"><span data-stu-id="2be80-258">A domain workgroup is a collection of computers on the same network.</span></span> <span data-ttu-id="2be80-259">Por ejemplo, una propiedad **DomainRole** puede mostrar que un equipo es una estación de trabajo miembro.</span><span class="sxs-lookup"><span data-stu-id="2be80-259">For example, a **DomainRole** property may show that a computer is a member workstation.</span></span>

<span data-ttu-id="2be80-260">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-260">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

<span data-ttu-id="2be80-261">**Estación de trabajo independiente** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-261">**Standalone Workstation** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

<span data-ttu-id="2be80-262">**Estación de trabajo miembro** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-262">**Member Workstation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

<span data-ttu-id="2be80-263">**Servidor independiente** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-263">**Standalone Server** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

<span data-ttu-id="2be80-264">**Servidor miembro** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-264">**Member Server** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="2be80-265">**Controlador de dominio de copia de seguridad** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-265">**Backup Domain Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="2be80-266">**Controlador de dominio principal** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-266">**Primary Domain Controller** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-267">**EnableDaylightSavingsTime**</span><span class="sxs-lookup"><span data-stu-id="2be80-267">**EnableDaylightSavingsTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-268">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-269">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2be80-270">Habilita el horario de verano (DST) en un equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-270">Enables daylight savings time (DST) on a computer.</span></span> <span data-ttu-id="2be80-271">Un valor de **true** indica que la hora del sistema cambia a una hora de antemano o detrás cuando se inicia o finaliza el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2be80-271">A value of **True** indicates that the system time changes to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="2be80-272">Un valor de **false** indica que la hora del sistema no cambia a una hora de antemano o de retraso cuando se inicia o finaliza el horario de verano.</span><span class="sxs-lookup"><span data-stu-id="2be80-272">A value of **False** indicates that the system time does not change to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="2be80-273">Un valor **null** indica que el estado de DST es desconocido en un sistema.</span><span class="sxs-lookup"><span data-stu-id="2be80-273">A value of **NULL** indicates that the DST status is unknown on a system.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-274">**FrontPanelResetStatus**</span><span class="sxs-lookup"><span data-stu-id="2be80-274">**FrontPanelResetStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-275">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-277">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 24 \| configuración de seguridad de hardware \| FrontPanelResetStatus")</span><span class="sxs-lookup"><span data-stu-id="2be80-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|FrontPanelResetStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-278">En la tabla siguiente se muestra la configuración de seguridad de hardware para el botón de restablecimiento de un equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-278">The following table lists the hardware security settings for the reset button on a computer.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2be80-279">**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-279">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2be80-280">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-280">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2be80-281">**No implementado** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-281">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-282">**Desconocido** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-282">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-283">**HypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="2be80-283">**HypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-284">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-286">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2be80-286">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-287">Si es **true**, hay un hipervisor presente.</span><span class="sxs-lookup"><span data-stu-id="2be80-287">If **True**, a hypervisor is present.</span></span>

<span data-ttu-id="2be80-288">**Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 8 y Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2be80-288">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-289">**InfraredSupported**</span><span class="sxs-lookup"><span data-stu-id="2be80-289">**InfraredSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-290">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-291">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-292">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2be80-292">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-293">Si **es true**, existe un puerto de infrarrojos (ir) en un equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-293">If **True**, an infrared (IR) port exists on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-294">**InitialLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="2be80-294">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-295">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2be80-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2be80-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2be80-297">Datos necesarios para buscar el dispositivo de carga inicial o el servicio de arranque para solicitar que se inicie el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2be80-297">Data required to find the initial load device or boot service to request that the operating system start up.</span></span>

<span data-ttu-id="2be80-298">Esta propiedad se hereda de [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-298">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<span data-ttu-id="2be80-299">**Windows Server 2008 R2:** Esta propiedad está disponible, pero está vacía.</span><span class="sxs-lookup"><span data-stu-id="2be80-299">**Windows Server 2008 R2:** This property is available, but empty.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2be80-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-301">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2be80-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-303">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="2be80-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-304">El objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="2be80-304">Object is installed.</span></span> <span data-ttu-id="2be80-305">Un objeto no necesita un valor para indicar que está instalado.</span><span class="sxs-lookup"><span data-stu-id="2be80-305">An object does not need a value to indicate that it is installed.</span></span>

<span data-ttu-id="2be80-306">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-307">**KeyboardPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="2be80-307">**KeyboardPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-308">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-310">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 24 \| configuración de seguridad de hardware \| KeyboardPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="2be80-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|KeyboardPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-311">Configuración de seguridad del hardware del sistema para el estado de la contraseña del teclado.</span><span class="sxs-lookup"><span data-stu-id="2be80-311">System hardware security settings for Keyboard Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2be80-312">**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-312">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2be80-313">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-313">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2be80-314">**No implementado** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-314">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-315">**Desconocido** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-315">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-316">**LastLoadInfo**</span><span class="sxs-lookup"><span data-stu-id="2be80-316">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2be80-319">Entrada de matriz de la propiedad **InitialLoadInfo** que contiene los datos para iniciar el sistema operativo cargado.</span><span class="sxs-lookup"><span data-stu-id="2be80-319">Array entry of the **InitialLoadInfo** property that contains the data to start the loaded operating system.</span></span>

<span data-ttu-id="2be80-320">Esta propiedad se hereda de [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-320">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-321">**Le**</span><span class="sxs-lookup"><span data-stu-id="2be80-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-324">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| fabricante de información del sistema de tipo de SMBIOS 1 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="2be80-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-325">Nombre del fabricante de un equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-325">Name of a computer manufacturer.</span></span>

<span data-ttu-id="2be80-326">Ejemplo: Adventure Works</span><span class="sxs-lookup"><span data-stu-id="2be80-326">Example: Adventure Works</span></span>

</dd> <dt>

<span data-ttu-id="2be80-327">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="2be80-327">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-328">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-330">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 1 \| System Information \| Product Name")</span><span class="sxs-lookup"><span data-stu-id="2be80-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Product Name")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-331">Nombre del producto que un fabricante proporciona a un equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-331">Product name that a manufacturer gives to a computer.</span></span> <span data-ttu-id="2be80-332">Esta propiedad debe tener un valor.</span><span class="sxs-lookup"><span data-stu-id="2be80-332">This property must have a value.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-333">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2be80-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-334">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-336">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2be80-336">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2be80-337">Clave de una [**instancia \_ del sistema CIM**](cim-system.md) en un entorno empresarial.</span><span class="sxs-lookup"><span data-stu-id="2be80-337">Key of a [**CIM\_System**](cim-system.md) instance in an enterprise environment.</span></span>

<span data-ttu-id="2be80-338">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-339">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="2be80-339">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2be80-342">Valor de **nombre** de sistema del equipo que se genera automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2be80-342">Computer system **Name** value that is generated automatically.</span></span> <span data-ttu-id="2be80-343">El [**objeto \_ ComputerSystem de CIM**](cim-computersystem.md) y sus derivados son objetos de nivel superior del modelo de información común (CIM).</span><span class="sxs-lookup"><span data-stu-id="2be80-343">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of the Common Information Model (CIM).</span></span> <span data-ttu-id="2be80-344">Proporcionan el ámbito de varios componentes.</span><span class="sxs-lookup"><span data-stu-id="2be80-344">They provide the scope for several components.</span></span> <span data-ttu-id="2be80-345">Se requieren claves de [**\_ Sistema CIM**](cim-system.md) únicas, pero se puede definir una heurística para crear el nombre de **\_ ComputerSystem de CIM** que genera el mismo nombre y es independiente del Protocolo de detección.</span><span class="sxs-lookup"><span data-stu-id="2be80-345">Unique [**CIM\_System**](cim-system.md) keys are required, but you can define a heuristic to create the **CIM\_ComputerSystem** name that generates the same name, and is independent from the discovery protocol.</span></span> <span data-ttu-id="2be80-346">Esto evita los problemas de inventario y administración cuando el mismo recurso o entidad se detecta varias veces, pero no se puede resolver en un objeto.</span><span class="sxs-lookup"><span data-stu-id="2be80-346">This prevents inventory and management problems when the same asset or entity is discovered multiple times, but cannot be resolved to one object.</span></span> <span data-ttu-id="2be80-347">Se recomienda usar una heurística, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="2be80-347">Using a heuristic is recommended, but not required.</span></span>

<span data-ttu-id="2be80-348">La heurística se describe en la especificación de modelo común de CIM V2 y presupone que las reglas documentadas se utilizan para determinar y asignar un nombre.</span><span class="sxs-lookup"><span data-stu-id="2be80-348">The heuristic is outlined in the CIM V2 Common Model specification, and assumes that the documented rules are used to determine and assign a name.</span></span> <span data-ttu-id="2be80-349">La lista de valores de **NameFormat** define el orden de asignación de un nombre de sistema de equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-349">The **NameFormat** values list defines the order to assign a computer system name.</span></span> <span data-ttu-id="2be80-350">Varias reglas se asignan al mismo valor.</span><span class="sxs-lookup"><span data-stu-id="2be80-350">Several rules map to the same value.</span></span>

<span data-ttu-id="2be80-351">El valor de [**\_ nombre de ComputerSystem de CIM**](cim-computersystem.md) que se calcula con la heurística es el valor de clave del sistema.</span><span class="sxs-lookup"><span data-stu-id="2be80-351">The [**CIM\_ComputerSystem Name**](cim-computersystem.md) value that is calculated using the heuristic is the key value of the system.</span></span> <span data-ttu-id="2be80-352">Sin embargo, use alias para asignar un nombre diferente para el equipo de **CIM \_**, que puede ser más exclusivo para su empresa.</span><span class="sxs-lookup"><span data-stu-id="2be80-352">However, use aliases to assign a different name for **CIM\_ComputerSystem**, which can be more unique to your company.</span></span>

<span data-ttu-id="2be80-353">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-353">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="2be80-354">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2be80-354">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="2be80-355">**IP** ("IP")</span><span class="sxs-lookup"><span data-stu-id="2be80-355">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="2be80-356">**Dial** ("dial")</span><span class="sxs-lookup"><span data-stu-id="2be80-356">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="2be80-357">**HID** ("HID")</span><span class="sxs-lookup"><span data-stu-id="2be80-357">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="2be80-358">**NWA** ("NWA")</span><span class="sxs-lookup"><span data-stu-id="2be80-358">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="2be80-359">**Hwa** ("Hwa")</span><span class="sxs-lookup"><span data-stu-id="2be80-359">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="2be80-360">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="2be80-360">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="2be80-361">**ISDN (RDSI** ) ("ISDN")</span><span class="sxs-lookup"><span data-stu-id="2be80-361">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="2be80-362">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="2be80-362">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="2be80-363">**DCC** ("DCC")</span><span class="sxs-lookup"><span data-stu-id="2be80-363">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="2be80-364">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="2be80-364">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="2be80-365">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="2be80-365">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="2be80-366">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="2be80-366">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="2be80-367">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="2be80-367">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2be80-368">**Otro** ("otro")</span><span class="sxs-lookup"><span data-stu-id="2be80-368">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-369">**NetworkServerModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="2be80-369">**NetworkServerModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-370">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-372">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Network Management Structures \| [**Server \_ info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ Type \| SV \_ Type \_ Server")</span><span class="sxs-lookup"><span data-stu-id="2be80-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SERVER\_INFO\_101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101)\|sv101\_type\|SV\_TYPE\_SERVER")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-373">Si es **true**, el modo de servidor de red está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2be80-373">If **True**, the network Server Mode is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-374">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="2be80-374">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-375">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2be80-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-377">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2be80-377">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-378">Número de procesadores lógicos disponibles en el equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-378">Number of logical processors available on the computer.</span></span>

<span data-ttu-id="2be80-379">Puede usar **NumberOfLogicalProcessors** y **NumberOfProcessors** para determinar si el equipo es hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="2be80-379">You can use **NumberOfLogicalProcessors** and **NumberOfProcessors** to determine if the computer is hyperthreading.</span></span> <span data-ttu-id="2be80-380">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2be80-380">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-381">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="2be80-381">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-382">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2be80-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-384">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| System Information Structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| dwNumberOfProcessors")</span><span class="sxs-lookup"><span data-stu-id="2be80-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|dwNumberOfProcessors")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-385">Número de procesadores físicos disponibles actualmente en un sistema.</span><span class="sxs-lookup"><span data-stu-id="2be80-385">Number of physical processors currently available on a system.</span></span> <span data-ttu-id="2be80-386">Es el número de procesadores habilitados para un sistema, que no incluye los procesadores deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="2be80-386">This is the number of enabled processors for a system, which does not include the disabled processors.</span></span> <span data-ttu-id="2be80-387">Si un equipo tiene dos procesadores físicos que contienen dos procesadores lógicos, el valor de **NumberOfProcessors** es 2 y **NumberOfLogicalProcessors** es 4.</span><span class="sxs-lookup"><span data-stu-id="2be80-387">If a computer system has two physical processors each containing two logical processors, then the value of **NumberOfProcessors** is 2 and **NumberOfLogicalProcessors** is 4.</span></span> <span data-ttu-id="2be80-388">Los procesadores pueden ser varios núcleos o pueden ser procesadores de hiperproceso.</span><span class="sxs-lookup"><span data-stu-id="2be80-388">The processors may be multicore or they may be hyperthreading processors.</span></span> <span data-ttu-id="2be80-389">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="2be80-389">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-390">**OEMLogoBitmap**</span><span class="sxs-lookup"><span data-stu-id="2be80-390">**OEMLogoBitmap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-391">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="2be80-391">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2be80-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-393">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2be80-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-394">Lista de datos de un mapa de bits que crea el fabricante de equipos originales (OEM).</span><span class="sxs-lookup"><span data-stu-id="2be80-394">List of data for a bitmap that the original equipment manufacturer (OEM) creates.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-395">**OEMStringArray**</span><span class="sxs-lookup"><span data-stu-id="2be80-395">**OEMStringArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-396">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2be80-396">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2be80-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-398">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo SMBIOS 11 \| cadenas OEM")</span><span class="sxs-lookup"><span data-stu-id="2be80-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 11\|OEM Strings")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-399">Lista de cadenas de formato libre que define un OEM.</span><span class="sxs-lookup"><span data-stu-id="2be80-399">List of free-form strings that an OEM defines.</span></span> <span data-ttu-id="2be80-400">Por ejemplo, un OEM define los números de pieza de los documentos de referencia del sistema, la información de contacto del fabricante, etc.</span><span class="sxs-lookup"><span data-stu-id="2be80-400">For example, an OEM defines the part numbers for system reference documents, manufacturer contact information, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-401">**PartOfDomain**</span><span class="sxs-lookup"><span data-stu-id="2be80-401">**PartOfDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-402">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-404">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="2be80-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-405">Si es **true**, el equipo forma parte de un dominio.</span><span class="sxs-lookup"><span data-stu-id="2be80-405">If **True**, the computer is part of a domain.</span></span> <span data-ttu-id="2be80-406">Si el valor es **null**, el equipo no se encuentra en un dominio o el estado es desconocido.</span><span class="sxs-lookup"><span data-stu-id="2be80-406">If the value is **NULL**, the computer is not in a domain or the status is unknown.</span></span> <span data-ttu-id="2be80-407">Si quita el equipo de un dominio, el valor se convierte en **false**.</span><span class="sxs-lookup"><span data-stu-id="2be80-407">If you remove the computer from a domain, the value becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-408">**PauseAfterReset**</span><span class="sxs-lookup"><span data-stu-id="2be80-408">**PauseAfterReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-409">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="2be80-409">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-411">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| tiempo de espera de tipo de SMBIOS 23"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")</span><span class="sxs-lookup"><span data-stu-id="2be80-411">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-412">Retraso de tiempo antes de que se inicie un reinicio en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="2be80-412">Time delay before a reboot is initiated in milliseconds.</span></span> <span data-ttu-id="2be80-413">Se utiliza después de un ciclo de alimentación del sistema, un restablecimiento local o remoto del sistema y el restablecimiento automático del sistema.</span><span class="sxs-lookup"><span data-stu-id="2be80-413">It is used after a system power cycle, local or remote system reset, and automatic system reset.</span></span> <span data-ttu-id="2be80-414">Un valor de 1 (menos uno) indica que se desconoce el valor de pausa.</span><span class="sxs-lookup"><span data-stu-id="2be80-414">A value of  1 (minus one) indicates that the pause value is unknown.</span></span>

<span data-ttu-id="2be80-415">**Windows Vista:** Esta propiedad puede devolver un número desconocido.</span><span class="sxs-lookup"><span data-stu-id="2be80-415">**Windows Vista:** This property may return an unknown number.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-416">**PCSystemType**</span><span class="sxs-lookup"><span data-stu-id="2be80-416">**PCSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-417">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-419">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="2be80-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-420">Tipo de equipo en uso, como portátil, escritorio o tableta.</span><span class="sxs-lookup"><span data-stu-id="2be80-420">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="2be80-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>No **especificado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="2be80-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Escritorio** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="2be80-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Móvil** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="2be80-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Estación de trabajo** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="2be80-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="2be80-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Servidor Soho** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO Server** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-427">Servidor de oficinas pequeñas y oficinas domésticas (SOHO)</span><span class="sxs-lookup"><span data-stu-id="2be80-427">Small Office and Home Office (SOHO) Server</span></span>

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="2be80-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**PC del dispositivo** (6)</span><span class="sxs-lookup"><span data-stu-id="2be80-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="2be80-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Servidor de rendimiento** (7)</span><span class="sxs-lookup"><span data-stu-id="2be80-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="2be80-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (8)</span><span class="sxs-lookup"><span data-stu-id="2be80-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-431">**PCSystemTypeEx**</span><span class="sxs-lookup"><span data-stu-id="2be80-431">**PCSystemTypeEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-432">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-433">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-434">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="2be80-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-435">Tipo de equipo en uso, como portátil, escritorio o tableta.</span><span class="sxs-lookup"><span data-stu-id="2be80-435">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<span data-ttu-id="2be80-436">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="2be80-436">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="2be80-437">No **especificado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-437">**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="2be80-438">**Escritorio** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-438">**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="2be80-439">**Móvil** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-439">**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="2be80-440">**Estación de trabajo** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-440">**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="2be80-441">**Enterprise Server** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-441">**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="2be80-442">**Servidor Soho** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-442">**SOHO Server** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="2be80-443">**PC del dispositivo** (6)</span><span class="sxs-lookup"><span data-stu-id="2be80-443">**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="2be80-444">**Servidor de rendimiento** (7)</span><span class="sxs-lookup"><span data-stu-id="2be80-444">**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

<span data-ttu-id="2be80-445">**Pizarra** (8)</span><span class="sxs-lookup"><span data-stu-id="2be80-445">**Slate** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="2be80-446">**Máximo** (9)</span><span class="sxs-lookup"><span data-stu-id="2be80-446">**Maximum** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-447">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2be80-447">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-448">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-448">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2be80-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-450">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Controles de alimentación del sistema DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="2be80-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-451">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2be80-451">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2be80-452">Esta propiedad se hereda del **\_ LogicalDevice de CIM**.</span><span class="sxs-lookup"><span data-stu-id="2be80-452">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2be80-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2be80-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2be80-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-457">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2be80-457">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2be80-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-459">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="2be80-459">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2be80-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-461">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="2be80-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2be80-462">Este método se encuentra en la clase primaria de **\_ LogicalDevice de CIM** y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="2be80-462">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2be80-463">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2be80-463">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2be80-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="2be80-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-465">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="2be80-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2be80-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="2be80-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-467">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="2be80-467">Timed Power-On Supported</span></span>

<span data-ttu-id="2be80-468">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="2be80-468">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-469">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2be80-469">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-470">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2be80-470">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-471">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2be80-472">Si **es true**, el dispositivo puede administrarse con energía, por ejemplo, un dispositivo se puede poner en modo de suspensión, etc.</span><span class="sxs-lookup"><span data-stu-id="2be80-472">If **True**, device can be power-managed, for example, a device can be put into suspend mode, and so on.</span></span> <span data-ttu-id="2be80-473">Esta propiedad no indica que las características de administración de energía están habilitadas actualmente, pero indica que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="2be80-473">This property does not indicate that power management features are enabled currently, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="2be80-474">Esta propiedad se hereda de [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-474">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-475">**PowerOnPasswordStatus**</span><span class="sxs-lookup"><span data-stu-id="2be80-475">**PowerOnPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-476">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-476">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-478">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 24 \| configuración de seguridad de hardware \| PowerOnPasswordStatus")</span><span class="sxs-lookup"><span data-stu-id="2be80-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|PowerOnPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-479">Configuración de seguridad de hardware del sistema para Power-On estado de contraseña.</span><span class="sxs-lookup"><span data-stu-id="2be80-479">System hardware security settings for Power-On Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2be80-480">**Deshabilitado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-480">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2be80-481">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-481">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2be80-482">**No implementado** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-482">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-483">**Desconocido** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-483">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-484">**PowerState**</span><span class="sxs-lookup"><span data-stu-id="2be80-484">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-485">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-486">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2be80-487">Estado de energía actual de un equipo y su sistema operativo asociado.</span><span class="sxs-lookup"><span data-stu-id="2be80-487">Current power state of a computer and its associated operating system.</span></span> <span data-ttu-id="2be80-488">Los Estados de ahorro de energía tienen los siguientes valores: valor 4 (desconocido) indica que se sabe que el sistema está en modo de ahorro de energía, pero su estado exacto en este modo es desconocido; 2 (modo de baja energía) indica que el sistema está en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado. 3 (en espera) indica que el sistema no funciona, pero podría volverse a la alimentación completa rápidamente. y 7 (ADVERTENCIA) indica que el equipo está en estado de advertencia y en modo de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="2be80-488">The power saving states have the following values: Value 4 (Unknown) indicates that the system is known to be in a power save mode, but its exact status in this mode is unknown; 2 (Low Power Mode) indicates that the system is in a power save state, but still functioning and may exhibit degraded performance; 3 (Standby) indicates that the system is not functioning, but could be brought to full power quickly; and 7 (Warning) indicates that the computer system is in a warning state and a power save mode.</span></span>

<span data-ttu-id="2be80-489">Esta propiedad se hereda de [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-489">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="2be80-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Potencia completa** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2be80-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2be80-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2be80-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2be80-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2be80-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (6** )</span><span class="sxs-lookup"><span data-stu-id="2be80-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2be80-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (7)</span><span class="sxs-lookup"><span data-stu-id="2be80-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="2be80-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Ahorro **de energía: hibernación** (8)</span><span class="sxs-lookup"><span data-stu-id="2be80-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-499">Power Save Hibernate.</span><span class="sxs-lookup"><span data-stu-id="2be80-499">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="2be80-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Ahorro **de energía: Soft off** (9)</span><span class="sxs-lookup"><span data-stu-id="2be80-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-501">Ahorro flexible de energía.</span><span class="sxs-lookup"><span data-stu-id="2be80-501">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-502">**PowerSupplyState**</span><span class="sxs-lookup"><span data-stu-id="2be80-502">**PowerSupplyState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-503">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-503">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-504">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-505">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("el \| \| alojamiento del sistema de tipo SMBIOS 3 o el estado de la fuente de alimentación del chasis \| ")</span><span class="sxs-lookup"><span data-stu-id="2be80-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Power Supply State")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-506">Estado de la fuente de alimentación o suministros cuando se arrancó por última vez.</span><span class="sxs-lookup"><span data-stu-id="2be80-506">State of the power supply or supplies when last booted.</span></span>

<span data-ttu-id="2be80-507">Este valor procede del miembro de estado de la **fuente de alimentación** del **alojamiento del sistema o** la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2be80-507">This value comes from the **Power Supply State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2be80-508">En la lista siguiente se identifican los valores de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2be80-508">The following list identifies the values for this property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2be80-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="2be80-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2be80-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2be80-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="2be80-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**No recuperable** (6)</span><span class="sxs-lookup"><span data-stu-id="2be80-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non-recoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-515">Irrecuperable</span><span class="sxs-lookup"><span data-stu-id="2be80-515">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-516">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="2be80-516">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-517">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-518">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2be80-519">Información de contacto del propietario del sistema principal, por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.</span><span class="sxs-lookup"><span data-stu-id="2be80-519">Contact information for the primary system owner, for example, phone number, email address, and so on.</span></span>

<span data-ttu-id="2be80-520">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-520">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-521">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="2be80-521">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-522">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-523">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-524">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2be80-524">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2be80-525">Nombre del propietario del sistema principal.</span><span class="sxs-lookup"><span data-stu-id="2be80-525">Name of the primary system owner.</span></span>

<span data-ttu-id="2be80-526">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-526">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-527">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="2be80-527">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-528">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-529">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-530">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Seguridad de hardware del sistema DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="2be80-530">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-531">Si está habilitada, el valor es 4 y el sistema del equipo unitario puede restablecerse con los botones de encendido y restauración.</span><span class="sxs-lookup"><span data-stu-id="2be80-531">If enabled, the value is 4 and the unitary computer system can be reset using the power and reset buttons.</span></span> <span data-ttu-id="2be80-532">Si está deshabilitado, el valor es 3 y no se permite el restablecimiento.</span><span class="sxs-lookup"><span data-stu-id="2be80-532">If disabled, the value is 3, and a reset is not allowed.</span></span>

<span data-ttu-id="2be80-533">Esta propiedad se hereda de [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-533">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2be80-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2be80-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2be80-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="2be80-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**No implementado** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Not Implemented** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2be80-539">Irrecuperable</span><span class="sxs-lookup"><span data-stu-id="2be80-539">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-540">**ResetCount**</span><span class="sxs-lookup"><span data-stu-id="2be80-540">**ResetCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-541">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2be80-541">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-542">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-543">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) de inicio (" \| recuento de restablecimiento del sistema de tipo SMBIOS 23 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="2be80-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\|Reset Count")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-544">Número de restablecimientos automáticos desde el último restablecimiento.</span><span class="sxs-lookup"><span data-stu-id="2be80-544">Number of automatic resets since the last reset.</span></span> <span data-ttu-id="2be80-545">Un valor de 1 (menos uno) indica que se desconoce el recuento.</span><span class="sxs-lookup"><span data-stu-id="2be80-545">A value of  1 (minus one) indicates that the count is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-546">**ResetLimit**</span><span class="sxs-lookup"><span data-stu-id="2be80-546">**ResetLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-547">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="2be80-547">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-548">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-549">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo de SMBIOS \| 23 límite de restablecimiento \| del sistema \| ")</span><span class="sxs-lookup"><span data-stu-id="2be80-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\| Reset Limit")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-550">Número de veces consecutivas en las que se intenta restablecer el sistema.</span><span class="sxs-lookup"><span data-stu-id="2be80-550">Number of consecutive times a system reset is attempted.</span></span> <span data-ttu-id="2be80-551">Un valor de 1 (menos uno) indica que se desconoce el límite.</span><span class="sxs-lookup"><span data-stu-id="2be80-551">A value of  1 (minus one) indicates that the limit is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-552">**Roles**</span><span class="sxs-lookup"><span data-stu-id="2be80-552">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-553">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2be80-553">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2be80-554">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2be80-555">Lista que especifica los roles de un sistema en el entorno de tecnología de la información.</span><span class="sxs-lookup"><span data-stu-id="2be80-555">List that specifies the roles of a system in the information technology environment.</span></span>

<span data-ttu-id="2be80-556">Esta propiedad se hereda del [**\_ Sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-556">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-557">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2be80-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-558">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-559">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-560">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2be80-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-561">Estado actual de un objeto.</span><span class="sxs-lookup"><span data-stu-id="2be80-561">Current status of an object.</span></span>

<span data-ttu-id="2be80-562">Por Win32_ComputerSystem, el estado siempre es "correcto".</span><span class="sxs-lookup"><span data-stu-id="2be80-562">For Win32_ComputerSystem, the Status is always “OK”.</span></span>

<span data-ttu-id="2be80-563">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-563">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dl>

</dd> <dt>

<span data-ttu-id="2be80-564">**SupportContactDescription**</span><span class="sxs-lookup"><span data-stu-id="2be80-564">**SupportContactDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-565">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2be80-565">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2be80-566">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-567">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| [**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| support Information")</span><span class="sxs-lookup"><span data-stu-id="2be80-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring)\|Support Information")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-568">Lista de la información de contacto de soporte técnico para el sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="2be80-568">List of the support contact information for the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-569">**SystemFamily**</span><span class="sxs-lookup"><span data-stu-id="2be80-569">**SystemFamily**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-570">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-571">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-572">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| grupo de información del sistema de tipo SMBIOS 1 \| \| ")</span><span class="sxs-lookup"><span data-stu-id="2be80-572">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Family")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-573">Familia a la que pertenece un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="2be80-573">The family to which a particular computer belongs.</span></span> <span data-ttu-id="2be80-574">Una familia hace referencia a un conjunto de equipos que son similares pero no idénticos desde un punto de vista de hardware o software.</span><span class="sxs-lookup"><span data-stu-id="2be80-574">A family refers to a set of computers that are similar but not identical from a hardware or software point of view.</span></span>

<span data-ttu-id="2be80-575">Este valor procede del miembro **Family** de la estructura de **información del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2be80-575">This value comes from the **Family** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2be80-576">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2be80-576">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-577">**SystemSKUNumber**</span><span class="sxs-lookup"><span data-stu-id="2be80-577">**SystemSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-578">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-579">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-580">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 1 \| información del sistema \| número SKU")</span><span class="sxs-lookup"><span data-stu-id="2be80-580">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-581">Identifica una configuración de equipo determinada para la venta.</span><span class="sxs-lookup"><span data-stu-id="2be80-581">Identifies a particular computer configuration for sale.</span></span> <span data-ttu-id="2be80-582">A veces también se denomina ID. de producto o número de pedido de compra.</span><span class="sxs-lookup"><span data-stu-id="2be80-582">It is sometimes also called a product ID or purchase order number.</span></span>

<span data-ttu-id="2be80-583">Este valor procede del miembro de **número de SKU** de la estructura de **información del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2be80-583">This value comes from the **SKU Number** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="2be80-584">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="2be80-584">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-585">**SystemStartupDelay**</span><span class="sxs-lookup"><span data-stu-id="2be80-585">**SystemStartupDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-586">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-586">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-587">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-587">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2be80-588">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilegios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| [**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| boot loader \| timeout"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span><span class="sxs-lookup"><span data-stu-id="2be80-588">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint)\|Boot Loader\|timeout"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-589">**SystemStartupDelay** ya no está disponible para su uso porque Boot.ini no se usa para configurar el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="2be80-589">**SystemStartupDelay** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="2be80-590">En su lugar, use las [clases BCD](/previous-versions/windows/desktop/bcd/bcd-classes) suministradas por el proveedor WMI de datos de la configuración de arranque (BCD) (BCD) o el comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="2be80-590">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-591">**SystemStartupOptions**</span><span class="sxs-lookup"><span data-stu-id="2be80-591">**SystemStartupOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-592">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2be80-592">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2be80-593">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-593">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2be80-594">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilegios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| [**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| sistemas operativos")</span><span class="sxs-lookup"><span data-stu-id="2be80-594">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection)\|Operating Systems")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-595">**SystemStartupOptions** ya no está disponible para su uso porque Boot.ini no se usa para configurar el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="2be80-595">**SystemStartupOptions** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="2be80-596">En su lugar, use las [clases BCD](/previous-versions/windows/desktop/bcd/bcd-classes) suministradas por el proveedor WMI de datos de la configuración de arranque (BCD) (BCD) o el comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="2be80-596">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-597">**SystemStartupSetting**</span><span class="sxs-lookup"><span data-stu-id="2be80-597">**SystemStartupSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-598">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2be80-598">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-599">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-599">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2be80-600">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**privilegios**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2be80-600">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-601">**SystemStartupSetting** ya no está disponible para su uso porque Boot.ini no se usa para configurar el inicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="2be80-601">**SystemStartupSetting** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="2be80-602">En su lugar, use las [clases BCD](/previous-versions/windows/desktop/bcd/bcd-classes) suministradas por el proveedor WMI de datos de la configuración de arranque (BCD) (BCD) o el comando **bcdedit** .</span><span class="sxs-lookup"><span data-stu-id="2be80-602">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="2be80-603">**SystemType**</span><span class="sxs-lookup"><span data-stu-id="2be80-603">**SystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-604">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-605">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-605">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-606">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| System Information Structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| wProcessorArchitecture")</span><span class="sxs-lookup"><span data-stu-id="2be80-606">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|wProcessorArchitecture")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-607">Sistema que se ejecuta en el equipo basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="2be80-607">System running on the Windows-based computer.</span></span> <span data-ttu-id="2be80-608">Esta propiedad debe tener un valor.</span><span class="sxs-lookup"><span data-stu-id="2be80-608">This property must have a value.</span></span>

<span data-ttu-id="2be80-609">En la siguiente lista se identifican algunos de los valores posibles para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2be80-609">The following list identifies some of the possible values for this property.</span></span>

<dl> <dd><span data-ttu-id="2be80-610">"equipo basado en x64"</span><span class="sxs-lookup"><span data-stu-id="2be80-610">"x64-based PC"</span></span></dd> <dd><span data-ttu-id="2be80-611">"Equipo basado en x86"</span><span class="sxs-lookup"><span data-stu-id="2be80-611">"X86-based PC"</span></span></dd> <dd><span data-ttu-id="2be80-612">"Equipo basado en MIPS"</span><span class="sxs-lookup"><span data-stu-id="2be80-612">"MIPS-based PC"</span></span></dd> <dd><span data-ttu-id="2be80-613">"Equipo basado en Alpha"</span><span class="sxs-lookup"><span data-stu-id="2be80-613">"Alpha-based PC"</span></span></dd> <dd><span data-ttu-id="2be80-614">"Power PC"</span><span class="sxs-lookup"><span data-stu-id="2be80-614">"Power PC"</span></span></dd> <dd><span data-ttu-id="2be80-615">"SH-x PC"</span><span class="sxs-lookup"><span data-stu-id="2be80-615">"SH-x PC"</span></span></dd> <dd><span data-ttu-id="2be80-616">"StrongARM PC"</span><span class="sxs-lookup"><span data-stu-id="2be80-616">"StrongARM PC"</span></span></dd> <dd><span data-ttu-id="2be80-617">"PC Intel de 64 bits"</span><span class="sxs-lookup"><span data-stu-id="2be80-617">"64-bit Intel PC"</span></span></dd> <dd><span data-ttu-id="2be80-618">"PC Alpha de 64 bits"</span><span class="sxs-lookup"><span data-stu-id="2be80-618">"64-bit Alpha PC"</span></span></dd> <dd><span data-ttu-id="2be80-619">Unknown</span><span class="sxs-lookup"><span data-stu-id="2be80-619">"Unknown"</span></span></dd> <dd><span data-ttu-id="2be80-620">"X86-Nec98 PC"</span><span class="sxs-lookup"><span data-stu-id="2be80-620">"X86-Nec98 PC"</span></span></dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

<span data-ttu-id="2be80-621">**Equipo basado en x86** ("equipo basado en x86")</span><span class="sxs-lookup"><span data-stu-id="2be80-621">**X86-based PC** ("X86-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

<span data-ttu-id="2be80-622">**Equipo basado en MIPS** ("equipo basado en MIPS")</span><span class="sxs-lookup"><span data-stu-id="2be80-622">**MIPS-based PC** ("MIPS-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

<span data-ttu-id="2be80-623">**Equipo basado en Alpha** ("equipo basado en Alpha")</span><span class="sxs-lookup"><span data-stu-id="2be80-623">**Alpha-based PC** ("Alpha-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

<span data-ttu-id="2be80-624">**Power PC** ("Power PC")</span><span class="sxs-lookup"><span data-stu-id="2be80-624">**Power PC** ("Power PC")</span></span>


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

<span data-ttu-id="2be80-625">**PC SH-x** ("sh-x PC")</span><span class="sxs-lookup"><span data-stu-id="2be80-625">**SH-x PC** ("SH-x PC")</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

<span data-ttu-id="2be80-626">**PC StrongARM** ("PC StrongARM")</span><span class="sxs-lookup"><span data-stu-id="2be80-626">**StrongARM PC** ("StrongARM PC")</span></span>


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

<span data-ttu-id="2be80-627">**PC Intel de 64 bits** ("sistema intel de 64 bits")</span><span class="sxs-lookup"><span data-stu-id="2be80-627">**64-bit Intel PC** ("64-bit Intel PC")</span></span>


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

<span data-ttu-id="2be80-628">**equipo basado en x64** ("equipo basado en x64")</span><span class="sxs-lookup"><span data-stu-id="2be80-628">**x64-based PC** ("x64-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-629">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="2be80-629">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

<span data-ttu-id="2be80-630">**Equipo x86-nec98** ("x86-nec98 PC")</span><span class="sxs-lookup"><span data-stu-id="2be80-630">**X86-Nec98 PC** ("X86-Nec98 PC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-631">**ThermalState**</span><span class="sxs-lookup"><span data-stu-id="2be80-631">**ThermalState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-632">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-632">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-633">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-634">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| alojamiento del sistema de tipo SMBIOS 3 o \| estado térmico del chasis")</span><span class="sxs-lookup"><span data-stu-id="2be80-634">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Thermal State")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-635">Estado térmico del sistema cuando se arrancó por última vez.</span><span class="sxs-lookup"><span data-stu-id="2be80-635">Thermal state of the system when last booted.</span></span>

<span data-ttu-id="2be80-636">Este valor procede del miembro de **estado térmico** del **alojamiento del sistema o** de la estructura del chasis en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2be80-636">This value comes from the **Thermal State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2be80-637">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-637">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-638">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-638">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="2be80-639">**Safe** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-639">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2be80-640">**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-640">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="2be80-641">**Crítico** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-641">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="2be80-642">**No recuperable** (6)</span><span class="sxs-lookup"><span data-stu-id="2be80-642">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-643">**TotalPhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="2be80-643">**TotalPhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-644">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2be80-644">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-645">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-646">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| estructuras de administración de memoria inesperados win32api \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| dwTotalPhys"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="2be80-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus)\|dwTotalPhys"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-647">Tamaño total de la memoria física.</span><span class="sxs-lookup"><span data-stu-id="2be80-647">Total size of physical memory.</span></span> <span data-ttu-id="2be80-648">Tenga en cuenta que, en algunas circunstancias, es posible que esta propiedad no devuelva un valor preciso para la memoria física.</span><span class="sxs-lookup"><span data-stu-id="2be80-648">Be aware that, under some circumstances, this property may not return an accurate value for the physical memory.</span></span> <span data-ttu-id="2be80-649">Por ejemplo, no es preciso si el BIOS utiliza parte de la memoria física.</span><span class="sxs-lookup"><span data-stu-id="2be80-649">For example, it is not accurate if the BIOS is using some of the physical memory.</span></span> <span data-ttu-id="2be80-650">Para obtener un valor preciso, use la propiedad **Capacity** de [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2be80-650">For an accurate value, use the **Capacity** property in [**Win32\_PhysicalMemory**](win32-physicalmemory.md) instead.</span></span>

<span data-ttu-id="2be80-651">Ejemplo: 67108864</span><span class="sxs-lookup"><span data-stu-id="2be80-651">Example: 67108864</span></span>

<span data-ttu-id="2be80-652">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2be80-652">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2be80-653">**UserName**</span><span class="sxs-lookup"><span data-stu-id="2be80-653">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-654">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-654">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-655">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-655">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-656">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| System Information Functions \| [**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span><span class="sxs-lookup"><span data-stu-id="2be80-656">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Functions\|[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-657">Nombre de un usuario que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="2be80-657">Name of a user that is logged on currently.</span></span> <span data-ttu-id="2be80-658">Esta propiedad debe tener un valor.</span><span class="sxs-lookup"><span data-stu-id="2be80-658">This property must have a value.</span></span> <span data-ttu-id="2be80-659">En una sesión de servicios de Terminal Server, **nombre** de usuario devuelve el nombre del usuario que ha iniciado sesión en la consola y no el usuario que ha iniciado sesión durante la sesión de Terminal Services.</span><span class="sxs-lookup"><span data-stu-id="2be80-659">In a terminal services session, **UserName** returns the name of the user that is logged on to the console not the user logged on during the terminal service session.</span></span>

<span data-ttu-id="2be80-660">Ejemplo: juanpérez</span><span class="sxs-lookup"><span data-stu-id="2be80-660">Example: jeffsmith</span></span>

</dd> <dt>

<span data-ttu-id="2be80-661">**WakeUpType**</span><span class="sxs-lookup"><span data-stu-id="2be80-661">**WakeUpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-662">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2be80-662">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-663">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2be80-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2be80-664">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( \| \| \| tipo de reactivación de información del sistema de tipo SMBIOS 1 ")</span><span class="sxs-lookup"><span data-stu-id="2be80-664">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Wake-up Type")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-665">Evento que hace que el sistema se encienda.</span><span class="sxs-lookup"><span data-stu-id="2be80-665">Event that causes the system to power up.</span></span>

<span data-ttu-id="2be80-666">Este valor procede del miembro de **tipo de reactivación** de la estructura de **información del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="2be80-666">This value comes from the **Wake-up Type** member of the **System Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="2be80-667">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="2be80-667">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2be80-668">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2be80-668">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2be80-669">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2be80-669">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

<span data-ttu-id="2be80-670">**Temporizador de APM** (3)</span><span class="sxs-lookup"><span data-stu-id="2be80-670">**APM Timer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

<span data-ttu-id="2be80-671">**Anillo de módem** (4)</span><span class="sxs-lookup"><span data-stu-id="2be80-671">**Modem Ring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

<span data-ttu-id="2be80-672">**LAN remota** (5)</span><span class="sxs-lookup"><span data-stu-id="2be80-672">**LAN Remote** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

<span data-ttu-id="2be80-673">**Interruptor de alimentación** (6)</span><span class="sxs-lookup"><span data-stu-id="2be80-673">**Power Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

<span data-ttu-id="2be80-674">**PME \# PCI** 7</span><span class="sxs-lookup"><span data-stu-id="2be80-674">**PCI PME\#** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

<span data-ttu-id="2be80-675">**Energía de CA restaurada** (8)</span><span class="sxs-lookup"><span data-stu-id="2be80-675">**AC Power Restored** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2be80-676">**Grupo de trabajo**</span><span class="sxs-lookup"><span data-stu-id="2be80-676">**Workgroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2be80-677">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2be80-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2be80-678">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2be80-678">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="2be80-679">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="2be80-679">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="2be80-680">Nombre del grupo de trabajo de este equipo.</span><span class="sxs-lookup"><span data-stu-id="2be80-680">Name of the workgroup for this computer.</span></span> <span data-ttu-id="2be80-681">Si el valor de la propiedad **PartOfDomain** es **false**, se devuelve el nombre del grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2be80-681">If the value of the **PartOfDomain** property is **False**, then the name of the workgroup is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2be80-682">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2be80-682">Remarks</span></span>

<span data-ttu-id="2be80-683">Para determinar el número total de instancias de procesador asociadas a un objeto de sistema de equipo, use la clase de asociación [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="2be80-683">To determine the total number of processor instances associated with a computer system object, use the [**Win32\_ComputerSystemProcessor**](win32-computersystemprocessor.md) association class.</span></span>

<span data-ttu-id="2be80-684">Una instancia de **Win32 \_ ComputerSystem** que tiene varios procesadores físicos tiene asociadas varias instancias de [**\_ procesador de Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="2be80-684">A **Win32\_ComputerSystem** instance that has multiple physical processors has multiple [**Win32\_Processor**](win32-processor.md) instances associated with it.</span></span> <span data-ttu-id="2be80-685">Si el valor de **NumberOfLogicalProcessors** es mayor que el valor de **NumberOfProcessors** , el sistema del equipo es un sistema multinúcleo o tiene uno o varios procesadores habilitados para el hyperthreading.</span><span class="sxs-lookup"><span data-stu-id="2be80-685">If the value of **NumberOfLogicalProcessors** is greater than the value of **NumberOfProcessors** then the computer system is either a multicore system or has one or more processors enabled for hyperthreading.</span></span> <span data-ttu-id="2be80-686">Para obtener más información, vea las propiedades **NumberOfLogicalProcessors** y **NumberOfCores** y la sección Comentarios en el **\_ procesador Win32**.</span><span class="sxs-lookup"><span data-stu-id="2be80-686">For more information, see the **NumberOfLogicalProcessors** and **NumberOfCores** properties and Remarks section in **Win32\_Processor**.</span></span>

<span data-ttu-id="2be80-687">La clase de **\_ ComputerSystem de Win32** se deriva de [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="2be80-687">The **Win32\_ComputerSystem** class is derived from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2be80-688">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2be80-688">Examples</span></span>

<span data-ttu-id="2be80-689">En el siguiente ejemplo de [código](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) del centro de scripting se usa el **\_ ComputerSystem de Win32** para recuperar información de varios sistemas informáticos y mostrarlos en una GUI.</span><span class="sxs-lookup"><span data-stu-id="2be80-689">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) uses the **Win32\_ComputerSystem** to retrieve information from a number of computer systems, and display them in a GUI.</span></span>

<span data-ttu-id="2be80-690">Puede encontrar un script de ejemplo que obtiene los datos del sistema operativo y del procesador de **Win32 \_ ComputerSystem**, el [**\_ procesador Win32**](win32-processor.md)y el [**\_ OperatingSystem de Win32**](win32-operatingsystem.md) en los ejemplos de temas del [**\_ procesador Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="2be80-690">You can find an example script that obtains operating system and processor data from **Win32\_ComputerSystem**, [**Win32\_Processor**](win32-processor.md), and [**Win32\_OperatingSystem**](win32-operatingsystem.md) in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="2be80-691">En el siguiente ejemplo de VBScript se describe cómo recuperar el nombre de dominio del equipo local de las instancias de **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="2be80-691">The following VBScript sample describes how to retrieve the domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



<span data-ttu-id="2be80-692">En el siguiente ejemplo de Perl se describe cómo recuperar el nombre del equipo local de las instancias de **\_ ComputerSystem de Win32**.</span><span class="sxs-lookup"><span data-stu-id="2be80-692">The following Perl sample describes how to retrieve the local machine name from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="2be80-693">En el siguiente ejemplo de Perl se describe cómo recuperar el nombre de dominio DNS del equipo local de las instancias de **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="2be80-693">The following Perl sample describes how to retrieve the DNS domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="2be80-694">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be80-694">Requirements</span></span>



| <span data-ttu-id="2be80-695">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be80-695">Requirement</span></span> | <span data-ttu-id="2be80-696">Value</span><span class="sxs-lookup"><span data-stu-id="2be80-696">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2be80-697">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2be80-697">Minimum supported client</span></span><br/> | <span data-ttu-id="2be80-698">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2be80-698">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2be80-699">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2be80-699">Minimum supported server</span></span><br/> | <span data-ttu-id="2be80-700">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2be80-700">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2be80-701">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2be80-701">Namespace</span></span><br/>                | <span data-ttu-id="2be80-702">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2be80-702">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2be80-703">MOF</span><span class="sxs-lookup"><span data-stu-id="2be80-703">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2be80-704"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2be80-704"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2be80-705">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2be80-705">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2be80-706"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2be80-706"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be80-707">Vea también</span><span class="sxs-lookup"><span data-stu-id="2be80-707">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be80-708">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="2be80-708">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dt>

<span data-ttu-id="2be80-709">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2be80-709">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2be80-710">Tareas de WMI: cuentas y dominios</span><span class="sxs-lookup"><span data-stu-id="2be80-710">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2be80-711">Tareas WMI: hardware del equipo</span><span class="sxs-lookup"><span data-stu-id="2be80-711">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="2be80-712">Tareas WMI: administración de escritorio</span><span class="sxs-lookup"><span data-stu-id="2be80-712">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

