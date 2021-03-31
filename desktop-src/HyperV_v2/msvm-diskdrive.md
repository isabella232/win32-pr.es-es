---
description: Representa una unidad de disco duro dentro de una máquina virtual.
ms.assetid: BF03CD02-7CDE-45E2-84D1-EC8E4457094A
title: Clase Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive
- Msvm_DiskDrive.SetPowerState
- Msvm_DiskDrive.EnableDevice
- Msvm_DiskDrive.OnlineDevice
- Msvm_DiskDrive.QuiesceDevice
- Msvm_DiskDrive.SaveProperties
- Msvm_DiskDrive.RestoreProperties
- Msvm_DiskDrive.InstanceID
- Msvm_DiskDrive.Caption
- Msvm_DiskDrive.Description
- Msvm_DiskDrive.ElementName
- Msvm_DiskDrive.InstallDate
- Msvm_DiskDrive.Name
- Msvm_DiskDrive.OperationalStatus
- Msvm_DiskDrive.StatusDescriptions
- Msvm_DiskDrive.Status
- Msvm_DiskDrive.HealthState
- Msvm_DiskDrive.CommunicationStatus
- Msvm_DiskDrive.DetailedStatus
- Msvm_DiskDrive.OperatingStatus
- Msvm_DiskDrive.PrimaryStatus
- Msvm_DiskDrive.EnabledState
- Msvm_DiskDrive.OtherEnabledState
- Msvm_DiskDrive.RequestedState
- Msvm_DiskDrive.EnabledDefault
- Msvm_DiskDrive.TimeOfLastStateChange
- Msvm_DiskDrive.AvailableRequestedStates
- Msvm_DiskDrive.TransitioningToState
- Msvm_DiskDrive.SystemCreationClassName
- Msvm_DiskDrive.SystemName
- Msvm_DiskDrive.CreationClassName
- Msvm_DiskDrive.DeviceID
- Msvm_DiskDrive.PowerManagementSupported
- Msvm_DiskDrive.PowerManagementCapabilities
- Msvm_DiskDrive.Availability
- Msvm_DiskDrive.StatusInfo
- Msvm_DiskDrive.LastErrorCode
- Msvm_DiskDrive.ErrorDescription
- Msvm_DiskDrive.ErrorCleared
- Msvm_DiskDrive.OtherIdentifyingInfo
- Msvm_DiskDrive.PowerOnHours
- Msvm_DiskDrive.TotalPowerOnHours
- Msvm_DiskDrive.IdentifyingDescriptions
- Msvm_DiskDrive.AdditionalAvailability
- Msvm_DiskDrive.MaxQuiesceTime
- Msvm_DiskDrive.Capabilities
- Msvm_DiskDrive.CapabilityDescriptions
- Msvm_DiskDrive.ErrorMethodology
- Msvm_DiskDrive.CompressionMethod
- Msvm_DiskDrive.NumberOfMediaSupported
- Msvm_DiskDrive.MaxMediaSize
- Msvm_DiskDrive.DefaultBlockSize
- Msvm_DiskDrive.MaxBlockSize
- Msvm_DiskDrive.MinBlockSize
- Msvm_DiskDrive.NeedsCleaning
- Msvm_DiskDrive.MediaIsLocked
- Msvm_DiskDrive.Security
- Msvm_DiskDrive.LastCleaned
- Msvm_DiskDrive.MaxAccessTime
- Msvm_DiskDrive.UncompressedDataRate
- Msvm_DiskDrive.LoadTime
- Msvm_DiskDrive.UnloadTime
- Msvm_DiskDrive.MountCount
- Msvm_DiskDrive.TimeOfLastMount
- Msvm_DiskDrive.TotalMountTime
- Msvm_DiskDrive.UnitsDescription
- Msvm_DiskDrive.MaxUnitsBeforeCleaning
- Msvm_DiskDrive.UnitsUsed
- Msvm_DiskDrive.DriveNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 60a08a2b73149285ddf3b0edf0003e5490b1c5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912577"
---
# <a name="msvm_diskdrive-class"></a><span data-ttu-id="8b3d2-103">MSVM \_ DiskDrive (clase)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-103">Msvm\_DiskDrive class</span></span>

