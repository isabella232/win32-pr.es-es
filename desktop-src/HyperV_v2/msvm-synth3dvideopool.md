---
description: Contiene información acerca de las unidades de procesamiento de gráficos (GPU) sintéticas de vídeo 3D disponibles en el sistema host.
ms.assetid: 771A42C3-4888-49DF-A389-161A2D0E3DBD
title: Msvm_Synth3dVideoPool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synth3dVideoPool
- Msvm_Synth3dVideoPool.InstanceID
- Msvm_Synth3dVideoPool.Caption
- Msvm_Synth3dVideoPool.Description
- Msvm_Synth3dVideoPool.ElementName
- Msvm_Synth3dVideoPool.InstallDate
- Msvm_Synth3dVideoPool.Name
- Msvm_Synth3dVideoPool.OperationalStatus
- Msvm_Synth3dVideoPool.StatusDescriptions
- Msvm_Synth3dVideoPool.Status
- Msvm_Synth3dVideoPool.HealthState
- Msvm_Synth3dVideoPool.CommunicationStatus
- Msvm_Synth3dVideoPool.DetailedStatus
- Msvm_Synth3dVideoPool.OperatingStatus
- Msvm_Synth3dVideoPool.PrimaryStatus
- Msvm_Synth3dVideoPool.PoolID
- Msvm_Synth3dVideoPool.Primordial
- Msvm_Synth3dVideoPool.Capacity
- Msvm_Synth3dVideoPool.Reserved
- Msvm_Synth3dVideoPool.ResourceType
- Msvm_Synth3dVideoPool.OtherResourceType
- Msvm_Synth3dVideoPool.ResourceSubType
- Msvm_Synth3dVideoPool.AllocationUnits
- Msvm_Synth3dVideoPool.ConsumedResourceUnits
- Msvm_Synth3dVideoPool.CurrentlyConsumedResource
- Msvm_Synth3dVideoPool.MaxConsumableResource
- Msvm_Synth3dVideoPool.Is3dVideoSupported
- Msvm_Synth3dVideoPool.IsSLATCapable
- Msvm_Synth3dVideoPool.IsGPUCapable
- Msvm_Synth3dVideoPool.DirectXVersion
- Msvm_Synth3dVideoPool.RequiredMinimumDirectXVersion
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1afad0f1b2e80a747bb518cb3eafc75d494de62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001613"
---
# <a name="msvm_synth3dvideopool-class"></a><span data-ttu-id="3ff45-103">MSVM \_ Synth3dVideoPool (clase)</span><span class="sxs-lookup"><span data-stu-id="3ff45-103">Msvm\_Synth3dVideoPool class</span></span>

<span data-ttu-id="3ff45-104">Contiene información acerca de las unidades de procesamiento de gráficos (GPU) sintéticas de vídeo 3D disponibles en el sistema host.</span><span class="sxs-lookup"><span data-stu-id="3ff45-104">Contains information about the synthetic 3-D video graphics processing units (GPUs) available on the host system.</span></span> <span data-ttu-id="3ff45-105">Esta clase solo se usa con sistemas host compatibles con RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="3ff45-105">This class is only used with host systems that support RemoteFX.</span></span>

