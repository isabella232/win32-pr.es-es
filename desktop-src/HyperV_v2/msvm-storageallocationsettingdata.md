---
description: Representa la configuración relacionada específicamente con la asignación de almacenamiento virtual.
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Msvm_StorageAllocationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d889c262eee9d827a02547ddbfdff2cb121cb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277567"
---
# <a name="msvm_storageallocationsettingdata-class"></a><span data-ttu-id="06420-103">MSVM \_ StorageAllocationSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="06420-103">Msvm\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="06420-104">Representa la configuración relacionada específicamente con la asignación de almacenamiento virtual.</span><span class="sxs-lookup"><span data-stu-id="06420-104">Represents settings specifically related to the allocation of virtual storage.</span></span>

<span data-ttu-id="06420-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="06420-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06420-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06420-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a><span data-ttu-id="06420-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="06420-107">Members</span></span>

<span data-ttu-id="06420-108">La clase **MSVM \_ StorageAllocationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="06420-108">The **Msvm\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="06420-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06420-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06420-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06420-110">Properties</span></span>

<span data-ttu-id="06420-111">La clase **MSVM \_ StorageAllocationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="06420-111">The **Msvm\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06420-112">**Acceder**</span><span class="sxs-lookup"><span data-stu-id="06420-112">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06420-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06420-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-115">Especifica el acceso de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="06420-115">Specifies the storage access.</span></span> <span data-ttu-id="06420-116">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-116">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="06420-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="06420-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06420-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)</span><span class="sxs-lookup"><span data-stu-id="06420-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06420-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)</span><span class="sxs-lookup"><span data-stu-id="06420-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06420-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)</span><span class="sxs-lookup"><span data-stu-id="06420-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06420-121">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="06420-121">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-124">Dirección del recurso.</span><span class="sxs-lookup"><span data-stu-id="06420-124">The address of the resource.</span></span> <span data-ttu-id="06420-125">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-125">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-126">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="06420-126">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-129">Describe la dirección de este recurso en el contexto del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="06420-129">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="06420-130">Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador.</span><span class="sxs-lookup"><span data-stu-id="06420-130">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="06420-131">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-131">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-132">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="06420-132">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-135">Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** .</span><span class="sxs-lookup"><span data-stu-id="06420-135">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="06420-136">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-136">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-137">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="06420-137">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="06420-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06420-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-140">Indica si el recurso se asignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="06420-140">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="06420-141">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-141">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-142">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="06420-142">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="06420-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06420-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-145">Indica si el recurso se desasignará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="06420-145">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="06420-146">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-147">**CachingMode**</span><span class="sxs-lookup"><span data-stu-id="06420-147">**CachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-148">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06420-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06420-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-150">Indica si se debe usar el almacenamiento en caché de archivos en memoria para este VHD.</span><span class="sxs-lookup"><span data-stu-id="06420-150">Indicates whether and how in-memory file caching should be used for this VHD.</span></span> <span data-ttu-id="06420-151">La directiva predeterminada se establece en el campo **DefaultVirtualHardDiskCachingMode** de la clase [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="06420-151">The default policy is set in the **DefaultVirtualHardDiskCachingMode** field of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="06420-152">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="06420-152">Added in Windows 10.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="06420-153">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="06420-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="06420-154">**Predeterminado** (2)</span><span class="sxs-lookup"><span data-stu-id="06420-154">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="06420-155">**Sin almacenamiento en caché** (3)</span><span class="sxs-lookup"><span data-stu-id="06420-155">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="06420-156">**Elementos primarios que se pueda compartir en caché** (4)</span><span class="sxs-lookup"><span data-stu-id="06420-156">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="06420-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="06420-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06420-160">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="06420-160">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="06420-161">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="06420-161">A short description of the object.</span></span> <span data-ttu-id="06420-162">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración predeterminada de la imagen de disco duro".</span><span class="sxs-lookup"><span data-stu-id="06420-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hard Disk Image Default Settings".</span></span>

</dd> <dt>

