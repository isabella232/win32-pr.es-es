---
description: Representa medios de unidad de almacenamiento y se usa para rellenar las unidades de almacenamiento.
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Clase Msvm_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5071f2a102a32364888c9c7de5121ede5249f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687644"
---
# <a name="msvm_logicaldisk-class"></a><span data-ttu-id="110af-103">MSVM \_ LogicalDisk (clase)</span><span class="sxs-lookup"><span data-stu-id="110af-103">Msvm\_LogicalDisk class</span></span>

<span data-ttu-id="110af-104">Representa medios de unidad de almacenamiento y se usa para rellenar las unidades de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="110af-104">Represents storage drive media and is used to populate the storage drives.</span></span> <span data-ttu-id="110af-105">Entre los tipos de medios admitidos se incluyen archivos de disco duro virtuales, archivos de disquete virtuales, archivos ISO y medios de dispositivo físicos.</span><span class="sxs-lookup"><span data-stu-id="110af-105">The media types supported include virtual hard files, virtual floppy files, ISO files, and physical device media.</span></span>

<span data-ttu-id="110af-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="110af-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="110af-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="110af-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  uint16   CreationClassName = "Msvm_LogicalDisk";
  string   DeviceID;
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
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="110af-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="110af-108">Members</span></span>

<span data-ttu-id="110af-109">La clase **MSVM \_ LogicalDisk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="110af-109">The **Msvm\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="110af-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="110af-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="110af-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="110af-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="110af-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="110af-112">Methods</span></span>

<span data-ttu-id="110af-113">La clase **MSVM \_ LogicalDisk** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="110af-113">The **Msvm\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="110af-114">Método</span><span class="sxs-lookup"><span data-stu-id="110af-114">Method</span></span>                                                            | <span data-ttu-id="110af-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="110af-115">Description</span></span>                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="110af-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="110af-116">**EnableDevice**</span></span>                                                  | <span data-ttu-id="110af-117">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="110af-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="110af-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="110af-118">**OnlineDevice**</span></span>                                                  | <span data-ttu-id="110af-119">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="110af-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="110af-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="110af-120">**QuiesceDevice**</span></span>                                                 | <span data-ttu-id="110af-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="110af-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="110af-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="110af-122">**RequestStateChange**</span></span>](msvm-logicaldisk-requeststatechange.md) | <span data-ttu-id="110af-123">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="110af-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="110af-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="110af-124">**Reset**</span></span>](msvm-logicaldisk-reset.md)                           | <span data-ttu-id="110af-125">Restablece el servicio.</span><span class="sxs-lookup"><span data-stu-id="110af-125">Resets the service.</span></span><br/>           |
| <span data-ttu-id="110af-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="110af-126">**RestoreProperties**</span></span>                                             | <span data-ttu-id="110af-127">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="110af-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="110af-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="110af-128">**SaveProperties**</span></span>                                                | <span data-ttu-id="110af-129">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="110af-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="110af-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="110af-130">**SetPowerState**</span></span>                                                 | <span data-ttu-id="110af-131">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="110af-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="110af-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="110af-132">Properties</span></span>

