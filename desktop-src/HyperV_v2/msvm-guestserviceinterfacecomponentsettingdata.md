---
description: Representa el estado configurado del componente de la interfaz de servicio de invitado.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Msvm_GuestServiceInterfaceComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666335"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a><span data-ttu-id="01d1d-103">MSVM \_ GuestServiceInterfaceComponentSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="01d1d-103">Msvm\_GuestServiceInterfaceComponentSettingData class</span></span>

<span data-ttu-id="01d1d-104">Representa el estado configurado del componente de la interfaz de servicio de invitado.</span><span class="sxs-lookup"><span data-stu-id="01d1d-104">Represents the configured state of the guest service interface component.</span></span> <span data-ttu-id="01d1d-105">Esta clase se deriva de la [**clase \_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) .</span><span class="sxs-lookup"><span data-stu-id="01d1d-105">This class derives from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class.</span></span>

<span data-ttu-id="01d1d-106">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="01d1d-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d1d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01d1d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
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
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a><span data-ttu-id="01d1d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="01d1d-108">Members</span></span>

<span data-ttu-id="01d1d-109">La clase **MSVM \_ GuestServiceInterfaceComponentSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01d1d-109">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="01d1d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01d1d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01d1d-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01d1d-111">Properties</span></span>

<span data-ttu-id="01d1d-112">La clase **MSVM \_ GuestServiceInterfaceComponentSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01d1d-112">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01d1d-113">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="01d1d-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01d1d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-116">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-116">The address of the resource.</span></span> <span data-ttu-id="01d1d-117">Por ejemplo, la dirección MAC de un puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="01d1d-117">For example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-118">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="01d1d-118">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01d1d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-121">Esta propiedad especifica las unidades de asignación utilizadas por las propiedades de reserva y límite.</span><span class="sxs-lookup"><span data-stu-id="01d1d-121">This property specifies the units of allocation used by the Reservation and Limit properties.</span></span> <span data-ttu-id="01d1d-122">Por ejemplo, si ResourceType = processor, AllocationUnits se puede establecer en MHz.</span><span class="sxs-lookup"><span data-stu-id="01d1d-122">For example, when ResourceType=Processor, AllocationUnits may be set to MHz.</span></span> <span data-ttu-id="01d1d-123">Cuando ResourceType = Memory, AllocationUnits se puede establecer en MB</span><span class="sxs-lookup"><span data-stu-id="01d1d-123">When ResourceType=Memory, AllocationUnits may be set to MB</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-124">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="01d1d-124">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-125">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="01d1d-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-127">Esta propiedad especifica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="01d1d-127">This property specifies if the resource will be automatically allocated.</span></span> <span data-ttu-id="01d1d-128">Por ejemplo, si se establece en true, cuando se enciende el sistema de equipo virtual de consumo, se asignará este recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-128">For example when set to true, when the consuming virtual computer system is powered on, this resource would be allocated.</span></span> <span data-ttu-id="01d1d-129">Un valor de False indica que el recurso debe asignarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="01d1d-129">A value of false indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="01d1d-130">Por ejemplo, la configuración puede representar un medio extraíble (es decir, un CDROM o disquete) en el momento en que se enciende el tiempo, el medio no está presente.</span><span class="sxs-lookup"><span data-stu-id="01d1d-130">For example, the setting may represent removable media (that is, cdrom or floppy) where at power on time, the media is not present.</span></span> <span data-ttu-id="01d1d-131">Se requiere una operación explícita para asignar el recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-131">An explicit operation is required to allocate the resource.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-132">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="01d1d-132">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="01d1d-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-135">Esta propiedad especifica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="01d1d-135">This property specifies if the resource will be automatically deallocated.</span></span> <span data-ttu-id="01d1d-136">Por ejemplo, cuando se establece en true, cuando el sistema de equipo virtual de consumo está apagado, se desasignará este recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-136">For example, when set to true, when the consuming virtual computer system is powered off, this resource would be deallocated.</span></span> <span data-ttu-id="01d1d-137">Cuando se establece en false, el recurso permanecerá asignado y debe desasignarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="01d1d-137">When set to false, the resource will remain allocated and must be explicitly deallocated.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-138">**Connection**</span><span class="sxs-lookup"><span data-stu-id="01d1d-138">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-139">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="01d1d-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-141">Elemento al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-141">The thing to which this resource is connected.</span></span> <span data-ttu-id="01d1d-142">Por ejemplo, una red con nombre o un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="01d1d-142">For example, a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-143">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="01d1d-143">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d1d-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-146">Describe la visibilidad de los consumidores para el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="01d1d-146">Describes the consumers visibility to the allocated resource.</span></span>



