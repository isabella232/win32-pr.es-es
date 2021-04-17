---
description: Representa la configuración del procesador virtual para una máquina virtual.
ms.assetid: 2B299793-E1CD-49D4-898C-AE60B49F44F5
title: Msvm_ProcessorSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorSettingData
- Msvm_ProcessorSettingData.InstanceID
- Msvm_ProcessorSettingData.Caption
- Msvm_ProcessorSettingData.Description
- Msvm_ProcessorSettingData.ElementName
- Msvm_ProcessorSettingData.ResourceType
- Msvm_ProcessorSettingData.OtherResourceType
- Msvm_ProcessorSettingData.ResourceSubType
- Msvm_ProcessorSettingData.PoolID
- Msvm_ProcessorSettingData.ConsumerVisibility
- Msvm_ProcessorSettingData.HostResource
- Msvm_ProcessorSettingData.AllocationUnits
- Msvm_ProcessorSettingData.VirtualQuantity
- Msvm_ProcessorSettingData.Reservation
- Msvm_ProcessorSettingData.Limit
- Msvm_ProcessorSettingData.Weight
- Msvm_ProcessorSettingData.AutomaticAllocation
- Msvm_ProcessorSettingData.AutomaticDeallocation
- Msvm_ProcessorSettingData.Parent
- Msvm_ProcessorSettingData.Connection
- Msvm_ProcessorSettingData.Address
- Msvm_ProcessorSettingData.MappingBehavior
- Msvm_ProcessorSettingData.AddressOnParent
- Msvm_ProcessorSettingData.VirtualQuantityUnits
- Msvm_ProcessorSettingData.LimitCPUID
- Msvm_ProcessorSettingData.HwThreadsPerCore
- Msvm_ProcessorSettingData.LimitProcessorFeatures
- Msvm_ProcessorSettingData.MaxProcessorsPerNumaNode
- Msvm_ProcessorSettingData.MaxNumaNodesPerSocket
- Msvm_ProcessorSettingData.EnableHostResourceProtection
- Msvm_ProcessorSettingData.CpuGroupId
- Msvm_ProcessorSettingData.HideHypervisorPresent
- Msvm_ProcessorSettingData.ExposeVirtualizationExtensions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5154105c4deab13f93bb65078a5c9527283620e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667559"
---
# <a name="msvm_processorsettingdata-class"></a><span data-ttu-id="2044a-103">MSVM \_ ProcessorSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="2044a-103">Msvm\_ProcessorSettingData class</span></span>

<span data-ttu-id="2044a-104">Representa la configuración del procesador virtual para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-104">Represents the virtual processor settings for a virtual machine.</span></span>

