---
description: La \_ clase CIM RedundancyGroup representa una colección de elementos del sistema administrados, que indica que los componentes agregados, juntos, proporcionan redundancia.
ms.assetid: b47899cc-eafc-431f-96d4-edb01bf4bcd1
ms.tgt_platform: multiple
title: CIM_RedundancyGroup (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyGroup
- CIM_RedundancyGroup.Caption
- CIM_RedundancyGroup.Description
- CIM_RedundancyGroup.InstallDate
- CIM_RedundancyGroup.Name
- CIM_RedundancyGroup.Status
- CIM_RedundancyGroup.CreationClassName
- CIM_RedundancyGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1394e052b4741dee5b2646c903d83477bfa1ccf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906988"
---
# <a name="cim_redundancygroup-class"></a><span data-ttu-id="eff07-103">\_Clase RedundancyGroup de CIM</span><span class="sxs-lookup"><span data-stu-id="eff07-103">CIM\_RedundancyGroup class</span></span>

<span data-ttu-id="eff07-104">La clase **CIM \_ RedundancyGroup** representa una colección de elementos del sistema administrados, que indica que los componentes agregados, juntos, proporcionan redundancia.</span><span class="sxs-lookup"><span data-stu-id="eff07-104">The **CIM\_RedundancyGroup** class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="eff07-105">Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="eff07-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eff07-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="eff07-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eff07-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eff07-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eff07-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="eff07-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="eff07-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="eff07-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eff07-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eff07-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C3A040A-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
};
```

## <a name="members"></a><span data-ttu-id="eff07-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="eff07-111">Members</span></span>

<span data-ttu-id="eff07-112">La clase **CIM \_ RedundancyGroup** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eff07-112">The **CIM\_RedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="eff07-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eff07-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eff07-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eff07-114">Properties</span></span>

<span data-ttu-id="eff07-115">La clase **CIM \_ RedundancyGroup** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="eff07-115">The **CIM\_RedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eff07-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="eff07-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eff07-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eff07-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eff07-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eff07-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eff07-119">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="eff07-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="eff07-120">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="eff07-120">A short textual description of the object.</span></span>

<span data-ttu-id="eff07-121">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eff07-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eff07-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eff07-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eff07-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eff07-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eff07-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eff07-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eff07-125">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="eff07-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="eff07-126">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="eff07-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="eff07-127">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="eff07-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="eff07-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="eff07-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eff07-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eff07-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eff07-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eff07-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eff07-131">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="eff07-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="eff07-132">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="eff07-132">A textual description of the object.</span></span>

<span data-ttu-id="eff07-133">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eff07-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eff07-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eff07-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eff07-135">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eff07-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eff07-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eff07-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eff07-137">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="eff07-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="eff07-138">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="eff07-138">Indicates when the object was installed.</span></span> <span data-ttu-id="eff07-139">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="eff07-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="eff07-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eff07-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eff07-141">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="eff07-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eff07-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eff07-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eff07-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eff07-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eff07-144">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="eff07-144">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="eff07-145">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="eff07-145">Label by which the object is known.</span></span> <span data-ttu-id="eff07-146">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="eff07-146">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="eff07-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eff07-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eff07-148">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="eff07-148">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eff07-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eff07-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eff07-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eff07-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eff07-151">Información sobre el estado del grupo de redundancia.</span><span class="sxs-lookup"><span data-stu-id="eff07-151">Information about the state of the redundancy group.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eff07-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="eff07-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eff07-153">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="eff07-153">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eff07-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="eff07-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eff07-155">Otros.</span><span class="sxs-lookup"><span data-stu-id="eff07-155">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="eff07-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Totalmente redundante** (2)</span><span class="sxs-lookup"><span data-stu-id="eff07-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eff07-157">Toda la redundancia configurada está disponible.</span><span class="sxs-lookup"><span data-stu-id="eff07-157">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="eff07-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redundancia degradada** (3)</span><span class="sxs-lookup"><span data-stu-id="eff07-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eff07-159">La cantidad reducida de redundancia está disponible debido a errores.</span><span class="sxs-lookup"><span data-stu-id="eff07-159">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="eff07-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancia perdida** (4)</span><span class="sxs-lookup"><span data-stu-id="eff07-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eff07-161">La redundancia no está disponible debido a un número suficiente de errores.</span><span class="sxs-lookup"><span data-stu-id="eff07-161">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="eff07-162">El siguiente error producirá un error general.</span><span class="sxs-lookup"><span data-stu-id="eff07-162">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eff07-163">**Estado**</span><span class="sxs-lookup"><span data-stu-id="eff07-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eff07-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="eff07-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eff07-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="eff07-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eff07-166">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="eff07-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="eff07-167">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="eff07-167">String that indicates the current status of the object.</span></span> <span data-ttu-id="eff07-168">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="eff07-168">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="eff07-169">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="eff07-169">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="eff07-170">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="eff07-170">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="eff07-171">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="eff07-171">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="eff07-172">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="eff07-172">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="eff07-173">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="eff07-173">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="eff07-174">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eff07-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="eff07-175">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="eff07-175">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eff07-176">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="eff07-176">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="eff07-177">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="eff07-177">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eff07-178">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="eff07-178">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eff07-179">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="eff07-179">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="eff07-180">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="eff07-180">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="eff07-181">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="eff07-181">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="eff07-182">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="eff07-182">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="eff07-183">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="eff07-183">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="eff07-184">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="eff07-184">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="eff07-185">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="eff07-185">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="eff07-186">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="eff07-186">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="eff07-187">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="eff07-187">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="eff07-188"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eff07-188"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="eff07-189">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eff07-189">Remarks</span></span>

<span data-ttu-id="eff07-190">La clase **CIM \_ RedundancyGroup** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="eff07-190">The **CIM\_RedundancyGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="eff07-191">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="eff07-191">WMI does not implement this class.</span></span>

<span data-ttu-id="eff07-192">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="eff07-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eff07-193">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="eff07-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eff07-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eff07-194">Requirements</span></span>



| <span data-ttu-id="eff07-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="eff07-195">Requirement</span></span> | <span data-ttu-id="eff07-196">Value</span><span class="sxs-lookup"><span data-stu-id="eff07-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eff07-197">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eff07-197">Minimum supported client</span></span><br/> | <span data-ttu-id="eff07-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eff07-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eff07-199">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eff07-199">Minimum supported server</span></span><br/> | <span data-ttu-id="eff07-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eff07-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eff07-201">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eff07-201">Namespace</span></span><br/>                | <span data-ttu-id="eff07-202">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="eff07-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eff07-203">MOF</span><span class="sxs-lookup"><span data-stu-id="eff07-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eff07-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eff07-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eff07-205">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eff07-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eff07-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eff07-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eff07-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="eff07-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eff07-208">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="eff07-208">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

