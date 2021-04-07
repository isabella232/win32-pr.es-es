---
description: Un elemento lógico que representa una unidad de trabajo que se va a ejecutar, como un script o un trabajo de impresión. Un trabajo es distinto de un proceso porque un trabajo se puede programar o poner en cola, y su ejecución no se limita a un solo sistema.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: CIM_Job (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002490"
---
# <a name="cim_job-class-hyper-v-management"></a><span data-ttu-id="bbdea-104">CIM_Job (clase, administración de Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="bbdea-104">CIM_Job class (Hyper-V management)</span></span>

<span data-ttu-id="bbdea-105">Un elemento lógico que representa una unidad de trabajo que se va a ejecutar, como un script o un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="bbdea-105">A logical element that represents a unit of work to execute, such as a script or a print job.</span></span> <span data-ttu-id="bbdea-106">Un trabajo es distinto de un proceso porque un trabajo se puede programar o poner en cola, y su ejecución no se limita a un solo sistema.</span><span class="sxs-lookup"><span data-stu-id="bbdea-106">A job is distinct from a process because a job can be scheduled or queued, and its execution is not limited to a single system.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbdea-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bbdea-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a><span data-ttu-id="bbdea-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bbdea-108">Members</span></span>

<span data-ttu-id="bbdea-109">La clase de **\_ trabajo CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bbdea-109">The **CIM\_Job** class has these types of members:</span></span>

-   [<span data-ttu-id="bbdea-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="bbdea-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bbdea-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbdea-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bbdea-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bbdea-112">Methods</span></span>

<span data-ttu-id="bbdea-113">La clase de **\_ trabajo CIM** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bbdea-113">The **CIM\_Job** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="bbdea-114">Método</span><span class="sxs-lookup"><span data-stu-id="bbdea-114">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="bbdea-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbdea-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="bbdea-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span><span class="sxs-lookup"><span data-stu-id="bbdea-116"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="bbdea-117">Este método es desusado.</span><span class="sxs-lookup"><span data-stu-id="bbdea-117">This method is deprecated.</span></span> <span data-ttu-id="bbdea-118">En su lugar, use el método <strong>RequestStateChange</strong> .</span><span class="sxs-lookup"><span data-stu-id="bbdea-118">Instead, use the <strong>RequestStateChange</strong> method.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bbdea-119">Descripción desusada: cierra un trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-119">Deprecated description: Shuts down a job.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="bbdea-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbdea-120">Properties</span></span>

<span data-ttu-id="bbdea-121">La clase de **\_ trabajo CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bbdea-121">The **CIM\_Job** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bbdea-122">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="bbdea-122">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-123">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bbdea-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-125">**True** para eliminar el trabajo tras su finalización; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="bbdea-125">**True** to delete the job upon completion; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="bbdea-126">Esta propiedad no eliminará los trabajos que se completen antes de que esta propiedad se establezca en **true**.</span><span class="sxs-lookup"><span data-stu-id="bbdea-126">This property will not delete jobs that complete before this property is set to **True**.</span></span>

 

</dd> <dt>

<span data-ttu-id="bbdea-127">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-127">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-128">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-130">La duración de la ejecución del trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-130">The duration for which the job has run.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-131">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="bbdea-131">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-132">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbdea-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-134">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**ErrorDescription**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-135">Código de error específico del proveedor que captura la información de procesamiento de los trabajos periódicos.</span><span class="sxs-lookup"><span data-stu-id="bbdea-135">A vendor-specific error code that captures processing information for recurring jobs.</span></span> <span data-ttu-id="bbdea-136">El valor debe establecerse en cero si el trabajo se completó sin errores.</span><span class="sxs-lookup"><span data-stu-id="bbdea-136">The value must be set to zero if the job completed without error.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-137">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="bbdea-137">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bbdea-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-140">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-140">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-141">Una cadena de forma libre que contiene una descripción del código de error correspondiente en la propiedad **ErrorCode** .</span><span class="sxs-lookup"><span data-stu-id="bbdea-141">A free-form string that contains a description of the corresponding error code in the **ErrorCode** property.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-142">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="bbdea-142">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbdea-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-145">Número de veces que se va a ejecutar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-145">The number of times to run the job.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-146">**Estado del trabajo**</span><span class="sxs-lookup"><span data-stu-id="bbdea-146">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bbdea-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-149">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**el \_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).**OperationalStatus**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-149">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-150">Cadena de forma libre que representa el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-150">A free-form string that represents the status of the job.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-151">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-151">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-152">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbdea-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-154">Indica si las horas de las propiedades **RunStartInterval** y **UntilTime** representan horas locales o horas UTC.</span><span class="sxs-lookup"><span data-stu-id="bbdea-154">Indicates whether the times in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

<span data-ttu-id="bbdea-155">**Hora local** (1)</span><span class="sxs-lookup"><span data-stu-id="bbdea-155">**Local Time** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

<span data-ttu-id="bbdea-156">**Hora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="bbdea-156">**UTC Time** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbdea-157">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="bbdea-157">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bbdea-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-160">El usuario al que se notificará cuando un trabajo se complete o se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="bbdea-160">The user to notify when a job completes or fails.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-161">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="bbdea-161">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bbdea-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-164">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RecoveryAction**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-165">Una cadena que describe la acción de recuperación cuando la propiedad **RecoveryAction** es **otra** ("1").</span><span class="sxs-lookup"><span data-stu-id="bbdea-165">A string that describes the recovery action when the **RecoveryAction** property is **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-166">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="bbdea-166">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bbdea-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-169">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")</span><span class="sxs-lookup"><span data-stu-id="bbdea-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OwningJobElement**](cim-owningjobelement.md).")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-170">El usuario que envió el trabajo, o el nombre de servicio o método que solicitó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-170">The user that submitted the Job, or the service or method name that requested the job.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-171">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="bbdea-171">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-172">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbdea-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-174">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **punitivo** ("Percent")</span><span class="sxs-lookup"><span data-stu-id="bbdea-174">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("percent")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-175">Porcentaje del trabajo que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="bbdea-175">The percentage of the job that is complete.</span></span>