<span data-ttu-id="06420-163">**Connection**</span><span class="sxs-lookup"><span data-stu-id="06420-163">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-164">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="06420-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06420-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-166">El dispositivo al que está conectado este recurso.</span><span class="sxs-lookup"><span data-stu-id="06420-166">The device to which this resource is connected.</span></span> <span data-ttu-id="06420-167">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-167">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-168">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="06420-168">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-169">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06420-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06420-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-171">Visibilidad del consumidor en el recurso asignado.</span><span class="sxs-lookup"><span data-stu-id="06420-171">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="06420-172">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-172">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="06420-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="06420-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06420-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Pass-through** (2)</span><span class="sxs-lookup"><span data-stu-id="06420-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passed-Through** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06420-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualizado** (3)</span><span class="sxs-lookup"><span data-stu-id="06420-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualized** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06420-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**No se representa** (4)</span><span class="sxs-lookup"><span data-stu-id="06420-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Not represented** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06420-177">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="06420-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-180">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="06420-180">A description of the object.</span></span> <span data-ttu-id="06420-181">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "describe la configuración predeterminada para los recursos de imagen de disco duro".</span><span class="sxs-lookup"><span data-stu-id="06420-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the default settings for the hard disk image resources".</span></span>

</dd> <dt>

<span data-ttu-id="06420-182">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="06420-182">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-185">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="06420-185">A display name for the object.</span></span> <span data-ttu-id="06420-186">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="06420-186">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06420-187">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="06420-187">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-190">Identificador único para la extensión del host.</span><span class="sxs-lookup"><span data-stu-id="06420-190">A unique identifier for the host extent.</span></span> <span data-ttu-id="06420-191">La extensión de host identificada se usa para la asignación de recursos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="06420-191">The identified host extent is used for the storage resource allocation.</span></span> <span data-ttu-id="06420-192">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-192">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="06420-193">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="06420-193">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-194">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06420-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06420-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-196">Identifica el formato que se usa para la propiedad **HostExtentName** .</span><span class="sxs-lookup"><span data-stu-id="06420-196">Identifies the format that is used for the **HostExtentName** property.</span></span> <span data-ttu-id="06420-197">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-197">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="06420-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="06420-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06420-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="06420-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06420-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="06420-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="06420-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="06420-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="06420-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="06420-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>
</dt> <dt>

<span data-ttu-id="06420-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="06420-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>
</dt> <dt>

<span data-ttu-id="06420-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nombre del dispositivo de SO** (12)</span><span class="sxs-lookup"><span data-stu-id="06420-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>
</dt> <dt>

<span data-ttu-id="06420-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="06420-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="06420-206">)</span><span class="sxs-lookup"><span data-stu-id="06420-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06420-207">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="06420-207">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06420-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06420-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-210">Si la extensión del host es un volumen SCSI, el origen preferido para los nombres de los volúmenes SCSI es la página de VPD 83 de las respuestas.</span><span class="sxs-lookup"><span data-stu-id="06420-210">If the host extent is a SCSI volume, then the preferred source for SCSI volume names is SCSI VPD Page 83 responses.</span></span> <span data-ttu-id="06420-211">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-211">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="06420-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="06420-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="06420-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="06420-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06420-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="06420-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06420-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="06420-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06420-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="06420-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06420-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="06420-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span></span>
</dt> <dt>

<span data-ttu-id="06420-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="06420-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span></span>
</dt> <dt>

<span data-ttu-id="06420-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="06420-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="06420-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Espacio de nombres de dispositivo de SO** (8)</span><span class="sxs-lookup"><span data-stu-id="06420-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**OS Device Namespace** (8)</span></span>
</dt> <dt>