| <span data-ttu-id="01d1d-147">Value</span><span class="sxs-lookup"><span data-stu-id="01d1d-147">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="01d1d-148">Significado</span><span class="sxs-lookup"><span data-stu-id="01d1d-148">Meaning</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="01d1d-149"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01d1d-149"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                            | <span data-ttu-id="01d1d-150">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="01d1d-150">Unknown.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <span data-ttu-id="01d1d-151"><dt>**Paso a través**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="01d1d-151"><dt>**Passed-Through**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="01d1d-152">El recurso de host o subyacente se utiliza y pasa al consumidor, posiblemente mediante el uso de particiones.</span><span class="sxs-lookup"><span data-stu-id="01d1d-152">The underlying or host resource is utilized and passed through to the consumer, possibly using partitioning.</span></span> <span data-ttu-id="01d1d-153">Al menos un elemento debe estar presente en la propiedad DeviceID.</span><span class="sxs-lookup"><span data-stu-id="01d1d-153">At least one item shall be present in the DeviceID property.</span></span><br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <span data-ttu-id="01d1d-154"><dt>**Virtualizado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="01d1d-154"><dt>**Virtualized**</dt> <dt>3</dt></span></span> </dl>                            | <span data-ttu-id="01d1d-155">El recurso está virtualizado y no se puede asignar directamente a un recurso de host o subyacente.</span><span class="sxs-lookup"><span data-stu-id="01d1d-155">The resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="01d1d-156">Algunas implementaciones pueden admitir la asignación específica de recursos virtualizados, en cuyo caso los recursos del host se exponen mediante la propiedad DeviceID.</span><span class="sxs-lookup"><span data-stu-id="01d1d-156">Some implementations may support specific assignment for virtualized resources, in which case the host resource(s) are exposed using the DeviceID property.</span></span><br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <span data-ttu-id="01d1d-157"><dt>**No se representa**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="01d1d-157"><dt>**Not represented**</dt> <dt>4</dt></span></span> </dl>            | <span data-ttu-id="01d1d-158">Una representación del recurso no existe en el contexto del consumidor del recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-158">A representation of the resource does not exist within the context of the resource consumer.</span></span><br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="01d1d-159"><dt>**DMTF reservado**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="01d1d-159"><dt>**DMTF reserved**</dt> <dt>..</dt></span></span> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="01d1d-160">El <dt>**proveedor ha reservado**</dt> <dt>32767.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="01d1d-160"><dt>**Vendor Reserved**</dt> <dt>32767..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="01d1d-161">**DefaultEnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="01d1d-161">**DefaultEnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-162">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d1d-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-164">Los Estados habilitado y deshabilitado de los servicios de comunicación de invitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="01d1d-164">The enabled and disabled states of guest communication services by default.</span></span>

