---
description: Representa la memoria asignada actualmente a una máquina virtual.
ms.assetid: 4CAA64FC-5A06-409B-9E92-32DF3F47D5FD
title: Clase Msvm_Memory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Memory
- Msvm_Memory.SetPowerState
- Msvm_Memory.EnableDevice
- Msvm_Memory.OnlineDevice
- Msvm_Memory.QuiesceDevice
- Msvm_Memory.SaveProperties
- Msvm_Memory.RestoreProperties
- Msvm_Memory.InstanceID
- Msvm_Memory.Caption
- Msvm_Memory.Description
- Msvm_Memory.ElementName
- Msvm_Memory.InstallDate
- Msvm_Memory.OperationalStatus
- Msvm_Memory.StatusDescriptions
- Msvm_Memory.Status
- Msvm_Memory.HealthState
- Msvm_Memory.CommunicationStatus
- Msvm_Memory.DetailedStatus
- Msvm_Memory.OperatingStatus
- Msvm_Memory.PrimaryStatus
- Msvm_Memory.EnabledState
- Msvm_Memory.OtherEnabledState
- Msvm_Memory.RequestedState
- Msvm_Memory.EnabledDefault
- Msvm_Memory.TimeOfLastStateChange
- Msvm_Memory.AvailableRequestedStates
- Msvm_Memory.TransitioningToState
- Msvm_Memory.SystemCreationClassName
- Msvm_Memory.SystemName
- Msvm_Memory.CreationClassName
- Msvm_Memory.DeviceID
- Msvm_Memory.PowerManagementSupported
- Msvm_Memory.PowerManagementCapabilities
- Msvm_Memory.Availability
- Msvm_Memory.StatusInfo
- Msvm_Memory.LastErrorCode
- Msvm_Memory.ErrorDescription
- Msvm_Memory.ErrorCleared
- Msvm_Memory.OtherIdentifyingInfo
- Msvm_Memory.PowerOnHours
- Msvm_Memory.TotalPowerOnHours
- Msvm_Memory.IdentifyingDescriptions
- Msvm_Memory.AdditionalAvailability
- Msvm_Memory.MaxQuiesceTime
- Msvm_Memory.DataOrganization
- Msvm_Memory.Purpose
- Msvm_Memory.Access
- Msvm_Memory.BlockSize
- Msvm_Memory.NumberOfBlocks
- Msvm_Memory.ConsumableBlocks
- Msvm_Memory.IsBasedOnUnderlyingRedundancy
- Msvm_Memory.SequentialAccess
- Msvm_Memory.ExtentStatus
- Msvm_Memory.NoSinglePointOfFailure
- Msvm_Memory.DataRedundancy
- Msvm_Memory.PackageRedundancy
- Msvm_Memory.DeltaReservation
- Msvm_Memory.Primordial
- Msvm_Memory.Name
- Msvm_Memory.NameFormat
- Msvm_Memory.NameNamespace
- Msvm_Memory.OtherNameNamespace
- Msvm_Memory.OtherNameFormat
- Msvm_Memory.Volatile
- Msvm_Memory.ErrorMethodology
- Msvm_Memory.StartingAddress
- Msvm_Memory.EndingAddress
- Msvm_Memory.ErrorInfo
- Msvm_Memory.OtherErrorDescription
- Msvm_Memory.CorrectableError
- Msvm_Memory.ErrorTime
- Msvm_Memory.ErrorAccess
- Msvm_Memory.ErrorTransferSize
- Msvm_Memory.ErrorData
- Msvm_Memory.ErrorDataOrder
- Msvm_Memory.ErrorAddress
- Msvm_Memory.SystemLevelAddress
- Msvm_Memory.ErrorResolution
- Msvm_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ec6b287f3281fd0224e9c2efc39391781bd7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913129"
---
# <a name="msvm_memory-class"></a><span data-ttu-id="93bc1-103">\_Clase de memoria MSVM</span><span class="sxs-lookup"><span data-stu-id="93bc1-103">Msvm\_Memory class</span></span>

<span data-ttu-id="93bc1-104">Representa la memoria asignada actualmente a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93bc1-104">Represents the memory currently allocated to a virtual machine.</span></span>

