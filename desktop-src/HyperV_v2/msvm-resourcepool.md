---
description: Describe un tipo de recurso virtual disponible para su uso en máquinas virtuales.
ms.assetid: A93D990E-D921-4113-8D88-218D0F84EFA0
title: Msvm_ResourcePool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePool
- Msvm_ResourcePool.InstanceID
- Msvm_ResourcePool.Caption
- Msvm_ResourcePool.Description
- Msvm_ResourcePool.ElementName
- Msvm_ResourcePool.InstallDate
- Msvm_ResourcePool.Name
- Msvm_ResourcePool.OperationalStatus
- Msvm_ResourcePool.StatusDescriptions
- Msvm_ResourcePool.Status
- Msvm_ResourcePool.HealthState
- Msvm_ResourcePool.CommunicationStatus
- Msvm_ResourcePool.DetailedStatus
- Msvm_ResourcePool.OperatingStatus
- Msvm_ResourcePool.PrimaryStatus
- Msvm_ResourcePool.PoolID
- Msvm_ResourcePool.Primordial
- Msvm_ResourcePool.Capacity
- Msvm_ResourcePool.Reserved
- Msvm_ResourcePool.ResourceType
- Msvm_ResourcePool.OtherResourceType
- Msvm_ResourcePool.ResourceSubType
- Msvm_ResourcePool.AllocationUnits
- Msvm_ResourcePool.ConsumedResourceUnits
- Msvm_ResourcePool.CurrentlyConsumedResource
- Msvm_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7c45f67a3e1b7c2b4b5291b24beddcdd4cf5e964
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277380"
---
# <a name="msvm_resourcepool-class"></a><span data-ttu-id="6f134-103">MSVM \_ ResourcePool (clase)</span><span class="sxs-lookup"><span data-stu-id="6f134-103">Msvm\_ResourcePool class</span></span>

<span data-ttu-id="6f134-104">Describe un tipo de recurso virtual disponible para su uso en máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="6f134-104">Describes a type of virtual resource available for use in virtual machines.</span></span> <span data-ttu-id="6f134-105">El grupo de recursos agrega recursos físicos y se usa para asignar recursos a las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="6f134-105">The resource pool aggregates physical resources and is used to allocate resources to virtual machines.</span></span> <span data-ttu-id="6f134-106">En Hyper-V, todos los grupos de recursos son primordiales y hay exactamente un grupo para cada tipo de recurso específico que se puede asignar a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6f134-106">In Hyper-V, all resource pools are primordial, and there is exactly one pool for each specific type of resource which may be allocated to a virtual machine.</span></span>

<span data-ttu-id="6f134-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6f134-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f134-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f134-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePool : CIM_ResourcePool
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

## <a name="members"></a><span data-ttu-id="6f134-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="6f134-109">Members</span></span>

<span data-ttu-id="6f134-110">La clase **MSVM \_ ResourcePool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6f134-110">The **Msvm\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="6f134-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f134-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f134-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f134-112">Properties</span></span>

<span data-ttu-id="6f134-113">La clase **MSVM \_ ResourcePool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6f134-113">The **Msvm\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f134-114">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="6f134-114">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-117">Las unidades de asignación que usa el grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f134-117">The units of allocation used by the resource pool.</span></span> <span data-ttu-id="6f134-118">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))y está establecida en "megabyte".</span><span class="sxs-lookup"><span data-stu-id="6f134-118">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to "Megabyte".</span></span>

</dd> <dt>

<span data-ttu-id="6f134-119">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="6f134-119">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-120">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f134-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-122">Cantidad máxima (en unidades de **AllocationUnits**) de las reservas activas que puede admitir el grupo de recursos de servicio.</span><span class="sxs-lookup"><span data-stu-id="6f134-122">The maximum amount (in units of **AllocationUnits**) of active reservations that the resource pool can support.</span></span> <span data-ttu-id="6f134-123">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6f134-123">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6f134-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-127">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6f134-127">A short description of the object.</span></span> <span data-ttu-id="6f134-128">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="6f134-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f134-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-132">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="6f134-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6f134-133">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6f134-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f134-134">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6f134-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6f134-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="6f134-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="6f134-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="6f134-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="6f134-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6f134-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="6f134-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6f134-142">)</span><span class="sxs-lookup"><span data-stu-id="6f134-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f134-143">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="6f134-143">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-146">Especifica las unidades para las propiedades **MaxConsumableResource** y **CurrentlyConsumedResource** .</span><span class="sxs-lookup"><span data-stu-id="6f134-146">Specifies the units for the **MaxConsumableResource** and the **CurrentlyConsumedResource** properties.</span></span>

