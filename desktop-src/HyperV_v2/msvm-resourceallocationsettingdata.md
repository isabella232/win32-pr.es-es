---
description: Representa los Estados de asignación actuales y registrados de un recurso virtual.
ms.assetid: 5C180933-2013-4E16-A9BD-653D5426F468
title: Msvm_ResourceAllocationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationSettingData
- Msvm_ResourceAllocationSettingData.InstanceID
- Msvm_ResourceAllocationSettingData.Caption
- Msvm_ResourceAllocationSettingData.Description
- Msvm_ResourceAllocationSettingData.ElementName
- Msvm_ResourceAllocationSettingData.ResourceType
- Msvm_ResourceAllocationSettingData.OtherResourceType
- Msvm_ResourceAllocationSettingData.ResourceSubType
- Msvm_ResourceAllocationSettingData.PoolID
- Msvm_ResourceAllocationSettingData.ConsumerVisibility
- Msvm_ResourceAllocationSettingData.HostResource
- Msvm_ResourceAllocationSettingData.AllocationUnits
- Msvm_ResourceAllocationSettingData.VirtualQuantity
- Msvm_ResourceAllocationSettingData.Reservation
- Msvm_ResourceAllocationSettingData.Limit
- Msvm_ResourceAllocationSettingData.Weight
- Msvm_ResourceAllocationSettingData.AutomaticAllocation
- Msvm_ResourceAllocationSettingData.AutomaticDeallocation
- Msvm_ResourceAllocationSettingData.Parent
- Msvm_ResourceAllocationSettingData.Connection
- Msvm_ResourceAllocationSettingData.Address
- Msvm_ResourceAllocationSettingData.MappingBehavior
- Msvm_ResourceAllocationSettingData.AddressOnParent
- Msvm_ResourceAllocationSettingData.VirtualQuantityUnits
- Msvm_ResourceAllocationSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6d1cb2f97dcb3fa144db5cf27c1a82690214b11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360809"
---
# <a name="msvm_resourceallocationsettingdata-class"></a><span data-ttu-id="ff352-103">MSVM \_ ResourceAllocationSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="ff352-103">Msvm\_ResourceAllocationSettingData class</span></span>

<span data-ttu-id="ff352-104">Representa los Estados de asignación actuales y registrados de un recurso virtual.</span><span class="sxs-lookup"><span data-stu-id="ff352-104">Represents the current and recorded allocation states of a virtual resource.</span></span>

