---
description: Representa el estado configurado de un puerto de Canal de fibra sintético.
ms.assetid: 5d47dd80-de34-4ae4-a300-c16da1cd4974
title: Msvm_SyntheticFcPortSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPortSettingData
- Msvm_SyntheticFcPortSettingData.InstanceID
- Msvm_SyntheticFcPortSettingData.Caption
- Msvm_SyntheticFcPortSettingData.Description
- Msvm_SyntheticFcPortSettingData.ElementName
- Msvm_SyntheticFcPortSettingData.ResourceType
- Msvm_SyntheticFcPortSettingData.OtherResourceType
- Msvm_SyntheticFcPortSettingData.ResourceSubType
- Msvm_SyntheticFcPortSettingData.PoolID
- Msvm_SyntheticFcPortSettingData.ConsumerVisibility
- Msvm_SyntheticFcPortSettingData.HostResource
- Msvm_SyntheticFcPortSettingData.AllocationUnits
- Msvm_SyntheticFcPortSettingData.VirtualQuantity
- Msvm_SyntheticFcPortSettingData.Reservation
- Msvm_SyntheticFcPortSettingData.Limit
- Msvm_SyntheticFcPortSettingData.Weight
- Msvm_SyntheticFcPortSettingData.AutomaticAllocation
- Msvm_SyntheticFcPortSettingData.AutomaticDeallocation
- Msvm_SyntheticFcPortSettingData.Parent
- Msvm_SyntheticFcPortSettingData.Connection
- Msvm_SyntheticFcPortSettingData.Address
- Msvm_SyntheticFcPortSettingData.MappingBehavior
- Msvm_SyntheticFcPortSettingData.AddressOnParent
- Msvm_SyntheticFcPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticFcPortSettingData.VirtualPortWWPN
- Msvm_SyntheticFcPortSettingData.VirtualPortWWNN
- Msvm_SyntheticFcPortSettingData.SecondaryWWPN
- Msvm_SyntheticFcPortSettingData.SecondaryWWNN
- Msvm_SyntheticFcPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticFcPortSettingData.ChapEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdd0342f5429f5314f5c744a3a760101dbaa043b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808798"
---
# <a name="msvm_syntheticfcportsettingdata-class"></a><span data-ttu-id="c9a2d-103">MSVM \_ SyntheticFcPortSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="c9a2d-103">Msvm\_SyntheticFcPortSettingData class</span></span>

