---
description: Representa el estado configurado del componente de virtualización de Escritorio remoto (RDV). El estado predeterminado es habilitado.
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Msvm_RdvComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfc8decda2bf0c505331c9d681069d55f40687f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910145"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a><span data-ttu-id="87387-104">MSVM \_ RdvComponentSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="87387-104">Msvm\_RdvComponentSettingData class</span></span>

<span data-ttu-id="87387-105">Representa el estado configurado del componente de virtualización de Escritorio remoto (RDV).</span><span class="sxs-lookup"><span data-stu-id="87387-105">Represents the configured state of the Remote Desktop Virtualization (RDV) component.</span></span> <span data-ttu-id="87387-106">El estado predeterminado es habilitado.</span><span class="sxs-lookup"><span data-stu-id="87387-106">The default state is Enabled.</span></span>

<span data-ttu-id="87387-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="87387-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="87387-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87387-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a><span data-ttu-id="87387-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="87387-109">Members</span></span>

<span data-ttu-id="87387-110">La clase **MSVM \_ RdvComponentSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="87387-110">The **Msvm\_RdvComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="87387-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="87387-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87387-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="87387-112">Properties</span></span>

<span data-ttu-id="87387-113">La clase **MSVM \_ RdvComponentSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="87387-113">The **Msvm\_RdvComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87387-114">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="87387-114">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-117">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="87387-117">The address of the resource.</span></span> <span data-ttu-id="87387-118">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-118">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="87387-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-122">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="87387-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="87387-123">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="87387-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="87387-124">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="87387-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-128">Unidad de asignación utilizada por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="87387-128">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="87387-129">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="87387-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-131">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="87387-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87387-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-133">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="87387-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="87387-134">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="87387-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-136">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="87387-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87387-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-138">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="87387-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="87387-139">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="87387-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87387-143">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="87387-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="87387-144">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="87387-144">A short description of the object.</span></span> <span data-ttu-id="87387-145">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="87387-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="87387-146">**Connection**</span><span class="sxs-lookup"><span data-stu-id="87387-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-147">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="87387-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87387-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-149">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="87387-149">The device to which this resource is connected.</span></span> <span data-ttu-id="87387-150">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-151">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="87387-151">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-152">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87387-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87387-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-154">Visibilidad del consumidor en el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="87387-154">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="87387-155">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 3 (virtualizado).</span><span class="sxs-lookup"><span data-stu-id="87387-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="87387-156">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87387-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-159">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="87387-159">A description of the object.</span></span> <span data-ttu-id="87387-160">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="87387-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="87387-161">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="87387-161">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-164">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="87387-164">A display name for the object.</span></span> <span data-ttu-id="87387-165">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87387-165">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="87387-166">Al cambiar esta propiedad, se cambiará el nombre del elemento del derivado del dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="87387-166">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="87387-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="87387-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87387-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87387-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-170">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="87387-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="87387-171">Los valores válidos son 2 (habilitado) y 3 (deshabilitado).</span><span class="sxs-lookup"><span data-stu-id="87387-171">Valid values are 2 (enabled) and 3 (disabled).</span></span> <span data-ttu-id="87387-172">El valor predeterminado es 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="87387-172">The default value is 2 (enabled).</span></span> <span data-ttu-id="87387-173">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="87387-173">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="87387-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="87387-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-175">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="87387-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87387-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-177">Solo se puede asignar un recurso de host a cada dispositivo del conmutador virtual, por lo que solo se puede establecer el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="87387-177">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="87387-178">En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="87387-178">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="87387-179">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-179">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-180">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="87387-180">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-181">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87387-183">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="87387-183">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="87387-184">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="87387-184">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="87387-185">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="87387-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="87387-186">**Límite**</span><span class="sxs-lookup"><span data-stu-id="87387-186">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-187">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87387-187">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87387-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-189">La cantidad máxima de recursos de host correspondientes que puede consumir el conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="87387-189">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="87387-190">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-190">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-191">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="87387-191">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-192">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87387-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87387-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-194">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="87387-194">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="87387-195">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-196">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="87387-196">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-199">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="87387-199">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="87387-200">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="87387-200">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="87387-201">**Parent**</span><span class="sxs-lookup"><span data-stu-id="87387-201">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-204">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="87387-204">The parent of the resource.</span></span> <span data-ttu-id="87387-205">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-205">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-206">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="87387-206">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-207">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-209">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="87387-209">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="87387-210">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-210">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-211">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="87387-211">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-212">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87387-212">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87387-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-214">La cantidad de recursos reservados para su uso por el conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="87387-214">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="87387-215">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-215">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-216">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="87387-216">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-219">Cadena que describe un subtipo específico de la implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="87387-219">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="87387-220">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="87387-220">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="87387-221">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="87387-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-223">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87387-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87387-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-225">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="87387-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="87387-226">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 33 (conexión Ethernet).</span><span class="sxs-lookup"><span data-stu-id="87387-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="87387-227">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="87387-227">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-228">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="87387-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="87387-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-230">El número total de puertos en el conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="87387-230">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="87387-231">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-232">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="87387-232">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87387-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87387-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-235">Especifica la unidad de medida para la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="87387-235">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="87387-236">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="87387-236">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="87387-237">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="87387-238">**Peso**</span><span class="sxs-lookup"><span data-stu-id="87387-238">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87387-239">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87387-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87387-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87387-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87387-241">Un entero que define el peso de cada conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="87387-241">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="87387-242">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="87387-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="87387-243">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="87387-243">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87387-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87387-244">Requirements</span></span>



| <span data-ttu-id="87387-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="87387-245">Requirement</span></span> | <span data-ttu-id="87387-246">Value</span><span class="sxs-lookup"><span data-stu-id="87387-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87387-247">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87387-247">Minimum supported client</span></span><br/> | <span data-ttu-id="87387-248">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="87387-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="87387-249">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87387-249">Minimum supported server</span></span><br/> | <span data-ttu-id="87387-250">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="87387-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87387-251">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="87387-251">Namespace</span></span><br/>                | <span data-ttu-id="87387-252">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="87387-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="87387-253">MOF</span><span class="sxs-lookup"><span data-stu-id="87387-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87387-254"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87387-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87387-255">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87387-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87387-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87387-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

