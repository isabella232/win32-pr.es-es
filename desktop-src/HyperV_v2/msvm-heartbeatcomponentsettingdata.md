---
description: Representa el estado configurado del servicio de latido.
ms.assetid: 2946FA02-A751-4576-BB8A-004C80E21E5B
title: Msvm_HeartbeatComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponentSettingData
- Msvm_HeartbeatComponentSettingData.InstanceID
- Msvm_HeartbeatComponentSettingData.Caption
- Msvm_HeartbeatComponentSettingData.Description
- Msvm_HeartbeatComponentSettingData.ElementName
- Msvm_HeartbeatComponentSettingData.ResourceType
- Msvm_HeartbeatComponentSettingData.OtherResourceType
- Msvm_HeartbeatComponentSettingData.ResourceSubType
- Msvm_HeartbeatComponentSettingData.PoolID
- Msvm_HeartbeatComponentSettingData.ConsumerVisibility
- Msvm_HeartbeatComponentSettingData.HostResource
- Msvm_HeartbeatComponentSettingData.AllocationUnits
- Msvm_HeartbeatComponentSettingData.VirtualQuantity
- Msvm_HeartbeatComponentSettingData.Reservation
- Msvm_HeartbeatComponentSettingData.Limit
- Msvm_HeartbeatComponentSettingData.Weight
- Msvm_HeartbeatComponentSettingData.AutomaticAllocation
- Msvm_HeartbeatComponentSettingData.AutomaticDeallocation
- Msvm_HeartbeatComponentSettingData.Parent
- Msvm_HeartbeatComponentSettingData.Connection
- Msvm_HeartbeatComponentSettingData.Address
- Msvm_HeartbeatComponentSettingData.MappingBehavior
- Msvm_HeartbeatComponentSettingData.AddressOnParent
- Msvm_HeartbeatComponentSettingData.VirtualQuantityUnits
- Msvm_HeartbeatComponentSettingData.EnabledState
- Msvm_HeartbeatComponentSettingData.ErrorThreshold
- Msvm_HeartbeatComponentSettingData.Interval
- Msvm_HeartbeatComponentSettingData.Latency
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a36afbd8ab17a3fc2dfddb99b0a648fddbada415
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686949"
---
# <a name="msvm_heartbeatcomponentsettingdata-class"></a><span data-ttu-id="e7dd8-103">MSVM \_ HeartbeatComponentSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="e7dd8-103">Msvm\_HeartbeatComponentSettingData class</span></span>

<span data-ttu-id="e7dd8-104">Representa el estado configurado del servicio de latido.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-104">Represents the configured state of the heartbeat service.</span></span>