<span data-ttu-id="ff352-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ff352-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff352-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff352-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption;
  string  Description;
  string  ElementName;
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
  string  VirtualSystemIdentifiers[] = { "GUID" };
};
```

## <a name="members"></a><span data-ttu-id="ff352-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff352-107">Members</span></span>

<span data-ttu-id="ff352-108">La clase **MSVM \_ ResourceAllocationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ff352-108">The **Msvm\_ResourceAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="ff352-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff352-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff352-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff352-110">Properties</span></span>

<span data-ttu-id="ff352-111">La clase **MSVM \_ ResourceAllocationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ff352-111">The **Msvm\_ResourceAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff352-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="ff352-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="ff352-115">The address of the resource.</span></span> <span data-ttu-id="ff352-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ff352-117">Se trata de una propiedad de solo lectura, pero si la propiedad **resourcetype** es 20 (controladora de gráficos), se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ff352-117">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ff352-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="ff352-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-121">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="ff352-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="ff352-122">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="ff352-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="ff352-123">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="ff352-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-127">Unidad de asignación utilizada por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="ff352-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="ff352-128">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="ff352-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ff352-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-132">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ff352-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="ff352-133">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="ff352-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ff352-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-137">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ff352-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="ff352-138">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ff352-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff352-142">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ff352-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ff352-143">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ff352-143">A short description of the object.</span></span> <span data-ttu-id="ff352-144">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ff352-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-145">**Connection**</span><span class="sxs-lookup"><span data-stu-id="ff352-145">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-146">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ff352-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ff352-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-148">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="ff352-148">The device to which this resource is connected.</span></span> <span data-ttu-id="ff352-149">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-149">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ff352-150">Se trata de una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff352-150">This is a read-only property.</span></span> <span data-ttu-id="ff352-151">Pero si la propiedad **resourcetype** es 21 (puerto serie) y la **propiedad subtipo** es "Microsoft: Hyper-V: Serial Port", la propiedad de **conexión** se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ff352-151">But if the **ResourceType** property is 21 (Serial port) and the **ResourceSubType** property is "Microsoft:Hyper-V:Serial Port", the **Connection** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ff352-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="ff352-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff352-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-155">Visibilidad del consumidor en el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="ff352-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="ff352-156">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ff352-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-160">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ff352-160">A description of the object.</span></span> <span data-ttu-id="ff352-161">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ff352-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ff352-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-165">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="ff352-165">A display name for the object.</span></span> <span data-ttu-id="ff352-166">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ff352-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="ff352-167">Al cambiar esta propiedad, se cambiará el nombre del elemento del derivado del dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="ff352-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="ff352-168">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ff352-168">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ff352-169">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="ff352-169">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-170">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ff352-170">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ff352-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-172">Solo se puede asignar un recurso de host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="ff352-172">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="ff352-173">En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="ff352-173">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="ff352-174">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-174">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ff352-175">Se trata de una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ff352-175">This is a read-only property.</span></span> <span data-ttu-id="ff352-176">Pero si la propiedad **resourcetype** es 17 (Disk) y la propiedad **subtipo** es "Microsoft: Hyper-V: Physical Disk Drive", se puede cambiar la propiedad **HostResource** mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ff352-176">But if the **ResourceType** property is 17 (Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Physical Disk Drive", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ff352-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ff352-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff352-180">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="ff352-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ff352-181">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ff352-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ff352-182">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="ff352-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="ff352-183">**Límite**</span><span class="sxs-lookup"><span data-stu-id="ff352-183">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-184">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ff352-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-186">La cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="ff352-186">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="ff352-187">La unidad de medida para esta propiedad se especifica mediante la propiedad **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="ff352-187">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="ff352-188">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-189">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="ff352-189">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-190">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff352-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-192">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="ff352-192">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="ff352-193">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-194">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="ff352-194">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-197">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="ff352-197">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="ff352-198">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-198">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-199">**Parent**</span><span class="sxs-lookup"><span data-stu-id="ff352-199">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-202">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="ff352-202">The parent of the resource.</span></span> <span data-ttu-id="ff352-203">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-203">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-204">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="ff352-204">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-205">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-207">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="ff352-207">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="ff352-208">En el caso de las instancias asociadas a una máquina virtual, será "Microsoft:*GUID* \\ *específico del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="ff352-208">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="ff352-209">En el caso de las instancias que definen valores posibles para una máquina virtual, será "Microsoft: Definition \\ *GUID* \\ *Type*", donde el *tipo* puede ser "Maximum", "Minimum", "default" o "Increment".</span><span class="sxs-lookup"><span data-stu-id="ff352-209">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="ff352-210">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-211">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="ff352-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-212">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ff352-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-214">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="ff352-214">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="ff352-215">La unidad de medida para esta propiedad se especifica mediante la propiedad **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="ff352-215">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="ff352-216">Se garantiza que estos recursos están disponibles para su consumo por parte de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff352-216">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="ff352-217">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-218">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="ff352-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-221">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="ff352-221">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="ff352-222">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="ff352-222">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="ff352-223">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-223">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-224">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="ff352-224">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-225">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ff352-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-227">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="ff352-227">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="ff352-228">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-228">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="ff352-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="ff352-229"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="ff352-230"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="ff352-231"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="ff352-232"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="ff352-233"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="ff352-234"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="ff352-235"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="ff352-236"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="ff352-237"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="ff352-238"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="ff352-239"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="ff352-240"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="ff352-241"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="ff352-242"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="ff352-243"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="ff352-244"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidad de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="ff352-245"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidad de cinta** (18)</span><span class="sxs-lookup"><span data-stu-id="ff352-246"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de almacenamiento** (19)</span><span class="sxs-lookup"><span data-stu-id="ff352-247"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (20)</span><span class="sxs-lookup"><span data-stu-id="ff352-248"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (21)</span><span class="sxs-lookup"><span data-stu-id="ff352-249"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (22)</span><span class="sxs-lookup"><span data-stu-id="ff352-250"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controladora USB** (23)</span><span class="sxs-lookup"><span data-stu-id="ff352-251"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controladora de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="ff352-252"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="ff352-253"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="ff352-254"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="ff352-255"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fuente de alimentación** (28)</span><span class="sxs-lookup"><span data-stu-id="ff352-256"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de refrigeración** (29)</span><span class="sxs-lookup"><span data-stu-id="ff352-257"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Puerto de conmutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="ff352-258"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="ff352-259"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volumen de almacenamiento** (32)</span><span class="sxs-lookup"><span data-stu-id="ff352-260"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexión Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="ff352-261"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="ff352-262"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="ff352-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="ff352-263"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ff352-264">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="ff352-264">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-265">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ff352-265">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-266">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-267">Especifica la cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="ff352-267">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="ff352-268">La unidad de medida para esta propiedad se especifica mediante la propiedad **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="ff352-268">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="ff352-269">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-269">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-270">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="ff352-270">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-271">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ff352-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-272">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-273">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="ff352-273">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="ff352-274">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ff352-274">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="ff352-275">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="ff352-276">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="ff352-276">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-277">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ff352-277">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ff352-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff352-279">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="ff352-279">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="ff352-280">Matriz de cadenas de identificadores de este recurso que se presenta al sistema operativo de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff352-280">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="ff352-281">Estos valores se usan solo si la propiedad **resourcetype** está establecida en 6 (HBA SCSI paralelo) y la propiedad **subtipo** se establece en "controlador SCSI de Microsoft sintético".</span><span class="sxs-lookup"><span data-stu-id="ff352-281">These values are used only if the **ResourceType** property is set to 6 (Parallel SCSI HBA) and the **ResourceSubType** property is set to "Microsoft Synthetic SCSI Controller".</span></span> <span data-ttu-id="ff352-282">Esta propiedad se establece en "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="ff352-282">This property is set to "*GUID*".</span></span>

<span data-ttu-id="ff352-283">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ff352-283">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="ff352-284">**Peso**</span><span class="sxs-lookup"><span data-stu-id="ff352-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff352-285">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff352-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ff352-286">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff352-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff352-287">Un entero que define el peso relativo de cada procesador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff352-287">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="ff352-288">Una vez que se hayan cumplido todas las reservas, la capacidad de procesador físico restante de la plataforma de hospedaje se asignará a las máquinas virtuales en función de sus ponderaciones relativas.</span><span class="sxs-lookup"><span data-stu-id="ff352-288">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="ff352-289">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="ff352-289">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="ff352-290">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="ff352-290">Range: 0 1000</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff352-291">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff352-291">Remarks</span></span>

<span data-ttu-id="ff352-292">El acceso a la clase **MSVM \_ ResourceAllocationSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="ff352-292">Access to the **Msvm\_ResourceAllocationSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ff352-293">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ff352-293">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff352-294">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff352-294">Requirements</span></span>



| <span data-ttu-id="ff352-295">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff352-295">Requirement</span></span> | <span data-ttu-id="ff352-296">Value</span><span class="sxs-lookup"><span data-stu-id="ff352-296">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff352-297">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff352-297">Minimum supported client</span></span><br/> | <span data-ttu-id="ff352-298">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff352-298">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ff352-299">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff352-299">Minimum supported server</span></span><br/> | <span data-ttu-id="ff352-300">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff352-300">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff352-301">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ff352-301">Namespace</span></span><br/>                | <span data-ttu-id="ff352-302">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ff352-302">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ff352-303">MOF</span><span class="sxs-lookup"><span data-stu-id="ff352-303">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff352-304"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff352-304"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff352-305">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff352-305">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff352-306"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff352-306"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ff352-307">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff352-307">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff352-308">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ff352-308">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="ff352-309">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="ff352-309">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="ff352-310">**MSVM \_ ResourceAllocationSettingData (V1)**</span><span class="sxs-lookup"><span data-stu-id="ff352-310">**Msvm\_ResourceAllocationSettingData (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="ff352-311">Clases de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="ff352-311">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