</dd> <dt>

<span data-ttu-id="6f134-147">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="6f134-147">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-148">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f134-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-150">Especifica la cantidad de recursos que el grupo de recursos de recurso presenta actualmente a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="6f134-150">Specifies the amount of resource that the resource pool currently presents to consumers.</span></span> <span data-ttu-id="6f134-151">Esta propiedad es diferente de la propiedad **Reserved** en que describe la vista de consumidores del recurso, mientras que la propiedad **Reserved** describe la vista de productores del recurso.</span><span class="sxs-lookup"><span data-stu-id="6f134-151">This property is different from the **Reserved** property in that it describes the consumers view of the resource, while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="6f134-152">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f134-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-155">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6f134-155">A description of the object.</span></span> <span data-ttu-id="6f134-156">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6f134-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-158">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f134-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-160">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="6f134-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6f134-161">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6f134-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f134-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6f134-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="6f134-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="6f134-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="6f134-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="6f134-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="6f134-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="6f134-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6f134-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="6f134-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6f134-171">)</span><span class="sxs-lookup"><span data-stu-id="6f134-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f134-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6f134-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-175">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="6f134-175">A display name for the object.</span></span> <span data-ttu-id="6f134-176">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-177">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6f134-177">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-178">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f134-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-180">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="6f134-180">The current health of the element.</span></span> <span data-ttu-id="6f134-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-182">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6f134-182">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-183">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6f134-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-185">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="6f134-185">The date and time when the object was installed.</span></span> <span data-ttu-id="6f134-186">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="6f134-186">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="6f134-187">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-188">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f134-188">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f134-191">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="6f134-191">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6f134-192">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="6f134-192">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6f134-193">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-194">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="6f134-194">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-195">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f134-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-197">Especifica la cantidad máxima de recursos consumibles que el grupo de recursos puede presentar a los consumidores.</span><span class="sxs-lookup"><span data-stu-id="6f134-197">Specifies the maximum amount of consumable resource that the resource pool can present to consumers.</span></span> <span data-ttu-id="6f134-198">Esta propiedad es diferente de la propiedad **Capacity** en que describe la vista de consumidores del recurso, mientras que la propiedad **Capacity** describe la vista de productores del recurso.</span><span class="sxs-lookup"><span data-stu-id="6f134-198">This property is different from the **Capacity** property in that it describes the consumers view of the resource, while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="6f134-199">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6f134-199">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-202">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="6f134-202">The label by which the object is known.</span></span> <span data-ttu-id="6f134-203">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-204">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="6f134-204">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-205">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f134-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-207">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="6f134-207">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6f134-208">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6f134-208">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f134-209">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6f134-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6f134-210"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="6f134-211"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="6f134-212"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="6f134-213"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="6f134-214"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="6f134-215"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="6f134-216"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="6f134-217"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="6f134-218"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="6f134-219"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="6f134-220"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="6f134-221"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="6f134-222"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="6f134-223"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="6f134-224"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="6f134-225"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="6f134-226"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6f134-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="6f134-228"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6f134-229">)</span><span class="sxs-lookup"><span data-stu-id="6f134-229">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f134-230">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6f134-230">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-231">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f134-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f134-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f134-233">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="6f134-233">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="6f134-234">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="6f134-234">The current statuses of the object.</span></span> <span data-ttu-id="6f134-235">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="6f134-236">Si no se han detectado condiciones relacionadas con QoS, el estado principal (OperationalStatus \[ 0 \] ) se establece en OK (2).</span><span class="sxs-lookup"><span data-stu-id="6f134-236">If no QoS related conditions have been detected, the primary status (OperationalStatus\[0\]) is set to OK (2).</span></span> <span data-ttu-id="6f134-237">De lo contrario, el estado principal se establece en degradado (3) y uno o varios valores de estado secundarios se rellenan en la matriz, empezando por el índice 1, que notifican condiciones más específicas, según esta tabla.</span><span class="sxs-lookup"><span data-stu-id="6f134-237">Otherwise, the primary status is set to Degraded (3), and one or more secondary status values is filled in the array, starting at index 1, which report more specific conditions, according to this table.</span></span>



