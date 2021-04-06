---
description: Representa el estado configurado del servicio de sincronización de hora.
ms.assetid: AACEDE11-3F5B-42AB-A16F-0474FA98D3FD
title: Msvm_TimeSyncComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TimeSyncComponentSettingData
- Msvm_TimeSyncComponentSettingData.InstanceID
- Msvm_TimeSyncComponentSettingData.Caption
- Msvm_TimeSyncComponentSettingData.Description
- Msvm_TimeSyncComponentSettingData.ElementName
- Msvm_TimeSyncComponentSettingData.ResourceType
- Msvm_TimeSyncComponentSettingData.OtherResourceType
- Msvm_TimeSyncComponentSettingData.ResourceSubType
- Msvm_TimeSyncComponentSettingData.PoolID
- Msvm_TimeSyncComponentSettingData.ConsumerVisibility
- Msvm_TimeSyncComponentSettingData.HostResource
- Msvm_TimeSyncComponentSettingData.AllocationUnits
- Msvm_TimeSyncComponentSettingData.VirtualQuantity
- Msvm_TimeSyncComponentSettingData.Reservation
- Msvm_TimeSyncComponentSettingData.Limit
- Msvm_TimeSyncComponentSettingData.Weight
- Msvm_TimeSyncComponentSettingData.AutomaticAllocation
- Msvm_TimeSyncComponentSettingData.AutomaticDeallocation
- Msvm_TimeSyncComponentSettingData.Parent
- Msvm_TimeSyncComponentSettingData.Connection
- Msvm_TimeSyncComponentSettingData.Address
- Msvm_TimeSyncComponentSettingData.MappingBehavior
- Msvm_TimeSyncComponentSettingData.AddressOnParent
- Msvm_TimeSyncComponentSettingData.VirtualQuantityUnits
- Msvm_TimeSyncComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 063c0f7904976d50d7c1914f810e71ff84f740b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001403"
---
# <a name="msvm_timesynccomponentsettingdata-class"></a><span data-ttu-id="b8a70-103">MSVM \_ TimeSyncComponentSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="b8a70-103">Msvm\_TimeSyncComponentSettingData class</span></span>

<span data-ttu-id="b8a70-104">Representa el estado configurado del servicio de sincronización de hora.</span><span class="sxs-lookup"><span data-stu-id="b8a70-104">Represents the configured state of the time synchronization service.</span></span>

<span data-ttu-id="b8a70-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b8a70-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a70-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8a70-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TimeSyncComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Time Synchronization";
  string  Description = "Microsoft Time Synchronization Service Setting Data";
  string  ElementName = "Time Synchronization";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Time Synchronization Component";
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

## <a name="members"></a><span data-ttu-id="b8a70-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8a70-107">Members</span></span>

<span data-ttu-id="b8a70-108">La clase **MSVM \_ TimeSyncComponentSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b8a70-108">The **Msvm\_TimeSyncComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b8a70-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8a70-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8a70-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8a70-110">Properties</span></span>

<span data-ttu-id="b8a70-111">La clase **MSVM \_ TimeSyncComponentSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b8a70-111">The **Msvm\_TimeSyncComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8a70-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="b8a70-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="b8a70-115">The address of the resource.</span></span> <span data-ttu-id="b8a70-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="b8a70-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-120">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="b8a70-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="b8a70-121">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="b8a70-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="b8a70-122">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="b8a70-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-126">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="b8a70-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="b8a70-127">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="b8a70-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8a70-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-131">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b8a70-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="b8a70-132">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="b8a70-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b8a70-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-136">Indica si el recurso se anulará la asignación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b8a70-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="b8a70-137">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b8a70-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-141">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8a70-141">A short description of the object.</span></span> <span data-ttu-id="b8a70-142">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b8a70-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="b8a70-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-144">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b8a70-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-146">Elemento al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="b8a70-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="b8a70-147">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="b8a70-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8a70-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-151">La visibilidad de los consumidores del recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="b8a70-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="b8a70-152">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="b8a70-153">Value</span><span class="sxs-lookup"><span data-stu-id="b8a70-153">Value</span></span>                                                                        | <span data-ttu-id="b8a70-154">Significado</span><span class="sxs-lookup"><span data-stu-id="b8a70-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="b8a70-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b8a70-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b8a70-156">Virtualizado</span><span class="sxs-lookup"><span data-stu-id="b8a70-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8a70-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b8a70-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-160">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8a70-160">A description of the object.</span></span> <span data-ttu-id="b8a70-161">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b8a70-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b8a70-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-165">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="b8a70-165">A display name for the object.</span></span> <span data-ttu-id="b8a70-166">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b8a70-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b8a70-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8a70-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-170">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="b8a70-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b8a70-171">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b8a70-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span></span>

