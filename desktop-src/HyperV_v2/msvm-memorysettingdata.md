---
description: Representa el estado configurado de la memoria de una máquina virtual.
ms.assetid: 4B6FEE50-1C5F-4F41-B14A-E10B40400A1B
title: Msvm_MemorySettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MemorySettingData
- Msvm_MemorySettingData.InstanceID
- Msvm_MemorySettingData.Caption
- Msvm_MemorySettingData.Description
- Msvm_MemorySettingData.ElementName
- Msvm_MemorySettingData.ResourceType
- Msvm_MemorySettingData.OtherResourceType
- Msvm_MemorySettingData.ResourceSubType
- Msvm_MemorySettingData.PoolID
- Msvm_MemorySettingData.ConsumerVisibility
- Msvm_MemorySettingData.HostResource
- Msvm_MemorySettingData.HugePagesEnabled
- Msvm_MemorySettingData.AllocationUnits
- Msvm_MemorySettingData.VirtualQuantity
- Msvm_MemorySettingData.Reservation
- Msvm_MemorySettingData.Limit
- Msvm_MemorySettingData.Weight
- Msvm_MemorySettingData.AutomaticAllocation
- Msvm_MemorySettingData.AutomaticDeallocation
- Msvm_MemorySettingData.Parent
- Msvm_MemorySettingData.Connection
- Msvm_MemorySettingData.Address
- Msvm_MemorySettingData.MappingBehavior
- Msvm_MemorySettingData.AddressOnParent
- Msvm_MemorySettingData.VirtualQuantityUnits
- Msvm_MemorySettingData.DynamicMemoryEnabled
- Msvm_MemorySettingData.TargetMemoryBuffer
- Msvm_MemorySettingData.IsVirtualized
- Msvm_MemorySettingData.SwapFilesInUse
- Msvm_MemorySettingData.MaxMemoryBlocksPerNumaNode
- Msvm_MemorySettingData.SgxSize
- Msvm_MemorySettingData.SgxEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47309fead7ee45936f34e1e4286ee94437823df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001890"
---
# <a name="msvm_memorysettingdata-class"></a><span data-ttu-id="c9630-103">MSVM \_ MemorySettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="c9630-103">Msvm\_MemorySettingData class</span></span>

<span data-ttu-id="c9630-104">Representa el estado configurado de la memoria de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9630-104">Represents the configured state of the memory for a virtual machine.</span></span>