| <span data-ttu-id="6f134-238">Value</span><span class="sxs-lookup"><span data-stu-id="6f134-238">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="6f134-239">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f134-239">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f134-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Rendimiento insuficiente (32788)</span><span class="sxs-lookup"><span data-stu-id="6f134-240"><span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Insufficient Throughput  (32788)</span></span><br/> | <span data-ttu-id="6f134-241">Al menos uno de los discos virtuales asignados del grupo está notificando actualmente un estado de rendimiento insuficiente.</span><span class="sxs-lookup"><span data-stu-id="6f134-241">At least one of the virtual disks allocated from the pool is currently reporting an  Insufficient Throughput  status.</span></span><br/> |



 

<span data-ttu-id="6f134-242">El proveedor WMI de Hyper-V genera un evento [**MSVM \_ StorageAlert**](msvm-storagealert.md) cada vez que cambia el OperationalStatus de la clase **MSVM \_ ResourcePool** .</span><span class="sxs-lookup"><span data-stu-id="6f134-242">The Hyper-V WMI provider raises an [**Msvm\_StorageAlert**](msvm-storagealert.md) event each time the OperationalStatus of the **Msvm\_ResourcePool** class changes.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6f134-243">**Aceptar** (2)</span><span class="sxs-lookup"><span data-stu-id="6f134-243">**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6f134-244">**Degradado** (3)</span><span class="sxs-lookup"><span data-stu-id="6f134-244">**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="6f134-245">**Error no recuperable** (7)</span><span class="sxs-lookup"><span data-stu-id="6f134-245">**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6f134-246">**Sin contacto** (12)</span><span class="sxs-lookup"><span data-stu-id="6f134-246">**No Contact** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="6f134-247">**Comunicación perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="6f134-247">**Lost Communication** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="6f134-248">El **Protocolo no coincide** (32775)</span><span class="sxs-lookup"><span data-stu-id="6f134-248">**Protocol Mismatch** (32775)</span></span>


</dt> <dd></dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span data-ttu-id="6f134-249">**Rendimiento insuficiente** (32788)</span><span class="sxs-lookup"><span data-stu-id="6f134-249">**Insufficient Throughput** (32788)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6f134-250">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="6f134-250">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-253">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorpool.md) está establecido en 0 ("otro").</span><span class="sxs-lookup"><span data-stu-id="6f134-253">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorpool.md) is set to 0 ("Other").</span></span> <span data-ttu-id="6f134-254">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)) y está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="6f134-254">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)) and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f134-255">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="6f134-255">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-256">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-258">Las instancias de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que se asignaron desde este grupo hacen referencia a este valor.</span><span class="sxs-lookup"><span data-stu-id="6f134-258">This value is referenced by the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) instances which were allocated from this pool.</span></span> <span data-ttu-id="6f134-259">Esta propiedad se hereda de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))y siempre está establecida en "Microsoft:*GUID* \\ raíz".</span><span class="sxs-lookup"><span data-stu-id="6f134-259">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is always set to "Microsoft:*GUID*\\Root".</span></span>

</dd> <dt>

