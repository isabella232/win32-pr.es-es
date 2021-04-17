---
description: Agrega los recursos del procesador que se pueden asignar a una máquina virtual.
ms.assetid: 73424568-fa6c-4ed8-9640-a67a6d2829f0
title: Msvm_ProcessorPool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool
- Msvm_ProcessorPool.InstanceID
- Msvm_ProcessorPool.Caption
- Msvm_ProcessorPool.Description
- Msvm_ProcessorPool.ElementName
- Msvm_ProcessorPool.InstallDate
- Msvm_ProcessorPool.Name
- Msvm_ProcessorPool.OperationalStatus
- Msvm_ProcessorPool.StatusDescriptions
- Msvm_ProcessorPool.Status
- Msvm_ProcessorPool.HealthState
- Msvm_ProcessorPool.CommunicationStatus
- Msvm_ProcessorPool.DetailedStatus
- Msvm_ProcessorPool.OperatingStatus
- Msvm_ProcessorPool.PrimaryStatus
- Msvm_ProcessorPool.PoolID
- Msvm_ProcessorPool.Primordial
- Msvm_ProcessorPool.Capacity
- Msvm_ProcessorPool.Reserved
- Msvm_ProcessorPool.ResourceType
- Msvm_ProcessorPool.OtherResourceType
- Msvm_ProcessorPool.ResourceSubType
- Msvm_ProcessorPool.AllocationUnits
- Msvm_ProcessorPool.ConsumedResourceUnits
- Msvm_ProcessorPool.CurrentlyConsumedResource
- Msvm_ProcessorPool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 93927483c23147fd387e24cdc5a550a1771457cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687639"
---
# <a name="msvm_processorpool-class"></a><span data-ttu-id="c731d-103">MSVM \_ ProcessorPool (clase)</span><span class="sxs-lookup"><span data-stu-id="c731d-103">Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="c731d-104">Agrega los recursos del procesador que se pueden asignar a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c731d-104">Aggregates the processor resources that may be allocated to a virtual machine.</span></span>

<span data-ttu-id="c731d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c731d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c731d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c731d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorPool : CIM_ResourcePool
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
  string   PoolID = "Microsoft:GUID\Root";
  boolean  Primordial = False;
  uint64   Capacity;
  uint64   Reserved;
  uint16   ResourceType = 4;
  string   OtherResourceType;
  string   ResourceSubType;
  string   AllocationUnits = "Megabyte";
  string   ConsumedResourceUnits = "count";
  uint64   CurrentlyConsumedResource;
  uint64   MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="c731d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c731d-107">Members</span></span>

<span data-ttu-id="c731d-108">La clase **MSVM \_ ProcessorPool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c731d-108">The **Msvm\_ProcessorPool** class has these types of members:</span></span>

-   [<span data-ttu-id="c731d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c731d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c731d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c731d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c731d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c731d-111">Methods</span></span>

<span data-ttu-id="c731d-112">La clase **MSVM \_ ProcessorPool** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c731d-112">The **Msvm\_ProcessorPool** class has these methods.</span></span>



| <span data-ttu-id="c731d-113">Método</span><span class="sxs-lookup"><span data-stu-id="c731d-113">Method</span></span>                                                                          | <span data-ttu-id="c731d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c731d-114">Description</span></span>                                           |
|:--------------------------------------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="c731d-115">**CalculatePossibleReserve**</span><span class="sxs-lookup"><span data-stu-id="c731d-115">**CalculatePossibleReserve**</span></span>](calculatepossiblereserve-msvm-processorpool.md) | <span data-ttu-id="c731d-116">Se usa para buscar la reserva real del procesador.</span><span class="sxs-lookup"><span data-stu-id="c731d-116">Used to find the actual processor reserve.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c731d-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c731d-117">Properties</span></span>

