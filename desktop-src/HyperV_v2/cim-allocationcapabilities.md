---
description: Representa la configuración de asignación de recursos de un elemento administrado para un tipo de recurso específico.
ms.assetid: f27910c7-a88a-4694-80fe-7761945782e0
title: CIM_AllocationCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocationCapabilities
- CIM_AllocationCapabilities.ResourceType
- CIM_AllocationCapabilities.OtherResourceType
- CIM_AllocationCapabilities.ResourceSubType
- CIM_AllocationCapabilities.RequestTypesSupported
- CIM_AllocationCapabilities.SharingMode
- CIM_AllocationCapabilities.SupportedAddStates
- CIM_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d022023142b38905067e30a4c1be3b133e49a86f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666243"
---
# <a name="cim_allocationcapabilities-class"></a><span data-ttu-id="0d0e3-103">\_Clase AllocationCapabilities de CIM</span><span class="sxs-lookup"><span data-stu-id="0d0e3-103">CIM\_AllocationCapabilities class</span></span>

<span data-ttu-id="0d0e3-104">Representa la configuración de asignación de recursos de un elemento administrado para un tipo de recurso específico.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-104">Represents the resource allocation settings of a managed element for a specific resource type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d0e3-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_AllocationCapabilities : CIM_Capabilities
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="0d0e3-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d0e3-106">Members</span></span>

<span data-ttu-id="0d0e3-107">La clase **CIM \_ AllocationCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0d0e3-107">The **CIM\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="0d0e3-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d0e3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d0e3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d0e3-109">Properties</span></span>

<span data-ttu-id="0d0e3-110">La clase **CIM \_ AllocationCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-110">The **CIM\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d0e3-111">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-111">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0e3-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d0e3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-114">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="0d0e3-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="0d0e3-115">El tipo de recurso para esta configuración de asignación cuando la propiedad **resourcetype** está establecida en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="0d0e3-115">The resource type for this allocation setting when the **ResourceType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="0d0e3-116">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-116">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0e3-117">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d0e3-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d0e3-119">Indica si se admite la solicitud de un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-119">Indicates whether requesting a specific resource is supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d0e3-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>

<span data-ttu-id="0d0e3-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Específico** (2)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-121"><span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span>**Specific** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0d0e3-122">La solicitud puede incluir una solicitud para un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-122">Request can include a request for specific resource.</span></span>

</dd> <dt>

<span id="General"></span><span id="general"></span><span id="GENERAL"></span>

<span data-ttu-id="0d0e3-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**General** (3)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-123"><span id="General"></span><span id="general"></span><span id="GENERAL"></span>**General** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0d0e3-124">La solicitud no incluye un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-124">Request does not include specific resource.</span></span>

</dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="0d0e3-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Ambos** (4)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-125"><span id="Both"></span><span id="both"></span><span id="BOTH"></span>**Both** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0d0e3-126">Se admiten tanto solicitudes específicas como generales.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-126">Both specific and general requests are supported.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0d0e3-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-127"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0d0e3-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="0d0e3-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d0e3-129">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-129">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0e3-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d0e3-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d0e3-132">Descripción de un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-132">A description of an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="0d0e3-133">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-133">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="0d0e3-134">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-134">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0e3-135">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d0e3-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-137">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AllocationCapabilities**.**OtherResourceType**","[**\_ ResourceAllocationSettingData CIM**](cim-resourceallocationsettingdata.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="0d0e3-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AllocationCapabilities**.**OtherResourceType**", "[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="0d0e3-138">El tipo de recurso que se asigna a esta configuración de asignación.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-138">The type of resource that is assigned to this allocation setting.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d0e3-139">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="0d0e3-140">**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-140">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="0d0e3-141">**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-141">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="0d0e3-142">**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-142">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="0d0e3-143">**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-143">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="0d0e3-144">**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-144">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="0d0e3-145">**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-145">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="0d0e3-146">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-146">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="0d0e3-147">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-147">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="0d0e3-148">**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-148">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="0d0e3-149">**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-149">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="0d0e3-150">**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-150">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="0d0e3-151">**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-151">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="0d0e3-152">**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-152">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="0d0e3-153">**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-153">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="0d0e3-154">**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-154">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="0d0e3-155">**Unidad de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-155">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="0d0e3-156">**Unidad de cinta** (18)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-156">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="0d0e3-157">**Extensión de almacenamiento** (19)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-157">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="0d0e3-158">**Otro dispositivo de almacenamiento** (20)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-158">**Other Storage Device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="0d0e3-159">**Puerto serie** (21)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-159">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="0d0e3-160">**Puerto paralelo** (22)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-160">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="0d0e3-161">**Controladora USB** (23)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-161">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="0d0e3-162">**Controladora de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-162">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="0d0e3-163">**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-163">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="0d0e3-164">**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-164">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="0d0e3-165">**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-165">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="0d0e3-166">**Potencia** (28)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-166">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="0d0e3-167">**Capacidad de enfriamiento** (29)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-167">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="0d0e3-168">**Puerto de conmutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-168">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="0d0e3-169">**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-169">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="0d0e3-170">**Volumen de almacenamiento** (32)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-170">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="0d0e3-171">**Conexión Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-171">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0d0e3-172">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-172">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0d0e3-173">**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="0d0e3-173">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d0e3-174">**SharingMode**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-174">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0e3-175">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d0e3-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d0e3-177">Indica cómo se concede el acceso al recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-177">Indicates how access to the underlying resource is granted.</span></span>

<span data-ttu-id="0d0e3-178">La cantidad real se controla mediante min, Max size, Weights, etc.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-178">Actual quantity is controlled by min, max size, weights, etc.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d0e3-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="0d0e3-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (2)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-180"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0d0e3-181">Acceso exclusivo al recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-181">Exclusive access to underlying resource.</span></span>

</dd> <dt>

<span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>

<span data-ttu-id="0d0e3-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Compartido** (3)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-182"><span id="Shared"></span><span id="shared"></span><span id="SHARED"></span>**Shared** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0d0e3-183">Uso compartido del recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-183">Shared use of underlying resource.</span></span>

</dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0d0e3-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-184"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0d0e3-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="0d0e3-185"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d0e3-186">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-186">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0e3-187">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-187">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d0e3-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-189">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="0d0e3-189">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="0d0e3-190">Los Estados del sistema que se admiten al crear un nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-190">The system states that are supported when a new resource is created.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d0e3-191">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0d0e3-192">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-192">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0d0e3-193">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-193">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="0d0e3-194">**Cerrando** (4)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-194">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d0e3-195">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-195">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="0d0e3-196">**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-196">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0d0e3-197">**En pruebas** (7)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-197">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="0d0e3-198">**Diferida** (8)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-198">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="0d0e3-199">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-199">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0d0e3-200">**Inicio** (10)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-200">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0d0e3-201">En **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-201">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="0d0e3-202">**Suspendido** (12)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-202">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0d0e3-203">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-203">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0d0e3-204">**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="0d0e3-204">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d0e3-205">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-205">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d0e3-206">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-206">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-207">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0d0e3-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d0e3-208">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="0d0e3-208">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="0d0e3-209">Estados del sistema que se admiten cuando se quita un recurso.</span><span class="sxs-lookup"><span data-stu-id="0d0e3-209">The system states that are supported when a resource is removed.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d0e3-210">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-210">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0d0e3-211">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-211">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0d0e3-212">**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-212">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="0d0e3-213">**Cerrando** (4)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-213">**Shutting Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d0e3-214">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-214">**Not Applicable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>

<span data-ttu-id="0d0e3-215">**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-215">**Enabled but Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0d0e3-216">**En pruebas** (7)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-216">**In Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="0d0e3-217">**Diferida** (8)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-217">**Deferred** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="0d0e3-218">Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-218">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0d0e3-219">**Inicio** (10)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-219">**Starting** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0d0e3-220">En **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-220">**Paused** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="0d0e3-221">**Suspendido** (12)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-221">**Suspended** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0d0e3-222">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0d0e3-222">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0d0e3-223">**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="0d0e3-223">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="0d0e3-224"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0d0e3-224"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0d0e3-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d0e3-225">Requirements</span></span>



| <span data-ttu-id="0d0e3-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d0e3-226">Requirement</span></span> | <span data-ttu-id="0d0e3-227">Value</span><span class="sxs-lookup"><span data-stu-id="0d0e3-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0e3-228">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d0e3-228">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0e3-229">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0d0e3-229">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0d0e3-230">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d0e3-230">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0e3-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0d0e3-231">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0d0e3-232">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d0e3-232">Namespace</span></span><br/>                | <span data-ttu-id="0d0e3-233">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0d0e3-233">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d0e3-234">MOF</span><span class="sxs-lookup"><span data-stu-id="0d0e3-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d0e3-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d0e3-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d0e3-236">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d0e3-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d0e3-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d0e3-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d0e3-238">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d0e3-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0e3-239">**Capacidades de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0d0e3-239">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

