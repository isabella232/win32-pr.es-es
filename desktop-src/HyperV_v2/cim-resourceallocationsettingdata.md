---
description: Representa la configuración de un recurso asignado que está fuera del ámbito de la clase CIM que se usa normalmente para representar el propio recurso.
ms.assetid: 6261bab9-aa51-479e-bd6a-43c4a9b294a6
title: CIM_ResourceAllocationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationSettingData
- CIM_ResourceAllocationSettingData.ResourceType
- CIM_ResourceAllocationSettingData.OtherResourceType
- CIM_ResourceAllocationSettingData.ResourceSubType
- CIM_ResourceAllocationSettingData.PoolID
- CIM_ResourceAllocationSettingData.ConsumerVisibility
- CIM_ResourceAllocationSettingData.HostResource
- CIM_ResourceAllocationSettingData.AllocationUnits
- CIM_ResourceAllocationSettingData.VirtualQuantity
- CIM_ResourceAllocationSettingData.Reservation
- CIM_ResourceAllocationSettingData.Limit
- CIM_ResourceAllocationSettingData.Weight
- CIM_ResourceAllocationSettingData.AutomaticAllocation
- CIM_ResourceAllocationSettingData.AutomaticDeallocation
- CIM_ResourceAllocationSettingData.Parent
- CIM_ResourceAllocationSettingData.Connection
- CIM_ResourceAllocationSettingData.Address
- CIM_ResourceAllocationSettingData.MappingBehavior
- CIM_ResourceAllocationSettingData.AddressOnParent
- CIM_ResourceAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22289511f454e0d3b128d0e73d32687924c7a7ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687524"
---
# <a name="cim_resourceallocationsettingdata-class"></a><span data-ttu-id="54f92-103">\_Clase ResourceAllocationSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="54f92-103">CIM\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="54f92-104">Representa la configuración de un recurso asignado que está fuera del ámbito de la clase CIM que se usa normalmente para representar el propio recurso.</span><span class="sxs-lookup"><span data-stu-id="54f92-104">Represents settings for an allocated resource that are outside the scope of the CIM class typically used to represent the resource itself.</span></span> <span data-ttu-id="54f92-105">Esta configuración incluye información específica de la asignación que puede que no sea visible para el consumidor del recurso.</span><span class="sxs-lookup"><span data-stu-id="54f92-105">These settings include information specific to the allocation that may not be visible to the consumer of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="54f92-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54f92-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourceAllocationSettingData : CIM_SettingData
{
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
};
```

## <a name="members"></a><span data-ttu-id="54f92-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="54f92-107">Members</span></span>

<span data-ttu-id="54f92-108">La clase **CIM \_ ResourceAllocationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="54f92-108">The **CIM\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="54f92-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54f92-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54f92-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54f92-110">Properties</span></span>

<span data-ttu-id="54f92-111">La clase **CIM \_ ResourceAllocationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="54f92-111">The **CIM\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54f92-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="54f92-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="54f92-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-115">La dirección del recurso, por ejemplo, la dirección MAC de un puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="54f92-115">The address of the resource, for example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-116">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="54f92-116">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="54f92-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-119">Dirección de este recurso desde el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="54f92-119">The address of this resource from the context of the parent.</span></span> <span data-ttu-id="54f92-120">Esta propiedad se usa para describir una relación de controlador y el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="54f92-120">This property is used to describe a controller relationship and the ordering of devices on a controller.</span></span> <span data-ttu-id="54f92-121">Por ejemplo, si el elemento primario es un controlador PCI, esta propiedad especificaría la ranura PCI de este dispositivo secundario.</span><span class="sxs-lookup"><span data-stu-id="54f92-121">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-122">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="54f92-122">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="54f92-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-125">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**Reserva**","**CIM \_ ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="54f92-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**Reservation**", "**CIM\_ResourceAllocationSettingData**.**Limit**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="54f92-126">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="54f92-126">The allocation units used by the **Reservation** and **Limit** properties.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-127">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="54f92-127">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="54f92-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-130">**true** para asignar automáticamente el recurso; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="54f92-130">**true** to automatically allocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-131">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="54f92-131">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-132">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="54f92-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-134">**true** para desasignar automáticamente el recurso; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="54f92-134">**true** to automatically deallocate the resource; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-135">**Connection**</span><span class="sxs-lookup"><span data-stu-id="54f92-135">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-136">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="54f92-136">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="54f92-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-138">Una matriz que indica los objetos conectados al recurso, como una red con nombre o un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="54f92-138">An array that indicates the objects connected to the resource, such as a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-139">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="54f92-139">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f92-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-142">La visibilidad de los consumidores del recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="54f92-142">The consumers visibility to the allocated resource.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54f92-143">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="54f92-143">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

<span data-ttu-id="54f92-144">**Pass-through** (2)</span><span class="sxs-lookup"><span data-stu-id="54f92-144">**Passed-Through** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

<span data-ttu-id="54f92-145">**Virtualizado** (3)</span><span class="sxs-lookup"><span data-stu-id="54f92-145">**Virtualized** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

<span data-ttu-id="54f92-146">**No se representa** (4)</span><span class="sxs-lookup"><span data-stu-id="54f92-146">**Not represented** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54f92-147">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="54f92-147">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54f92-148">**Proveedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="54f92-148">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54f92-149">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="54f92-149">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-150">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="54f92-150">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="54f92-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-152">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ConsumerVisibility**","**\_ ResourceAllocationSettingData CIM**.**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="54f92-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ConsumerVisibility**", "**CIM\_ResourceAllocationSettingData**.**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="54f92-153">Una matriz que contiene la asignación de los recursos asignados.</span><span class="sxs-lookup"><span data-stu-id="54f92-153">An array that contains the assignment of the allocated resources.</span></span> <span data-ttu-id="54f92-154">Cada valor distinto de NULL de esta propiedad debe tener el formato de un URI basado en RFC3986.</span><span class="sxs-lookup"><span data-stu-id="54f92-154">Each non-null value of this property must be formated as an RFC3986 based URI.</span></span> <span data-ttu-id="54f92-155">Si se modela el recurso, el valor debe ser un URI de WBEM.</span><span class="sxs-lookup"><span data-stu-id="54f92-155">If the resource is modeled, then the value should be a WBEM URI.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-156">**Límite**</span><span class="sxs-lookup"><span data-stu-id="54f92-156">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-157">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="54f92-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-159">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")</span><span class="sxs-lookup"><span data-stu-id="54f92-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="54f92-160">Cantidad máxima de recursos que se va a conceder a la asignación.</span><span class="sxs-lookup"><span data-stu-id="54f92-160">The maximum amount of resource to grant to the allocation.</span></span> <span data-ttu-id="54f92-161">El tipo de unidad de esta propiedad se especifica mediante la propiedad **AllocationUnits** .</span><span class="sxs-lookup"><span data-stu-id="54f92-161">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-162">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="54f92-162">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f92-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-165">Indica cómo se asigna el recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="54f92-165">Indicates how the resource maps to underlying resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="54f92-166">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="54f92-166">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="54f92-167">**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="54f92-167">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="54f92-168">**Dedicado** (3)</span><span class="sxs-lookup"><span data-stu-id="54f92-168">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="54f92-169">**Afinidad de software** (4)</span><span class="sxs-lookup"><span data-stu-id="54f92-169">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="54f92-170">**Afinidad fuerte** (5)</span><span class="sxs-lookup"><span data-stu-id="54f92-170">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54f92-171">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="54f92-171">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54f92-172">**Proveedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="54f92-172">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54f92-173">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="54f92-173">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="54f92-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-176">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="54f92-176">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="54f92-177">Una descripción del tipo de recurso cuando la propiedad **resourcetype** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="54f92-177">A description of the resource type when the **ResourceType** property is set to 1 (other).</span></span>

</dd> <dt>

<span data-ttu-id="54f92-178">**Parent**</span><span class="sxs-lookup"><span data-stu-id="54f92-178">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="54f92-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-181">El elemento primario del recurso, por ejemplo, un controlador para la asignación actual.</span><span class="sxs-lookup"><span data-stu-id="54f92-181">The parent of the resource, for example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-182">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="54f92-182">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="54f92-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-185">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolId**")</span><span class="sxs-lookup"><span data-stu-id="54f92-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="54f92-186">IDENTIFICADOR del grupo de recursos que generó el recurso.</span><span class="sxs-lookup"><span data-stu-id="54f92-186">The ID of the resource pool that generated the resource.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-187">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="54f92-187">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-188">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="54f92-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-190">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")</span><span class="sxs-lookup"><span data-stu-id="54f92-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**AllocationUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="54f92-191">El número de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="54f92-191">The number of resource that are guaranteed to be available for this allocation.</span></span> <span data-ttu-id="54f92-192">En los sistemas que admiten el compromiso excesivo de recursos, este valor se utiliza normalmente para el control de admisión.</span><span class="sxs-lookup"><span data-stu-id="54f92-192">On systems that support over-commitment of resources, this value is typically used for admission control.</span></span>

<span data-ttu-id="54f92-193">El tipo de unidad de esta propiedad se especifica mediante la propiedad **AllocationUnits** .</span><span class="sxs-lookup"><span data-stu-id="54f92-193">The unit type of this property is specified by the **AllocationUnits** property.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-194">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="54f92-194">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="54f92-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-197">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="54f92-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="54f92-198">Un subtipo específico de la implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="54f92-198">An implementation specific sub-type for this resource.</span></span> <span data-ttu-id="54f92-199">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="54f92-199">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-200">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="54f92-200">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-201">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54f92-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-203">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**OtherResourceType**","**\_ ResourceAllocationSettingData CIM**.**Subtipo**")</span><span class="sxs-lookup"><span data-stu-id="54f92-203">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**OtherResourceType**", "**CIM\_ResourceAllocationSettingData**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="54f92-204">El tipo de recurso representado por la configuración de asignación.</span><span class="sxs-lookup"><span data-stu-id="54f92-204">The type of resource that is represented by the allocation settings.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="54f92-205">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="54f92-205">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="54f92-206">**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="54f92-206">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="54f92-207">**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="54f92-207">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="54f92-208">**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="54f92-208">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="54f92-209">**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="54f92-209">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="54f92-210">**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="54f92-210">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="54f92-211">**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="54f92-211">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="54f92-212">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="54f92-212">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="54f92-213">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="54f92-213">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="54f92-214">**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="54f92-214">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="54f92-215">**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="54f92-215">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="54f92-216">**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="54f92-216">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="54f92-217">**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="54f92-217">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="54f92-218">**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="54f92-218">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="54f92-219">**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="54f92-219">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="54f92-220">**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="54f92-220">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="54f92-221">**Unidad de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="54f92-221">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="54f92-222">**Unidad de cinta** (18)</span><span class="sxs-lookup"><span data-stu-id="54f92-222">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="54f92-223">**Extensión de almacenamiento** (19)</span><span class="sxs-lookup"><span data-stu-id="54f92-223">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="54f92-224">**Otro dispositivo de almacenamiento** (20)</span><span class="sxs-lookup"><span data-stu-id="54f92-224">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="54f92-225">**Puerto serie** (21)</span><span class="sxs-lookup"><span data-stu-id="54f92-225">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="54f92-226">**Puerto paralelo** (22)</span><span class="sxs-lookup"><span data-stu-id="54f92-226">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="54f92-227">**Controladora USB** (23)</span><span class="sxs-lookup"><span data-stu-id="54f92-227">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="54f92-228">**Controladora de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="54f92-228">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="54f92-229">**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="54f92-229">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="54f92-230">**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="54f92-230">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="54f92-231">**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="54f92-231">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="54f92-232">**Potencia** (28)</span><span class="sxs-lookup"><span data-stu-id="54f92-232">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="54f92-233">**Capacidad de enfriamiento** (29)</span><span class="sxs-lookup"><span data-stu-id="54f92-233">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="54f92-234">**Puerto de conmutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="54f92-234">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="54f92-235">**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="54f92-235">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="54f92-236">**Volumen de almacenamiento** (32)</span><span class="sxs-lookup"><span data-stu-id="54f92-236">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="54f92-237">**Conexión Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="54f92-237">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="54f92-238">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="54f92-238">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="54f92-239">**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="54f92-239">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="54f92-240">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="54f92-240">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-241">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="54f92-241">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-243">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span><span class="sxs-lookup"><span data-stu-id="54f92-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="54f92-244">El número de recursos que se presentan al consumidor del recurso.</span><span class="sxs-lookup"><span data-stu-id="54f92-244">The number of resources presented to the consumer of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-245">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="54f92-245">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-246">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="54f92-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54f92-248">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="54f92-248">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="54f92-249">Unidades utilizadas por la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="54f92-249">The units used by the **VirtualQuantity** property.</span></span>

</dd> <dt>

<span data-ttu-id="54f92-250">**Peso**</span><span class="sxs-lookup"><span data-stu-id="54f92-250">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54f92-251">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="54f92-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="54f92-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="54f92-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54f92-253">Prioridad relativa de esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="54f92-253">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54f92-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54f92-254">Requirements</span></span>



| <span data-ttu-id="54f92-255">Requisito</span><span class="sxs-lookup"><span data-stu-id="54f92-255">Requirement</span></span> | <span data-ttu-id="54f92-256">Value</span><span class="sxs-lookup"><span data-stu-id="54f92-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54f92-257">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54f92-257">Minimum supported client</span></span><br/> | <span data-ttu-id="54f92-258">Windows 8</span><span class="sxs-lookup"><span data-stu-id="54f92-258">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="54f92-259">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54f92-259">Minimum supported server</span></span><br/> | <span data-ttu-id="54f92-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="54f92-260">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="54f92-261">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54f92-261">Namespace</span></span><br/>                | <span data-ttu-id="54f92-262">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="54f92-262">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="54f92-263">MOF</span><span class="sxs-lookup"><span data-stu-id="54f92-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54f92-264"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54f92-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="54f92-265">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54f92-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54f92-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="54f92-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="54f92-267">Vea también</span><span class="sxs-lookup"><span data-stu-id="54f92-267">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f92-268">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="54f92-268">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

