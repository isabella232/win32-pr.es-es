---
description: Representa el estado configurado del servicio de intercambio de pares clave-valor.
ms.assetid: B7ED1091-E49A-4C38-9794-E074E6B9EF48
title: Msvm_KvpExchangeComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeComponentSettingData
- Msvm_KvpExchangeComponentSettingData.DisableHostKVPItems
- Msvm_KvpExchangeComponentSettingData.InstanceID
- Msvm_KvpExchangeComponentSettingData.Caption
- Msvm_KvpExchangeComponentSettingData.Description
- Msvm_KvpExchangeComponentSettingData.ElementName
- Msvm_KvpExchangeComponentSettingData.ResourceType
- Msvm_KvpExchangeComponentSettingData.OtherResourceType
- Msvm_KvpExchangeComponentSettingData.ResourceSubType
- Msvm_KvpExchangeComponentSettingData.PoolID
- Msvm_KvpExchangeComponentSettingData.ConsumerVisibility
- Msvm_KvpExchangeComponentSettingData.HostResource
- Msvm_KvpExchangeComponentSettingData.AllocationUnits
- Msvm_KvpExchangeComponentSettingData.VirtualQuantity
- Msvm_KvpExchangeComponentSettingData.Reservation
- Msvm_KvpExchangeComponentSettingData.Limit
- Msvm_KvpExchangeComponentSettingData.Weight
- Msvm_KvpExchangeComponentSettingData.AutomaticAllocation
- Msvm_KvpExchangeComponentSettingData.AutomaticDeallocation
- Msvm_KvpExchangeComponentSettingData.Parent
- Msvm_KvpExchangeComponentSettingData.Connection
- Msvm_KvpExchangeComponentSettingData.Address
- Msvm_KvpExchangeComponentSettingData.MappingBehavior
- Msvm_KvpExchangeComponentSettingData.AddressOnParent
- Msvm_KvpExchangeComponentSettingData.VirtualQuantityUnits
- Msvm_KvpExchangeComponentSettingData.EnabledState
- Msvm_KvpExchangeComponentSettingData.HostExchangeItems
- Msvm_KvpExchangeComponentSettingData.HostOnlyItems
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fe2ef128d3212ba2dfd47a3d71f713c26ba2435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667174"
---
# <a name="msvm_kvpexchangecomponentsettingdata-class"></a><span data-ttu-id="3e26e-103">MSVM \_ KvpExchangeComponentSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="3e26e-103">Msvm\_KvpExchangeComponentSettingData class</span></span>

<span data-ttu-id="3e26e-104">Representa el estado configurado del servicio de intercambio de pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="3e26e-104">Represents the configured state of the key/value pair exchange service.</span></span>

