---
description: Representa el estado configurado del servicio Servicio de instantáneas de volumen (VSS).
ms.assetid: FAE8E8F7-525A-4E5A-91B3-B73343337352
title: Msvm_VssComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssComponentSettingData
- Msvm_VssComponentSettingData.InstanceID
- Msvm_VssComponentSettingData.Caption
- Msvm_VssComponentSettingData.Description
- Msvm_VssComponentSettingData.ElementName
- Msvm_VssComponentSettingData.ResourceType
- Msvm_VssComponentSettingData.OtherResourceType
- Msvm_VssComponentSettingData.ResourceSubType
- Msvm_VssComponentSettingData.PoolID
- Msvm_VssComponentSettingData.ConsumerVisibility
- Msvm_VssComponentSettingData.HostResource
- Msvm_VssComponentSettingData.AllocationUnits
- Msvm_VssComponentSettingData.VirtualQuantity
- Msvm_VssComponentSettingData.Reservation
- Msvm_VssComponentSettingData.Limit
- Msvm_VssComponentSettingData.Weight
- Msvm_VssComponentSettingData.AutomaticAllocation
- Msvm_VssComponentSettingData.AutomaticDeallocation
- Msvm_VssComponentSettingData.Parent
- Msvm_VssComponentSettingData.Connection
- Msvm_VssComponentSettingData.Address
- Msvm_VssComponentSettingData.MappingBehavior
- Msvm_VssComponentSettingData.AddressOnParent
- Msvm_VssComponentSettingData.VirtualQuantityUnits
- Msvm_VssComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d37f46c10cc702c66a30fb484553a8c5da03d8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666310"
---
# <a name="msvm_vsscomponentsettingdata-class"></a><span data-ttu-id="08c3b-103">MSVM \_ VssComponentSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="08c3b-103">Msvm\_VssComponentSettingData class</span></span>

<span data-ttu-id="08c3b-104">Representa el estado configurado del servicio Servicio de instantáneas de volumen (VSS).</span><span class="sxs-lookup"><span data-stu-id="08c3b-104">Represents the configured state of the Volume Shadow Copy Service (VSS) service.</span></span>

<span data-ttu-id="08c3b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="08c3b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c3b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08c3b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "VSS";
  string  Description = "Microsoft VSS Service Setting Data";
  string  ElementName = "VSS";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:VSS Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource;
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

## <a name="members"></a><span data-ttu-id="08c3b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="08c3b-107">Members</span></span>

<span data-ttu-id="08c3b-108">La clase **MSVM \_ VssComponentSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="08c3b-108">The **Msvm\_VssComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="08c3b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08c3b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08c3b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08c3b-110">Properties</span></span>

<span data-ttu-id="08c3b-111">La clase **MSVM \_ VssComponentSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="08c3b-111">The **Msvm\_VssComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08c3b-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="08c3b-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="08c3b-115">The address of the resource.</span></span> <span data-ttu-id="08c3b-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="08c3b-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-120">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="08c3b-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="08c3b-121">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="08c3b-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="08c3b-122">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="08c3b-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-126">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="08c3b-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="08c3b-127">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="08c3b-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="08c3b-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-131">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="08c3b-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="08c3b-132">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="08c3b-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="08c3b-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-136">Indica si el recurso se anulará la asignación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="08c3b-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="08c3b-137">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="08c3b-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-141">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="08c3b-141">A short description of the object.</span></span> <span data-ttu-id="08c3b-142">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08c3b-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="08c3b-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-144">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="08c3b-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-146">Elemento al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="08c3b-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="08c3b-147">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="08c3b-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08c3b-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-151">La visibilidad de los consumidores del recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="08c3b-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="08c3b-152">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="08c3b-153">Value</span><span class="sxs-lookup"><span data-stu-id="08c3b-153">Value</span></span>                                                                        | <span data-ttu-id="08c3b-154">Significado</span><span class="sxs-lookup"><span data-stu-id="08c3b-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="08c3b-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="08c3b-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="08c3b-156">Virtualizado</span><span class="sxs-lookup"><span data-stu-id="08c3b-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="08c3b-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="08c3b-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-160">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="08c3b-160">A description of the object.</span></span> <span data-ttu-id="08c3b-161">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08c3b-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="08c3b-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-165">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="08c3b-165">A display name for the object.</span></span> <span data-ttu-id="08c3b-166">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="08c3b-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="08c3b-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08c3b-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-170">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="08c3b-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="08c3b-171">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) y tiene un valor predeterminado de 2 (habilitado).</span><span class="sxs-lookup"><span data-stu-id="08c3b-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and has a default value of 2 (Enabled).</span></span>

<span data-ttu-id="08c3b-172">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="08c3b-172">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>



 <span data-ttu-id="08c3b-173">(2)</span><span class="sxs-lookup"><span data-stu-id="08c3b-173">(2)</span></span>