> [!Note]  
> <span data-ttu-id="bbdea-176">El valor "101" no está definido y no se permitirá en la siguiente revisión principal de la especificación.</span><span class="sxs-lookup"><span data-stu-id="bbdea-176">The value "101" is undefined and will be not be allowed in the next major revision of the specification.</span></span>

 

</dd> <dt>

<span data-ttu-id="bbdea-177">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="bbdea-177">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-178">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbdea-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-179">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-180">Importancia del trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-180">The importance of the job.</span></span> <span data-ttu-id="bbdea-181">Cuanto menor sea el número, mayor será la prioridad.</span><span class="sxs-lookup"><span data-stu-id="bbdea-181">The lower the number, the higher the priority.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-182">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="bbdea-182">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-183">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bbdea-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-185">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**OtherRecoveryAction**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**OtherRecoveryAction**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-186">Describe la acción de recuperación que se realizará cuando se produzca un error en un trabajo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="bbdea-186">Describes the recovery action to take when a run job fails.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bbdea-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bbdea-187"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bbdea-188">Se desconoce el modo en que se realiza la acción de recuperación.</span><span class="sxs-lookup"><span data-stu-id="bbdea-188">It is unknown as to what recovery action to take.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bbdea-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bbdea-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bbdea-190">La acción de recuperación se especificará en la propiedad **OtherRecoveryAction** .</span><span class="sxs-lookup"><span data-stu-id="bbdea-190">The recovery action will be specified in the **OtherRecoveryAction** property.</span></span>

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span data-ttu-id="bbdea-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**No continuar** (2)</span><span class="sxs-lookup"><span data-stu-id="bbdea-191"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bbdea-192">Detenga la ejecución del trabajo y actualice su estado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bbdea-192">Stop the execution of the job and appropriately update its status.</span></span>

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span data-ttu-id="bbdea-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar con el trabajo siguiente** (3)</span><span class="sxs-lookup"><span data-stu-id="bbdea-193"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>