<span data-ttu-id="110af-133">La clase **MSVM \_ LogicalDisk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="110af-133">The **Msvm\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="110af-134">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="110af-134">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-137">Indica si el medio es legible, grabable o ambos.</span><span class="sxs-lookup"><span data-stu-id="110af-137">Indicates whether the media is readable, writeable, or both.</span></span> <span data-ttu-id="110af-138">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-138">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="110af-139">Value</span><span class="sxs-lookup"><span data-stu-id="110af-139">Value</span></span>                                                                        | <span data-ttu-id="110af-140">Significado</span><span class="sxs-lookup"><span data-stu-id="110af-140">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="110af-141"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="110af-141"><dt>0</dt></span></span> </dl> | <span data-ttu-id="110af-142">Unknown</span><span class="sxs-lookup"><span data-stu-id="110af-142">Unknown</span></span><br/>     |
| <dl> <span data-ttu-id="110af-143"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="110af-143"><dt>1</dt></span></span> </dl> | <span data-ttu-id="110af-144">Puedan.</span><span class="sxs-lookup"><span data-stu-id="110af-144">Readable.</span></span><br/>   |
| <dl> <span data-ttu-id="110af-145"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="110af-145"><dt>2</dt></span></span> </dl> | <span data-ttu-id="110af-146">Grabable.</span><span class="sxs-lookup"><span data-stu-id="110af-146">Writeable.</span></span><br/>  |
| <dl> <span data-ttu-id="110af-147"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="110af-147"><dt>3</dt></span></span> </dl> | <span data-ttu-id="110af-148">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="110af-148">Read/write.</span></span><br/> |
| <dl> <span data-ttu-id="110af-149"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="110af-149"><dt>4</dt></span></span> </dl> | <span data-ttu-id="110af-150">Escribir una vez.</span><span class="sxs-lookup"><span data-stu-id="110af-150">Write once.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="110af-151">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="110af-151">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-152">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="110af-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-154">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="110af-154">Any additional availability and status of the device.</span></span> <span data-ttu-id="110af-155">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="110af-155">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="110af-156">Value</span><span class="sxs-lookup"><span data-stu-id="110af-156">Value</span></span>                                                                            | <span data-ttu-id="110af-157">Significado</span><span class="sxs-lookup"><span data-stu-id="110af-157">Meaning</span></span>                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="110af-158"><dt>1,8</dt></span><span class="sxs-lookup"><span data-stu-id="110af-158"><dt>{ 6 }</dt></span></span> </dl> | <span data-ttu-id="110af-159">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="110af-159">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="110af-160">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="110af-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-163">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="110af-163">The primary availability and status of the device.</span></span> <span data-ttu-id="110af-164">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="110af-164">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="110af-165">Value</span><span class="sxs-lookup"><span data-stu-id="110af-165">Value</span></span>                                                                        | <span data-ttu-id="110af-166">Significado</span><span class="sxs-lookup"><span data-stu-id="110af-166">Meaning</span></span>                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="110af-167"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="110af-167"><dt>6</dt></span></span> </dl> | <span data-ttu-id="110af-168">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="110af-168">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="110af-169">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="110af-169">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-170">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-170">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="110af-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-172">Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="110af-172">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="110af-173">Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="110af-173">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="110af-174">Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="110af-174">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="110af-175">Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.</span><span class="sxs-lookup"><span data-stu-id="110af-175">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="110af-176">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="110af-176">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="110af-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="110af-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-178">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="110af-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="110af-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-180">Tamaño, en bytes, de los bloques que forman la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="110af-180">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="110af-181">Si el tamaño de bloque es variable, se debe especificar el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="110af-181">If the block size is variable, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="110af-182">Si se desconoce el tamaño de bloque, o si un concepto de bloque no es válido (por ejemplo, para las extensiones de agregado, la memoria o los discos lógicos), contendrá 1.</span><span class="sxs-lookup"><span data-stu-id="110af-182">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), this will contain 1.</span></span> <span data-ttu-id="110af-183">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-183">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-184">**Caption**</span><span class="sxs-lookup"><span data-stu-id="110af-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-187">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="110af-187">A short description of the object.</span></span> <span data-ttu-id="110af-188">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="110af-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="110af-189">"Imagen de disco ISO"</span><span class="sxs-lookup"><span data-stu-id="110af-189">"ISO Disk Image"</span></span>

<span data-ttu-id="110af-190">"Imagen de disco duro"</span><span class="sxs-lookup"><span data-stu-id="110af-190">"Hard Disk Image"</span></span>

<span data-ttu-id="110af-191">"Imagen de disquete"</span><span class="sxs-lookup"><span data-stu-id="110af-191">"Floppy Disk Image"</span></span>

