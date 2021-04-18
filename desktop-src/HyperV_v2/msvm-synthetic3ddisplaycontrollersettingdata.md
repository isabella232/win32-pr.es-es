---
description: Representa la configuración de un controlador de pantalla sintético 3D para una máquina virtual.
ms.assetid: 7162AEED-90CB-41C3-BD44-8B552C00F597
title: Msvm_Synthetic3DDisplayControllerSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DDisplayControllerSettingData
- Msvm_Synthetic3DDisplayControllerSettingData.InstanceID
- Msvm_Synthetic3DDisplayControllerSettingData.Caption
- Msvm_Synthetic3DDisplayControllerSettingData.Description
- Msvm_Synthetic3DDisplayControllerSettingData.ElementName
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.OtherResourceType
- Msvm_Synthetic3DDisplayControllerSettingData.ResourceSubType
- Msvm_Synthetic3DDisplayControllerSettingData.PoolID
- Msvm_Synthetic3DDisplayControllerSettingData.ConsumerVisibility
- Msvm_Synthetic3DDisplayControllerSettingData.HostResource
- Msvm_Synthetic3DDisplayControllerSettingData.AllocationUnits
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantity
- Msvm_Synthetic3DDisplayControllerSettingData.Reservation
- Msvm_Synthetic3DDisplayControllerSettingData.Limit
- Msvm_Synthetic3DDisplayControllerSettingData.Weight
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticAllocation
- Msvm_Synthetic3DDisplayControllerSettingData.AutomaticDeallocation
- Msvm_Synthetic3DDisplayControllerSettingData.Parent
- Msvm_Synthetic3DDisplayControllerSettingData.Connection
- Msvm_Synthetic3DDisplayControllerSettingData.Address
- Msvm_Synthetic3DDisplayControllerSettingData.MappingBehavior
- Msvm_Synthetic3DDisplayControllerSettingData.AddressOnParent
- Msvm_Synthetic3DDisplayControllerSettingData.VirtualQuantityUnits
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumScreenResolution
- Msvm_Synthetic3DDisplayControllerSettingData.MaximumMonitors
- Msvm_Synthetic3DDisplayControllerSettingData.VRAMSizeBytes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c93bb67cd4a66c4ecc5f6820ff2de7cf3816b2b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687263"
---
# <a name="msvm_synthetic3ddisplaycontrollersettingdata-class"></a><span data-ttu-id="0c483-103">MSVM \_ Synthetic3DDisplayControllerSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="0c483-103">Msvm\_Synthetic3DDisplayControllerSettingData class</span></span>

<span data-ttu-id="0c483-104">Representa la configuración de un controlador de pantalla sintético 3D para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c483-104">Represents settings for a synthetic 3-D display controller for a virtual machine.</span></span> <span data-ttu-id="0c483-105">Esta clase solo se usa con máquinas virtuales que usan RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="0c483-105">This class is only used with virtual machines that use RemoteFX.</span></span>