<span data-ttu-id="8b3d2-104">Representa una unidad de disco duro dentro de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-104">Represents a hard disk drive inside of a virtual machine.</span></span> <span data-ttu-id="8b3d2-105">Esta unidad de disco duro puede ser un dispositivo de paso a través (si se ha conectado un disco duro físico a la máquina virtual) o un dispositivo sintético que se rellena con un medio de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-105">This hard disk drive can be either a pass-through device (if a physical hard disk was attached to the virtual machine) or a synthetic device that is populated with virtual hard disk media.</span></span> <span data-ttu-id="8b3d2-106">Dado que los discos duros virtuales y físicos se pueden agregar y quitar de la máquina virtual, hay dos grupos de recursos asociados a esta clase, uno para los discos duros de paso a través y otro para los discos duros virtuales.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-106">Because virtual and physical hard disks can be added and removed from the virtual machine, there are two resource pools associated with this class, one for pass-through hard disks and the other for virtual hard disks.</span></span> <span data-ttu-id="8b3d2-107">Los discos duros solo se pueden agregar o quitar de la controladora SCSI virtual cuando la máquina virtual está en línea.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-107">Hard disks can only be added to or removed from the virtual SCSI controller when the virtual machine is online.</span></span> <span data-ttu-id="8b3d2-108">Los discos solo se pueden agregar o quitar de la controladora IDE virtual cuando la máquina virtual está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-108">Disks can only be added to or removed from the virtual IDE controller when the virtual machine is offline.</span></span>