<span data-ttu-id="c731d-118">La clase **MSVM \_ ProcessorPool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c731d-118">The **Msvm\_ProcessorPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c731d-119">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="c731d-119">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-122">Las unidades de asignación que usa el grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c731d-122">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="c731d-123">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))y está establecida en "megabyte".</span><span class="sxs-lookup"><span data-stu-id="c731d-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="c731d-124">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="c731d-124">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-125">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c731d-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-127">Cantidad máxima (en unidades de **AllocationUnits**) de las reservas activas que puede admitir el grupo de recursos de servicio.</span><span class="sxs-lookup"><span data-stu-id="c731d-127">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="c731d-128">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c731d-128">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-129">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c731d-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-132">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c731d-132">A short description of the object.</span></span> <span data-ttu-id="c731d-133">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-134">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c731d-134">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c731d-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-137">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="c731d-137">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c731d-138">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c731d-138">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c731d-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-139">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c731d-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c731d-140"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="c731d-141"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="c731d-142"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="c731d-143"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="c731d-144"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c731d-145"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="c731d-146"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c731d-147">)</span><span class="sxs-lookup"><span data-stu-id="c731d-147">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c731d-148">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="c731d-148">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-151">Especifica las unidades para las propiedades **MaxConsumableResource** y **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="c731d-151">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span> <span data-ttu-id="c731d-152">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c731d-152">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-153">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="c731d-153">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-154">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c731d-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-156">Especifica la cantidad de recursos que el grupo de recursos de recurso presenta actualmente a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="c731d-156">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="c731d-157">Esta propiedad es diferente de la propiedad **Reserved** en que describe la vista de consumidores del recurso, mientras que la propiedad **Reserved** describe la vista de productores del recurso.</span><span class="sxs-lookup"><span data-stu-id="c731d-157">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span> <span data-ttu-id="c731d-158">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c731d-158">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-159">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c731d-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-162">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c731d-162">A description of the object.</span></span> <span data-ttu-id="c731d-163">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-164">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c731d-164">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c731d-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-167">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="c731d-167">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c731d-168">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c731d-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c731d-169">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c731d-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="c731d-170"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="c731d-171"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="c731d-172"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="c731d-173"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="c731d-174"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="c731d-175"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c731d-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="c731d-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c731d-178">)</span><span class="sxs-lookup"><span data-stu-id="c731d-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c731d-179">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c731d-179">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-182">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="c731d-182">A display name for the object.</span></span> <span data-ttu-id="c731d-183">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-184">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c731d-184">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-185">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c731d-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-187">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="c731d-187">The current health of the element.</span></span> <span data-ttu-id="c731d-188">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-189">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c731d-189">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-190">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c731d-190">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-192">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c731d-192">The date and time when the object was installed.</span></span> <span data-ttu-id="c731d-193">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="c731d-193">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="c731d-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-195">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c731d-195">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c731d-198">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="c731d-198">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c731d-199">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c731d-199">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c731d-200">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-201">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="c731d-201">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-202">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c731d-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-204">Especifica la cantidad máxima de recursos consumibles que el grupo de recursos puede presentar a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="c731d-204">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="c731d-205">Esta propiedad es diferente de la propiedad **Capacity** en que describe la vista de consumidores del recurso, mientras que la propiedad **Capacity** describe la vista de productores del recurso.</span><span class="sxs-lookup"><span data-stu-id="c731d-205">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span> <span data-ttu-id="c731d-206">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c731d-206">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-207">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c731d-207">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-210">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c731d-210">The label by which the object is known.</span></span> <span data-ttu-id="c731d-211">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-212">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c731d-212">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-213">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c731d-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-215">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c731d-215">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c731d-216">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c731d-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c731d-217">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c731d-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c731d-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="c731d-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="c731d-220"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="c731d-221"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="c731d-222"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="c731d-223"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="c731d-224"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="c731d-225"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="c731d-226"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="c731d-227"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="c731d-228"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="c731d-229"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="c731d-230"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="c731d-231"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="c731d-232"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="c731d-233"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="c731d-234"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c731d-235"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="c731d-236"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c731d-237">)</span><span class="sxs-lookup"><span data-stu-id="c731d-237">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c731d-238">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c731d-238">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-239">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c731d-239">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c731d-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-241">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="c731d-241">The current statuses of the object.</span></span> <span data-ttu-id="c731d-242">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-242">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-243">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="c731d-243">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-244">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-246">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** está establecido en 0 ("otro").</span><span class="sxs-lookup"><span data-stu-id="c731d-246">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to 0 ("Other").</span></span> <span data-ttu-id="c731d-247">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="c731d-247">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c731d-248">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="c731d-248">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-249">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-251">Las instancias de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que se asignaron desde este grupo hacen referencia a este valor.</span><span class="sxs-lookup"><span data-stu-id="c731d-251">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="c731d-252">Esta propiedad se hereda de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))y siempre está establecida en "Microsoft:*GUID* \\ raíz".</span><span class="sxs-lookup"><span data-stu-id="c731d-252">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="c731d-253">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c731d-253">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-254">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c731d-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-256">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="c731d-256">Provides high level status information.</span></span> <span data-ttu-id="c731d-257">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="c731d-257">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c731d-258">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="c731d-258">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c731d-259">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c731d-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="c731d-260"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-261"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="c731d-261"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="c731d-262"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="c731d-263"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c731d-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c731d-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="c731d-265"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c731d-266">)</span><span class="sxs-lookup"><span data-stu-id="c731d-266">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c731d-267">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="c731d-267">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-268">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c731d-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-270">**True** si este grupo de recursos es la base de la que se dibujan y devuelven los recursos en la actividad de administración de recursos; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c731d-270">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="c731d-271">Ser primordial significa que el grupo de recursos no se puede crear o eliminar por los consumidores de este modelo.</span><span class="sxs-lookup"><span data-stu-id="c731d-271">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="c731d-272">Sin embargo, otras acciones, modeladas o no, pueden afectar a las características o el tamaño de los grupos de recursos primordiales.</span><span class="sxs-lookup"><span data-stu-id="c731d-272">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="c731d-273">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c731d-273">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-274">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c731d-274">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-275">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c731d-275">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-277">Las reservas actuales (en unidades de **AllocationUnits**) se distribuyen entre todas las asignaciones activas de este grupo.</span><span class="sxs-lookup"><span data-stu-id="c731d-277">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="c731d-278">En una configuración jerárquica, representa la suma de todas las reservas actuales del grupo de recursos descendientes.</span><span class="sxs-lookup"><span data-stu-id="c731d-278">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="c731d-279">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c731d-279">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-280">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="c731d-280">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-283">Cadena que describe un subtipo específico de implementación para este grupo.</span><span class="sxs-lookup"><span data-stu-id="c731d-283">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="c731d-284">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c731d-284">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="c731d-285">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c731d-285">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c731d-286">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c731d-286">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-287">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c731d-287">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-288">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-289">El tipo de recurso que puede asignar este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c731d-289">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="c731d-290">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))y está establecida en 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="c731d-290">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="c731d-291">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c731d-291">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-292">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c731d-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c731d-293">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-294">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c731d-294">The current status of the object.</span></span> <span data-ttu-id="c731d-295">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="c731d-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c731d-296">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c731d-296">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c731d-297">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c731d-297">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c731d-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c731d-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c731d-299">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c731d-299">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c731d-300">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c731d-300">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c731d-301">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c731d-301">Remarks</span></span>