<span data-ttu-id="06420-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="06420-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="06420-222">)</span><span class="sxs-lookup"><span data-stu-id="06420-222">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06420-223">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="06420-223">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-224">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06420-224">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06420-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-226">Identifica la dirección de inicio en la extensión de almacenamiento de host, identificada por la propiedad **HostExtentName** , que se usa para la asignación de la extensión de almacenamiento virtual.</span><span class="sxs-lookup"><span data-stu-id="06420-226">Identifies the starting address on the host storage extent, identified by the **HostExtentName** property, that is used for the allocation of the virtual storage extent.</span></span> <span data-ttu-id="06420-227">Un valor **null** indica que no hay ninguna asignación directa de la extensión de almacenamiento virtual a la extensión de almacenamiento de host al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="06420-227">A **Null** value indicates that there is no direct mapping of the virtual storage extent to the referenced host storage extent.</span></span> <span data-ttu-id="06420-228">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-228">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="06420-229">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="06420-229">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-230">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="06420-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="06420-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-232">Solo se puede asignar un recurso de host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz.</span><span class="sxs-lookup"><span data-stu-id="06420-232">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="06420-233">En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar.</span><span class="sxs-lookup"><span data-stu-id="06420-233">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="06420-234">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-234">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="06420-235">Se trata de una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="06420-235">This is a read-only property.</span></span> <span data-ttu-id="06420-236">Pero si la propiedad **resourcetype** es 31 (disco lógico) y la propiedad **subtipo** es "Microsoft: Hyper-v: disco duro virtual", "Microsoft: Hyper-v: disco de CD/DVD virtual" o "Microsoft: Hyper-v: disquete virtual", se puede cambiar la propiedad **HostResource** mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="06420-236">But if the **ResourceType** property is 31 (Logical Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Virtual Hard Disk", "Microsoft:Hyper-V:Virtual CD/DVD Disk", or "Microsoft:Hyper-V:Virtual Floppy Disk", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="06420-237">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="06420-237">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-238">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06420-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06420-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-240">Tamaño, en bytes, de los bloques que se asignan en el host como resultado de la asignación de recursos de almacenamiento o la solicitud de asignación de recursos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="06420-240">The size, in bytes, of the blocks that are allocated at the host as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="06420-241">Si el tamaño de bloque es variable, se especificará el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="06420-241">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="06420-242">Si el tamaño de bloque es desconocido o si no se aplica un concepto de bloque, se usará el valor 1.</span><span class="sxs-lookup"><span data-stu-id="06420-242">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="06420-243">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-243">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="06420-244">**IgnoreFlushes**</span><span class="sxs-lookup"><span data-stu-id="06420-244">**IgnoreFlushes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-245">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="06420-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06420-246">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-247">Si se establece en true, Hyper-V omitirá el vaciado de escritura de la máquina virtual en cuestión.</span><span class="sxs-lookup"><span data-stu-id="06420-247">If set to true, Hyper-V will ignore write back flushing for that particular virtual machine.</span></span> <span data-ttu-id="06420-248">Si se establece en false, Hyper-V seguirá reescribiendo en el disco en cada vaciado.</span><span class="sxs-lookup"><span data-stu-id="06420-248">If set to false, Hyper-V will continue to write back to the disk on every flush.</span></span> <span data-ttu-id="06420-249">False es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="06420-249">The default setting is false.</span></span>

<span data-ttu-id="06420-250">**Windows 10:** Este valor no se admite hasta Windows 10.</span><span class="sxs-lookup"><span data-stu-id="06420-250">**Windows 10:** This value is not supported until Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="06420-251">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="06420-251">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06420-254">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="06420-254">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="06420-255">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="06420-255">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="06420-256">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="06420-256">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="06420-257">**IOPSAllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="06420-257">**IOPSAllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-258">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-259">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-260">Especifica las unidades de asignación utilizadas por las propiedades **IOPSLimit** y **IOPSReservation** .</span><span class="sxs-lookup"><span data-stu-id="06420-260">Specifies the allocation units used by the **IOPSLimit** and **IOPSReservation** properties.</span></span> <span data-ttu-id="06420-261">Esta propiedad siempre tiene el valor:</span><span class="sxs-lookup"><span data-stu-id="06420-261">This property always has the value:</span></span>

<span data-ttu-id="06420-262">"recuento (e/s normalizado)/segundo"</span><span class="sxs-lookup"><span data-stu-id="06420-262">"count(normalized I/O) / second"</span></span>

<span data-ttu-id="06420-263">El rendimiento se mide en operaciones de e/s normalizadas por segundo (IOPS) en lugar de IOPS sin procesar.</span><span class="sxs-lookup"><span data-stu-id="06420-263">Throughput is measured in normalized I/O operations per second (IOPS) instead of raw IOPS.</span></span> <span data-ttu-id="06420-264">Cuando se usa la IOPS normalizada, cada solicitud de e/s se cuenta como 1 e/s normalizada si el tamaño de la solicitud es menor o igual que un tamaño base predefinido (8 KB).</span><span class="sxs-lookup"><span data-stu-id="06420-264">When using normalized IOPS, each I/O request is accounted for as 1 normalized I/O if the size of the request is less than or equal to a predefined base size (8 KB).</span></span> <span data-ttu-id="06420-265">Las solicitudes que son mayores que el tamaño base se tienen en cuenta como operaciones de e/s de N, donde N es el valor redondeado del tamaño de la solicitud dividido por el tamaño base.</span><span class="sxs-lookup"><span data-stu-id="06420-265">Requests that are larger than the base size are accounted for as N I/O operations, where N is the rounded-up value of the request size divided by the base size.</span></span> <span data-ttu-id="06420-266">Por ejemplo, si el tamaño base es de 8 KB, una solicitud de 16 KB se cuenta como dos operaciones de e/s normalizadas, una solicitud de 32 KB como 4 operaciones de e/s normalizadas, etc.</span><span class="sxs-lookup"><span data-stu-id="06420-266">For example, if the base size is 8 KB, a 16-KB request is counted as 2 normalized I/O operations, a 32-KB request as 4 normalized I/O operations, and so on.</span></span>

<span data-ttu-id="06420-267">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="06420-267">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="06420-268">**IOPSLimit**</span><span class="sxs-lookup"><span data-stu-id="06420-268">**IOPSLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-269">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06420-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06420-270">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06420-271">Calificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 mil millones)</span><span class="sxs-lookup"><span data-stu-id="06420-271">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="06420-272">Número máximo de operaciones de e/s por segundo (IOPS) que se van a atender para esta extensión de almacenamiento virtual.</span><span class="sxs-lookup"><span data-stu-id="06420-272">The maximum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span> <span data-ttu-id="06420-273">Si el valor no está definido o es cero, no hay ningún límite en el número de IOPS que el dispositivo puede emitir.</span><span class="sxs-lookup"><span data-stu-id="06420-273">If the value isn't defined or is zero, there is no limit to the number of IOPS that the device can issue.</span></span>

> [!Note]  
> <span data-ttu-id="06420-274">Puede usar el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="06420-274">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="06420-275">Esta propiedad solo es significativa para las instancias de **MSVM \_ StorageAllocationSettingData** que solicitan asignaciones de recursos para máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="06420-275">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="06420-276">Se omite cuando se asignan recursos a un grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="06420-276">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="06420-277">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="06420-277">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="06420-278">**IOPSReservation**</span><span class="sxs-lookup"><span data-stu-id="06420-278">**IOPSReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-279">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06420-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06420-280">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06420-281">Calificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 mil millones)</span><span class="sxs-lookup"><span data-stu-id="06420-281">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="06420-282">El número mínimo de operaciones de e/s por segundo (IOPS) que se van a atender para esta extensión de almacenamiento virtual.</span><span class="sxs-lookup"><span data-stu-id="06420-282">The minimum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span>

<span data-ttu-id="06420-283">Si se definen tanto **IOPSLimit** como **IOPSReservation** , el valor de **IOPSLimit** debe ser mayor o igual que el valor de **IOPSReservation**.</span><span class="sxs-lookup"><span data-stu-id="06420-283">If both **IOPSLimit** and **IOPSReservation** are defined, the value of **IOPSLimit** must be greater than or equal to the value of **IOPSReservation**.</span></span>

> [!Note]  
> <span data-ttu-id="06420-284">Puede usar el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar el valor de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="06420-284">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="06420-285">Esta propiedad solo es significativa para las instancias de **MSVM \_ StorageAllocationSettingData** que solicitan asignaciones de recursos para máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="06420-285">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="06420-286">Se omite cuando se asignan recursos a un grupo secundario.</span><span class="sxs-lookup"><span data-stu-id="06420-286">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="06420-287">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="06420-287">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="06420-288">**Límite**</span><span class="sxs-lookup"><span data-stu-id="06420-288">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-289">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06420-289">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06420-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-291">Número máximo de bloques que se concederán para esta asignación de recursos de almacenamiento en el host.</span><span class="sxs-lookup"><span data-stu-id="06420-291">The maximum number of blocks that will be granted for this storage resource allocation at the host.</span></span> <span data-ttu-id="06420-292">El tamaño de bloque se especifica mediante la propiedad **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="06420-292">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="06420-293">Normalmente, el valor de esta propiedad reflejará un tamaño máximo para la extensión de host asignada que coincida con el tamaño de la extensión de almacenamiento virtual presentada al consumidor.</span><span class="sxs-lookup"><span data-stu-id="06420-293">Usually the value of this property would reflect a maximum size for the allocated host extent that matches the size of the virtual storage extent presented to the consumer.</span></span> <span data-ttu-id="06420-294">Un valor menor que esto indicaría una situación en la que se espera una extensión de almacenamiento virtual parcialmente rellenada, donde la velocidad de relleno está limitada por el valor de la propiedad Limit.</span><span class="sxs-lookup"><span data-stu-id="06420-294">A value less than that would indicate a situation where a sparsely populated virtual storage extent is expected, where the fill rate is limited by the value of the Limit property.</span></span> <span data-ttu-id="06420-295">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-295">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-296">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="06420-296">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-297">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06420-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06420-298">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-299">Especifica cómo se asigna este recurso a los recursos subyacentes.</span><span class="sxs-lookup"><span data-stu-id="06420-299">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="06420-300">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-300">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-301">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="06420-301">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-302">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-303">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-304">Cadena que describe el formato de la propiedad **HostExtentName** si la propiedad **HostExtentNameFormat** es 1 (otra).</span><span class="sxs-lookup"><span data-stu-id="06420-304">A string that describes the format of the **HostExtentName** property if the **HostExtentNameFormat** property is 1 (Other).</span></span> <span data-ttu-id="06420-305">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-305">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="06420-306">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="06420-306">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-307">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-308">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-309">Una cadena que describe el espacio de nombres de la propiedad **HostExtentName** si la propiedad **HostExtentNameNamespace** contiene 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="06420-309">A string that describes the namespace of the **HostExtentName** property if the **HostExtentNameNamespace** property contains 1 (Other).</span></span> <span data-ttu-id="06420-310">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-310">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="06420-311">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="06420-311">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-314">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="06420-314">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="06420-315">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-315">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-316">**Parent**</span><span class="sxs-lookup"><span data-stu-id="06420-316">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-319">Elemento primario del recurso.</span><span class="sxs-lookup"><span data-stu-id="06420-319">The parent of the resource.</span></span> <span data-ttu-id="06420-320">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-320">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-321">**PersistentReservationsSupported**</span><span class="sxs-lookup"><span data-stu-id="06420-321">**PersistentReservationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-322">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="06420-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="06420-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-324">Indica si el disco duro virtual admite reservas persistentes SCSI-3.</span><span class="sxs-lookup"><span data-stu-id="06420-324">Indicates whether the virtual hard disk supports SCSI-3 persistent reservations.</span></span>

<span data-ttu-id="06420-325">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="06420-325">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="06420-326">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="06420-326">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-327">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-329">Identificador del grupo de recursos desde el que se asignó este recurso.</span><span class="sxs-lookup"><span data-stu-id="06420-329">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="06420-330">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-330">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-331">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="06420-331">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-332">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06420-332">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06420-333">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06420-334">Calificadores: **override** ("reserva"), **ModelCorrespondence** ("CIM \_ StorageAllocationSettingData. HostResourceBlockSize")</span><span class="sxs-lookup"><span data-stu-id="06420-334">Qualifiers: **Override** ("Reservation"), **ModelCorrespondence** ("CIM\_StorageAllocationSettingData.HostResourceBlockSize")</span></span>
</dt> </dl>

<span data-ttu-id="06420-335">El número de bloques que se garantiza que estarán disponibles para esta asignación de recursos de almacenamiento en el host.</span><span class="sxs-lookup"><span data-stu-id="06420-335">The number of blocks that are guaranteed to be available for this storage resource allocation at the host.</span></span> <span data-ttu-id="06420-336">El tamaño de bloque se especifica mediante la propiedad **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="06420-336">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="06420-337">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-337">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="06420-338">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="06420-338">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-339">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-340">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-341">Cadena que describe un subtipo específico de la implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="06420-341">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="06420-342">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="06420-342">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="06420-343">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-343">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-344">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="06420-344">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-345">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06420-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06420-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-347">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="06420-347">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="06420-348">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-348">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="06420-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="06420-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="06420-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="06420-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="06420-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="06420-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="06420-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="06420-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="06420-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="06420-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="06420-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="06420-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="06420-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="06420-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="06420-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="06420-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="06420-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="06420-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="06420-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="06420-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="06420-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="06420-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="06420-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="06420-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="06420-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="06420-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="06420-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="06420-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="06420-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="06420-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="06420-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="06420-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="06420-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidad de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="06420-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="06420-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidad de cinta** (18)</span><span class="sxs-lookup"><span data-stu-id="06420-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="06420-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de almacenamiento** (19)</span><span class="sxs-lookup"><span data-stu-id="06420-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="06420-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (20)</span><span class="sxs-lookup"><span data-stu-id="06420-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="06420-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (21)</span><span class="sxs-lookup"><span data-stu-id="06420-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="06420-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (22)</span><span class="sxs-lookup"><span data-stu-id="06420-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="06420-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controladora USB** (23)</span><span class="sxs-lookup"><span data-stu-id="06420-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="06420-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controladora de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="06420-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="06420-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="06420-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="06420-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="06420-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="06420-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="06420-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="06420-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fuente de alimentación** (28)</span><span class="sxs-lookup"><span data-stu-id="06420-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="06420-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de refrigeración** (29)</span><span class="sxs-lookup"><span data-stu-id="06420-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="06420-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Puerto de conmutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="06420-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="06420-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="06420-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="06420-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volumen de almacenamiento** (32)</span><span class="sxs-lookup"><span data-stu-id="06420-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="06420-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexión Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="06420-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="06420-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="06420-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="06420-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="06420-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="06420-384">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="06420-384">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-385">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-386">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-387">Un GUID que representa qué instantánea del archivo del conjunto de VHD se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="06420-387">A GUID representing which snapshot within the VHD Set file is to be attached.</span></span>

> [!Note]  
> <span data-ttu-id="06420-388">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="06420-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="06420-389">**StorageQoSPolicyID**</span><span class="sxs-lookup"><span data-stu-id="06420-389">**StorageQoSPolicyID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-390">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-390">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-391">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-392">Especifica el identificador único de la Directiva de QoS de almacenamiento que se va a aplicar a esta extensión de almacenamiento virtual.</span><span class="sxs-lookup"><span data-stu-id="06420-392">Specifies the unique identifier of the Storage QoS Policy to be applied to this virtual storage extent.</span></span>

> [!Note]  
> <span data-ttu-id="06420-393">Agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="06420-393">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="06420-394">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="06420-394">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-395">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06420-395">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06420-396">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-397">El número de bloques que se presentan al consumidor.</span><span class="sxs-lookup"><span data-stu-id="06420-397">The number of blocks that are presented to the consumer.</span></span> <span data-ttu-id="06420-398">El tamaño de bloque se especifica mediante la propiedad **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="06420-398">The block size is specified by the **VirtualResourceBlockSize** property.</span></span> <span data-ttu-id="06420-399">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-399">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="06420-400">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="06420-400">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-401">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06420-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06420-402">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-403">Especifica las unidades utilizadas por la propiedad **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="06420-403">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="06420-404">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-404">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>



| <span data-ttu-id="06420-405">Value</span><span class="sxs-lookup"><span data-stu-id="06420-405">Value</span></span>                                                                                                | <span data-ttu-id="06420-406">Significado</span><span class="sxs-lookup"><span data-stu-id="06420-406">Meaning</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06420-407"><dt>"recuento (bloque de tamaño fijo)"</dt></span><span class="sxs-lookup"><span data-stu-id="06420-407"><dt>"count(fixed size block)"</dt></span></span> </dl> | <span data-ttu-id="06420-408">El tamaño de bloque fijo está contenido en la propiedad **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="06420-408">The fixed block size is contained in the **VirtualResourceBlockSize** property.</span></span><br/> |
| <dl> <span data-ttu-id="06420-409"><dt>bytes</dt></span><span class="sxs-lookup"><span data-stu-id="06420-409"><dt>"byte"</dt></span></span> </dl>                    | <span data-ttu-id="06420-410">La propiedad **VirtualQuantity** se mide en bytes.</span><span class="sxs-lookup"><span data-stu-id="06420-410">The **VirtualQuantity** property is measured in bytes.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="06420-411">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="06420-411">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-412">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="06420-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="06420-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-414">Tamaño, en bytes, de los bloques que se presentan al consumidor como resultado de la asignación de recursos de almacenamiento o la solicitud de asignación de recursos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="06420-414">The size, in bytes, of the blocks that are presented to the consumer as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="06420-415">Si el tamaño de bloque es variable, se especificará el tamaño máximo de bloque, en bytes.</span><span class="sxs-lookup"><span data-stu-id="06420-415">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="06420-416">Si el tamaño de bloque es desconocido o si no se aplica un concepto de bloque, se usará el valor 1.</span><span class="sxs-lookup"><span data-stu-id="06420-416">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="06420-417">Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.</span><span class="sxs-lookup"><span data-stu-id="06420-417">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="06420-418">**Peso**</span><span class="sxs-lookup"><span data-stu-id="06420-418">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-419">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06420-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06420-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06420-421">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("peso"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span><span class="sxs-lookup"><span data-stu-id="06420-421">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span></span>
</dt> </dl>

<span data-ttu-id="06420-422">Especifica una prioridad relativa para esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio.</span><span class="sxs-lookup"><span data-stu-id="06420-422">Specifies a relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="06420-423">Esta propiedad no tiene ninguna unidad de medida y solo es relevante en comparación con otras asignaciones vying para los mismos recursos de host.</span><span class="sxs-lookup"><span data-stu-id="06420-423">This property has no unit of measure and is only relevant when compared to other allocations vying for the same host resources.</span></span> <span data-ttu-id="06420-424">Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="06420-424">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="06420-425">Intervalo: 1 10000</span><span class="sxs-lookup"><span data-stu-id="06420-425">Range: 1 10000</span></span>

</dd> <dt>

<span data-ttu-id="06420-426">**WriteHardeningMethod**</span><span class="sxs-lookup"><span data-stu-id="06420-426">**WriteHardeningMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06420-427">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06420-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06420-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06420-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="06420-429">Indica qué método de protección de escritura es compatible con el disco.</span><span class="sxs-lookup"><span data-stu-id="06420-429">Indicates what write hardening method is supported by the disk.</span></span>

> [!Note]  
> <span data-ttu-id="06420-430">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="06420-430">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="06420-431">**Valor predeterminado** (0)</span><span class="sxs-lookup"><span data-stu-id="06420-431">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

<span data-ttu-id="06420-432">**WriteCacheEnabled** (1)</span><span class="sxs-lookup"><span data-stu-id="06420-432">**WriteCacheEnabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

<span data-ttu-id="06420-433">**WriteCacheandFUAEnabled** (2)</span><span class="sxs-lookup"><span data-stu-id="06420-433">**WriteCacheandFUAEnabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

<span data-ttu-id="06420-434">**WriteCacheDisabled** (3)</span><span class="sxs-lookup"><span data-stu-id="06420-434">**WriteCacheDisabled** (3)</span></span>


<span data-ttu-id="06420-435"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="06420-435"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="06420-436">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06420-436">Requirements</span></span>



| <span data-ttu-id="06420-437">Requisito</span><span class="sxs-lookup"><span data-stu-id="06420-437">Requirement</span></span> | <span data-ttu-id="06420-438">Value</span><span class="sxs-lookup"><span data-stu-id="06420-438">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06420-439">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06420-439">Minimum supported client</span></span><br/> | <span data-ttu-id="06420-440">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="06420-440">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="06420-441">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06420-441">Minimum supported server</span></span><br/> | <span data-ttu-id="06420-442">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="06420-442">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="06420-443">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="06420-443">Namespace</span></span><br/>                | <span data-ttu-id="06420-444">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="06420-444">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="06420-445">MOF</span><span class="sxs-lookup"><span data-stu-id="06420-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06420-446"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06420-446"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="06420-447">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="06420-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06420-448"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="06420-448"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

