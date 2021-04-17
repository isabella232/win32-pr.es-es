---
description: Representa una solicitud de asignación para un puerto de conmutador estático o dinámico, o representa la configuración activa de un puerto de conmutador estático o dinámico asignado actualmente.
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Msvm_EthernetPortAllocationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a310daf30127aec5069efcf7ca4fd5ead9277e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687646"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a><span data-ttu-id="23486-103">MSVM \_ EthernetPortAllocationSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="23486-103">Msvm\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="23486-104">Representa una solicitud de asignación para un puerto de conmutador estático o dinámico, o representa la configuración activa de un puerto de conmutador estático o dinámico asignado actualmente.</span><span class="sxs-lookup"><span data-stu-id="23486-104">Represents an allocation request for a static or dynamic switch port, or represents the active configuration of a currently allocated static or dynamic switch port.</span></span> <span data-ttu-id="23486-105">Una solicitud de asignación de un puerto de conmutador dinámico también se denomina solicitud de conexión.</span><span class="sxs-lookup"><span data-stu-id="23486-105">An allocation request for a dynamic switch port is also known as a connection request.</span></span>

<span data-ttu-id="23486-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="23486-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="23486-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23486-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a><span data-ttu-id="23486-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="23486-108">Members</span></span>

<span data-ttu-id="23486-109">La clase **MSVM \_ EthernetPortAllocationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="23486-109">The **Msvm\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="23486-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23486-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="23486-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="23486-111">Properties</span></span>

<span data-ttu-id="23486-112">La clase **MSVM \_ EthernetPortAllocationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="23486-112">The **Msvm\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="23486-113">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="23486-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-116">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="23486-116">The address of the resource.</span></span> <span data-ttu-id="23486-117">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-118">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="23486-118">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-121">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="23486-121">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="23486-122">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="23486-122">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="23486-123">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-123">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-124">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="23486-124">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-127">Unidad de asignación utilizada por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="23486-127">The unit of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="23486-128">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-128">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-129">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="23486-129">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-130">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="23486-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23486-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-132">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="23486-132">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="23486-133">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-133">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-134">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="23486-134">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="23486-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="23486-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-137">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="23486-137">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="23486-138">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-138">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-139">**Caption**</span><span class="sxs-lookup"><span data-stu-id="23486-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23486-142">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="23486-142">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="23486-143">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="23486-143">A short description of the object.</span></span> <span data-ttu-id="23486-144">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="23486-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="23486-145">**CompartmentGuid**</span><span class="sxs-lookup"><span data-stu-id="23486-145">**CompartmentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="23486-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23486-148">Esta propiedad especifica el compartimiento de red de destino para el puerto.</span><span class="sxs-lookup"><span data-stu-id="23486-148">This property specifies the target network compartment for the port.</span></span> <span data-ttu-id="23486-149">Solo se admite para los adaptadores internos.</span><span class="sxs-lookup"><span data-stu-id="23486-149">It is only supported for internal adapters.</span></span>

> [!Note]  
> <span data-ttu-id="23486-150">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="23486-150">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="23486-151">**Connection**</span><span class="sxs-lookup"><span data-stu-id="23486-151">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-152">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="23486-152">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23486-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-154">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="23486-154">The device to which this resource is connected.</span></span> <span data-ttu-id="23486-155">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-155">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-156">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="23486-156">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-157">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23486-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23486-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-159">Visibilidad del consumidor en el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="23486-159">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="23486-160">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 3 (virtualizado).</span><span class="sxs-lookup"><span data-stu-id="23486-160">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 3 (Virtualized).</span></span>

</dd> <dt>

<span data-ttu-id="23486-161">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="23486-161">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-164">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="23486-164">A description of the object.</span></span> <span data-ttu-id="23486-165">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="23486-165">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Settings".</span></span>

</dd> <dt>