<span data-ttu-id="8b3d2-109">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b3d2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b3d2-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskDrive : CIM_DiskDrive
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 2000000000;
  uint64   DefaultBlockSize = 512;
  uint64   MaxBlockSize;
  uint64   MinBlockSize = 512;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = True;
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
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint32   DriveNumber;
};
```

## <a name="members"></a><span data-ttu-id="8b3d2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8b3d2-111">Members</span></span>

<span data-ttu-id="8b3d2-112">La clase **MSVM \_ DiskDrive** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8b3d2-112">The **Msvm\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="8b3d2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b3d2-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="8b3d2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b3d2-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8b3d2-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b3d2-115">Methods</span></span>

<span data-ttu-id="8b3d2-116">La clase **MSVM \_ DiskDrive** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-116">The **Msvm\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="8b3d2-117">Método</span><span class="sxs-lookup"><span data-stu-id="8b3d2-117">Method</span></span>                                                          | <span data-ttu-id="8b3d2-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b3d2-118">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="8b3d2-119">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-119">**EnableDevice**</span></span>                                                | <span data-ttu-id="8b3d2-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="8b3d2-121">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-121">**LockMedia**</span></span>](msvm-diskdrive-lockmedia.md)                   | <span data-ttu-id="8b3d2-122">Bloquea o libera los medios.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-122">Locks or releases the media.</span></span><br/>  |
| <span data-ttu-id="8b3d2-123">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-123">**OnlineDevice**</span></span>                                                | <span data-ttu-id="8b3d2-124">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8b3d2-125">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-125">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="8b3d2-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-126">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="8b3d2-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-127">**RequestStateChange**</span></span>](msvm-diskdrive-requeststatechange.md) | <span data-ttu-id="8b3d2-128">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-128">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="8b3d2-129">**Reset**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-129">**Reset**</span></span>](msvm-diskdrive-reset.md)                           | <span data-ttu-id="8b3d2-130">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-130">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="8b3d2-131">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-131">**RestoreProperties**</span></span>                                           | <span data-ttu-id="8b3d2-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-132">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8b3d2-133">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-133">**SaveProperties**</span></span>                                              | <span data-ttu-id="8b3d2-134">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-134">This method is not supported.</span></span><br/> |
| <span data-ttu-id="8b3d2-135">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-135">**SetPowerState**</span></span>                                               | <span data-ttu-id="8b3d2-136">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-136">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8b3d2-137">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b3d2-137">Properties</span></span>

<span data-ttu-id="8b3d2-138">La clase **MSVM \_ DiskDrive** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-138">The **Msvm\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b3d2-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-140">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-142">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en 6 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-143">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-146">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-148">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-150">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8b3d2-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="8b3d2-151">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-152">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-152">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-153">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-155">Las capacidades del dispositivo de acceso a medios.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-155">The capabilities of the media access device.</span></span> <span data-ttu-id="8b3d2-156">Esta propiedad se hereda de [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y se establece en los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-156">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to the following values.</span></span>



| <span data-ttu-id="8b3d2-157">Value</span><span class="sxs-lookup"><span data-stu-id="8b3d2-157">Value</span></span>                                                                        | <span data-ttu-id="8b3d2-158">Significado</span><span class="sxs-lookup"><span data-stu-id="8b3d2-158">Meaning</span></span>                                                                                 |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b3d2-159"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-159"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8b3d2-160">La entrada correspondiente en **CapabilityDescriptions** es "Random Access".</span><span class="sxs-lookup"><span data-stu-id="8b3d2-160">The corresponding entry in **CapabilityDescriptions** is "Random Access".</span></span><br/>    |
| <dl> <span data-ttu-id="8b3d2-161"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-161"><dt>4</dt></span></span> </dl> | <span data-ttu-id="8b3d2-162">La entrada correspondiente en **CapabilityDescriptions** es "supportly Writing".</span><span class="sxs-lookup"><span data-stu-id="8b3d2-162">The corresponding entry in **CapabilityDescriptions** is "Supports Writing".</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8b3d2-163">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-163">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-164">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-166">Matriz de cadenas de formato libre que proporciona explicaciones detalladas para las características del dispositivo de acceso indicadas en la matriz de propiedades **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="8b3d2-166">An array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="8b3d2-167">Cada entrada de esta matriz está relacionada con la entrada de la matriz de propiedades **Capabilities** , que se encuentra en el mismo índice.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-167">Each entry of this array is related to the entry in the **Capabilities** property array, located at the same index.</span></span> <span data-ttu-id="8b3d2-168">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-168">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-169">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-172">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-172">A short description of the object.</span></span> <span data-ttu-id="8b3d2-173">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-174">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-174">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-175">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-177">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-177">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8b3d2-178">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-178">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8b3d2-179">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-179">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8b3d2-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-180"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-181"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-182"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-183"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-184"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-185"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="8b3d2-186"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8b3d2-187">)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-187">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b3d2-188">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-188">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-191">Cadena que indica el algoritmo o la herramienta que se usa para comprimir el archivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-191">A string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="8b3d2-192">Si el esquema de compresión es desconocido o no se ha descrito, use "Unknown".</span><span class="sxs-lookup"><span data-stu-id="8b3d2-192">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="8b3d2-193">Si el archivo lógico está comprimido, pero el esquema de compresión es desconocido o no se ha descrito, use "comprimido".</span><span class="sxs-lookup"><span data-stu-id="8b3d2-193">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="8b3d2-194">Si el archivo lógico no está comprimido, use "no comprimido".</span><span class="sxs-lookup"><span data-stu-id="8b3d2-194">If the logical file is not compressed, use "Not Compressed".</span></span> <span data-ttu-id="8b3d2-195">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en "Not Compressed".</span><span class="sxs-lookup"><span data-stu-id="8b3d2-195">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "Not Compressed".</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-197">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-199">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-199">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8b3d2-200">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-200">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-201">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-201">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-202">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-204">Tamaño de bloque predeterminado, en bytes, para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-204">The default block size, in bytes, for the device.</span></span> <span data-ttu-id="8b3d2-205">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 512.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-205">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-206">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-209">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-209">A description of the object.</span></span> <span data-ttu-id="8b3d2-210">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-212">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-214">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-214">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8b3d2-215">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8b3d2-216">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8b3d2-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-217"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-218"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-219"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-220"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-221"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-222"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="8b3d2-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8b3d2-225">)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b3d2-226">**ID**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-226">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-229">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-229">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="8b3d2-230">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-231">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-231">**DriveNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-232">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-234">El número de unidades físicas en el sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-234">The number of the physical drives on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-235">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-235">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-236">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-238">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-238">A display name for the object.</span></span> <span data-ttu-id="8b3d2-239">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-239">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-241">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-243">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-243">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="8b3d2-244">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-246">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-248">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="8b3d2-249">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="8b3d2-250">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8b3d2-251">Value</span><span class="sxs-lookup"><span data-stu-id="8b3d2-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="8b3d2-252">Significado</span><span class="sxs-lookup"><span data-stu-id="8b3d2-252">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="8b3d2-253"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="8b3d2-254">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-254">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="8b3d2-255"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="8b3d2-256"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="8b3d2-257">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-257">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="8b3d2-258"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="8b3d2-259">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-259">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="8b3d2-260"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="8b3d2-261">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="8b3d2-262"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="8b3d2-263">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="8b3d2-264"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="8b3d2-265">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="8b3d2-266"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="8b3d2-267">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-267">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="8b3d2-268"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="8b3d2-269">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="8b3d2-270">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="8b3d2-271">El elemento está habilitado, pero está en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-271">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="8b3d2-272">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-272">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="8b3d2-273">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="8b3d2-274"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="8b3d2-275">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-275">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="8b3d2-276">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-276">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="8b3d2-277">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-277">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-278">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-280">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-280">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-281">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-281">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-282">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-284">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-285">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-285">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-286">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-287">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-288">Cadena que describe los tipos de detección y corrección de errores admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-288">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="8b3d2-289">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en "none".</span><span class="sxs-lookup"><span data-stu-id="8b3d2-289">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to "None".</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-291">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-292">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-293">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-293">The current health of the element.</span></span> <span data-ttu-id="8b3d2-294">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="8b3d2-295">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8b3d2-296">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-297">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-297">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-298">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-298">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-300">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-302">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-304">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="8b3d2-305">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-309">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-310">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8b3d2-311">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-312">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-312">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-313">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-315">Fecha y hora en que se limpió por última vez el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-315">The date and time when the device was last cleaned.</span></span> <span data-ttu-id="8b3d2-316">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-316">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-317">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-318">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-320">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-320">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-321">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-321">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-322">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-322">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-324">Tiempo, en milisegundos, desde la carga hasta la capacidad de leer o escribir un medio.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-324">The time, in milliseconds, from load to being able to read or write a media.</span></span> <span data-ttu-id="8b3d2-325">Por ejemplo, en el caso de las unidades de disco, es el intervalo entre un disco que no gira hasta el disco que informa de que está listo para lectura y escritura (es decir, el disco gira a velocidades nominales).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-325">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write (that is, the disk spinning at nominal speeds).</span></span> <span data-ttu-id="8b3d2-326">En el caso de las unidades de cinta, es el momento desde que se inserta un medio para informar de que está listo para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-326">For tape drives, this is the time from a media being injected to reporting that it is ready for an application.</span></span> <span data-ttu-id="8b3d2-327">Normalmente, se encuentra en el área de BOT de la cinta.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-327">This is usually at the tape's BOT area.</span></span> <span data-ttu-id="8b3d2-328">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) y está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-328">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice) and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-329">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-329">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-330">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-332">Tiempo, en milisegundos, que se va a pasar de la primera ubicación del medio a la ubicación más lejana con respecto a la hora.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-332">The time, in milliseconds, to move from the first location on the media to the location that is furthest with respect to time.</span></span> <span data-ttu-id="8b3d2-333">En el caso de una unidad de disco, representa la búsqueda completa y el retraso de rotación completo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-333">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="8b3d2-334">En el caso de las unidades de cinta, representa una búsqueda desde el principio de la cinta hasta el punto más alejado físicamente.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-334">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span> <span data-ttu-id="8b3d2-335">(El final de una cinta puede estar en su punto más lejano físicamente, pero esto no es necesariamente cierto). Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-335">(The end of a tape may be at its most physically distant point, but this is not necessarily true.) This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-336">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-336">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-337">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-338">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-339">Tamaño máximo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-339">The maximum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="8b3d2-340">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 512 para las unidades de disco duro virtual, la variable para las unidades de paso a través.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-340">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-341">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-341">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-342">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-342">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-343">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-344">Tamaño máximo, en kilobytes, de los medios admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-344">The maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="8b3d2-345">Los kilobytes se interpretan como el número de bytes multiplicado por 1000 (no por el número de bytes multiplicado por 1024).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-345">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span> <span data-ttu-id="8b3d2-346">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 2 mil millones para las unidades de disco duro virtual, la variable para las unidades de paso a través.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-346">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 2,000,000,000 for virtual hard disk drives, variable for pass-through drives.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-347">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-347">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-348">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-349">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-350">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-351">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-351">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-352">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-354">Las unidades máximas que se pueden usar antes de que se limpie el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-354">The maximum units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="8b3d2-355">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 0xffffffffffffffff.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-355">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0xffffffffffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-356">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-356">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-357">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-358">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-359">**True** si el medio está bloqueado en el dispositivo y no se puede expulsar; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-359">**True** if the media is locked in the device and cannot be ejected; otherwise, **False**.</span></span> <span data-ttu-id="8b3d2-360">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en **true**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-360">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-361">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-361">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-362">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-362">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-364">Tamaño mínimo del bloque, en bytes, para los medios a los que tiene acceso el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-364">The minimum block size, in bytes, for media accessed by the device.</span></span> <span data-ttu-id="8b3d2-365">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 512.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-365">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 512.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-366">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-366">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-367">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-368">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-369">En el caso de un dispositivo que admita medios extraíbles, el número de veces que los medios se han montado para la transferencia de datos o para limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-369">For a device that supports removable media, the number of times that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="8b3d2-370">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no es aplicable y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-370">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="8b3d2-371">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-371">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-372">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-373">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-374">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-375">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-375">The label by which the object is known.</span></span> <span data-ttu-id="8b3d2-376">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-377">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-377">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-378">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-378">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-379">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-380">**True** si el dispositivo de acceso a medios necesita limpieza; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-380">**True** if the media access device needs cleaning; otherwise, **False**.</span></span> <span data-ttu-id="8b3d2-381">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en **false**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-381">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **False**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-382">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-382">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-383">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-384">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-385">Número máximo de medios individuales que se pueden admitir o insertar.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-385">The maximum number of multiple individual media that can be supported or inserted.</span></span> <span data-ttu-id="8b3d2-386">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-386">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-387">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-387">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-388">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-388">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-389">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-390">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8b3d2-390">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8b3d2-391">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-391">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8b3d2-392">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-392">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8b3d2-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-394"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-395"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-396"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-397"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-398"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-399"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-400"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-401"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-402"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-403"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-404"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-405"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-406"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-407"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-408"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-409"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-410"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="8b3d2-411"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8b3d2-412">)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-412">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b3d2-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-414">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-416">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-416">The current statuses of the object.</span></span> <span data-ttu-id="8b3d2-417">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-418">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-418">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-419">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-421">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-421">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8b3d2-422">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-422">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="8b3d2-423">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-423">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-424">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-424">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-425">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-427">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-427">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-428">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-428">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-429">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-429">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-431">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-432">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-432">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-433">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-434">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-435">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-437">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-438">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-439">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-440">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-440">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-441">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-443">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-443">Provides high level status information.</span></span> <span data-ttu-id="8b3d2-444">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-444">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8b3d2-445">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-445">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8b3d2-446">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-446">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8b3d2-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-447"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-448"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-448"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-449"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-450"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-451"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="8b3d2-452"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8b3d2-453">)</span><span class="sxs-lookup"><span data-stu-id="8b3d2-453">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8b3d2-454">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-454">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-455">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-455">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-456">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-457">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-457">The last requested or desired state for the element.</span></span> <span data-ttu-id="8b3d2-458">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-458">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="8b3d2-459">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-459">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="8b3d2-460">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8b3d2-460">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="8b3d2-461">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-461">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="8b3d2-462">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-462">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-463">**Seguridad**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-463">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-464">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-465">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-466">La seguridad operativa definida para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-466">The operational security defined for the device.</span></span> <span data-ttu-id="8b3d2-467">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 3 (ninguno).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-467">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 3 (None).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-468">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-468">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-469">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-470">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-471">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-471">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-472">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-472">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-473">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-473">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-474">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-475">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8b3d2-475">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8b3d2-476">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-476">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-478">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-479">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-480">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-480">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-481">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-481">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-482">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-482">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-483">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-484">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-484">The scoping system's creation class name.</span></span> <span data-ttu-id="8b3d2-485">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-485">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-488">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-488">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-489">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-489">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="8b3d2-490">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-490">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-491">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-491">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-492">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-492">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-493">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-494">Para un dispositivo que admita medios extraíbles, la fecha y la hora más recientes en que se montó el medio en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-494">For a device that supports removable media, the most recent date and time that media was mounted on the device.</span></span> <span data-ttu-id="8b3d2-495">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no tiene ningún significado y no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-495">For devices accessing nonremovable media, such as hard disks, this property has no meaning and is not applicable.</span></span> <span data-ttu-id="8b3d2-496">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-496">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-497">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-497">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-498">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-498">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-499">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-500">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-500">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8b3d2-501">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en "null".</span><span class="sxs-lookup"><span data-stu-id="8b3d2-501">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-502">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-502">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-503">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-503">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-504">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-505">En el caso de un dispositivo que admita medios extraíbles, el tiempo total (en segundos) que los medios se han montado para la transferencia de datos o para limpiar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-505">For a device that supports removable media, the total time (in seconds) that media have been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="8b3d2-506">En el caso de los dispositivos que tienen acceso a medios no extraíbles, como discos duros, esta propiedad no es aplicable y debe establecerse en 0.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-506">For devices accessing nonremovable media, such as hard disks, this property is not applicable and should be set to 0.</span></span> <span data-ttu-id="8b3d2-507">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-507">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-508">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-508">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-509">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-509">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-510">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-511">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-511">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-512">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-512">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-513">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-513">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-514">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-515">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-515">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8b3d2-516">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-516">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-517">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-517">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-518">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-520">La velocidad de transferencia de datos sostenida en KB/s que el dispositivo puede leer y escribir en un medio.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-520">The sustained data transfer rate in KB/sec that the device can read from and write to a media.</span></span> <span data-ttu-id="8b3d2-521">Se trata de una velocidad de datos sin procesar y sostenida.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-521">This is a sustained, raw data rate.</span></span> <span data-ttu-id="8b3d2-522">Las tarifas máximas o tarifas suponiendo que no se debería informar de la compresión en esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-522">Maximum rates or rates assuming compression should not be reported in this property.</span></span> <span data-ttu-id="8b3d2-523">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-523">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-524">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-524">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-525">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-526">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-527">Unidades relativas a su uso en **MaxUnitsBeforeCleaning**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-527">The units relative to its use in **MaxUnitsBeforeCleaning**.</span></span> <span data-ttu-id="8b3d2-528">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-528">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-529">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-529">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-530">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-531">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-532">Número actual de unidades utilizadas.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-532">The current number of units used.</span></span> <span data-ttu-id="8b3d2-533">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-533">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8b3d2-534">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-534">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b3d2-535">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-535">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8b3d2-536">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8b3d2-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8b3d2-537">Tiempo, en milisegundos, desde que se puede leer o escribir un elemento multimedia en su descarga.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-537">The time, in milliseconds, from being able to read or write a media to its unload.</span></span> <span data-ttu-id="8b3d2-538">Esta propiedad se hereda de [**\_ MediaAccessDevice CIM**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)y está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-538">This property is inherited from [**CIM\_MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice), and it is set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b3d2-539">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b3d2-539">Remarks</span></span>

<span data-ttu-id="8b3d2-540">El acceso a la clase **MSVM \_ DiskDrive** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="8b3d2-540">Access to the **Msvm\_DiskDrive** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8b3d2-541">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8b3d2-541">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b3d2-542">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b3d2-542">Requirements</span></span>



| <span data-ttu-id="8b3d2-543">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b3d2-543">Requirement</span></span> | <span data-ttu-id="8b3d2-544">Value</span><span class="sxs-lookup"><span data-stu-id="8b3d2-544">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b3d2-545">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b3d2-545">Minimum supported client</span></span><br/> | <span data-ttu-id="8b3d2-546">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b3d2-546">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8b3d2-547">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8b3d2-547">Minimum supported server</span></span><br/> | <span data-ttu-id="8b3d2-548">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8b3d2-548">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b3d2-549">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8b3d2-549">Namespace</span></span><br/>                | <span data-ttu-id="8b3d2-550">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8b3d2-550">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8b3d2-551">MOF</span><span class="sxs-lookup"><span data-stu-id="8b3d2-551">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b3d2-552"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-552"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b3d2-553">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8b3d2-553">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b3d2-554"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b3d2-554"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8b3d2-555">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b3d2-555">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b3d2-556">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-556">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dt>

[<span data-ttu-id="8b3d2-557">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="8b3d2-557">**CIM\_DiskDrive**</span></span>](/windows/desktop/CIMWin32Prov/cim-diskdrive)
</dt> <dt>

[<span data-ttu-id="8b3d2-558">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="8b3d2-558">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