</dt> <dd>

<span data-ttu-id="bbdea-194">Continúe con el siguiente trabajo de la cola.</span><span class="sxs-lookup"><span data-stu-id="bbdea-194">Continue with the next job in the queue.</span></span>

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span data-ttu-id="bbdea-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Volver a ejecutar el trabajo** (4)</span><span class="sxs-lookup"><span data-stu-id="bbdea-195"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>


</dt> <dd>

<span data-ttu-id="bbdea-196">Se debe volver a ejecutar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-196">The job should be re-run.</span></span>

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span data-ttu-id="bbdea-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Ejecutar trabajo de recuperación** (5)</span><span class="sxs-lookup"><span data-stu-id="bbdea-197"><span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Run Recovery Job** (5)</span></span>


</dt> <dd>

<span data-ttu-id="bbdea-198">Ejecute el trabajo asociado mediante la relación **RecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="bbdea-198">Run the Job associated using the **RecoveryJob** relationship.</span></span> <span data-ttu-id="bbdea-199">Tenga en cuenta que el trabajo de recuperación debe estar ya en la cola desde la que se ejecutará.</span><span class="sxs-lookup"><span data-stu-id="bbdea-199">Note that the recovery Job must already be in the queue from which it will run.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bbdea-200">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="bbdea-200">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-201">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="bbdea-201">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-202">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-203">Calificadores: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RunMonth**","**\_ trabajo de CIM**.**RunDayOfWeek**","**\_ trabajo de CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-203">Qualifiers: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-204">Entero que se usa junto con la propiedad **RunDayOfWeek** para indicar el día en el que se procesa el trabajo; o bien, si **RunDayOfWeek** se establece en cero, **RunDay** indica el día del mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-204">An integer that is used on conjunction with the **RunDayOfWeek** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span> <span data-ttu-id="bbdea-205">Si **RunDay** es un entero negativo, especifica un día relativo al final del mes, o bien, si **RunDay** es un entero positivo, especifica un día relativo al comienzo del mes.</span><span class="sxs-lookup"><span data-stu-id="bbdea-205">If **RunDay** is a negative integer, it specifies a day relative to the end of the month, or if **RunDay** is a positive integer, it specifies a day relative to the beginning of the month.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-206">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="bbdea-206">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-207">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="bbdea-207">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-208">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-209">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RunMonth**","**\_ trabajo de CIM**.**RunDay**","**\_ trabajo de CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-209">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-210">Entero que se usa junto con la propiedad **RunDay** para indicar el día en el que se procesa el trabajo; o bien, si **RunDayOfWeek** se establece en cero, **RunDay** indica el día del mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-210">An integer that is used on conjunction with the **RunDay** property to indicate the day when the job is processed; or, if **RunDayOfWeek** is set to zero, **RunDay** indicates the day of the month when the job is processed.</span></span>

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

<span data-ttu-id="bbdea-211">**-Sábado** (-7)</span><span class="sxs-lookup"><span data-stu-id="bbdea-211">**-Saturday** (-7)</span></span>


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

<span data-ttu-id="bbdea-212">**-Viernes** (-6)</span><span class="sxs-lookup"><span data-stu-id="bbdea-212">**-Friday** (-6)</span></span>


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

<span data-ttu-id="bbdea-213">**-Jueves** (-5)</span><span class="sxs-lookup"><span data-stu-id="bbdea-213">**-Thursday** (-5)</span></span>


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

<span data-ttu-id="bbdea-214">**-Miércoles** (-4)</span><span class="sxs-lookup"><span data-stu-id="bbdea-214">**-Wednesday** (-4)</span></span>


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

<span data-ttu-id="bbdea-215">**-Martes** (-3)</span><span class="sxs-lookup"><span data-stu-id="bbdea-215">**-Tuesday** (-3)</span></span>


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

