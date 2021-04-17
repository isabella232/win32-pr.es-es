---
description: Representa el estado configurado de un adaptador Ethernet sintético.
ms.assetid: BE895BAF-7766-43A2-9659-3ABA97A16134
title: Msvm_SyntheticEthernetPortSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPortSettingData
- Msvm_SyntheticEthernetPortSettingData.InstanceID
- Msvm_SyntheticEthernetPortSettingData.Caption
- Msvm_SyntheticEthernetPortSettingData.Description
- Msvm_SyntheticEthernetPortSettingData.ElementName
- Msvm_SyntheticEthernetPortSettingData.ResourceType
- Msvm_SyntheticEthernetPortSettingData.OtherResourceType
- Msvm_SyntheticEthernetPortSettingData.ResourceSubType
- Msvm_SyntheticEthernetPortSettingData.PoolID
- Msvm_SyntheticEthernetPortSettingData.ConsumerVisibility
- Msvm_SyntheticEthernetPortSettingData.HostResource
- Msvm_SyntheticEthernetPortSettingData.AllocationUnits
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantity
- Msvm_SyntheticEthernetPortSettingData.Reservation
- Msvm_SyntheticEthernetPortSettingData.Limit
- Msvm_SyntheticEthernetPortSettingData.Weight
- Msvm_SyntheticEthernetPortSettingData.AutomaticAllocation
- Msvm_SyntheticEthernetPortSettingData.AutomaticDeallocation
- Msvm_SyntheticEthernetPortSettingData.Parent
- Msvm_SyntheticEthernetPortSettingData.Connection
- Msvm_SyntheticEthernetPortSettingData.Address
- Msvm_SyntheticEthernetPortSettingData.MappingBehavior
- Msvm_SyntheticEthernetPortSettingData.AddressOnParent
- Msvm_SyntheticEthernetPortSettingData.VirtualQuantityUnits
- Msvm_SyntheticEthernetPortSettingData.DesiredVLANEndpointMode
- Msvm_SyntheticEthernetPortSettingData.OtherEndpointMode
- Msvm_SyntheticEthernetPortSettingData.VirtualSystemIdentifiers
- Msvm_SyntheticEthernetPortSettingData.DeviceNamingEnabled
- Msvm_SyntheticEthernetPortSettingData.AllowPacketDirect
- Msvm_SyntheticEthernetPortSettingData.StaticMacAddress
- Msvm_SyntheticEthernetPortSettingData.ClusterMonitored
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5b31b02782c0f215f70f3bb5d2767b01294c7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686610"
---
# <a name="msvm_syntheticethernetportsettingdata-class"></a><span data-ttu-id="fab45-103">MSVM \_ SyntheticEthernetPortSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="fab45-103">Msvm\_SyntheticEthernetPortSettingData class</span></span>

<span data-ttu-id="fab45-104">Representa el estado configurado de un adaptador Ethernet sintético.</span><span class="sxs-lookup"><span data-stu-id="fab45-104">Represents the configured state of a synthetic Ethernet adapter.</span></span>