<span data-ttu-id="3e26e-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3e26e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e26e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e26e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_KvpExchangeComponentSettingData : CIM_ResourceAllocationSettingData
{
  boolean DisableHostKVPItems;
  string  InstanceID;
  string  Caption = "Key-Value Pair Exchange";
  string  Description = "Microsoft Key-Value Pair Exchange Service Setting Data";
  string  ElementName = "Key-Value Pair Exchange";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft:Hyper-V:Key-Value Pair Exchange Component";
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
  String  HostExchangeItems[];
  String  HostOnlyItems[];
};
```

## <a name="members"></a><span data-ttu-id="3e26e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e26e-107">Members</span></span>

<span data-ttu-id="3e26e-108">La clase **MSVM \_ KvpExchangeComponentSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3e26e-108">The **Msvm\_KvpExchangeComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3e26e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e26e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e26e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e26e-110">Properties</span></span>

<span data-ttu-id="3e26e-111">La clase **MSVM \_ KvpExchangeComponentSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3e26e-111">The **Msvm\_KvpExchangeComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e26e-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="3e26e-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="3e26e-115">The address of the resource.</span></span> <span data-ttu-id="3e26e-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="3e26e-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="3e26e-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-120">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="3e26e-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="3e26e-121">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="3e26e-121">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="3e26e-122">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-122">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-123">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="3e26e-123">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-126">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="3e26e-126">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="3e26e-127">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-127">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-128">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="3e26e-128">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3e26e-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-131">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3e26e-131">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="3e26e-132">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-132">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-133">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="3e26e-133">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3e26e-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-136">Indica si el recurso se anulará la asignación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3e26e-136">Indicates whether the resource will be automatically de-allocated.</span></span> <span data-ttu-id="3e26e-137">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-137">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3e26e-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-141">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3e26e-141">A short description of the object.</span></span> <span data-ttu-id="3e26e-142">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3e26e-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-143">**Connection**</span><span class="sxs-lookup"><span data-stu-id="3e26e-143">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-144">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3e26e-144">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-146">Elemento al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="3e26e-146">The thing to which this resource is connected.</span></span> <span data-ttu-id="3e26e-147">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="3e26e-147">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-148">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="3e26e-148">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e26e-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-151">La visibilidad de los consumidores del recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="3e26e-151">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="3e26e-152">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-152">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="3e26e-153">Value</span><span class="sxs-lookup"><span data-stu-id="3e26e-153">Value</span></span>                                                                        | <span data-ttu-id="3e26e-154">Significado</span><span class="sxs-lookup"><span data-stu-id="3e26e-154">Meaning</span></span>                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="3e26e-155"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3e26e-155"><dt>3</dt></span></span> </dl> | <span data-ttu-id="3e26e-156">Virtualizado</span><span class="sxs-lookup"><span data-stu-id="3e26e-156">Virtualized</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3e26e-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3e26e-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-160">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3e26e-160">A description of the object.</span></span> <span data-ttu-id="3e26e-161">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3e26e-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-162">**DisableHostKVPItems**</span><span class="sxs-lookup"><span data-stu-id="3e26e-162">**DisableHostKVPItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-163">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3e26e-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e26e-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-165">Esta propiedad deshabilita el host de populatinghost automáticamente el nombre y la información del sistema operativo dentro del invitado.</span><span class="sxs-lookup"><span data-stu-id="3e26e-165">This property disables the host from automatically populatinghost name and OS information inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="3e26e-166">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="3e26e-166">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="3e26e-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3e26e-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-170">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="3e26e-170">A display name for the object.</span></span> <span data-ttu-id="3e26e-171">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3e26e-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-172">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3e26e-172">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-173">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e26e-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-175">Estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3e26e-175">The enabled state of the element.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3e26e-176">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="3e26e-176">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3e26e-177">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="3e26e-177">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e26e-178">**HostExchangeItems**</span><span class="sxs-lookup"><span data-stu-id="3e26e-178">**HostExchangeItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-179">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3e26e-179">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-181">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="3e26e-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-182">Matriz de instancias de [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) incrustadas que representan los pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="3e26e-182">An array of embedded [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances that represent the key/value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-183">**HostOnlyItems**</span><span class="sxs-lookup"><span data-stu-id="3e26e-183">**HostOnlyItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-184">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3e26e-184">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-186">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("MSVM \_ KvpExchangeDataItem")</span><span class="sxs-lookup"><span data-stu-id="3e26e-186">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_KvpExchangeDataItem")</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-187">Matriz de instancias de [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) que contiene los pares clave-valor que se almacenan en el archivo de configuración, pero no se intercambian con el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="3e26e-187">An array of [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) instances containing the key/value pairs that are stored in the configuration file but not exchanged with the guest operating system.</span></span> <span data-ttu-id="3e26e-188">Esto permite que las aplicaciones almacenen datos específicos de la máquina virtual que no es necesario que sean visibles para el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="3e26e-188">This allows applications to store virtual machine-specific data that does not need to be visible to the guest operating system.</span></span> <span data-ttu-id="3e26e-189">Los elementos tienen el mismo formato que los elementos de la propiedad **HostExchangeItems** , excepto que la propiedad **source** de la instancia de **MSVM \_ KvpExchangeDataItem** se establece en 4.</span><span class="sxs-lookup"><span data-stu-id="3e26e-189">The items are formatted the same as the items in the **HostExchangeItems** property except the **Source** property of the **Msvm\_KvpExchangeDataItem** instance is set to 4.</span></span> <span data-ttu-id="3e26e-190">Cada archivo de configuración está limitado a 128 pares clave-valor, donde cada campo de valor puede tener un tamaño de hasta 16 KB y el campo de clave puede tener hasta 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="3e26e-190">Each configuration file is limited to 128 key/value pairs, where each value field is allowed to be up to 16 KB in size and the key field is allowed to be up to 512 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-191">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="3e26e-191">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-192">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3e26e-192">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-194">Expone una asignación específica para hospedar o los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="3e26e-194">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="3e26e-195">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="3e26e-195">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-196">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e26e-196">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-199">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3e26e-199">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-200">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="3e26e-200">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3e26e-201">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3e26e-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-202">**Límite**</span><span class="sxs-lookup"><span data-stu-id="3e26e-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-203">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e26e-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-205">El límite superior o la cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="3e26e-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="3e26e-206">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="3e26e-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e26e-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-210">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="3e26e-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="3e26e-211">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="3e26e-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="3e26e-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-215">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="3e26e-215">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="3e26e-216">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="3e26e-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-220">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="3e26e-220">The parent of the resource.</span></span> <span data-ttu-id="3e26e-221">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="3e26e-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-222">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="3e26e-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-225">IDENTIFICADOR del grupo de recursos desde el que se asigna el recurso.</span><span class="sxs-lookup"><span data-stu-id="3e26e-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="3e26e-226">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-227">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="3e26e-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-228">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e26e-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-230">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="3e26e-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="3e26e-231">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-232">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="3e26e-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-235">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="3e26e-235">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="3e26e-236">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="3e26e-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-238">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3e26e-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-240">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="3e26e-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="3e26e-241">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>



| <span data-ttu-id="3e26e-242">Value</span><span class="sxs-lookup"><span data-stu-id="3e26e-242">Value</span></span>                                                                        | <span data-ttu-id="3e26e-243">Significado</span><span class="sxs-lookup"><span data-stu-id="3e26e-243">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="3e26e-244"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3e26e-244"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3e26e-245">Otros</span><span class="sxs-lookup"><span data-stu-id="3e26e-245">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3e26e-246">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="3e26e-246">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-247">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3e26e-247">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-249">La cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="3e26e-249">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="3e26e-250">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-250">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-251">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="3e26e-251">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e26e-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-254">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e26e-254">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="3e26e-255">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="3e26e-255">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="3e26e-256">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-256">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="3e26e-257">**Peso**</span><span class="sxs-lookup"><span data-stu-id="3e26e-257">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e26e-258">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3e26e-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e26e-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e26e-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e26e-260">Prioridad relativa de esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="3e26e-260">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="3e26e-261">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="3e26e-261">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e26e-262">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e26e-262">Remarks</span></span>

<span data-ttu-id="3e26e-263">El acceso a la clase **MSVM \_ KvpExchangeComponentSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="3e26e-263">Access to the **Msvm\_KvpExchangeComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3e26e-264">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3e26e-264">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e26e-265">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e26e-265">Requirements</span></span>



| <span data-ttu-id="3e26e-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e26e-266">Requirement</span></span> | <span data-ttu-id="3e26e-267">Value</span><span class="sxs-lookup"><span data-stu-id="3e26e-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e26e-268">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e26e-268">Minimum supported client</span></span><br/> | <span data-ttu-id="3e26e-269">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e26e-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3e26e-270">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e26e-270">Minimum supported server</span></span><br/> | <span data-ttu-id="3e26e-271">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e26e-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e26e-272">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e26e-272">Namespace</span></span><br/>                | <span data-ttu-id="3e26e-273">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3e26e-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3e26e-274">MOF</span><span class="sxs-lookup"><span data-stu-id="3e26e-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e26e-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e26e-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e26e-276">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e26e-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e26e-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e26e-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e26e-278">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e26e-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e26e-279">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3e26e-279">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="3e26e-280">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3e26e-280">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

