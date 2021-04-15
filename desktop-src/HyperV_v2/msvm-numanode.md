---
description: Representa un nodo de acceso a memoria no uniforme (NUMA) de un sistema virtual.
ms.assetid: a2e9aa74-15e5-4a78-b7f8-ffe2883a31d0
title: Msvm_NumaNode (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NumaNode
- Msvm_NumaNode.RequestStateChange
- Msvm_NumaNode.InstanceID
- Msvm_NumaNode.Caption
- Msvm_NumaNode.Description
- Msvm_NumaNode.ElementName
- Msvm_NumaNode.InstallDate
- Msvm_NumaNode.Name
- Msvm_NumaNode.OperationalStatus
- Msvm_NumaNode.StatusDescriptions
- Msvm_NumaNode.Status
- Msvm_NumaNode.HealthState
- Msvm_NumaNode.CommunicationStatus
- Msvm_NumaNode.DetailedStatus
- Msvm_NumaNode.OperatingStatus
- Msvm_NumaNode.PrimaryStatus
- Msvm_NumaNode.EnabledState
- Msvm_NumaNode.OtherEnabledState
- Msvm_NumaNode.RequestedState
- Msvm_NumaNode.EnabledDefault
- Msvm_NumaNode.TimeOfLastStateChange
- Msvm_NumaNode.AvailableRequestedStates
- Msvm_NumaNode.TransitioningToState
- Msvm_NumaNode.SystemCreationClassName
- Msvm_NumaNode.SystemName
- Msvm_NumaNode.CreationClassName
- Msvm_NumaNode.NodeID
- Msvm_NumaNode.NumberOfProcessorCores
- Msvm_NumaNode.NumberOfLogicalProcessors
- Msvm_NumaNode.CurrentlyConsumableMemoryBlocks
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4bdbd600cd4a78f66376f21ee264b2dfe9854147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669766"
---
# <a name="msvm_numanode-class"></a><span data-ttu-id="9d1a7-103">MSVM \_ NumaNode (clase)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-103">Msvm\_NumaNode class</span></span>

<span data-ttu-id="9d1a7-104">Representa un nodo de acceso a memoria no uniforme (NUMA) de un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-104">Represents a Non-Uniform Memory Access (NUMA) node of a virtual system.</span></span>

<span data-ttu-id="9d1a7-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1a7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d1a7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_NumaNode : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NodeID;
  uint32   NumberOfProcessorCores;
  uint32   NumberOfLogicalProcessors;
  uint64   CurrentlyConsumableMemoryBlocks;
};
```

## <a name="members"></a><span data-ttu-id="9d1a7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9d1a7-107">Members</span></span>

<span data-ttu-id="9d1a7-108">La clase **MSVM \_ NumaNode** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9d1a7-108">The **Msvm\_NumaNode** class has these types of members:</span></span>

-   [<span data-ttu-id="9d1a7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d1a7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="9d1a7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9d1a7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9d1a7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d1a7-111">Methods</span></span>

<span data-ttu-id="9d1a7-112">La clase **MSVM \_ NumaNode** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-112">The **Msvm\_NumaNode** class has these methods.</span></span>



| <span data-ttu-id="9d1a7-113">Método</span><span class="sxs-lookup"><span data-stu-id="9d1a7-113">Method</span></span>                 | <span data-ttu-id="9d1a7-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d1a7-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="9d1a7-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-115">**RequestStateChange**</span></span> | <span data-ttu-id="9d1a7-116">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-116">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9d1a7-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9d1a7-117">Properties</span></span>

<span data-ttu-id="9d1a7-118">La clase **MSVM \_ NumaNode** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-118">The **Msvm\_NumaNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d1a7-119">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-119">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-120">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-122">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9d1a7-122">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="9d1a7-123">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-123">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-127">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-127">A short description of the object.</span></span> <span data-ttu-id="9d1a7-128">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-129">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-129">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-132">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-132">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9d1a7-133">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9d1a7-134">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9d1a7-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-136"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-137"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-138"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-139"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-140"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9d1a7-141"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9d1a7-142">)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-142">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d1a7-143">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-143">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-146">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-147">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-147">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-148">**CurrentlyConsumableMemoryBlocks**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-148">**CurrentlyConsumableMemoryBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-149">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-151">El número de bloques de memoria actualmente disponibles para el consumo por parte de las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-151">The number of memory blocks currently available for consumption by virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-152">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-152">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-155">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-155">A description of the object.</span></span> <span data-ttu-id="9d1a7-156">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-157">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-157">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-158">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-158">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-160">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-160">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9d1a7-161">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-161">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9d1a7-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9d1a7-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-163"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-164"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-165"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-166"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-167"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-168"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-169"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9d1a7-170"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9d1a7-171">)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-171">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d1a7-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-175">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-175">A display name for the object.</span></span> <span data-ttu-id="9d1a7-176">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-177">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-177">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-178">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-180">Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-180">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9d1a7-181">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-181">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-182">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-182">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-183">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-185">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-185">The enabled and disabled states of an element.</span></span> <span data-ttu-id="9d1a7-186">También puede indicar las transiciones entre estos Estados solicitados.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-186">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="9d1a7-187">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="9d1a7-188">Value</span><span class="sxs-lookup"><span data-stu-id="9d1a7-188">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9d1a7-189">Significado</span><span class="sxs-lookup"><span data-stu-id="9d1a7-189">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9d1a7-190"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-190"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9d1a7-191">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-191">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9d1a7-192"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-192"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="9d1a7-193"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-193"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="9d1a7-194">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-194">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="9d1a7-195"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-195"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9d1a7-196">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-196">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="9d1a7-197"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-197"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="9d1a7-198">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-198">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="9d1a7-199"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="9d1a7-200">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-200">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="9d1a7-201"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="9d1a7-202">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-202">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="9d1a7-203"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-203"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="9d1a7-204">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-204">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="9d1a7-205"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-205"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="9d1a7-206">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-206">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="9d1a7-207">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-207"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="9d1a7-208">El elemento está habilitado, pero está en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-208">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="9d1a7-209">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-209">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="9d1a7-210">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-210">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="9d1a7-211"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-211"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="9d1a7-212">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-212">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="9d1a7-213">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-213">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="9d1a7-214">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-214">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-215">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-216">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-217">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-217">The current health of the element.</span></span> <span data-ttu-id="9d1a7-218">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-218">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9d1a7-219">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-219">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9d1a7-220">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-221">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-221">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-222">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-222">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-223">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-224">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-224">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="9d1a7-225">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-225">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-226">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-226">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-229">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-229">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-230">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-230">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9d1a7-231">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-231">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-232">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-232">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-233">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-234">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-235">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-235">The label by which the object is known.</span></span> <span data-ttu-id="9d1a7-236">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-236">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-237">**NodeID**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-237">**NodeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-238">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-238">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-239">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-240">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-240">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-241">Identificador del nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-241">The NUMA node identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-242">**NumberOfLogicalProcessors**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-242">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-243">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-245">Número total de núcleos de procesador lógico en este nodo.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-245">The total number of logical processor cores in this node.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-246">**NumberOfProcessorCores**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-246">**NumberOfProcessorCores**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-247">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-249">El número total de núcleos de procesador en este nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-249">The total number of processor cores in this NUMA node.</span></span> <span data-ttu-id="9d1a7-250">Esto puede diferir del número de objetos de [**\_ procesador de MSVM**](msvm-processor.md) asociados a este nodo si cada núcleo de procesador admite varios subprocesos de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-250">This may differ from the number of [**Msvm\_Processor**](msvm-processor.md) objects associated to this node if each processor core supports multiple compute threads.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-251">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-251">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-252">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-254">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9d1a7-254">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9d1a7-255">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9d1a7-256">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9d1a7-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-257"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-258"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-259"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-260"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-261"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-262"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-263"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-264"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-265"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-266"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-267"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-268"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-269"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-270"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-271"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-272"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-273"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-274"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9d1a7-275"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9d1a7-276">)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-276">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d1a7-277">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-277">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-278">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-278">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-280">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-280">The current statuses of the object.</span></span> <span data-ttu-id="9d1a7-281">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-282">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-282">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-283">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-284">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-285">Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-285">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="9d1a7-286">Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-286">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9d1a7-287">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-287">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-288">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-288">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-289">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-289">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-290">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-291">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-291">Provides high level status information.</span></span> <span data-ttu-id="9d1a7-292">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-292">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="9d1a7-293">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-293">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9d1a7-294">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-294">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="9d1a7-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-295"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-296"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-296"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-297"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-298"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-299"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="9d1a7-300"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="9d1a7-301">)</span><span class="sxs-lookup"><span data-stu-id="9d1a7-301">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d1a7-302">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-302">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-303">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-305">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-305">The last requested or desired state for the element.</span></span> <span data-ttu-id="9d1a7-306">El estado real del elemento se representa mediante **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-306">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="9d1a7-307">Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-307">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="9d1a7-308">Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="9d1a7-308">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support the **RequestStateChange** method.</span></span> <span data-ttu-id="9d1a7-309">Si esto ocurre, se usa el valor 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-309">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="9d1a7-310">Esta propiedad se hereda de **\_ EnabledLogicalElement CIM**.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-310">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-311">**Estado**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-311">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-312">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-314">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-315">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-315">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-316">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-316">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-317">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-318">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9d1a7-318">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9d1a7-319">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-320">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-320">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-321">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-322">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-323">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="9d1a7-323">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-324">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-324">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-325">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-325">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-326">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-327">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-328">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="9d1a7-328">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-329">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-329">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-330">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-330">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-331">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-332">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-333">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-333">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9d1a7-334">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en "null".</span><span class="sxs-lookup"><span data-stu-id="9d1a7-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to "NULL".</span></span>

</dd> <dt>

<span data-ttu-id="9d1a7-335">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-335">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d1a7-336">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d1a7-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d1a7-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9d1a7-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d1a7-338">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="9d1a7-338">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9d1a7-339">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9d1a7-339">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d1a7-340">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d1a7-340">Requirements</span></span>



| <span data-ttu-id="9d1a7-341">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d1a7-341">Requirement</span></span> | <span data-ttu-id="9d1a7-342">Value</span><span class="sxs-lookup"><span data-stu-id="9d1a7-342">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1a7-343">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d1a7-343">Minimum supported client</span></span><br/> | <span data-ttu-id="9d1a7-344">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d1a7-344">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d1a7-345">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9d1a7-345">Minimum supported server</span></span><br/> | <span data-ttu-id="9d1a7-346">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9d1a7-346">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d1a7-347">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9d1a7-347">Namespace</span></span><br/>                | <span data-ttu-id="9d1a7-348">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9d1a7-348">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d1a7-349">MOF</span><span class="sxs-lookup"><span data-stu-id="9d1a7-349">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d1a7-350"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-350"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d1a7-351">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9d1a7-351">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d1a7-352"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d1a7-352"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