<span data-ttu-id="c9630-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c9630-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9630-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9630-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MemorySettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Memory Default Settings";
  string  Description = "Describes the default settings for the memory resources.";
  string  ElementName;
  uint16  ResourceType = 4;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Memory";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  boolean HugePagesEnabled;
  string  AllocationUnits = "byte * 2^20";
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "byte * 2^20";
  boolean DynamicMemoryEnabled;
  uint32  TargetMemoryBuffer;
  boolean IsVirtualized = True;
  boolean SwapFilesInUse;
  uint64  MaxMemoryBlocksPerNumaNode;
  uint64  SgxSize;
  boolean SgxEnabled;
};
```

## <a name="members"></a><span data-ttu-id="c9630-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c9630-107">Members</span></span>

<span data-ttu-id="c9630-108">La clase **MSVM \_ MemorySettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c9630-108">The **Msvm\_MemorySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c9630-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9630-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9630-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9630-110">Properties</span></span>

<span data-ttu-id="c9630-111">La clase **MSVM \_ MemorySettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c9630-111">The **Msvm\_MemorySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9630-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="c9630-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-115">The address of the resource.</span></span> <span data-ttu-id="c9630-116">Por ejemplo, la dirección MAC de un puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c9630-116">For example, the MAC address of an Ethernet port.</span></span> <span data-ttu-id="c9630-117">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="c9630-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-121">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="c9630-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="c9630-122">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="c9630-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="c9630-123">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="c9630-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-127">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="c9630-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="c9630-128">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="c9630-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9630-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-132">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c9630-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="c9630-133">Por ejemplo, cuando esta propiedad se establece en **true** y la máquina virtual de consumo se enciende, se asignaría este recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-133">For example, when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="c9630-134">Un valor de **false** indica que el recurso debe asignarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="c9630-134">A value of **False** indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="c9630-135">Por ejemplo, la configuración puede representar un medio extraíble (como un CD-ROM o un disquete) en el inicio, el medio no está presente.</span><span class="sxs-lookup"><span data-stu-id="c9630-135">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="c9630-136">Se requiere una operación explícita para asignar el recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-136">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="c9630-137">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-138">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="c9630-138">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9630-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-141">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c9630-141">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="c9630-142">Por ejemplo, si esta propiedad se establece en **true** y la máquina virtual de consumo está encendida, se asignará este recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-142">For example when this property is set to **True** and the consuming virtual machine is powered on, this resource would be allocated.</span></span> <span data-ttu-id="c9630-143">Cuando esta propiedad es **false**, el recurso debe asignarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="c9630-143">When this property is **False**, the resource must be explicitly allocated.</span></span> <span data-ttu-id="c9630-144">Por ejemplo, la configuración puede representar un medio extraíble (como un CD-ROM o un disquete) en el inicio, el medio no está presente.</span><span class="sxs-lookup"><span data-stu-id="c9630-144">For example, the setting may represent removable media (such as a CD-ROM or a floppy disk) where at startup, the media is not present.</span></span> <span data-ttu-id="c9630-145">Se requiere una operación explícita para asignar el recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-145">An explicit operation is required to allocate the resource.</span></span> <span data-ttu-id="c9630-146">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c9630-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9630-150">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="c9630-150">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="c9630-151">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9630-151">A short description of the object.</span></span> <span data-ttu-id="c9630-152">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9630-152">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-153">**Connection**</span><span class="sxs-lookup"><span data-stu-id="c9630-153">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-154">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c9630-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9630-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-156">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-156">The device to which this resource is connected.</span></span> <span data-ttu-id="c9630-157">Por ejemplo, una red con nombre o un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="c9630-157">For example, a named network or switch port.</span></span> <span data-ttu-id="c9630-158">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-158">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="c9630-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-160">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9630-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-162">Describe la visibilidad de los consumidores para el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="c9630-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="c9630-163">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-164">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9630-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-167">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9630-167">A description of the object.</span></span> <span data-ttu-id="c9630-168">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9630-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-169">**DynamicMemoryEnabled**</span><span class="sxs-lookup"><span data-stu-id="c9630-169">**DynamicMemoryEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-170">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9630-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-172">Indica si la memoria dinámica está habilitada para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9630-172">Indicates whether dynamic memory is enabled for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c9630-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c9630-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-176">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9630-176">A display name for the object.</span></span> <span data-ttu-id="c9630-177">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9630-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-178">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="c9630-178">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-179">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c9630-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9630-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-181">El primer elemento de esta matriz contiene una referencia al recurso de host subyacente que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="c9630-181">The first element of this array contains a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="c9630-182">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="c9630-182">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but it is not used.</span></span>

</dd> <dt>
  
<span data-ttu-id="c9630-183">**HugePagesEnabled**</span><span class="sxs-lookup"><span data-stu-id="c9630-183">**HugePagesEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9630-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-186">Si la memoria está respaldada por 1 GB de páginas o no.</span><span class="sxs-lookup"><span data-stu-id="c9630-186">Whether the memory is backed by 1GB pages or not.</span></span>

</dd> <dt>

<span data-ttu-id="c9630-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c9630-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9630-190">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="c9630-190">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c9630-191">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c9630-191">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c9630-192">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9630-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-193">**IsVirtualized**</span><span class="sxs-lookup"><span data-stu-id="c9630-193">**IsVirtualized**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-194">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9630-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-196">Indica si este dispositivo se ha virtualizado o se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="c9630-196">Indicates whether this device is virtualized or passed through.</span></span> <span data-ttu-id="c9630-197">Cuando se establece en **false**, se utiliza el recurso de host o subyacente.</span><span class="sxs-lookup"><span data-stu-id="c9630-197">When set to **False**, the underlying or host resource is used.</span></span> <span data-ttu-id="c9630-198">Debe haber al menos un elemento presente en la propiedad **DeviceID** .</span><span class="sxs-lookup"><span data-stu-id="c9630-198">At least one item should be present in the **DeviceID** property.</span></span> <span data-ttu-id="c9630-199">Cuando se establece en **true**, el recurso se virtualiza y es posible que no se asigne directamente a un recurso de host o subyacente.</span><span class="sxs-lookup"><span data-stu-id="c9630-199">When set to **True**, the resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="c9630-200">Algunas implementaciones pueden admitir la asignación específica de recursos virtualizados, en cuyo caso los recursos del host se exponen mediante la propiedad **DeviceID** .</span><span class="sxs-lookup"><span data-stu-id="c9630-200">Some implementations may support specific assignment for virtualized resources, in which case the host resources are exposed by using the **DeviceID** property.</span></span> <span data-ttu-id="c9630-201">Esta propiedad siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="c9630-201">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="c9630-202">**Límite**</span><span class="sxs-lookup"><span data-stu-id="c9630-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-203">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9630-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-205">Cantidad máxima de memoria que puede consumir la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9630-205">The maximum amount of memory that may be consumed by the virtual machine.</span></span> <span data-ttu-id="c9630-206">En el caso de una máquina virtual con memoria dinámica habilitada, representa la configuración de memoria máxima.</span><span class="sxs-lookup"><span data-stu-id="c9630-206">For a virtual machine with dynamic memory enabled, this represents the maximum memory setting.</span></span> <span data-ttu-id="c9630-207">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="c9630-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-209">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9630-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-211">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="c9630-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="c9630-212">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-213">**MaxMemoryBlocksPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="c9630-213">**MaxMemoryBlocksPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-214">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9630-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-216">La cantidad máxima de memoria que se puede observar dentro de la máquina virtual como perteneciente a un solo nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="c9630-216">The maximum amount of memory that can be observed within the virtual machine as belonging to a single NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="c9630-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="c9630-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-220">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor "Other".</span><span class="sxs-lookup"><span data-stu-id="c9630-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="c9630-221">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-222">**Parent**</span><span class="sxs-lookup"><span data-stu-id="c9630-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-225">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-225">The parent of the resource.</span></span> <span data-ttu-id="c9630-226">Por ejemplo, un controlador para la asignación actual.</span><span class="sxs-lookup"><span data-stu-id="c9630-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="c9630-227">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-228">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="c9630-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-231">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-231">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="c9630-232">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-233">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="c9630-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-234">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9630-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-236">Especifica la cantidad de memoria garantizada que estará disponible para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9630-236">Specifies the amount of memory guaranteed to be available for this virtual machine.</span></span> <span data-ttu-id="c9630-237">En el caso de una máquina virtual con memoria dinámica habilitada, representa la configuración de memoria mínima.</span><span class="sxs-lookup"><span data-stu-id="c9630-237">For a virtual machine with dynamic memory enabled, this represents the minimum memory setting.</span></span> <span data-ttu-id="c9630-238">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-239">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="c9630-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-242">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="c9630-243">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c9630-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="c9630-244">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c9630-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-246">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9630-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-248">Tipo de recurso que representa esta configuración de asignación.</span><span class="sxs-lookup"><span data-stu-id="c9630-248">The type of resource that this allocation setting represents.</span></span> <span data-ttu-id="c9630-249">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 4 (memoria).</span><span class="sxs-lookup"><span data-stu-id="c9630-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 4 (Memory).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-250">**SgxEnabled**</span><span class="sxs-lookup"><span data-stu-id="c9630-250">**SgxEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-251">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9630-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-253">Indica si SGX está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c9630-253">Indicates if SGX is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="c9630-254">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c9630-254">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="c9630-255">**SgxSize**</span><span class="sxs-lookup"><span data-stu-id="c9630-255">**SgxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-256">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9630-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-258">Cantidad de memoria SGX que se va a asignar a la máquina virtual, en MB.</span><span class="sxs-lookup"><span data-stu-id="c9630-258">The amount of SGX memory to allocate for the VM, in MB.</span></span>

> [!Note]  
> <span data-ttu-id="c9630-259">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c9630-259">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="c9630-260">**SwapFilesInUse**</span><span class="sxs-lookup"><span data-stu-id="c9630-260">**SwapFilesInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-261">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9630-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-263">**True** si la paginación de segundo nivel está activa; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c9630-263">**True** if second level paging is active; otherwise, **False**.</span></span>

</dd> <dt>

<span data-ttu-id="c9630-264">**TargetMemoryBuffer**</span><span class="sxs-lookup"><span data-stu-id="c9630-264">**TargetMemoryBuffer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-265">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9630-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-267">Define la cantidad de memoria adicional que se debe reservar para una máquina virtual en tiempo de ejecución, como un porcentaje de la memoria total que se considera que la máquina virtual necesita.</span><span class="sxs-lookup"><span data-stu-id="c9630-267">Defines the amount of extra memory that should be reserved for a virtual machine at runtime, as a percentage of the total memory that the virtual machine is thought to need.</span></span> <span data-ttu-id="c9630-268">Esto solo se aplica a las máquinas virtuales con memoria dinámica habilitada.</span><span class="sxs-lookup"><span data-stu-id="c9630-268">This only applies to virtual machines with dynamic memory enabled.</span></span>

<span data-ttu-id="c9630-269">Esta propiedad puede estar en el intervalo comprendido entre 5 y 2000.</span><span class="sxs-lookup"><span data-stu-id="c9630-269">This property can be in the range of 5 to 2000.</span></span>

</dd> <dt>

<span data-ttu-id="c9630-270">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="c9630-270">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-271">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9630-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-273">La cantidad total de memoria RAM de la máquina virtual, tal como la detecta el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="c9630-273">The total amount of RAM in the virtual machine, as seen by the guest operating system.</span></span> <span data-ttu-id="c9630-274">En el caso de una máquina virtual con memoria dinámica habilitada, esta representa la memoria inicial disponible en el inicio.</span><span class="sxs-lookup"><span data-stu-id="c9630-274">For a virtual machine with dynamic memory enabled, this represents the initial memory available at startup.</span></span> <span data-ttu-id="c9630-275">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-276">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="c9630-276">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-277">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9630-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-279">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9630-279">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="c9630-280">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c9630-280">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="c9630-281">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9630-282">**Peso**</span><span class="sxs-lookup"><span data-stu-id="c9630-282">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9630-283">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9630-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9630-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9630-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9630-285">Define el valor de ponderación de la asignación de memoria para cada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9630-285">Defines the memory allocation weighting value for each virtual machine.</span></span> <span data-ttu-id="c9630-286">Una vez que se hayan cumplido todas las reservas, la memoria restante de la plataforma de hospedaje se asignará a las máquinas virtuales en función de sus pesos relativos (no superar el valor especificado por la propiedad **Limit** ).</span><span class="sxs-lookup"><span data-stu-id="c9630-286">After all reserves have been met, the remaining memory of the hosting platform will be allocated to virtual machines based on their relative weights (not to exceed the value specified by the **Limit** property).</span></span> <span data-ttu-id="c9630-287">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9630-287">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9630-288">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c9630-288">Remarks</span></span>

<span data-ttu-id="c9630-289">El acceso a la clase **MSVM \_ MemorySettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="c9630-289">Access to the **Msvm\_MemorySettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c9630-290">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c9630-290">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="c9630-291">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c9630-291">Examples</span></span>

```powershell
function WaitForResult
{
  param($result)
  if ($result.ReturnValue -eq 4096)
  {
    while($true)
    {
      $result.Job
      if ($result.Job -ne $null)
      {
        if ($result.Job.JobState -gt 4)
        {
          return $result.Job.ErrorCode
        }
      }
      start-sleep 1
    }
  }
  else
  {
    return $result.ReturnValue
  }
}

