---
description: Representa un grupo de recursos de servidor, que es una entidad lógica proporcionada por el sistema host para asignar y asignar recursos.
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: CIM_ResourcePool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11a073f817da27dbbd45be26a008486a776470cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154540"
---
# <a name="cim_resourcepool-class"></a><span data-ttu-id="60c42-103">\_Clase ResourcePool de CIM</span><span class="sxs-lookup"><span data-stu-id="60c42-103">CIM\_ResourcePool class</span></span>

<span data-ttu-id="60c42-104">Representa un grupo de recursos de servidor, que es una entidad lógica proporcionada por el sistema host para asignar y asignar recursos.</span><span class="sxs-lookup"><span data-stu-id="60c42-104">Represents a resource pool, which is a logical entity provided by the host system to allocate and assign resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60c42-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a><span data-ttu-id="60c42-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="60c42-106">Members</span></span>

<span data-ttu-id="60c42-107">La clase **CIM \_ ResourcePool** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60c42-107">The **CIM\_ResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="60c42-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60c42-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60c42-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60c42-109">Properties</span></span>

<span data-ttu-id="60c42-110">La clase **CIM \_ ResourcePool** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="60c42-110">The **CIM\_ResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60c42-111">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="60c42-111">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c42-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-114">Calificadores: **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="60c42-114">Qualifiers: **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="60c42-115">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="60c42-115">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="60c42-116">Por ejemplo, si **resourcetype** está establecido en "procesador", **AllocationUnits** se puede establecer en "hercios \* 10 ^ 6" o "porcentaje".</span><span class="sxs-lookup"><span data-stu-id="60c42-116">For example, when **ResourceType** is set to "Processor", **AllocationUnits** may be set to "hertz\*10^6" or "percent".</span></span> <span data-ttu-id="60c42-117">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación del Apéndice C. 1 de *DSP0004 v 2.4* o posterior.</span><span class="sxs-lookup"><span data-stu-id="60c42-117">The value of this property should be a legal value of the Programmatic Units qualifier from Appendix C.1 of *DSP0004 V2.4* or later.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-118">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="60c42-118">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-119">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c42-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c42-121">La cantidad máxima de reservas que el grupo de recursos de servicio puede admitir.</span><span class="sxs-lookup"><span data-stu-id="60c42-121">The maximum amount of reservations that the resource pool can support.</span></span> <span data-ttu-id="60c42-122">La propiedad **AllocationUnits** especifica el tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="60c42-122">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-123">**ConsumedResourceUnits**</span><span class="sxs-lookup"><span data-stu-id="60c42-123">**ConsumedResourceUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c42-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-126">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**MaxConsumableResource**","**\_ ResourcePool CIM**.**CurrentlyConsumedResource**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="60c42-126">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**MaxConsumableResource**", "**CIM\_ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="60c42-127">Unidades para las propiedades **MaxConsumable** y **Consumed** .</span><span class="sxs-lookup"><span data-stu-id="60c42-127">The units for the **MaxConsumable** and the **Consumed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-128">**CurrentlyConsumedResource**</span><span class="sxs-lookup"><span data-stu-id="60c42-128">**CurrentlyConsumedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-129">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c42-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-131">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")</span><span class="sxs-lookup"><span data-stu-id="60c42-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="60c42-132">La cantidad de recursos que el grupo de recursos de recurso presenta actualmente a los consumidores de recursos.</span><span class="sxs-lookup"><span data-stu-id="60c42-132">The amount of resource that the resource pool currently presents to resource consumers.</span></span> <span data-ttu-id="60c42-133">Esta propiedad es diferente de la propiedad **reservada** porque describe la vista de consumidores del recurso mientras que la propiedad **reservada** describe la vista de productores del recurso.</span><span class="sxs-lookup"><span data-stu-id="60c42-133">This property is different from the **Reserved** property because it describes the consumers view of the resource while the **Reserved** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="60c42-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c42-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-137">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span><span class="sxs-lookup"><span data-stu-id="60c42-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="60c42-138">Identifica de forma única una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.</span><span class="sxs-lookup"><span data-stu-id="60c42-138">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="60c42-139">Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="60c42-139">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="60c42-140">*OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define la propiedad **InstanceID** , o bien un identificador registrado asignado por una entidad global reconocida.</span><span class="sxs-lookup"><span data-stu-id="60c42-140">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="60c42-141">*OrgID* no debe contener un signo de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="60c42-141">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="60c42-142">Los primeros dos puntos de **InstanceID** deben estar entre el *OrgID* y *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="60c42-142">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="60c42-143">La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.</span><span class="sxs-lookup"><span data-stu-id="60c42-143">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="60c42-144">Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="60c42-144">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="60c42-145">En el caso de las instancias definidas por DMTF, el patrón debe usarse con el valor de *OrgID* establecido en "CIM".</span><span class="sxs-lookup"><span data-stu-id="60c42-145">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> <dt>

