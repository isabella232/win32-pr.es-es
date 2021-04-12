---
description: La \_ clase CIM ExtraCapacityGroup se deriva de un grupo de redundancia que indica que los elementos agregados tienen más capacidad o capacidad de la necesaria.
ms.assetid: fbbbd6ed-4a67-4917-8b0e-3cba4cac3b45
ms.tgt_platform: multiple
title: CIM_ExtraCapacityGroup (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExtraCapacityGroup
- CIM_ExtraCapacityGroup.Caption
- CIM_ExtraCapacityGroup.Description
- CIM_ExtraCapacityGroup.InstallDate
- CIM_ExtraCapacityGroup.Name
- CIM_ExtraCapacityGroup.Status
- CIM_ExtraCapacityGroup.CreationClassName
- CIM_ExtraCapacityGroup.RedundancyStatus
- CIM_ExtraCapacityGroup.MinNumberNeeded
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78f9aa79cfcc7b93d176859069d1b71f5adf450e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274998"
---
# <a name="cim_extracapacitygroup-class"></a><span data-ttu-id="040c2-103">\_Clase ExtraCapacityGroup de CIM</span><span class="sxs-lookup"><span data-stu-id="040c2-103">CIM\_ExtraCapacityGroup class</span></span>

<span data-ttu-id="040c2-104">La clase **CIM \_ ExtraCapacityGroup** se deriva de un grupo de redundancia que indica que los elementos agregados tienen más capacidad o capacidad de la necesaria.</span><span class="sxs-lookup"><span data-stu-id="040c2-104">The **CIM\_ExtraCapacityGroup** class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="040c2-105">Un ejemplo de este tipo de redundancia es la instalación de fuentes de alimentación N + 1 o ventiladores en un sistema.</span><span class="sxs-lookup"><span data-stu-id="040c2-105">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="040c2-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="040c2-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="040c2-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="040c2-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="040c2-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="040c2-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="040c2-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="040c2-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="040c2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="040c2-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{570ED2E8-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ExtraCapacityGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint32   MinNumberNeeded;
};
```

## <a name="members"></a><span data-ttu-id="040c2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="040c2-111">Members</span></span>

<span data-ttu-id="040c2-112">La clase **CIM \_ ExtraCapacityGroup** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="040c2-112">The **CIM\_ExtraCapacityGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="040c2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="040c2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="040c2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="040c2-114">Properties</span></span>

<span data-ttu-id="040c2-115">La clase **CIM \_ ExtraCapacityGroup** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="040c2-115">The **CIM\_ExtraCapacityGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="040c2-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="040c2-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040c2-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="040c2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="040c2-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="040c2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="040c2-119">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="040c2-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="040c2-120">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="040c2-120">A short textual description of the object.</span></span>

<span data-ttu-id="040c2-121">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="040c2-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="040c2-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="040c2-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040c2-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="040c2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="040c2-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="040c2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="040c2-125">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="040c2-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="040c2-126">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="040c2-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="040c2-127">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="040c2-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="040c2-128">Esta propiedad se hereda de [**\_ RedundancyGroup CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="040c2-128">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="040c2-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="040c2-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040c2-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="040c2-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="040c2-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="040c2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="040c2-132">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="040c2-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="040c2-133">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="040c2-133">A textual description of the object.</span></span>

<span data-ttu-id="040c2-134">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="040c2-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="040c2-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="040c2-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040c2-136">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="040c2-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="040c2-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="040c2-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="040c2-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="040c2-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="040c2-139">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="040c2-139">Indicates when the object was installed.</span></span> <span data-ttu-id="040c2-140">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="040c2-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="040c2-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="040c2-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="040c2-142">**MinNumberNeeded**</span><span class="sxs-lookup"><span data-stu-id="040c2-142">**MinNumberNeeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040c2-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="040c2-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="040c2-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="040c2-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="040c2-145">Menor número de elementos que deben estar operativos para tener redundancia.</span><span class="sxs-lookup"><span data-stu-id="040c2-145">Smallest number of elements that must be operational to have redundancy.</span></span> <span data-ttu-id="040c2-146">Por ejemplo, en una relación de redundancia N + 1, esta propiedad debe establecerse en N.</span><span class="sxs-lookup"><span data-stu-id="040c2-146">For example, in an N+1 redundancy relationship, this property should be set equal to N.</span></span>

</dd> <dt>

<span data-ttu-id="040c2-147">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="040c2-147">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040c2-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="040c2-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="040c2-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="040c2-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="040c2-150">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="040c2-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="040c2-151">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="040c2-151">Label by which the object is known.</span></span> <span data-ttu-id="040c2-152">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="040c2-152">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="040c2-153">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="040c2-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="040c2-154">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="040c2-154">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040c2-155">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="040c2-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="040c2-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="040c2-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="040c2-157">Información sobre el estado del grupo de redundancia.</span><span class="sxs-lookup"><span data-stu-id="040c2-157">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="040c2-158">Esta propiedad se hereda de [**\_ RedundancyGroup CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="040c2-158">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="040c2-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="040c2-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="040c2-160">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="040c2-160">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="040c2-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="040c2-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="040c2-162">Otros.</span><span class="sxs-lookup"><span data-stu-id="040c2-162">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="040c2-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Totalmente redundante** (2)</span><span class="sxs-lookup"><span data-stu-id="040c2-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="040c2-164">Toda la redundancia configurada está disponible.</span><span class="sxs-lookup"><span data-stu-id="040c2-164">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="040c2-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redundancia degradada** (3)</span><span class="sxs-lookup"><span data-stu-id="040c2-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="040c2-166">La cantidad reducida de redundancia está disponible debido a errores.</span><span class="sxs-lookup"><span data-stu-id="040c2-166">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="040c2-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancia perdida** (4)</span><span class="sxs-lookup"><span data-stu-id="040c2-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="040c2-168">La redundancia no está disponible debido a un número suficiente de errores.</span><span class="sxs-lookup"><span data-stu-id="040c2-168">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="040c2-169">El siguiente error producirá un error general.</span><span class="sxs-lookup"><span data-stu-id="040c2-169">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="040c2-170">**Estado**</span><span class="sxs-lookup"><span data-stu-id="040c2-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="040c2-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="040c2-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="040c2-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="040c2-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="040c2-173">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="040c2-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="040c2-174">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="040c2-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="040c2-175">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="040c2-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="040c2-176">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="040c2-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="040c2-177">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="040c2-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="040c2-178">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="040c2-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="040c2-179">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="040c2-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="040c2-180">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="040c2-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="040c2-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="040c2-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="040c2-182">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="040c2-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="040c2-183">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="040c2-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="040c2-184">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="040c2-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="040c2-185">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="040c2-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="040c2-186">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="040c2-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="040c2-187">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="040c2-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="040c2-188">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="040c2-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="040c2-189">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="040c2-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="040c2-190">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="040c2-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="040c2-191">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="040c2-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="040c2-192">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="040c2-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="040c2-193">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="040c2-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="040c2-194">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="040c2-194">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="040c2-195"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="040c2-195"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="040c2-196">Observaciones</span><span class="sxs-lookup"><span data-stu-id="040c2-196">Remarks</span></span>

<span data-ttu-id="040c2-197">La clase **CIM \_ ExtraCapacityGroup** se deriva de [**\_ RedundancyGroup de CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="040c2-197">The **CIM\_ExtraCapacityGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="040c2-198">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="040c2-198">WMI does not implement this class.</span></span>

<span data-ttu-id="040c2-199">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="040c2-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="040c2-200">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="040c2-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="040c2-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="040c2-201">Requirements</span></span>



| <span data-ttu-id="040c2-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="040c2-202">Requirement</span></span> | <span data-ttu-id="040c2-203">Value</span><span class="sxs-lookup"><span data-stu-id="040c2-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="040c2-204">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="040c2-204">Minimum supported client</span></span><br/> | <span data-ttu-id="040c2-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="040c2-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="040c2-206">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="040c2-206">Minimum supported server</span></span><br/> | <span data-ttu-id="040c2-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="040c2-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="040c2-208">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="040c2-208">Namespace</span></span><br/>                | <span data-ttu-id="040c2-209">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="040c2-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="040c2-210">MOF</span><span class="sxs-lookup"><span data-stu-id="040c2-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="040c2-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="040c2-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="040c2-212">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="040c2-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="040c2-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="040c2-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="040c2-214">Vea también</span><span class="sxs-lookup"><span data-stu-id="040c2-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040c2-215">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="040c2-215">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

