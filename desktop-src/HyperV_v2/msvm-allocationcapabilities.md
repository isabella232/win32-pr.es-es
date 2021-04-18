---
description: Define los medios por los que un cliente puede detectar el intervalo válido de valores predeterminados para un recurso virtual.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Msvm_AllocationCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7642d1b590affcb3704f7d854d65edb5481c2285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688454"
---
# <a name="msvm_allocationcapabilities-class"></a><span data-ttu-id="140c3-103">MSVM \_ AllocationCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="140c3-103">Msvm\_AllocationCapabilities class</span></span>

<span data-ttu-id="140c3-104">Define los medios por los que un cliente puede detectar el intervalo válido de valores predeterminados para un recurso virtual.</span><span class="sxs-lookup"><span data-stu-id="140c3-104">Defines the means by which a client can discover the valid range of default settings for a virtual resource.</span></span> <span data-ttu-id="140c3-105">Un objeto **MSVM \_ AllocationCapabilities** está asociado a cada grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="140c3-105">A **Msvm\_AllocationCapabilities** object is associated with each resource pool.</span></span> <span data-ttu-id="140c3-106">Cuatro objetos [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) están asociados al objeto **MSVM \_ AllocationCapabilities** para describir los valores mínimo, máximo, predeterminado e incremental para la asignación del recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="140c3-106">Four [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) objects are associated with the **Msvm\_AllocationCapabilities** object to describe the minimum, maximum, default, and incremental values for the given resource's allocation.</span></span> <span data-ttu-id="140c3-107">Juntas, estas clases describen el intervalo general de las capacidades admitidas.</span><span class="sxs-lookup"><span data-stu-id="140c3-107">Together, these classes describe the overall range of supported capabilities.</span></span>

<span data-ttu-id="140c3-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="140c3-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="140c3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="140c3-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a><span data-ttu-id="140c3-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="140c3-110">Members</span></span>

<span data-ttu-id="140c3-111">La clase **MSVM \_ AllocationCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="140c3-111">The **Msvm\_AllocationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="140c3-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="140c3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="140c3-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="140c3-113">Properties</span></span>

