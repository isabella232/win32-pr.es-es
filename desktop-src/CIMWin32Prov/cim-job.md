---
description: La \_ clase de trabajo CIM representa una unidad de trabajo para un sistema, como un trabajo de impresión. Un trabajo es distinto de un proceso porque se puede programar un trabajo.
ms.assetid: a689230e-2a62-4f0d-9961-9bbc055d3c6e
ms.tgt_platform: multiple
title: CIM_Job (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.Caption
- CIM_Job.Description
- CIM_Job.InstallDate
- CIM_Job.Name
- CIM_Job.Status
- CIM_Job.ElapsedTime
- CIM_Job.JobStatus
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.StartTime
- CIM_Job.TimeSubmitted
- CIM_Job.UntilTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd527474309802a4c6d2315d8a9e61b6733e70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153165"
---
# <a name="cim_job-class-cimwin32-wmi-providers"></a><span data-ttu-id="80c36-104">CIM_Job (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="80c36-104">CIM_Job class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="80c36-105">La clase de **\_ trabajo CIM** representa una unidad de trabajo para un sistema, como un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="80c36-105">The **CIM\_Job** class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="80c36-106">Un trabajo es distinto de un proceso porque se puede programar un trabajo.</span><span class="sxs-lookup"><span data-stu-id="80c36-106">A job is distinct from a process because a job can be scheduled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80c36-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="80c36-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="80c36-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="80c36-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="80c36-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="80c36-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="80c36-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="80c36-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c36-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80c36-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C564-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
};
```

## <a name="members"></a><span data-ttu-id="80c36-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="80c36-112">Members</span></span>

<span data-ttu-id="80c36-113">La clase de **\_ trabajo CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="80c36-113">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="80c36-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80c36-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80c36-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80c36-115">Properties</span></span>

<span data-ttu-id="80c36-116">La clase de **\_ trabajo CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="80c36-116">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80c36-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="80c36-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80c36-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80c36-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="80c36-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="80c36-121">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="80c36-121">A short textual description of the object.</span></span>

<span data-ttu-id="80c36-122">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80c36-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80c36-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="80c36-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80c36-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80c36-126">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="80c36-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="80c36-127">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="80c36-127">A textual description of the object.</span></span>

<span data-ttu-id="80c36-128">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80c36-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80c36-129">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="80c36-129">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-130">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80c36-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c36-132">Período de tiempo durante el que se ha estado ejecutando el trabajo.</span><span class="sxs-lookup"><span data-stu-id="80c36-132">Length of time the job has been executing.</span></span>

</dd> <dt>

<span data-ttu-id="80c36-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="80c36-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-134">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80c36-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80c36-136">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="80c36-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="80c36-137">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="80c36-137">Indicates when the object was installed.</span></span> <span data-ttu-id="80c36-138">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="80c36-138">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="80c36-139">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80c36-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80c36-140">**Estado del trabajo**</span><span class="sxs-lookup"><span data-stu-id="80c36-140">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80c36-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c36-143">Cadena de forma libre que representa el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="80c36-143">Free-form string that represents the job status.</span></span>

</dd> <dt>

<span data-ttu-id="80c36-144">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="80c36-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80c36-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80c36-147">Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="80c36-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="80c36-148">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="80c36-148">Label by which the object is known.</span></span> <span data-ttu-id="80c36-149">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="80c36-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="80c36-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80c36-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="80c36-151">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="80c36-151">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80c36-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c36-154">Se notifica al usuario sobre la finalización o el error del trabajo.</span><span class="sxs-lookup"><span data-stu-id="80c36-154">User is notified upon job completion or failure.</span></span>

</dd> <dt>

<span data-ttu-id="80c36-155">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="80c36-155">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80c36-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c36-158">Usuario que envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="80c36-158">User who submitted the job.</span></span>

</dd> <dt>

<span data-ttu-id="80c36-159">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="80c36-159">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80c36-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c36-162">Importancia de la ejecución de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="80c36-162">Importance of a job's execution.</span></span>

</dd> <dt>

<span data-ttu-id="80c36-163">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="80c36-163">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-164">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80c36-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c36-166">Hora a la que comenzó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="80c36-166">Time that the job began.</span></span>

</dd> <dt>

<span data-ttu-id="80c36-167">**Estado**</span><span class="sxs-lookup"><span data-stu-id="80c36-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="80c36-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80c36-170">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="80c36-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="80c36-171">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="80c36-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="80c36-172">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="80c36-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="80c36-173">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="80c36-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="80c36-174">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="80c36-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="80c36-175">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="80c36-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="80c36-176">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="80c36-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="80c36-177">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="80c36-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="80c36-178">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="80c36-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="80c36-179">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="80c36-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="80c36-180">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="80c36-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="80c36-181">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="80c36-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="80c36-182">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="80c36-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="80c36-183">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="80c36-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="80c36-184">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="80c36-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="80c36-185">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="80c36-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="80c36-186">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="80c36-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="80c36-187">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="80c36-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="80c36-188">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="80c36-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="80c36-189">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="80c36-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="80c36-190">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="80c36-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="80c36-191">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="80c36-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="80c36-192">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="80c36-192">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-193">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80c36-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c36-195">Hora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="80c36-195">Time that the job was submitted.</span></span>

</dd> <dt>

<span data-ttu-id="80c36-196">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="80c36-196">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80c36-197">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="80c36-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="80c36-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80c36-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80c36-199">Hora en la que el trabajo no es válido o debe detenerse.</span><span class="sxs-lookup"><span data-stu-id="80c36-199">Time at which the job is invalid or should be stopped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80c36-200">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80c36-200">Remarks</span></span>

<span data-ttu-id="80c36-201">La clase de **\_ trabajo CIM** se deriva de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="80c36-201">The **CIM\_Job** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="80c36-202">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="80c36-202">WMI does not implement this class.</span></span> <span data-ttu-id="80c36-203">Para las clases derivadas del **\_ trabajo CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="80c36-203">For classes derived from **CIM\_Job**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="80c36-204">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="80c36-204">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="80c36-205">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="80c36-205">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="80c36-206">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80c36-206">Requirements</span></span>



| <span data-ttu-id="80c36-207">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c36-207">Requirement</span></span> | <span data-ttu-id="80c36-208">Value</span><span class="sxs-lookup"><span data-stu-id="80c36-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80c36-209">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80c36-209">Minimum supported client</span></span><br/> | <span data-ttu-id="80c36-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80c36-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80c36-211">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80c36-211">Minimum supported server</span></span><br/> | <span data-ttu-id="80c36-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80c36-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80c36-213">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="80c36-213">Namespace</span></span><br/>                | <span data-ttu-id="80c36-214">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="80c36-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="80c36-215">MOF</span><span class="sxs-lookup"><span data-stu-id="80c36-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80c36-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80c36-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="80c36-217">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80c36-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80c36-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80c36-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80c36-219">Vea también</span><span class="sxs-lookup"><span data-stu-id="80c36-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c36-220">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="80c36-220">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