<span data-ttu-id="93bc1-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="93bc1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bc1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93bc1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Memory : CIM_Memory
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose = "System Memory";
  uint16   Access = 3;
  uint64   BlockSize = 1048576;
  uint64   NumberOfBlocks;
  uint64   ConsumableBlocks;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = 2;
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 1;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial;
  string   Name = "GUID";
  uint16   NameFormat = 0;
  uint16   NameNamespace = 0;
  string   OtherNameNamespace;
  string   OtherNameFormat;
  boolean  Volatile = True;
  string   ErrorMethodology;
  uint64   StartingAddress = 0;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a><span data-ttu-id="93bc1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="93bc1-107">Members</span></span>

<span data-ttu-id="93bc1-108">La clase de **\_ memoria MSVM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="93bc1-108">The **Msvm\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="93bc1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="93bc1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="93bc1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93bc1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="93bc1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="93bc1-111">Methods</span></span>

<span data-ttu-id="93bc1-112">La clase de **\_ memoria MSVM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="93bc1-112">The **Msvm\_Memory** class has these methods.</span></span>



| <span data-ttu-id="93bc1-113">Método</span><span class="sxs-lookup"><span data-stu-id="93bc1-113">Method</span></span>                                                       | <span data-ttu-id="93bc1-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="93bc1-114">Description</span></span>                              |
|:-------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="93bc1-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="93bc1-115">**EnableDevice**</span></span>                                             | <span data-ttu-id="93bc1-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="93bc1-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93bc1-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="93bc1-117">**OnlineDevice**</span></span>                                             | <span data-ttu-id="93bc1-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="93bc1-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93bc1-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="93bc1-119">**QuiesceDevice**</span></span>                                            | <span data-ttu-id="93bc1-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="93bc1-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="93bc1-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="93bc1-121">**RequestStateChange**</span></span>](msvm-memory-requeststatechange.md) | <span data-ttu-id="93bc1-122">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="93bc1-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="93bc1-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="93bc1-123">**Reset**</span></span>](msvm-memory-reset.md)                           | <span data-ttu-id="93bc1-124">Restablece la memoria virtual.</span><span class="sxs-lookup"><span data-stu-id="93bc1-124">Resets the virtual memory.</span></span><br/>    |
| <span data-ttu-id="93bc1-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="93bc1-125">**RestoreProperties**</span></span>                                        | <span data-ttu-id="93bc1-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="93bc1-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93bc1-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="93bc1-127">**SaveProperties**</span></span>                                           | <span data-ttu-id="93bc1-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="93bc1-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="93bc1-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="93bc1-129">**SetPowerState**</span></span>                                            | <span data-ttu-id="93bc1-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="93bc1-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="93bc1-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93bc1-131">Properties</span></span>

