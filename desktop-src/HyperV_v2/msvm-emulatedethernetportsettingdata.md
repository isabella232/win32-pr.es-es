---
description: Representa el estado configurado de un adaptador Ethernet emulado.
ms.assetid: 8BFD69D8-65B6-4C6F-9972-BD2F3C4FB5B8
title: Msvm_EmulatedEthernetPortSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPortSettingData
- Msvm_EmulatedEthernetPortSettingData.Caption
- Msvm_EmulatedEthernetPortSettingData.Description
- Msvm_EmulatedEthernetPortSettingData.InstanceID
- Msvm_EmulatedEthernetPortSettingData.ElementName
- Msvm_EmulatedEthernetPortSettingData.ResourceType
- Msvm_EmulatedEthernetPortSettingData.OtherResourceType
- Msvm_EmulatedEthernetPortSettingData.ResourceSubType
- Msvm_EmulatedEthernetPortSettingData.PoolID
- Msvm_EmulatedEthernetPortSettingData.ConsumerVisibility
- Msvm_EmulatedEthernetPortSettingData.HostResource
- Msvm_EmulatedEthernetPortSettingData.AllocationUnits
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantity
- Msvm_EmulatedEthernetPortSettingData.Reservation
- Msvm_EmulatedEthernetPortSettingData.Limit
- Msvm_EmulatedEthernetPortSettingData.Weight
- Msvm_EmulatedEthernetPortSettingData.AutomaticAllocation
- Msvm_EmulatedEthernetPortSettingData.AutomaticDeallocation
- Msvm_EmulatedEthernetPortSettingData.Parent
- Msvm_EmulatedEthernetPortSettingData.Connection
- Msvm_EmulatedEthernetPortSettingData.Address
- Msvm_EmulatedEthernetPortSettingData.MappingBehavior
- Msvm_EmulatedEthernetPortSettingData.AddressOnParent
- Msvm_EmulatedEthernetPortSettingData.VirtualQuantityUnits
- Msvm_EmulatedEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_EmulatedEthernetPortSettingData.OtherEndpointMode
- Msvm_EmulatedEthernetPortSettingData.StaticMacAddress
- Msvm_EmulatedEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f80a1f14f7a5bd388aec747f19ef84ecf0a32b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908605"
---
# <a name="msvm_emulatedethernetportsettingdata-class"></a><span data-ttu-id="67487-103">MSVM \_ EmulatedEthernetPortSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="67487-103">Msvm\_EmulatedEthernetPortSettingData class</span></span>

<span data-ttu-id="67487-104">Representa el estado configurado de un adaptador Ethernet emulado.</span><span class="sxs-lookup"><span data-stu-id="67487-104">Represents the configured state of an emulated Ethernet adapter.</span></span>

<span data-ttu-id="67487-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="67487-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67487-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67487-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  Caption = "Ethernet Port";
  string  Description = "Settings for the Microsoft Emulated Ethernet Port";
  string  InstanceID = "Microsoft:VMID\VDID\device-specific-data";
  string  ElementName = "Ethernet Port";
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft Emulated Ethernet Port";
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "Ports";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  boolean StaticMacAddress = TRUE;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="67487-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="67487-107">Members</span></span>

<span data-ttu-id="67487-108">La clase **MSVM \_ EmulatedEthernetPortSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="67487-108">The **Msvm\_EmulatedEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="67487-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67487-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67487-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67487-110">Properties</span></span>

<span data-ttu-id="67487-111">La clase **MSVM \_ EmulatedEthernetPortSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="67487-111">The **Msvm\_EmulatedEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67487-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="67487-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="67487-115">The address of the resource.</span></span> <span data-ttu-id="67487-116">Por ejemplo, la dirección MAC de un puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="67487-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="67487-117">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="67487-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="67487-118">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="67487-118">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="67487-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="67487-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-122">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="67487-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="67487-123">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="67487-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="67487-124">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="67487-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="67487-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="67487-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-128">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="67487-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="67487-129">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en "ports".</span><span class="sxs-lookup"><span data-stu-id="67487-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Ports".</span></span>

</dd> <dt>