<span data-ttu-id="60c42-146">**MaxConsumableResource**</span><span class="sxs-lookup"><span data-stu-id="60c42-146">**MaxConsumableResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-147">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c42-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-149">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")</span><span class="sxs-lookup"><span data-stu-id="60c42-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ConsumedResourceUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="60c42-150">La cantidad máxima de recursos consumibles que el grupo de recursos de recurso puede presentar a los consumidores de recursos.</span><span class="sxs-lookup"><span data-stu-id="60c42-150">The maximum of amount of consumable resources that the resource pool can present to resource consumers.</span></span> <span data-ttu-id="60c42-151">Esta propiedad es diferente de la propiedad **Capacity** porque describe la vista de consumidores del recurso, mientras que la propiedad **Capacity** describe la vista de productores del recurso.</span><span class="sxs-lookup"><span data-stu-id="60c42-151">This property is different from the **Capacity** property because it describes the consumers view of the resource while the **Capacity** property describes the producers view of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-152">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="60c42-152">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c42-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-155">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="60c42-155">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="60c42-156">El tipo de recurso cuando la propiedad **resourcetype** está establecida en "0" (otro).</span><span class="sxs-lookup"><span data-stu-id="60c42-156">The resource type when the **ResourceType** property is set to "0" (other).</span></span>

</dd> <dt>

<span data-ttu-id="60c42-157">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="60c42-157">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c42-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-160">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span><span class="sxs-lookup"><span data-stu-id="60c42-160">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")</span></span>
</dt> </dl>

