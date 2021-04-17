---
description: Representa una unidad de trabajo y se usa para realizar el seguimiento del progreso de las operaciones asincrónicas.
ms.assetid: 33c13880-92a4-4367-8f0b-ecdf38b2ff8e
title: Msvm_ConcreteJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob
- Msvm_ConcreteJob.KillJob
- Msvm_ConcreteJob.InstanceID
- Msvm_ConcreteJob.Caption
- Msvm_ConcreteJob.Description
- Msvm_ConcreteJob.ElementName
- Msvm_ConcreteJob.InstallDate
- Msvm_ConcreteJob.Name
- Msvm_ConcreteJob.OperationalStatus
- Msvm_ConcreteJob.StatusDescriptions
- Msvm_ConcreteJob.Status
- Msvm_ConcreteJob.HealthState
- Msvm_ConcreteJob.CommunicationStatus
- Msvm_ConcreteJob.DetailedStatus
- Msvm_ConcreteJob.OperatingStatus
- Msvm_ConcreteJob.PrimaryStatus
- Msvm_ConcreteJob.JobStatus
- Msvm_ConcreteJob.TimeSubmitted
- Msvm_ConcreteJob.ScheduledStartTime
- Msvm_ConcreteJob.StartTime
- Msvm_ConcreteJob.ElapsedTime
- Msvm_ConcreteJob.JobRunTimes
- Msvm_ConcreteJob.RunMonth
- Msvm_ConcreteJob.RunDay
- Msvm_ConcreteJob.RunDayOfWeek
- Msvm_ConcreteJob.RunStartInterval
- Msvm_ConcreteJob.LocalOrUtcTime
- Msvm_ConcreteJob.UntilTime
- Msvm_ConcreteJob.Notify
- Msvm_ConcreteJob.Owner
- Msvm_ConcreteJob.Priority
- Msvm_ConcreteJob.PercentComplete
- Msvm_ConcreteJob.DeleteOnCompletion
- Msvm_ConcreteJob.ErrorCode
- Msvm_ConcreteJob.ErrorDescription
- Msvm_ConcreteJob.ErrorSummaryDescription
- Msvm_ConcreteJob.RecoveryAction
- Msvm_ConcreteJob.OtherRecoveryAction
- Msvm_ConcreteJob.JobState
- Msvm_ConcreteJob.TimeOfLastStateChange
- Msvm_ConcreteJob.TimeBeforeRemoval
- Msvm_ConcreteJob.Cancellable
- Msvm_ConcreteJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2cff9594bfd39cf365020a1da8ae2f1ec0aea562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667828"
---
# <a name="msvm_concretejob-class"></a><span data-ttu-id="7abc7-103">MSVM \_ ConcreteJob (clase)</span><span class="sxs-lookup"><span data-stu-id="7abc7-103">Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="7abc7-104">Una versión concreta del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-104">A concrete version of job.</span></span> <span data-ttu-id="7abc7-105">Esta clase representa una unidad de trabajo genérica y con capacidad de creación de instancias, como un lote o un trabajo de impresión, y se usa específicamente en Hyper-V para realizar el seguimiento del progreso de las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="7abc7-105">This class represents a generic and instantiatable unit of work, such as a batch or a print job, and is specifically used in Hyper-V to track the progress of asynchronous operations.</span></span>

<span data-ttu-id="7abc7-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7abc7-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abc7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7abc7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
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
  string   ErrorSummaryDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 
                00000000000500.000000:000
              ;
  boolean  Cancellable;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="7abc7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7abc7-108">Members</span></span>

<span data-ttu-id="7abc7-109">La clase **MSVM \_ ConcreteJob** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7abc7-109">The **Msvm\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="7abc7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7abc7-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="7abc7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7abc7-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7abc7-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="7abc7-112">Methods</span></span>

