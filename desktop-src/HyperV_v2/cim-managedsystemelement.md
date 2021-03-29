---
description: El \_ ManagedSystemElement de CIM es la clase base para la jerarquía de elementos del sistema. Cualquier componente de un sistema podría estar representado por esta clase o sus subclases.
ms.assetid: 838cc77f-8a8d-429a-8e17-5ede3cc9b6ed
title: CIM_ManagedSystemElement (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.OperationalStatus
- CIM_ManagedSystemElement.StatusDescriptions
- CIM_ManagedSystemElement.Status
- CIM_ManagedSystemElement.HealthState
- CIM_ManagedSystemElement.CommunicationStatus
- CIM_ManagedSystemElement.DetailedStatus
- CIM_ManagedSystemElement.OperatingStatus
- CIM_ManagedSystemElement.PrimaryStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f16b84e24929d5cfdb6e5dd8855d69a8bce2dfda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277577"
---
# <a name="cim_managedsystemelement-class-hyper-v-management"></a><span data-ttu-id="0bfae-104">CIM_ManagedSystemElement (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="0bfae-104">CIM_ManagedSystemElement class (Hyper-V management)</span></span>

<span data-ttu-id="0bfae-105">**CIM \_ ManagedSystemElement** es la clase base para la jerarquía de elementos del sistema.</span><span class="sxs-lookup"><span data-stu-id="0bfae-105">**CIM\_ManagedSystemElement** is the base class for the system element hierarchy.</span></span> <span data-ttu-id="0bfae-106">Cualquier componente de un sistema podría estar representado por esta clase o sus subclases.</span><span class="sxs-lookup"><span data-stu-id="0bfae-106">Any component of a system can potentially be represented by this class or its subclasses.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bfae-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bfae-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedSystemElement : CIM_ManagedElement
{
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
};
```

## <a name="members"></a><span data-ttu-id="0bfae-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0bfae-108">Members</span></span>

<span data-ttu-id="0bfae-109">La clase del **\_ ManagedSystemElement de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0bfae-109">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="0bfae-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0bfae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0bfae-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0bfae-111">Properties</span></span>

<span data-ttu-id="0bfae-112">La clase del **\_ ManagedSystemElement de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0bfae-112">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0bfae-113">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="0bfae-113">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bfae-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-116">Indica la capacidad de la instrumentación de comunicarse con este elemento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-116">Indicates the ability of the instrumentation to communicate with this element.</span></span> <span data-ttu-id="0bfae-117">Un valor **null** indica que la instrumentación no admite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0bfae-117">A **NULL** value indicates that instrumentation does not support this property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bfae-118">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bfae-118">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="0bfae-119">**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="0bfae-119">**Not Available** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>

<span data-ttu-id="0bfae-120">**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="0bfae-120">**Communication OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="0bfae-121">**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="0bfae-121">**Lost Communication** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0bfae-122">**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="0bfae-122">**No Contact** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0bfae-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0bfae-123">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0bfae-124">**Proveedor reservado** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="0bfae-124">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bfae-125">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="0bfae-125">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bfae-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-128">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**","**el \_ ManagedSystemElement de CIM**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="0bfae-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**PrimaryStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-129">Indica detalles de estado adicionales que complementan la propiedad **PrimaryStatus** .</span><span class="sxs-lookup"><span data-stu-id="0bfae-129">Indicates additional status details that complement the **PrimaryStatus** property.</span></span> <span data-ttu-id="0bfae-130">Un valor **null** indica que la instrumentación no admite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0bfae-130">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="0bfae-131">**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="0bfae-131">**Not Available** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>

<span data-ttu-id="0bfae-132">**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="0bfae-132">**No Additional Information** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0bfae-133">Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="0bfae-133">**Stressed** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="0bfae-134">**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="0bfae-134">**Predictive Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="0bfae-135">**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="0bfae-135">**Non-Recoverable Error** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="0bfae-136">**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="0bfae-136">**Supporting Entity in Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0bfae-137">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0bfae-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0bfae-138">**Proveedor reservado** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="0bfae-138">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bfae-139">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0bfae-139">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bfae-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-142">Indica el estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-142">Indicates the current health of the element.</span></span> <span data-ttu-id="0bfae-143">Este atributo expresa el estado de este elemento, pero no necesariamente el estado de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="0bfae-143">This attribute expresses the health of this element, but not necessarily the health of its subcomponents.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bfae-144">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bfae-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0bfae-145">**Aceptar** (5)</span><span class="sxs-lookup"><span data-stu-id="0bfae-145">**OK** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="0bfae-146">**Degradado/ADVERTENCIA** (10)</span><span class="sxs-lookup"><span data-stu-id="0bfae-146">**Degraded/Warning** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Minor_failure"></span><span id="minor_failure"></span><span id="MINOR_FAILURE"></span>

<span data-ttu-id="0bfae-147">**Error leve** (15)</span><span class="sxs-lookup"><span data-stu-id="0bfae-147">**Minor failure** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Major_failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span>

<span data-ttu-id="0bfae-148">**Error principal** (20)</span><span class="sxs-lookup"><span data-stu-id="0bfae-148">**Major failure** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span>

<span data-ttu-id="0bfae-149">**Error crítico** (25)</span><span class="sxs-lookup"><span data-stu-id="0bfae-149">**Critical failure** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable_error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="0bfae-150">**Error no recuperable** (30)</span><span class="sxs-lookup"><span data-stu-id="0bfae-150">**Non-recoverable error** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0bfae-151">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0bfae-151">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bfae-152">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0bfae-152">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-153">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0bfae-153">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-155">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0bfae-155">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-156">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="0bfae-156">Indicates when the object was installed.</span></span> <span data-ttu-id="0bfae-157">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="0bfae-157">The lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="0bfae-158">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0bfae-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0bfae-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-161">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="0bfae-161">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-162">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="0bfae-162">The label by which the object is known.</span></span> <span data-ttu-id="0bfae-163">Cuando se subclasen, la propiedad **Name** se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="0bfae-163">When subclassed, the **Name** property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="0bfae-164">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="0bfae-164">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bfae-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-167">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span><span class="sxs-lookup"><span data-stu-id="0bfae-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**EnabledState**")</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-168">Indica la condición operativa actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-168">Indicates the current operational condition of the element.</span></span> <span data-ttu-id="0bfae-169">Esta propiedad se puede usar para proporcionar más detalles sobre el valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="0bfae-169">This property can be used to provide more detail about the value of the **EnabledState** property.</span></span> <span data-ttu-id="0bfae-170">Un valor **null** indica que la instrumentación no admite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="0bfae-170">A **NULL** value indicates that the instrumentation does not support this property.</span></span>

<span data-ttu-id="0bfae-171">"Unknown" indica</span><span class="sxs-lookup"><span data-stu-id="0bfae-171">"Unknown" indicates</span></span>

<span data-ttu-id="0bfae-172">"None" indica que</span><span class="sxs-lookup"><span data-stu-id="0bfae-172">"None" indicates that</span></span>

<span data-ttu-id="0bfae-173">Mantenimiento</span><span class="sxs-lookup"><span data-stu-id="0bfae-173">"Servicing"</span></span>

<span data-ttu-id="0bfae-174">Comenzar</span><span class="sxs-lookup"><span data-stu-id="0bfae-174">"Starting"</span></span>

<span data-ttu-id="0bfae-175">Bloqueo</span><span class="sxs-lookup"><span data-stu-id="0bfae-175">"Stopping"</span></span>

<span data-ttu-id="0bfae-176">"Stopped" y "Abortd" son similares, aunque el primero, mientras que el segundo</span><span class="sxs-lookup"><span data-stu-id="0bfae-176">"Stopped" and "Aborted" are similar, although the former , while the latter i</span></span>

<span data-ttu-id="0bfae-177">"Inactivo" indica que</span><span class="sxs-lookup"><span data-stu-id="0bfae-177">"Dormant" indicates that</span></span>

<span data-ttu-id="0bfae-178">"Completado" indica que t</span><span class="sxs-lookup"><span data-stu-id="0bfae-178">"Completed" indicates that t</span></span>

<span data-ttu-id="0bfae-179">Migrar</span><span class="sxs-lookup"><span data-stu-id="0bfae-179">"Migrating"</span></span>

<span data-ttu-id="0bfae-180">"Inmigrando"</span><span class="sxs-lookup"><span data-stu-id="0bfae-180">"Immigrating"</span></span>

<span data-ttu-id="0bfae-181">"Emigrating"</span><span class="sxs-lookup"><span data-stu-id="0bfae-181">"Emigrating"</span></span>

<span data-ttu-id="0bfae-182">"Cerrando"</span><span class="sxs-lookup"><span data-stu-id="0bfae-182">"Shutting Down"</span></span>

<span data-ttu-id="0bfae-183">"In test"</span><span class="sxs-lookup"><span data-stu-id="0bfae-183">"In Test"</span></span>

<span data-ttu-id="0bfae-184">Transición</span><span class="sxs-lookup"><span data-stu-id="0bfae-184">"Transitioning"</span></span>

<span data-ttu-id="0bfae-185">"En servicio"</span><span class="sxs-lookup"><span data-stu-id="0bfae-185">"In Service"</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bfae-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bfae-186"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-187">La implementación es, en general, capaz de devolver esta propiedad, pero no puede hacerlo en este momento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-187">The implementation is in general capable of returning this property, but is unable to do so at this time.</span></span>

</dd> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span data-ttu-id="0bfae-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="0bfae-188"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-189">La implementación (proveedor) es capaz de devolver un valor para esta propiedad, pero no para esta parte concreta de hardware o software, o bien la propiedad no se usa intencionadamente porque no agrega información significativa (como en el caso de una propiedad diseñada para agregar información adicional a otra propiedad).</span><span class="sxs-lookup"><span data-stu-id="0bfae-189">The implementation (provider) is capable of returning a value for this property, but not ever for this particular piece of hardware/software or the property is intentionally not used because it adds no meaningful information (as in the case of a property that is intended to add additional info to another property).</span></span>

</dd> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>

<span data-ttu-id="0bfae-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="0bfae-190"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-191">Describe un elemento que se va a configurar, mantener, limpiar o administrar de otra manera.</span><span class="sxs-lookup"><span data-stu-id="0bfae-191">Describes an element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0bfae-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="0bfae-192"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-193">Describe un elemento que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="0bfae-193">Describes an element being initialized.</span></span>

</dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0bfae-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="0bfae-194"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-195">Describe un elemento que se va a devolver a orden.</span><span class="sxs-lookup"><span data-stu-id="0bfae-195">Describes an element being brought to an orderly stop.</span></span>

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="0bfae-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="0bfae-196"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-197">Se ha producido una detención limpia y ordenada.</span><span class="sxs-lookup"><span data-stu-id="0bfae-197">A clean and orderly stop has occurred.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="0bfae-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="0bfae-198"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-199">Se ha producido una detención abrupta, donde es posible que sea necesario actualizar el estado y la configuración del elemento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-199">An abrupt stop has occurred, where the state and configuration of the element might need to be updated.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="0bfae-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="0bfae-200"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-201">El elemento está inactivo o inactivo.</span><span class="sxs-lookup"><span data-stu-id="0bfae-201">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="0bfae-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="0bfae-202"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-203">El elemento ha completado su operación.</span><span class="sxs-lookup"><span data-stu-id="0bfae-203">The element has completed its operation.</span></span> <span data-ttu-id="0bfae-204">Este valor se debe combinar con correcto, error o degradado en el PrimaryStatus para que un cliente pueda saber si la operación completa se completó con correcto (superado), se completó con error (error) o se completó con degradado (la operación finalizó, pero no se completó correctamente o no ha notificado un error).</span><span class="sxs-lookup"><span data-stu-id="0bfae-204">This value should be combined with either OK, Error, or Degraded in the PrimaryStatus so that a client can tell if the complete operation Completed with OK (passed), Completed with Error (failed), or Completed with Degraded (the operation finished, but it did not complete OK or did not report an error).</span></span>

</dd> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>

<span data-ttu-id="0bfae-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="0bfae-205"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-206">El elemento se mueve entre los elementos host.</span><span class="sxs-lookup"><span data-stu-id="0bfae-206">The element is being moved between host elements.</span></span>

</dd> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>

<span data-ttu-id="0bfae-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="0bfae-207"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-208">El elemento se está moviendo fuera del elemento host.</span><span class="sxs-lookup"><span data-stu-id="0bfae-208">The element is being moved away from host element.</span></span>

</dd> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>

<span data-ttu-id="0bfae-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="0bfae-209"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-210">El elemento se está moviendo al nuevo elemento host.</span><span class="sxs-lookup"><span data-stu-id="0bfae-210">The element is being moved to new host element.</span></span>

</dd> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>

<span data-ttu-id="0bfae-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="0bfae-211"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="0bfae-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="0bfae-212"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-213">Describe un elemento que se va a devolver a una detención abrupta.</span><span class="sxs-lookup"><span data-stu-id="0bfae-213">Describes an element being brought to an abrupt stop.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0bfae-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="0bfae-214"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-215">El elemento está realizando funciones de prueba.</span><span class="sxs-lookup"><span data-stu-id="0bfae-215">The element is performing test functions.</span></span>

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>

<span data-ttu-id="0bfae-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="0bfae-216"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-217">Describe un elemento que está entre Estados, es decir, no está totalmente disponible en su estado anterior o en su siguiente estado.</span><span class="sxs-lookup"><span data-stu-id="0bfae-217">Describes an element that is between states, that is, it is not fully available in either its previous state or its next state.</span></span> <span data-ttu-id="0bfae-218">Este valor debe usarse si no se aplican otros valores que indican una transición a un estado específico.</span><span class="sxs-lookup"><span data-stu-id="0bfae-218">This value should be used if other values indicating a transition to a specific state are not applicable.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="0bfae-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="0bfae-219"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-220">Describe un elemento que está en servicio y operativo.</span><span class="sxs-lookup"><span data-stu-id="0bfae-220">Describes an element that is in service and operational.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0bfae-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0bfae-221"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0bfae-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="0bfae-222"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bfae-223">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0bfae-223">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-224">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bfae-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-226">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("el **\_ ManagedSystemElement de CIM**.**StatusDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="0bfae-226">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**StatusDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-227">Contiene indicadores del estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-227">Contains indicators of the current status of the element.</span></span> <span data-ttu-id="0bfae-228">El primer valor de la propiedad **OperationalStatus** debe contener el estado principal del elemento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-228">The first value of the **OperationalStatus** property should contain the primary status for the element.</span></span>

> [!Note]  
> <span data-ttu-id="0bfae-229">La propiedad **OperationalStatus** reemplaza a la propiedad de **Estado** deprecated.</span><span class="sxs-lookup"><span data-stu-id="0bfae-229">The **OperationalStatus** property replaces the deprecated **Status** property.</span></span> <span data-ttu-id="0bfae-230">Debido al uso generalizado de la propiedad de **Estado** existente en las aplicaciones de administración, recomendamos encarecidamente que los proveedores o la instrumentación proporcionen las propiedades **status** y **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0bfae-230">Due to the widespread use of the existing **Status** property in management applications, we strongly recommend that providers or instrumentation provide both the **Status** and **OperationalStatus** properties.</span></span> <span data-ttu-id="0bfae-231">Cuando se instrumenta, el **Estado**, porque es una propiedad de un solo valor, también debe proporcionar el estado principal del elemento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-231">When instrumented, **Status**, because it is a single-valued property, should also provide the primary status of the element.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bfae-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bfae-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0bfae-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="0bfae-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0bfae-234"><span id="OK"></span><span id="ok"></span>**Aceptar** (2)</span><span class="sxs-lookup"><span data-stu-id="0bfae-234"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0bfae-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (3)</span><span class="sxs-lookup"><span data-stu-id="0bfae-235"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0bfae-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (4)</span><span class="sxs-lookup"><span data-stu-id="0bfae-236"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-237">El elemento está funcionando, pero necesita atención.</span><span class="sxs-lookup"><span data-stu-id="0bfae-237">The element is functioning, but needs attention.</span></span> <span data-ttu-id="0bfae-238">Ejemplos de Estados "acentuados" son sobrecarga, sobrecalentada, etc.</span><span class="sxs-lookup"><span data-stu-id="0bfae-238">Examples of "Stressed" states are overload, overheated, and so on.</span></span>

</dd> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>

<span data-ttu-id="0bfae-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (5)</span><span class="sxs-lookup"><span data-stu-id="0bfae-239"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-240">Un elemento está funcionando de forma nominal pero predice un error en un futuro próximo.</span><span class="sxs-lookup"><span data-stu-id="0bfae-240">An element is functioning nominally but predicting a failure in the near future.</span></span>

</dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0bfae-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span><span class="sxs-lookup"><span data-stu-id="0bfae-241"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="0bfae-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (7)</span><span class="sxs-lookup"><span data-stu-id="0bfae-242"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0bfae-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (8)</span><span class="sxs-lookup"><span data-stu-id="0bfae-243"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0bfae-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (9)</span><span class="sxs-lookup"><span data-stu-id="0bfae-244"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="0bfae-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (10)</span><span class="sxs-lookup"><span data-stu-id="0bfae-245"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (10)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-246">Se ha producido una detención ordenada.</span><span class="sxs-lookup"><span data-stu-id="0bfae-246">An orderly stop has occurred.</span></span>

</dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span data-ttu-id="0bfae-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (11)</span><span class="sxs-lookup"><span data-stu-id="0bfae-247"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-248">Elemento que se va a configurar, mantener, limpiar o administrar de otra manera.</span><span class="sxs-lookup"><span data-stu-id="0bfae-248">An element being configured, maintained, cleaned, or otherwise administered.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0bfae-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (12)</span><span class="sxs-lookup"><span data-stu-id="0bfae-249"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-250">El sistema de supervisión tiene conocimiento de este elemento, pero nunca ha podido establecer comunicaciones con él.</span><span class="sxs-lookup"><span data-stu-id="0bfae-250">The monitoring system has knowledge of this element, but has never been able to establish communications with it.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="0bfae-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (13)</span><span class="sxs-lookup"><span data-stu-id="0bfae-251"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-252">El elemento ManagedSystem se sabe que existe y se ha puesto en contacto correctamente en el pasado, pero actualmente no es accesible.</span><span class="sxs-lookup"><span data-stu-id="0bfae-252">The ManagedSystem Element is known to exist and has been contacted successfully in the past, but is currently unreachable.</span></span>

</dd> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>

<span data-ttu-id="0bfae-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (14)</span><span class="sxs-lookup"><span data-stu-id="0bfae-253"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-254">Se ha producido una detención abrupta, donde es posible que sea necesario actualizar el estado y la configuración del elemento.</span><span class="sxs-lookup"><span data-stu-id="0bfae-254">An abrupt stop, where where the state and configuration of the element might need to be updated, has occurred.</span></span>

</dd> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>

<span data-ttu-id="0bfae-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (15)</span><span class="sxs-lookup"><span data-stu-id="0bfae-255"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-256">El elemento está inactivo o inactivo.</span><span class="sxs-lookup"><span data-stu-id="0bfae-256">The element is inactive or quiesced.</span></span>

</dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span data-ttu-id="0bfae-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (16)</span><span class="sxs-lookup"><span data-stu-id="0bfae-257"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (16)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-258">Este elemento podría ser "OK" pero otro elemento, del que depende, es un error.</span><span class="sxs-lookup"><span data-stu-id="0bfae-258">This element might be "OK" but that another element, on which it is dependent, is in error.</span></span> <span data-ttu-id="0bfae-259">Un ejemplo es un servicio de red o un punto de conexión que no funciona debido a problemas de red de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="0bfae-259">An example is a network service or endpoint that cannot function due to lower-layer networking problems.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="0bfae-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (17)</span><span class="sxs-lookup"><span data-stu-id="0bfae-260"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-261">El elemento ha completado su operación.</span><span class="sxs-lookup"><span data-stu-id="0bfae-261">The element has completed its operation.</span></span>

</dd> <dt>

<span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>

<span data-ttu-id="0bfae-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Modo de energía** (18)</span><span class="sxs-lookup"><span data-stu-id="0bfae-262"><span id="Power_Mode"></span><span id="power_mode"></span><span id="POWER_MODE"></span>**Power Mode** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0bfae-263">El elemento tiene información adicional del modelo de energía incluida en la Asociación PowerManagementService asociada.</span><span class="sxs-lookup"><span data-stu-id="0bfae-263">The element has additional power model information contained in the Associated PowerManagementService association.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0bfae-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0bfae-264"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0bfae-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="0bfae-265"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bfae-266">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="0bfae-266">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0bfae-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-269">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**el \_ ManagedSystemElement de CIM**.**DetailedStatus**","**el \_ ManagedSystemElement de CIM**.**HealthState**")</span><span class="sxs-lookup"><span data-stu-id="0bfae-269">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**DetailedStatus**", "**CIM\_ManagedSystemElement**.**HealthState**")</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-270">Indica un valor de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="0bfae-270">Indicates a high-level status value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0bfae-271">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0bfae-271">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0bfae-272">**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="0bfae-272">**OK** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0bfae-273">**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="0bfae-273">**Degraded** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0bfae-274">**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="0bfae-274">**Error** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0bfae-275">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0bfae-275">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0bfae-276">**Proveedor reservado** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="0bfae-276">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bfae-277">**Estado**</span><span class="sxs-lookup"><span data-stu-id="0bfae-277">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-278">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0bfae-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-279">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-280">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("el **\_ ManagedSystemElement de CIM**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0bfae-280">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-281">Indica el estado principal del objeto.</span><span class="sxs-lookup"><span data-stu-id="0bfae-281">Indicates the primary status of the object.</span></span>

> [!Note]  
> <span data-ttu-id="0bfae-282">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="0bfae-282">This property is deprecated.</span></span> <span data-ttu-id="0bfae-283">Se reemplaza por la propiedad **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0bfae-283">It is replaced by the **OperationalStatus** property.</span></span> <span data-ttu-id="0bfae-284">Si opta por usar la propiedad **status** para mantener la compatibilidad con versiones anteriores, debería ser secundaria para la propiedad **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0bfae-284">If you choose to use the **Status** property for backward compatibility, it should be secondary to the **OperationalStatus** property.</span></span>

 

<dt>



 <span data-ttu-id="0bfae-285">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="0bfae-285">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-286">("Error")</span><span class="sxs-lookup"><span data-stu-id="0bfae-286">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-287">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="0bfae-287">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-288">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="0bfae-288">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-289">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="0bfae-289">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-290">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0bfae-290">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-291">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="0bfae-291">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-292">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="0bfae-292">("Service")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-293">("Acentuado")</span><span class="sxs-lookup"><span data-stu-id="0bfae-293">("Stressed")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-294">("Recover")</span><span class="sxs-lookup"><span data-stu-id="0bfae-294">("NonRecover")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-295">("Sin contacto")</span><span class="sxs-lookup"><span data-stu-id="0bfae-295">("No Contact")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-296">("Pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="0bfae-296">("Lost Comm")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0bfae-297">("Detenido")</span><span class="sxs-lookup"><span data-stu-id="0bfae-297">("Stopped")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0bfae-298">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0bfae-298">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0bfae-299">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="0bfae-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-300">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0bfae-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0bfae-301">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("el **\_ ManagedSystemElement de CIM**.**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="0bfae-301">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ManagedSystemElement**.**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="0bfae-302">Indica las descripciones de los valores correspondientes de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0bfae-302">Indicates descriptions of the corresponding values in the **OperationalStatus** array.</span></span> <span data-ttu-id="0bfae-303">Por ejemplo, si un elemento de la propiedad **OperationalStatus** contiene el valor **deteniéndose**, el elemento situado en el mismo índice de matriz de esta propiedad podría contener una explicación de por qué se detiene un objeto.</span><span class="sxs-lookup"><span data-stu-id="0bfae-303">For example, if an element in the **OperationalStatus** property contains the value **Stopping**, then the element at the same array index in this property might contain an explanation as to why an object is being stopped.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bfae-304">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bfae-304">Requirements</span></span>



| <span data-ttu-id="0bfae-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bfae-305">Requirement</span></span> | <span data-ttu-id="0bfae-306">Value</span><span class="sxs-lookup"><span data-stu-id="0bfae-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bfae-307">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bfae-307">Minimum supported client</span></span><br/> | <span data-ttu-id="0bfae-308">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0bfae-308">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0bfae-309">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0bfae-309">Minimum supported server</span></span><br/> | <span data-ttu-id="0bfae-310">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0bfae-310">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0bfae-311">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0bfae-311">Namespace</span></span><br/>                | <span data-ttu-id="0bfae-312">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0bfae-312">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0bfae-313">MOF</span><span class="sxs-lookup"><span data-stu-id="0bfae-313">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bfae-314"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bfae-314"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bfae-315">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0bfae-315">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bfae-316"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0bfae-316"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0bfae-317">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bfae-317">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bfae-318">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0bfae-318">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