<span data-ttu-id="2044a-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2044a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2044a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2044a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Processor";
  string  Description = "A logical processor of the hypervisor running on the host computer system.";
  string  ElementName;
  uint16  ResourceType = 3;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Processor";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits = "percent / 1000";
  uint64  VirtualQuantity = "count";
  uint64  Reservation = 0;
  uint64  Limit = 100000;
  uint32  Weight = 100;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  boolean LimitCPUID;
  uint64  HwThreadsPerCore;
  boolean LimitProcessorFeatures;
  uint64  MaxProcessorsPerNumaNode;
  uint64  MaxNumaNodesPerSocket;
  boolean EnableHostResourceProtection;
  string  CpuGroupId;
  boolean HideHypervisorPresent;
  boolean ExposeVirtualizationExtensions;
};
```

## <a name="members"></a><span data-ttu-id="2044a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2044a-107">Members</span></span>

<span data-ttu-id="2044a-108">La clase **MSVM \_ ProcessorSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2044a-108">The **Msvm\_ProcessorSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2044a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2044a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2044a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2044a-110">Properties</span></span>

<span data-ttu-id="2044a-111">La clase **MSVM \_ ProcessorSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2044a-111">The **Msvm\_ProcessorSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2044a-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="2044a-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="2044a-115">The address of the resource.</span></span> <span data-ttu-id="2044a-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="2044a-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-120">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="2044a-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="2044a-121">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="2044a-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="2044a-122">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="2044a-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-126">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="2044a-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="2044a-127">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="2044a-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2044a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-131">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2044a-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="2044a-132">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="2044a-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2044a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-136">Indica si el recurso se anulará la asignación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2044a-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="2044a-137">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2044a-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2044a-141">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="2044a-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="2044a-142">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2044a-142">A short description of the object.</span></span> <span data-ttu-id="2044a-143">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2044a-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="2044a-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-145">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2044a-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2044a-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-147">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="2044a-147">The device to which this resource is connected.</span></span> <span data-ttu-id="2044a-148">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="2044a-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2044a-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-152">Describe la visibilidad del consumidor para el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="2044a-152">Describes the consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="2044a-153">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-154">**CpuGroupId**</span><span class="sxs-lookup"><span data-stu-id="2044a-154">**CpuGroupId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-157">El identificador de grupo de CPU al que está enlazada esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-157">The Cpu Group Id this VM is bound to.</span></span> <span data-ttu-id="2044a-158">Cuando el valor es 0 significa que no está enlazado a un grupo de CPU específico.</span><span class="sxs-lookup"><span data-stu-id="2044a-158">When value is 0 it means is not bound to a specific CPU group.</span></span>

> [!Note]  
> <span data-ttu-id="2044a-159">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2044a-159">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2044a-160">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2044a-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-163">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2044a-163">A description of the object.</span></span> <span data-ttu-id="2044a-164">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2044a-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-165">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2044a-165">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-168">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="2044a-168">A display name for the object.</span></span> <span data-ttu-id="2044a-169">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2044a-169">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="2044a-170">Si se cambia esta propiedad, se cambiará el **ElementName** del derivado del dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="2044a-170">Changing this property will change the **ElementName** of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="2044a-171">**EnableHostResourceProtection**</span><span class="sxs-lookup"><span data-stu-id="2044a-171">**EnableHostResourceProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-172">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2044a-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-174">Indica si la máquina virtual debe habilitar características que aumentan la protección de los recursos de host de la carga de trabajo que se ejecuta en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-174">Indicates whether the VM should enable features that increase the protection of host resources from workload running in the VM.</span></span>

> [!Note]  
> <span data-ttu-id="2044a-175">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2044a-175">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="2044a-176">**ExposeVirtualizationExtensions**</span><span class="sxs-lookup"><span data-stu-id="2044a-176">**ExposeVirtualizationExtensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-177">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2044a-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-179">Indica si Hyper-V debe exponer las extensiones de virtualización de hardware virtualizado a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-179">Indicates whether Hyper-V should expose virtualized hardware virtualization extensions to the VM.</span></span>

> [!Note]  
> <span data-ttu-id="2044a-180">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2044a-180">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2044a-181">**HideHypervisorPresent**</span><span class="sxs-lookup"><span data-stu-id="2044a-181">**HideHypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-182">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2044a-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-184">Indica si Hyper-V debe notificar que hay un hipervisor presente en el invitado anidado.</span><span class="sxs-lookup"><span data-stu-id="2044a-184">Indicates whether Hyper-V should report that a hypervisor is present to the nested guest.</span></span>

> [!Note]  
> <span data-ttu-id="2044a-185">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2044a-185">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2044a-186">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="2044a-186">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-187">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2044a-187">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2044a-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-189">Expone una asignación específica para hospedar o los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="2044a-189">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="2044a-190">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="2044a-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2044a-191">**HwThreadsPerCore**</span><span class="sxs-lookup"><span data-stu-id="2044a-191">**HwThreadsPerCore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-192">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2044a-192">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-194">Indica el número de subprocesos de SMT por núcleo que se ha comunicado al invitado.</span><span class="sxs-lookup"><span data-stu-id="2044a-194">Indicates the number of SMT threads per core reported to the guest.</span></span> <span data-ttu-id="2044a-195">Este informe es independiente de si el hardware de SMT está presente.</span><span class="sxs-lookup"><span data-stu-id="2044a-195">This reporting is independent of whether the hardware for SMT is present.</span></span>

> [!Note]  
> <span data-ttu-id="2044a-196">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2044a-196">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="2044a-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2044a-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2044a-200">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="2044a-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2044a-201">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="2044a-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2044a-202">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2044a-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-203">**Límite**</span><span class="sxs-lookup"><span data-stu-id="2044a-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-204">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2044a-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-206">La cantidad máxima de recursos de CPU que puede usar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-206">The maximum amount of CPU resources that may be consumed by the virtual machine.</span></span> <span data-ttu-id="2044a-207">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="2044a-208">100000</span><span class="sxs-lookup"><span data-stu-id="2044a-208">100000</span></span>

<span data-ttu-id="2044a-209">Intervalo: 0 100000</span><span class="sxs-lookup"><span data-stu-id="2044a-209">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="2044a-210">**LimitCPUID**</span><span class="sxs-lookup"><span data-stu-id="2044a-210">**LimitCPUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-211">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2044a-211">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-213">Indica si la máquina virtual debe reducir el identificador de la CPU.</span><span class="sxs-lookup"><span data-stu-id="2044a-213">Indicates whether the virtual machine should lower the CPU identifier.</span></span> <span data-ttu-id="2044a-214">Algunos sistemas operativos anteriores pueden requerir la limitación de la funcionalidad del procesador de esta manera para poder ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="2044a-214">Some older operating systems may require you to limit processor functionality in this way in order to run.</span></span>

</dd> <dt>

<span data-ttu-id="2044a-215">**LimitProcessorFeatures**</span><span class="sxs-lookup"><span data-stu-id="2044a-215">**LimitProcessorFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-216">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2044a-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-218">Indica si la máquina virtual debe limitar las características de CPU que se exponen al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2044a-218">Indicates whether the virtual machine should limit the CPU features exposed to the operating system.</span></span> <span data-ttu-id="2044a-219">Limitar las características del procesador permite migrar la máquina virtual a diferentes sistemas de equipos host con distintos procesadores.</span><span class="sxs-lookup"><span data-stu-id="2044a-219">Limiting the processor features enables the virtual machine to be migrated to different host computer systems with different processors.</span></span> <span data-ttu-id="2044a-220">No se admite la migración de máquinas virtuales entre equipos con procesadores de distintos proveedores.</span><span class="sxs-lookup"><span data-stu-id="2044a-220">Migrating virtual machines between computers with processors from different vendors is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2044a-221">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="2044a-221">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-222">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2044a-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-224">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="2044a-224">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="2044a-225">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-226">**MaxNumaNodesPerSocket**</span><span class="sxs-lookup"><span data-stu-id="2044a-226">**MaxNumaNodesPerSocket**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-227">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2044a-227">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-229">El número máximo de nodos NUMA que se pueden observar dentro de la máquina virtual como pertenecientes a un solo socket de procesador.</span><span class="sxs-lookup"><span data-stu-id="2044a-229">The maximum number of NUMA nodes that can be observed within the virtual machine as belonging to a single processor socket.</span></span>

</dd> <dt>

<span data-ttu-id="2044a-230">**MaxProcessorsPerNumaNode**</span><span class="sxs-lookup"><span data-stu-id="2044a-230">**MaxProcessorsPerNumaNode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-231">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2044a-231">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-233">El número máximo de procesadores virtuales que se pueden observar dentro de la máquina virtual como pertenecientes a un solo nodo NUMA virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-233">The maximum number of virtual processors that can be observed within the virtual machine as belonging to a single virtual NUMA node.</span></span>

</dd> <dt>

<span data-ttu-id="2044a-234">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="2044a-234">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-237">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="2044a-237">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="2044a-238">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-239">**Parent**</span><span class="sxs-lookup"><span data-stu-id="2044a-239">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-242">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="2044a-242">The parent of the resource.</span></span> <span data-ttu-id="2044a-243">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-244">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="2044a-244">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-245">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-247">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="2044a-247">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="2044a-248">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-249">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="2044a-249">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-250">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2044a-250">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-252">La cantidad de recursos de CPU que se reservan para su uso por parte de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-252">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="2044a-253">Se garantiza que estos recursos están disponibles para su consumo por parte de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-253">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="2044a-254">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="2044a-255">0</span><span class="sxs-lookup"><span data-stu-id="2044a-255">0</span></span>

<span data-ttu-id="2044a-256">Intervalo: 0 100000</span><span class="sxs-lookup"><span data-stu-id="2044a-256">Range: 0 100000</span></span>

</dd> <dt>

<span data-ttu-id="2044a-257">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="2044a-257">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-260">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="2044a-260">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="2044a-261">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="2044a-261">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="2044a-262">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-263">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="2044a-263">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-264">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2044a-264">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-266">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="2044a-266">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="2044a-267">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="2044a-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-269">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2044a-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-271">El número total de núcleos de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2044a-271">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="2044a-272">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="2044a-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2044a-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-276">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="2044a-276">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="2044a-277">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2044a-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="2044a-278">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="2044a-279">**Peso**</span><span class="sxs-lookup"><span data-stu-id="2044a-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2044a-280">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2044a-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2044a-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2044a-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2044a-282">El peso de cada procesador de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="2044a-282">The weight for each virtual machine processor.</span></span> <span data-ttu-id="2044a-283">Una vez que se hayan cumplido todas las reservas, la capacidad de procesador físico restante de la plataforma de hospedaje se asignará a las máquinas virtuales en función de sus ponderaciones relativas.</span><span class="sxs-lookup"><span data-stu-id="2044a-283">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="2044a-284">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="2044a-284">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="2044a-285">100</span><span class="sxs-lookup"><span data-stu-id="2044a-285">100</span></span>

<span data-ttu-id="2044a-286">Intervalo: 0 10000</span><span class="sxs-lookup"><span data-stu-id="2044a-286">Range: 0 10000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2044a-287">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2044a-287">Remarks</span></span>

<span data-ttu-id="2044a-288">El acceso a la clase **MSVM \_ ProcessorSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="2044a-288">Access to the **Msvm\_ProcessorSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2044a-289">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2044a-289">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="2044a-290">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2044a-290">Requirements</span></span>



| <span data-ttu-id="2044a-291">Requisito</span><span class="sxs-lookup"><span data-stu-id="2044a-291">Requirement</span></span> | <span data-ttu-id="2044a-292">Value</span><span class="sxs-lookup"><span data-stu-id="2044a-292">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2044a-293">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2044a-293">Minimum supported client</span></span><br/> | <span data-ttu-id="2044a-294">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2044a-294">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2044a-295">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2044a-295">Minimum supported server</span></span><br/> | <span data-ttu-id="2044a-296">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2044a-296">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2044a-297">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2044a-297">Namespace</span></span><br/>                | <span data-ttu-id="2044a-298">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2044a-298">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2044a-299">MOF</span><span class="sxs-lookup"><span data-stu-id="2044a-299">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2044a-300"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2044a-300"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2044a-301">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2044a-301">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2044a-302"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2044a-302"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2044a-303">Vea también</span><span class="sxs-lookup"><span data-stu-id="2044a-303">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2044a-304">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="2044a-304">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="2044a-305">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="2044a-305">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="2044a-306">Clases de procesador</span><span class="sxs-lookup"><span data-stu-id="2044a-306">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

