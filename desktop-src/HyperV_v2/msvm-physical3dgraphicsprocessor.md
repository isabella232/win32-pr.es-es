---
description: Describe la unidad de procesamiento de gráficos (GPU) física 3D.
ms.assetid: 24e3d141-cbfe-4d40-907c-9a467c586c46
title: Msvm_Physical3dGraphicsProcessor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Physical3dGraphicsProcessor
- Msvm_Physical3dGraphicsProcessor.RequestStateChange
- Msvm_Physical3dGraphicsProcessor.SetPowerState
- Msvm_Physical3dGraphicsProcessor.Reset
- Msvm_Physical3dGraphicsProcessor.EnableDevice
- Msvm_Physical3dGraphicsProcessor.OnlineDevice
- Msvm_Physical3dGraphicsProcessor.QuiesceDevice
- Msvm_Physical3dGraphicsProcessor.SaveProperties
- Msvm_Physical3dGraphicsProcessor.RestoreProperties
- Msvm_Physical3dGraphicsProcessor.InstanceID
- Msvm_Physical3dGraphicsProcessor.Caption
- Msvm_Physical3dGraphicsProcessor.Description
- Msvm_Physical3dGraphicsProcessor.ElementName
- Msvm_Physical3dGraphicsProcessor.InstallDate
- Msvm_Physical3dGraphicsProcessor.Name
- Msvm_Physical3dGraphicsProcessor.OperationalStatus
- Msvm_Physical3dGraphicsProcessor.StatusDescriptions
- Msvm_Physical3dGraphicsProcessor.Status
- Msvm_Physical3dGraphicsProcessor.HealthState
- Msvm_Physical3dGraphicsProcessor.CommunicationStatus
- Msvm_Physical3dGraphicsProcessor.DetailedStatus
- Msvm_Physical3dGraphicsProcessor.OperatingStatus
- Msvm_Physical3dGraphicsProcessor.PrimaryStatus
- Msvm_Physical3dGraphicsProcessor.EnabledState
- Msvm_Physical3dGraphicsProcessor.OtherEnabledState
- Msvm_Physical3dGraphicsProcessor.RequestedState
- Msvm_Physical3dGraphicsProcessor.EnabledDefault
- Msvm_Physical3dGraphicsProcessor.TimeOfLastStateChange
- Msvm_Physical3dGraphicsProcessor.AvailableRequestedStates
- Msvm_Physical3dGraphicsProcessor.TransitioningToState
- Msvm_Physical3dGraphicsProcessor.SystemCreationClassName
- Msvm_Physical3dGraphicsProcessor.SystemName
- Msvm_Physical3dGraphicsProcessor.CreationClassName
- Msvm_Physical3dGraphicsProcessor.DeviceID
- Msvm_Physical3dGraphicsProcessor.PowerManagementSupported
- Msvm_Physical3dGraphicsProcessor.PowerManagementCapabilities
- Msvm_Physical3dGraphicsProcessor.Availability
- Msvm_Physical3dGraphicsProcessor.StatusInfo
- Msvm_Physical3dGraphicsProcessor.LastErrorCode
- Msvm_Physical3dGraphicsProcessor.ErrorDescription
- Msvm_Physical3dGraphicsProcessor.ErrorCleared
- Msvm_Physical3dGraphicsProcessor.OtherIdentifyingInfo
- Msvm_Physical3dGraphicsProcessor.PowerOnHours
- Msvm_Physical3dGraphicsProcessor.TotalPowerOnHours
- Msvm_Physical3dGraphicsProcessor.IdentifyingDescriptions
- Msvm_Physical3dGraphicsProcessor.AdditionalAvailability
- Msvm_Physical3dGraphicsProcessor.MaxQuiesceTime
- Msvm_Physical3dGraphicsProcessor.EnabledForVirtualization
- Msvm_Physical3dGraphicsProcessor.CompatibleForVirtualization
- Msvm_Physical3dGraphicsProcessor.GPUID
- Msvm_Physical3dGraphicsProcessor.DirectXVersion
- Msvm_Physical3dGraphicsProcessor.PixelShaderVersion
- Msvm_Physical3dGraphicsProcessor.DedicatedVideoMemory
- Msvm_Physical3dGraphicsProcessor.DedicatedSystemMemory
- Msvm_Physical3dGraphicsProcessor.SharedSystemMemory
- Msvm_Physical3dGraphicsProcessor.TotalVideoMemory
- Msvm_Physical3dGraphicsProcessor.AvailableVideoMemory
- Msvm_Physical3dGraphicsProcessor.DriverProvider
- Msvm_Physical3dGraphicsProcessor.DriverDate
- Msvm_Physical3dGraphicsProcessor.DriverInstalled
- Msvm_Physical3dGraphicsProcessor.DriverVersion
- Msvm_Physical3dGraphicsProcessor.DriverModelVersion
- Msvm_Physical3dGraphicsProcessor.Rating
- Msvm_Physical3dGraphicsProcessor.AdapterIndexID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e257fa319b1d1b55562f47c7a3049a694fc27f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817883"
---
# <a name="msvm_physical3dgraphicsprocessor-class"></a><span data-ttu-id="245f3-103">MSVM \_ Physical3dGraphicsProcessor (clase)</span><span class="sxs-lookup"><span data-stu-id="245f3-103">Msvm\_Physical3dGraphicsProcessor class</span></span>