<span data-ttu-id="01d1d-165">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="01d1d-165">This is a read-only property, but it can be changed using the [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="01d1d-166">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="01d1d-166">Added in Windows 10.</span></span>

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="01d1d-167">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="01d1d-167">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="01d1d-168">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="01d1d-168">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01d1d-169">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="01d1d-169">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01d1d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-172">Nombre para mostrar de esta instancia de SettingData.</span><span class="sxs-lookup"><span data-stu-id="01d1d-172">The display name for this instance of SettingData.</span></span> <span data-ttu-id="01d1d-173">Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o una consulta.</span><span class="sxs-lookup"><span data-stu-id="01d1d-173">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="01d1d-174">(Nota: el nombre no tiene que ser único dentro de un espacio de nombres).</span><span class="sxs-lookup"><span data-stu-id="01d1d-174">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-175">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="01d1d-175">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-176">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d1d-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-178">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="01d1d-178">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="01d1d-179">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (o [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) en Windows 10 o posterior) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="01d1d-179">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method (or [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 or later) of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="01d1d-180">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="01d1d-180">Valid values are:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="01d1d-181">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="01d1d-181">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="01d1d-182">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="01d1d-182">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01d1d-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="01d1d-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-184">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="01d1d-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-186">Esta propiedad expone una asignación específica a recursos de host o subyacentes.</span><span class="sxs-lookup"><span data-stu-id="01d1d-186">This property exposes specific assignment to host or underlying resources.</span></span> <span data-ttu-id="01d1d-187">Las instancias incrustadas solo contendrán propiedades clave y se tratarán como rutas de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="01d1d-187">The embedded instances shall contain only key properties and be treated as Object Paths.</span></span> <span data-ttu-id="01d1d-188">Si el recurso virtual se puede programar en varios recursos subyacentes, esta propiedad debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="01d1d-188">If the virtual resource may be scheduled on a number of underlying resources, this property should remain **NULL**.</span></span> <span data-ttu-id="01d1d-189">En ese caso, las asociaciones de DeviceAllocatedFromPool o ResourceAllocationFromPool se pueden usar para determinar el grupo de recursos de host en el que se puede programar este recurso virtual.</span><span class="sxs-lookup"><span data-stu-id="01d1d-189">In that case, the DeviceAllocatedFromPool or ResourceAllocationFromPool associations may be used to determine the pool of host resources on which this virtual resource may be scheduled.</span></span> <span data-ttu-id="01d1d-190">Si se utiliza una asignación específica, todos los recursos subyacentes que usa este recurso virtual se enumerarán en esta matriz.</span><span class="sxs-lookup"><span data-stu-id="01d1d-190">If specific assignment is utilized, all underlying resources used by this virtual resource shall be listed in this array.</span></span> <span data-ttu-id="01d1d-191">Normalmente, la matriz contendrá un elemento, pero para las asignaciones de agregado, como varios procesadores, se pueden especificar varios recursos de host.</span><span class="sxs-lookup"><span data-stu-id="01d1d-191">Typically, the array will contain one item, however for aggregate allocations, such as multiple processors, multiple host resources may be specified.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-192">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="01d1d-192">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01d1d-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-195">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="01d1d-195">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-196">Dentro del ámbito del espacio de nombres de la creación de instancias, InstanceID identifica de forma opaca y única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="01d1d-196">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="01d1d-197">Para garantizar la unicidad dentro del espacio de nombres, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido": *OrgID*:*LocalID* donde *orgid* y *LocalID* se separan mediante dos puntos (:), y donde *OrgID* debe incluir un nombre con copyright, marca comercial o de otro tipo que sea propiedad de la entidad empresarial que está creando o definiendo el InstanceID o que es un ID</span><span class="sxs-lookup"><span data-stu-id="01d1d-197">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="01d1d-198">(Este requisito es similar al de *SchemaName* \_ Estructura *className* de los nombres de clase de esquema.) Además, para garantizar la exclusividad, *OrgID* no debe contener dos puntos (:).</span><span class="sxs-lookup"><span data-stu-id="01d1d-198">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="01d1d-199">Al usar este algoritmo, el primer signo de dos puntos que aparece en InstanceID debe aparecer entre *OrgID* y *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="01d1d-199">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="01d1d-200">La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar distintos elementos subyacentes (del mundo real).</span><span class="sxs-lookup"><span data-stu-id="01d1d-200">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="01d1d-201">Si no se usa el algoritmo "preferido" anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceIDs generado por este u otros proveedores para el espacio de nombres de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="01d1d-201">If the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="01d1d-202">En el caso de las instancias definidas por DMTF, el algoritmo "preferido" se debe usar con el valor de *OrgID* establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="01d1d-202">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-203">**Límite**</span><span class="sxs-lookup"><span data-stu-id="01d1d-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-204">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="01d1d-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-206">Esta propiedad especifica el límite superior o la cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="01d1d-206">This property specifies the upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="01d1d-207">Por ejemplo, un sistema que admita la paginación de memoria puede admitir el establecimiento del límite de una asignación de memoria por debajo de la de VirtualQuantity, lo que obliga a que se produzca la paginación para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="01d1d-207">For example, a system which supports memory paging may support setting the Limit of a Memory allocation below that of the VirtualQuantity, thus forcing paging to occur for this allocation.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="01d1d-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-209">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d1d-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-211">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="01d1d-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="01d1d-212">Si la matriz HostResource contiene entradas, esta propiedad refleja el modo en que el recurso se asigna a esos recursos específicos.</span><span class="sxs-lookup"><span data-stu-id="01d1d-212">If the HostResource array contains any entries, this property reflects how the resource maps to those specific resources.</span></span>

<dl> <dt>

<span data-ttu-id="01d1d-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="01d1d-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="01d1d-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (2)</span><span class="sxs-lookup"><span data-stu-id="01d1d-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Afinidad de software** (3)</span><span class="sxs-lookup"><span data-stu-id="01d1d-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (3)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Afinidad fuerte** (4)</span><span class="sxs-lookup"><span data-stu-id="01d1d-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="01d1d-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="01d1d-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="01d1d-220">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="01d1d-220">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01d1d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-223">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y ResourceType tiene el valor "Other".</span><span class="sxs-lookup"><span data-stu-id="01d1d-223">A string that describes the resource type when a well defined value is not available and ResourceType has the value "Other".</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-224">**Parent**</span><span class="sxs-lookup"><span data-stu-id="01d1d-224">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-225">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01d1d-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-227">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-227">The Parent of the resource.</span></span> <span data-ttu-id="01d1d-228">Por ejemplo, un controlador para la asignación actual.</span><span class="sxs-lookup"><span data-stu-id="01d1d-228">For example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-229">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="01d1d-229">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01d1d-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-232">Esta propiedad especifica a qué ResourcePool se asigna actualmente el recurso, o a qué ResourcePool se asignará el recurso cuando se produzca la asignación.</span><span class="sxs-lookup"><span data-stu-id="01d1d-232">This property specifies which ResourcePool the resource is currently allocated from, or which ResourcePool the resource will be allocated from when the allocation occurs.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-233">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="01d1d-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-234">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="01d1d-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-236">Esta propiedad especifica la cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="01d1d-236">This property specifies the amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="01d1d-237">En el sistema que admiten el compromiso excesivo de recursos, este valor se utiliza normalmente para el control de admisión con el fin de evitar que se acepte una asignación, lo que impide el agotamiento de los recursos.</span><span class="sxs-lookup"><span data-stu-id="01d1d-237">On system which support over-commitment of resources, this value is typically used for admission control to prevent an an allocation from being accepted thus preventing resource depletion.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-238">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="01d1d-238">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-239">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="01d1d-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-241">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-241">A string describing an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="01d1d-242">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="01d1d-242">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-243">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="01d1d-243">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-244">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01d1d-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-246">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="01d1d-246">The type of resource this allocation setting represents.</span></span>

<dl> <dt>

<span data-ttu-id="01d1d-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="01d1d-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="01d1d-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="01d1d-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="01d1d-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="01d1d-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="01d1d-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="01d1d-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="01d1d-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="01d1d-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="01d1d-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="01d1d-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="01d1d-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="01d1d-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="01d1d-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="01d1d-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="01d1d-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (17)</span><span class="sxs-lookup"><span data-stu-id="01d1d-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (18)</span><span class="sxs-lookup"><span data-stu-id="01d1d-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controladora USB** (19)</span><span class="sxs-lookup"><span data-stu-id="01d1d-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controladora de gráficos** (20)</span><span class="sxs-lookup"><span data-stu-id="01d1d-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de almacenamiento** (21)</span><span class="sxs-lookup"><span data-stu-id="01d1d-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="01d1d-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Cinta** (23)</span><span class="sxs-lookup"><span data-stu-id="01d1d-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (24)</span><span class="sxs-lookup"><span data-stu-id="01d1d-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controlador Firewire** (25)</span><span class="sxs-lookup"><span data-stu-id="01d1d-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="01d1d-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="01d1d-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fuente de alimentación** (28)</span><span class="sxs-lookup"><span data-stu-id="01d1d-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de refrigeración** (29)</span><span class="sxs-lookup"><span data-stu-id="01d1d-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="01d1d-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="01d1d-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="01d1d-278">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="01d1d-278">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-279">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="01d1d-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-281">Esta propiedad especifica la cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="01d1d-281">This property specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="01d1d-282">Por ejemplo, si ResourceType = procesador, esta propiedad reflejará el número de procesadores discretos que se presentan al sistema del equipo virtual.</span><span class="sxs-lookup"><span data-stu-id="01d1d-282">For example, when ResourceType=Processor, this property would reflect the number of discrete Processors presented to the virtual computer system.</span></span> <span data-ttu-id="01d1d-283">Cuando ResourceType = Memory, esta propiedad podría reflejar el número de MB que se ha comunicado al sistema del equipo virtual.</span><span class="sxs-lookup"><span data-stu-id="01d1d-283">When ResourceType=Memory, this property could reflect the number of MB reported to the virtual computer system.</span></span>

</dd> <dt>

<span data-ttu-id="01d1d-284">**Peso**</span><span class="sxs-lookup"><span data-stu-id="01d1d-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01d1d-285">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="01d1d-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="01d1d-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01d1d-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01d1d-287">Esta propiedad especifica una prioridad relativa para esta asignación en relación con otras asignaciones de la misma ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="01d1d-287">This property specifies a relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="01d1d-288">Esta propiedad no tiene ninguna unidad de medida y solo es relevante en comparación con otras asignaciones que compiten por los mismos recursos de host.</span><span class="sxs-lookup"><span data-stu-id="01d1d-288">This property has no unit of measure, and is only relevant when compared to other allocations competing for the same host resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01d1d-289">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01d1d-289">Requirements</span></span>



| <span data-ttu-id="01d1d-290">Requisito</span><span class="sxs-lookup"><span data-stu-id="01d1d-290">Requirement</span></span> | <span data-ttu-id="01d1d-291">Value</span><span class="sxs-lookup"><span data-stu-id="01d1d-291">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01d1d-292">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01d1d-292">Minimum supported client</span></span><br/> | <span data-ttu-id="01d1d-293">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="01d1d-293">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="01d1d-294">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01d1d-294">Minimum supported server</span></span><br/> | <span data-ttu-id="01d1d-295">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="01d1d-295">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="01d1d-296">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01d1d-296">Namespace</span></span><br/>                | <span data-ttu-id="01d1d-297">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="01d1d-297">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="01d1d-298">MOF</span><span class="sxs-lookup"><span data-stu-id="01d1d-298">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01d1d-299"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01d1d-299"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="01d1d-300">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01d1d-300">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d1d-301"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="01d1d-301"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="01d1d-302">Vea también</span><span class="sxs-lookup"><span data-stu-id="01d1d-302">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d1d-303">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="01d1d-303">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="01d1d-304">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="01d1d-304">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