<span data-ttu-id="bbdea-216">**-Lunes** (-2)</span><span class="sxs-lookup"><span data-stu-id="bbdea-216">**-Monday** (-2)</span></span>


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

<span data-ttu-id="bbdea-217">**-Sunday** (-1)</span><span class="sxs-lookup"><span data-stu-id="bbdea-217">**-Sunday** (-1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

<span data-ttu-id="bbdea-218">**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="bbdea-218">**ExactDayOfMonth** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="bbdea-219">**Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="bbdea-219">**Sunday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="bbdea-220">**Lunes** (2)</span><span class="sxs-lookup"><span data-stu-id="bbdea-220">**Monday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="bbdea-221">**Martes** (3)</span><span class="sxs-lookup"><span data-stu-id="bbdea-221">**Tuesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="bbdea-222">**Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="bbdea-222">**Wednesday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="bbdea-223">**Jueves** (5)</span><span class="sxs-lookup"><span data-stu-id="bbdea-223">**Thursday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="bbdea-224">**Viernes** (6)</span><span class="sxs-lookup"><span data-stu-id="bbdea-224">**Friday** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="bbdea-225">**Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="bbdea-225">**Saturday** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbdea-226">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="bbdea-226">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-227">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bbdea-227">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-228">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-229">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RunDay**","**\_ trabajo de CIM**.**RunDayOfWeek**","**\_ trabajo de CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-229">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-230">Mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-230">The month when the job is processed.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="bbdea-231">**Enero** (0)</span><span class="sxs-lookup"><span data-stu-id="bbdea-231">**January** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="bbdea-232">**Febrero** (1)</span><span class="sxs-lookup"><span data-stu-id="bbdea-232">**February** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="bbdea-233">**Marzo** (2)</span><span class="sxs-lookup"><span data-stu-id="bbdea-233">**March** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="bbdea-234">**Abril** (3)</span><span class="sxs-lookup"><span data-stu-id="bbdea-234">**April** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="bbdea-235">**Mayo** (4)</span><span class="sxs-lookup"><span data-stu-id="bbdea-235">**May** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="bbdea-236">**Junio** (5)</span><span class="sxs-lookup"><span data-stu-id="bbdea-236">**June** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="bbdea-237">**Julio** (6)</span><span class="sxs-lookup"><span data-stu-id="bbdea-237">**July** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="bbdea-238">**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="bbdea-238">**August** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="bbdea-239">**Septiembre** (8)</span><span class="sxs-lookup"><span data-stu-id="bbdea-239">**September** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="bbdea-240">**Octubre** (9)</span><span class="sxs-lookup"><span data-stu-id="bbdea-240">**October** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="bbdea-241">**Noviembre** (10)</span><span class="sxs-lookup"><span data-stu-id="bbdea-241">**November** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="bbdea-242">**Diciembre** (11)</span><span class="sxs-lookup"><span data-stu-id="bbdea-242">**December** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bbdea-243">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="bbdea-243">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-244">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-244">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-245">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-246">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**RunMonth**","**\_ trabajo de CIM**.**RunDay**","**\_ trabajo de CIM**.**RunDayOfWeek**","**\_ trabajo de CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-246">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-247">El intervalo de tiempo después de medianoche cuando se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-247">The time interval after midnight when the job is be processed.</span></span> <span data-ttu-id="bbdea-248">Por ejemplo, "00000000020000.000000:000" indica que el trabajo se ejecuta en la hora local o después de dos horas, o la hora UTC (UTC se especifica con la propiedad **LocalOrUtcTime** ).</span><span class="sxs-lookup"><span data-stu-id="bbdea-248">For example, "00000000020000.000000:000" indicates that the job is be run on or after two o'clock local time, or UTC time (UTC is specified with the **LocalOrUtcTime** property).</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-249">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-249">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-250">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-251">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-251">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-252">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (**" \_ trabajo de CIM**.**RunMonth**","**\_ trabajo de CIM**.**RunDay**","**\_ trabajo de CIM**.**RunDayOfWeek**","**\_ trabajo de CIM**.**RunStartInterval**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-252">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Job**.**RunMonth**", "**CIM\_Job**.**RunDay**", "**CIM\_Job**.**RunDayOfWeek**", "**CIM\_Job**.**RunStartInterval**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="bbdea-253">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="bbdea-253">This property is deprecated.</span></span> <span data-ttu-id="bbdea-254">En su lugar, se recomienda usar las propiedades **RunMonth**, **RunDay**, **RunDayOfWeek** y **RunStartInterval** .</span><span class="sxs-lookup"><span data-stu-id="bbdea-254">Instead we recommend that you use the **RunMonth**, **RunDay**, **RunDayOfWeek**, and **RunStartInterval** properties.</span></span>

 

<span data-ttu-id="bbdea-255">La hora a la que se programa el inicio del trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="bbdea-255">The time when the current job is scheduled to start.</span></span> <span data-ttu-id="bbdea-256">Esta vez se puede representar mediante una fecha y hora, o un intervalo relativo a la hora a la que se solicita la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bbdea-256">This time can be represented by a date and time, or an interval relative to the time when the property is requested.</span></span> <span data-ttu-id="bbdea-257">Un valor de ceros indica que el trabajo ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="bbdea-257">A value of all zeroes indicates that the job is already executing.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-258">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-258">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-259">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-261">La hora a la que se inició el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-261">The time when the job started.</span></span> <span data-ttu-id="bbdea-262">Esta vez se puede representar mediante una fecha y hora, o por un intervalo relativo a la hora a la que se solicita la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bbdea-262">This time can be represented by a date and time, or by an interval relative to the time when the property is requested.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-263">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="bbdea-263">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-264">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-264">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbdea-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-266">La hora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="bbdea-266">The time when the job was submitted.</span></span> <span data-ttu-id="bbdea-267">Un valor de ceros indica que el elemento primario no es capaz de notificar una fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="bbdea-267">A value of all zeroes indicates that the parent element is not capable of reporting a date and time.</span></span>

</dd> <dt>

<span data-ttu-id="bbdea-268">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-268">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bbdea-269">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bbdea-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-270">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bbdea-270">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bbdea-271">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabajo de CIM**.**LocalOrUtcTime**")</span><span class="sxs-lookup"><span data-stu-id="bbdea-271">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Job**.**LocalOrUtcTime**")</span></span>
</dt> </dl>