</dt> <dd>

<span data-ttu-id="08c3b-174">habilitado</span><span class="sxs-lookup"><span data-stu-id="08c3b-174">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-175">3</span><span class="sxs-lookup"><span data-stu-id="08c3b-175">3</span></span>
</dt> <dd>

<span data-ttu-id="08c3b-176">Disabled</span><span class="sxs-lookup"><span data-stu-id="08c3b-176">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08c3b-177">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="08c3b-177">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-180">Expone una asignación específica para hospedar o los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="08c3b-180">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="08c3b-181">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="08c3b-181">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08c3b-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-185">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="08c3b-185">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-186">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="08c3b-186">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="08c3b-187">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="08c3b-187">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-188">**Límite**</span><span class="sxs-lookup"><span data-stu-id="08c3b-188">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-189">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08c3b-189">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-191">El límite superior o la cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="08c3b-191">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="08c3b-192">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-193">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="08c3b-193">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-194">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08c3b-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-196">Indica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="08c3b-196">Indicates how this resource maps to underlying resources.</span></span> <span data-ttu-id="08c3b-197">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-197">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-198">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="08c3b-198">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-199">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-200">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-201">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="08c3b-201">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="08c3b-202">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-202">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-203">**Parent**</span><span class="sxs-lookup"><span data-stu-id="08c3b-203">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-206">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="08c3b-206">The parent of the resource.</span></span> <span data-ttu-id="08c3b-207">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-207">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-208">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="08c3b-208">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-209">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-210">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-211">IDENTIFICADOR del grupo de recursos desde el que se asigna el recurso.</span><span class="sxs-lookup"><span data-stu-id="08c3b-211">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="08c3b-212">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-212">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-213">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="08c3b-213">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-214">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08c3b-214">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-216">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="08c3b-216">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="08c3b-217">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-217">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-218">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="08c3b-218">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-219">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-221">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="08c3b-221">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="08c3b-222">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="08c3b-222">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-223">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="08c3b-223">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-224">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08c3b-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-226">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="08c3b-226">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="08c3b-227">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="08c3b-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1 (Other).</span></span>



| <span data-ttu-id="08c3b-228">Value</span><span class="sxs-lookup"><span data-stu-id="08c3b-228">Value</span></span>                                                                        | <span data-ttu-id="08c3b-229">Significado</span><span class="sxs-lookup"><span data-stu-id="08c3b-229">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="08c3b-230"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="08c3b-230"><dt>1</dt></span></span> </dl> | <span data-ttu-id="08c3b-231">Otros</span><span class="sxs-lookup"><span data-stu-id="08c3b-231">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="08c3b-232">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="08c3b-232">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-233">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08c3b-233">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-235">La cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="08c3b-235">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="08c3b-236">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-237">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="08c3b-237">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-238">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08c3b-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-240">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="08c3b-240">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="08c3b-241">El valor de esta propiedad es un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="08c3b-241">The value of this property is a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="08c3b-242">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-242">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="08c3b-243">**Peso**</span><span class="sxs-lookup"><span data-stu-id="08c3b-243">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08c3b-244">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08c3b-244">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08c3b-245">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08c3b-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08c3b-246">Prioridad relativa de esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="08c3b-246">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="08c3b-247">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="08c3b-247">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08c3b-248">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08c3b-248">Remarks</span></span>

<span data-ttu-id="08c3b-249">El acceso a la clase **MSVM \_ VssComponentSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="08c3b-249">Access to the **Msvm\_VssComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="08c3b-250">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="08c3b-250">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="08c3b-251">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08c3b-251">Requirements</span></span>



| <span data-ttu-id="08c3b-252">Requisito</span><span class="sxs-lookup"><span data-stu-id="08c3b-252">Requirement</span></span> | <span data-ttu-id="08c3b-253">Value</span><span class="sxs-lookup"><span data-stu-id="08c3b-253">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c3b-254">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08c3b-254">Minimum supported client</span></span><br/> | <span data-ttu-id="08c3b-255">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="08c3b-255">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="08c3b-256">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08c3b-256">Minimum supported server</span></span><br/> | <span data-ttu-id="08c3b-257">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="08c3b-257">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08c3b-258">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08c3b-258">Namespace</span></span><br/>                | <span data-ttu-id="08c3b-259">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="08c3b-259">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="08c3b-260">MOF</span><span class="sxs-lookup"><span data-stu-id="08c3b-260">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08c3b-261"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08c3b-261"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08c3b-262">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08c3b-262">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08c3b-263"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08c3b-263"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08c3b-264">Vea también</span><span class="sxs-lookup"><span data-stu-id="08c3b-264">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c3b-265">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="08c3b-265">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="08c3b-266">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="08c3b-266">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