if ($($args.count) -ne 2)
{
  Write-Host "EnableHugePages.ps1 VMName SizeInMB"
  return
}

$vmName = $args[0]
$sizeInMB = $args[1]
 
$namespace = "root\virtualization\v2"
$vm = Get-WmiObject -class MSVM_ComputerSystem -filter "ElementName='$vmName'" -namespace $namespace
$settings = Get-WmiObject -query "Associators of {$vm} where ResultClass = Msvm_VirtualSystemSettingData" -namespace $namespace
$vmSettings = $settings | ? VirtualSystemType -eq "Microsoft:Hyper-V:System:Realized"
$memorySettings = Get-WmiObject -query "Associators of {$vmSettings} where ResultClass = Msvm_MemorySettingData" -namespace $namespace

$memorySettings.MaxMemoryBlocksPerNumaNode = $sizeInMB
$memorySettings.Reservation = $sizeInMB
$memorySettings.Limit = $sizeInMB
$memorySettings.VirtualQuantity = $sizeInMB
$memorySettings.HugePagesEnabled = $True

$vmSvc = Get-WmiObject -class Msvm_VirtualSystemManagementService -namespace $namespace
$res = $vmSvc.ModifyResourceSettings($memorySettings.GetText(2))
if (WaitForResult($res) -ne 0)
{
  Write-Host "Failed."
}
```

## <a name="requirements"></a><span data-ttu-id="c9630-292">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9630-292">Requirements</span></span>



| <span data-ttu-id="c9630-293">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9630-293">Requirement</span></span> | <span data-ttu-id="c9630-294">Value</span><span class="sxs-lookup"><span data-stu-id="c9630-294">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9630-295">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9630-295">Minimum supported client</span></span><br/> | <span data-ttu-id="c9630-296">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9630-296">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c9630-297">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9630-297">Minimum supported server</span></span><br/> | <span data-ttu-id="c9630-298">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9630-298">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9630-299">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9630-299">Namespace</span></span><br/>                | <span data-ttu-id="c9630-300">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c9630-300">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c9630-301">MOF</span><span class="sxs-lookup"><span data-stu-id="c9630-301">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9630-302"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9630-302"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9630-303">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9630-303">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9630-304"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9630-304"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c9630-305">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9630-305">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9630-306">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c9630-306">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="c9630-307">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c9630-307">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="c9630-308">Clases de memoria</span><span class="sxs-lookup"><span data-stu-id="c9630-308">Memory Classes</span></span>](memory-classes.md)
</dt> </dl>

 

