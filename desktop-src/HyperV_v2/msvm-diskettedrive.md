---
description: Representa una unidad de disquete dentro de la máquina virtual.
ms.assetid: 4624ABAF-3761-416F-9044-7A39EBF53D3D
title: Clase Msvm_DisketteDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive
- Msvm_DisketteDrive.SetPowerState
- Msvm_DisketteDrive.EnableDevice
- Msvm_DisketteDrive.OnlineDevice
- Msvm_DisketteDrive.QuiesceDevice
- Msvm_DisketteDrive.SaveProperties
- Msvm_DisketteDrive.RestoreProperties
- Msvm_DisketteDrive.InstanceID
- Msvm_DisketteDrive.Caption
- Msvm_DisketteDrive.Description
- Msvm_DisketteDrive.ElementName
- Msvm_DisketteDrive.InstallDate
- Msvm_DisketteDrive.Name
- Msvm_DisketteDrive.OperationalStatus
- Msvm_DisketteDrive.StatusDescriptions
- Msvm_DisketteDrive.Status
- Msvm_DisketteDrive.HealthState
- Msvm_DisketteDrive.CommunicationStatus
- Msvm_DisketteDrive.DetailedStatus
- Msvm_DisketteDrive.OperatingStatus
- Msvm_DisketteDrive.PrimaryStatus
- Msvm_DisketteDrive.EnabledState
- Msvm_DisketteDrive.OtherEnabledState
- Msvm_DisketteDrive.RequestedState
- Msvm_DisketteDrive.EnabledDefault
- Msvm_DisketteDrive.TimeOfLastStateChange
- Msvm_DisketteDrive.AvailableRequestedStates
- Msvm_DisketteDrive.TransitioningToState
- Msvm_DisketteDrive.SystemCreationClassName
- Msvm_DisketteDrive.SystemName
- Msvm_DisketteDrive.CreationClassName
- Msvm_DisketteDrive.DeviceID
- Msvm_DisketteDrive.PowerManagementSupported
- Msvm_DisketteDrive.PowerManagementCapabilities
- Msvm_DisketteDrive.Availability
- Msvm_DisketteDrive.StatusInfo
- Msvm_DisketteDrive.LastErrorCode
- Msvm_DisketteDrive.ErrorDescription
- Msvm_DisketteDrive.ErrorCleared
- Msvm_DisketteDrive.OtherIdentifyingInfo
- Msvm_DisketteDrive.PowerOnHours
- Msvm_DisketteDrive.TotalPowerOnHours
- Msvm_DisketteDrive.IdentifyingDescriptions
- Msvm_DisketteDrive.AdditionalAvailability
- Msvm_DisketteDrive.MaxQuiesceTime
- Msvm_DisketteDrive.Capabilities
- Msvm_DisketteDrive.CapabilityDescriptions
- Msvm_DisketteDrive.ErrorMethodology
- Msvm_DisketteDrive.CompressionMethod
- Msvm_DisketteDrive.NumberOfMediaSupported
- Msvm_DisketteDrive.MaxMediaSize
- Msvm_DisketteDrive.DefaultBlockSize
- Msvm_DisketteDrive.MaxBlockSize
- Msvm_DisketteDrive.MinBlockSize
- Msvm_DisketteDrive.NeedsCleaning
- Msvm_DisketteDrive.MediaIsLocked
- Msvm_DisketteDrive.Security
- Msvm_DisketteDrive.LastCleaned
- Msvm_DisketteDrive.MaxAccessTime
- Msvm_DisketteDrive.UncompressedDataRate
- Msvm_DisketteDrive.LoadTime
- Msvm_DisketteDrive.UnloadTime
- Msvm_DisketteDrive.MountCount
- Msvm_DisketteDrive.TimeOfLastMount
- Msvm_DisketteDrive.TotalMountTime
- Msvm_DisketteDrive.UnitsDescription
- Msvm_DisketteDrive.MaxUnitsBeforeCleaning
- Msvm_DisketteDrive.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1dbc9e21626e2f5e8269fb3a398dd48a6ea442e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815230"
---
# <a name="msvm_diskettedrive-class"></a><span data-ttu-id="3b5ac-103">MSVM \_ DisketteDrive (clase)</span><span class="sxs-lookup"><span data-stu-id="3b5ac-103">Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="3b5ac-104">Representa una unidad de disquete dentro de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-104">Represents a floppy drive inside the virtual machine.</span></span> <span data-ttu-id="3b5ac-105">Una unidad de disquete se puede rellenar con un archivo que represente un disquete o la unidad puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-105">A floppy drive can be populated with a file representing floppy media or the drive can be empty.</span></span> <span data-ttu-id="3b5ac-106">No se admiten medios físicos.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-106">Physical media is not supported.</span></span> <span data-ttu-id="3b5ac-107">Hay exactamente una unidad de disquete por cada controlador de disquete y no es extraíble.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-107">There is exactly one floppy drive per floppy controller and it is not removable.</span></span>