<span data-ttu-id="e7dd8-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7dd8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7dd8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Heartbeat";
  string  Description = "Microsoft Heartbeat Service Setting Data";
  string  ElementName = "Heartbeat";
  uint16  ResourceType = 1;
  string  OtherResourceType = "Microsoft Heartbeat Component";
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Integration Components";
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
  uint32  ErrorThreshold = 2;
  uint32  Interval = 2000;
  uint32  Latency = 1000;
};
```

## <a name="members"></a><span data-ttu-id="e7dd8-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e7dd8-107">Members</span></span>

<span data-ttu-id="e7dd8-108">La clase **MSVM \_ HeartbeatComponentSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e7dd8-108">The **Msvm\_HeartbeatComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e7dd8-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7dd8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e7dd8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7dd8-110">Properties</span></span>

<span data-ttu-id="e7dd8-111">La clase **MSVM \_ HeartbeatComponentSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-111">The **Msvm\_HeartbeatComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e7dd8-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-115">The address of the resource.</span></span> <span data-ttu-id="e7dd8-116">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-116">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-117">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-117">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-120">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-120">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="e7dd8-121">Las propiedades **principales** de / **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-121">The **Parent**/**AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="e7dd8-122">Por ejemplo, si el elemento primario es un controlador PCI, esta propiedad especificaría la ranura PCI de este dispositivo secundario.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-122">For example, if the parent is a PCI Controller, this property would specify the PCI slot of this child device.</span></span> <span data-ttu-id="e7dd8-123">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-127">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="e7dd8-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="e7dd8-128">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en "componentes de integración".</span><span class="sxs-lookup"><span data-stu-id="e7dd8-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Integration Components".</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-132">Indica si el recurso se asigna automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-132">Indicates whether the resource is automatically allocated.</span></span> <span data-ttu-id="e7dd8-133">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-137">Indica si el recurso se ha anulado la asignación automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-137">Indicates whether the resource is automatically de-allocated.</span></span> <span data-ttu-id="e7dd8-138">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-142">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-142">A short description of the object.</span></span> <span data-ttu-id="e7dd8-143">Esta propiedad se hereda de la clase de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y siempre se establece en "latido".</span><span class="sxs-lookup"><span data-stu-id="e7dd8-143">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-144">**Connection**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-144">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-145">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-145">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-147">Elemento al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-147">The thing to which this resource is connected.</span></span> <span data-ttu-id="e7dd8-148">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-148">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-149">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-149">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-152">Describe la visibilidad de los consumidores en el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-152">Describes the consumers' visibility to the allocated resource.</span></span> <span data-ttu-id="e7dd8-153">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre está establecida en 3 (virtualizado).</span><span class="sxs-lookup"><span data-stu-id="e7dd8-153">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-154">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-155">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-157">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-157">A description of the object.</span></span> <span data-ttu-id="e7dd8-158">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "datos de configuración del servicio de latido de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="e7dd8-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-159">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-159">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-162">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-162">A display name for the object.</span></span> <span data-ttu-id="e7dd8-163">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "latido".</span><span class="sxs-lookup"><span data-stu-id="e7dd8-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Heartbeat".</span></span> <span data-ttu-id="e7dd8-164">Al cambiar esta propiedad, se cambiará la propiedad **ElementName** del derivado de [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) asociado.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-164">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="e7dd8-165">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e7dd8-165">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-166">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-166">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-169">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-169">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="e7dd8-170">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e7dd8-170">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="e7dd8-171">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="e7dd8-171">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="e7dd8-172">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="e7dd8-172">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e7dd8-173">**ErrorThreshold**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-173">**ErrorThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-174">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-176">Configuración de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-176">An administrator's startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e7dd8-177">Esta propiedad siempre se establece en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="e7dd8-177">This property is always set to 2 (Enabled).</span></span>

<span data-ttu-id="e7dd8-178">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e7dd8-178">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-179">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-179">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-180">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-182">Expone una asignación específica para hospedar o los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-182">Exposes a specific assignment to host or underlying resources.</span></span> <span data-ttu-id="e7dd8-183">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-184">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-184">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-187">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-187">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-188">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-188">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e7dd8-189">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) y siempre se establece en "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="e7dd8-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-190">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-190">**Interval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-191">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-193">El intervalo, en milisegundos, entre los intentos de ping.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-193">The interval, in milliseconds, between ping attempts.</span></span> <span data-ttu-id="e7dd8-194">Siempre se establece en 2000.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-194">This is always set to 2000.</span></span>

<span data-ttu-id="e7dd8-195">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e7dd8-195">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-196">**Latency**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-196">**Latency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-197">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-199">La latencia máxima esperada, en milisegundos, entre un ping de solicitud y una respuesta antes de que una solicitud determinada se considere quitada.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-199">The maximum expected latency, in milliseconds, between a request ping and a response before a given request is considered dropped.</span></span> <span data-ttu-id="e7dd8-200">Esta propiedad siempre se establece en 1000.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-200">This property is always set to 1000.</span></span>

<span data-ttu-id="e7dd8-201">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e7dd8-201">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-202">**Límite**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-202">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-203">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-205">El límite superior o la cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-205">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="e7dd8-206">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-206">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-207">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-207">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-210">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-210">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="e7dd8-211">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-211">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-212">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-212">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-213">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-215">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y la propiedad **resourcetype** tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="e7dd8-215">A string that describes the resource type when a well-defined value is not available and the **ResourceType** property has the value 1 (Other).</span></span> <span data-ttu-id="e7dd8-216">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en "Microsoft Heartbeat Component".</span><span class="sxs-lookup"><span data-stu-id="e7dd8-216">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "Microsoft Heartbeat Component".</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-217">**Parent**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-217">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-220">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-220">The parent of the resource.</span></span> <span data-ttu-id="e7dd8-221">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-222">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-222">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-225">IDENTIFICADOR del grupo de recursos desde el que se asigna el recurso.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-225">The ID of the resource pool from which the resource is allocated.</span></span> <span data-ttu-id="e7dd8-226">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="e7dd8-226">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-227">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-227">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-228">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-228">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-230">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-230">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="e7dd8-231">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-231">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-232">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-232">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-235">Un subtipo específico de la implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-235">An implementation specific subtype for this resource.</span></span> <span data-ttu-id="e7dd8-236">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-238">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-240">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-240">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="e7dd8-241">Esta propiedad se hereda de la clase [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="e7dd8-241">This property is inherited from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class and is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-242">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-242">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-243">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-243">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-245">La cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-245">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="e7dd8-246">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-246">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-247">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-247">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-248">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-250">Especifica las unidades utilizadas por la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="e7dd8-250">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="e7dd8-251">Por ejemplo, si ResourceType = processor, el valor de la propiedad **VirtualQuantityUnits** se puede establecer en "Count", lo que indica que el valor de la propiedad **VirtualQuantity** se expresa como un recuento.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-251">For example, if ResourceType=Processor, the value of the **VirtualQuantityUnits** property can be set to "count", indicating that the value of the **VirtualQuantity** property is expressed as a count.</span></span> <span data-ttu-id="e7dd8-252">Si ResourceType = Memory, el valor de la propiedad **VirtualQuantityUnits** se puede establecer en "bytes \* 10 ^ 3", lo que indica que el valor de la propiedad **VirtualQuantity** se expresa en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-252">If ResourceType=Memory, the value of the **VirtualQuantityUnits** property can be set to "bytes\*10^3", indicating that the value of the **VirtualQuantity** property is expressed in kilobytes.</span></span> <span data-ttu-id="e7dd8-253">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre se establece en "Count".</span><span class="sxs-lookup"><span data-stu-id="e7dd8-253">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to "count".</span></span>

</dd> <dt>

<span data-ttu-id="e7dd8-254">**Peso**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-254">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e7dd8-255">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e7dd8-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e7dd8-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e7dd8-257">Prioridad relativa de esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-257">The relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="e7dd8-258">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) and is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7dd8-259">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7dd8-259">Remarks</span></span>

<span data-ttu-id="e7dd8-260">El acceso a la clase **MSVM \_ HeartbeatComponentSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="e7dd8-260">Access to the **Msvm\_HeartbeatComponentSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e7dd8-261">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e7dd8-261">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7dd8-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7dd8-262">Requirements</span></span>



| <span data-ttu-id="e7dd8-263">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7dd8-263">Requirement</span></span> | <span data-ttu-id="e7dd8-264">Value</span><span class="sxs-lookup"><span data-stu-id="e7dd8-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7dd8-265">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7dd8-265">Minimum supported client</span></span><br/> | <span data-ttu-id="e7dd8-266">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7dd8-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e7dd8-267">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7dd8-267">Minimum supported server</span></span><br/> | <span data-ttu-id="e7dd8-268">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7dd8-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e7dd8-269">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e7dd8-269">Namespace</span></span><br/>                | <span data-ttu-id="e7dd8-270">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e7dd8-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e7dd8-271">MOF</span><span class="sxs-lookup"><span data-stu-id="e7dd8-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7dd8-272"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7dd8-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7dd8-273">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7dd8-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7dd8-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e7dd8-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e7dd8-275">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7dd8-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7dd8-276">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-276">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="e7dd8-277">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-277">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[<span data-ttu-id="e7dd8-278">**MSVM \_ HeartbeatComponentSettingData**</span><span class="sxs-lookup"><span data-stu-id="e7dd8-278">**Msvm\_HeartbeatComponentSettingData**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponentsettingdata)
</dt> </dl>

 