<span data-ttu-id="93bc1-132">La clase de **\_ memoria MSVM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="93bc1-132">The **Msvm\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93bc1-133">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="93bc1-133">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-134">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-136">Describe las propiedades de lectura y escritura del medio.</span><span class="sxs-lookup"><span data-stu-id="93bc1-136">Describes the read/write properties of the media.</span></span> <span data-ttu-id="93bc1-137">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y está establecida en 3 (compatible con lectura y escritura) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="93bc1-137">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to 3 (Read/Write Supported) by default.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="93bc1-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-139">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-141">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="93bc1-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-142">**AdditionalErrorData**</span><span class="sxs-lookup"><span data-stu-id="93bc1-142">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-143">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="93bc1-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-145">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-145">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-146">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="93bc1-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-147">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-149">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="93bc1-149">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-150">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="93bc1-150">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-151">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-151">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-153">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="93bc1-153">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="93bc1-154">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93bc1-154">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-155">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="93bc1-155">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-156">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-158">Tamaño, en bytes, de los bloques que forman la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-158">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="93bc1-159">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="93bc1-159">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="93bc1-160">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), escriba 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="93bc1-160">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span> <span data-ttu-id="93bc1-161">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre se establece en 1048576.</span><span class="sxs-lookup"><span data-stu-id="93bc1-161">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1048576.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-162">**Caption**</span><span class="sxs-lookup"><span data-stu-id="93bc1-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-165">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="93bc1-165">A short description of the object.</span></span> <span data-ttu-id="93bc1-166">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="93bc1-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-170">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="93bc1-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="93bc1-171">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="93bc1-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="93bc1-172">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="93bc1-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="93bc1-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="93bc1-174"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="93bc1-175"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="93bc1-176"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="93bc1-177"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="93bc1-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="93bc1-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="93bc1-180">)</span><span class="sxs-lookup"><span data-stu-id="93bc1-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93bc1-181">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="93bc1-181">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-182">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-184">Número máximo de bloques, de tamaño de **bloqueos**, que están disponibles para el consumo al encapar las extensiones de almacenamiento mediante la Asociación BasedOn.</span><span class="sxs-lookup"><span data-stu-id="93bc1-184">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the BasedOn association.</span></span> <span data-ttu-id="93bc1-185">Esta propiedad se hereda de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-185">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-186">**CorrectableError**</span><span class="sxs-lookup"><span data-stu-id="93bc1-186">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-187">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-189">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-189">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-190">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93bc1-190">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-191">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-193">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="93bc1-193">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="93bc1-194">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="93bc1-194">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-195">**Organización de los mismos**</span><span class="sxs-lookup"><span data-stu-id="93bc1-195">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-198">El tipo de organización de datos que se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-198">The type of data organization used.</span></span> <span data-ttu-id="93bc1-199">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en 2.</span><span class="sxs-lookup"><span data-stu-id="93bc1-199">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-200">**Redundancia de los mismos**</span><span class="sxs-lookup"><span data-stu-id="93bc1-200">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-201">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-203">El número de copias completas de los datos que se mantienen actualmente.</span><span class="sxs-lookup"><span data-stu-id="93bc1-203">The number of complete copies of data that is currently maintained.</span></span> <span data-ttu-id="93bc1-204">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="93bc1-204">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-205">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="93bc1-205">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-206">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="93bc1-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-208">Valor actual para la reserva Delta.</span><span class="sxs-lookup"><span data-stu-id="93bc1-208">The current value for delta reservation.</span></span> <span data-ttu-id="93bc1-209">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="93bc1-209">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-210">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="93bc1-210">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-213">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="93bc1-213">A description of the object.</span></span> <span data-ttu-id="93bc1-214">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-214">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-215">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="93bc1-215">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-216">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-218">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="93bc1-218">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="93bc1-219">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="93bc1-219">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="93bc1-220">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="93bc1-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="93bc1-221"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="93bc1-222"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="93bc1-223"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="93bc1-224"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="93bc1-225"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="93bc1-226"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="93bc1-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="93bc1-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="93bc1-229">)</span><span class="sxs-lookup"><span data-stu-id="93bc1-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93bc1-230">**ID**</span><span class="sxs-lookup"><span data-stu-id="93bc1-230">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-231">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-233">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="93bc1-233">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="93bc1-234">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="93bc1-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="93bc1-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-238">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="93bc1-238">A display name for the object.</span></span> <span data-ttu-id="93bc1-239">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="93bc1-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-241">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-243">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="93bc1-244">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93bc1-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="93bc1-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-246">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-248">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="93bc1-249">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="93bc1-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="93bc1-250">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93bc1-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="93bc1-251">Value</span><span class="sxs-lookup"><span data-stu-id="93bc1-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="93bc1-252">Significado</span><span class="sxs-lookup"><span data-stu-id="93bc1-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="93bc1-253"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="93bc1-254">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="93bc1-255"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="93bc1-256"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="93bc1-257">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="93bc1-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="93bc1-258"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="93bc1-259">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="93bc1-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="93bc1-260"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="93bc1-261">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="93bc1-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="93bc1-262"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="93bc1-263">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="93bc1-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="93bc1-264"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="93bc1-265">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="93bc1-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="93bc1-266"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="93bc1-267">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="93bc1-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="93bc1-268"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="93bc1-269">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="93bc1-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="93bc1-270">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="93bc1-271">El elemento está habilitado, pero está en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="93bc1-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="93bc1-272">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="93bc1-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="93bc1-273">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="93bc1-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="93bc1-274"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="93bc1-275">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="93bc1-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="93bc1-276">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="93bc1-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="93bc1-277">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="93bc1-277">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-278">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-278">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-280">Dirección final del bloque de memoria contiguo.</span><span class="sxs-lookup"><span data-stu-id="93bc1-280">The ending address of the contiguous memory block.</span></span> <span data-ttu-id="93bc1-281">Dado que la propiedad **StartingAddress** siempre es 0, este valor siempre refleja la cantidad total de memoria de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93bc1-281">Since the **StartingAddress** property is always 0, this value always reflects the total amount of memory in the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-282">**ErrorAccess**</span><span class="sxs-lookup"><span data-stu-id="93bc1-282">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-283">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-285">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-285">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-286">**ErrorAddress**</span><span class="sxs-lookup"><span data-stu-id="93bc1-286">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-287">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-287">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-289">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-289">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-290">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="93bc1-290">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-291">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-293">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-293">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-294">**Datoserror**</span><span class="sxs-lookup"><span data-stu-id="93bc1-294">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-295">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="93bc1-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-297">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-297">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-298">**ErrorDataOrder**</span><span class="sxs-lookup"><span data-stu-id="93bc1-298">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-299">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-301">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-301">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="93bc1-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-305">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-305">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-306">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="93bc1-306">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-307">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-309">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-309">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-310">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="93bc1-310">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-311">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-312">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-313">Cadena que describe el tipo de detección y corrección de errores admitidos por esta extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-313">A string that describes the type of error detection and correction supported by this storage extent.</span></span> <span data-ttu-id="93bc1-314">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-314">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-315">**ErrorResolution**</span><span class="sxs-lookup"><span data-stu-id="93bc1-315">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-316">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-318">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-318">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-319">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="93bc1-319">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-320">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93bc1-320">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-322">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory) pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-322">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory) but it not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-323">**ErrorTransferSize**</span><span class="sxs-lookup"><span data-stu-id="93bc1-323">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-324">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bc1-324">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-326">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-326">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-327">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="93bc1-327">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-328">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-328">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-329">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-330">Las extensiones de almacenamiento tienen información de estado adicional más allá de la capturada en **OperationalStatus** y otras propiedades heredadas del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-330">Storage extents have additional status information beyond that captured in the **OperationalStatus** and other properties inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="93bc1-331">Esta información adicional (por ejemplo, "protección deshabilitada", valor = 9) se captura en la propiedad **VolumeStatus** .</span><span class="sxs-lookup"><span data-stu-id="93bc1-331">This additional information (for example, "Protection Disabled", value=9) is captured in the **VolumeStatus** property.</span></span> <span data-ttu-id="93bc1-332">Esta propiedad se hereda de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en 2 (ninguna/no aplicable).</span><span class="sxs-lookup"><span data-stu-id="93bc1-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 2 (None/Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-333">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="93bc1-333">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-334">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-335">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-336">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-336">The current health of the element.</span></span> <span data-ttu-id="93bc1-337">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="93bc1-337">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="93bc1-338">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="93bc1-338">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="93bc1-339">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="93bc1-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-340">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="93bc1-340">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-341">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="93bc1-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-343">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-344">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="93bc1-344">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-345">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93bc1-345">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-347">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93bc1-347">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="93bc1-348">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-349">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93bc1-349">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-350">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-352">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="93bc1-352">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-353">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="93bc1-353">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="93bc1-354">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-354">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-355">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="93bc1-355">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-356">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-358">**True** si las extensiones de almacenamiento subyacentes participan en un grupo de redundancia de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-358">**True** if the underlying storage extents participate in a Storage Redundancy Group.</span></span> <span data-ttu-id="93bc1-359">Esta propiedad se hereda de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-359">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-360">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="93bc1-360">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-361">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93bc1-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-363">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-364">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="93bc1-364">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-365">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-365">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-367">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-367">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-368">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="93bc1-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-369">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-371">Calificadores: **MaxLen** (1024), **invalidación** ("nombre")</span><span class="sxs-lookup"><span data-stu-id="93bc1-371">Qualifiers: **MaxLen** (1024), **Override** ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-372">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="93bc1-372">The label by which the object is known.</span></span> <span data-ttu-id="93bc1-373">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="93bc1-373">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="93bc1-374">Esta propiedad se hereda de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="93bc1-374">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-375">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="93bc1-375">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-376">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-378">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="93bc1-378">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-379">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="93bc1-379">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-380">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-382">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="93bc1-382">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-383">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="93bc1-383">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-384">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-386">**True** si no existe ningún punto único de error.</span><span class="sxs-lookup"><span data-stu-id="93bc1-386">**True** if there exists no single point of failure.</span></span> <span data-ttu-id="93bc1-387">Esta propiedad se hereda de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-387">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-388">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="93bc1-388">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-389">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-391">Un valor calculado que representa la cantidad total de memoria dividida por el **bloque**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-391">A calculated value that represents the total amount of memory divided by the **BlockSize**.</span></span> <span data-ttu-id="93bc1-392">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="93bc1-392">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-393">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="93bc1-393">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-394">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-396">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="93bc1-396">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="93bc1-397">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="93bc1-397">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="93bc1-398">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-398">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="93bc1-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="93bc1-399"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="93bc1-400"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="93bc1-401"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="93bc1-402"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="93bc1-403"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="93bc1-404"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="93bc1-405"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="93bc1-406"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="93bc1-407"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="93bc1-408"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="93bc1-409"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="93bc1-410"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="93bc1-411"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="93bc1-412"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="93bc1-413"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="93bc1-414"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="93bc1-415"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="93bc1-416"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="93bc1-417"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="93bc1-418">)</span><span class="sxs-lookup"><span data-stu-id="93bc1-418">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93bc1-419">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="93bc1-419">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-420">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-420">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-422">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="93bc1-422">The current statuses of the object.</span></span> <span data-ttu-id="93bc1-423">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-424">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="93bc1-424">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-425">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-427">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="93bc1-427">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="93bc1-428">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="93bc1-428">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="93bc1-429">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-429">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-430">**OtherErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="93bc1-430">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-431">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-431">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-432">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-433">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-433">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-434">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="93bc1-434">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-435">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="93bc1-435">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-437">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-438">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="93bc1-438">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-439">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-440">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-441">El espacio de nombres de la propiedad **Name** cuando la propiedad **NameFormat** incluye el valor 1 (Other).</span><span class="sxs-lookup"><span data-stu-id="93bc1-441">The namespace of the **Name** property when the **NameFormat** property includes the value 1 (Other").</span></span> <span data-ttu-id="93bc1-442">Esta propiedad se hereda de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-442">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-443">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="93bc1-443">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-444">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-445">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-446">El espacio de nombres de la propiedad **Name** cuando la propiedad **NameNamespace** incluye el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="93bc1-446">The namespace of the **Name** property when the **NameNamespace** property includes the value 1 (Other).</span></span> <span data-ttu-id="93bc1-447">Esta propiedad se hereda de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-447">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-448">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="93bc1-448">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-449">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-451">El número de paquetes físicos que pueden fallar actualmente sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="93bc1-451">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="93bc1-452">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="93bc1-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-453">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="93bc1-453">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-454">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-454">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-456">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-456">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-457">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="93bc1-457">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-458">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-459">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-460">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-460">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-461">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="93bc1-461">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-462">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-462">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-463">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-464">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-464">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-465">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="93bc1-465">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-466">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-466">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-467">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-468">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="93bc1-468">Provides high level status information.</span></span> <span data-ttu-id="93bc1-469">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="93bc1-469">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="93bc1-470">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="93bc1-470">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="93bc1-471">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="93bc1-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="93bc1-472"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-473"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="93bc1-473"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="93bc1-474"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="93bc1-475"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="93bc1-476"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="93bc1-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="93bc1-478">)</span><span class="sxs-lookup"><span data-stu-id="93bc1-478">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93bc1-479">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="93bc1-479">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-480">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-480">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-481">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-482">**True** si el sistema que lo contiene no tiene la capacidad de crear o eliminar este elemento operativo.</span><span class="sxs-lookup"><span data-stu-id="93bc1-482">**True** if the containing system does not have the ability to create or delete this operational element.</span></span> <span data-ttu-id="93bc1-483">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="93bc1-483">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-484">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="93bc1-484">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-485">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-486">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-487">Cadena que describe el medio y su uso.</span><span class="sxs-lookup"><span data-stu-id="93bc1-487">A string that describes the media and its use.</span></span> <span data-ttu-id="93bc1-488">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre se establece en "memoria del sistema".</span><span class="sxs-lookup"><span data-stu-id="93bc1-488">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to "System Memory".</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-489">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="93bc1-489">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-490">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-490">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-491">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-491">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-492">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-492">The last requested or desired state for the element.</span></span> <span data-ttu-id="93bc1-493">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-493">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="93bc1-494">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="93bc1-494">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="93bc1-495">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="93bc1-495">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="93bc1-496">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="93bc1-496">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="93bc1-497">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-497">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-498">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="93bc1-498">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-499">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-499">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-500">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-501">**True** si un dispositivo de acceso multimedia tiene acceso de forma secuencial al almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-501">**True** if the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="93bc1-502">Una partición de cinta es un ejemplo de una extensión de almacenamiento de acceso secuencial.</span><span class="sxs-lookup"><span data-stu-id="93bc1-502">A tape partition is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="93bc1-503">Los volúmenes de almacenamiento, las particiones de disco y los discos lógicos representan extensiones de acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="93bc1-503">Storage volumes, disk partitions, and logical disks represent randomly accessed extents.</span></span> <span data-ttu-id="93bc1-504">Esta propiedad se hereda de [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)y siempre está establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-504">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is always set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-505">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="93bc1-505">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-506">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-506">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-507">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-508">Dirección inicial a la que hace referencia una aplicación o un sistema operativo y asignada por un controlador de memoria para este objeto de memoria.</span><span class="sxs-lookup"><span data-stu-id="93bc1-508">The beginning address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="93bc1-509">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="93bc1-509">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-510">**Estado**</span><span class="sxs-lookup"><span data-stu-id="93bc1-510">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-511">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-512">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-512">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-513">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-513">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-514">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="93bc1-514">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-515">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="93bc1-515">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-516">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-517">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="93bc1-517">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="93bc1-518">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93bc1-518">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-519">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="93bc1-519">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-520">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-521">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-522">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-522">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-523">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93bc1-523">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-524">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-524">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-525">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-526">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="93bc1-526">The scoping system's creation class name.</span></span> <span data-ttu-id="93bc1-527">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="93bc1-527">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-528">**SystemLevelAddress**</span><span class="sxs-lookup"><span data-stu-id="93bc1-528">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-529">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-530">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-531">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-531">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-532">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="93bc1-532">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-533">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="93bc1-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-534">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-535">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="93bc1-535">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="93bc1-536">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="93bc1-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-537">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="93bc1-537">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-538">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93bc1-538">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-539">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-540">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="93bc1-540">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="93bc1-541">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en "null".</span><span class="sxs-lookup"><span data-stu-id="93bc1-541">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-542">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="93bc1-542">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-543">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="93bc1-543">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-544">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-545">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="93bc1-545">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-546">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="93bc1-546">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-547">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93bc1-547">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-548">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-549">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="93bc1-549">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="93bc1-550">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="93bc1-550">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="93bc1-551">**Volatil**</span><span class="sxs-lookup"><span data-stu-id="93bc1-551">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93bc1-552">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="93bc1-552">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93bc1-553">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93bc1-553">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93bc1-554">Indica si la memoria es volátil.</span><span class="sxs-lookup"><span data-stu-id="93bc1-554">Indicates whether memory is volatile.</span></span> <span data-ttu-id="93bc1-555">Esta propiedad se hereda de [**la \_ memoria CIM**](/windows/desktop/CIMWin32Prov/cim-memory)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="93bc1-555">This property is inherited from [**CIM\_Memory**](/windows/desktop/CIMWin32Prov/cim-memory), and it is always set to **True**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93bc1-556">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93bc1-556">Remarks</span></span>