<span data-ttu-id="0c483-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0c483-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c483-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c483-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "3D Display Controller Default Settings";
  string  Description = "Describes the default settings for the 3D video controller resource pool.";
  string  ElementName;
  uint16  ResourceType = 24;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Synthetic 3D Display Controller";
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
  uint8   MaximumScreenResolution;
  uint8   MaximumMonitors;
  uint64  VRAMSizeBytes;
};
```

## <a name="members"></a><span data-ttu-id="0c483-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c483-108">Members</span></span>

<span data-ttu-id="0c483-109">La clase **MSVM \_ Synthetic3DDisplayControllerSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0c483-109">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0c483-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c483-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c483-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c483-111">Properties</span></span>

<span data-ttu-id="0c483-112">La clase **MSVM \_ Synthetic3DDisplayControllerSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c483-112">The **Msvm\_Synthetic3DDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c483-113">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="0c483-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-116">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="0c483-116">The address of the resource.</span></span> <span data-ttu-id="0c483-117">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-117">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0c483-118">Se trata de una propiedad de solo lectura, pero si la propiedad **resourcetype** es 20 (controladora de gráficos), se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0c483-118">This is a read-only property, but if the **ResourceType** property is 20 (Graphics controller), it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0c483-119">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="0c483-119">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-122">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="0c483-122">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="0c483-123">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="0c483-123">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="0c483-124">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-124">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-125">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="0c483-125">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-128">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="0c483-128">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="0c483-129">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-129">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-130">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="0c483-130">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-131">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0c483-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-133">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0c483-133">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="0c483-134">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-134">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-135">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="0c483-135">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-136">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="0c483-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-138">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="0c483-138">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="0c483-139">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-139">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-140">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0c483-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c483-143">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="0c483-143">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="0c483-144">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0c483-144">A short description of the object.</span></span> <span data-ttu-id="0c483-145">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c483-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-146">**Connection**</span><span class="sxs-lookup"><span data-stu-id="0c483-146">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-147">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0c483-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c483-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-149">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="0c483-149">The device to which this resource is connected.</span></span> <span data-ttu-id="0c483-150">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-150">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0c483-151">Se trata de una propiedad de solo lectura, pero si 1) la propiedad **resourcetype** es 17 (puerto serie) o 2) la propiedad **resourcetype** es 21 (extensión de almacenamiento) y la propiedad **subtipo** es "disco duro virtual de Microsoft" y, después, se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0c483-151">This is a read-only property, but if either 1) the **ResourceType** property is 17 (Serial port), or 2) the **ResourceType** property is 21 (Storage Extent) and the **ResourceSubType** property is "Microsoft Virtual Hard Disk", then it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="0c483-152">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="0c483-152">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c483-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-155">Visibilidad del consumidor en el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="0c483-155">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="0c483-156">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-156">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-157">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0c483-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-160">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0c483-160">A description of the object.</span></span> <span data-ttu-id="0c483-161">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c483-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-162">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0c483-162">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-165">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="0c483-165">A display name for the object.</span></span> <span data-ttu-id="0c483-166">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c483-166">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="0c483-167">Al cambiar esta propiedad, se cambiará el nombre del elemento del derivado del dispositivo lógico asociado.</span><span class="sxs-lookup"><span data-stu-id="0c483-167">Changing this property will change the element name of the associated logical device derivative.</span></span>

</dd> <dt>

<span data-ttu-id="0c483-168">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="0c483-168">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-169">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0c483-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0c483-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-171">Solo se puede asignar un recurso de host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="0c483-171">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="0c483-172">En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="0c483-172">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource that is to be assigned.</span></span> <span data-ttu-id="0c483-173">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-173">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-174">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0c483-174">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-177">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0c483-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0c483-178">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0c483-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-179">**Límite**</span><span class="sxs-lookup"><span data-stu-id="0c483-179">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-180">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c483-180">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-182">La cantidad máxima de recursos de host correspondientes que puede usar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c483-182">The maximum amount of corresponding host resources that can be consumed by the virtual machine.</span></span> <span data-ttu-id="0c483-183">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-183">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-184">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="0c483-184">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-185">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c483-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-186">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-187">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="0c483-187">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="0c483-188">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-188">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-189">**MaximumMonitors**</span><span class="sxs-lookup"><span data-stu-id="0c483-189">**MaximumMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-190">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0c483-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-191">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0c483-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0c483-192">Número máximo de monitores disponibles para el controlador de pantalla 3D.</span><span class="sxs-lookup"><span data-stu-id="0c483-192">The maximum number of monitors available to the 3-D display controller.</span></span> <span data-ttu-id="0c483-193">El número mínimo de monitores es 1 y el máximo depende de la resolución de pantalla máxima.</span><span class="sxs-lookup"><span data-stu-id="0c483-193">The minimum number of monitors is 1 and the maximum is dependent upon the maximum screen resolution.</span></span> <span data-ttu-id="0c483-194">En la tabla siguiente se define el número máximo de monitores permitido para diferentes resoluciones.</span><span class="sxs-lookup"><span data-stu-id="0c483-194">The following table defines the maximum number of monitors allowed for different resolutions.</span></span>



| <span data-ttu-id="0c483-195">Solución</span><span class="sxs-lookup"><span data-stu-id="0c483-195">Resolution</span></span>            | <span data-ttu-id="0c483-196">Monitores máximos</span><span class="sxs-lookup"><span data-stu-id="0c483-196">Maximum monitors</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="0c483-197">1024 768</span><span class="sxs-lookup"><span data-stu-id="0c483-197">1024  768</span></span><br/>  | <span data-ttu-id="0c483-198">4</span><span class="sxs-lookup"><span data-stu-id="0c483-198">4</span></span><br/>     |
| <span data-ttu-id="0c483-199">1280 1024</span><span class="sxs-lookup"><span data-stu-id="0c483-199">1280  1024</span></span><br/> | <span data-ttu-id="0c483-200">4</span><span class="sxs-lookup"><span data-stu-id="0c483-200">4</span></span><br/>     |
| <span data-ttu-id="0c483-201">1600 1200</span><span class="sxs-lookup"><span data-stu-id="0c483-201">1600  1200</span></span><br/> | <span data-ttu-id="0c483-202">3</span><span class="sxs-lookup"><span data-stu-id="0c483-202">3</span></span><br/>     |
| <span data-ttu-id="0c483-203">1920 1200</span><span class="sxs-lookup"><span data-stu-id="0c483-203">1920  1200</span></span><br/> | <span data-ttu-id="0c483-204">2</span><span class="sxs-lookup"><span data-stu-id="0c483-204">2</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="0c483-205">**MaximumScreenResolution**</span><span class="sxs-lookup"><span data-stu-id="0c483-205">**MaximumScreenResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-206">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0c483-206">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-208">Especifica la resolución de pantalla máxima para el controlador de pantalla 3D.</span><span class="sxs-lookup"><span data-stu-id="0c483-208">Specifies the maximum screen resolution for the 3-D display controller.</span></span> <span data-ttu-id="0c483-209">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0c483-209">This must be one of the following values.</span></span>

<dt>

<span id="1024___768"></span>

<span data-ttu-id="0c483-210"><span id="1024___768"></span>**1024 \* 768** (0)</span><span class="sxs-lookup"><span data-stu-id="0c483-210"><span id="1024___768"></span>**1024 \* 768** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0c483-211">La resolución máxima es 1024 768.</span><span class="sxs-lookup"><span data-stu-id="0c483-211">The maximum resolution is 1024   768.</span></span>

</dd> <dt>

<span id="1280___1024"></span>

<span data-ttu-id="0c483-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span><span class="sxs-lookup"><span data-stu-id="0c483-212"><span id="1280___1024"></span>**1280 \* 1024** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0c483-213">La resolución máxima es 1280 1024.</span><span class="sxs-lookup"><span data-stu-id="0c483-213">The maximum resolution is 1280   1024.</span></span>

</dd> <dt>

<span id="1600___1200"></span>

<span data-ttu-id="0c483-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span><span class="sxs-lookup"><span data-stu-id="0c483-214"><span id="1600___1200"></span>**1600 \* 1200** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0c483-215">La resolución máxima es 1600 1200.</span><span class="sxs-lookup"><span data-stu-id="0c483-215">The maximum resolution is 1600   1200.</span></span>

</dd> <dt>

<span id="1920___1200"></span>

<span data-ttu-id="0c483-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span><span class="sxs-lookup"><span data-stu-id="0c483-216"><span id="1920___1200"></span>**1920 \* 1200** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0c483-217">La resolución máxima es 1920 1200.</span><span class="sxs-lookup"><span data-stu-id="0c483-217">The maximum resolution is 1920   1200.</span></span>

</dd> <dt>

<span id="2560___1600"></span>

<span data-ttu-id="0c483-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span><span class="sxs-lookup"><span data-stu-id="0c483-218"><span id="2560___1600"></span>**2560 \* 1600** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0c483-219">La resolución máxima es 2650 1600.</span><span class="sxs-lookup"><span data-stu-id="0c483-219">The maximum resolution is 2650   1600.</span></span>

</dd> <dt>

<span id="3840___2160"></span>

<span data-ttu-id="0c483-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span><span class="sxs-lookup"><span data-stu-id="0c483-220"><span id="3840___2160"></span>**3840 \* 2160** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0c483-221">La resolución máxima es 3840 2160.</span><span class="sxs-lookup"><span data-stu-id="0c483-221">The maximum resolution is 3840   2160.</span></span>

> [!Note]  
> <span data-ttu-id="0c483-222">Agregado en Windows 10 y Windows Server 2016. MSVM \_ synte</span><span class="sxs-lookup"><span data-stu-id="0c483-222">Added in Windows 10 and Windows Server 2016.msvm\_synte</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0c483-223">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="0c483-223">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-226">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="0c483-226">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="0c483-227">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-227">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-228">**Parent**</span><span class="sxs-lookup"><span data-stu-id="0c483-228">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-229">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-230">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-231">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="0c483-231">The parent of the resource.</span></span> <span data-ttu-id="0c483-232">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-232">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-233">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="0c483-233">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-234">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-235">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-236">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="0c483-236">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="0c483-237">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-237">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-238">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="0c483-238">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-239">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c483-239">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-240">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-241">La cantidad de recursos de CPU que se reservan para su uso por parte de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c483-241">The amount of CPU resources that are reserved for use by the virtual machine.</span></span> <span data-ttu-id="0c483-242">Se garantiza que estos recursos están disponibles para su consumo por parte de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c483-242">These resources are guaranteed to be available for consumption by the virtual machine.</span></span> <span data-ttu-id="0c483-243">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-243">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-244">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="0c483-244">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-245">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-247">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="0c483-247">A string that describes an implementation specific subtype for this resource.</span></span> <span data-ttu-id="0c483-248">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="0c483-248">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="0c483-249">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-249">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-250">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0c483-250">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-251">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0c483-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-253">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="0c483-253">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="0c483-254">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-254">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-255">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="0c483-255">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-256">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c483-256">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-258">El número total de núcleos de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c483-258">The total number of cores in the virtual machine.</span></span> <span data-ttu-id="0c483-259">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-259">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-260">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="0c483-260">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-261">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0c483-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-263">Especifica la unidad de medida para la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="0c483-263">Specifies the unit of measurement for the **VirtualQuantity** property.</span></span> <span data-ttu-id="0c483-264">El valor de esta propiedad debe ser un valor válido del calificador de unidades de programación, tal y como se define en el anexo C. 1 de DSP0004 V 2.5 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0c483-264">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Annex C.1 of DSP0004 V2.5 or later.</span></span> <span data-ttu-id="0c483-265">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-265">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="0c483-266">**VRAMSizeBytes**</span><span class="sxs-lookup"><span data-stu-id="0c483-266">**VRAMSizeBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-267">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c483-267">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0c483-268">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0c483-269">Tamaño de la memoria de vídeo de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c483-269">The video memory size for the Virtual Machine.</span></span>

> [!Note]  
> <span data-ttu-id="0c483-270">Agregado en Windows 10 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="0c483-270">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>



 <span data-ttu-id="0c483-271">(67108864)</span><span class="sxs-lookup"><span data-stu-id="0c483-271">(67108864)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0c483-272">(134217728)</span><span class="sxs-lookup"><span data-stu-id="0c483-272">(134217728)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0c483-273">(268435456)</span><span class="sxs-lookup"><span data-stu-id="0c483-273">(268435456)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0c483-274">(536870912)</span><span class="sxs-lookup"><span data-stu-id="0c483-274">(536870912)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0c483-275">(1073741824)</span><span class="sxs-lookup"><span data-stu-id="0c483-275">(1073741824)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c483-276">**Peso**</span><span class="sxs-lookup"><span data-stu-id="0c483-276">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c483-277">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c483-277">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c483-278">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c483-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c483-279">Un entero que define el peso de cada procesador de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c483-279">An integer that defines the weight for each virtual machine processor.</span></span> <span data-ttu-id="0c483-280">Una vez que se hayan cumplido todas las reservas, la capacidad de procesador físico restante de la plataforma de hospedaje se asignará a las máquinas virtuales en función de sus ponderaciones relativas.</span><span class="sxs-lookup"><span data-stu-id="0c483-280">After all reserves have been met, the remaining physical processor capacity of the hosting platform will be allocated to virtual machines based on their relative weights.</span></span> <span data-ttu-id="0c483-281">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c483-281">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0c483-282">0</span><span class="sxs-lookup"><span data-stu-id="0c483-282">0</span></span>

<span data-ttu-id="0c483-283">Intervalo: 0 1000</span><span class="sxs-lookup"><span data-stu-id="0c483-283">Range: 0 1000</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c483-284">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c483-284">Requirements</span></span>



| <span data-ttu-id="0c483-285">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c483-285">Requirement</span></span> | <span data-ttu-id="0c483-286">Value</span><span class="sxs-lookup"><span data-stu-id="0c483-286">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c483-287">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c483-287">Minimum supported client</span></span><br/> | <span data-ttu-id="0c483-288">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c483-288">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c483-289">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c483-289">Minimum supported server</span></span><br/> | <span data-ttu-id="0c483-290">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c483-290">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c483-291">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0c483-291">Namespace</span></span><br/>                | <span data-ttu-id="0c483-292">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0c483-292">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c483-293">MOF</span><span class="sxs-lookup"><span data-stu-id="0c483-293">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c483-294"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c483-294"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c483-295">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c483-295">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c483-296"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c483-296"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