<span data-ttu-id="bbdea-272">Hora a partir de la cual el trabajo deja de ser válido o debe detenerse.</span><span class="sxs-lookup"><span data-stu-id="bbdea-272">The time after which the job becomes invalid or should be stopped.</span></span> <span data-ttu-id="bbdea-273">La hora se puede representar mediante una fecha y una hora, o por un intervalo relativo a la hora a la que se solicita esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="bbdea-273">The time can be represented by a date and time, or by an interval relative to the time when this property is requested.</span></span> <span data-ttu-id="bbdea-274">Un valor de los nueves indica que el trabajo puede ejecutarse indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="bbdea-274">A value of all nines indicates that the job can run indefinitely.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bbdea-275">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbdea-275">Requirements</span></span>



| <span data-ttu-id="bbdea-276">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbdea-276">Requirement</span></span> | <span data-ttu-id="bbdea-277">Value</span><span class="sxs-lookup"><span data-stu-id="bbdea-277">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdea-278">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbdea-278">Minimum supported client</span></span><br/> | <span data-ttu-id="bbdea-279">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bbdea-279">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bbdea-280">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbdea-280">Minimum supported server</span></span><br/> | <span data-ttu-id="bbdea-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bbdea-281">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bbdea-282">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bbdea-282">Namespace</span></span><br/>                | <span data-ttu-id="bbdea-283">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bbdea-283">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bbdea-284">MOF</span><span class="sxs-lookup"><span data-stu-id="bbdea-284">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbdea-285"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbdea-285"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bbdea-286">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bbdea-286">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbdea-287"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bbdea-287"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bbdea-288">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbdea-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbdea-289">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="bbdea-289">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