<span data-ttu-id="7abc7-113">La clase **MSVM \_ ConcreteJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7abc7-113">The **Msvm\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="7abc7-114">Método</span><span class="sxs-lookup"><span data-stu-id="7abc7-114">Method</span></span>                                                            | <span data-ttu-id="7abc7-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7abc7-115">Description</span></span>                                                                      |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="7abc7-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="7abc7-116">**GetError**</span></span>](geterror-msvm-concretejob.md)                     | <span data-ttu-id="7abc7-117">Recupera el objeto de error del trabajo, si existe uno.</span><span class="sxs-lookup"><span data-stu-id="7abc7-117">Retrieves the error object for the job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="7abc7-118">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="7abc7-118">**GetErrorEx**</span></span>](geterrorex-msvm-concretejob.md)                 | <span data-ttu-id="7abc7-119">Recupera los objetos de error del trabajo, si existen.</span><span class="sxs-lookup"><span data-stu-id="7abc7-119">Retrieves the error objects for the job, if any exist.</span></span><br/>                |
| <span data-ttu-id="7abc7-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="7abc7-120">**KillJob**</span></span>                                                       | <span data-ttu-id="7abc7-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="7abc7-121">This method is not supported.</span></span><br/>                                         |
| [<span data-ttu-id="7abc7-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="7abc7-122">**RequestStateChange**</span></span>](requeststatechange-msvm-concretejob.md) | <span data-ttu-id="7abc7-123">Solicita que el estado del trabajo se cambie al estado especificado.</span><span class="sxs-lookup"><span data-stu-id="7abc7-123">Requests that the state of the job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7abc7-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7abc7-124">Properties</span></span>

<span data-ttu-id="7abc7-125">La clase **MSVM \_ ConcreteJob** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7abc7-125">The **Msvm\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7abc7-126">**Cancelable**</span><span class="sxs-lookup"><span data-stu-id="7abc7-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-127">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7abc7-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-129">Indica si se puede cancelar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="7abc7-130">El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="7abc7-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7abc7-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-134">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7abc7-134">A short description of the object.</span></span> <span data-ttu-id="7abc7-135">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-136">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="7abc7-136">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-139">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="7abc7-139">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7abc7-140">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="7abc7-140">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7abc7-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-141">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-142">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="7abc7-142">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7abc7-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-145">Especifica si el trabajo debe eliminarse automáticamente al finalizar.</span><span class="sxs-lookup"><span data-stu-id="7abc7-145">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="7abc7-146">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-146">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-147">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7abc7-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-150">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7abc7-150">A description of the object.</span></span> <span data-ttu-id="7abc7-151">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-152">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7abc7-152">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-153">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-155">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="7abc7-155">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7abc7-156">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="7abc7-156">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7abc7-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-158">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-158">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-159">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-161">El intervalo de tiempo en el que se ha estado ejecutando el trabajo o el tiempo total de ejecución si el trabajo ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="7abc7-161">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="7abc7-162">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-162">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-163">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7abc7-163">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-166">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="7abc7-166">A display name for the object.</span></span> <span data-ttu-id="7abc7-167">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-168">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7abc7-168">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-169">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-171">Un código de error específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7abc7-171">A vendor-specific error code.</span></span> <span data-ttu-id="7abc7-172">El valor debe establecerse en cero si el trabajo se completó sin errores.</span><span class="sxs-lookup"><span data-stu-id="7abc7-172">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="7abc7-173">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-173">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-174">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7abc7-174">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-177">Cadena que contiene la descripción del error del proveedor.</span><span class="sxs-lookup"><span data-stu-id="7abc7-177">A string that contains the vendor error description.</span></span> <span data-ttu-id="7abc7-178">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-178">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-179">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="7abc7-179">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-182">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabajo de CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="7abc7-182">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-183">Descripción breve del error, si está presente.</span><span class="sxs-lookup"><span data-stu-id="7abc7-183">A summary description of the error, if present.</span></span> <span data-ttu-id="7abc7-184">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-184">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-185">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7abc7-185">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-186">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-187">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-188">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="7abc7-188">The current health of the element.</span></span> <span data-ttu-id="7abc7-189">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="7abc7-189">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7abc7-190">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="7abc7-190">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="7abc7-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="7abc7-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-192">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7abc7-192">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-193">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-193">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-195">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7abc7-195">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="7abc7-196">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-197">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7abc7-197">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-198">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-200">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="7abc7-200">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-201">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="7abc7-201">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7abc7-202">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="7abc7-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-203">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="7abc7-203">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-204">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7abc7-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-206">El número de veces que se debe ejecutar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-206">The number of times that the job should be run.</span></span> <span data-ttu-id="7abc7-207">Un valor de 1 indica que el trabajo no se repite, mientras que cualquier valor distinto de cero indica un límite del número de veces que se repetirá el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-207">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="7abc7-208">Cero indica que no hay ningún límite en el número de veces que se puede procesar el trabajo, pero se terminará después de que se haya alcanzado el **UntilTime** o cuando el trabajo finalice manualmente.</span><span class="sxs-lookup"><span data-stu-id="7abc7-208">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="7abc7-209">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-209">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-210">**JobState**</span><span class="sxs-lookup"><span data-stu-id="7abc7-210">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-211">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-213">**JobState** es una enumeración de enteros que indica el estado operativo de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-213">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="7abc7-214">También puede indicar transiciones entre estos Estados, por ejemplo, "apagar" e "iniciando".</span><span class="sxs-lookup"><span data-stu-id="7abc7-214">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="7abc7-215">Esta propiedad se hereda de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7abc7-215">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="7abc7-216">Value</span><span class="sxs-lookup"><span data-stu-id="7abc7-216">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="7abc7-217">Significado</span><span class="sxs-lookup"><span data-stu-id="7abc7-217">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="7abc7-218"><dt>**Nuevo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-218"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="7abc7-219">Nunca se ha iniciado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-219">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="7abc7-220"><dt>**Inicio**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-220"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="7abc7-221">El trabajo se mueve de los Estados 2 (nuevo), 5 (suspendido) u 11 (servicio) al estado 4 (en ejecución).</span><span class="sxs-lookup"><span data-stu-id="7abc7-221">The job is moving from the 2 (New), 5 (Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                   |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="7abc7-222"><dt>**Ejecución**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-222"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="7abc7-223">El trabajo se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="7abc7-223">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="7abc7-224"><dt>**Suspendido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-224"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="7abc7-225">El trabajo se ha detenido, pero se puede reiniciar sin problemas.</span><span class="sxs-lookup"><span data-stu-id="7abc7-225">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="7abc7-226"><dt>**Cerrando**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-226"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="7abc7-227">El trabajo se está cambiando a un estado 7 (completado), 8 (finalizado) o 9 (con terminación).</span><span class="sxs-lookup"><span data-stu-id="7abc7-227">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="7abc7-228"><dt>**Completado**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-228"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="7abc7-229">El trabajo se ha completado con normalidad.</span><span class="sxs-lookup"><span data-stu-id="7abc7-229">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="7abc7-230"><dt>**Terminó**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-230"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="7abc7-231">El trabajo se ha detenido mediante una solicitud de cambio de estado "finalizar".</span><span class="sxs-lookup"><span data-stu-id="7abc7-231">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="7abc7-232">El trabajo y todos sus procesos subyacentes finalizan y solo se pueden reiniciar como un nuevo trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-232">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="7abc7-233">El requisito de que el trabajo se reinicie solo como un nuevo trabajo es específico del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-233">The requirement that the job be restarted only as a new job is job-specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="7abc7-234"><dt>**Eliminado**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-234"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="7abc7-235">La solicitud de cambio de estado "Kill" detuvo el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-235">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="7abc7-236">Es posible que los procesos subyacentes sigan en ejecución y que sea necesario realizar una limpieza para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="7abc7-236">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="7abc7-237"><dt>**Excepción**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-237"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="7abc7-238">El trabajo está en un estado anómalo que podría ser indicativo de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="7abc7-238">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="7abc7-239">El estado real del trabajo podría estar disponible a través de objetos específicos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-239">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="7abc7-240"><dt>**Servicio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-240"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="7abc7-241">El trabajo está en un estado específico del proveedor que admite la detección de problemas, la resolución o ambos.</span><span class="sxs-lookup"><span data-stu-id="7abc7-241">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="7abc7-242"><dt>**DMTF reservado**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-242"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="7abc7-243">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7abc7-243">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="7abc7-244"><dt>**Proveedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-244"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="7abc7-245">Reservado.</span><span class="sxs-lookup"><span data-stu-id="7abc7-245">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="7abc7-246">**Estado del trabajo**</span><span class="sxs-lookup"><span data-stu-id="7abc7-246">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-247">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-249">Cadena que representa el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-249">A string that represents the job status.</span></span> <span data-ttu-id="7abc7-250">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-250">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-251">**JobType**</span><span class="sxs-lookup"><span data-stu-id="7abc7-251">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-252">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-254">Indica el tipo de trabajo del que este objeto realiza el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7abc7-254">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7abc7-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7abc7-255"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Definir máquina virtual** (1)</span><span class="sxs-lookup"><span data-stu-id="7abc7-256"><span id="Define_Virtual_Machine"></span><span id="define_virtual_machine"></span><span id="DEFINE_VIRTUAL_MACHINE"></span>**Define Virtual Machine** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modificar máquina virtual** (2)</span><span class="sxs-lookup"><span data-stu-id="7abc7-257"><span id="Modify_Virtual_Machine"></span><span id="modify_virtual_machine"></span><span id="MODIFY_VIRTUAL_MACHINE"></span>**Modify Virtual Machine** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destruir máquina virtual** (3)</span><span class="sxs-lookup"><span data-stu-id="7abc7-258"><span id="Destroy_Virtual_Machine"></span><span id="destroy_virtual_machine"></span><span id="DESTROY_VIRTUAL_MACHINE"></span>**Destroy Virtual Machine** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>

<span data-ttu-id="7abc7-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modificar la configuración del servicio de administración** (4)</span><span class="sxs-lookup"><span data-stu-id="7abc7-259"><span id="Modify_Management_Service_Settings"></span><span id="modify_management_service_settings"></span><span id="MODIFY_MANAGEMENT_SERVICE_SETTINGS"></span>**Modify Management Service Settings** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Inicializar máquina virtual** (10)</span><span class="sxs-lookup"><span data-stu-id="7abc7-260"><span id="Initialize_Virtual_Machine"></span><span id="initialize_virtual_machine"></span><span id="INITIALIZE_VIRTUAL_MACHINE"></span>**Initialize Virtual Machine** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Esperando para iniciar la máquina virtual** (11)</span><span class="sxs-lookup"><span data-stu-id="7abc7-261"><span id="Waiting_to_Start_Virtual_Machine"></span><span id="waiting_to_start_virtual_machine"></span><span id="WAITING_TO_START_VIRTUAL_MACHINE"></span>**Waiting to Start Virtual Machine** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Iniciar máquina virtual** (12)</span><span class="sxs-lookup"><span data-stu-id="7abc7-262"><span id="Start_Virtual_Machine"></span><span id="start_virtual_machine"></span><span id="START_VIRTUAL_MACHINE"></span>**Start Virtual Machine** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Apagar la máquina virtual** (13)</span><span class="sxs-lookup"><span data-stu-id="7abc7-263"><span id="Power_Off_Virtual_Machine"></span><span id="power_off_virtual_machine"></span><span id="POWER_OFF_VIRTUAL_MACHINE"></span>**Power Off Virtual Machine** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Guardar la máquina virtual** (14)</span><span class="sxs-lookup"><span data-stu-id="7abc7-264"><span id="Save_Virtual_Machine"></span><span id="save_virtual_machine"></span><span id="SAVE_VIRTUAL_MACHINE"></span>**Save Virtual Machine** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restaurar la máquina virtual** (15)</span><span class="sxs-lookup"><span data-stu-id="7abc7-265"><span id="Restore_Virtual_Machine"></span><span id="restore_virtual_machine"></span><span id="RESTORE_VIRTUAL_MACHINE"></span>**Restore Virtual Machine** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Apagar la máquina virtual** (16)</span><span class="sxs-lookup"><span data-stu-id="7abc7-266"><span id="Shut_Down_Virtual_Machine"></span><span id="shut_down_virtual_machine"></span><span id="SHUT_DOWN_VIRTUAL_MACHINE"></span>**Shut Down Virtual Machine** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pausar máquina virtual** (26)</span><span class="sxs-lookup"><span data-stu-id="7abc7-267"><span id="Pause_Virtual_Machine"></span><span id="pause_virtual_machine"></span><span id="PAUSE_VIRTUAL_MACHINE"></span>**Pause Virtual Machine** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Reanudar máquina virtual** (27)</span><span class="sxs-lookup"><span data-stu-id="7abc7-268"><span id="Resume_Virtual_Machine"></span><span id="resume_virtual_machine"></span><span id="RESUME_VIRTUAL_MACHINE"></span>**Resume Virtual Machine** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Restablecer máquina virtual** (28)</span><span class="sxs-lookup"><span data-stu-id="7abc7-269"><span id="Reset_Virtual_Machine"></span><span id="reset_virtual_machine"></span><span id="RESET_VIRTUAL_MACHINE"></span>**Reset Virtual Machine** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reiniciar la máquina virtual** (29)</span><span class="sxs-lookup"><span data-stu-id="7abc7-270"><span id="Reboot_Virtual_Machine"></span><span id="reboot_virtual_machine"></span><span id="REBOOT_VIRTUAL_MACHINE"></span>**Reboot Virtual Machine** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="7abc7-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Agregar recursos de máquina virtual** (30)</span><span class="sxs-lookup"><span data-stu-id="7abc7-271"><span id="Add_Virtual_Machine_Resources"></span><span id="add_virtual_machine_resources"></span><span id="ADD_VIRTUAL_MACHINE_RESOURCES"></span>**Add Virtual Machine Resources** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="7abc7-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modificar recursos de máquina virtual** (31)</span><span class="sxs-lookup"><span data-stu-id="7abc7-272"><span id="Modify_Virtual_Machine_Resources"></span><span id="modify_virtual_machine_resources"></span><span id="MODIFY_VIRTUAL_MACHINE_RESOURCES"></span>**Modify Virtual Machine Resources** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>

<span data-ttu-id="7abc7-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Quitar recursos de máquina virtual** (32)</span><span class="sxs-lookup"><span data-stu-id="7abc7-273"><span id="Remove_Virtual_Machine_Resources"></span><span id="remove_virtual_machine_resources"></span><span id="REMOVE_VIRTUAL_MACHINE_RESOURCES"></span>**Remove Virtual Machine Resources** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>

<span data-ttu-id="7abc7-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Solicitar la memoria de la máquina virtual inicial** (40)</span><span class="sxs-lookup"><span data-stu-id="7abc7-274"><span id="Request_Initial_Virtual_Machine_Memory"></span><span id="request_initial_virtual_machine_memory"></span><span id="REQUEST_INITIAL_VIRTUAL_MACHINE_MEMORY"></span>**Request Initial Virtual Machine Memory** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Agregar memoria a la máquina virtual** (41)</span><span class="sxs-lookup"><span data-stu-id="7abc7-275"><span id="Add_Memory_to_Virtual_Machine"></span><span id="add_memory_to_virtual_machine"></span><span id="ADD_MEMORY_TO_VIRTUAL_MACHINE"></span>**Add Memory to Virtual Machine** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Quitar memoria de la máquina virtual** (42)</span><span class="sxs-lookup"><span data-stu-id="7abc7-276"><span id="Remove_Memory_from_Virtual_Machine"></span><span id="remove_memory_from_virtual_machine"></span><span id="REMOVE_MEMORY_FROM_VIRTUAL_MACHINE"></span>**Remove Memory from Virtual Machine** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>

<span data-ttu-id="7abc7-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Combinación de discos VHD** (50)</span><span class="sxs-lookup"><span data-stu-id="7abc7-277"><span id="Merging_VHD_Disks"></span><span id="merging_vhd_disks"></span><span id="MERGING_VHD_DISKS"></span>**Merging VHD Disks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Crear una instantánea de VSS dentro de la máquina virtual** (51)</span><span class="sxs-lookup"><span data-stu-id="7abc7-278"><span id="Create_VSS_Snapshot_inside_Virtual_Machine"></span><span id="create_vss_snapshot_inside_virtual_machine"></span><span id="CREATE_VSS_SNAPSHOT_INSIDE_VIRTUAL_MACHINE"></span>**Create VSS Snapshot inside Virtual Machine** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>

<span data-ttu-id="7abc7-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Obtener datos de configuración de importación** (60)</span><span class="sxs-lookup"><span data-stu-id="7abc7-279"><span id="Get_Import_Setting_Data"></span><span id="get_import_setting_data"></span><span id="GET_IMPORT_SETTING_DATA"></span>**Get Import Setting Data** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Importar máquina virtual** (61)</span><span class="sxs-lookup"><span data-stu-id="7abc7-280"><span id="Import_Virtual_Machine"></span><span id="import_virtual_machine"></span><span id="IMPORT_VIRTUAL_MACHINE"></span>**Import Virtual Machine** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Exportar máquina virtual** (62)</span><span class="sxs-lookup"><span data-stu-id="7abc7-281"><span id="Export_Virtual_Machine"></span><span id="export_virtual_machine"></span><span id="EXPORT_VIRTUAL_MACHINE"></span>**Export Virtual Machine** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>

<span data-ttu-id="7abc7-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Configuración de registro** (63)</span><span class="sxs-lookup"><span data-stu-id="7abc7-282"><span id="Register_Configuration"></span><span id="register_configuration"></span><span id="REGISTER_CONFIGURATION"></span>**Register Configuration** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>

<span data-ttu-id="7abc7-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Anular el registro** de la configuración (64)</span><span class="sxs-lookup"><span data-stu-id="7abc7-283"><span id="Unregister_Configuration"></span><span id="unregister_configuration"></span><span id="UNREGISTER_CONFIGURATION"></span>**Unregister Configuration** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Máquina virtual de instantáneas** (70)</span><span class="sxs-lookup"><span data-stu-id="7abc7-284"><span id="Snapshot_Virtual_Machine"></span><span id="snapshot_virtual_machine"></span><span id="SNAPSHOT_VIRTUAL_MACHINE"></span>**Snapshot Virtual Machine** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="7abc7-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Aplicar instantánea de máquina virtual** (71)</span><span class="sxs-lookup"><span data-stu-id="7abc7-285"><span id="Apply_Virtual_Machine_Snapshot"></span><span id="apply_virtual_machine_snapshot"></span><span id="APPLY_VIRTUAL_MACHINE_SNAPSHOT"></span>**Apply Virtual Machine Snapshot** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>

<span data-ttu-id="7abc7-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Eliminar instantánea de máquina virtual** (72)</span><span class="sxs-lookup"><span data-stu-id="7abc7-286"><span id="Delete_Virtual_Machine_Snapshot"></span><span id="delete_virtual_machine_snapshot"></span><span id="DELETE_VIRTUAL_MACHINE_SNAPSHOT"></span>**Delete Virtual Machine Snapshot** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>

<span data-ttu-id="7abc7-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Borrar estado de instantánea de máquina virtual** (73)</span><span class="sxs-lookup"><span data-stu-id="7abc7-287"><span id="Clear_Virtual_Machine_Snapshot_State"></span><span id="clear_virtual_machine_snapshot_state"></span><span id="CLEAR_VIRTUAL_MACHINE_SNAPSHOT_STATE"></span>**Clear Virtual Machine Snapshot State** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>

<span data-ttu-id="7abc7-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Agregar recursos al grupo de recursos** (80)</span><span class="sxs-lookup"><span data-stu-id="7abc7-288"><span id="Add_Resources_to_Resource_Pool"></span><span id="add_resources_to_resource_pool"></span><span id="ADD_RESOURCES_TO_RESOURCE_POOL"></span>**Add Resources to Resource Pool** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>

<span data-ttu-id="7abc7-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Quitar recursos del grupo de recursos** (81)</span><span class="sxs-lookup"><span data-stu-id="7abc7-289"><span id="Remove_Resources_from_Resource_Pool"></span><span id="remove_resources_from_resource_pool"></span><span id="REMOVE_RESOURCES_FROM_RESOURCE_POOL"></span>**Remove Resources from Resource Pool** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>

<span data-ttu-id="7abc7-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modificar la configuración del servidor de replicación** (90)</span><span class="sxs-lookup"><span data-stu-id="7abc7-290"><span id="Modify_Replication_Server_Settings"></span><span id="modify_replication_server_settings"></span><span id="MODIFY_REPLICATION_SERVER_SETTINGS"></span>**Modify Replication Server Settings** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="7abc7-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Crear relación de replicación** (91)</span><span class="sxs-lookup"><span data-stu-id="7abc7-291"><span id="Create_Replication_Relationship"></span><span id="create_replication_relationship"></span><span id="CREATE_REPLICATION_RELATIONSHIP"></span>**Create Replication Relationship** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>

<span data-ttu-id="7abc7-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modificar la configuración** de la relación de replicación (92)</span><span class="sxs-lookup"><span data-stu-id="7abc7-292"><span id="Modify_Replication_Relationship_Settings"></span><span id="modify_replication_relationship_settings"></span><span id="MODIFY_REPLICATION_RELATIONSHIP_SETTINGS"></span>**Modify Replication Relationship Settings** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>

<span data-ttu-id="7abc7-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Quitar relación de replicación** (93)</span><span class="sxs-lookup"><span data-stu-id="7abc7-293"><span id="Remove_Replication_Relationship"></span><span id="remove_replication_relationship"></span><span id="REMOVE_REPLICATION_RELATIONSHIP"></span>**Remove Replication Relationship** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>

<span data-ttu-id="7abc7-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Iniciar la replicación inicial en banda** (94)</span><span class="sxs-lookup"><span data-stu-id="7abc7-294"><span id="Start_Inband_Initial_Replication"></span><span id="start_inband_initial_replication"></span><span id="START_INBAND_INITIAL_REPLICATION"></span>**Start Inband Initial Replication** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>

<span data-ttu-id="7abc7-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Replicación de importación** (95)</span><span class="sxs-lookup"><span data-stu-id="7abc7-295"><span id="Import_Replication"></span><span id="import_replication"></span><span id="IMPORT_REPLICATION"></span>**Import Replication** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>

<span data-ttu-id="7abc7-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Cambio de estado de replicación** (96)</span><span class="sxs-lookup"><span data-stu-id="7abc7-296"><span id="Replicate_State_Change"></span><span id="replicate_state_change"></span><span id="REPLICATE_STATE_CHANGE"></span>**Replicate State Change** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>

<span data-ttu-id="7abc7-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Iniciar conmutación por error** (97)</span><span class="sxs-lookup"><span data-stu-id="7abc7-297"><span id="Initiate_Failover"></span><span id="initiate_failover"></span><span id="INITIATE_FAILOVER"></span>**Initiate Failover** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>

<span data-ttu-id="7abc7-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Reversión de conmutación por error** (98)</span><span class="sxs-lookup"><span data-stu-id="7abc7-298"><span id="Revert_Failover"></span><span id="revert_failover"></span><span id="REVERT_FAILOVER"></span>**Revert Failover** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>

<span data-ttu-id="7abc7-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Confirmación de la conmutación por error** (99)</span><span class="sxs-lookup"><span data-stu-id="7abc7-299"><span id="Commit_Failover"></span><span id="commit_failover"></span><span id="COMMIT_FAILOVER"></span>**Commit Failover** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>

<span data-ttu-id="7abc7-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Replicación sincronizada de Inititate** (100)</span><span class="sxs-lookup"><span data-stu-id="7abc7-300"><span id="Inititate_Synced_Replication"></span><span id="inititate_synced_replication"></span><span id="INITITATE_SYNCED_REPLICATION"></span>**Inititate Synced Replication** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>

<span data-ttu-id="7abc7-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancelar replicación sincronizada** (101)</span><span class="sxs-lookup"><span data-stu-id="7abc7-301"><span id="Cancel_Synced_Replication"></span><span id="cancel_synced_replication"></span><span id="CANCEL_SYNCED_REPLICATION"></span>**Cancel Synced Replication** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>

<span data-ttu-id="7abc7-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Iniciar réplica de prueba** (102)</span><span class="sxs-lookup"><span data-stu-id="7abc7-302"><span id="Initiate_Test_Replica"></span><span id="initiate_test_replica"></span><span id="INITIATE_TEST_REPLICA"></span>**Initiate Test Replica** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>

<span data-ttu-id="7abc7-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Quitar réplica de prueba** (103)</span><span class="sxs-lookup"><span data-stu-id="7abc7-303"><span id="Remove_Test_Replica"></span><span id="remove_test_replica"></span><span id="REMOVE_TEST_REPLICA"></span>**Remove Test Replica** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>

<span data-ttu-id="7abc7-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Replicación inversa** (104)</span><span class="sxs-lookup"><span data-stu-id="7abc7-304"><span id="Reverse_Replication"></span><span id="reverse_replication"></span><span id="REVERSE_REPLICATION"></span>**Reverse Replication** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>

<span data-ttu-id="7abc7-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Diferencia de envío de replicación** (105)</span><span class="sxs-lookup"><span data-stu-id="7abc7-305"><span id="Replication_Sending_Delta"></span><span id="replication_sending_delta"></span><span id="REPLICATION_SENDING_DELTA"></span>**Replication Sending Delta** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>

<span data-ttu-id="7abc7-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Delta de recepción de replicación** (106)</span><span class="sxs-lookup"><span data-stu-id="7abc7-306"><span id="Replication_Receiving_Delta"></span><span id="replication_receiving_delta"></span><span id="REPLICATION_RECEIVING_DELTA"></span>**Replication Receiving Delta** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="7abc7-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>Volver a **sincronizar** (107)</span><span class="sxs-lookup"><span data-stu-id="7abc7-307"><span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resynchronizing** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>

<span data-ttu-id="7abc7-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Aplicar registro de cambios** (108)</span><span class="sxs-lookup"><span data-stu-id="7abc7-308"><span id="Apply_change_log"></span><span id="apply_change_log"></span><span id="APPLY_CHANGE_LOG"></span>**Apply change log** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>

<span data-ttu-id="7abc7-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Detener la replicación inicial** (109)</span><span class="sxs-lookup"><span data-stu-id="7abc7-309"><span id="Stop_Initial_Replication"></span><span id="stop_initial_replication"></span><span id="STOP_INITIAL_REPLICATION"></span>**Stop Initial Replication** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>

<span data-ttu-id="7abc7-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Detener la resincronización** (110)</span><span class="sxs-lookup"><span data-stu-id="7abc7-310"><span id="Stop_Resynchronizing"></span><span id="stop_resynchronizing"></span><span id="STOP_RESYNCHRONIZING"></span>**Stop Resynchronizing** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>

<span data-ttu-id="7abc7-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Obtener estadísticas de réplica** (111)</span><span class="sxs-lookup"><span data-stu-id="7abc7-311"><span id="Get_Replica_statistics"></span><span id="get_replica_statistics"></span><span id="GET_REPLICA_STATISTICS"></span>**Get Replica statistics** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="7abc7-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Preparar el comprobador de coherencia** (112)</span><span class="sxs-lookup"><span data-stu-id="7abc7-312"><span id="Prepare_for_Consistency_Checker"></span><span id="prepare_for_consistency_checker"></span><span id="PREPARE_FOR_CONSISTENCY_CHECKER"></span>**Prepare for Consistency Checker** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>

<span data-ttu-id="7abc7-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Comprobador de coherencia** (113)</span><span class="sxs-lookup"><span data-stu-id="7abc7-313"><span id="Consistency_Checker"></span><span id="consistency_checker"></span><span id="CONSISTENCY_CHECKER"></span>**Consistency Checker** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>

<span data-ttu-id="7abc7-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Detener el comprobador de coherencia** (114)</span><span class="sxs-lookup"><span data-stu-id="7abc7-314"><span id="Stop_Consistency_Checker"></span><span id="stop_consistency_checker"></span><span id="STOP_CONSISTENCY_CHECKER"></span>**Stop Consistency Checker** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>

<span data-ttu-id="7abc7-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Prueba** de la conexión de replicación (115)</span><span class="sxs-lookup"><span data-stu-id="7abc7-315"><span id="Test_Replication_Connection"></span><span id="test_replication_connection"></span><span id="TEST_REPLICATION_CONNECTION"></span>**Test Replication Connection** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>

<span data-ttu-id="7abc7-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Enviando réplica inicial** (116)</span><span class="sxs-lookup"><span data-stu-id="7abc7-316"><span id="Sending_Initial_Replica"></span><span id="sending_initial_replica"></span><span id="SENDING_INITIAL_REPLICA"></span>**Sending Initial Replica** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>

<span data-ttu-id="7abc7-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Iniciar la replicación inicial de resincronización** (117)</span><span class="sxs-lookup"><span data-stu-id="7abc7-317"><span id="Start_Resync_Initial_Replication"></span><span id="start_resync_initial_replication"></span><span id="START_RESYNC_INITIAL_REPLICATION"></span>**Start Resync Initial Replication** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>

<span data-ttu-id="7abc7-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Iniciar exportar replicación inicial** (118)</span><span class="sxs-lookup"><span data-stu-id="7abc7-318"><span id="Start_Export_Initial_Replication"></span><span id="start_export_initial_replication"></span><span id="START_EXPORT_INITIAL_REPLICATION"></span>**Start Export Initial Replication** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>

<span data-ttu-id="7abc7-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Restablecer estadísticas de réplica** (119)</span><span class="sxs-lookup"><span data-stu-id="7abc7-319"><span id="Reset_Replica_Statistics"></span><span id="reset_replica_statistics"></span><span id="RESET_REPLICA_STATISTICS"></span>**Reset Replica Statistics** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>

<span data-ttu-id="7abc7-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Aplicar diferencias registradas** (120)</span><span class="sxs-lookup"><span data-stu-id="7abc7-320"><span id="Apply_Registered_Deltas"></span><span id="apply_registered_deltas"></span><span id="APPLY_REGISTERED_DELTAS"></span>**Apply Registered Deltas** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>

<span data-ttu-id="7abc7-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>Volver a **sincronizar la replicación extendida** (121)</span><span class="sxs-lookup"><span data-stu-id="7abc7-321"><span id="Resynchronizing_Extended_Replication"></span><span id="resynchronizing_extended_replication"></span><span id="RESYNCHRONIZING_EXTENDED_REPLICATION"></span>**Resynchronizing Extended Replication** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>

<span data-ttu-id="7abc7-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Leyendo configuración de réplica de prueba** (122)</span><span class="sxs-lookup"><span data-stu-id="7abc7-322"><span id="Reading_Test_Replica_Configuration"></span><span id="reading_test_replica_configuration"></span><span id="READING_TEST_REPLICA_CONFIGURATION"></span>**Reading Test Replica Configuration** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>

<span data-ttu-id="7abc7-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Cambiar el modo de replicación a principal** (123)</span><span class="sxs-lookup"><span data-stu-id="7abc7-323"><span id="Change_the_replication_mode_to_primary"></span><span id="change_the_replication_mode_to_primary"></span><span id="CHANGE_THE_REPLICATION_MODE_TO_PRIMARY"></span>**Change the replication mode to primary** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>

<span data-ttu-id="7abc7-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Iniciar conmutación por recuperación** (124)</span><span class="sxs-lookup"><span data-stu-id="7abc7-324"><span id="Initiate_Failback"></span><span id="initiate_failback"></span><span id="INITIATE_FAILBACK"></span>**Initiate Failback** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>

<span data-ttu-id="7abc7-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Actualizar conjunto de discos** (125)</span><span class="sxs-lookup"><span data-stu-id="7abc7-325"><span id="Update_Disk_Set"></span><span id="update_disk_set"></span><span id="UPDATE_DISK_SET"></span>**Update Disk Set** (125)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-326">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-326">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>

<span data-ttu-id="7abc7-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Definir el conmutador Ethernet** (130)</span><span class="sxs-lookup"><span data-stu-id="7abc7-327"><span id="Define_Ethernet_Switch"></span><span id="define_ethernet_switch"></span><span id="DEFINE_ETHERNET_SWITCH"></span>**Define Ethernet Switch** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>

<span data-ttu-id="7abc7-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modificar la configuración del conmutador Ethernet** (131)</span><span class="sxs-lookup"><span data-stu-id="7abc7-328"><span id="Modify_Ethernet_Switch_Settings"></span><span id="modify_ethernet_switch_settings"></span><span id="MODIFY_ETHERNET_SWITCH_SETTINGS"></span>**Modify Ethernet Switch Settings** (131)</span></span>


</dt> <dd></dd> <dt>

<span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>

<span data-ttu-id="7abc7-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destruir conmutador Ethernet** (132)</span><span class="sxs-lookup"><span data-stu-id="7abc7-329"><span id="Destroy_Ethernet_Switch"></span><span id="destroy_ethernet_switch"></span><span id="DESTROY_ETHERNET_SWITCH"></span>**Destroy Ethernet Switch** (132)</span></span>


</dt> <dd></dd> <dt>

<span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="7abc7-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Agregar recursos de conmutador Ethernet** (133)</span><span class="sxs-lookup"><span data-stu-id="7abc7-330"><span id="Add_Ethernet_Switch_Resources"></span><span id="add_ethernet_switch_resources"></span><span id="ADD_ETHERNET_SWITCH_RESOURCES"></span>**Add Ethernet Switch Resources** (133)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="7abc7-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modificar los recursos del conmutador Ethernet** (134)</span><span class="sxs-lookup"><span data-stu-id="7abc7-331"><span id="Modify_Ethernet_Switch_Resources"></span><span id="modify_ethernet_switch_resources"></span><span id="MODIFY_ETHERNET_SWITCH_RESOURCES"></span>**Modify Ethernet Switch Resources** (134)</span></span>


</dt> <dd></dd> <dt>

<span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>

<span data-ttu-id="7abc7-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Quitar recursos del conmutador Ethernet** (135)</span><span class="sxs-lookup"><span data-stu-id="7abc7-332"><span id="Remove_Ethernet_Switch_Resources"></span><span id="remove_ethernet_switch_resources"></span><span id="REMOVE_ETHERNET_SWITCH_RESOURCES"></span>**Remove Ethernet Switch Resources** (135)</span></span>


</dt> <dd></dd> <dt>

<span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validar máquina virtual planeada** (140)</span><span class="sxs-lookup"><span data-stu-id="7abc7-333"><span id="Validate_Planned_Virtual_Machine"></span><span id="validate_planned_virtual_machine"></span><span id="VALIDATE_PLANNED_VIRTUAL_MACHINE"></span>**Validate Planned Virtual Machine** (140)</span></span>


</dt> <dd></dd> <dt>

<span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realización de la máquina virtual** (141)</span><span class="sxs-lookup"><span data-stu-id="7abc7-334"><span id="Realizing_Virtual_Machine"></span><span id="realizing_virtual_machine"></span><span id="REALIZING_VIRTUAL_MACHINE"></span>**Realizing Virtual Machine** (141)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>

<span data-ttu-id="7abc7-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Crear un grupo de recursos** (150)</span><span class="sxs-lookup"><span data-stu-id="7abc7-335"><span id="Creating_a_Resource_Pool"></span><span id="creating_a_resource_pool"></span><span id="CREATING_A_RESOURCE_POOL"></span>**Creating a Resource Pool** (150)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="7abc7-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Cambiar los recursos primarios de un grupo de recursos de sitio** (151)</span><span class="sxs-lookup"><span data-stu-id="7abc7-336"><span id="Changing_the_Parent_Resources_of_a_Resource_Pool"></span><span id="changing_the_parent_resources_of_a_resource_pool"></span><span id="CHANGING_THE_PARENT_RESOURCES_OF_A_RESOURCE_POOL"></span>**Changing the Parent Resources of a Resource Pool** (151)</span></span>


</dt> <dd></dd> <dt>

<span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>

<span data-ttu-id="7abc7-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Cambiar la configuración de un grupo de recursos que no es alloction** (152)</span><span class="sxs-lookup"><span data-stu-id="7abc7-337"><span id="Changing_the_Non-alloction_Settings_of_a_Resource_Pool"></span><span id="changing_the_non-alloction_settings_of_a_resource_pool"></span><span id="CHANGING_THE_NON-ALLOCTION_SETTINGS_OF_A_RESOURCE_POOL"></span>**Changing the Non-alloction Settings of a Resource Pool** (152)</span></span>


</dt> <dd></dd> <dt>

<span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>

<span data-ttu-id="7abc7-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Eliminar un grupo de recursos** (153)</span><span class="sxs-lookup"><span data-stu-id="7abc7-338"><span id="Deleting_a_Resource_Pool"></span><span id="deleting_a_resource_pool"></span><span id="DELETING_A_RESOURCE_POOL"></span>**Deleting a Resource Pool** (153)</span></span>


</dt> <dd></dd> <dt>

<span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="7abc7-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Habilitar GPU de RemoteFx** (160)</span><span class="sxs-lookup"><span data-stu-id="7abc7-339"><span id="Enable_RemoteFx_GPU"></span><span id="enable_remotefx_gpu"></span><span id="ENABLE_REMOTEFX_GPU"></span>**Enable RemoteFx GPU** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>

<span data-ttu-id="7abc7-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Deshabilitar GPU de RemoteFx** (161)</span><span class="sxs-lookup"><span data-stu-id="7abc7-340"><span id="Disable_RemoteFx_GPU"></span><span id="disable_remotefx_gpu"></span><span id="DISABLE_REMOTEFX_GPU"></span>**Disable RemoteFx GPU** (161)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>

<span data-ttu-id="7abc7-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modificar la configuración del servicio 3D** (162)</span><span class="sxs-lookup"><span data-stu-id="7abc7-341"><span id="Modify_3D_Service_Settings"></span><span id="modify_3d_service_settings"></span><span id="MODIFY_3D_SERVICE_SETTINGS"></span>**Modify 3D Service Settings** (162)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-342">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-342">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>

<span data-ttu-id="7abc7-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Copia de seguridad de máquina virtual** (170)</span><span class="sxs-lookup"><span data-stu-id="7abc7-343"><span id="Backup_Virtual_Machine"></span><span id="backup_virtual_machine"></span><span id="BACKUP_VIRTUAL_MACHINE"></span>**Backup Virtual Machine** (170)</span></span>


</dt> <dd></dd> <dt>

<span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>

<span data-ttu-id="7abc7-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Interfaz de servicio de invitado** (180)</span><span class="sxs-lookup"><span data-stu-id="7abc7-344"><span id="Guest_Service_Interface"></span><span id="guest_service_interface"></span><span id="GUEST_SERVICE_INTERFACE"></span>**Guest Service Interface** (180)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-345">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-345">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>

<span data-ttu-id="7abc7-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Consultar la información del clúster invitado** (181)</span><span class="sxs-lookup"><span data-stu-id="7abc7-346"><span id="Query_Guest_Cluster_Information"></span><span id="query_guest_cluster_information"></span><span id="QUERY_GUEST_CLUSTER_INFORMATION"></span>**Query Guest Cluster Information** (181)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-347">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-347">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>

<span data-ttu-id="7abc7-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Definir colección** (190)</span><span class="sxs-lookup"><span data-stu-id="7abc7-348"><span id="Define_Collection"></span><span id="define_collection"></span><span id="DEFINE_COLLECTION"></span>**Define Collection** (190)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-349">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-349">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>

<span data-ttu-id="7abc7-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destruir recopilación** (191)</span><span class="sxs-lookup"><span data-stu-id="7abc7-350"><span id="Destroy_Collection"></span><span id="destroy_collection"></span><span id="DESTROY_COLLECTION"></span>**Destroy Collection** (191)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-351">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-351">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>

<span data-ttu-id="7abc7-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Cambiar el nombre** de la colección (192)</span><span class="sxs-lookup"><span data-stu-id="7abc7-352"><span id="Rename_Collection"></span><span id="rename_collection"></span><span id="RENAME_COLLECTION"></span>**Rename Collection** (192)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-353">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-353">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>

<span data-ttu-id="7abc7-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Agregar miembro a la colección** (193)</span><span class="sxs-lookup"><span data-stu-id="7abc7-354"><span id="Add_Member_to_Collection"></span><span id="add_member_to_collection"></span><span id="ADD_MEMBER_TO_COLLECTION"></span>**Add Member to Collection** (193)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-355">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-355">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>

<span data-ttu-id="7abc7-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Quitar miembro de la colección** (194)</span><span class="sxs-lookup"><span data-stu-id="7abc7-356"><span id="Remove_Member_from_Collection"></span><span id="remove_member_from_collection"></span><span id="REMOVE_MEMBER_FROM_COLLECTION"></span>**Remove Member from Collection** (194)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-357">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-357">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>

<span data-ttu-id="7abc7-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Agregar configuración a la colección** (195)</span><span class="sxs-lookup"><span data-stu-id="7abc7-358"><span id="Add_Setting_to_Collection"></span><span id="add_setting_to_collection"></span><span id="ADD_SETTING_TO_COLLECTION"></span>**Add Setting to Collection** (195)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-359">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-359">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>

<span data-ttu-id="7abc7-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Quitar configuración de la colección** (196)</span><span class="sxs-lookup"><span data-stu-id="7abc7-360"><span id="Remove_Setting_from_Collection"></span><span id="remove_setting_from_collection"></span><span id="REMOVE_SETTING_FROM_COLLECTION"></span>**Remove Setting from Collection** (196)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-361">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-361">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>

<span data-ttu-id="7abc7-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modificar configuración en la colección** (197)</span><span class="sxs-lookup"><span data-stu-id="7abc7-362"><span id="Modify_Setting_on_Collection"></span><span id="modify_setting_on_collection"></span><span id="MODIFY_SETTING_ON_COLLECTION"></span>**Modify Setting on Collection** (197)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-363">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-363">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>

<span data-ttu-id="7abc7-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Recopilación de instantáneas** (198)</span><span class="sxs-lookup"><span data-stu-id="7abc7-364"><span id="Snapshot_Collection"></span><span id="snapshot_collection"></span><span id="SNAPSHOT_COLLECTION"></span>**Snapshot Collection** (198)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-365">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-365">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>

<span data-ttu-id="7abc7-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convertir instantánea en punto de referencia** (200)</span><span class="sxs-lookup"><span data-stu-id="7abc7-366"><span id="Convert_Snapshot_to_Reference_Point"></span><span id="convert_snapshot_to_reference_point"></span><span id="CONVERT_SNAPSHOT_TO_REFERENCE_POINT"></span>**Convert Snapshot to Reference Point** (200)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-367">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-367">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>

<span data-ttu-id="7abc7-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Crear punto de referencia** (201)</span><span class="sxs-lookup"><span data-stu-id="7abc7-368"><span id="Create_Reference_Point"></span><span id="create_reference_point"></span><span id="CREATE_REFERENCE_POINT"></span>**Create Reference Point** (201)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-369">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-369">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>

<span data-ttu-id="7abc7-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Eliminar punto de referencia** (202)</span><span class="sxs-lookup"><span data-stu-id="7abc7-370"><span id="Delete_Reference_Point"></span><span id="delete_reference_point"></span><span id="DELETE_REFERENCE_POINT"></span>**Delete Reference Point** (202)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-371">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-371">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>

<span data-ttu-id="7abc7-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Exportar punto de referencia** (203)</span><span class="sxs-lookup"><span data-stu-id="7abc7-372"><span id="Export_Reference_Point"></span><span id="export_reference_point"></span><span id="EXPORT_REFERENCE_POINT"></span>**Export Reference Point** (203)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-373">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-373">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>

<span data-ttu-id="7abc7-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Quitar datos asociados de un punto de referencia** (204)</span><span class="sxs-lookup"><span data-stu-id="7abc7-374"><span id="Remove_Associated_Data_from_Reference_Point"></span><span id="remove_associated_data_from_reference_point"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT"></span>**Remove Associated Data from Reference Point** (204)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-375">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-375">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="7abc7-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Crear punto de referencia en la colección** (205)</span><span class="sxs-lookup"><span data-stu-id="7abc7-376"><span id="Create_Reference_Point_on_Collection"></span><span id="create_reference_point_on_collection"></span><span id="CREATE_REFERENCE_POINT_ON_COLLECTION"></span>**Create Reference Point on Collection** (205)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-377">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-377">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="7abc7-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Exportar punto de referencia en la colección** (206)</span><span class="sxs-lookup"><span data-stu-id="7abc7-378"><span id="Export_Reference_Point_on_Collection"></span><span id="export_reference_point_on_collection"></span><span id="EXPORT_REFERENCE_POINT_ON_COLLECTION"></span>**Export Reference Point on Collection** (206)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-379">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-379">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="7abc7-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Quitar los datos asociados del punto de referencia de la colección** (207)</span><span class="sxs-lookup"><span data-stu-id="7abc7-380"><span id="Remove_Associated_Data_from_Reference_Point_on_Collection"></span><span id="remove_associated_data_from_reference_point_on_collection"></span><span id="REMOVE_ASSOCIATED_DATA_FROM_REFERENCE_POINT_ON_COLLECTION"></span>**Remove Associated Data from Reference Point on Collection** (207)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-381">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-381">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>

<span data-ttu-id="7abc7-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Eliminar punto de referencia de la colección** (208)</span><span class="sxs-lookup"><span data-stu-id="7abc7-382"><span id="Delete_Reference_Point_on_Collection"></span><span id="delete_reference_point_on_collection"></span><span id="DELETE_REFERENCE_POINT_ON_COLLECTION"></span>**Delete Reference Point on Collection** (208)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-383">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-383">Value added in Windows 10.</span></span>

 

</dd> <dt>

<span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>

<span data-ttu-id="7abc7-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Importar metadatos de punto de referencia** (209)</span><span class="sxs-lookup"><span data-stu-id="7abc7-384"><span id="Import_Reference_Point_metadata"></span><span id="import_reference_point_metadata"></span><span id="IMPORT_REFERENCE_POINT_METADATA"></span>**Import Reference Point metadata** (209)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-385">Valor agregado en Windows 10 como **punto de referencia de limpieza**.</span><span class="sxs-lookup"><span data-stu-id="7abc7-385">Value added in Windows 10 as **Cleanup Reference Point**.</span></span>

 

</dd> <dt>

<span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>

<span data-ttu-id="7abc7-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Montaje o desmontaje de un dispositivo asignable** (260)</span><span class="sxs-lookup"><span data-stu-id="7abc7-386"><span id="Mount_or_Dismount_Assignable_Device"></span><span id="mount_or_dismount_assignable_device"></span><span id="MOUNT_OR_DISMOUNT_ASSIGNABLE_DEVICE"></span>**Mount or Dismount Assignable Device** (260)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7abc7-387">Valor agregado en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7abc7-387">Value added in Windows 10.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7abc7-388">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-388">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-389">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-391">Indica si las horas representadas en las propiedades **RunStartInterval** y **UntilTime** representan las horas locales o las horas UTC.</span><span class="sxs-lookup"><span data-stu-id="7abc7-391">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="7abc7-392">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="7abc7-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Hora local** (1)</span><span class="sxs-lookup"><span data-stu-id="7abc7-393"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Hora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="7abc7-394"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7abc7-395">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="7abc7-395">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-396">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-397">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-398">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="7abc7-398">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-399">Nombre para mostrar de esta instancia de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-399">The display name for this instance of a job.</span></span> <span data-ttu-id="7abc7-400">Además, el nombre para mostrar se puede usar como una propiedad para una búsqueda o una consulta.</span><span class="sxs-lookup"><span data-stu-id="7abc7-400">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="7abc7-401">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-402">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="7abc7-402">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-405">Usuario al que se notifica el error o la finalización del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-405">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="7abc7-406">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-406">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-407">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="7abc7-407">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-408">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-409">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-410">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="7abc7-410">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7abc7-411">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="7abc7-411">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7abc7-412">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-412">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-413">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7abc7-413">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-414">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-414">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-416">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="7abc7-416">The current statuses of the object.</span></span> <span data-ttu-id="7abc7-417">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="7abc7-417">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-418">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="7abc7-418">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-419">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-421">Una cadena que describe la acción de recuperación cuando la propiedad **RecoveryAction** de la instancia es 1 (otra).</span><span class="sxs-lookup"><span data-stu-id="7abc7-421">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="7abc7-422">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-422">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-423">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="7abc7-423">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-426">El usuario que envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-426">The user who submitted the job.</span></span> <span data-ttu-id="7abc7-427">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-427">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-428">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="7abc7-428">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-429">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-429">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-431">Calificadores: **MinValue** (0), **MaxValue** (100), **unidades** ("porcentaje")</span><span class="sxs-lookup"><span data-stu-id="7abc7-431">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-432">Porcentaje de finalización del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-432">The completion percentage of the job.</span></span> <span data-ttu-id="7abc7-433">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-433">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-434">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="7abc7-434">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-435">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-436">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-437">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="7abc7-437">Provides high level status information.</span></span> <span data-ttu-id="7abc7-438">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="7abc7-438">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="7abc7-439">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="7abc7-439">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7abc7-440">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7abc7-440">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-441">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="7abc7-441">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-442">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7abc7-442">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-444">La importancia de la ejecución de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-444">The importance of a job's execution.</span></span> <span data-ttu-id="7abc7-445">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-445">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-446">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="7abc7-446">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-447">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7abc7-447">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-448">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-449">Describe la acción de recuperación que se va a realizar para un trabajo que no se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7abc7-449">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="7abc7-450">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-450">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="7abc7-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7abc7-451"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7abc7-452"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**No continuar** (2)</span><span class="sxs-lookup"><span data-stu-id="7abc7-453"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar con el trabajo siguiente** (3)</span><span class="sxs-lookup"><span data-stu-id="7abc7-454"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Volver a ejecutar el trabajo** (4)</span><span class="sxs-lookup"><span data-stu-id="7abc7-455"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Ejecutar trabajo de recuperación** (5)</span><span class="sxs-lookup"><span data-stu-id="7abc7-456"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7abc7-457">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="7abc7-457">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-458">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="7abc7-458">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-459">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-460">Calificadores: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="7abc7-460">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-461">Día del mes en el que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-461">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="7abc7-462">Hay distintas interpretaciones para esta propiedad, dependiendo del valor de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="7abc7-462">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="7abc7-463">Cuando **RunDayOfWeek** es 0 y **RunDay** es positivo, **RunDay** define el día del mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-463">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="7abc7-464">Por ejemplo, si **RunDayOfWeek** es 0 y **RunDay** es 12, el trabajo se procesará <sup>el día 12</sup> del mes.</span><span class="sxs-lookup"><span data-stu-id="7abc7-464">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="7abc7-465">Cuando **RunDayOfWeek** es 0 y **RunDay** es negativo, **RunDay** define el número de días antes del último día del mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-465">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="7abc7-466">1 indica el último día del mes, 2 indica un día antes del último día del mes, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7abc7-466">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="7abc7-467">Por ejemplo, si **RunDayOfWeek** es 0 y **RunDay** es 1, el trabajo se procesará el último día del mes.</span><span class="sxs-lookup"><span data-stu-id="7abc7-467">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="7abc7-468">Cuando **RunDayOfWeek** no es 0, **RunDayOfWeek** es el día de la semana en el que se procesará el trabajo, en relación con **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="7abc7-468">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="7abc7-469">Por ejemplo, si **RunDay** es 15 y **RunDayOfWeek** es 7 (+ sábado), el trabajo se procesará el primer sábado en o después <sup>del día 15</sup> del mes.</span><span class="sxs-lookup"><span data-stu-id="7abc7-469">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="7abc7-470">Si el **RunDay** es 20 y el de **RunDayOfWeek** es 7 (sábado), el trabajo se procesará el primer sábado en <sup>el día del</sup> mes o antes del mismo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-470">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="7abc7-471">Si **RunDay** es 1 y **RunDayOfWeek** es 1 (domingo), el trabajo se procesará el último domingo del mes.</span><span class="sxs-lookup"><span data-stu-id="7abc7-471">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="7abc7-472">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-472">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-473">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="7abc7-473">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-474">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="7abc7-474">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-475">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-476">Entero positivo o negativo que se usa junto con **RunDay** para indicar el día de la semana o el mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-476">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="7abc7-477">Vea la descripción de la propiedad **RunDay** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7abc7-477">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="7abc7-478">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-478">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="7abc7-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="7abc7-479"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Viernes** (6)</span><span class="sxs-lookup"><span data-stu-id="7abc7-480"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Jueves** (5)</span><span class="sxs-lookup"><span data-stu-id="7abc7-481"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="7abc7-482"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Martes** (3)</span><span class="sxs-lookup"><span data-stu-id="7abc7-483"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lunes** (2)</span><span class="sxs-lookup"><span data-stu-id="7abc7-484"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** (1)</span><span class="sxs-lookup"><span data-stu-id="7abc7-485"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="7abc7-486"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="7abc7-487"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lunes** (2)</span><span class="sxs-lookup"><span data-stu-id="7abc7-488"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Martes** (3)</span><span class="sxs-lookup"><span data-stu-id="7abc7-489"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="7abc7-490"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Jueves** (5)</span><span class="sxs-lookup"><span data-stu-id="7abc7-491"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Viernes** (6)</span><span class="sxs-lookup"><span data-stu-id="7abc7-492"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="7abc7-493"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7abc7-494">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="7abc7-494">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-495">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7abc7-495">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-496">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-496">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-497">Mes en el que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-497">The month during which the job should be processed.</span></span> <span data-ttu-id="7abc7-498">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-498">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="7abc7-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Enero** (0)</span><span class="sxs-lookup"><span data-stu-id="7abc7-499"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Febrero** (1)</span><span class="sxs-lookup"><span data-stu-id="7abc7-500"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Marzo** (2)</span><span class="sxs-lookup"><span data-stu-id="7abc7-501"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Abril** (3)</span><span class="sxs-lookup"><span data-stu-id="7abc7-502"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mayo** (4)</span><span class="sxs-lookup"><span data-stu-id="7abc7-503"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Junio** (5)</span><span class="sxs-lookup"><span data-stu-id="7abc7-504"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Julio** (6)</span><span class="sxs-lookup"><span data-stu-id="7abc7-505"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="7abc7-506"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Septiembre** (8)</span><span class="sxs-lookup"><span data-stu-id="7abc7-507"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Octubre** (9)</span><span class="sxs-lookup"><span data-stu-id="7abc7-508"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Noviembre** (10)</span><span class="sxs-lookup"><span data-stu-id="7abc7-509"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Diciembre** (11)</span><span class="sxs-lookup"><span data-stu-id="7abc7-510"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7abc7-511">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="7abc7-511">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-512">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-512">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-514">El intervalo de tiempo después de medianoche en el momento en que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-514">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="7abc7-515">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-515">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-516">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-516">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-517">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-517">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-518">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-519">La hora de inicio programada para el trabajo, si procede.</span><span class="sxs-lookup"><span data-stu-id="7abc7-519">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="7abc7-520">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-520">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-521">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-521">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-522">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-522">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-523">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-524">La hora a la que comenzó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-524">The time that the job began.</span></span> <span data-ttu-id="7abc7-525">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-525">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-526">**Estado**</span><span class="sxs-lookup"><span data-stu-id="7abc7-526">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-527">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7abc7-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-528">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-528">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-529">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="7abc7-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-530">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7abc7-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-531">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="7abc7-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-532">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-533">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="7abc7-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7abc7-534">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="7abc7-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-535">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="7abc7-535">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-536">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-536">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-537">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-538">Cantidad de tiempo, en minutos, que el trabajo se conserva una vez finalizada la ejecución, ya sea correctamente o con errores en esa ejecución.</span><span class="sxs-lookup"><span data-stu-id="7abc7-538">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="7abc7-539">El trabajo debe permanecer en vigor durante un período de tiempo, independientemente del valor de la propiedad **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="7abc7-539">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="7abc7-540">El valor predeterminado es cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="7abc7-540">The default is five minutes.</span></span> <span data-ttu-id="7abc7-541">Esta propiedad se hereda de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))y siempre está establecida en 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="7abc7-541">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="7abc7-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-543">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-544">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-545">Fecha u hora en que cambió por última vez el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-545">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="7abc7-546">Si el estado del trabajo no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0.</span><span class="sxs-lookup"><span data-stu-id="7abc7-546">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="7abc7-547">Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="7abc7-547">If a state change was requested but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="7abc7-548">Esta propiedad se hereda de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7abc7-548">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-549">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="7abc7-549">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-550">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-550">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-551">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-551">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-552">La hora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="7abc7-552">The time that the job was submitted.</span></span> <span data-ttu-id="7abc7-553">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-553">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="7abc7-554">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-554">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7abc7-555">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7abc7-555">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7abc7-556">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7abc7-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7abc7-557">Hora a la que el trabajo no es válido o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="7abc7-557">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="7abc7-558">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="7abc7-558">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7abc7-559">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7abc7-559">Remarks</span></span>

<span data-ttu-id="7abc7-560">El acceso a la clase **MSVM \_ ConcreteJob** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="7abc7-560">Access to the **Msvm\_ConcreteJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7abc7-561">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7abc7-561">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7abc7-562">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7abc7-562">Requirements</span></span>



| <span data-ttu-id="7abc7-563">Requisito</span><span class="sxs-lookup"><span data-stu-id="7abc7-563">Requirement</span></span> | <span data-ttu-id="7abc7-564">Value</span><span class="sxs-lookup"><span data-stu-id="7abc7-564">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7abc7-565">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7abc7-565">Minimum supported client</span></span><br/> | <span data-ttu-id="7abc7-566">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7abc7-566">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7abc7-567">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7abc7-567">Minimum supported server</span></span><br/> | <span data-ttu-id="7abc7-568">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7abc7-568">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7abc7-569">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7abc7-569">Namespace</span></span><br/>                | <span data-ttu-id="7abc7-570">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7abc7-570">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7abc7-571">MOF</span><span class="sxs-lookup"><span data-stu-id="7abc7-571">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7abc7-572"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-572"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7abc7-573">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7abc7-573">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7abc7-574"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7abc7-574"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7abc7-575">Vea también</span><span class="sxs-lookup"><span data-stu-id="7abc7-575">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7abc7-576">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="7abc7-576">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="7abc7-577">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7abc7-577">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7abc7-578">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="7abc7-578">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