<span data-ttu-id="67487-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="67487-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-131">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="67487-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67487-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-133">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="67487-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="67487-134">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="67487-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="67487-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="67487-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-136">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="67487-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67487-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-138">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="67487-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="67487-139">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="67487-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="67487-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="67487-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-143">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="67487-143">A short description of the object.</span></span> <span data-ttu-id="67487-144">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "puerto Ethernet".</span><span class="sxs-lookup"><span data-stu-id="67487-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="67487-145">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="67487-145">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-146">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="67487-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67487-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-148">Indica si un clúster supervisa este adaptador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="67487-148">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="67487-149">El valor predeterminado de esta propiedad es true si no se ha configurado.</span><span class="sxs-lookup"><span data-stu-id="67487-149">This property defaults to true if not configured.</span></span>

<span data-ttu-id="67487-150">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="67487-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="67487-151">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="67487-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="67487-152">**Connection**</span><span class="sxs-lookup"><span data-stu-id="67487-152">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-153">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="67487-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67487-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-155">Elemento al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="67487-155">The thing to which this resource is connected.</span></span> <span data-ttu-id="67487-156">Por ejemplo, una red con nombre o un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="67487-156">For example, a named network or switch port.</span></span> <span data-ttu-id="67487-157">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="67487-157">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="67487-158">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="67487-158">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="67487-159">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="67487-159">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-160">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67487-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67487-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-162">Describe la visibilidad de los consumidores para el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="67487-162">Describes the consumers visibility to the allocated resource.</span></span> <span data-ttu-id="67487-163">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 3 (virtualizado).</span><span class="sxs-lookup"><span data-stu-id="67487-163">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="67487-164">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67487-164">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-167">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="67487-167">A description of the object.</span></span> <span data-ttu-id="67487-168">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del puerto Ethernet emulado de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="67487-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Settings for the Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="67487-169">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="67487-169">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-170">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67487-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67487-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-172">El modo de configuración deseado para el extremo de VLAN.</span><span class="sxs-lookup"><span data-stu-id="67487-172">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="67487-173">Esta propiedad se usa para establecer el valor de la propiedad **OperationalEndpointMode** inicial en la instancia de la clase [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) asociada al puerto Ethernet de destino.</span><span class="sxs-lookup"><span data-stu-id="67487-173">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="67487-174">Vea la propiedad **OperationalEndpointMode** de la clase **MSVM \_ VLANEndpoint** para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="67487-174">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="67487-175">Esta propiedad se hereda de **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="67487-175">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="67487-176">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="67487-176">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-179">Nombre para mostrar configurable por el usuario para el dispositivo al que está asociada esta instancia de RASD.</span><span class="sxs-lookup"><span data-stu-id="67487-179">The user-configurable display name for the device this RASD instance is associated with.</span></span> <span data-ttu-id="67487-180">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y se establece en "puerto Ethernet".</span><span class="sxs-lookup"><span data-stu-id="67487-180">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is set to "Ethernet Port".</span></span> <span data-ttu-id="67487-181">Al cambiar esta propiedad, se cambiará el nombre del elemento del derivado del dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="67487-181">Changing this property will change the element name of the associated logical device derivative.</span></span>