<span data-ttu-id="3ff45-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3ff45-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ff45-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ff45-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synth3dVideoPool : CIM_ResourcePool
{
  string   InstanceID;
  string   Caption = "3D Display Controller Resource Pool";
  string   Description = "Resource pool used to allocate synthetic 3D video controller resources to a virtual machine.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = {"OK"};
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   PoolID;
  boolean  Primordial = True;
  uint64   Capacity;
  uint64   Reserved = 0;
  uint16   ResourceType;
  string   OtherResourceType;
  string   ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
  string   AllocationUnits = "count";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
  boolean  Is3dVideoSupported;
  boolean  IsSLATCapable;
  boolean  IsGPUCapable;
  string   DirectXVersion;
  string   RequiredMinimumDirectXVersion;
};
```

## <a name="members"></a><span data-ttu-id="3ff45-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ff45-108">Members</span></span>

<span data-ttu-id="3ff45-109">La clase **MSVM \_ Synth3dVideoPool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3ff45-109">The **Msvm\_Synth3dVideoPool** class has these types of members:</span></span>

-   [<span data-ttu-id="3ff45-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ff45-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3ff45-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ff45-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3ff45-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ff45-112">Methods</span></span>

<span data-ttu-id="3ff45-113">La clase **MSVM \_ Synth3dVideoPool** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3ff45-113">The **Msvm\_Synth3dVideoPool** class has these methods.</span></span>



| <span data-ttu-id="3ff45-114">Método</span><span class="sxs-lookup"><span data-stu-id="3ff45-114">Method</span></span>                                                                                             | <span data-ttu-id="3ff45-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ff45-115">Description</span></span>                                                                               |
|:---------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ff45-116">**CalculateVideoMemoryRequirements**</span><span class="sxs-lookup"><span data-stu-id="3ff45-116">**CalculateVideoMemoryRequirements**</span></span>](msvm-synth3dvideopool-calculatevideomemoryrequirements.md) | <span data-ttu-id="3ff45-117">Calcula la cantidad de memoria de vídeo necesaria para una máquina virtual de RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="3ff45-117">Calculates the amount of video memory required for a RemoteFX virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3ff45-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ff45-118">Properties</span></span>

<span data-ttu-id="3ff45-119">La clase **MSVM \_ Synth3dVideoPool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3ff45-119">The **Msvm\_Synth3dVideoPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ff45-120">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="3ff45-120">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-123">Las unidades de asignación que usa el grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ff45-123">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="3ff45-124">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff45-124">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-125">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="3ff45-125">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ff45-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-128">Cantidad máxima (en unidades de **AllocationUnits**) de las reservas activas que puede admitir el grupo de recursos de servicio.</span><span class="sxs-lookup"><span data-stu-id="3ff45-128">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="3ff45-129">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff45-129">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3ff45-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-133">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="3ff45-133">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-134">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ff45-134">A short description of the object.</span></span> <span data-ttu-id="3ff45-135">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3ff45-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ff45-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-139">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="3ff45-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3ff45-140">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3ff45-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3ff45-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3ff45-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ff45-142"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="3ff45-143"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="3ff45-144"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="3ff45-145"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="3ff45-146"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ff45-147"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3ff45-148"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3ff45-149">)</span><span class="sxs-lookup"><span data-stu-id="3ff45-149">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ff45-150">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="3ff45-150">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-153">Especifica las unidades para las propiedades **MaxConsumableResource** y **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="3ff45-153">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="3ff45-154">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff45-154">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-155">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="3ff45-155">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-156">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ff45-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-158">Especifica la cantidad de recursos que el grupo de recursos de recurso presenta actualmente a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="3ff45-158">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="3ff45-159">Esta propiedad es diferente de la propiedad **Reserved** en que describe la vista de consumidores del recurso, mientras que la propiedad **Reserved** describe la vista de productores del recurso.</span><span class="sxs-lookup"><span data-stu-id="3ff45-159">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="3ff45-160">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff45-160">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ff45-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-164">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ff45-164">A description of the object.</span></span> <span data-ttu-id="3ff45-165">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-166">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3ff45-166">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ff45-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-169">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="3ff45-169">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3ff45-170">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3ff45-170">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3ff45-171">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-171">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3ff45-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="3ff45-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="3ff45-173"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="3ff45-174"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="3ff45-175"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="3ff45-176"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="3ff45-177"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ff45-178"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3ff45-179"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3ff45-180">)</span><span class="sxs-lookup"><span data-stu-id="3ff45-180">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ff45-181">**DirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="3ff45-181">**DirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-184">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="3ff45-184">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-185">Especifica la versión más antigua de DirectX compatible con las tarjetas del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ff45-185">Specifies the lowest version of DirectX that is supported by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-186">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3ff45-186">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-187">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-189">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ff45-189">A display name for the object.</span></span> <span data-ttu-id="3ff45-190">Esta propiedad permite a cada instancia definir un nombre para mostrar además de las propiedades de clave, los datos de identidad y la información de descripción.</span><span class="sxs-lookup"><span data-stu-id="3ff45-190">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="3ff45-191">La propiedad [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la clase del **\_ ManagedSystemElement de CIM** también se define como un nombre para mostrar, pero a menudo se considera una clave.</span><span class="sxs-lookup"><span data-stu-id="3ff45-191">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name, but it is often subclassed to be a Key.</span></span> <span data-ttu-id="3ff45-192">No es razonable que la misma propiedad pueda transmitir tanto la identidad como un nombre para mostrar, sin incoherencias.</span><span class="sxs-lookup"><span data-stu-id="3ff45-192">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="3ff45-193">Donde [**Name**](msvm-keyboard.md) existe y no es una clave (como en el caso de las instancias de LogicalDevice), la misma información puede estar presente en las propiedades **Name** y **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="3ff45-193">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of LogicalDevice), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="3ff45-194">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-195">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3ff45-195">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-196">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ff45-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-198">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ff45-198">The current health of the element.</span></span> <span data-ttu-id="3ff45-199">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="3ff45-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-200">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3ff45-200">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-201">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ff45-201">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-203">Fecha y hora en que se creó la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ff45-203">The date and time at which the virtual machine was created.</span></span> <span data-ttu-id="3ff45-204">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-205">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3ff45-205">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-208">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3ff45-208">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-209">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="3ff45-209">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3ff45-210">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-211">**Is3dVideoSupported**</span><span class="sxs-lookup"><span data-stu-id="3ff45-211">**Is3dVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-212">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ff45-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-214">Especifica si el sistema host admite el vídeo 3D.</span><span class="sxs-lookup"><span data-stu-id="3ff45-214">Specifies whether 3-D video is supported by the host system.</span></span> <span data-ttu-id="3ff45-215">Contiene un valor distinto de cero si se admite el vídeo 3D, o bien cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3ff45-215">Contains a nonzero value if 3-D video is supported, or zero otherwise.</span></span> <span data-ttu-id="3ff45-216">Para admitir vídeo en 3D, el host de RemoteFX debe tener capacidades de traducción de direcciones de segundo nivel (SLAT) y tener al menos una GPU física que admita RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="3ff45-216">To support 3-D video, the RemoteFX host must have second level address translation (SLAT) capabilities and have at least one physical GPU that supports RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-217">**IsGPUCapable**</span><span class="sxs-lookup"><span data-stu-id="3ff45-217">**IsGPUCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-218">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ff45-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-220">Especifica si el host tiene GPU que admiten RemoteFX y si sus versiones de DirectX cumplen el requisito mínimo.</span><span class="sxs-lookup"><span data-stu-id="3ff45-220">Specifies whether the host has GPUs that support RemoteFX and whether their DirectX versions meet the minimum requirement.</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-221">**IsSLATCapable**</span><span class="sxs-lookup"><span data-stu-id="3ff45-221">**IsSLATCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-222">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ff45-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-224">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")</span><span class="sxs-lookup"><span data-stu-id="3ff45-224">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-225">Especifica si el host tiene una CPU compatible con la traducción de direcciones de segundo nivel (SLAT).</span><span class="sxs-lookup"><span data-stu-id="3ff45-225">Specifies whether the host has a second level address translation (SLAT) capable CPU.</span></span>

> [!Note]  
> <span data-ttu-id="3ff45-226">En desuso en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="3ff45-226">Deprecated in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="3ff45-227">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="3ff45-227">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-228">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ff45-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-230">Especifica la cantidad máxima de recursos consumibles que el grupo de recursos puede presentar a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="3ff45-230">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="3ff45-231">Esta propiedad es diferente de la propiedad **Capacity** en que describe la vista de consumidores del recurso, mientras que la propiedad **Capacity** describe la vista de productores del recurso.</span><span class="sxs-lookup"><span data-stu-id="3ff45-231">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="3ff45-232">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff45-232">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-233">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3ff45-233">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-236">Calificadores: **MaxLen** (1024)</span><span class="sxs-lookup"><span data-stu-id="3ff45-236">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-237">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="3ff45-237">The label by which the object is known.</span></span> <span data-ttu-id="3ff45-238">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="3ff45-238">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="3ff45-239">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-240">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3ff45-240">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-241">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ff45-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-243">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3ff45-243">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3ff45-244">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3ff45-244">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3ff45-245">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3ff45-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ff45-246"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="3ff45-247"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="3ff45-248"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="3ff45-249"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="3ff45-250"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="3ff45-251"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="3ff45-252"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="3ff45-253"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="3ff45-254"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="3ff45-255"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="3ff45-256"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="3ff45-257"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="3ff45-258"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="3ff45-259"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="3ff45-260"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="3ff45-261"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="3ff45-262"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ff45-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3ff45-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3ff45-265">)</span><span class="sxs-lookup"><span data-stu-id="3ff45-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ff45-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3ff45-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-267">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ff45-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-269">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ff45-269">The current status of the element.</span></span> <span data-ttu-id="3ff45-270">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 2 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="3ff45-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span> <span data-ttu-id="3ff45-271">Hyper-V solo usará el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="3ff45-271">Hyper-V will only ever use the first element of this array.</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-272">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="3ff45-272">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-273">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-274">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-275">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorpool.md) está establecido en 0 ("otro").</span><span class="sxs-lookup"><span data-stu-id="3ff45-275">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="3ff45-276">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3ff45-276">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-277">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="3ff45-277">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-280">Las instancias de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que se asignaron desde este grupo hacen referencia a este valor.</span><span class="sxs-lookup"><span data-stu-id="3ff45-280">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="3ff45-281">Esta propiedad se hereda de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))y siempre está establecida en "Microsoft:*GUID* \\ raíz".</span><span class="sxs-lookup"><span data-stu-id="3ff45-281">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-282">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3ff45-282">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-283">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ff45-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-285">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="3ff45-285">Provides high level status information.</span></span> <span data-ttu-id="3ff45-286">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3ff45-286">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3ff45-287">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3ff45-287">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3ff45-288">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ff45-288">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3ff45-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ff45-289"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-290"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="3ff45-290"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="3ff45-291"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="3ff45-292"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ff45-293"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3ff45-294"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3ff45-295">)</span><span class="sxs-lookup"><span data-stu-id="3ff45-295">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ff45-296">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="3ff45-296">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-297">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ff45-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-299">**True** si este grupo de recursos es la base de la que se dibujan y devuelven los recursos en la actividad de administración de recursos; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="3ff45-299">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="3ff45-300">Ser primordial significa que el grupo de recursos no se puede crear o eliminar por los consumidores de este modelo.</span><span class="sxs-lookup"><span data-stu-id="3ff45-300">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="3ff45-301">Sin embargo, otras acciones, modeladas o no, pueden afectar a las características o el tamaño de los grupos de recursos primordiales.</span><span class="sxs-lookup"><span data-stu-id="3ff45-301">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="3ff45-302">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff45-302">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-303">**RequiredMinimumDirectXVersion**</span><span class="sxs-lookup"><span data-stu-id="3ff45-303">**RequiredMinimumDirectXVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-304">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-306">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="3ff45-306">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-307">Especifica la versión más antigua de DirectX necesaria para las tarjetas del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3ff45-307">Specifies the lowest version of DirectX that is required by the cards within the resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-308">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="3ff45-308">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-309">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ff45-309">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-311">Las reservas actuales (en unidades de **AllocationUnits**) se distribuyen entre todas las asignaciones activas de este grupo.</span><span class="sxs-lookup"><span data-stu-id="3ff45-311">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="3ff45-312">En una configuración jerárquica, representa la suma de todas las reservas actuales del grupo de recursos descendientes.</span><span class="sxs-lookup"><span data-stu-id="3ff45-312">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="3ff45-313">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff45-313">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-314">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="3ff45-314">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-315">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-316">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-317">Cadena que describe un subtipo específico de implementación para este grupo.</span><span class="sxs-lookup"><span data-stu-id="3ff45-317">A string that describes an implementation specific subtype for this pool.</span></span> <span data-ttu-id="3ff45-318">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="3ff45-318">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="3ff45-319">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ff45-319">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-320">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3ff45-320">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-321">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ff45-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-323">El tipo de recurso que este grupo de recursos puede asignar.</span><span class="sxs-lookup"><span data-stu-id="3ff45-323">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="3ff45-324">Esta propiedad se hereda de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))y siempre está establecida en 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="3ff45-324">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-325">**Estado**</span><span class="sxs-lookup"><span data-stu-id="3ff45-325">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ff45-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-328">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ff45-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ff45-329">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3ff45-329">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ff45-330">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3ff45-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3ff45-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ff45-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ff45-332">Cadenas que describen los distintos valores de la matriz [**OperationalStatus**](msvm-bioselement.md) .</span><span class="sxs-lookup"><span data-stu-id="3ff45-332">Strings that describe the various [**OperationalStatus**](msvm-bioselement.md) array values.</span></span> <span data-ttu-id="3ff45-333">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".</span><span class="sxs-lookup"><span data-stu-id="3ff45-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span> <span data-ttu-id="3ff45-334">Hyper-V solo usará el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="3ff45-334">Hyper-V will only ever use the first element of this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ff45-335">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ff45-335">Requirements</span></span>



| <span data-ttu-id="3ff45-336">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ff45-336">Requirement</span></span> | <span data-ttu-id="3ff45-337">Value</span><span class="sxs-lookup"><span data-stu-id="3ff45-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff45-338">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ff45-338">Minimum supported client</span></span><br/> | <span data-ttu-id="3ff45-339">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ff45-339">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3ff45-340">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ff45-340">Minimum supported server</span></span><br/> | <span data-ttu-id="3ff45-341">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ff45-341">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ff45-342">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ff45-342">Namespace</span></span><br/>                | <span data-ttu-id="3ff45-343">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3ff45-343">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3ff45-344">MOF</span><span class="sxs-lookup"><span data-stu-id="3ff45-344">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ff45-345"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ff45-345"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ff45-346">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ff45-346">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ff45-347"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ff45-347"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3ff45-348">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ff45-348">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ff45-349">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="3ff45-349">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> </dl>

 