<span data-ttu-id="6f134-260">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="6f134-260">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-261">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f134-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-263">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="6f134-263">Provides high level status information.</span></span> <span data-ttu-id="6f134-264">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="6f134-264">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="6f134-265">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6f134-265">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f134-266">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6f134-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6f134-267"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-268"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="6f134-268"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="6f134-269"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="6f134-270"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6f134-271"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f134-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="6f134-272"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6f134-273">)</span><span class="sxs-lookup"><span data-stu-id="6f134-273">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f134-274">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="6f134-274">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-275">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6f134-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-277">**True** si este grupo de recursos es la base de la que se dibujan y devuelven los recursos en la actividad de administración de recursos; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="6f134-277">**True** if this resource pool is the base from which resources are drawn and returned in the activity of resource management; otherwise, **False**.</span></span> <span data-ttu-id="6f134-278">Ser primordial significa que el grupo de recursos no se puede crear o eliminar por los consumidores de este modelo.</span><span class="sxs-lookup"><span data-stu-id="6f134-278">Being primordial means that this resource pool cannot be created or deleted by consumers of this model.</span></span> <span data-ttu-id="6f134-279">Sin embargo, otras acciones, modeladas o no, pueden afectar a las características o el tamaño de los grupos de recursos primordiales.</span><span class="sxs-lookup"><span data-stu-id="6f134-279">However, other actions, modeled or not, may affect the characteristics or size of primordial resource pools.</span></span> <span data-ttu-id="6f134-280">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6f134-280">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-281">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="6f134-281">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-282">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6f134-282">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-283">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-284">Las reservas actuales (en unidades de **AllocationUnits**) se distribuyen entre todas las asignaciones activas de este grupo.</span><span class="sxs-lookup"><span data-stu-id="6f134-284">The current reservations (in units of **AllocationUnits**) spread across all active allocations from this pool.</span></span> <span data-ttu-id="6f134-285">En una configuración jerárquica, representa la suma de todas las reservas actuales del grupo de recursos descendientes.</span><span class="sxs-lookup"><span data-stu-id="6f134-285">In a hierarchical configuration, this represents the sum of all descendant resource pool current reservations.</span></span> <span data-ttu-id="6f134-286">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6f134-286">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-287">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="6f134-287">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-290">Cadena que describe un subtipo específico de implementación para este grupo.</span><span class="sxs-lookup"><span data-stu-id="6f134-290">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="6f134-291">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="6f134-291">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="6f134-292">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6f134-292">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6f134-293">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="6f134-293">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-294">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6f134-294">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-295">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-296">El tipo de recurso que puede asignar este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f134-296">The type of resource this resource pool may allocate.</span></span> <span data-ttu-id="6f134-297">Esta propiedad se hereda de [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85))y está establecida en 4 ("Memory").</span><span class="sxs-lookup"><span data-stu-id="6f134-297">This property is inherited from [**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85)), and it is set to 4 ("Memory").</span></span>

</dd> <dt>

<span data-ttu-id="6f134-298">**Estado**</span><span class="sxs-lookup"><span data-stu-id="6f134-298">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-299">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6f134-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f134-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-301">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="6f134-301">The current status of the object.</span></span> <span data-ttu-id="6f134-302">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6f134-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6f134-303">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6f134-303">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f134-304">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="6f134-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f134-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f134-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f134-306">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="6f134-306">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6f134-307">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6f134-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f134-308">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f134-308">Remarks</span></span>

<span data-ttu-id="6f134-309">El acceso a la clase **MSVM \_ ResourcePool** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="6f134-309">Access to the **Msvm\_ResourcePool** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6f134-310">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6f134-310">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f134-311">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f134-311">Requirements</span></span>



| <span data-ttu-id="6f134-312">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f134-312">Requirement</span></span> | <span data-ttu-id="6f134-313">Value</span><span class="sxs-lookup"><span data-stu-id="6f134-313">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f134-314">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f134-314">Minimum supported client</span></span><br/> | <span data-ttu-id="6f134-315">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f134-315">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f134-316">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f134-316">Minimum supported server</span></span><br/> | <span data-ttu-id="6f134-317">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f134-317">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f134-318">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6f134-318">Namespace</span></span><br/>                | <span data-ttu-id="6f134-319">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6f134-319">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f134-320">MOF</span><span class="sxs-lookup"><span data-stu-id="6f134-320">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f134-321"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f134-321"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f134-322">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f134-322">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f134-323"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f134-323"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f134-324">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f134-324">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f134-325">**\_RESOURCEPOOL CIM**</span><span class="sxs-lookup"><span data-stu-id="6f134-325">**CIM\_ResourcePool**</span></span>](cim-resourcepool.md)
</dt> <dt>

<span data-ttu-id="6f134-326">[**\_RESOURCEPOOL CIM**](/previous-versions//cc136903(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f134-326">[**CIM\_ResourcePool**](/previous-versions//cc136903(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6f134-327">**MSVM \_ ResourcePool (V1)**</span><span class="sxs-lookup"><span data-stu-id="6f134-327">**Msvm\_ResourcePool (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourcepool)
</dt> <dt>

[<span data-ttu-id="6f134-328">**MSVM \_ StorageAlert**</span><span class="sxs-lookup"><span data-stu-id="6f134-328">**Msvm\_StorageAlert**</span></span>](msvm-storagealert.md)
</dt> <dt>

[<span data-ttu-id="6f134-329">Clases de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="6f134-329">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