<span data-ttu-id="67487-182">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="67487-182">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="67487-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="67487-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-184">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="67487-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67487-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-186">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="67487-186">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="67487-187">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="67487-187">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-190">Dentro del ámbito del espacio de nombres de la creación de instancias, **InstanceID** identifica de forma opaca y única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="67487-190">Within the scope of the instantiating namespace, **InstanceID** opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="67487-191">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "Microsoft:*VMID* \\ *VDID* \\ *Device-specific-Data*".</span><span class="sxs-lookup"><span data-stu-id="67487-191">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*VMID*\\*VDID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="67487-192">**Límite**</span><span class="sxs-lookup"><span data-stu-id="67487-192">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-193">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67487-193">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67487-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-195">El límite superior o la cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="67487-195">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="67487-196">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="67487-196">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="67487-197">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="67487-197">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67487-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67487-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-200">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="67487-200">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="67487-201">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="67487-201">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="67487-202">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="67487-202">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-205">Cadena que describe el tipo de modelo de punto de conexión de VLAN compatible con este extremo de VLAN.</span><span class="sxs-lookup"><span data-stu-id="67487-205">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="67487-206">Esta propiedad solo se usa cuando la propiedad **DesiredVLANEndpointMode** se establece en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="67487-206">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="67487-207">Esta propiedad debe establecerse en **null** cuando la propiedad **DesiredVLANEndpointMode** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="67487-207">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="67487-208">Esta propiedad se hereda de **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="67487-208">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="67487-209">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="67487-209">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-212">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y ResourceType está establecido en 0 ("otro").</span><span class="sxs-lookup"><span data-stu-id="67487-212">A string that describes the resource type when a well-defined value is not available and ResourceType is set to 0 ("Other").</span></span> <span data-ttu-id="67487-213">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="67487-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="67487-214">**Parent**</span><span class="sxs-lookup"><span data-stu-id="67487-214">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-217">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="67487-217">The parent of the resource.</span></span> <span data-ttu-id="67487-218">Por ejemplo, un controlador para la asignación actual.</span><span class="sxs-lookup"><span data-stu-id="67487-218">For example, a controller for the current allocation.</span></span> <span data-ttu-id="67487-219">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="67487-219">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="67487-220">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="67487-220">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-223">El grupo al que está asignado actualmente el recurso, o el grupo al que se asignará el recurso cuando se produzca la asignación.</span><span class="sxs-lookup"><span data-stu-id="67487-223">The pool the resource is currently allocated from, or the pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="67487-224">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="67487-224">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="67487-225">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="67487-225">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-226">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67487-226">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67487-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-228">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="67487-228">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="67487-229">En los sistemas que admiten el compromiso excesivo de recursos, este valor se utiliza normalmente para el control de admisión a fin de evitar que se acepte una asignación.</span><span class="sxs-lookup"><span data-stu-id="67487-229">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="67487-230">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="67487-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="67487-231">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="67487-231">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-234">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="67487-234">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="67487-235">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="67487-235">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="67487-236">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre se establece en "puerto Ethernet emulado de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="67487-236">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="67487-237">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="67487-237">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-238">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67487-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67487-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-240">Tipo de recurso al que se aplica esta configuración.</span><span class="sxs-lookup"><span data-stu-id="67487-240">The type of resource this setting applies to.</span></span> <span data-ttu-id="67487-241">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 10 (adaptador Ethernet).</span><span class="sxs-lookup"><span data-stu-id="67487-241">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="67487-242">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="67487-242">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-243">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="67487-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="67487-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-245">Indica si se va a usar una dirección MAC estática.</span><span class="sxs-lookup"><span data-stu-id="67487-245">Indicates whether to use a static MAC address.</span></span>

<span data-ttu-id="67487-246">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="67487-246">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="67487-247">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="67487-247">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-248">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67487-248">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67487-249">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-250">La cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="67487-250">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="67487-251">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="67487-251">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="67487-252">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="67487-252">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-253">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="67487-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67487-254">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-255">Especifica la unidad de medida para esta asignación de recursos.</span><span class="sxs-lookup"><span data-stu-id="67487-255">Specifies the unit of measurement for this resource allocation.</span></span> <span data-ttu-id="67487-256">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="67487-256">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="67487-257">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="67487-257">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="67487-258">**Peso**</span><span class="sxs-lookup"><span data-stu-id="67487-258">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67487-259">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67487-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67487-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="67487-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67487-261">Prioridad relativa de esta asignación en relación con otras asignaciones de la misma ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="67487-261">A relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="67487-262">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 0.</span><span class="sxs-lookup"><span data-stu-id="67487-262">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67487-263">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67487-263">Remarks</span></span>

<span data-ttu-id="67487-264">El acceso a la clase **MSVM \_ EmulatedEthernetPortSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="67487-264">Access to the **Msvm\_EmulatedEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="67487-265">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="67487-265">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="67487-266">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="67487-266">Examples</span></span>

<span data-ttu-id="67487-267">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="67487-267">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67487-268">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67487-268">Requirements</span></span>



| <span data-ttu-id="67487-269">Requisito</span><span class="sxs-lookup"><span data-stu-id="67487-269">Requirement</span></span> | <span data-ttu-id="67487-270">Value</span><span class="sxs-lookup"><span data-stu-id="67487-270">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67487-271">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67487-271">Minimum supported client</span></span><br/> | <span data-ttu-id="67487-272">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="67487-272">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="67487-273">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67487-273">Minimum supported server</span></span><br/> | <span data-ttu-id="67487-274">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="67487-274">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67487-275">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67487-275">Namespace</span></span><br/>                | <span data-ttu-id="67487-276">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="67487-276">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67487-277">MOF</span><span class="sxs-lookup"><span data-stu-id="67487-277">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67487-278"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67487-278"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67487-279">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67487-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67487-280"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67487-280"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67487-281">Vea también</span><span class="sxs-lookup"><span data-stu-id="67487-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67487-282">**\_ETHERNETPORTALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="67487-282">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="67487-283">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="67487-283">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

