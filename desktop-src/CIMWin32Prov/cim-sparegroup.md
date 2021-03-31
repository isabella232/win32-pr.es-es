---
description: La \_ clase CIM SpareGroup se deriva de la \_ clase REDUNDANCYGROUP de CIM e indica que uno o varios de los elementos agregados se pueden retener.
ms.assetid: e60f8cab-a9e8-4f5a-b8d7-833c7832ef7e
ms.tgt_platform: multiple
title: CIM_SpareGroup (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SpareGroup
- CIM_SpareGroup.Caption
- CIM_SpareGroup.Description
- CIM_SpareGroup.InstallDate
- CIM_SpareGroup.Name
- CIM_SpareGroup.Status
- CIM_SpareGroup.CreationClassName
- CIM_SpareGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 17907c62ace9f75c8d807e56d35b91f4c28e5f42
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807022"
---
# <a name="cim_sparegroup-class"></a><span data-ttu-id="57465-103">\_Clase SpareGroup de CIM</span><span class="sxs-lookup"><span data-stu-id="57465-103">CIM\_SpareGroup class</span></span>

<span data-ttu-id="57465-104">La clase **CIM \_ SpareGroup** se deriva de la clase [**\_ RedundancyGroup de CIM**](cim-redundancygroup.md) e indica que uno o varios de los elementos agregados se pueden retener.</span><span class="sxs-lookup"><span data-stu-id="57465-104">The **CIM\_SpareGroup** class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span> <span data-ttu-id="57465-105">Las reservas se definen mediante la [**Asociación \_ ActsAsSpare de CIM**](cim-actsasspare.md) .</span><span class="sxs-lookup"><span data-stu-id="57465-105">Spares are defined using the [**CIM\_ActsAsSpare**](cim-actsasspare.md) association.</span></span> <span data-ttu-id="57465-106">Un ejemplo de una reserva es el uso de NIC redundantes en un sistema informático, donde una NIC es principal y la otra es reserva.</span><span class="sxs-lookup"><span data-stu-id="57465-106">An example of a spare is the use of redundant NICs in a computer system, where one NIC is primary and the other is spare.</span></span> <span data-ttu-id="57465-107">La NIC principal sería miembro del grupo de reserva, asociada mediante la clase [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) , y la otra NIC se asociaría mediante la relación **\_ ActsAsSpare de CIM** .</span><span class="sxs-lookup"><span data-stu-id="57465-107">The primary NIC would be a member of the spare group, associated using the [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class, and the other NIC would be associated using the **CIM\_ActsAsSpare** relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57465-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="57465-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="57465-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="57465-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="57465-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="57465-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="57465-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="57465-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="57465-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57465-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{64B86CA6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SpareGroup : CIM_RedundancyGroup
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

## <a name="members"></a><span data-ttu-id="57465-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="57465-113">Members</span></span>

<span data-ttu-id="57465-114">La clase **CIM \_ SpareGroup** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="57465-114">The **CIM\_SpareGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="57465-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57465-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57465-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57465-116">Properties</span></span>

<span data-ttu-id="57465-117">La clase **CIM \_ SpareGroup** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="57465-117">The **CIM\_SpareGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57465-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="57465-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57465-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="57465-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57465-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57465-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57465-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="57465-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="57465-122">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="57465-122">A short textual description of the object.</span></span>

<span data-ttu-id="57465-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57465-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57465-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="57465-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57465-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="57465-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57465-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57465-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57465-127">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="57465-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="57465-128">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="57465-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="57465-129">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="57465-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="57465-130">Esta propiedad se hereda de [**\_ RedundancyGroup CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="57465-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="57465-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="57465-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57465-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="57465-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57465-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57465-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57465-134">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="57465-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="57465-135">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="57465-135">A textual description of the object.</span></span>

<span data-ttu-id="57465-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57465-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57465-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="57465-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57465-138">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="57465-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="57465-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57465-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57465-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="57465-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="57465-141">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="57465-141">Indicates when the object was installed.</span></span> <span data-ttu-id="57465-142">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="57465-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="57465-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57465-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57465-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="57465-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57465-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="57465-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57465-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57465-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57465-147">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="57465-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="57465-148">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="57465-148">Label by which the object is known.</span></span> <span data-ttu-id="57465-149">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="57465-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="57465-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57465-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="57465-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="57465-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57465-152">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57465-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57465-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57465-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57465-154">Información sobre el estado del grupo de redundancia.</span><span class="sxs-lookup"><span data-stu-id="57465-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="57465-155">Esta propiedad se hereda de [**\_ RedundancyGroup CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="57465-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="57465-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="57465-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="57465-157">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="57465-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="57465-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="57465-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="57465-159">Otros.</span><span class="sxs-lookup"><span data-stu-id="57465-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="57465-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Totalmente redundante** (2)</span><span class="sxs-lookup"><span data-stu-id="57465-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="57465-161">Toda la redundancia configurada está disponible.</span><span class="sxs-lookup"><span data-stu-id="57465-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="57465-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redundancia degradada** (3)</span><span class="sxs-lookup"><span data-stu-id="57465-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="57465-163">La cantidad reducida de redundancia está disponible debido a errores.</span><span class="sxs-lookup"><span data-stu-id="57465-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="57465-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancia perdida** (4)</span><span class="sxs-lookup"><span data-stu-id="57465-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="57465-165">La redundancia no está disponible debido a un número suficiente de errores.</span><span class="sxs-lookup"><span data-stu-id="57465-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="57465-166">El siguiente error producirá un error general.</span><span class="sxs-lookup"><span data-stu-id="57465-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="57465-167">**Estado**</span><span class="sxs-lookup"><span data-stu-id="57465-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57465-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="57465-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57465-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57465-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57465-170">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="57465-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="57465-171">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="57465-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="57465-172">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="57465-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="57465-173">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="57465-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="57465-174">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="57465-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="57465-175">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="57465-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="57465-176">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="57465-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="57465-177">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="57465-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="57465-178">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="57465-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="57465-179">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="57465-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="57465-180">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="57465-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="57465-181">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="57465-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="57465-182">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="57465-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="57465-183">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="57465-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="57465-184">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="57465-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="57465-185">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="57465-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="57465-186">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="57465-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="57465-187">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="57465-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="57465-188">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="57465-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="57465-189">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="57465-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="57465-190">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="57465-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="57465-191">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="57465-191">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="57465-192"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="57465-192"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="57465-193">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57465-193">Remarks</span></span>

<span data-ttu-id="57465-194">La clase **CIM \_ SpareGroup** se deriva de [**\_ RedundancyGroup de CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="57465-194">The **CIM\_SpareGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="57465-195">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="57465-195">WMI does not implement this class.</span></span>

<span data-ttu-id="57465-196">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="57465-196">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="57465-197">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="57465-197">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="57465-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57465-198">Requirements</span></span>



| <span data-ttu-id="57465-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="57465-199">Requirement</span></span> | <span data-ttu-id="57465-200">Value</span><span class="sxs-lookup"><span data-stu-id="57465-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57465-201">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57465-201">Minimum supported client</span></span><br/> | <span data-ttu-id="57465-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57465-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57465-203">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57465-203">Minimum supported server</span></span><br/> | <span data-ttu-id="57465-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57465-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57465-205">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="57465-205">Namespace</span></span><br/>                | <span data-ttu-id="57465-206">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="57465-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57465-207">MOF</span><span class="sxs-lookup"><span data-stu-id="57465-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57465-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57465-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57465-209">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57465-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57465-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57465-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57465-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="57465-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57465-212">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="57465-212">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