<span data-ttu-id="23486-166">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="23486-166">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23486-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23486-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-169">El modo de configuración deseado para el extremo de VLAN.</span><span class="sxs-lookup"><span data-stu-id="23486-169">The desired configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="23486-170">Esta propiedad se usa para establecer el valor de la propiedad **OperationalEndpointMode** inicial en la instancia de la clase [**MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md) asociada al puerto Ethernet de destino.</span><span class="sxs-lookup"><span data-stu-id="23486-170">This property is used to set the initial **OperationalEndpointMode** property value in the instance of [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) class associated with the targeted Ethernet port.</span></span> <span data-ttu-id="23486-171">Vea la propiedad **OperationalEndpointMode** de la clase **MSVM \_ VLANEndpoint** para ver los posibles valores.</span><span class="sxs-lookup"><span data-stu-id="23486-171">See the **OperationalEndpointMode** property of the **Msvm\_VLANEndpoint** class for possible values.</span></span> <span data-ttu-id="23486-172">Esta propiedad se hereda de **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="23486-172">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="23486-173">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="23486-173">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-176">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="23486-176">A display name for the object.</span></span> <span data-ttu-id="23486-177">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="23486-177">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="23486-178">Al cambiar esta propiedad, se cambiará el nombre del elemento del derivado del dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="23486-178">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="23486-179">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="23486-179">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-180">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23486-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23486-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-182">Indica si la solicitud de asignación está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="23486-182">Indicates whether the allocation request is enabled or disabled.</span></span> <span data-ttu-id="23486-183">Cuando una solicitud de asignación se marca como deshabilitada (3), la asignación no se procesa.</span><span class="sxs-lookup"><span data-stu-id="23486-183">When an allocation request is marked as Disabled (3), then the allocation is not processed.</span></span> <span data-ttu-id="23486-184">El **EnabledState** de una configuración activa siempre está marcado como habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="23486-184">The **EnabledState** for an active configuration is always marked as Enabled (2).</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="23486-185">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="23486-185">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="23486-186">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="23486-186">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="23486-187">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="23486-187">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-188">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="23486-188">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23486-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-190">Solo se puede asignar un recurso de host a cada dispositivo del conmutador virtual, por lo que solo se puede establecer el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="23486-190">Only one host resource can be assigned to each device in the virtual switch, so only the first element of this array can be set.</span></span> <span data-ttu-id="23486-191">En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="23486-191">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="23486-192">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-192">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="23486-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="23486-196">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="23486-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="23486-197">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="23486-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="23486-198">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="23486-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="23486-199">**LastKnownSwitchName**</span><span class="sxs-lookup"><span data-stu-id="23486-199">**LastKnownSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-202">El último nombre descriptivo conocido del conmutador al que este puerto tenía una afinidad fuerte, si lo hubiera.</span><span class="sxs-lookup"><span data-stu-id="23486-202">The last known friendly name of the switch this port had a hard affinity to, if any.</span></span>

> [!Note]  
> <span data-ttu-id="23486-203">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="23486-203">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="23486-204">**Límite**</span><span class="sxs-lookup"><span data-stu-id="23486-204">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-205">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="23486-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="23486-206">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-207">La cantidad máxima de recursos de host correspondientes que puede consumir el conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="23486-207">The maximum amount of corresponding host resources that can be consumed by the virtual switch.</span></span> <span data-ttu-id="23486-208">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-208">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-209">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="23486-209">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-210">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23486-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23486-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-212">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="23486-212">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="23486-213">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-213">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-214">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="23486-214">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-215">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-217">Cadena que describe el tipo de modelo de punto de conexión de VLAN compatible con este extremo de VLAN.</span><span class="sxs-lookup"><span data-stu-id="23486-217">A string that describes the type of VLAN endpoint model that is supported by this VLAN endpoint.</span></span> <span data-ttu-id="23486-218">Esta propiedad solo se usa cuando la propiedad **DesiredVLANEndpointMode** se establece en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="23486-218">This property is only used when the **DesiredVLANEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="23486-219">Esta propiedad debe establecerse en **null** cuando la propiedad **DesiredVLANEndpointMode** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="23486-219">This property should be set to **Null** when the **DesiredVLANEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="23486-220">Esta propiedad se hereda de **\_ EthernetPortAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="23486-220">This property is inherited from **CIM\_EthernetPortAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="23486-221">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="23486-221">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-224">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="23486-224">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1 (Other).</span></span> <span data-ttu-id="23486-225">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="23486-225">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="23486-226">**Parent**</span><span class="sxs-lookup"><span data-stu-id="23486-226">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-229">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="23486-229">The parent of the resource.</span></span> <span data-ttu-id="23486-230">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-230">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-231">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="23486-231">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-234">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="23486-234">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="23486-235">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-235">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-236">**RequiredFeatureHints**</span><span class="sxs-lookup"><span data-stu-id="23486-236">**RequiredFeatureHints**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-237">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="23486-237">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23486-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-239">La lista de nombres para mostrar que corresponden a cada entrada de la matriz **RequiredFeatures** .</span><span class="sxs-lookup"><span data-stu-id="23486-239">The list of display names that correspond to each entry in the **RequiredFeatures** array.</span></span>