<span data-ttu-id="3b5ac-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b5ac-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b5ac-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DisketteDrive : CIM_DisketteDrive
{
  string   InstanceID;
  string   Caption = "Diskette Drive";
  string   Description = "Microsoft Virtual Diskette Drive";
  string   ElementName = "Diskette Drive";
  datetime InstallDate;
  string   Name = "Diskette Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DisketteDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint16   Capabilities[] = {3, 4, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Writing", "Supports Removable Media"};
  string   ErrorMethodology = { "None" };
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 1440;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize = 512;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 18446744073709551615;
  uint64   UnitsUsed = 0;
};
```

## <a name="members"></a><span data-ttu-id="3b5ac-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3b5ac-110">Members</span></span>

<span data-ttu-id="3b5ac-111">La clase **MSVM \_ DisketteDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3b5ac-111">The **Msvm\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="3b5ac-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b5ac-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3b5ac-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b5ac-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3b5ac-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="3b5ac-114">Methods</span></span>

<span data-ttu-id="3b5ac-115">La clase **MSVM \_ DisketteDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-115">The **Msvm\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="3b5ac-116">Método</span><span class="sxs-lookup"><span data-stu-id="3b5ac-116">Method</span></span>                                                              | <span data-ttu-id="3b5ac-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b5ac-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="3b5ac-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="3b5ac-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-119">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="3b5ac-120">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-120">**LockMedia**</span></span>](msvm-diskettedrive-lockmedia.md)                   | <span data-ttu-id="3b5ac-121">Bloquea o libera los medios.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-121">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="3b5ac-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-122">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="3b5ac-123">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3b5ac-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-124">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="3b5ac-125">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="3b5ac-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-126">**RequestStateChange**</span></span>](msvm-diskettedrive-requeststatechange.md) | <span data-ttu-id="3b5ac-127">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="3b5ac-128">**Reset**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-128">**Reset**</span></span>](msvm-diskettedrive-reset.md)                           | <span data-ttu-id="3b5ac-129">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-129">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="3b5ac-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-130">**RestoreProperties**</span></span>                                               | <span data-ttu-id="3b5ac-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3b5ac-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-132">**SaveProperties**</span></span>                                                  | <span data-ttu-id="3b5ac-133">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3b5ac-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-134">**SetPowerState**</span></span>                                                   | <span data-ttu-id="3b5ac-135">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3b5ac-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3b5ac-136">Properties</span></span>

<span data-ttu-id="3b5ac-137">La clase **MSVM \_ DisketteDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-137">The **Msvm\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b5ac-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-139">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-141">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="3b5ac-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="3b5ac-143">Value</span><span class="sxs-lookup"><span data-stu-id="3b5ac-143">Value</span></span>                                                                        | <span data-ttu-id="3b5ac-144">Significado</span><span class="sxs-lookup"><span data-stu-id="3b5ac-144">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="3b5ac-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-145"><dt>6</dt></span></span> </dl> | <span data-ttu-id="3b5ac-146">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-146">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b5ac-147">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-147">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-148">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-150">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-150">The primary availability and status of the device.</span></span> <span data-ttu-id="3b5ac-151">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-151">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="3b5ac-152">Value</span><span class="sxs-lookup"><span data-stu-id="3b5ac-152">Value</span></span>                                                                        | <span data-ttu-id="3b5ac-153">Significado</span><span class="sxs-lookup"><span data-stu-id="3b5ac-153">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="3b5ac-154"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-154"><dt>6</dt></span></span> </dl> | <span data-ttu-id="3b5ac-155">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-155">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b5ac-156">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-156">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-157">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-159">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-159">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="3b5ac-160">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3b5ac-160">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="3b5ac-161">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-161">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="3b5ac-162">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-162">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="3b5ac-163">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-163">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-164">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-164">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-165">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-165">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-167">Las capacidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-167">The capabilities of the media access device.</span></span> <span data-ttu-id="3b5ac-168">Esta propiedad se hereda de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y se establece en los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="3b5ac-169">Value</span><span class="sxs-lookup"><span data-stu-id="3b5ac-169">Value</span></span>                                                                                | <span data-ttu-id="3b5ac-170">Significado</span><span class="sxs-lookup"><span data-stu-id="3b5ac-170">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3b5ac-171"><dt>{3, 4, 7}</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-171"><dt>{3, 4, 7}</dt></span></span> </dl> |                                                                                                 |
| <dl> <span data-ttu-id="3b5ac-172"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-172"><dt>3</dt></span></span> </dl>         | <span data-ttu-id="3b5ac-173">La entrada correspondiente en **CapabilityDescriptions** es "Random Access".</span><span class="sxs-lookup"><span data-stu-id="3b5ac-173">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>            |
| <dl> <span data-ttu-id="3b5ac-174"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-174"><dt>4</dt></span></span> </dl>         | <span data-ttu-id="3b5ac-175">La entrada correspondiente en **CapabilityDescriptions** es "supportly Writing".</span><span class="sxs-lookup"><span data-stu-id="3b5ac-175">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/>         |
| <dl> <span data-ttu-id="3b5ac-176"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-176"><dt>7</dt></span></span> </dl>         | <span data-ttu-id="3b5ac-177">La entrada correspondiente en **CapabilityDescriptions** es "Supported medios extraíbles".</span><span class="sxs-lookup"><span data-stu-id="3b5ac-177">The corresponding entry in **CapabilityDescriptions** is "Supports Removable Media".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b5ac-178">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-178">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-179">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-181">Matriz de cadenas de formato libre que proporciona explicaciones detalladas para las características del dispositivo de acceso indicadas en la matriz de propiedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="3b5ac-181">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="3b5ac-182">Cada entrada de esta matriz está relacionada con la entrada de la matriz de **funciones** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-182">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span> <span data-ttu-id="3b5ac-183">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-183">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-187">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-187">A short description of the object.</span></span> <span data-ttu-id="3b5ac-188">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-189">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-189">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-190">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-192">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-192">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3b5ac-193">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3b5ac-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-195">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-195">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-198">Cadena que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-198">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="3b5ac-199">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="3b5ac-199">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="3b5ac-200">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="3b5ac-200">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="3b5ac-201">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="3b5ac-201">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="3b5ac-202">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-202">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

<span data-ttu-id="3b5ac-203">"No comprimido"</span><span class="sxs-lookup"><span data-stu-id="3b5ac-203">"Not Compressed"</span></span>

<span data-ttu-id="3b5ac-204">Unknown</span><span class="sxs-lookup"><span data-stu-id="3b5ac-204">"Unknown"</span></span>

<span data-ttu-id="3b5ac-205">Comprimido</span><span class="sxs-lookup"><span data-stu-id="3b5ac-205">"Compressed"</span></span>

<span data-ttu-id="3b5ac-206">"No comprimido"</span><span class="sxs-lookup"><span data-stu-id="3b5ac-206">"Not Compressed"</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-210">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-210">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="3b5ac-211">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-211">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-212">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-212">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-213">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-215">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-215">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="3b5ac-216">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-216">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-217">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-217">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-220">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-220">A description of the object.</span></span> <span data-ttu-id="3b5ac-221">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-221">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-222">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-222">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-223">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-225">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-225">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3b5ac-226">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-226">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3b5ac-227">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-227">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-228">**ID**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-228">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-231">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en "Microsoft:*GUID* del \\ *dispositivo-datos específicos*".</span><span class="sxs-lookup"><span data-stu-id="3b5ac-231">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-232">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-232">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-235">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-235">A display name for the object.</span></span> <span data-ttu-id="3b5ac-236">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-236">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-237">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-237">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-238">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-240">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-240">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="3b5ac-241">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-241">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-242">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-242">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-245">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-245">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3b5ac-246">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-246">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="3b5ac-247">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-248">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-248">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-249">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-251">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-251">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="3b5ac-252">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-252">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-253">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-253">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-254">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-256">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-256">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="3b5ac-257">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-257">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-258">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-258">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-259">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-261">Cadena que describe los tipos de detección y corrección de errores admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-261">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="3b5ac-262">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-262">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-263">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-263">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-264">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-266">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-266">The current health of the element.</span></span> <span data-ttu-id="3b5ac-267">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-267">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="3b5ac-268">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-268">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="3b5ac-269">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-269">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-270">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-270">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-271">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-271">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-273">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="3b5ac-273">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="3b5ac-274">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-276">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-278">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-278">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="3b5ac-279">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-280">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-280">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-283">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-283">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-284">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-284">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3b5ac-285">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-285">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-286">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-286">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-287">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-287">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-289">Fecha y hora en que se limpió por última vez el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-289">The date and time on which the device was last cleaned.</span></span> <span data-ttu-id="3b5ac-290">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-290">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-291">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-291">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-292">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-294">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-294">The last error code reported by the logical device.</span></span> <span data-ttu-id="3b5ac-295">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-295">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-296">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-296">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-297">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-299">Tiempo, en milisegundos, desde la carga hasta la capacidad de leer o escribir un medio.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-299">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="3b5ac-300">Por ejemplo, en el caso de las unidades de disco, es el intervalo entre un disco que no gira hasta el disco que informa de que está listo para lectura y escritura (es decir, el disco gira a velocidades nominales).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-300">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="3b5ac-301">En el caso de las unidades de cinta, es el momento desde que se inserta un medio para informar de que está listo para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-301">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="3b5ac-302">Normalmente, se encuentra en el área de BOT de la cinta.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-302">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="3b5ac-303">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-303">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-304">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-304">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-305">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-306">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-307">Tiempo, en milisegundos, que se va a pasar de la primera ubicación del medio a la ubicación más lejana con respecto a la hora.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-307">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="3b5ac-308">En el caso de una unidad de disco, representa una búsqueda completa + un retraso de rotación completo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-308">For a disk drive, this represents full seek + full rotational delay.</span></span> <span data-ttu-id="3b5ac-309">En el caso de las unidades de cinta, representa una búsqueda desde el principio de la cinta hasta el punto más alejado físicamente.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-309">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="3b5ac-310">(El final de una cinta puede estar en su punto más lejano físicamente, pero esto no es necesariamente cierto). Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-310">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-311">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-311">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-312">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-312">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-314">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-314">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="3b5ac-315">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-315">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-316">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-316">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-317">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-317">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-319">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-319">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="3b5ac-320">Los kilobytes se interpretan como el número de bytes multiplicado por 1000 (no por el número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-320">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="3b5ac-321">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-321">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-322">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-322">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-323">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-325">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-325">This property has been deprecated.</span></span> <span data-ttu-id="3b5ac-326">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-327">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-327">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-328">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-328">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-330">Las unidades máximas que se pueden usar antes de que se limpie el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-330">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="3b5ac-331">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-331">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-332">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-332">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-333">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-335">**True** si el medio está bloqueado en el dispositivo y no se puede expulsar; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-335">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="3b5ac-336">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-336">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-337">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-337">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-338">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-338">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-339">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-340">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-340">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="3b5ac-341">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-341">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-342">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-342">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-343">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-343">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-345">En el caso de un dispositivo que admita medios extraíbles, el número de veces que los medios se han montado para la transferencia de datos o para limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-345">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="3b5ac-346">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no es aplicable y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-346">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="3b5ac-347">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-347">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-348">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-348">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-351">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-351">The label by which the object is known.</span></span> <span data-ttu-id="3b5ac-352">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="3b5ac-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-353">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-353">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-354">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-355">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-356">**True** si el dispositivo de acceso a medios necesita limpieza; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-356">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="3b5ac-357">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-357">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-358">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-358">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-359">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-359">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-360">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-361">Número máximo de medios individuales que se pueden admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-361">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="3b5ac-362">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-362">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-364">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-365">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-366">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3b5ac-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3b5ac-367">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3b5ac-368">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-370">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-371">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-372">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-372">The current statuses of the object.</span></span> <span data-ttu-id="3b5ac-373">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-374">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-374">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-375">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-377">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-377">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3b5ac-378">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-378">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="3b5ac-379">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-380">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-380">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-381">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-381">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-382">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-383">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-383">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="3b5ac-384">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-385">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-385">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-386">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-386">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-387">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-388">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-388">The power management capabilities of the device.</span></span> <span data-ttu-id="3b5ac-389">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-390">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-390">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-391">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-391">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-392">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-393">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-393">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="3b5ac-394">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-395">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-395">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-396">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-396">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-398">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-398">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="3b5ac-399">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-399">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-400">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-400">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-401">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-403">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-403">Provides high level status information.</span></span> <span data-ttu-id="3b5ac-404">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-404">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="3b5ac-405">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-405">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3b5ac-406">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-407">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-407">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-408">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-410">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-410">The last requested or desired state for the element.</span></span> <span data-ttu-id="3b5ac-411">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-411">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="3b5ac-412">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-412">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="3b5ac-413">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no ser compatible con **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-413">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="3b5ac-414">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-414">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="3b5ac-415">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-415">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-416">**Seguridad**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-416">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-417">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-419">La seguridad operativa definida para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-419">The operational security defined for the device.</span></span> <span data-ttu-id="3b5ac-420">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-420">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>



| <span data-ttu-id="3b5ac-421">Value</span><span class="sxs-lookup"><span data-stu-id="3b5ac-421">Value</span></span>                                                                        | <span data-ttu-id="3b5ac-422">Significado</span><span class="sxs-lookup"><span data-stu-id="3b5ac-422">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="3b5ac-423"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-423"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3b5ac-424">None</span><span class="sxs-lookup"><span data-stu-id="3b5ac-424">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b5ac-425">**Estado**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-425">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-426">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-427">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-428">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-428">The current status of the object.</span></span> <span data-ttu-id="3b5ac-429">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-430">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-430">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-431">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-431">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-433">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3b5ac-433">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3b5ac-434">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="3b5ac-434">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-436">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-438">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-438">The current state of the logical device.</span></span> <span data-ttu-id="3b5ac-439">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-440">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-440">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-441">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-441">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-443">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-443">The scoping system's creation class name.</span></span> <span data-ttu-id="3b5ac-444">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-445">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-445">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-446">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-446">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-448">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-448">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="3b5ac-449">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-450">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-450">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-451">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-451">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-453">Para un dispositivo que admita medios extraíbles, la fecha y la hora más recientes en que se montó el medio en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-453">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="3b5ac-454">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no tiene ningún significado y no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-454">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="3b5ac-455">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-455">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-456">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-456">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-457">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-459">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-459">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3b5ac-460">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-460">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-461">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-461">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-462">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-463">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-464">En el caso de un dispositivo que admita medios extraíbles, el tiempo total (en segundos) que los medios se han montado para la transferencia de datos o para limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-464">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="3b5ac-465">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no es aplicable y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-465">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="3b5ac-466">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-466">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-467">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-467">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-468">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-468">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-470">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-470">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="3b5ac-471">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-471">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-472">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-472">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-473">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-473">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-474">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-475">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-475">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3b5ac-476">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-476">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-477">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-477">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-478">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-478">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-479">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-480">La velocidad de transferencia de datos sostenida, en KB/s, que el dispositivo puede leer y escribir en un medio.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-480">The sustained data transfer rate, in KB/sec, that the device can read from and write to a media.</span></span> <span data-ttu-id="3b5ac-481">Se trata de una velocidad de datos sin procesar y sostenida.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-481">This is a sustained, raw data rate.</span></span> <span data-ttu-id="3b5ac-482">Las tarifas máximas o tarifas suponiendo que no se debería informar de la compresión en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-482">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="3b5ac-483">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-483">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-484">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-484">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-485">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-486">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-487">Unidades relativas a su uso en **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-487">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="3b5ac-488">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-488">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-489">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-489">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-490">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-490">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-491">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-492">Número actual de unidades utilizadas.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-492">The current number of units used.</span></span> <span data-ttu-id="3b5ac-493">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-493">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="3b5ac-494">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-494">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b5ac-495">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-495">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3b5ac-496">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3b5ac-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b5ac-497">Tiempo, en milisegundos, desde que se puede leer o escribir un elemento multimedia en su ' Unload '.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-497">The time, in milliseconds, from being able to read or write a media to its 'unload'.</span></span> <span data-ttu-id="3b5ac-498">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-498">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b5ac-499">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b5ac-499">Remarks</span></span>

<span data-ttu-id="3b5ac-500">El acceso a la clase **MSVM \_ DisketteDrive** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="3b5ac-500">Access to the **Msvm\_DisketteDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3b5ac-501">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3b5ac-501">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5ac-502">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b5ac-502">Requirements</span></span>



| <span data-ttu-id="3b5ac-503">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b5ac-503">Requirement</span></span> | <span data-ttu-id="3b5ac-504">Value</span><span class="sxs-lookup"><span data-stu-id="3b5ac-504">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b5ac-505">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b5ac-505">Minimum supported client</span></span><br/> | <span data-ttu-id="3b5ac-506">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b5ac-506">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3b5ac-507">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b5ac-507">Minimum supported server</span></span><br/> | <span data-ttu-id="3b5ac-508">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b5ac-508">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b5ac-509">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3b5ac-509">Namespace</span></span><br/>                | <span data-ttu-id="3b5ac-510">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3b5ac-510">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3b5ac-511">MOF</span><span class="sxs-lookup"><span data-stu-id="3b5ac-511">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b5ac-512"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-512"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b5ac-513">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b5ac-513">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b5ac-514"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b5ac-514"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3b5ac-515">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b5ac-515">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b5ac-516">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-516">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="3b5ac-517">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="3b5ac-517">**CIM\_DisketteDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskettedrive)
</dt> <dt>

[<span data-ttu-id="3b5ac-518">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="3b5ac-518">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