<span data-ttu-id="245f3-104">Describe la unidad de procesamiento de gráficos (GPU) física 3D.</span><span class="sxs-lookup"><span data-stu-id="245f3-104">Describes the physical 3-D graphics processing unit (GPU).</span></span>

<span data-ttu-id="245f3-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="245f3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="245f3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="245f3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_Physical3dGraphicsProcessor : CIM_LogicalDevice
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
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  Boolean  EnabledForVirtualization;
  Boolean  CompatibleForVirtualization;
  string   GPUID;
  string   DirectXVersion;
  string   PixelShaderVersion;
  uint64   DedicatedVideoMemory;
  uint64   DedicatedSystemMemory;
  uint64   SharedSystemMemory;
  uint64   TotalVideoMemory;
  uint64   AvailableVideoMemory;
  string   DriverProvider;
  datetime DriverDate;
  datetime DriverInstalled;
  string   DriverVersion;
  string   DriverModelVersion;
  uint64   Rating;
  uint64   AdapterIndexID;
};
```

## <a name="members"></a><span data-ttu-id="245f3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="245f3-107">Members</span></span>

<span data-ttu-id="245f3-108">La clase **MSVM \_ Physical3dGraphicsProcessor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="245f3-108">The **Msvm\_Physical3dGraphicsProcessor** class has these types of members:</span></span>

-   [<span data-ttu-id="245f3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="245f3-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="245f3-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="245f3-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="245f3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="245f3-111">Methods</span></span>

<span data-ttu-id="245f3-112">La clase **MSVM \_ Physical3dGraphicsProcessor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="245f3-112">The **Msvm\_Physical3dGraphicsProcessor** class has these methods.</span></span>



| <span data-ttu-id="245f3-113">Método</span><span class="sxs-lookup"><span data-stu-id="245f3-113">Method</span></span>                 | <span data-ttu-id="245f3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="245f3-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="245f3-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="245f3-115">**EnableDevice**</span></span>       | <span data-ttu-id="245f3-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="245f3-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="245f3-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="245f3-117">**OnlineDevice**</span></span>       | <span data-ttu-id="245f3-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="245f3-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="245f3-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="245f3-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="245f3-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="245f3-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="245f3-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="245f3-121">**RequestStateChange**</span></span> | <span data-ttu-id="245f3-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="245f3-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="245f3-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="245f3-123">**Reset**</span></span>              | <span data-ttu-id="245f3-124">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="245f3-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="245f3-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="245f3-125">**RestoreProperties**</span></span>  | <span data-ttu-id="245f3-126">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="245f3-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="245f3-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="245f3-127">**SaveProperties**</span></span>     | <span data-ttu-id="245f3-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="245f3-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="245f3-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="245f3-129">**SetPowerState**</span></span>      | <span data-ttu-id="245f3-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="245f3-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="245f3-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="245f3-131">Properties</span></span>

<span data-ttu-id="245f3-132">La clase **MSVM \_ Physical3dGraphicsProcessor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="245f3-132">The **Msvm\_Physical3dGraphicsProcessor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="245f3-133">**AdapterIndexID**</span><span class="sxs-lookup"><span data-stu-id="245f3-133">**AdapterIndexID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-134">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-136">Especifica el identificador del índice de adaptador asignado a este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="245f3-136">Specifies the adapter index identifier allocated to this device.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="245f3-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-138">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="245f3-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-140">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="245f3-140">Any additional availability and status of the device.</span></span> <span data-ttu-id="245f3-141">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-142">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="245f3-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-145">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="245f3-145">The primary availability and status of the device.</span></span> <span data-ttu-id="245f3-146">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-146">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-147">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="245f3-147">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-148">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="245f3-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-150">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="245f3-150">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="245f3-151">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="245f3-151">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-152">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="245f3-152">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-153">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-155">Especifica la cantidad de memoria de vídeo, en bytes, que está disponible para la GPU.</span><span class="sxs-lookup"><span data-stu-id="245f3-155">Specifies the amount of video memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-156">**Caption**</span><span class="sxs-lookup"><span data-stu-id="245f3-156">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-159">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="245f3-159">A short description of the object.</span></span> <span data-ttu-id="245f3-160">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-161">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="245f3-161">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-162">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-164">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="245f3-164">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="245f3-165">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="245f3-165">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="245f3-166">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-166">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="245f3-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="245f3-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="245f3-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="245f3-169"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="245f3-170"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="245f3-171"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="245f3-172"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="245f3-173"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="245f3-174">)</span><span class="sxs-lookup"><span data-stu-id="245f3-174">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="245f3-175">**CompatibleForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="245f3-175">**CompatibleForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-176">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="245f3-176">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-178">**true si es** compatible con la virtualización; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="245f3-178">**true** if compatible for virtualization; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="245f3-179">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="245f3-179">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="245f3-180">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="245f3-180">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-183">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="245f3-183">The scoping system's creation class name.</span></span> <span data-ttu-id="245f3-184">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="245f3-184">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-185">**DedicatedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="245f3-185">**DedicatedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-186">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-188">Especifica la cantidad de memoria del sistema, en bytes, dedicada a la GPU.</span><span class="sxs-lookup"><span data-stu-id="245f3-188">Specifies the amount of system memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-189">**DedicatedVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="245f3-189">**DedicatedVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-190">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-192">Especifica la cantidad de memoria de vídeo, en bytes, dedicada a la GPU.</span><span class="sxs-lookup"><span data-stu-id="245f3-192">Specifies the amount of video memory, in bytes, that is dedicated to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-193">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="245f3-193">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-196">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="245f3-196">A description of the object.</span></span> <span data-ttu-id="245f3-197">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-198">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="245f3-198">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-199">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-201">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="245f3-201">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="245f3-202">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="245f3-202">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="245f3-203">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="245f3-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="245f3-204"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="245f3-205"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="245f3-206"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="245f3-207"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="245f3-208"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="245f3-209"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="245f3-210"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="245f3-211"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="245f3-212">)</span><span class="sxs-lookup"><span data-stu-id="245f3-212">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="245f3-213">**ID**</span><span class="sxs-lookup"><span data-stu-id="245f3-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-214">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-216">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="245f3-216">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="245f3-217">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="245f3-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-218">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="245f3-218">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245f3-221">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="245f3-221">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="245f3-222">Especifica el versión de DirectX compatible con la GPU.</span><span class="sxs-lookup"><span data-stu-id="245f3-222">Specifies the verison of DirectX that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-223">**DriverDate**</span><span class="sxs-lookup"><span data-stu-id="245f3-223">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-224">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="245f3-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-226">Especifica la fecha de compilación del controlador.</span><span class="sxs-lookup"><span data-stu-id="245f3-226">Specifies the driver build date.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-227">**DriverInstalled**</span><span class="sxs-lookup"><span data-stu-id="245f3-227">**DriverInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-228">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="245f3-228">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-230">Especifica la fecha y la hora en que se instaló el controlador.</span><span class="sxs-lookup"><span data-stu-id="245f3-230">Specifies the date and time that the driver was installed.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-231">**DriverModelVersion**</span><span class="sxs-lookup"><span data-stu-id="245f3-231">**DriverModelVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245f3-234">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="245f3-234">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="245f3-235">Especifica la versión del modelo de controlador.</span><span class="sxs-lookup"><span data-stu-id="245f3-235">Specifies the driver model version.</span></span>

> [!Note]  
> <span data-ttu-id="245f3-236">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="245f3-236">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="245f3-237">**DriverProvider**</span><span class="sxs-lookup"><span data-stu-id="245f3-237">**DriverProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-238">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245f3-240">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="245f3-240">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="245f3-241">Especifica el nombre del proveedor del controlador.</span><span class="sxs-lookup"><span data-stu-id="245f3-241">Specifies the name of the driver provider.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-242">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="245f3-242">**DriverVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-243">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245f3-245">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="245f3-245">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="245f3-246">Especifica la versión del controlador.</span><span class="sxs-lookup"><span data-stu-id="245f3-246">Specifies the driver version.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-247">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="245f3-247">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-250">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="245f3-250">A display name for the object.</span></span> <span data-ttu-id="245f3-251">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-251">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-252">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="245f3-252">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-253">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-255">Configuración predeterminada o de inicio de un administrador para la propiedad **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="245f3-255">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="245f3-256">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="245f3-256">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-257">**EnabledForVirtualization**</span><span class="sxs-lookup"><span data-stu-id="245f3-257">**EnabledForVirtualization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-258">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="245f3-258">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-260">Especifica si el adaptador se ha habilitado para su uso con RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="245f3-260">Specifies whether the adapter has been enabled for use with RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-261">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="245f3-261">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-262">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-264">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="245f3-264">The enabled and disabled states of an element.</span></span> <span data-ttu-id="245f3-265">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="245f3-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="245f3-266">Value</span><span class="sxs-lookup"><span data-stu-id="245f3-266">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="245f3-267">Significado</span><span class="sxs-lookup"><span data-stu-id="245f3-267">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="245f3-268"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-268"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="245f3-269">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="245f3-269">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="245f3-270"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-270"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="245f3-271"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-271"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="245f3-272">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="245f3-272">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="245f3-273"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-273"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="245f3-274">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="245f3-274">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="245f3-275"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-275"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="245f3-276">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="245f3-276">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="245f3-277"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-277"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="245f3-278">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="245f3-278">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="245f3-279"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-279"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="245f3-280">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="245f3-280">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="245f3-281"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-281"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="245f3-282">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="245f3-282">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="245f3-283"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-283"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="245f3-284">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="245f3-284">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="245f3-285">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-285"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="245f3-286">El elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="245f3-286">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="245f3-287">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="245f3-287">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="245f3-288">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="245f3-288">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="245f3-289"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-289"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="245f3-290">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="245f3-290">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="245f3-291">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="245f3-291">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="245f3-292">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="245f3-292">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-293">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="245f3-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-295">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="245f3-295">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="245f3-296">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-297">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="245f3-297">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-298">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-300">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="245f3-300">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="245f3-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-302">**GPUID**</span><span class="sxs-lookup"><span data-stu-id="245f3-302">**GPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245f3-305">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="245f3-305">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="245f3-306">Contiene el identificador de la GPU para el adaptador.</span><span class="sxs-lookup"><span data-stu-id="245f3-306">Contains the GPU identifier for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-307">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="245f3-307">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-308">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-310">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="245f3-310">The current health of the element.</span></span> <span data-ttu-id="245f3-311">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-312">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="245f3-312">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-313">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="245f3-313">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="245f3-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-315">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="245f3-315">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="245f3-316">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-317">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="245f3-317">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-318">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="245f3-318">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-320">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="245f3-320">The date and time when the object was installed.</span></span> <span data-ttu-id="245f3-321">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="245f3-321">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="245f3-322">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-322">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-323">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="245f3-323">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-324">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-325">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245f3-326">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="245f3-326">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="245f3-327">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="245f3-327">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="245f3-328">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-328">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-329">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="245f3-329">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-330">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="245f3-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-332">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="245f3-332">The last error code reported by the logical device.</span></span> <span data-ttu-id="245f3-333">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-333">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-334">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="245f3-334">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-335">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-337">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="245f3-337">This property has been deprecated.</span></span> <span data-ttu-id="245f3-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-339">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="245f3-339">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-340">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-342">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="245f3-342">The label by which the object is known.</span></span> <span data-ttu-id="245f3-343">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-344">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="245f3-344">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-345">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-347">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="245f3-347">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="245f3-348">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="245f3-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="245f3-349">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="245f3-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="245f3-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="245f3-351"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="245f3-352"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="245f3-353"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="245f3-354"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="245f3-355"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="245f3-356"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="245f3-357"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="245f3-358"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="245f3-359"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="245f3-360"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="245f3-361"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="245f3-362"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="245f3-363"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="245f3-364"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="245f3-365"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="245f3-366"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="245f3-367"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="245f3-368"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="245f3-369">)</span><span class="sxs-lookup"><span data-stu-id="245f3-369">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="245f3-370">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="245f3-370">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-371">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-371">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="245f3-372">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-373">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="245f3-373">The current statuses of the object.</span></span> <span data-ttu-id="245f3-374">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-375">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="245f3-375">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-376">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-377">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-378">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="245f3-378">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="245f3-379">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="245f3-379">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="245f3-380">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="245f3-380">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-381">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="245f3-381">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-382">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="245f3-382">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="245f3-383">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-384">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="245f3-384">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="245f3-385">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-385">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-386">**PixelShaderVersion**</span><span class="sxs-lookup"><span data-stu-id="245f3-386">**PixelShaderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-387">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-388">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245f3-389">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="245f3-389">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="245f3-390">Especifica el versión del sombreador de píxeles Compatible con la GPU.</span><span class="sxs-lookup"><span data-stu-id="245f3-390">Specifies the pixel shader verison that is supported by the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-391">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="245f3-391">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-392">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-392">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="245f3-393">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-394">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="245f3-394">The power management capabilities of the device.</span></span> <span data-ttu-id="245f3-395">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-395">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-396">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="245f3-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-397">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="245f3-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-398">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-399">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="245f3-399">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="245f3-400">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-401">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="245f3-401">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-402">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-402">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-403">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-404">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="245f3-404">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="245f3-405">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-405">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-406">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="245f3-406">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-407">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-407">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-408">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-409">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="245f3-409">Provides high level status information.</span></span> <span data-ttu-id="245f3-410">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="245f3-410">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="245f3-411">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="245f3-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="245f3-412">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="245f3-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="245f3-413"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-414"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="245f3-414"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="245f3-415"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="245f3-416"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="245f3-417"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="245f3-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="245f3-418"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="245f3-419">)</span><span class="sxs-lookup"><span data-stu-id="245f3-419">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="245f3-420">**Rating**</span><span class="sxs-lookup"><span data-stu-id="245f3-420">**Rating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-421">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-422">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="245f3-423">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")</span><span class="sxs-lookup"><span data-stu-id="245f3-423">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="245f3-424">Especifica la clasificación de la GPU RemoteFX para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="245f3-424">Specifies the GPU RemoteFX rating for this device.</span></span> <span data-ttu-id="245f3-425">Esta propiedad no se usa actualmente.</span><span class="sxs-lookup"><span data-stu-id="245f3-425">This property is not currently used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-426">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="245f3-426">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-427">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-429">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="245f3-429">The last requested or desired state for the element.</span></span> <span data-ttu-id="245f3-430">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="245f3-430">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-431">**SharedSystemMemory**</span><span class="sxs-lookup"><span data-stu-id="245f3-431">**SharedSystemMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-432">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-432">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-433">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-434">Especifica la cantidad de memoria del sistema compartida, en bytes, que está disponible para la GPU.</span><span class="sxs-lookup"><span data-stu-id="245f3-434">Specifies the amount of shared system memory, in bytes, that is available to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-435">**Estado**</span><span class="sxs-lookup"><span data-stu-id="245f3-435">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-436">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-438">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="245f3-438">The current status of the object.</span></span> <span data-ttu-id="245f3-439">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-439">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-440">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="245f3-440">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-441">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="245f3-441">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="245f3-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-443">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="245f3-443">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="245f3-444">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="245f3-444">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-445">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="245f3-445">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-446">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-448">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="245f3-448">The current state of the logical device.</span></span> <span data-ttu-id="245f3-449">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-449">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-450">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="245f3-450">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-451">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-453">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="245f3-453">The scoping system's creation class name.</span></span> <span data-ttu-id="245f3-454">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="245f3-454">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-455">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="245f3-455">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-456">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="245f3-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-458">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="245f3-458">The scoping system's name.</span></span> <span data-ttu-id="245f3-459">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="245f3-459">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="245f3-460">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="245f3-460">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-461">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="245f3-461">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-462">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-462">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-463">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="245f3-463">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="245f3-464">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="245f3-464">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-465">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="245f3-465">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-466">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-466">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-467">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-467">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-468">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="245f3-468">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="245f3-469">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="245f3-469">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-470">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="245f3-470">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-471">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="245f3-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-473">Especifica la cantidad total de memoria de vídeo, en bytes, que se encuentra en la GPU.</span><span class="sxs-lookup"><span data-stu-id="245f3-473">Specifies the total amount of video memory, in bytes, present on the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="245f3-474">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="245f3-474">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="245f3-475">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="245f3-475">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="245f3-476">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="245f3-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="245f3-477">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="245f3-477">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="245f3-478">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="245f3-478">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="245f3-479">Requisitos</span><span class="sxs-lookup"><span data-stu-id="245f3-479">Requirements</span></span>



| <span data-ttu-id="245f3-480">Requisito</span><span class="sxs-lookup"><span data-stu-id="245f3-480">Requirement</span></span> | <span data-ttu-id="245f3-481">Value</span><span class="sxs-lookup"><span data-stu-id="245f3-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="245f3-482">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="245f3-482">Minimum supported client</span></span><br/> | <span data-ttu-id="245f3-483">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="245f3-483">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="245f3-484">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="245f3-484">Minimum supported server</span></span><br/> | <span data-ttu-id="245f3-485">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="245f3-485">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="245f3-486">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="245f3-486">Namespace</span></span><br/>                | <span data-ttu-id="245f3-487">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="245f3-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="245f3-488">MOF</span><span class="sxs-lookup"><span data-stu-id="245f3-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="245f3-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="245f3-490">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="245f3-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="245f3-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="245f3-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