<span data-ttu-id="c9a2d-104">Representa el estado configurado de un puerto de Canal de fibra sintético.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-104">Represents the configured state of a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="c9a2d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a2d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9a2d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPortSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel Port Default Settings";
  string  Description = "Describes the default settings for the virtual Fibre Channel port resources.";
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
  string  VirtualPortWWPN;
  string  VirtualPortWWNN;
  string  SecondaryWWPN;
  string  SecondaryWWNN;
  string  VirtualSystemIdentifiers[];
  boolean ChapEnabled;
};
```

## <a name="members"></a><span data-ttu-id="c9a2d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c9a2d-107">Members</span></span>

<span data-ttu-id="c9a2d-108">La clase **MSVM \_ SyntheticFcPortSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c9a2d-108">The **Msvm\_SyntheticFcPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c9a2d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9a2d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9a2d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9a2d-110">Properties</span></span>

<span data-ttu-id="c9a2d-111">La clase **MSVM \_ SyntheticFcPortSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-111">The **Msvm\_SyntheticFcPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9a2d-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-115">The address of the resource.</span></span> <span data-ttu-id="c9a2d-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-120">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="c9a2d-121">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="c9a2d-122">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-126">Unidad de asignación utilizada por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="c9a2d-126">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="c9a2d-127">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-131">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="c9a2d-132">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-136">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="c9a2d-137">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-141">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="c9a2d-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-142">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-142">A short description of the object.</span></span> <span data-ttu-id="c9a2d-143">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-144">**ChapEnabled**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-144">**ChapEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-145">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-147">Indica que este puerto se ha configurado con un secreto compartido mediante DH-CHAP, lo que permite que el tejido de Canal de fibra autentique que esta máquina virtual puede usar legítimamente los nombres World Wide Name asignados a este puerto.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-147">Indicates that this port has been configured with a shared secret using DH-CHAP, which allows the Fibre Channel fabric to authenticate that this virtual machine can legitimately use the world wide names that are assigned to this port.</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-148">**Connection**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-148">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-149">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-151">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-151">The device to which this resource is connected.</span></span> <span data-ttu-id="c9a2d-152">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-153">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-153">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-156">Visibilidad del consumidor en el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-156">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="c9a2d-157">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-161">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-161">A description of the object.</span></span> <span data-ttu-id="c9a2d-162">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-166">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-166">A display name for the object.</span></span> <span data-ttu-id="c9a2d-167">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-167">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="c9a2d-168">Al cambiar esta propiedad, se cambiará el nombre del elemento del derivado del dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-168">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="c9a2d-169">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c9a2d-169">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-170">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-170">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-171">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-171">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-173">Solo se puede asignar un recurso de host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-173">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="c9a2d-174">En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-174">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="c9a2d-175">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-175">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-176">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-176">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-179">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-179">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-180">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-180">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c9a2d-181">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-181">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-182">**Límite**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-182">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-183">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-185">La cantidad máxima de recursos de host correspondientes que puede usar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-185">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="c9a2d-186">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-187">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-187">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-188">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-190">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-190">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="c9a2d-191">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-192">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-192">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-193">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-195">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-195">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="c9a2d-196">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-197">**Parent**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-197">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-200">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-200">The parent of the resource.</span></span> <span data-ttu-id="c9a2d-201">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-202">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-202">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-205">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-205">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="c9a2d-206">En el caso de las instancias asociadas a una máquina virtual, será "Microsoft:*GUID* \\ *específico del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="c9a2d-206">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="c9a2d-207">En el caso de las instancias que definen valores posibles para una máquina virtual, será "Microsoft: Definition \\ *GUID* \\ *Type*", donde el *tipo* puede ser "Maximum", "Minimum", "default" o "Increment".</span><span class="sxs-lookup"><span data-stu-id="c9a2d-207">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="c9a2d-208">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-209">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-209">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-210">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-212">La cantidad de recursos reservados para su uso por parte de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-212">The amount of resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="c9a2d-213">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-214">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-217">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="c9a2d-218">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="c9a2d-219">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-221">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-223">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="c9a2d-224">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="c9a2d-225">Value</span><span class="sxs-lookup"><span data-stu-id="c9a2d-225">Value</span></span>                                                                                                                                                                                          | <span data-ttu-id="c9a2d-226">Significado</span><span class="sxs-lookup"><span data-stu-id="c9a2d-226">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC_HBA"></span><span id="fc_hba"></span><dl> <span data-ttu-id="c9a2d-227"><dt>**HBA de FC**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c9a2d-227"><dt>**FC HBA**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="c9a2d-228">Canal de fibra</span><span class="sxs-lookup"><span data-stu-id="c9a2d-228">Fibre Channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c9a2d-229">**SecondaryWWNN**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-229">**SecondaryWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-232">Indica el nombre de nodo World Wide node Name del puerto HBA virtual que se va a usar durante la migración en vivo de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-232">Indicates the world wide node name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-233">**SecondaryWWPN**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-233">**SecondaryWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-236">Indica el nombre de Puerto WWPN del puerto HBA virtual que se va a usar durante la migración en vivo de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-236">Indicates the world wide port name of the virtual HBA port to be used during live migration of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-237">**VirtualPortWWNN**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-237">**VirtualPortWWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-238">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-240">Indica el nombre de nodo WWPN del puerto HBA virtual.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-240">Indicates the world wide node name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-241">**VirtualPortWWPN**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-241">**VirtualPortWWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-242">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-244">Indica el nombre de Puerto WWPN del puerto HBA virtual.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-244">Indicates the world wide port name of the virtual HBA port.</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-245">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-245">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-246">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-246">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-248">Especifica la cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-248">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="c9a2d-249">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-250">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-250">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-251">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-253">Especifica la unidad de medida para la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="c9a2d-253">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="c9a2d-254">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-254">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="c9a2d-255">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-255">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-256">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-256">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-257">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-259">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="c9a2d-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-260">Matriz de cadenas de identificadores de este recurso que se presenta al sistema operativo de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-260">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="c9a2d-261">Los índices y valores por índice se definen por cada recurso (es decir, por cada valor **resourcetype** enumerado).</span><span class="sxs-lookup"><span data-stu-id="c9a2d-261">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** value).</span></span> <span data-ttu-id="c9a2d-262">Esta propiedad no se utiliza</span><span class="sxs-lookup"><span data-stu-id="c9a2d-262">This property is not used</span></span>

</dd> <dt>

<span data-ttu-id="c9a2d-263">**Peso**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-263">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a2d-264">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9a2d-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9a2d-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c9a2d-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c9a2d-266">Un entero que define el peso relativo de cada procesador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-266">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="c9a2d-267">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="c9a2d-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), but is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9a2d-268">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9a2d-268">Requirements</span></span>



| <span data-ttu-id="c9a2d-269">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a2d-269">Requirement</span></span> | <span data-ttu-id="c9a2d-270">Value</span><span class="sxs-lookup"><span data-stu-id="c9a2d-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a2d-271">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9a2d-271">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a2d-272">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9a2d-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c9a2d-273">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9a2d-273">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a2d-274">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9a2d-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c9a2d-275">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c9a2d-275">Namespace</span></span><br/>                | <span data-ttu-id="c9a2d-276">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c9a2d-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c9a2d-277">MOF</span><span class="sxs-lookup"><span data-stu-id="c9a2d-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9a2d-278"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9a2d-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9a2d-279">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c9a2d-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9a2d-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9a2d-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