<span data-ttu-id="140c3-114">La clase **MSVM \_ AllocationCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="140c3-114">The **Msvm\_AllocationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="140c3-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="140c3-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="140c3-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="140c3-118">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="140c3-118">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="140c3-119">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="140c3-119">A short description of the object.</span></span> <span data-ttu-id="140c3-120">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="140c3-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="140c3-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="140c3-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="140c3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-124">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="140c3-124">A description of the object.</span></span> <span data-ttu-id="140c3-125">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="140c3-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="140c3-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="140c3-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="140c3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-129">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="140c3-129">A display name for the object.</span></span> <span data-ttu-id="140c3-130">Esta propiedad permite a cada instancia definir un nombre para mostrar además de las propiedades de clave, los datos de identidad y la información de descripción.</span><span class="sxs-lookup"><span data-stu-id="140c3-130">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="140c3-131">La propiedad [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la clase del **\_ ManagedSystemElement de CIM** también se define como un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="140c3-131">The [**Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) property of the **CIM\_ManagedSystemElement** class is also defined as a display name.</span></span> <span data-ttu-id="140c3-132">Sin embargo, a menudo se considera una clave.</span><span class="sxs-lookup"><span data-stu-id="140c3-132">But, it is often subclassed to be a Key.</span></span> <span data-ttu-id="140c3-133">No es razonable que la misma propiedad pueda transmitir tanto la identidad como un nombre para mostrar, sin incoherencias.</span><span class="sxs-lookup"><span data-stu-id="140c3-133">It is not reasonable that the same property can convey both identity and a display name, without inconsistencies.</span></span> <span data-ttu-id="140c3-134">Donde el [**nombre**](msvm-keyboard.md) existe y no es una clave (por ejemplo, para las instancias de un dispositivo lógico), la misma información puede estar presente en las propiedades **nombre** y **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="140c3-134">Where [**Name**](msvm-keyboard.md) exists and is not a Key (such as for instances of a logical device), the same information can be present in both the **Name** and **ElementName** properties.</span></span> <span data-ttu-id="140c3-135">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="140c3-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="140c3-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="140c3-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="140c3-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-139">Identificador único para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="140c3-139">A unique identifier for this resource pool.</span></span> <span data-ttu-id="140c3-140">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="140c3-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="140c3-141">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="140c3-141">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="140c3-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-144">Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **resourcetype** tiene el valor "Other".</span><span class="sxs-lookup"><span data-stu-id="140c3-144">A string that describes the resource type when a well-defined value is not available and **ResourceType** has the value "Other".</span></span> <span data-ttu-id="140c3-145">Esta propiedad se hereda de [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="140c3-145">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="140c3-146">**RequestTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="140c3-146">**RequestTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-147">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="140c3-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-149">Indica si se admite la solicitud de un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="140c3-149">Indicates whether requesting a specific resource is supported.</span></span> <span data-ttu-id="140c3-150">Esta propiedad se hereda de [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="140c3-150">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="140c3-151">Value</span><span class="sxs-lookup"><span data-stu-id="140c3-151">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="140c3-152">Significado</span><span class="sxs-lookup"><span data-stu-id="140c3-152">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="140c3-153"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="140c3-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="140c3-154">Unknown</span><span class="sxs-lookup"><span data-stu-id="140c3-154">Unknown</span></span><br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <span data-ttu-id="140c3-155"><dt>**Específico**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="140c3-155"><dt>**Specific**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="140c3-156">La solicitud puede incluir una solicitud para un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="140c3-156">The request can include a request for a specific resource.</span></span><br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <span data-ttu-id="140c3-157"><dt>**General**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="140c3-157"><dt>**General**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="140c3-158">La solicitud no incluye una solicitud para un recurso específico.</span><span class="sxs-lookup"><span data-stu-id="140c3-158">The request does not include a request for a specific resource.</span></span><br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <span data-ttu-id="140c3-159"><dt>**Ambos**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="140c3-159"><dt>**Both**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="140c3-160">Se admiten tanto solicitudes específicas como generales.</span><span class="sxs-lookup"><span data-stu-id="140c3-160">Both specific and general requests are supported.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="140c3-161">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="140c3-161">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="140c3-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-164">Cadena que describe un subtipo específico de implementación para este recurso.</span><span class="sxs-lookup"><span data-stu-id="140c3-164">A string that describes an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="140c3-165">Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="140c3-165">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="140c3-166">Esta propiedad se hereda de [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="140c3-166">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="140c3-167">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="140c3-167">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="140c3-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-170">Tipo de recurso que esta configuración de asignación representa.</span><span class="sxs-lookup"><span data-stu-id="140c3-170">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="140c3-171">Esta propiedad se hereda de [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="140c3-171">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="140c3-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="140c3-172"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="140c3-173"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="140c3-174"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="140c3-175"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controladora IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="140c3-176"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="140c3-177"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA de FC** (7)</span><span class="sxs-lookup"><span data-stu-id="140c3-178"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="140c3-179"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="140c3-180"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="140c3-181"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="140c3-182"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de e/s** (12)</span><span class="sxs-lookup"><span data-stu-id="140c3-183"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)</span><span class="sxs-lookup"><span data-stu-id="140c3-184"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidad de disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="140c3-185"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="140c3-186"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="140c3-187"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidad de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="140c3-188"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidad de cinta** (18)</span><span class="sxs-lookup"><span data-stu-id="140c3-189"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de almacenamiento** (19)</span><span class="sxs-lookup"><span data-stu-id="140c3-190"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (20)</span><span class="sxs-lookup"><span data-stu-id="140c3-191"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (21)</span><span class="sxs-lookup"><span data-stu-id="140c3-192"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (22)</span><span class="sxs-lookup"><span data-stu-id="140c3-193"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controladora USB** (23)</span><span class="sxs-lookup"><span data-stu-id="140c3-194"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controladora de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="140c3-195"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controlador IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="140c3-196"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="140c3-197"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base con particiones** (27)</span><span class="sxs-lookup"><span data-stu-id="140c3-198"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Potencia** (28)</span><span class="sxs-lookup"><span data-stu-id="140c3-199"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacidad de enfriamiento** (29)</span><span class="sxs-lookup"><span data-stu-id="140c3-200"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Puerto de conmutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="140c3-201"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="140c3-202"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volumen de almacenamiento** (32)</span><span class="sxs-lookup"><span data-stu-id="140c3-203"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexión Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="140c3-204"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="140c3-205"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="140c3-206"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="140c3-207">**SharingMode**</span><span class="sxs-lookup"><span data-stu-id="140c3-207">**SharingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-208">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="140c3-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="140c3-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-210">Indica cómo se concede el acceso a un recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="140c3-210">Indicates how access to an underlying resource is granted.</span></span> <span data-ttu-id="140c3-211">Esta propiedad se hereda de [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="140c3-211">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>



| <span data-ttu-id="140c3-212">Value</span><span class="sxs-lookup"><span data-stu-id="140c3-212">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="140c3-213">Significado</span><span class="sxs-lookup"><span data-stu-id="140c3-213">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="140c3-214"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="140c3-214"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="140c3-215">Unknown</span><span class="sxs-lookup"><span data-stu-id="140c3-215">Unknown</span></span><br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <span data-ttu-id="140c3-216"><dt>**Dedicado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="140c3-216"><dt>**Dedicated**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="140c3-217">Acceso exclusivo a un recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="140c3-217">Exclusive access to an underlying resource.</span></span><br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <span data-ttu-id="140c3-218"><dt>**Compartido**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="140c3-218"><dt>**Shared**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="140c3-219">Uso compartido de un recurso subyacente.</span><span class="sxs-lookup"><span data-stu-id="140c3-219">Shared use of an underlying resource.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="140c3-220">**SupportedAddStates**</span><span class="sxs-lookup"><span data-stu-id="140c3-220">**SupportedAddStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-221">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="140c3-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="140c3-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-223">Indica los Estados en los que el sistema al que se asociará el recurso puede estar en el momento en que se crea un nuevo recurso.</span><span class="sxs-lookup"><span data-stu-id="140c3-223">Indicates the states that the system to which the resource will be associated can be in when a new resource is created.</span></span> <span data-ttu-id="140c3-224">Esta propiedad se hereda de [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="140c3-224">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="140c3-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="140c3-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="140c3-226"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="140c3-227"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (4)</span><span class="sxs-lookup"><span data-stu-id="140c3-228"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="140c3-229"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="140c3-230"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (7)</span><span class="sxs-lookup"><span data-stu-id="140c3-231"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Diferida** (8)</span><span class="sxs-lookup"><span data-stu-id="140c3-232"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="140c3-233"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (10)</span><span class="sxs-lookup"><span data-stu-id="140c3-234"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="140c3-235"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (12)</span><span class="sxs-lookup"><span data-stu-id="140c3-236"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="140c3-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="140c3-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="140c3-239">**SupportedRemoveStates**</span><span class="sxs-lookup"><span data-stu-id="140c3-239">**SupportedRemoveStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="140c3-240">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="140c3-240">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="140c3-241">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="140c3-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="140c3-242">Indica los Estados en los que el sistema al que está asociado el recurso puede estar en el momento en que se quita el recurso.</span><span class="sxs-lookup"><span data-stu-id="140c3-242">Indicates the states that the system to which the resource is associated can be in when the resource is removed.</span></span> <span data-ttu-id="140c3-243">Esta propiedad se hereda de [**\_ AllocationCapabilities CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span><span class="sxs-lookup"><span data-stu-id="140c3-243">This property is inherited from [**CIM\_AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities).</span></span>

<dl> <dt>

<span data-ttu-id="140c3-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="140c3-244"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="140c3-245"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="140c3-246"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (4)</span><span class="sxs-lookup"><span data-stu-id="140c3-247"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="140c3-248"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)</span><span class="sxs-lookup"><span data-stu-id="140c3-249"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (7)</span><span class="sxs-lookup"><span data-stu-id="140c3-250"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Diferida** (8)</span><span class="sxs-lookup"><span data-stu-id="140c3-251"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)</span><span class="sxs-lookup"><span data-stu-id="140c3-252"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (10)</span><span class="sxs-lookup"><span data-stu-id="140c3-253"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (10)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (11)</span><span class="sxs-lookup"><span data-stu-id="140c3-254"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (11)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (12)</span><span class="sxs-lookup"><span data-stu-id="140c3-255"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (12)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="140c3-256"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="140c3-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="140c3-257"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="140c3-258">Observaciones</span><span class="sxs-lookup"><span data-stu-id="140c3-258">Remarks</span></span>

<span data-ttu-id="140c3-259">El acceso a la clase **MSVM \_ AllocationCapabilities** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="140c3-259">Access to the **Msvm\_AllocationCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="140c3-260">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="140c3-260">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="140c3-261">Requisitos</span><span class="sxs-lookup"><span data-stu-id="140c3-261">Requirements</span></span>



| <span data-ttu-id="140c3-262">Requisito</span><span class="sxs-lookup"><span data-stu-id="140c3-262">Requirement</span></span> | <span data-ttu-id="140c3-263">Value</span><span class="sxs-lookup"><span data-stu-id="140c3-263">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140c3-264">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="140c3-264">Minimum supported client</span></span><br/> | <span data-ttu-id="140c3-265">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="140c3-265">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="140c3-266">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="140c3-266">Minimum supported server</span></span><br/> | <span data-ttu-id="140c3-267">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="140c3-267">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="140c3-268">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="140c3-268">Namespace</span></span><br/>                | <span data-ttu-id="140c3-269">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="140c3-269">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="140c3-270">MOF</span><span class="sxs-lookup"><span data-stu-id="140c3-270">MOF</span></span><br/>                      | <dl> <span data-ttu-id="140c3-271"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="140c3-271"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="140c3-272">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="140c3-272">DLL</span></span><br/>                      | <dl> <span data-ttu-id="140c3-273"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="140c3-273"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="140c3-274">Vea también</span><span class="sxs-lookup"><span data-stu-id="140c3-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140c3-275">**\_ALLOCATIONCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="140c3-275">**CIM\_AllocationCapabilities**</span></span>](cim-allocationcapabilities.md)
</dt> <dt>

[<span data-ttu-id="140c3-276">**\_ALLOCATIONCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="140c3-276">**CIM\_AllocationCapabilities**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="140c3-277">**MSVM \_ AllocationCapabilities (V1)**</span><span class="sxs-lookup"><span data-stu-id="140c3-277">**Msvm\_AllocationCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[<span data-ttu-id="140c3-278">Clases de administración de recursos</span><span class="sxs-lookup"><span data-stu-id="140c3-278">Resource Management Classes</span></span>](resource-management-classes.md)
</dt> </dl>

 