</dd> <dt>

<span data-ttu-id="23486-240">**RequiredFeatures**</span><span class="sxs-lookup"><span data-stu-id="23486-240">**RequiredFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-241">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="23486-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="23486-242">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="23486-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23486-243">Lista de identificadores de características que representan todas las características necesarias para un puerto.</span><span class="sxs-lookup"><span data-stu-id="23486-243">The list of feature identifiers that represent all the features that are required for a port.</span></span>

</dd> <dt>

<span data-ttu-id="23486-244">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="23486-244">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-245">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="23486-245">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="23486-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-247">La cantidad de recursos reservados para su uso por el conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="23486-247">The amount of resources that are reserved for use by the virtual switch.</span></span> <span data-ttu-id="23486-248">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-248">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-249">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="23486-249">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-252">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="23486-252">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="23486-253">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="23486-253">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="23486-254">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-255">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="23486-255">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-256">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="23486-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="23486-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-258">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="23486-258">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="23486-259">Esta propiedad se hereda de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)y siempre está establecida en 33 (conexión Ethernet).</span><span class="sxs-lookup"><span data-stu-id="23486-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), and it is always set to 33 (Ethernet connection).</span></span>

</dd> <dt>

<span data-ttu-id="23486-260">**TestReplicaPoolID**</span><span class="sxs-lookup"><span data-stu-id="23486-260">**TestReplicaPoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-262">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="23486-262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23486-263">Especifica el grupo de recursos de red desde el que se asignará una conexión al sistema de réplica de prueba cuando se cree.</span><span class="sxs-lookup"><span data-stu-id="23486-263">Specifies the network resource pool from which a connection will be allocated to the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="23486-264">**TestReplicaSwitchName**</span><span class="sxs-lookup"><span data-stu-id="23486-264">**TestReplicaSwitchName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-265">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-266">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="23486-266">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="23486-267">Especifica el nombre para mostrar del conmutador de red virtual al que se asignará una conexión para el sistema de réplica de prueba cuando se cree.</span><span class="sxs-lookup"><span data-stu-id="23486-267">Specifies the display name of the virtual network switch to which a connection will be allocated for the test replica system when it is created.</span></span>

</dd> <dt>

<span data-ttu-id="23486-268">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="23486-268">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-269">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="23486-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="23486-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-271">El número total de puertos en el conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="23486-271">The total number of ports in the virtual switch.</span></span> <span data-ttu-id="23486-272">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-272">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-273">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="23486-273">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-274">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="23486-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="23486-275">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-276">Especifica la unidad de medida para la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="23486-276">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="23486-277">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="23486-277">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="23486-278">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-278">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="23486-279">**Peso**</span><span class="sxs-lookup"><span data-stu-id="23486-279">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23486-280">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="23486-280">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="23486-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="23486-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="23486-282">Un entero que define el peso de cada conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="23486-282">An integer that defines the weight for each virtual switch.</span></span> <span data-ttu-id="23486-283">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="23486-283">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="23486-284">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="23486-284">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23486-285">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23486-285">Requirements</span></span>



| <span data-ttu-id="23486-286">Requisito</span><span class="sxs-lookup"><span data-stu-id="23486-286">Requirement</span></span> | <span data-ttu-id="23486-287">Value</span><span class="sxs-lookup"><span data-stu-id="23486-287">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23486-288">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23486-288">Minimum supported client</span></span><br/> | <span data-ttu-id="23486-289">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="23486-289">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23486-290">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23486-290">Minimum supported server</span></span><br/> | <span data-ttu-id="23486-291">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="23486-291">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23486-292">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="23486-292">Namespace</span></span><br/>                | <span data-ttu-id="23486-293">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="23486-293">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23486-294">MOF</span><span class="sxs-lookup"><span data-stu-id="23486-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23486-295"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23486-295"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23486-296">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23486-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23486-297"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23486-297"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

