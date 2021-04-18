---
description: Define una asignación de un tipo de recurso a sus clases de implementación.
ms.assetid: 0911454D-2494-49D5-8480-212E9ADD1B45
title: Msvm_ResourceTypeDefinition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceTypeDefinition
- Msvm_ResourceTypeDefinition.ResourceType
- Msvm_ResourceTypeDefinition.OtherResourceType
- Msvm_ResourceTypeDefinition.ResourceSubType
- Msvm_ResourceTypeDefinition.LogicalDeviceClassName
- Msvm_ResourceTypeDefinition.SettingDataClassName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: edfbf2ec9772fa710df5fc0d024abfcad6d826d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687946"
---
# <a name="msvm_resourcetypedefinition-class"></a><span data-ttu-id="34bf6-103">MSVM \_ ResourceTypeDefinition (clase)</span><span class="sxs-lookup"><span data-stu-id="34bf6-103">Msvm\_ResourceTypeDefinition class</span></span>

<span data-ttu-id="34bf6-104">Define una asignación de un tipo de recurso a sus clases de implementación.</span><span class="sxs-lookup"><span data-stu-id="34bf6-104">Defines a mapping of a resource type to its implementation classes.</span></span>

<span data-ttu-id="34bf6-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="34bf6-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="34bf6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34bf6-106">Syntax</span></span>

``` syntax
class Msvm_ResourceTypeDefinition
{
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  string LogicalDeviceClassName;
  string SettingDataClassName;
};
```

## <a name="members"></a><span data-ttu-id="34bf6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="34bf6-107">Members</span></span>

<span data-ttu-id="34bf6-108">La clase **MSVM \_ ResourceTypeDefinition** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="34bf6-108">The **Msvm\_ResourceTypeDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="34bf6-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34bf6-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34bf6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34bf6-110">Properties</span></span>

<span data-ttu-id="34bf6-111">La clase **MSVM \_ ResourceTypeDefinition** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="34bf6-111">The **Msvm\_ResourceTypeDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34bf6-112">**LogicalDeviceClassName**</span><span class="sxs-lookup"><span data-stu-id="34bf6-112">**LogicalDeviceClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34bf6-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="34bf6-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="34bf6-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34bf6-115">Nombre de la clase derivada del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que implementa el dispositivo lógico para este tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="34bf6-115">The name of the class derived from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) that implements the logical device for this resource type.</span></span>

</dd> <dt>

<span data-ttu-id="34bf6-116">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="34bf6-116">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34bf6-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="34bf6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="34bf6-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-119">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="34bf6-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="34bf6-120">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="34bf6-120">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value 1 (Other).</span></span> <span data-ttu-id="34bf6-121">Existe una correspondencia con la propiedad **OtherResourceType** de [**\_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="34bf6-121">There is a correspondence with the **OtherResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="34bf6-122">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="34bf6-122">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34bf6-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="34bf6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="34bf6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-125">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="34bf6-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="34bf6-126">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="34bf6-126">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="34bf6-127">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="34bf6-127">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="34bf6-128">Existe una correspondencia con la propiedad **subtipo** de [**\_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="34bf6-128">There is a correspondence with the **ResourceSubType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="34bf6-129">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="34bf6-129">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34bf6-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="34bf6-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="34bf6-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-132">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="34bf6-132">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="34bf6-133">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="34bf6-133">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="34bf6-134">Existe una correspondencia con la propiedad **resourcetype** de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="34bf6-134">There is a correspondence with the **ResourceType** property of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="34bf6-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="34bf6-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="34bf6-136"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="34bf6-137"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="34bf6-138"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="34bf6-139"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="34bf6-140"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="34bf6-141"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="34bf6-142"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="34bf6-143"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="34bf6-144"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="34bf6-145"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="34bf6-146"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="34bf6-147"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="34bf6-148"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="34bf6-149"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="34bf6-150"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (17)</span><span class="sxs-lookup"><span data-stu-id="34bf6-151"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (18)</span><span class="sxs-lookup"><span data-stu-id="34bf6-152"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controladora USB** (19)</span><span class="sxs-lookup"><span data-stu-id="34bf6-153"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controladora de gráficos** (20)</span><span class="sxs-lookup"><span data-stu-id="34bf6-154"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de almacenamiento** (21)</span><span class="sxs-lookup"><span data-stu-id="34bf6-155"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="34bf6-156"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Cinta** (23)</span><span class="sxs-lookup"><span data-stu-id="34bf6-157"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (24)</span><span class="sxs-lookup"><span data-stu-id="34bf6-158"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controlador Firewire** (25)</span><span class="sxs-lookup"><span data-stu-id="34bf6-159"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="34bf6-160"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="34bf6-161"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fuente de alimentación** (28)</span><span class="sxs-lookup"><span data-stu-id="34bf6-162"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de refrigeración** (29)</span><span class="sxs-lookup"><span data-stu-id="34bf6-163"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="34bf6-164"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="34bf6-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="34bf6-166">**SettingDataClassName**</span><span class="sxs-lookup"><span data-stu-id="34bf6-166">**SettingDataClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34bf6-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="34bf6-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="34bf6-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="34bf6-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34bf6-169">Nombre de la clase derivada de [**\_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que implementa la configuración para este tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="34bf6-169">The name of the class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) that implements the settings for this resource type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34bf6-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34bf6-170">Remarks</span></span>

<span data-ttu-id="34bf6-171">El acceso a la clase **MSVM \_ ResourceTypeDefinition** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="34bf6-171">Access to the **Msvm\_ResourceTypeDefinition** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="34bf6-172">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="34bf6-172">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="34bf6-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34bf6-173">Requirements</span></span>



| <span data-ttu-id="34bf6-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="34bf6-174">Requirement</span></span> | <span data-ttu-id="34bf6-175">Value</span><span class="sxs-lookup"><span data-stu-id="34bf6-175">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34bf6-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34bf6-176">Minimum supported client</span></span><br/> | <span data-ttu-id="34bf6-177">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="34bf6-177">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34bf6-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34bf6-178">Minimum supported server</span></span><br/> | <span data-ttu-id="34bf6-179">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="34bf6-179">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34bf6-180">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="34bf6-180">End of client support</span></span><br/>    | <span data-ttu-id="34bf6-181">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="34bf6-181">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="34bf6-182">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="34bf6-182">End of server support</span></span><br/>    | <span data-ttu-id="34bf6-183">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="34bf6-183">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="34bf6-184">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="34bf6-184">Namespace</span></span><br/>                | <span data-ttu-id="34bf6-185">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="34bf6-185">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="34bf6-186">MOF</span><span class="sxs-lookup"><span data-stu-id="34bf6-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34bf6-187"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34bf6-187"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34bf6-188">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34bf6-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34bf6-189"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34bf6-189"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