<span data-ttu-id="60c42-161">Identificador opaco para el grupo.</span><span class="sxs-lookup"><span data-stu-id="60c42-161">An opaque identifier for the pool.</span></span> <span data-ttu-id="60c42-162">Esta propiedad se utiliza para proporcionar correlación al guardar y restaurar los datos de configuración en el almacenamiento persistente subyacente.</span><span class="sxs-lookup"><span data-stu-id="60c42-162">This property is used to provide correlation when saving and restoring configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-163">**Primordial**</span><span class="sxs-lookup"><span data-stu-id="60c42-163">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-164">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="60c42-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c42-166">**true** si el grupo de recursos es primordial.</span><span class="sxs-lookup"><span data-stu-id="60c42-166">**true** if the resource pool is primordial.</span></span> <span data-ttu-id="60c42-167">**false** si el grupo de recursos es un grupo de recursos concreto.</span><span class="sxs-lookup"><span data-stu-id="60c42-167">**false** if the resource pool is a concrete resource pool.</span></span> <span data-ttu-id="60c42-168">Un grupo de recursos primordial es un grupo de recursos que los consumidores del recurso no crean o eliminan.</span><span class="sxs-lookup"><span data-stu-id="60c42-168">A primordial resource pool is a resource pool that is not created or deleted by consumers of the resource.</span></span> <span data-ttu-id="60c42-169">Los servicios de asignación de recursos pueden actualizar un grupo de recursos concreto.</span><span class="sxs-lookup"><span data-stu-id="60c42-169">A concrete resource pool can be updated by resource allocation services.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-170">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="60c42-170">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-171">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="60c42-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60c42-173">Número actual de reservas distribuidas en todas las asignaciones activas de este grupo.</span><span class="sxs-lookup"><span data-stu-id="60c42-173">The current number of reservations spread across all active allocations from this pool.</span></span> <span data-ttu-id="60c42-174">En una configuración jerárquica, representa la suma de todas las reservas descendientes actuales.</span><span class="sxs-lookup"><span data-stu-id="60c42-174">In a hierarchical configuration, this represents the sum of all current descendant reservations.</span></span> <span data-ttu-id="60c42-175">La propiedad **AllocationUnits** especifica el tipo de unidad.</span><span class="sxs-lookup"><span data-stu-id="60c42-175">The **AllocationUnits** property specifies the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-176">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="60c42-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="60c42-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-179">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="60c42-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="60c42-180">Subtipo específico de la implementación para el grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="60c42-180">The implementation specific sub-type for the resource pool.</span></span> <span data-ttu-id="60c42-181">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="60c42-181">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="60c42-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="60c42-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60c42-183">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="60c42-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="60c42-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60c42-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60c42-185">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**OtherResourceType**","**\_ ResourcePool CIM**.**Subtipo**")</span><span class="sxs-lookup"><span data-stu-id="60c42-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ResourcePool**.**OtherResourceType**", "**CIM\_ResourcePool**.**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="60c42-186">El tipo de recurso asignado por el grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60c42-186">The type of resource allocated by the resource pool.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="60c42-187">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="60c42-187">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="60c42-188">**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="60c42-188">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="60c42-189">**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="60c42-189">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="60c42-190">**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="60c42-190">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="60c42-191">**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="60c42-191">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="60c42-192">**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="60c42-192">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="60c42-193">**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="60c42-193">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="60c42-194">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="60c42-194">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="60c42-195">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="60c42-195">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="60c42-196">**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="60c42-196">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="60c42-197">**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="60c42-197">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="60c42-198">**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="60c42-198">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="60c42-199">**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="60c42-199">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="60c42-200">**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="60c42-200">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="60c42-201">**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="60c42-201">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="60c42-202">**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="60c42-202">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="60c42-203">**Unidad de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="60c42-203">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="60c42-204">**Unidad de cinta** (18)</span><span class="sxs-lookup"><span data-stu-id="60c42-204">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="60c42-205">**Extensión de almacenamiento** (19)</span><span class="sxs-lookup"><span data-stu-id="60c42-205">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="60c42-206">**Otro dispositivo de almacenamiento** (20)</span><span class="sxs-lookup"><span data-stu-id="60c42-206">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="60c42-207">**Puerto serie** (21)</span><span class="sxs-lookup"><span data-stu-id="60c42-207">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="60c42-208">**Puerto paralelo** (22)</span><span class="sxs-lookup"><span data-stu-id="60c42-208">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="60c42-209">**Controladora USB** (23)</span><span class="sxs-lookup"><span data-stu-id="60c42-209">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="60c42-210">**Controladora de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="60c42-210">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="60c42-211">**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="60c42-211">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="60c42-212">**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="60c42-212">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="60c42-213">**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="60c42-213">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="60c42-214">**Potencia** (28)</span><span class="sxs-lookup"><span data-stu-id="60c42-214">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="60c42-215">**Capacidad de enfriamiento** (29)</span><span class="sxs-lookup"><span data-stu-id="60c42-215">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="60c42-216">**Puerto de conmutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="60c42-216">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="60c42-217">**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="60c42-217">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="60c42-218">**Volumen de almacenamiento** (32)</span><span class="sxs-lookup"><span data-stu-id="60c42-218">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="60c42-219">**Conexión Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="60c42-219">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="60c42-220">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="60c42-220">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="60c42-221">**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="60c42-221">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="60c42-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="60c42-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="60c42-223">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60c42-223">Requirements</span></span>



| <span data-ttu-id="60c42-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c42-224">Requirement</span></span> | <span data-ttu-id="60c42-225">Value</span><span class="sxs-lookup"><span data-stu-id="60c42-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c42-226">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60c42-226">Minimum supported client</span></span><br/> | <span data-ttu-id="60c42-227">Windows 8</span><span class="sxs-lookup"><span data-stu-id="60c42-227">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="60c42-228">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60c42-228">Minimum supported server</span></span><br/> | <span data-ttu-id="60c42-229">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60c42-229">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="60c42-230">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60c42-230">Namespace</span></span><br/>                | <span data-ttu-id="60c42-231">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="60c42-231">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60c42-232">MOF</span><span class="sxs-lookup"><span data-stu-id="60c42-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60c42-233"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60c42-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60c42-234">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60c42-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c42-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60c42-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60c42-236">Vea también</span><span class="sxs-lookup"><span data-stu-id="60c42-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c42-237">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="60c42-237">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

