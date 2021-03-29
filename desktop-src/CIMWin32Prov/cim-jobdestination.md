---
description: La \_ clase CIM JobDestination representa dónde se envía un trabajo para su procesamiento.
ms.assetid: ad2a037d-a5d3-4422-972d-8ef10699bb60
ms.tgt_platform: multiple
title: CIM_JobDestination (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestination
- CIM_JobDestination.Caption
- CIM_JobDestination.Description
- CIM_JobDestination.InstallDate
- CIM_JobDestination.Name
- CIM_JobDestination.Status
- CIM_JobDestination.CreationClassName
- CIM_JobDestination.SystemCreationClassName
- CIM_JobDestination.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d01fbe3b6025795084bf0af4cca3d644fd3cf4a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907286"
---
# <a name="cim_jobdestination-class"></a><span data-ttu-id="8ceba-103">\_Clase JobDestination de CIM</span><span class="sxs-lookup"><span data-stu-id="8ceba-103">CIM\_JobDestination class</span></span>

<span data-ttu-id="8ceba-104">La clase **CIM \_ JobDestination** representa dónde se envía un trabajo para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="8ceba-104">The **CIM\_JobDestination** class represents where a job is submitted for processing.</span></span> <span data-ttu-id="8ceba-105">Puede hacer referencia a una cola que contiene cero o más trabajos, como una cola de impresión que contiene los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="8ceba-105">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="8ceba-106">Los destinos del trabajo se hospedan en sistemas, de forma similar a la manera en que los servicios se hospedan en los sistemas.</span><span class="sxs-lookup"><span data-stu-id="8ceba-106">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ceba-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="8ceba-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8ceba-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8ceba-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8ceba-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8ceba-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8ceba-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8ceba-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ceba-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ceba-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{673E0A2C-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestination : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="8ceba-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ceba-112">Members</span></span>

<span data-ttu-id="8ceba-113">La clase **CIM \_ JobDestination** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8ceba-113">The **CIM\_JobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="8ceba-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ceba-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ceba-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ceba-115">Properties</span></span>

<span data-ttu-id="8ceba-116">La clase **CIM \_ JobDestination** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8ceba-116">The **CIM\_JobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ceba-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8ceba-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ceba-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ceba-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ceba-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8ceba-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8ceba-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8ceba-121">A short textual description of the object.</span></span>

<span data-ttu-id="8ceba-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8ceba-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ceba-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ceba-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ceba-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ceba-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ceba-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-126">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8ceba-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ceba-127">Nombre de la clase o subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="8ceba-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8ceba-128">Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="8ceba-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="8ceba-129">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ceba-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ceba-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ceba-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ceba-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-132">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="8ceba-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8ceba-133">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8ceba-133">A textual description of the object.</span></span>

<span data-ttu-id="8ceba-134">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8ceba-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ceba-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8ceba-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ceba-136">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8ceba-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ceba-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-138">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="8ceba-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8ceba-139">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="8ceba-139">Indicates when the object was installed.</span></span> <span data-ttu-id="8ceba-140">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="8ceba-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8ceba-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8ceba-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ceba-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8ceba-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ceba-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ceba-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ceba-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-145">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8ceba-145">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8ceba-146">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="8ceba-146">Label by which the object is known.</span></span> <span data-ttu-id="8ceba-147">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="8ceba-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8ceba-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8ceba-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ceba-149">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8ceba-149">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ceba-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ceba-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ceba-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-152">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8ceba-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8ceba-153">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="8ceba-153">String that indicates the current status of the object.</span></span> <span data-ttu-id="8ceba-154">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="8ceba-154">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8ceba-155">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="8ceba-155">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8ceba-156">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="8ceba-156">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8ceba-157">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="8ceba-157">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8ceba-158">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="8ceba-158">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8ceba-159">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="8ceba-159">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8ceba-160">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8ceba-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8ceba-161">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8ceba-161">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8ceba-162">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="8ceba-162">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8ceba-163">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="8ceba-163">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8ceba-164">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8ceba-164">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8ceba-165">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="8ceba-165">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8ceba-166">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="8ceba-166">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8ceba-167">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="8ceba-167">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8ceba-168">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="8ceba-168">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8ceba-169">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="8ceba-169">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8ceba-170">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="8ceba-170">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8ceba-171">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8ceba-171">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8ceba-172">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="8ceba-172">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8ceba-173">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="8ceba-173">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8ceba-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ceba-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ceba-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ceba-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ceba-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-177">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="8ceba-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="8ceba-178">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8ceba-178">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="8ceba-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8ceba-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ceba-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ceba-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ceba-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ceba-182">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="8ceba-182">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="8ceba-183">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8ceba-183">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ceba-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ceba-184">Remarks</span></span>

<span data-ttu-id="8ceba-185">La clase **CIM \_ JobDestination** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="8ceba-185">The **CIM\_JobDestination** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="8ceba-186">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="8ceba-186">WMI does not implement this class.</span></span>

<span data-ttu-id="8ceba-187">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8ceba-187">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8ceba-188">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8ceba-188">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ceba-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ceba-189">Requirements</span></span>



| <span data-ttu-id="8ceba-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ceba-190">Requirement</span></span> | <span data-ttu-id="8ceba-191">Value</span><span class="sxs-lookup"><span data-stu-id="8ceba-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ceba-192">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ceba-192">Minimum supported client</span></span><br/> | <span data-ttu-id="8ceba-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ceba-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ceba-194">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ceba-194">Minimum supported server</span></span><br/> | <span data-ttu-id="8ceba-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ceba-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ceba-196">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8ceba-196">Namespace</span></span><br/>                | <span data-ttu-id="8ceba-197">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8ceba-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8ceba-198">MOF</span><span class="sxs-lookup"><span data-stu-id="8ceba-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ceba-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ceba-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ceba-200">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ceba-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ceba-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ceba-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ceba-202">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ceba-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ceba-203">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8ceba-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