<span data-ttu-id="93bc1-557">El acceso a la clase de **\_ memoria MSVM** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="93bc1-557">Access to the **Msvm\_Memory** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="93bc1-558">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="93bc1-558">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="93bc1-559">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93bc1-559">Requirements</span></span>



| <span data-ttu-id="93bc1-560">Requisito</span><span class="sxs-lookup"><span data-stu-id="93bc1-560">Requirement</span></span> | <span data-ttu-id="93bc1-561">Value</span><span class="sxs-lookup"><span data-stu-id="93bc1-561">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93bc1-562">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93bc1-562">Minimum supported client</span></span><br/> | <span data-ttu-id="93bc1-563">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="93bc1-563">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93bc1-564">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93bc1-564">Minimum supported server</span></span><br/> | <span data-ttu-id="93bc1-565">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="93bc1-565">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93bc1-566">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93bc1-566">Namespace</span></span><br/>                | <span data-ttu-id="93bc1-567">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="93bc1-567">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93bc1-568">MOF</span><span class="sxs-lookup"><span data-stu-id="93bc1-568">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93bc1-569"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-569"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93bc1-570">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93bc1-570">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93bc1-571"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93bc1-571"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93bc1-572">Vea también</span><span class="sxs-lookup"><span data-stu-id="93bc1-572">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bc1-573">**Memoria de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="93bc1-573">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dt>

[<span data-ttu-id="93bc1-574">**Memoria de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="93bc1-574">**CIM\_Memory**</span></span>](/windows/desktop/CIMWin32Prov/cim-memory)
</dt> <dt>

[<span data-ttu-id="93bc1-575">Clases de memoria</span><span class="sxs-lookup"><span data-stu-id="93bc1-575">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

