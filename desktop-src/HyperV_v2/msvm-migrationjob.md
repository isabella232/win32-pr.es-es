---
description: Esta clase representa un trabajo de operación de migración creado para el almacenamiento o la migración del sistema virtual por el servicio de migración del sistema virtual.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Msvm_MigrationJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687268"
---
# <a name="msvm_migrationjob-class"></a><span data-ttu-id="6de2f-103">MSVM \_ MigrationJob (clase)</span><span class="sxs-lookup"><span data-stu-id="6de2f-103">Msvm\_MigrationJob class</span></span>

<span data-ttu-id="6de2f-104">Esta clase representa un trabajo de operación de migración creado para el almacenamiento o la migración del sistema virtual por el servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6de2f-104">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span>

<span data-ttu-id="6de2f-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6de2f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6de2f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6de2f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
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
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="6de2f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6de2f-107">Members</span></span>

<span data-ttu-id="6de2f-108">La clase **MSVM \_ MigrationJob** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6de2f-108">The **Msvm\_MigrationJob** class has these types of members:</span></span>

-   [<span data-ttu-id="6de2f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6de2f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="6de2f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6de2f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6de2f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6de2f-111">Methods</span></span>

<span data-ttu-id="6de2f-112">La clase **MSVM \_ MigrationJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6de2f-112">The **Msvm\_MigrationJob** class has these methods.</span></span>



| <span data-ttu-id="6de2f-113">Método</span><span class="sxs-lookup"><span data-stu-id="6de2f-113">Method</span></span>                                                             | <span data-ttu-id="6de2f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="6de2f-114">Description</span></span>                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6de2f-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="6de2f-115">**GetError**</span></span>](geterror-msvm-migrationjob.md)                     | <span data-ttu-id="6de2f-116">Recupera el objeto de error para el trabajo de migración, si existe uno.</span><span class="sxs-lookup"><span data-stu-id="6de2f-116">Retrieves the error object for the migration job, if one exists.</span></span><br/>                |
| [<span data-ttu-id="6de2f-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="6de2f-117">**GetErrorEx**</span></span>](geterrorex-msvm-migrationjob.md)                 | <span data-ttu-id="6de2f-118">Recupera los objetos de error para el trabajo de migración, si existe alguno.</span><span class="sxs-lookup"><span data-stu-id="6de2f-118">Retrieves the error objects for the migration job, if any exist.</span></span><br/>                |
| <span data-ttu-id="6de2f-119">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="6de2f-119">**KillJob**</span></span>                                                        | <span data-ttu-id="6de2f-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="6de2f-120">This method is not supported.</span></span><br/>                                                   |
| [<span data-ttu-id="6de2f-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6de2f-121">**RequestStateChange**</span></span>](requeststatechange-msvm-migrationjob.md) | <span data-ttu-id="6de2f-122">Solicita que el estado del trabajo de migración se cambie al estado especificado.</span><span class="sxs-lookup"><span data-stu-id="6de2f-122">Requests that the state of the migration job be changed to the specified state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6de2f-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6de2f-123">Properties</span></span>

<span data-ttu-id="6de2f-124">La clase **MSVM \_ MigrationJob** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6de2f-124">The **Msvm\_MigrationJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6de2f-125">**Cancelable**</span><span class="sxs-lookup"><span data-stu-id="6de2f-125">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6de2f-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-128">Indica si se puede cancelar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-128">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="6de2f-129">El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="6de2f-129">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-130">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6de2f-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-133">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6de2f-133">A short description of the object.</span></span> <span data-ttu-id="6de2f-134">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-135">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="6de2f-135">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-136">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-138">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="6de2f-138">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6de2f-139">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6de2f-139">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6de2f-140">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-140">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-141">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="6de2f-141">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="6de2f-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-144">Especifica si el trabajo debe eliminarse automáticamente al finalizar.</span><span class="sxs-lookup"><span data-stu-id="6de2f-144">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="6de2f-145">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-145">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-146">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6de2f-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-149">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="6de2f-149">A description of the object.</span></span> <span data-ttu-id="6de2f-150">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-151">**DestinationHost**</span><span class="sxs-lookup"><span data-stu-id="6de2f-151">**DestinationHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-154">El nombre de host de la plataforma de virtualización de destino a la que está migrando el sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="6de2f-154">The hostname of the destination virtualization platform that the virtual system is migrating to.</span></span> <span data-ttu-id="6de2f-155">Será **null** para la migración de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="6de2f-155">This will be **Null** for storage migration.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6de2f-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-157">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-159">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="6de2f-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6de2f-160">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6de2f-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6de2f-161">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-162">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-163">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-165">El intervalo de tiempo en el que se ha estado ejecutando el trabajo o el tiempo total de ejecución si el trabajo ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="6de2f-165">The time interval that the job has been executing, or the total execution time if the job is complete.</span></span> <span data-ttu-id="6de2f-166">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6de2f-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-170">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="6de2f-170">A display name for the object.</span></span> <span data-ttu-id="6de2f-171">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="6de2f-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-173">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-175">Un código de error específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6de2f-175">A vendor-specific error code.</span></span> <span data-ttu-id="6de2f-176">El valor debe establecerse en cero si el trabajo se completó sin errores.</span><span class="sxs-lookup"><span data-stu-id="6de2f-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="6de2f-177">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="6de2f-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-181">Cadena que contiene la descripción del error del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6de2f-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="6de2f-182">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="6de2f-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-186">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabajo de CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="6de2f-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-187">Descripción breve del error, si está presente.</span><span class="sxs-lookup"><span data-stu-id="6de2f-187">A summary description of the error, if present.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-188">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6de2f-188">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-189">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-191">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="6de2f-191">The current health of the element.</span></span> <span data-ttu-id="6de2f-192">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="6de2f-192">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="6de2f-193">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="6de2f-193">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="6de2f-194">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="6de2f-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-195">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6de2f-195">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-196">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-196">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-198">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6de2f-198">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="6de2f-199">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-200">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6de2f-200">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-201">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-202">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-203">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="6de2f-203">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-204">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="6de2f-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6de2f-205">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="6de2f-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-206">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="6de2f-206">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-207">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6de2f-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-209">El número de veces que se debe ejecutar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-209">The number of times that the job should be run.</span></span> <span data-ttu-id="6de2f-210">Un valor de 1 indica que el trabajo no se repite, mientras que cualquier valor distinto de cero indica un límite del número de veces que se repetirá el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-210">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="6de2f-211">Cero indica que no hay ningún límite en el número de veces que se puede procesar el trabajo, pero se terminará después de que se haya alcanzado el **UntilTime** o cuando el trabajo finalice manualmente.</span><span class="sxs-lookup"><span data-stu-id="6de2f-211">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="6de2f-212">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-212">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-213">**JobState**</span><span class="sxs-lookup"><span data-stu-id="6de2f-213">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-214">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-215">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-216">**JobState** es una enumeración de enteros que indica el estado operativo de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-216">**JobState** is an integer enumeration that indicates the operational state of a job.</span></span> <span data-ttu-id="6de2f-217">También puede indicar transiciones entre estos Estados, por ejemplo, "apagar" e "iniciando".</span><span class="sxs-lookup"><span data-stu-id="6de2f-217">It can also indicate transitions between these states, for example, "Shutting Down" and "Starting".</span></span> <span data-ttu-id="6de2f-218">Esta propiedad se hereda de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6de2f-218">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="6de2f-219">Value</span><span class="sxs-lookup"><span data-stu-id="6de2f-219">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="6de2f-220">Significado</span><span class="sxs-lookup"><span data-stu-id="6de2f-220">Meaning</span></span>                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="6de2f-221"><dt>**Nuevo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-221"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                           | <span data-ttu-id="6de2f-222">Nunca se ha iniciado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-222">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="6de2f-223"><dt>**Inicio**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-223"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="6de2f-224">El trabajo se mueve de los Estados 2 (nuevo), 5 (suspendido) u 11 (servicio) al estado 4 (en ejecución).</span><span class="sxs-lookup"><span data-stu-id="6de2f-224">The job is moving from the 2 (New), 5(Suspended), or 11 (Service) states into the 4 (Running) state.</span></span><br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="6de2f-225"><dt>**Ejecución**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-225"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="6de2f-226">El trabajo se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="6de2f-226">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="6de2f-227"><dt>**Suspendido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-227"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                   | <span data-ttu-id="6de2f-228">El trabajo se ha detenido, pero se puede reiniciar sin problemas.</span><span class="sxs-lookup"><span data-stu-id="6de2f-228">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="6de2f-229"><dt>**Cerrando**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-229"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                   | <span data-ttu-id="6de2f-230">El trabajo se está cambiando a un estado 7 (completado), 8 (finalizado) o 9 (con terminación).</span><span class="sxs-lookup"><span data-stu-id="6de2f-230">The job is moving to a 7 (Completed), 8 (Terminated), or 9 (Killed) state.</span></span><br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="6de2f-231"><dt>**Completado**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-231"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="6de2f-232">El trabajo se ha completado con normalidad.</span><span class="sxs-lookup"><span data-stu-id="6de2f-232">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="6de2f-233"><dt>**Terminó**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-233"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                               | <span data-ttu-id="6de2f-234">El trabajo se ha detenido mediante una solicitud de cambio de estado "finalizar".</span><span class="sxs-lookup"><span data-stu-id="6de2f-234">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="6de2f-235">El trabajo y todos sus procesos subyacentes finalizan y solo se pueden reiniciar como un nuevo trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-235">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="6de2f-236">El requisito de que el trabajo se reinicie solo como un nuevo trabajo es específico del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-236">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="6de2f-237"><dt>**Eliminado**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-237"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                               | <span data-ttu-id="6de2f-238">La solicitud de cambio de estado "Kill" detuvo el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-238">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="6de2f-239">Es posible que los procesos subyacentes sigan en ejecución y que sea necesario realizar una limpieza para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="6de2f-239">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="6de2f-240"><dt>**Excepción**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-240"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                  | <span data-ttu-id="6de2f-241">El trabajo está en un estado anómalo que podría ser indicativo de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="6de2f-241">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="6de2f-242">El estado real del trabajo podría estar disponible a través de objetos específicos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-242">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="6de2f-243"><dt>**Servicio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-243"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                          | <span data-ttu-id="6de2f-244">El trabajo está en un estado específico del proveedor que admite la detección de problemas, la resolución o ambos.</span><span class="sxs-lookup"><span data-stu-id="6de2f-244">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="6de2f-245"><dt>**DMTF reservado**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-245"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>            | <span data-ttu-id="6de2f-246">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6de2f-246">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="6de2f-247"><dt>**Proveedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-247"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="6de2f-248">Reservado.</span><span class="sxs-lookup"><span data-stu-id="6de2f-248">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="6de2f-249">**Estado del trabajo**</span><span class="sxs-lookup"><span data-stu-id="6de2f-249">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-250">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-252">Cadena que representa el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-252">A string that represents the job status.</span></span> <span data-ttu-id="6de2f-253">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-253">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-254">**JobType**</span><span class="sxs-lookup"><span data-stu-id="6de2f-254">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-255">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-257">Indica el tipo de trabajo del que este objeto realiza el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="6de2f-257">Indicates the type of job being tracked by this object.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6de2f-258">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6de2f-258">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

<span data-ttu-id="6de2f-259">**Creación de una máquina virtual remota** (300)</span><span class="sxs-lookup"><span data-stu-id="6de2f-259">**Creating Remote Virtual Machine** (300)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

<span data-ttu-id="6de2f-260">**Comprobando la compatibilidad de las máquinas virtuales** (301)</span><span class="sxs-lookup"><span data-stu-id="6de2f-260">**Checking Virtual Machine Compatibility** (301)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="6de2f-261">**Comprobando la compatibilidad de la máquina virtual y el almacenamiento** (302)</span><span class="sxs-lookup"><span data-stu-id="6de2f-261">**Checking Virtual Machine and Storage Compatibility** (302)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

<span data-ttu-id="6de2f-262">**Comprobando la compatibilidad de almacenamiento** (303)</span><span class="sxs-lookup"><span data-stu-id="6de2f-262">**Checking Storage Compatibility** (303)</span></span>


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

<span data-ttu-id="6de2f-263">**Comprobando la migración de almacenamiento** (304)</span><span class="sxs-lookup"><span data-stu-id="6de2f-263">**Checking Storage Migration** (304)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

<span data-ttu-id="6de2f-264">**Mover la máquina virtual** (305)</span><span class="sxs-lookup"><span data-stu-id="6de2f-264">**Moving Virtual Machine** (305)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

<span data-ttu-id="6de2f-265">**Traslado de máquinas virtuales y almacenamiento** (306)</span><span class="sxs-lookup"><span data-stu-id="6de2f-265">**Moving Virtual Machine and Storage** (306)</span></span>


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

<span data-ttu-id="6de2f-266">**Mover almacenamiento** (307)</span><span class="sxs-lookup"><span data-stu-id="6de2f-266">**Moving Storage** (307)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6de2f-267">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-267">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-268">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-269">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-270">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-270">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<span data-ttu-id="6de2f-271">Indica si las horas representadas en las propiedades **RunStartInterval** y **UntilTime** representan las horas locales o las horas UTC.</span><span class="sxs-lookup"><span data-stu-id="6de2f-271">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span>

<dl> <dt>

<span data-ttu-id="6de2f-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Hora local** (1)</span><span class="sxs-lookup"><span data-stu-id="6de2f-272"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Hora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="6de2f-273"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6de2f-274">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="6de2f-274">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-275">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-277">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span><span class="sxs-lookup"><span data-stu-id="6de2f-277">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-278">El tipo de migración representado por este objeto de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-278">The migration type represented by this job object.</span></span> <span data-ttu-id="6de2f-279">Será uno de los valores definidos para la propiedad **MigrationType** de la clase [**\_ VirtualSystemMigrationSettingData de MSVM**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6de2f-279">This will be one of the values defined for the **MigrationType** property of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-280">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="6de2f-280">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-281">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-283">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="6de2f-283">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-284">Nombre para mostrar de esta instancia de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-284">The display name for this instance of a job.</span></span> <span data-ttu-id="6de2f-285">Además, el nombre para mostrar se puede usar como una propiedad para una búsqueda o una consulta.</span><span class="sxs-lookup"><span data-stu-id="6de2f-285">In addition, the display name can be used as a property for a search or query.</span></span> <span data-ttu-id="6de2f-286">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-287">**NewResourceSettingData**</span><span class="sxs-lookup"><span data-stu-id="6de2f-287">**NewResourceSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-288">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="6de2f-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-290">En el caso de una migración en vivo, siempre se establecerá en **null**.</span><span class="sxs-lookup"><span data-stu-id="6de2f-290">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="6de2f-291">En el caso de una migración de almacenamiento, si es **null**, no se mueve ninguno de los discos duros virtuales (VHD) de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6de2f-291">For a storage migration, if this is **Null**, none of the virtual machine's virtual hard disks (VHDs) will be moved.</span></span> <span data-ttu-id="6de2f-292">De lo contrario, contendrá una matriz de instancias incrustadas de la clase [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) que representan los VHD que se van a deshacer.</span><span class="sxs-lookup"><span data-stu-id="6de2f-292">Otherwise, this will contain an array of embedded instances of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) class that represent the VHDs to be moved.</span></span> <span data-ttu-id="6de2f-293">La propiedad de **conexión** de estas instancias especificará la ubicación de destino del VHD.</span><span class="sxs-lookup"><span data-stu-id="6de2f-293">The **Connection** property of these instances will specify the destination location of the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-294">**NewSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="6de2f-294">**NewSystemSettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-295">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-296">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-297">En el caso de una migración en vivo, siempre se establecerá en **null**.</span><span class="sxs-lookup"><span data-stu-id="6de2f-297">For a live migration, this will always be set to **Null**.</span></span>

<span data-ttu-id="6de2f-298">En el caso de una migración de almacenamiento, si es **null**, las raíces de datos de la máquina virtual no se mueven.</span><span class="sxs-lookup"><span data-stu-id="6de2f-298">For a storage migration, if this is **Null**, the virtual machine's data roots are not moving.</span></span> <span data-ttu-id="6de2f-299">De lo contrario, contendrá una instancia incrustada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) , donde las propiedades **ExternalDataRoot**, **SnapshotDataRoot** y **SwapFileDataRoot** especificarán las nuevas raíces de datos.</span><span class="sxs-lookup"><span data-stu-id="6de2f-299">Otherwise, this will contain an embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class, where the **ExternalDataRoot**, **SnapshotDataRoot**, and **SwapFileDataRoot** properties will specify the new data roots.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-300">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="6de2f-300">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-301">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-302">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-303">Usuario al que se notifica el error o la finalización del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-303">The user that is notified upon job completion or failure.</span></span> <span data-ttu-id="6de2f-304">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-304">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-305">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="6de2f-305">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-306">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-307">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-308">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="6de2f-308">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6de2f-309">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6de2f-309">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6de2f-310">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6de2f-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-312">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-313">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-314">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="6de2f-314">The current statuses of the object.</span></span> <span data-ttu-id="6de2f-315">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="6de2f-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-316">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="6de2f-316">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-317">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-318">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-319">Una cadena que describe la acción de recuperación cuando la propiedad **RecoveryAction** de la instancia es 1 (otra).</span><span class="sxs-lookup"><span data-stu-id="6de2f-319">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="6de2f-320">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-320">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-321">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="6de2f-321">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-322">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-323">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-324">El usuario que envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-324">The user who submitted the job.</span></span> <span data-ttu-id="6de2f-325">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-325">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-326">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="6de2f-326">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-327">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-328">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-329">Calificadores: **MinValue** (0), **MaxValue** (100), **unidades** ("porcentaje")</span><span class="sxs-lookup"><span data-stu-id="6de2f-329">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-330">Porcentaje de finalización del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-330">The completion percentage of the job.</span></span> <span data-ttu-id="6de2f-331">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-331">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-332">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="6de2f-332">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-333">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-333">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-334">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-335">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="6de2f-335">Provides high level status information.</span></span> <span data-ttu-id="6de2f-336">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="6de2f-336">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="6de2f-337">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="6de2f-337">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6de2f-338">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="6de2f-338">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-339">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="6de2f-339">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-340">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6de2f-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-342">La importancia de la ejecución de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-342">The importance of a job's execution.</span></span> <span data-ttu-id="6de2f-343">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-343">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-344">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="6de2f-344">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-345">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6de2f-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-347">Describe la acción de recuperación que se va a realizar para un trabajo que no se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="6de2f-347">Describes the recovery action to be taken for an unsuccessfully run job.</span></span> <span data-ttu-id="6de2f-348">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-348">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="6de2f-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6de2f-349"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="6de2f-350"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**No continuar** (2)</span><span class="sxs-lookup"><span data-stu-id="6de2f-351"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar con el trabajo siguiente** (3)</span><span class="sxs-lookup"><span data-stu-id="6de2f-352"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Volver a ejecutar el trabajo** (4)</span><span class="sxs-lookup"><span data-stu-id="6de2f-353"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Ejecutar trabajo de recuperación** (5)</span><span class="sxs-lookup"><span data-stu-id="6de2f-354"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6de2f-355">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="6de2f-355">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-356">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6de2f-356">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-357">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-358">Calificadores: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="6de2f-358">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-359">Día del mes en el que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-359">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="6de2f-360">Hay distintas interpretaciones para esta propiedad, dependiendo del valor de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="6de2f-360">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="6de2f-361">Cuando **RunDayOfWeek** es 0 y **RunDay** es positivo, **RunDay** define el día del mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-361">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="6de2f-362">Por ejemplo, si **RunDayOfWeek** es 0 y **RunDay** es 12, el trabajo se procesará <sup>el día 12</sup> del mes.</span><span class="sxs-lookup"><span data-stu-id="6de2f-362">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="6de2f-363">Cuando **RunDayOfWeek** es 0 y **RunDay** es negativo, **RunDay** define el número de días antes del último día del mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-363">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="6de2f-364">1 indica el último día del mes, 2 indica un día antes del último día del mes, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="6de2f-364">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="6de2f-365">Por ejemplo, si **RunDayOfWeek** es 0 y **RunDay** es 1, el trabajo se procesará el último día del mes.</span><span class="sxs-lookup"><span data-stu-id="6de2f-365">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="6de2f-366">Cuando **RunDayOfWeek** no es 0, **RunDayOfWeek** es el día de la semana en el que se procesará el trabajo, en relación con **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="6de2f-366">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="6de2f-367">Por ejemplo, si **RunDay** es 15 y **RunDayOfWeek** es 7 (+ sábado), el trabajo se procesará el primer sábado en o después <sup>del día 15</sup> del mes.</span><span class="sxs-lookup"><span data-stu-id="6de2f-367">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="6de2f-368">Si el **RunDay** es 20 y el de **RunDayOfWeek** es 7 (sábado), el trabajo se procesará el primer sábado en <sup>el día del</sup> mes o antes del mismo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-368">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="6de2f-369">Si **RunDay** es 1 y **RunDayOfWeek** es 1 (domingo), el trabajo se procesará el último domingo del mes.</span><span class="sxs-lookup"><span data-stu-id="6de2f-369">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="6de2f-370">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-370">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-371">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="6de2f-371">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-372">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6de2f-372">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-374">Entero positivo o negativo que se usa junto con **RunDay** para indicar el día de la semana o el mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-374">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="6de2f-375">Vea la descripción de la propiedad **RunDay** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="6de2f-375">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="6de2f-376">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-376">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="6de2f-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="6de2f-377"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Viernes** (6)</span><span class="sxs-lookup"><span data-stu-id="6de2f-378"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Jueves** (5)</span><span class="sxs-lookup"><span data-stu-id="6de2f-379"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="6de2f-380"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Martes** (3)</span><span class="sxs-lookup"><span data-stu-id="6de2f-381"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lunes** (2)</span><span class="sxs-lookup"><span data-stu-id="6de2f-382"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** (1)</span><span class="sxs-lookup"><span data-stu-id="6de2f-383"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="6de2f-384"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="6de2f-385"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lunes** (2)</span><span class="sxs-lookup"><span data-stu-id="6de2f-386"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Martes** (3)</span><span class="sxs-lookup"><span data-stu-id="6de2f-387"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="6de2f-388"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Jueves** (5)</span><span class="sxs-lookup"><span data-stu-id="6de2f-389"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Viernes** (6)</span><span class="sxs-lookup"><span data-stu-id="6de2f-390"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="6de2f-391"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6de2f-392">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="6de2f-392">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-393">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6de2f-393">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-394">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-395">Mes en el que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-395">The month during which the job should be processed.</span></span> <span data-ttu-id="6de2f-396">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-396">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="6de2f-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Enero** (0)</span><span class="sxs-lookup"><span data-stu-id="6de2f-397"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Febrero** (1)</span><span class="sxs-lookup"><span data-stu-id="6de2f-398"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Marzo** (2)</span><span class="sxs-lookup"><span data-stu-id="6de2f-399"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Abril** (3)</span><span class="sxs-lookup"><span data-stu-id="6de2f-400"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mayo** (4)</span><span class="sxs-lookup"><span data-stu-id="6de2f-401"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Junio** (5)</span><span class="sxs-lookup"><span data-stu-id="6de2f-402"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Julio** (6)</span><span class="sxs-lookup"><span data-stu-id="6de2f-403"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="6de2f-404"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Septiembre** (8)</span><span class="sxs-lookup"><span data-stu-id="6de2f-405"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Octubre** (9)</span><span class="sxs-lookup"><span data-stu-id="6de2f-406"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Noviembre** (10)</span><span class="sxs-lookup"><span data-stu-id="6de2f-407"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Diciembre** (11)</span><span class="sxs-lookup"><span data-stu-id="6de2f-408"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6de2f-409">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="6de2f-409">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-410">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-410">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-411">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-412">El intervalo de tiempo después de medianoche en el momento en que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-412">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="6de2f-413">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-414">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-414">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-415">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-417">La hora de inicio programada para el trabajo, si procede.</span><span class="sxs-lookup"><span data-stu-id="6de2f-417">The scheduled start time for the job, if applicable.</span></span> <span data-ttu-id="6de2f-418">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-419">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-419">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-420">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-420">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-422">La hora a la que comenzó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-422">The time that the job began.</span></span> <span data-ttu-id="6de2f-423">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-423">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-424">**Estado**</span><span class="sxs-lookup"><span data-stu-id="6de2f-424">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-425">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-426">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-427">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="6de2f-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-428">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6de2f-428">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-429">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="6de2f-429">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-431">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="6de2f-431">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6de2f-432">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="6de2f-432">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-433">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="6de2f-433">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-434">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-434">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-435">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-436">Cantidad de tiempo, en minutos, que el trabajo se conserva una vez finalizada la ejecución, ya sea correctamente o con errores en esa ejecución.</span><span class="sxs-lookup"><span data-stu-id="6de2f-436">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="6de2f-437">El trabajo debe permanecer en vigor durante un período de tiempo, independientemente del valor de la propiedad **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="6de2f-437">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="6de2f-438">El valor predeterminado es cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="6de2f-438">The default is five minutes.</span></span> <span data-ttu-id="6de2f-439">Esta propiedad se hereda de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))y siempre está establecida en 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="6de2f-439">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-440">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="6de2f-440">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-441">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-443">Fecha u hora en que cambió por última vez el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-443">The date or time when the state of the job last changed.</span></span> <span data-ttu-id="6de2f-444">Si el estado del trabajo no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0.</span><span class="sxs-lookup"><span data-stu-id="6de2f-444">If the state of the job has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="6de2f-445">Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar.</span><span class="sxs-lookup"><span data-stu-id="6de2f-445">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="6de2f-446">Esta propiedad se hereda de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6de2f-446">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-447">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="6de2f-447">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-448">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-448">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-449">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-450">La hora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="6de2f-450">The time that the job was submitted.</span></span> <span data-ttu-id="6de2f-451">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-451">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-452">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-452">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-453">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6de2f-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-454">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-455">Hora a la que el trabajo no es válido o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="6de2f-455">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="6de2f-456">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="6de2f-456">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="6de2f-457">**VirtualSystemName**</span><span class="sxs-lookup"><span data-stu-id="6de2f-457">**VirtualSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6de2f-458">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6de2f-458">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6de2f-459">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6de2f-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6de2f-460">Nombre único del sistema virtual afectado.</span><span class="sxs-lookup"><span data-stu-id="6de2f-460">The unique name of the affected virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6de2f-461">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6de2f-461">Requirements</span></span>



| <span data-ttu-id="6de2f-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="6de2f-462">Requirement</span></span> | <span data-ttu-id="6de2f-463">Value</span><span class="sxs-lookup"><span data-stu-id="6de2f-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de2f-464">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6de2f-464">Minimum supported client</span></span><br/> | <span data-ttu-id="6de2f-465">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="6de2f-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6de2f-466">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6de2f-466">Minimum supported server</span></span><br/> | <span data-ttu-id="6de2f-467">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6de2f-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6de2f-468">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6de2f-468">Namespace</span></span><br/>                | <span data-ttu-id="6de2f-469">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6de2f-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6de2f-470">MOF</span><span class="sxs-lookup"><span data-stu-id="6de2f-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6de2f-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6de2f-472">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6de2f-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6de2f-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6de2f-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

