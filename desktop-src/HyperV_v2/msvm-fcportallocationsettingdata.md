---
description: Representa el estado configurado de un puerto de Canal de fibra sintético o un puerto de conmutador Canal de fibra.
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Msvm_FcPortAllocationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 824f7077eeb3cb9e00ce8733cb5d2f57761716e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686957"
---
# <a name="msvm_fcportallocationsettingdata-class"></a><span data-ttu-id="0c70a-103">MSVM \_ FcPortAllocationSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="0c70a-103">Msvm\_FcPortAllocationSettingData class</span></span>

<span data-ttu-id="0c70a-104">Representa el estado configurado de un puerto de Canal de fibra sintético o un puerto de conmutador Canal de fibra.</span><span class="sxs-lookup"><span data-stu-id="0c70a-104">Represents the configured state of a synthetic Fibre Channel port or a Fibre Channel switch port.</span></span>

<span data-ttu-id="0c70a-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0c70a-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c70a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c70a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
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
};
```

## <a name="members"></a><span data-ttu-id="0c70a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c70a-107">Members</span></span>

<span data-ttu-id="0c70a-108">La clase **MSVM \_ FcPortAllocationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0c70a-108">The **Msvm\_FcPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0c70a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c70a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c70a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c70a-110">Properties</span></span>

<span data-ttu-id="0c70a-111">La clase **MSVM \_ FcPortAllocationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c70a-111">The **Msvm\_FcPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c70a-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="0c70a-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="0c70a-115">The address of the resource.</span></span> <span data-ttu-id="0c70a-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="0c70a-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-120">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="0c70a-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="0c70a-121">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="0c70a-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="0c70a-122">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="0c70a-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-126">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="0c70a-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="0c70a-127">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="0c70a-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0c70a-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-131">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0c70a-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="0c70a-132">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="0c70a-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0c70a-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-136">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0c70a-136">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="0c70a-137">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0c70a-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-141">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="0c70a-141">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-142">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0c70a-142">A short description of the object.</span></span> <span data-ttu-id="0c70a-143">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c70a-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="0c70a-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-145">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0c70a-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-147">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="0c70a-147">The device to which this resource is connected.</span></span> <span data-ttu-id="0c70a-148">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="0c70a-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c70a-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-152">Visibilidad del consumidor en el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="0c70a-152">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="0c70a-153">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-154">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0c70a-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-157">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0c70a-157">A description of the object.</span></span> <span data-ttu-id="0c70a-158">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c70a-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0c70a-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-162">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="0c70a-162">A display name for the object.</span></span> <span data-ttu-id="0c70a-163">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c70a-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="0c70a-164">Al cambiar esta propiedad, se cambiará el nombre del elemento del derivado del dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="0c70a-164">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="0c70a-165">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0c70a-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-166">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="0c70a-166">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-167">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0c70a-167">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-169">Solo se puede asignar un recurso de host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="0c70a-169">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="0c70a-170">En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="0c70a-170">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="0c70a-171">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-171">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0c70a-172">Se trata de una propiedad de solo lectura, pero si la propiedad **resourcetype** es 22 (disco) y la propiedad **subtipo** es "unidad de disco físico de Microsoft", se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0c70a-172">This is a read-only property, but if the **ResourceType** property is 22 (Disk) and the **ResourceSubType** property is "Microsoft Physical Disk Drive", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0c70a-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-176">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="0c70a-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-177">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0c70a-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0c70a-178">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c70a-178">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-179">**Límite**</span><span class="sxs-lookup"><span data-stu-id="0c70a-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-180">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c70a-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-182">La cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="0c70a-182">The maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="0c70a-183">La unidad de medida para esta propiedad se especifica mediante la propiedad **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="0c70a-183">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="0c70a-184">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-184">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-185">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="0c70a-185">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-186">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c70a-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-188">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="0c70a-188">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="0c70a-189">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-190">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="0c70a-190">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-193">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="0c70a-193">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="0c70a-194">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-195">**Parent**</span><span class="sxs-lookup"><span data-stu-id="0c70a-195">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-198">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="0c70a-198">The parent of the resource.</span></span> <span data-ttu-id="0c70a-199">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-200">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="0c70a-200">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-203">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="0c70a-203">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="0c70a-204">En el caso de las instancias asociadas a una máquina virtual, será "Microsoft:*GUID* \\ *específico del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="0c70a-204">For instances associated with a virtual machine, this will be "Microsoft:*GUID*\\*device-specific data*".</span></span> <span data-ttu-id="0c70a-205">En el caso de las instancias que definen valores posibles para una máquina virtual, será "Microsoft: Definition \\ *GUID* \\ *Type*", donde el *tipo* puede ser "Maximum", "Minimum", "default" o "Increment".</span><span class="sxs-lookup"><span data-stu-id="0c70a-205">For instances that define potential settings for a virtual machine, this will be "Microsoft:Definition\\*GUID*\\*Type*", where *Type* can be one of "Maximum", "Minimum", "Default", or "Increment".</span></span> <span data-ttu-id="0c70a-206">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-207">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="0c70a-207">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-208">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c70a-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-210">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="0c70a-210">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="0c70a-211">La unidad de medida para esta propiedad se especifica mediante la propiedad **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="0c70a-211">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="0c70a-212">Se garantiza que estos recursos están disponibles para su consumo por parte de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c70a-212">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="0c70a-213">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-214">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="0c70a-214">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-217">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="0c70a-217">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="0c70a-218">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="0c70a-218">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="0c70a-219">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0c70a-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-221">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c70a-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-223">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="0c70a-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="0c70a-224">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="0c70a-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="0c70a-225"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="0c70a-226"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="0c70a-227"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="0c70a-228"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="0c70a-229"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="0c70a-230"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="0c70a-231"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="0c70a-232"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="0c70a-233"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="0c70a-234"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="0c70a-235"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="0c70a-236"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="0c70a-237"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="0c70a-238"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="0c70a-239"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="0c70a-240"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (17)</span><span class="sxs-lookup"><span data-stu-id="0c70a-241"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (18)</span><span class="sxs-lookup"><span data-stu-id="0c70a-242"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controladora USB** (19)</span><span class="sxs-lookup"><span data-stu-id="0c70a-243"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controladora de gráficos** (20)</span><span class="sxs-lookup"><span data-stu-id="0c70a-244"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de almacenamiento** (21)</span><span class="sxs-lookup"><span data-stu-id="0c70a-245"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="0c70a-246"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Cinta** (23)</span><span class="sxs-lookup"><span data-stu-id="0c70a-247"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (24)</span><span class="sxs-lookup"><span data-stu-id="0c70a-248"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controlador Firewire** (25)</span><span class="sxs-lookup"><span data-stu-id="0c70a-249"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="0c70a-250"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="0c70a-251"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fuente de alimentación** (28)</span><span class="sxs-lookup"><span data-stu-id="0c70a-252"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de refrigeración** (29)</span><span class="sxs-lookup"><span data-stu-id="0c70a-253"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="0c70a-254"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="0c70a-255"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c70a-256">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="0c70a-256">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-257">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c70a-257">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-259">Especifica la cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="0c70a-259">Specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="0c70a-260">La unidad de medida para esta propiedad se especifica mediante la propiedad **VirtualQuantityUnits** .</span><span class="sxs-lookup"><span data-stu-id="0c70a-260">The unit of measurement for this property is specified by the **VirtualQuantityUnits** property.</span></span> <span data-ttu-id="0c70a-261">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-262">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="0c70a-262">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-263">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c70a-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-264">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-265">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c70a-265">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="0c70a-266">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0c70a-266">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="0c70a-267">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-267">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c70a-268">**Peso**</span><span class="sxs-lookup"><span data-stu-id="0c70a-268">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c70a-269">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c70a-269">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c70a-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c70a-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c70a-271">Un entero que define el peso relativo de cada procesador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c70a-271">An integer that defines the relative weight for each virtual machine processor.</span></span> <span data-ttu-id="0c70a-272">Una vez que se hayan cumplido todas las reservas, la capacidad de procesador físico restante de la plataforma de hospedaje se asignará a las máquinas virtuales en función de sus ponderaciones relativas.</span><span class="sxs-lookup"><span data-stu-id="0c70a-272">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="0c70a-273">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c70a-273">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0c70a-274">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="0c70a-274">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c70a-275">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c70a-275">Requirements</span></span>



| <span data-ttu-id="0c70a-276">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c70a-276">Requirement</span></span> | <span data-ttu-id="0c70a-277">Value</span><span class="sxs-lookup"><span data-stu-id="0c70a-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c70a-278">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c70a-278">Minimum supported client</span></span><br/> | <span data-ttu-id="0c70a-279">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c70a-279">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c70a-280">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c70a-280">Minimum supported server</span></span><br/> | <span data-ttu-id="0c70a-281">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c70a-281">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c70a-282">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0c70a-282">Namespace</span></span><br/>                | <span data-ttu-id="0c70a-283">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0c70a-283">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c70a-284">MOF</span><span class="sxs-lookup"><span data-stu-id="0c70a-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c70a-285"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c70a-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c70a-286">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c70a-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c70a-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c70a-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