<span data-ttu-id="110af-192">"Disco de CD/DVD"</span><span class="sxs-lookup"><span data-stu-id="110af-192">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="110af-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="110af-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-194">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-196">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="110af-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="110af-197">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="110af-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="110af-198">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="110af-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-199">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="110af-199">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-200">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="110af-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="110af-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-202">Número máximo de bloques, de tamaño de **bloqueos**, que están disponibles para el consumo al encapar las extensiones de almacenamiento mediante la Asociación de [**\_ base de MSVM**](msvm-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="110af-202">The maximum number of blocks, of size **BlockSize**, that are available for consumption when layering storage extents using the [**Msvm\_BasedOn**](msvm-basedon.md) association.</span></span> <span data-ttu-id="110af-203">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-203">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-204">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="110af-204">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-205">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-207">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="110af-207">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="110af-208">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="110af-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="110af-209">**Organización de los mismos**</span><span class="sxs-lookup"><span data-stu-id="110af-209">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-210">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-212">El tipo de organización de datos que se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-212">The type of data organization used.</span></span> <span data-ttu-id="110af-213">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-213">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="110af-214">Value</span><span class="sxs-lookup"><span data-stu-id="110af-214">Value</span></span>                                                                        | <span data-ttu-id="110af-215">Significado</span><span class="sxs-lookup"><span data-stu-id="110af-215">Meaning</span></span>                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <span data-ttu-id="110af-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="110af-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="110af-217">Bloque fijo.</span><span class="sxs-lookup"><span data-stu-id="110af-217">Fixed block.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="110af-218">**Redundancia de los mismos**</span><span class="sxs-lookup"><span data-stu-id="110af-218">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-219">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-221">El número de copias completas de los datos que se mantienen actualmente.</span><span class="sxs-lookup"><span data-stu-id="110af-221">The number of complete copies of data currently maintained.</span></span> <span data-ttu-id="110af-222">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-222">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-223">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="110af-223">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-224">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="110af-224">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="110af-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-226">Un porcentaje que especifica la cantidad de espacio que se debe reservar en una réplica para almacenar en caché los cambios.</span><span class="sxs-lookup"><span data-stu-id="110af-226">A percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span> <span data-ttu-id="110af-227">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-227">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-228">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="110af-228">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-229">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="110af-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="110af-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-231">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="110af-231">A description of the object.</span></span> <span data-ttu-id="110af-232">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="110af-232">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-233">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="110af-233">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-234">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-236">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="110af-236">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="110af-237">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="110af-237">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="110af-238">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="110af-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-239">**ID**</span><span class="sxs-lookup"><span data-stu-id="110af-239">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-242">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en "Microsoft:*GUID* del \\ *dispositivo-datos específicos*".</span><span class="sxs-lookup"><span data-stu-id="110af-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="110af-243">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="110af-243">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-246">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="110af-246">A display name for the object.</span></span> <span data-ttu-id="110af-247">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="110af-247">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="110af-248">"Imagen de disco ISO"</span><span class="sxs-lookup"><span data-stu-id="110af-248">"ISO Disk Image"</span></span>

<span data-ttu-id="110af-249">"Imagen de disco duro"</span><span class="sxs-lookup"><span data-stu-id="110af-249">"Hard Disk Image"</span></span>

<span data-ttu-id="110af-250">"Imagen de disquete"</span><span class="sxs-lookup"><span data-stu-id="110af-250">"Floppy Disk Image"</span></span>

<span data-ttu-id="110af-251">"Disco de CD/DVD"</span><span class="sxs-lookup"><span data-stu-id="110af-251">"CD/DVD Disk"</span></span>

</dd> <dt>

<span data-ttu-id="110af-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="110af-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-253">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-255">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="110af-255">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="110af-256">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="110af-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="110af-257">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="110af-257">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-260">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="110af-260">The enabled and disabled states of an element.</span></span> <span data-ttu-id="110af-261">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="110af-261">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="110af-262">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="110af-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="110af-263">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="110af-263">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-264">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="110af-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="110af-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-266">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="110af-266">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="110af-267">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-268">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="110af-268">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-269">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-271">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="110af-271">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="110af-272">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-272">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-273">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="110af-273">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-276">Cadena que describe los tipos de detección y corrección de errores admitidos por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="110af-276">A string that describes the types of error detection and correction supported by this device.</span></span> <span data-ttu-id="110af-277">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-277">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-278">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="110af-278">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-279">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="110af-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-281">Cualquier información de estado adicional más allá de la capturada en **OperationalStatus** y otras propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="110af-281">Any additional status information beyond that captured in the **OperationalStatus** and other inherited properties.</span></span>



| <span data-ttu-id="110af-282">Value</span><span class="sxs-lookup"><span data-stu-id="110af-282">Value</span></span>                                                                            | <span data-ttu-id="110af-283">Significado</span><span class="sxs-lookup"><span data-stu-id="110af-283">Meaning</span></span>                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="110af-284"><dt>dos</dt></span><span class="sxs-lookup"><span data-stu-id="110af-284"><dt>{ 2 }</dt></span></span> </dl> | <span data-ttu-id="110af-285">Ninguno/no aplicable.</span><span class="sxs-lookup"><span data-stu-id="110af-285">None/Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="110af-286">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="110af-286">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-287">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-289">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="110af-289">The current health of the element.</span></span> <span data-ttu-id="110af-290">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="110af-290">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="110af-291">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="110af-291">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="110af-292">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="110af-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-293">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="110af-293">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-294">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="110af-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="110af-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-296">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="110af-296">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="110af-297">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="110af-297">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="110af-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="110af-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-299">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="110af-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="110af-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-301">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="110af-301">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="110af-302">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="110af-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-303">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="110af-303">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="110af-306">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="110af-306">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="110af-307">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="110af-307">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="110af-308">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="110af-308">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-309">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="110af-309">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-310">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="110af-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="110af-311">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-312">Indica si las extensiones de almacenamiento subyacentes participan en un grupo de redundancia de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="110af-312">Indicates whether the underlying storage extents participate in a storage redundancy group.</span></span> <span data-ttu-id="110af-313">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-313">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-314">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="110af-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-315">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="110af-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="110af-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-317">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="110af-317">The last error code reported by the logical device.</span></span> <span data-ttu-id="110af-318">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-318">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-319">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="110af-319">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-320">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="110af-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="110af-321">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-322">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="110af-322">This property has been deprecated.</span></span> <span data-ttu-id="110af-323">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-324">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="110af-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-325">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-326">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-327">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="110af-327">The label by which the object is known.</span></span> <span data-ttu-id="110af-328">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y es igual que la propiedad **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="110af-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="110af-329">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="110af-329">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-330">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-332">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-332">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="110af-333">Value</span><span class="sxs-lookup"><span data-stu-id="110af-333">Value</span></span>                                                                         | <span data-ttu-id="110af-334">Significado</span><span class="sxs-lookup"><span data-stu-id="110af-334">Meaning</span></span>                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="110af-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="110af-335"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="110af-336">Otros</span><span class="sxs-lookup"><span data-stu-id="110af-336">Other</span></span><br/>                        |
| <dl> <span data-ttu-id="110af-337"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="110af-337"><dt>12</dt></span></span> </dl> | <span data-ttu-id="110af-338">Nombre del dispositivo del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="110af-338">Operating system device name</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="110af-339">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="110af-339">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-340">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-342">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-342">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>



| <span data-ttu-id="110af-343">Value</span><span class="sxs-lookup"><span data-stu-id="110af-343">Value</span></span>                                                                        | <span data-ttu-id="110af-344">Significado</span><span class="sxs-lookup"><span data-stu-id="110af-344">Meaning</span></span>                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="110af-345"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="110af-345"><dt>1</dt></span></span> </dl> | <span data-ttu-id="110af-346">Otros</span><span class="sxs-lookup"><span data-stu-id="110af-346">Other</span></span><br/>                             |
| <dl> <span data-ttu-id="110af-347"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="110af-347"><dt>8</dt></span></span> </dl> | <span data-ttu-id="110af-348">Espacio de nombres de dispositivo de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="110af-348">Operating system device namespace</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="110af-349">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="110af-349">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-350">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="110af-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="110af-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-352">Indica si no existe ningún punto único de error.</span><span class="sxs-lookup"><span data-stu-id="110af-352">Indicates whether there exists no single point of failure.</span></span> <span data-ttu-id="110af-353">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-353">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-354">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="110af-354">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-355">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="110af-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="110af-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-357">El número de bloques consecutivos, cada uno bloquea el tamaño del valor contenido en la propiedad **blocksize** , que forma la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="110af-357">The number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="110af-358">El tamaño total de la extensión de almacenamiento se puede calcular multiplicando el valor de la propiedad **blocksize** por el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="110af-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="110af-359">Si el valor de **blocksize** es 1, esta propiedad es el tamaño total de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="110af-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span> <span data-ttu-id="110af-360">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-360">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-361">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="110af-361">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-362">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-363">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-364">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="110af-364">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="110af-365">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="110af-365">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="110af-366">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="110af-366">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-367">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="110af-367">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-368">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="110af-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="110af-370">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="110af-370">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="110af-371">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="110af-371">The current statuses of the object.</span></span> <span data-ttu-id="110af-372">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="110af-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="110af-373">Cuando no se puede satisfacer el nivel de QoS necesario para el disco virtual, el estado principal (OperationalStatus \[ 0 \] ) se establece en degradado (3) y la matriz OperationalStatus contiene además un valor de estado secundario que indica la razón concreta de la condición QoS, según esta tabla.</span><span class="sxs-lookup"><span data-stu-id="110af-373">When the required QoS level for the virtual disk can't be satisfied, the primary status (OperationalStatus\[0\]) is set to Degraded (3) and the OperationalStatus array additionally contains a secondary status value that indicates the specific reason for the QoS condition, according to this table.</span></span>



| <span data-ttu-id="110af-374">Value</span><span class="sxs-lookup"><span data-stu-id="110af-374">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="110af-375">Descripción</span><span class="sxs-lookup"><span data-stu-id="110af-375">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="110af-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Rendimiento insuficiente (32788)</span><span class="sxs-lookup"><span data-stu-id="110af-376"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="110af-377">La tasa mínima de IOPS solicitada no está disponible actualmente para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="110af-377">The requested minimum IOPS rate is currently not available to the device.</span></span> <br/> |



 

> [!Note]  
> <span data-ttu-id="110af-378">OperationalStatus también se utiliza para notificar otras condiciones de error o ADVERTENCIA (por ejemplo, discrepancia de protocolo entre VSP y VSC).</span><span class="sxs-lookup"><span data-stu-id="110af-378">OperationalStatus is also used to report other error or warning conditions (for example, protocol mismatch between VSP and VSC).</span></span> <span data-ttu-id="110af-379">Si existen varias condiciones, el estado principal se establece degradado, y uno o varios valores de estado secundarios, en cualquier orden que empiece en el índice 1, se rellenan en la matriz.</span><span class="sxs-lookup"><span data-stu-id="110af-379">If multiple conditions exists, the primary status is set Degraded, and one or more secondary status values, in any order starting at index 1, is filled in the array.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="110af-380"><span id="OK"></span><span id="ok"></span>**Aceptar** (2)</span><span class="sxs-lookup"><span data-stu-id="110af-380"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="110af-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (3)</span><span class="sxs-lookup"><span data-stu-id="110af-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="110af-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (7)</span><span class="sxs-lookup"><span data-stu-id="110af-382"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="110af-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (11)</span><span class="sxs-lookup"><span data-stu-id="110af-383"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="110af-384">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="110af-384">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="110af-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (12)</span><span class="sxs-lookup"><span data-stu-id="110af-385"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="110af-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="110af-386"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="110af-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (16)</span><span class="sxs-lookup"><span data-stu-id="110af-387"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="110af-388">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="110af-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="110af-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>El **Protocolo no coincide** (32775)</span><span class="sxs-lookup"><span data-stu-id="110af-389"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="110af-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Tiempo de espera** de la comunicación (32783)</span><span class="sxs-lookup"><span data-stu-id="110af-390"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="110af-391">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="110af-391">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="110af-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Rendimiento insuficiente** (32788)</span><span class="sxs-lookup"><span data-stu-id="110af-392"><span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span data-ttu-id="110af-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Identificador de directiva QoS desconocido** (32791)</span><span class="sxs-lookup"><span data-stu-id="110af-393"><span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**Unknown QoS Policy ID** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span data-ttu-id="110af-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS no compatible** (32792)</span><span class="sxs-lookup"><span data-stu-id="110af-394"><span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS Not Supported** (32792)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="110af-395">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="110af-395">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span data-ttu-id="110af-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>La **configuración de QoS no coincide** (32793)</span><span class="sxs-lookup"><span data-stu-id="110af-396"><span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**QoS Configuration Mismatch** (32793)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="110af-397">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="110af-397">Added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span data-ttu-id="110af-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disco lleno** (32794)</span><span class="sxs-lookup"><span data-stu-id="110af-398"><span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disk Full** (32794)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="110af-399">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="110af-399">Added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="110af-400">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="110af-400">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-403">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="110af-403">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="110af-404">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="110af-404">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="110af-405">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="110af-405">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="110af-406">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="110af-406">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-407">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="110af-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="110af-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-409">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="110af-409">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="110af-410">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="110af-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="110af-411">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="110af-411">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-412">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-414">Cadena que describe el formato de la propiedad **Name** cuando **NameFormat** contiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="110af-414">A string that describes the format of the **Name** property when **NameFormat** contains the value 1 (Other).</span></span> <span data-ttu-id="110af-415">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-415">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-416">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="110af-416">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-417">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-419">Una cadena que describe el espacio de nombres de la propiedad **Name** cuando **NameNamespace** contiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="110af-419">A string that describes the namespace of the **Name** property when **NameNamespace** contains the value 1 (Other).</span></span> <span data-ttu-id="110af-420">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-420">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-421">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="110af-421">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-422">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-424">El número de paquetes físicos que pueden fallar actualmente sin pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="110af-424">The number of physical packages that can currently fail without data loss.</span></span> <span data-ttu-id="110af-425">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-425">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-426">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="110af-426">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-427">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-427">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="110af-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-429">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="110af-429">The power management capabilities of the device.</span></span> <span data-ttu-id="110af-430">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-430">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-431">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="110af-431">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-432">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="110af-432">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="110af-433">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-434">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="110af-434">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="110af-435">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-435">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-436">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="110af-436">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-437">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="110af-437">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="110af-438">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-439">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="110af-439">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="110af-440">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-440">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-441">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="110af-441">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-442">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-442">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-444">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="110af-444">Provides high level status information.</span></span> <span data-ttu-id="110af-445">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="110af-445">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="110af-446">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="110af-446">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="110af-447">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="110af-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-448">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="110af-448">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-449">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="110af-449">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="110af-450">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-451">Indica si el sistema contenedor tiene la capacidad de crear o eliminar este elemento operativo.</span><span class="sxs-lookup"><span data-stu-id="110af-451">Indicates whether the containing system has the ability to create or delete this operational element.</span></span> <span data-ttu-id="110af-452">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent)y está establecida en **false** para los medios basados en archivos y en **true** para los medios de paso a través.</span><span class="sxs-lookup"><span data-stu-id="110af-452">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent), and it is set to **False** for file-based media and **True** for pass-through media.</span></span>

