---
description: Representa el estado configurado del servicio de cierre.
ms.assetid: 434DE26A-E78A-403A-AFAB-2F9272426A16
title: Msvm_ShutdownComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponentSettingData
- Msvm_ShutdownComponentSettingData.InstanceID
- Msvm_ShutdownComponentSettingData.Caption
- Msvm_ShutdownComponentSettingData.Description
- Msvm_ShutdownComponentSettingData.ElementName
- Msvm_ShutdownComponentSettingData.ResourceType
- Msvm_ShutdownComponentSettingData.OtherResourceType
- Msvm_ShutdownComponentSettingData.ResourceSubType
- Msvm_ShutdownComponentSettingData.PoolID
- Msvm_ShutdownComponentSettingData.ConsumerVisibility
- Msvm_ShutdownComponentSettingData.HostResource
- Msvm_ShutdownComponentSettingData.AllocationUnits
- Msvm_ShutdownComponentSettingData.VirtualQuantity
- Msvm_ShutdownComponentSettingData.Reservation
- Msvm_ShutdownComponentSettingData.Limit
- Msvm_ShutdownComponentSettingData.Weight
- Msvm_ShutdownComponentSettingData.AutomaticAllocation
- Msvm_ShutdownComponentSettingData.AutomaticDeallocation
- Msvm_ShutdownComponentSettingData.Parent
- Msvm_ShutdownComponentSettingData.Connection
- Msvm_ShutdownComponentSettingData.Address
- Msvm_ShutdownComponentSettingData.MappingBehavior
- Msvm_ShutdownComponentSettingData.AddressOnParent
- Msvm_ShutdownComponentSettingData.VirtualQuantityUnits
- Msvm_ShutdownComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8ee2fcb910dc788b01a58544bbfe6a06ba215585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275936"
---
# <a name="msvm_shutdowncomponentsettingdata-class"></a><span data-ttu-id="0b6c5-103">MSVM \_ ShutdownComponentSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="0b6c5-103">Msvm\_ShutdownComponentSettingData class</span></span>

<span data-ttu-id="0b6c5-104">Representa el estado configurado del servicio de cierre.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-104">Represents the configured state of the shutdown service.</span></span>

<span data-ttu-id="0b6c5-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b6c5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b6c5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Shutdown";
  string  Description = "Microsoft Shutdown Service Setting Data";
  string  ElementName = "Shutdown";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Shutdown Component";
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

## <a name="members"></a><span data-ttu-id="0b6c5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b6c5-107">Members</span></span>

<span data-ttu-id="0b6c5-108">La clase **MSVM \_ ShutdownComponentSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0b6c5-108">The **Msvm\_ShutdownComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0b6c5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b6c5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b6c5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b6c5-110">Properties</span></span>

<span data-ttu-id="0b6c5-111">La clase **MSVM \_ ShutdownComponentSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-111">The **Msvm\_ShutdownComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b6c5-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-115">The address of the resource.</span></span> <span data-ttu-id="0b6c5-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-120">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="0b6c5-121">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="0b6c5-122">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-126">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="0b6c5-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="0b6c5-127">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-131">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="0b6c5-132">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-136">Indica si el recurso se anulará la asignación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="0b6c5-137">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-141">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-141">A short description of the object.</span></span> <span data-ttu-id="0b6c5-142">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "shutdown".</span><span class="sxs-lookup"><span data-stu-id="0b6c5-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Shutdown".</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-144">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-146">Elemento al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="0b6c5-147">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-151">La visibilidad de los consumidores del recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="0b6c5-152">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="0b6c5-153">Value</span><span class="sxs-lookup"><span data-stu-id="0b6c5-153">Value</span></span>                                                                        | <span data-ttu-id="0b6c5-154">Significado</span><span class="sxs-lookup"><span data-stu-id="0b6c5-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="0b6c5-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0b6c5-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0b6c5-156">Virtualizado</span><span class="sxs-lookup"><span data-stu-id="0b6c5-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b6c5-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-160">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-160">A description of the object.</span></span> <span data-ttu-id="0b6c5-161">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-165">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-165">A display name for the object.</span></span> <span data-ttu-id="0b6c5-166">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-167">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-167">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-170">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-170">The enabled and disabled states of an element.</span></span> <span data-ttu-id="0b6c5-171">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-171">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0b6c5-172">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0b6c5-172">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0b6c5-173">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0b6c5-173">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b6c5-174">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-174">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-175">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-175">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-177">Expone una asignación específica para hospedar o los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-177">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="0b6c5-178">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-178">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-179">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-179">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-182">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-182">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-183">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-183">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0b6c5-184">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-185">**Límite**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-185">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-186">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-186">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-188">El límite superior o la cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-188">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="0b6c5-189">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-189">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-190">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-190">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-191">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-193">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-193">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="0b6c5-194">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-194">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-195">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-195">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-196">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-198">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-198">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="0b6c5-199">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-199">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-200">**Parent**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-200">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-203">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-203">The parent of the resource.</span></span> <span data-ttu-id="0b6c5-204">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-205">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-205">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-208">IDENTIFICADOR del grupo de recursos desde el que se asigna el recurso.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-208">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="0b6c5-209">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-210">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-210">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-211">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-213">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-213">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="0b6c5-214">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-214">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-215">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-215">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-218">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-218">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="0b6c5-219">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-220">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-220">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-221">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-221">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-223">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-223">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="0b6c5-224">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="0b6c5-225">Value</span><span class="sxs-lookup"><span data-stu-id="0b6c5-225">Value</span></span>                                                                        | <span data-ttu-id="0b6c5-226">Significado</span><span class="sxs-lookup"><span data-stu-id="0b6c5-226">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="0b6c5-227"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0b6c5-227"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0b6c5-228">Otros</span><span class="sxs-lookup"><span data-stu-id="0b6c5-228">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b6c5-229">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-229">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-230">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-232">La cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-232">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="0b6c5-233">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-233">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-234">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-234">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-235">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-236">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-237">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-237">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="0b6c5-238">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-238">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="0b6c5-239">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-239">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0b6c5-240">**Peso**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-240">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b6c5-241">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b6c5-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b6c5-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b6c5-243">Prioridad relativa de esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-243">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="0b6c5-244">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b6c5-245">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b6c5-245">Remarks</span></span>

<span data-ttu-id="0b6c5-246">El acceso a la clase **MSVM \_ ShutdownComponentSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="0b6c5-246">Access to the **Msvm\_ShutdownComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0b6c5-247">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0b6c5-247">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6c5-248">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b6c5-248">Requirements</span></span>



| <span data-ttu-id="0b6c5-249">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b6c5-249">Requirement</span></span> | <span data-ttu-id="0b6c5-250">Value</span><span class="sxs-lookup"><span data-stu-id="0b6c5-250">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6c5-251">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b6c5-251">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6c5-252">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b6c5-252">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0b6c5-253">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b6c5-253">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6c5-254">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b6c5-254">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b6c5-255">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b6c5-255">Namespace</span></span><br/>                | <span data-ttu-id="0b6c5-256">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0b6c5-256">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0b6c5-257">MOF</span><span class="sxs-lookup"><span data-stu-id="0b6c5-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b6c5-258"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b6c5-258"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b6c5-259">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b6c5-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b6c5-260"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b6c5-260"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b6c5-261">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b6c5-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6c5-262">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-262">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="0b6c5-263">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="0b6c5-263">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