<dt>



 <span data-ttu-id="b8a70-172">(2)</span><span class="sxs-lookup"><span data-stu-id="b8a70-172">(2)</span></span>


</dt> <dd>

<span data-ttu-id="b8a70-173">habilitado</span><span class="sxs-lookup"><span data-stu-id="b8a70-173">Enabled</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-174">3</span><span class="sxs-lookup"><span data-stu-id="b8a70-174">3</span></span>
</dt> <dd>

<span data-ttu-id="b8a70-175">Disabled</span><span class="sxs-lookup"><span data-stu-id="b8a70-175">Disabled</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8a70-176">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="b8a70-176">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-177">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="b8a70-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-179">Expone una asignación específica para hospedar o los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="b8a70-179">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="b8a70-180">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="b8a70-180">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-181">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b8a70-181">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-184">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="b8a70-184">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-185">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="b8a70-185">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b8a70-186">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="b8a70-186">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-187">**Límite**</span><span class="sxs-lookup"><span data-stu-id="b8a70-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-188">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8a70-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-190">El límite superior o la cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="b8a70-190">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="b8a70-191">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-191">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-192">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="b8a70-192">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-193">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8a70-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-195">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="b8a70-195">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="b8a70-196">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-197">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="b8a70-197">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-200">El tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor "Other".</span><span class="sxs-lookup"><span data-stu-id="b8a70-200">The resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="b8a70-201">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-202">**Parent**</span><span class="sxs-lookup"><span data-stu-id="b8a70-202">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-205">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="b8a70-205">The parent of the resource.</span></span> <span data-ttu-id="b8a70-206">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-207">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="b8a70-207">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-210">IDENTIFICADOR del grupo de recursos desde el que se asigna el recurso.</span><span class="sxs-lookup"><span data-stu-id="b8a70-210">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="b8a70-211">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-212">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="b8a70-212">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-213">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8a70-213">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-215">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="b8a70-215">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="b8a70-216">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-217">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="b8a70-217">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-220">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="b8a70-220">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="b8a70-221">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="b8a70-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-222">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="b8a70-222">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-223">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8a70-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-225">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="b8a70-225">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="b8a70-226">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="b8a70-227">Value</span><span class="sxs-lookup"><span data-stu-id="b8a70-227">Value</span></span>                                                                        | <span data-ttu-id="b8a70-228">Significado</span><span class="sxs-lookup"><span data-stu-id="b8a70-228">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="b8a70-229"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b8a70-229"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b8a70-230">Otros</span><span class="sxs-lookup"><span data-stu-id="b8a70-230">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b8a70-231">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="b8a70-231">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-232">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b8a70-232">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-234">La cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="b8a70-234">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="b8a70-235">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-236">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="b8a70-236">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-237">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b8a70-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-239">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8a70-239">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="b8a70-240">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8a70-240">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="b8a70-241">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="b8a70-242">**Peso**</span><span class="sxs-lookup"><span data-stu-id="b8a70-242">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8a70-243">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b8a70-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8a70-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b8a70-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8a70-245">Prioridad relativa de esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="b8a70-245">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="b8a70-246">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="b8a70-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8a70-247">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8a70-247">Remarks</span></span>

<span data-ttu-id="b8a70-248">El acceso a la clase **MSVM \_ TimeSyncComponentSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b8a70-248">Access to the **Msvm\_TimeSyncComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b8a70-249">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b8a70-249">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a70-250">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8a70-250">Requirements</span></span>



| <span data-ttu-id="b8a70-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a70-251">Requirement</span></span> | <span data-ttu-id="b8a70-252">Value</span><span class="sxs-lookup"><span data-stu-id="b8a70-252">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a70-253">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8a70-253">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a70-254">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8a70-254">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b8a70-255">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8a70-255">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a70-256">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8a70-256">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8a70-257">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8a70-257">Namespace</span></span><br/>                | <span data-ttu-id="b8a70-258">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b8a70-258">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b8a70-259">MOF</span><span class="sxs-lookup"><span data-stu-id="b8a70-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8a70-260"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8a70-260"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8a70-261">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8a70-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8a70-262"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b8a70-262"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b8a70-263">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8a70-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a70-264">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b8a70-264">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="b8a70-265">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b8a70-265">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