<span data-ttu-id="fab45-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fab45-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab45-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fab45-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPortSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Ethernet Port Default Settings";
  string  Description = "Describes the default settings for the virtual Ethernet port resources.";
  string  ElementName;
  uint16  ResourceType = 10;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic Ethernet Port";
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
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  string  VirtualSystemIdentifiers[];
  boolean DeviceNamingEnabled = FALSE;
  boolean AllowPacketDirect = FALSE;
  boolean StaticMacAddress = False;
  boolean ClusterMonitored = TRUE;
};
```

## <a name="members"></a><span data-ttu-id="fab45-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fab45-107">Members</span></span>

<span data-ttu-id="fab45-108">La clase **MSVM \_ SyntheticEthernetPortSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fab45-108">The **Msvm\_SyntheticEthernetPortSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fab45-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fab45-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fab45-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fab45-110">Properties</span></span>

<span data-ttu-id="fab45-111">La clase **MSVM \_ SyntheticEthernetPortSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fab45-111">The **Msvm\_SyntheticEthernetPortSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fab45-112">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="fab45-112">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-115">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="fab45-115">The address of the resource.</span></span> <span data-ttu-id="fab45-116">Por ejemplo, la dirección MAC de un puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="fab45-116">For example, the MAC address of a Ethernet port.</span></span> <span data-ttu-id="fab45-117">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="fab45-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-121">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="fab45-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="fab45-122">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="fab45-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="fab45-123">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="fab45-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-127">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="fab45-127">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="fab45-128">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-129">**AllowPacketDirect**</span><span class="sxs-lookup"><span data-stu-id="fab45-129">**AllowPacketDirect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fab45-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fab45-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fab45-132">Indica si la proyección de PacketDirect está habilitada para la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fab45-132">Indicates if PacketDirect projection is enabled for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="fab45-133">Agregado en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fab45-133">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="fab45-134">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="fab45-134">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fab45-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-137">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fab45-137">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="fab45-138">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-139">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="fab45-139">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fab45-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-142">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fab45-142">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="fab45-143">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-143">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-144">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fab45-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-147">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="fab45-147">A short description of the object.</span></span> <span data-ttu-id="fab45-148">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fab45-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-149">**ClusterMonitored**</span><span class="sxs-lookup"><span data-stu-id="fab45-149">**ClusterMonitored**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-150">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fab45-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-152">Indica si un clúster supervisa este adaptador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="fab45-152">Indicates whether this ethernet adapter is monitored by a cluster.</span></span> <span data-ttu-id="fab45-153">El valor predeterminado de esta propiedad es true si no se ha configurado.</span><span class="sxs-lookup"><span data-stu-id="fab45-153">This property defaults to true if not configured.</span></span>

<span data-ttu-id="fab45-154">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fab45-154">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="fab45-155">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="fab45-155">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="fab45-156">**Connection**</span><span class="sxs-lookup"><span data-stu-id="fab45-156">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-157">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fab45-157">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fab45-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-159">Elemento al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="fab45-159">The thing to which this resource is connected.</span></span> <span data-ttu-id="fab45-160">Por ejemplo, una red con nombre o un puerto de conmutador.</span><span class="sxs-lookup"><span data-stu-id="fab45-160">For example, a named network or switch port.</span></span> <span data-ttu-id="fab45-161">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-161">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-162">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="fab45-162">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-163">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fab45-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-165">La visibilidad de los consumidores del recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="fab45-165">The consumers visibility to the allocated resource.</span></span> <span data-ttu-id="fab45-166">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 3 (virtualizado).</span><span class="sxs-lookup"><span data-stu-id="fab45-166">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-167">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fab45-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-170">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="fab45-170">A description of the object.</span></span> <span data-ttu-id="fab45-171">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fab45-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-172">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="fab45-172">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-173">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fab45-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-175">El modo de configuración deseado para el extremo de VLAN.</span><span class="sxs-lookup"><span data-stu-id="fab45-175">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="fab45-176">Esta propiedad se usa para establecer el valor de la propiedad **OperationalEndpointMode** inicial en la instancia de la clase [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) asociada al puerto Ethernet de destino.</span><span class="sxs-lookup"><span data-stu-id="fab45-176">This property is used to set the initial **OperationalEndpointMode** property value in the instance of the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="fab45-177">Vea la propiedad **OperationalEndpointMode** de la clase **MSVM \_ VLANEndpoint** para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="fab45-177">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="fab45-178">Esta propiedad se hereda de **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="fab45-178">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="fab45-179">**DeviceNamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="fab45-179">**DeviceNamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-180">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fab45-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-182">Indica si este adaptador Ethernet admite nombres de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fab45-182">Indicates whether this ethernet adapter supports device naming.</span></span>

<span data-ttu-id="fab45-183">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fab45-183">This is a read-only property, but it can be changed using the [**ModifyVirtualSystemResources**](https://www.bing.com/search?q=**ModifyVirtualSystemResources**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="fab45-184">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="fab45-184">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="fab45-185">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fab45-185">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-186">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-188">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="fab45-188">A short description of the object.</span></span> <span data-ttu-id="fab45-189">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fab45-189">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-190">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="fab45-190">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-191">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fab45-191">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fab45-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-193">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="fab45-193">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fab45-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fab45-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fab45-197">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="fab45-197">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fab45-198">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="fab45-198">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fab45-199">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fab45-199">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-200">**Límite**</span><span class="sxs-lookup"><span data-stu-id="fab45-200">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-201">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fab45-201">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-203">El límite superior o la cantidad máxima de recursos que se concederán para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="fab45-203">The upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="fab45-204">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-204">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-205">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="fab45-205">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-206">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fab45-206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-208">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="fab45-208">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="fab45-209">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-209">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-210">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="fab45-210">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-211">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-213">Cadena que describe el tipo de modelo de punto de conexión de VLAN compatible con este extremo de VLAN.</span><span class="sxs-lookup"><span data-stu-id="fab45-213">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="fab45-214">Esta propiedad solo se usa cuando la propiedad **DesiredVLANEndpointMode** se establece en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="fab45-214">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="fab45-215">Esta propiedad debe establecerse en **null** cuando la propiedad **DesiredVLANEndpointMode** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="fab45-215">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="fab45-216">Esta propiedad se hereda de **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="fab45-216">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="fab45-217">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="fab45-217">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-220">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** se establece en "Other" (0).</span><span class="sxs-lookup"><span data-stu-id="fab45-220">A string that describes the resource type when a well-defined value is not available and **ResourceType** is set to "Other" (0).</span></span> <span data-ttu-id="fab45-221">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="fab45-221">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fab45-222">**Parent**</span><span class="sxs-lookup"><span data-stu-id="fab45-222">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-223">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-224">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-225">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="fab45-225">The parent of the resource.</span></span> <span data-ttu-id="fab45-226">Por ejemplo, un controlador para la asignación actual.</span><span class="sxs-lookup"><span data-stu-id="fab45-226">For example, a controller for the current allocation.</span></span> <span data-ttu-id="fab45-227">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-228">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="fab45-228">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-231">Grupo al que está asignado actualmente el recurso, o a qué grupo se asignará el recurso cuando se produzca la asignación.</span><span class="sxs-lookup"><span data-stu-id="fab45-231">The pool the resource is currently allocated from, or which pool the resource will be allocated from when the allocation occurs.</span></span> <span data-ttu-id="fab45-232">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-233">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="fab45-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-234">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fab45-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-236">La cantidad de recursos que se garantiza que estarán disponibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="fab45-236">The amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="fab45-237">En los sistemas que admiten el compromiso excesivo de recursos, este valor se utiliza normalmente para el control de admisión a fin de evitar que se acepte una asignación.</span><span class="sxs-lookup"><span data-stu-id="fab45-237">On systems that support over-commitment of resources, this value is typically used for admission control to prevent an allocation from being accepted.</span></span> <span data-ttu-id="fab45-238">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-238">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-239">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="fab45-239">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-240">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-242">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="fab45-242">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="fab45-243">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="fab45-243">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="fab45-244">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-244">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-245">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="fab45-245">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-246">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fab45-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-247">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-248">Tipo de recurso al que se aplica esta configuración.</span><span class="sxs-lookup"><span data-stu-id="fab45-248">The type of resource this setting applies to.</span></span> <span data-ttu-id="fab45-249">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 10 (adaptador Ethernet).</span><span class="sxs-lookup"><span data-stu-id="fab45-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 10 (Ethernet Adapter).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-250">**StaticMacAddress**</span><span class="sxs-lookup"><span data-stu-id="fab45-250">**StaticMacAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-251">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fab45-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-253">Especifica si la dirección MAC es estática.</span><span class="sxs-lookup"><span data-stu-id="fab45-253">Specifies if the MAC address is static.</span></span>

</dd> <dt>

<span data-ttu-id="fab45-254">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="fab45-254">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-255">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fab45-255">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-257">La cantidad de recursos que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="fab45-257">The quantity of resources presented to the consumer.</span></span> <span data-ttu-id="fab45-258">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-258">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-259">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="fab45-259">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-260">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fab45-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-261">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-262">Especifica la unidad de medida para la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="fab45-262">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="fab45-263">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fab45-263">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="fab45-264">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-264">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-265">**VirtualSystemIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="fab45-265">**VirtualSystemIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-266">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fab45-266">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fab45-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fab45-268">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="fab45-268">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fab45-269">Matriz de cadenas de identificadores de este recurso que se presenta al sistema operativo de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fab45-269">A string array of identifiers of this resource presented to the virtual machine's operating system.</span></span> <span data-ttu-id="fab45-270">Los índices y valores por índice se definen por cada recurso (es decir, para cada valor de propiedad **resourcetype** enumerado).</span><span class="sxs-lookup"><span data-stu-id="fab45-270">The indexes and values per index are defined on a per resource basis (that is, for each enumerated **ResourceType** property value).</span></span>

</dd> <dt>

<span data-ttu-id="fab45-271">**Peso**</span><span class="sxs-lookup"><span data-stu-id="fab45-271">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fab45-272">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fab45-272">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fab45-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fab45-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fab45-274">Prioridad relativa de esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="fab45-274">A relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="fab45-275">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="fab45-275">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fab45-276">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fab45-276">Remarks</span></span>

<span data-ttu-id="fab45-277">El acceso a la clase **MSVM \_ SyntheticEthernetPortSettingData** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="fab45-277">Access to the **Msvm\_SyntheticEthernetPortSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fab45-278">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fab45-278">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="fab45-279">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fab45-279">Examples</span></span>

<span data-ttu-id="fab45-280">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fab45-280">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fab45-281">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fab45-281">Requirements</span></span>



| <span data-ttu-id="fab45-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab45-282">Requirement</span></span> | <span data-ttu-id="fab45-283">Value</span><span class="sxs-lookup"><span data-stu-id="fab45-283">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab45-284">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fab45-284">Minimum supported client</span></span><br/> | <span data-ttu-id="fab45-285">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fab45-285">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fab45-286">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fab45-286">Minimum supported server</span></span><br/> | <span data-ttu-id="fab45-287">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fab45-287">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fab45-288">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fab45-288">Namespace</span></span><br/>                | <span data-ttu-id="fab45-289">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fab45-289">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fab45-290">MOF</span><span class="sxs-lookup"><span data-stu-id="fab45-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fab45-291"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fab45-291"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fab45-292">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fab45-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fab45-293"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fab45-293"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fab45-294">Vea también</span><span class="sxs-lookup"><span data-stu-id="fab45-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab45-295">**\_ETHERNETPORTALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fab45-295">**CIM\_EthernetPortAllocationSettingData**</span></span>](cim-ethernetportallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="fab45-296">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="fab45-296">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