<span data-ttu-id="c731d-302">El acceso a la clase **MSVM \_ ProcessorPool** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="c731d-302">Access to the **Msvm\_ProcessorPool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c731d-303">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c731d-303">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c731d-304">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c731d-304">Requirements</span></span>



| <span data-ttu-id="c731d-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="c731d-305">Requirement</span></span> | <span data-ttu-id="c731d-306">Value</span><span class="sxs-lookup"><span data-stu-id="c731d-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c731d-307">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c731d-307">Minimum supported client</span></span><br/> | <span data-ttu-id="c731d-308">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c731d-308">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c731d-309">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c731d-309">Minimum supported server</span></span><br/> | <span data-ttu-id="c731d-310">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c731d-310">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c731d-311">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c731d-311">Namespace</span></span><br/>                | <span data-ttu-id="c731d-312">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c731d-312">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c731d-313">MOF</span><span class="sxs-lookup"><span data-stu-id="c731d-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c731d-314"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c731d-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c731d-315">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c731d-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c731d-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c731d-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c731d-317">Vea también</span><span class="sxs-lookup"><span data-stu-id="c731d-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c731d-318">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="c731d-318">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="c731d-319">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c731d-319">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c731d-320">Clases de procesador</span><span class="sxs-lookup"><span data-stu-id="c731d-320">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

