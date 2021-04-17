---
description: La \_ clase CIM StorageRedundancyGroup representa información de redundancia relacionada con el almacenamiento masivo.
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: CIM_StorageRedundancyGroup (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bef8cb8029c62957446ee5d7aefcf67fe5d7acb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659367"
---
# <a name="cim_storageredundancygroup-class"></a><span data-ttu-id="35f9d-103">\_Clase StorageRedundancyGroup de CIM</span><span class="sxs-lookup"><span data-stu-id="35f9d-103">CIM\_StorageRedundancyGroup class</span></span>

<span data-ttu-id="35f9d-104">La clase **CIM \_ StorageRedundancyGroup** representa información de redundancia relacionada con el almacenamiento masivo.</span><span class="sxs-lookup"><span data-stu-id="35f9d-104">The **CIM\_StorageRedundancyGroup** class represents mass storage-related redundancy information.</span></span> <span data-ttu-id="35f9d-105">Los grupos de redundancia de almacenamiento se usan para proteger los datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="35f9d-105">Storage redundancy groups are used to protect user data.</span></span> <span data-ttu-id="35f9d-106">Se componen de una o varias extensiones físicas, o de una o varias extensiones físicas de agregado.</span><span class="sxs-lookup"><span data-stu-id="35f9d-106">They are made up of one or more physical extents, or one or more aggregate physical extents.</span></span> <span data-ttu-id="35f9d-107">Los grupos de redundancia de almacenamiento pueden superponerse; sin embargo, las extensiones subyacentes dentro de la superposición no deben contener ningún dato de comprobación.</span><span class="sxs-lookup"><span data-stu-id="35f9d-107">Storage redundancy groups may overlap; however, the underlying extents within the overlap should not contain any check data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35f9d-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="35f9d-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="35f9d-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="35f9d-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="35f9d-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="35f9d-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="35f9d-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="35f9d-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f9d-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35f9d-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a><span data-ttu-id="35f9d-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="35f9d-113">Members</span></span>

<span data-ttu-id="35f9d-114">La clase **CIM \_ StorageRedundancyGroup** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35f9d-114">The **CIM\_StorageRedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="35f9d-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35f9d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35f9d-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35f9d-116">Properties</span></span>

<span data-ttu-id="35f9d-117">La clase **CIM \_ StorageRedundancyGroup** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35f9d-117">The **CIM\_StorageRedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35f9d-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="35f9d-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f9d-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35f9d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35f9d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="35f9d-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="35f9d-122">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="35f9d-122">A short textual description of the object.</span></span>

<span data-ttu-id="35f9d-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35f9d-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35f9d-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="35f9d-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f9d-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35f9d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35f9d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-127">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="35f9d-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="35f9d-128">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="35f9d-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="35f9d-129">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="35f9d-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="35f9d-130">Esta propiedad se hereda de [**\_ RedundancyGroup CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="35f9d-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="35f9d-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="35f9d-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f9d-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35f9d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35f9d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-134">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="35f9d-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="35f9d-135">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="35f9d-135">A textual description of the object.</span></span>

<span data-ttu-id="35f9d-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35f9d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35f9d-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="35f9d-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f9d-138">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35f9d-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35f9d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-140">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="35f9d-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="35f9d-141">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="35f9d-141">Indicates when the object was installed.</span></span> <span data-ttu-id="35f9d-142">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="35f9d-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="35f9d-143">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35f9d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35f9d-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="35f9d-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f9d-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35f9d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35f9d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-147">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="35f9d-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="35f9d-148">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="35f9d-148">Label by which the object is known.</span></span> <span data-ttu-id="35f9d-149">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="35f9d-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="35f9d-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35f9d-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="35f9d-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="35f9d-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f9d-152">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35f9d-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35f9d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35f9d-154">Información sobre el estado del grupo de redundancia.</span><span class="sxs-lookup"><span data-stu-id="35f9d-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="35f9d-155">Esta propiedad se hereda de [**\_ RedundancyGroup CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="35f9d-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="35f9d-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="35f9d-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="35f9d-157">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="35f9d-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="35f9d-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="35f9d-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="35f9d-159">Otros.</span><span class="sxs-lookup"><span data-stu-id="35f9d-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="35f9d-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Totalmente redundante** (2)</span><span class="sxs-lookup"><span data-stu-id="35f9d-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="35f9d-161">Toda la redundancia configurada está disponible.</span><span class="sxs-lookup"><span data-stu-id="35f9d-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="35f9d-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redundancia degradada** (3)</span><span class="sxs-lookup"><span data-stu-id="35f9d-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="35f9d-163">La cantidad reducida de redundancia está disponible debido a errores.</span><span class="sxs-lookup"><span data-stu-id="35f9d-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="35f9d-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancia perdida** (4)</span><span class="sxs-lookup"><span data-stu-id="35f9d-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="35f9d-165">La redundancia no está disponible debido a un número suficiente de errores.</span><span class="sxs-lookup"><span data-stu-id="35f9d-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="35f9d-166">El siguiente error producirá un error general.</span><span class="sxs-lookup"><span data-stu-id="35f9d-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="35f9d-167">**Estado**</span><span class="sxs-lookup"><span data-stu-id="35f9d-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f9d-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35f9d-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35f9d-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-170">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="35f9d-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="35f9d-171">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="35f9d-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="35f9d-172">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="35f9d-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="35f9d-173">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="35f9d-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="35f9d-174">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="35f9d-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="35f9d-175">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="35f9d-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="35f9d-176">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="35f9d-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="35f9d-177">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="35f9d-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="35f9d-178">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="35f9d-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="35f9d-179">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="35f9d-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="35f9d-180">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="35f9d-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="35f9d-181">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="35f9d-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="35f9d-182">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="35f9d-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="35f9d-183">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="35f9d-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="35f9d-184">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="35f9d-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="35f9d-185">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="35f9d-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="35f9d-186">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="35f9d-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="35f9d-187">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="35f9d-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="35f9d-188">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="35f9d-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="35f9d-189">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="35f9d-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="35f9d-190">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="35f9d-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="35f9d-191">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="35f9d-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35f9d-192">**TypeOfAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="35f9d-192">**TypeOfAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f9d-193">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35f9d-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35f9d-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35f9d-195">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Grupo de redundancia DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="35f9d-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Redundancy Group\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="35f9d-196">Algoritmo usado para la reconstrucción y la redundancia de datos.</span><span class="sxs-lookup"><span data-stu-id="35f9d-196">Algorithm used for data redundancy and reconstruction.</span></span> <span data-ttu-id="35f9d-197">El valor 0 no es válido en el esquema CIM porque representa que no existe redundancia en DMI.</span><span class="sxs-lookup"><span data-stu-id="35f9d-197">The value 0 is not valid in the CIM schema since it represents that no redundancy exists in DMI.</span></span> <span data-ttu-id="35f9d-198">En ese caso, no se debe crear una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="35f9d-198">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="35f9d-199">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="35f9d-199">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="35f9d-200">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="35f9d-200">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="35f9d-201">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="35f9d-201">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="35f9d-202">**Copiar** (3)</span><span class="sxs-lookup"><span data-stu-id="35f9d-202">**Copy** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

<span data-ttu-id="35f9d-203">**XOR** (4)</span><span class="sxs-lookup"><span data-stu-id="35f9d-203">**XOR** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

<span data-ttu-id="35f9d-204">**P + Q** (5)</span><span class="sxs-lookup"><span data-stu-id="35f9d-204">**P+Q** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

<span data-ttu-id="35f9d-205">**S** (6)</span><span class="sxs-lookup"><span data-stu-id="35f9d-205">**S** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

<span data-ttu-id="35f9d-206">**P + S** (7)</span><span class="sxs-lookup"><span data-stu-id="35f9d-206">**P+S** (7)</span></span>


<span data-ttu-id="35f9d-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="35f9d-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="35f9d-208">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35f9d-208">Remarks</span></span>

<span data-ttu-id="35f9d-209">La clase **CIM \_ StorageRedundancyGroup** se deriva de [**\_ RedundancyGroup de CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="35f9d-209">The **CIM\_StorageRedundancyGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="35f9d-210">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="35f9d-210">WMI does not implement this class.</span></span>

<span data-ttu-id="35f9d-211">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="35f9d-211">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="35f9d-212">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="35f9d-212">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="35f9d-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35f9d-213">Requirements</span></span>



| <span data-ttu-id="35f9d-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="35f9d-214">Requirement</span></span> | <span data-ttu-id="35f9d-215">Value</span><span class="sxs-lookup"><span data-stu-id="35f9d-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f9d-216">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35f9d-216">Minimum supported client</span></span><br/> | <span data-ttu-id="35f9d-217">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35f9d-217">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35f9d-218">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35f9d-218">Minimum supported server</span></span><br/> | <span data-ttu-id="35f9d-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35f9d-219">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35f9d-220">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35f9d-220">Namespace</span></span><br/>                | <span data-ttu-id="35f9d-221">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="35f9d-221">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35f9d-222">MOF</span><span class="sxs-lookup"><span data-stu-id="35f9d-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35f9d-223"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35f9d-223"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35f9d-224">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35f9d-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f9d-225"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f9d-225"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f9d-226">Vea también</span><span class="sxs-lookup"><span data-stu-id="35f9d-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f9d-227">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="35f9d-227">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