</dd> <dt>

<span data-ttu-id="110af-453">**Propósito**</span><span class="sxs-lookup"><span data-stu-id="110af-453">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-454">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-455">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-456">Cadena que describe el medio y/o su uso.</span><span class="sxs-lookup"><span data-stu-id="110af-456">A string that describes the media and/or its use.</span></span> <span data-ttu-id="110af-457">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-457">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-458">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="110af-458">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-459">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-460">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-461">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="110af-461">The last requested or desired state for the element.</span></span> <span data-ttu-id="110af-462">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="110af-462">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="110af-463">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="110af-463">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="110af-464">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="110af-464">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="110af-465">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="110af-465">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="110af-466">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="110af-466">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="110af-467">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="110af-467">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-468">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="110af-468">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="110af-469">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-470">Indica si un dispositivo de acceso multimedia tiene acceso de forma secuencial al almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="110af-470">Indicates whether the storage is sequentially accessed by a media access device.</span></span> <span data-ttu-id="110af-471">Los medios de cinta de paso a través son un ejemplo de una extensión de almacenamiento de acceso secuencial.</span><span class="sxs-lookup"><span data-stu-id="110af-471">Pass-through tape media is an example of a sequentially accessed storage extent.</span></span> <span data-ttu-id="110af-472">Esta propiedad se hereda de [**\_ StorageExtent CIM**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span><span class="sxs-lookup"><span data-stu-id="110af-472">This property is inherited from [**CIM\_StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).</span></span>

</dd> <dt>

<span data-ttu-id="110af-473">**Estado**</span><span class="sxs-lookup"><span data-stu-id="110af-473">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-474">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-476">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="110af-476">The current status of the object.</span></span> <span data-ttu-id="110af-477">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-477">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-478">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="110af-478">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-479">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="110af-479">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="110af-480">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-481">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="110af-481">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="110af-482">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="110af-482">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="110af-483">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="110af-483">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-484">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-484">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-485">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-486">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="110af-486">The current state of the logical device.</span></span> <span data-ttu-id="110af-487">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-488">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="110af-488">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-489">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-489">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-490">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-491">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="110af-491">The scoping system's creation class name.</span></span> <span data-ttu-id="110af-492">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="110af-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="110af-493">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="110af-493">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-494">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="110af-494">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="110af-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-496">Identificador único de la máquina virtual de ámbito.</span><span class="sxs-lookup"><span data-stu-id="110af-496">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="110af-497">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="110af-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="110af-498">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="110af-498">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-499">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="110af-499">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="110af-500">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-501">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="110af-501">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="110af-502">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="110af-502">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="110af-503">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="110af-503">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-504">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="110af-504">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="110af-505">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-506">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="110af-506">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="110af-507">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-507">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="110af-508">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="110af-508">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="110af-509">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="110af-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="110af-510">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="110af-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="110af-511">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="110af-511">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="110af-512">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="110af-512">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="110af-513">Observaciones</span><span class="sxs-lookup"><span data-stu-id="110af-513">Remarks</span></span>

<span data-ttu-id="110af-514">El acceso a la clase **MSVM \_ LogicalDisk** podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="110af-514">Access to the **Msvm\_LogicalDisk** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="110af-515">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="110af-515">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="110af-516">Requisitos</span><span class="sxs-lookup"><span data-stu-id="110af-516">Requirements</span></span>



| <span data-ttu-id="110af-517">Requisito</span><span class="sxs-lookup"><span data-stu-id="110af-517">Requirement</span></span> | <span data-ttu-id="110af-518">Value</span><span class="sxs-lookup"><span data-stu-id="110af-518">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="110af-519">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="110af-519">Minimum supported client</span></span><br/> | <span data-ttu-id="110af-520">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="110af-520">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="110af-521">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="110af-521">Minimum supported server</span></span><br/> | <span data-ttu-id="110af-522">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="110af-522">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="110af-523">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="110af-523">Namespace</span></span><br/>                | <span data-ttu-id="110af-524">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="110af-524">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="110af-525">MOF</span><span class="sxs-lookup"><span data-stu-id="110af-525">MOF</span></span><br/>                      | <dl> <span data-ttu-id="110af-526"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="110af-526"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="110af-527">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="110af-527">DLL</span></span><br/>                      | <dl> <span data-ttu-id="110af-528"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="110af-528"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="110af-529">Vea también</span><span class="sxs-lookup"><span data-stu-id="110af-529">See also</span></span>

<dl> <dt>

[<span data-ttu-id="110af-530">**LogicalDisk de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="110af-530">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="110af-531">**LogicalDisk de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="110af-531">**CIM\_LogicalDisk**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[<span data-ttu-id="110af-532">**MSVM \_ StorageAlert**</span><span class="sxs-lookup"><span data-stu-id="110af-532">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="110af-533">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="110af-533">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

