---
description: Representa un trabajo de operación de almacenamiento creado por el servicio de administración de imágenes de Hyper-V de Microsoft.
ms.assetid: a1517c1f-7fb6-4203-a5ec-2ecdfcbc4e8c
title: Msvm_StorageJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob
- Msvm_StorageJob.KillJob
- Msvm_StorageJob.InstanceID
- Msvm_StorageJob.Caption
- Msvm_StorageJob.Description
- Msvm_StorageJob.ElementName
- Msvm_StorageJob.InstallDate
- Msvm_StorageJob.Name
- Msvm_StorageJob.OperationalStatus
- Msvm_StorageJob.StatusDescriptions
- Msvm_StorageJob.Status
- Msvm_StorageJob.HealthState
- Msvm_StorageJob.CommunicationStatus
- Msvm_StorageJob.DetailedStatus
- Msvm_StorageJob.OperatingStatus
- Msvm_StorageJob.PrimaryStatus
- Msvm_StorageJob.JobStatus
- Msvm_StorageJob.TimeSubmitted
- Msvm_StorageJob.ScheduledStartTime
- Msvm_StorageJob.StartTime
- Msvm_StorageJob.ElapsedTime
- Msvm_StorageJob.JobRunTimes
- Msvm_StorageJob.RunMonth
- Msvm_StorageJob.RunDay
- Msvm_StorageJob.RunDayOfWeek
- Msvm_StorageJob.RunStartInterval
- Msvm_StorageJob.LocalOrUtcTime
- Msvm_StorageJob.UntilTime
- Msvm_StorageJob.Notify
- Msvm_StorageJob.Owner
- Msvm_StorageJob.Priority
- Msvm_StorageJob.PercentComplete
- Msvm_StorageJob.DeleteOnCompletion
- Msvm_StorageJob.ErrorCode
- Msvm_StorageJob.ErrorDescription
- Msvm_StorageJob.ErrorSummaryDescription
- Msvm_StorageJob.RecoveryAction
- Msvm_StorageJob.OtherRecoveryAction
- Msvm_StorageJob.JobState
- Msvm_StorageJob.TimeOfLastStateChange
- Msvm_StorageJob.TimeBeforeRemoval
- Msvm_StorageJob.Cancellable
- Msvm_StorageJob.Child
- Msvm_StorageJob.JobCompletionStatusCode
- Msvm_StorageJob.Parent
- Msvm_StorageJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3014cb9a8201d7baceaf39bb760b17c33844abeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913701"
---
# <a name="msvm_storagejob-class"></a><span data-ttu-id="f0a46-103">MSVM \_ StorageJob (clase)</span><span class="sxs-lookup"><span data-stu-id="f0a46-103">Msvm\_StorageJob class</span></span>

<span data-ttu-id="f0a46-104">Representa un trabajo de operación de almacenamiento creado por el servicio de administración de imágenes de Hyper-V de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f0a46-104">Represents a storage operation job created by the Microsoft Hyper-V Image Management Service.</span></span>

<span data-ttu-id="f0a46-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f0a46-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0a46-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0a46-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
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
  datetime TimeBeforeRemoval = 00000000000500.000000:000";
  boolean  Cancellable;
  string   Child;
  UINT32   JobCompletionStatusCode;
  string   Parent;
  uint16   JobType;
};
```

## <a name="members"></a><span data-ttu-id="f0a46-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0a46-107">Members</span></span>

<span data-ttu-id="f0a46-108">La clase **MSVM \_ StorageJob** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f0a46-108">The **Msvm\_StorageJob** class has these types of members:</span></span>

-   [<span data-ttu-id="f0a46-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f0a46-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="f0a46-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0a46-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f0a46-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f0a46-111">Methods</span></span>

<span data-ttu-id="f0a46-112">La clase **MSVM \_ StorageJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="f0a46-112">The **Msvm\_StorageJob** class has these methods.</span></span>



| <span data-ttu-id="f0a46-113">Método</span><span class="sxs-lookup"><span data-stu-id="f0a46-113">Method</span></span>                                                           | <span data-ttu-id="f0a46-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0a46-114">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0a46-115">**GetError**</span><span class="sxs-lookup"><span data-stu-id="f0a46-115">**GetError**</span></span>](msvm-storagejob-geterror.md)                     | <span data-ttu-id="f0a46-116">Recupera el error que describe la razón por la que se produjo un error en el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-116">Retrieves the error that describes the reason why the job failed.</span></span><br/>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f0a46-117">**GetErrorEx**</span><span class="sxs-lookup"><span data-stu-id="f0a46-117">**GetErrorEx**</span></span>](geterrorex-msvm-storagejob.md)                 | <span data-ttu-id="f0a46-118">Cuando el trabajo se está ejecutando o ha finalizado sin errores, este método no devuelve ninguna instancia de [**\_ error MSVM**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a46-118">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="f0a46-119">Sin embargo, si se ha producido un error en el trabajo debido a algún problema interno o porque el trabajo ha sido terminado por un cliente, se devuelven una o varias instancias de **\_ error de MSVM** .</span><span class="sxs-lookup"><span data-stu-id="f0a46-119">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span><br/> |
| <span data-ttu-id="f0a46-120">**KillJob**</span><span class="sxs-lookup"><span data-stu-id="f0a46-120">**KillJob**</span></span>                                                      | <span data-ttu-id="f0a46-121">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="f0a46-121">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="f0a46-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="f0a46-122">**RequestStateChange**</span></span>](msvm-storagejob-requeststatechange.md) | <span data-ttu-id="f0a46-123">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="f0a46-123">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="f0a46-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0a46-124">Properties</span></span>

<span data-ttu-id="f0a46-125">La clase **MSVM \_ StorageJob** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0a46-125">The **Msvm\_StorageJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0a46-126">**Cancelable**</span><span class="sxs-lookup"><span data-stu-id="f0a46-126">**Cancellable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-127">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f0a46-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-129">Indica si se puede cancelar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-129">Indicates whether the job can be canceled.</span></span> <span data-ttu-id="f0a46-130">El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0a46-130">The value of this property does not guarantee that a request to cancel the job will succeed.</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f0a46-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-134">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a46-134">A short description of the object.</span></span> <span data-ttu-id="f0a46-135">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-136">**Elemento secundario**</span><span class="sxs-lookup"><span data-stu-id="f0a46-136">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-139">En caso de que se produzca un error en la operación asincrónica, esta propiedad contiene la ruta de acceso completa del elemento secundario del VHD que se ve afectado por esta operación.</span><span class="sxs-lookup"><span data-stu-id="f0a46-139">On failure of the asynchronous operation, this property contains the full path of the child of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-140">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="f0a46-140">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-141">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-143">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="f0a46-143">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="f0a46-144">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="f0a46-144">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f0a46-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-145">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-146">**DeleteOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="f0a46-146">**DeleteOnCompletion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-147">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f0a46-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-149">Especifica si el trabajo debe eliminarse automáticamente al finalizar.</span><span class="sxs-lookup"><span data-stu-id="f0a46-149">Specifies whether the job should be automatically deleted upon completion.</span></span> <span data-ttu-id="f0a46-150">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-150">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-151">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f0a46-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-154">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a46-154">A description of the object.</span></span> <span data-ttu-id="f0a46-155">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="f0a46-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-157">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-159">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="f0a46-159">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="f0a46-160">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="f0a46-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f0a46-161">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-162">**ElapsedTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-162">**ElapsedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-163">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-163">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-165">Período de tiempo durante el que se ha estado ejecutando el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-165">The length of time that the job has been executing.</span></span> <span data-ttu-id="f0a46-166">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-166">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-167">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f0a46-167">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-170">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a46-170">A display name for the object.</span></span> <span data-ttu-id="f0a46-171">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-172">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="f0a46-172">**ErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-173">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-175">Un código de error específico del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f0a46-175">A vendor-specific error code.</span></span> <span data-ttu-id="f0a46-176">El valor debe establecerse en cero si el trabajo se completó sin errores.</span><span class="sxs-lookup"><span data-stu-id="f0a46-176">The value must be set to zero if the job completed without error.</span></span> <span data-ttu-id="f0a46-177">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-177">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-178">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f0a46-178">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-181">Cadena que contiene la descripción del error del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f0a46-181">A string that contains the vendor error description.</span></span> <span data-ttu-id="f0a46-182">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-182">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-183">**ErrorSummaryDescription**</span><span class="sxs-lookup"><span data-stu-id="f0a46-183">**ErrorSummaryDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-186">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabajo de CIM**](cim-job.md).**ErrorCode**")</span><span class="sxs-lookup"><span data-stu-id="f0a46-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Job**](cim-job.md).**ErrorCode**")</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-187">Descripción breve del error, si está presente.</span><span class="sxs-lookup"><span data-stu-id="f0a46-187">A summary description of the error, if present.</span></span> <span data-ttu-id="f0a46-188">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-188">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="f0a46-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-190">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-192">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="f0a46-192">The current health of the element.</span></span> <span data-ttu-id="f0a46-193">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="f0a46-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="f0a46-194">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="f0a46-194">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="f0a46-195">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.</span><span class="sxs-lookup"><span data-stu-id="f0a46-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-196">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f0a46-196">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-197">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-197">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-199">Fecha y hora en que se creó la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0a46-199">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="f0a46-200">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-201">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f0a46-201">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-202">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-204">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="f0a46-204">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f0a46-205">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-205">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-206">**JobCompletionStatusCode**</span><span class="sxs-lookup"><span data-stu-id="f0a46-206">**JobCompletionStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-207">Tipo de datos: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="f0a46-207">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-209">Código **HRESULT** que describe el estado de finalización de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f0a46-209">The **HRESULT** code that describes the completion status for the asynchronous operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-210">**JobRunTimes**</span><span class="sxs-lookup"><span data-stu-id="f0a46-210">**JobRunTimes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-211">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0a46-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-212">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-213">El número de veces que se debe ejecutar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-213">The number of times that the job should be run.</span></span> <span data-ttu-id="f0a46-214">Un valor de 1 indica que el trabajo no se repite, mientras que cualquier valor distinto de cero indica un límite del número de veces que se repetirá el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-214">A value of 1 indicates that the job is not recurring, while any nonzero value indicates a limit to the number of times that the job will recur.</span></span> <span data-ttu-id="f0a46-215">Cero indica que no hay ningún límite en el número de veces que se puede procesar el trabajo, pero se terminará después de que se haya alcanzado el **UntilTime** o cuando el trabajo finalice manualmente.</span><span class="sxs-lookup"><span data-stu-id="f0a46-215">Zero indicates that there is no limit to the number of times that the job can be processed, but it will be terminated either after the **UntilTime** has been reached, or the job is manually terminated.</span></span> <span data-ttu-id="f0a46-216">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-216">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-217">**JobState**</span><span class="sxs-lookup"><span data-stu-id="f0a46-217">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-218">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-220">El estado operativo de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-220">The operational state of a job.</span></span> <span data-ttu-id="f0a46-221">También puede indicar transiciones entre estos Estados, por ejemplo, 6 (apagado) y 3 (iniciando).</span><span class="sxs-lookup"><span data-stu-id="f0a46-221">It can also indicate transitions between these states, for example, 6 (Shutting Down) and 3 (Starting).</span></span> <span data-ttu-id="f0a46-222">Esta propiedad se hereda de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0a46-222">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>



| <span data-ttu-id="f0a46-223">Value</span><span class="sxs-lookup"><span data-stu-id="f0a46-223">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="f0a46-224">Significado</span><span class="sxs-lookup"><span data-stu-id="f0a46-224">Meaning</span></span>                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <span data-ttu-id="f0a46-225"><dt>**Nuevo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-225"><dt>**New**</dt> <dt>2</dt></span></span> </dl>                                                               | <span data-ttu-id="f0a46-226">Nunca se ha iniciado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-226">The job has never been started.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="f0a46-227"><dt>**Inicio**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-227"><dt>**Starting**</dt> <dt>3</dt></span></span> </dl>                                           | <span data-ttu-id="f0a46-228">El trabajo se mueve de los Estados "nuevo", "suspendido" o "servicio" al estado "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="f0a46-228">The job is moving from the "New", "Suspended", or "Service" states into the "Running" state.</span></span><br/>                                                                                                                                            |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <span data-ttu-id="f0a46-229"><dt>**Ejecución**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-229"><dt>**Running**</dt> <dt>4</dt></span></span> </dl>                                               | <span data-ttu-id="f0a46-230">El trabajo se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f0a46-230">The job is running.</span></span><br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <span data-ttu-id="f0a46-231"><dt>**Suspendido**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-231"><dt>**Suspended**</dt> <dt>5</dt></span></span> </dl>                                       | <span data-ttu-id="f0a46-232">El trabajo se ha detenido, pero se puede reiniciar sin problemas.</span><span class="sxs-lookup"><span data-stu-id="f0a46-232">The job is stopped, but it can be restarted in a seamless manner.</span></span><br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="f0a46-233"><dt>**Cerrando**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-233"><dt>**Shutting Down**</dt> <dt>6</dt></span></span> </dl>                       | <span data-ttu-id="f0a46-234">El trabajo se está cambiando a un estado "completado", "finalizado" o "eliminado".</span><span class="sxs-lookup"><span data-stu-id="f0a46-234">The job is moving to a "Completed", "Terminated", or "Killed" state.</span></span><br/>                                                                                                                                                                    |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <span data-ttu-id="f0a46-235"><dt>**Completado**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-235"><dt>**Completed**</dt> <dt>7</dt></span></span> </dl>                                       | <span data-ttu-id="f0a46-236">El trabajo se ha completado con normalidad.</span><span class="sxs-lookup"><span data-stu-id="f0a46-236">The job has completed normally.</span></span><br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <span data-ttu-id="f0a46-237"><dt>**Terminó**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-237"><dt>**Terminated**</dt> <dt>8</dt></span></span> </dl>                                   | <span data-ttu-id="f0a46-238">El trabajo se ha detenido mediante una solicitud de cambio de estado "finalizar".</span><span class="sxs-lookup"><span data-stu-id="f0a46-238">The job has been stopped by a "Terminate" state change request.</span></span> <span data-ttu-id="f0a46-239">El trabajo y todos sus procesos subyacentes finalizan y solo se pueden reiniciar como un nuevo trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-239">The job and all its underlying processes are ended and can be restarted only as a new job.</span></span> <span data-ttu-id="f0a46-240">El requisito de que el trabajo se reinicie solo como un nuevo trabajo es específico del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-240">The requirement that the job be restarted only as a new job is job specific.</span></span><br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <span data-ttu-id="f0a46-241"><dt>**Eliminado**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-241"><dt>**Killed**</dt> <dt>9</dt></span></span> </dl>                                                   | <span data-ttu-id="f0a46-242">La solicitud de cambio de estado "Kill" detuvo el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-242">The job has been stopped by a "Kill" state change request.</span></span> <span data-ttu-id="f0a46-243">Es posible que los procesos subyacentes sigan en ejecución y que sea necesario realizar una limpieza para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="f0a46-243">Underlying processes may still be running, and a clean-up might be required to free up resources.</span></span><br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <span data-ttu-id="f0a46-244"><dt>**Excepción**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-244"><dt>**Exception**</dt> <dt>10</dt></span></span> </dl>                                      | <span data-ttu-id="f0a46-245">El trabajo está en un estado anómalo que podría ser indicativo de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="f0a46-245">The job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="f0a46-246">El estado real del trabajo podría estar disponible a través de objetos específicos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-246">The actual status of the job might be available through job-specific objects.</span></span><br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <span data-ttu-id="f0a46-247"><dt>**Servicio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-247"><dt>**Service**</dt> <dt>11</dt></span></span> </dl>                                              | <span data-ttu-id="f0a46-248">El trabajo está en un estado específico del proveedor que admite la detección de problemas, la resolución o ambos.</span><span class="sxs-lookup"><span data-stu-id="f0a46-248">The job is in a vendor-specific state that supports problem discovery, or resolution, or both.</span></span><br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="f0a46-249"><dt>**DMTF reservado**</dt> <dt>12 32767</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-249"><dt>**DMTF Reserved**</dt> <dt>12 32767</dt></span></span> </dl>                | <span data-ttu-id="f0a46-250">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f0a46-250">Reserved.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="f0a46-251"><dt> **Proveedor reservado**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-251"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> | <span data-ttu-id="f0a46-252">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f0a46-252">Reserved.</span></span><br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="f0a46-253">**Estado del trabajo**</span><span class="sxs-lookup"><span data-stu-id="f0a46-253">**JobStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-254">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-255">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-256">Cadena que representa el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-256">A string that represents the job status.</span></span> <span data-ttu-id="f0a46-257">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-257">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-258">**JobType**</span><span class="sxs-lookup"><span data-stu-id="f0a46-258">**JobType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-259">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-261">Tipo de operación asincrónica cuyo seguimiento realiza esta instancia de **MSVM \_ StorageJob**.</span><span class="sxs-lookup"><span data-stu-id="f0a46-261">The type of asynchronous operation being tracked by this instance of **Msvm\_StorageJob**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f0a46-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a46-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>

<span data-ttu-id="f0a46-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**Creación de VHD** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a46-263"><span id="VHD_Creation"></span><span id="vhd_creation"></span><span id="VHD_CREATION"></span>**VHD Creation** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f0a46-264">Creación de una imagen de disco duro virtual (VHD).</span><span class="sxs-lookup"><span data-stu-id="f0a46-264">Creating a virtual hard disk (VHD) image.</span></span>

</dd> <dt>

<span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>

<span data-ttu-id="f0a46-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Creación de disquetes** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a46-265"><span id="Floppy_Creation"></span><span id="floppy_creation"></span><span id="FLOPPY_CREATION"></span>**Floppy Creation** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f0a46-266">Creación de una imagen de disquete virtual (VFD).</span><span class="sxs-lookup"><span data-stu-id="f0a46-266">Creating a virtual floppy disk image (VFD).</span></span>

</dd> <dt>

<span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>

<span data-ttu-id="f0a46-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compactación** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a46-267"><span id="Compaction"></span><span id="compaction"></span><span id="COMPACTION"></span>**Compaction** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f0a46-268">Compactar el tamaño de una imagen de VHD.</span><span class="sxs-lookup"><span data-stu-id="f0a46-268">Compacting the size of a VHD image.</span></span>

</dd> <dt>

<span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>

<span data-ttu-id="f0a46-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansión** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a46-269"><span id="Expansion"></span><span id="expansion"></span><span id="EXPANSION"></span>**Expansion** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f0a46-270">Expandir el tamaño de una imagen de VHD.</span><span class="sxs-lookup"><span data-stu-id="f0a46-270">Expanding the size of a VHD image.</span></span>

</dd> <dt>

<span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>

<span data-ttu-id="f0a46-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Combinación** (5)</span><span class="sxs-lookup"><span data-stu-id="f0a46-271"><span id="Merging"></span><span id="merging"></span><span id="MERGING"></span>**Merging** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f0a46-272">Combinación de varias imágenes VHD en una sola imagen.</span><span class="sxs-lookup"><span data-stu-id="f0a46-272">Merging multiple VHD images into a single image.</span></span>

</dd> <dt>

<span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>

<span data-ttu-id="f0a46-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversión** (6)</span><span class="sxs-lookup"><span data-stu-id="f0a46-273"><span id="Conversion"></span><span id="conversion"></span><span id="CONVERSION"></span>**Conversion** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f0a46-274">Convertir el tipo de una imagen de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="f0a46-274">Converting the type of a virtual hard disk image.</span></span>

</dd> <dt>

<span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>

<span data-ttu-id="f0a46-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Montaje de bucle invertido** (7)</span><span class="sxs-lookup"><span data-stu-id="f0a46-275"><span id="Loopback_Mount"></span><span id="loopback_mount"></span><span id="LOOPBACK_MOUNT"></span>**Loopback Mount** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f0a46-276">Montaje del disco duro virtual en la partición primaria</span><span class="sxs-lookup"><span data-stu-id="f0a46-276">Mounting the virtual hard disk on the parent partition</span></span>

</dd> <dt>

<span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>

<span data-ttu-id="f0a46-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Obtención de información de VHD** (8)</span><span class="sxs-lookup"><span data-stu-id="f0a46-277"><span id="Get_VHD_Info"></span><span id="get_vhd_info"></span><span id="GET_VHD_INFO"></span>**Get VHD Info** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f0a46-278">Montaje del VHD en el sistema operativo de administración.</span><span class="sxs-lookup"><span data-stu-id="f0a46-278">Mounting the VHD on the management operating system.</span></span>

</dd> <dt>

<span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>

<span data-ttu-id="f0a46-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validar imagen de VHD** (9)</span><span class="sxs-lookup"><span data-stu-id="f0a46-279"><span id="Validate_VHD_Image"></span><span id="validate_vhd_image"></span><span id="VALIDATE_VHD_IMAGE"></span>**Validate VHD Image** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f0a46-280">**LocalOrUtcTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-280">**LocalOrUtcTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-281">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-282">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-283">Indica si las horas representadas en las propiedades **RunStartInterval** y **UntilTime** representan las horas locales o las horas UTC.</span><span class="sxs-lookup"><span data-stu-id="f0a46-283">Indicates whether the times represented in the **RunStartInterval** and **UntilTime** properties represent local times or UTC times.</span></span> <span data-ttu-id="f0a46-284">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-284">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="f0a46-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Hora local** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a46-285"><span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Local Time** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Hora UTC** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a46-286"><span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**UTC Time** (2 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0a46-287">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f0a46-287">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-288">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-290">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a46-290">The label by which the object is known.</span></span> <span data-ttu-id="f0a46-291">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-292">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="f0a46-292">**Notify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-293">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-294">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-294">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-295">El usuario que recibe una notificación cuando se completa o se produce un error.</span><span class="sxs-lookup"><span data-stu-id="f0a46-295">The user who is notified upon job completion or failure.</span></span> <span data-ttu-id="f0a46-296">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-296">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-297">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="f0a46-297">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-298">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-300">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="f0a46-300">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="f0a46-301">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="f0a46-301">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f0a46-302">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-303">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="f0a46-303">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-304">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-304">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-305">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-306">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="f0a46-306">The current statuses of the object.</span></span> <span data-ttu-id="f0a46-307">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-308">**OtherRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="f0a46-308">**OtherRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-309">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-310">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-311">Una cadena que describe la acción de recuperación cuando la propiedad **RecoveryAction** de la instancia es 1 (otra).</span><span class="sxs-lookup"><span data-stu-id="f0a46-311">A string that describes the recovery action when the **RecoveryAction** property of the instance is 1 (Other).</span></span> <span data-ttu-id="f0a46-312">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-312">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-313">**Propietario**</span><span class="sxs-lookup"><span data-stu-id="f0a46-313">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-314">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-315">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-316">El usuario que envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-316">The user who submitted the job.</span></span> <span data-ttu-id="f0a46-317">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-317">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-318">**Parent**</span><span class="sxs-lookup"><span data-stu-id="f0a46-318">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-319">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-320">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-321">En caso de que se produzca un error en la operación asincrónica, esta propiedad contiene la ruta de acceso al elemento primario del VHD que se ve afectado por esta operación.</span><span class="sxs-lookup"><span data-stu-id="f0a46-321">On failure of the asynchronous operation, this property contains the file path to the parent of the VHD being affected by this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-322">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="f0a46-322">**PercentComplete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-323">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-325">Calificadores: **MinValue** (0), **MaxValue** (100), **unidades** ("porcentaje")</span><span class="sxs-lookup"><span data-stu-id="f0a46-325">Qualifiers: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-326">Porcentaje de finalización del trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-326">The completion percentage of the job.</span></span> <span data-ttu-id="f0a46-327">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-327">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-328">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="f0a46-328">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-329">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-329">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-331">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="f0a46-331">Provides high level status information.</span></span> <span data-ttu-id="f0a46-332">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="f0a46-332">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="f0a46-333">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="f0a46-333">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="f0a46-334">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-335">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="f0a46-335">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-336">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f0a46-336">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-338">La importancia de la ejecución de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-338">The importance of a job's execution.</span></span> <span data-ttu-id="f0a46-339">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-339">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-340">**RecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="f0a46-340">**RecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-341">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f0a46-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-342">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-343">Describe la acción de recuperación que se va a realizar para un trabajo que no se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0a46-343">Describes the recovery action to be taken for a job that did not run successfully.</span></span> <span data-ttu-id="f0a46-344">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-344">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="f0a46-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a46-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a46-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**No continuar** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a46-347"><span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Do Not Continue** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar con el trabajo siguiente** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a46-348"><span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continue With Next Job** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Volver a ejecutar el trabajo** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a46-349"><span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Re-run Job** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Ejecutar trabajo de recuperación** (5)</span><span class="sxs-lookup"><span data-stu-id="f0a46-350"><span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Run Recovery Job** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0a46-351">**RunDay**</span><span class="sxs-lookup"><span data-stu-id="f0a46-351">**RunDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-352">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f0a46-352">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-353">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-354">Calificadores: **MinValue** (-31), **MaxValue** (31)</span><span class="sxs-lookup"><span data-stu-id="f0a46-354">Qualifiers: **MinValue** ( -31 ), **MaxValue** ( 31 )</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-355">Día del mes en el que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-355">The day of the month on which the job should be processed.</span></span> <span data-ttu-id="f0a46-356">Hay distintas interpretaciones para esta propiedad, dependiendo del valor de **RunDayOfWeek**.</span><span class="sxs-lookup"><span data-stu-id="f0a46-356">There are different interpretations for this property, depending on the value of **RunDayOfWeek**.</span></span>

<span data-ttu-id="f0a46-357">Cuando **RunDayOfWeek** es 0 y **RunDay** es positivo, **RunDay** define el día del mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-357">When **RunDayOfWeek** is 0 and **RunDay** is positive, **RunDay** defines the day of the month on which the job is processed.</span></span> <span data-ttu-id="f0a46-358">Por ejemplo, si **RunDayOfWeek** es 0 y **RunDay** es 12, el trabajo se procesará <sup>el día 12</sup> del mes.</span><span class="sxs-lookup"><span data-stu-id="f0a46-358">For example, if **RunDayOfWeek** is 0 and **RunDay** is 12, then the job will be processed on the 12<sup>th</sup> day of the month.</span></span>

<span data-ttu-id="f0a46-359">Cuando **RunDayOfWeek** es 0 y **RunDay** es negativo, **RunDay** define el número de días antes del último día del mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-359">When **RunDayOfWeek** is 0 and **RunDay** is negative, **RunDay** defines the number of days before the last day of the month on which the job is processed.</span></span>  <span data-ttu-id="f0a46-360">1 indica el último día del mes, 2 indica un día antes del último día del mes, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f0a46-360">1 indicates the last day of the month,  2 indicates one day before the last day of the month, and so on.</span></span> <span data-ttu-id="f0a46-361">Por ejemplo, si **RunDayOfWeek** es 0 y **RunDay** es 1, el trabajo se procesará el último día del mes.</span><span class="sxs-lookup"><span data-stu-id="f0a46-361">For example, if **RunDayOfWeek** is 0 and **RunDay** is  1, then the job will be processed on the last day of the month.</span></span>

<span data-ttu-id="f0a46-362">Cuando **RunDayOfWeek** no es 0, **RunDayOfWeek** es el día de la semana en el que se procesará el trabajo, en relación con **RunDay**.</span><span class="sxs-lookup"><span data-stu-id="f0a46-362">When **RunDayOfWeek** is not 0, **RunDayOfWeek** is the day of the week that the job will be processed, relative to **RunDay**.</span></span> <span data-ttu-id="f0a46-363">Por ejemplo, si **RunDay** es 15 y **RunDayOfWeek** es 7 (+ sábado), el trabajo se procesará el primer sábado en o después <sup>del día 15</sup> del mes.</span><span class="sxs-lookup"><span data-stu-id="f0a46-363">For example, if **RunDay** is 15 and **RunDayOfWeek** is 7 (+Saturday), the job will be processed on the first Saturday on or after the 15<sup>th</sup> day of the month.</span></span> <span data-ttu-id="f0a46-364">Si el **RunDay** es 20 y el de **RunDayOfWeek** es 7 (sábado), el trabajo se procesará el primer sábado en <sup>el día del</sup> mes o antes del mismo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-364">If **RunDay** is 20 and **RunDayOfWeek** is  7 ( Saturday), the job will be processed on the first Saturday on or before the 20<sup>th</sup> day of the month.</span></span> <span data-ttu-id="f0a46-365">Si **RunDay** es 1 y **RunDayOfWeek** es 1 (domingo), el trabajo se procesará el último domingo del mes.</span><span class="sxs-lookup"><span data-stu-id="f0a46-365">If **RunDay** is  1 and **RunDayOfWeek** is  1 ( Sunday), then the job will be processed on the last Sunday of the month.</span></span>

<span data-ttu-id="f0a46-366">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-366">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-367">**RunDayOfWeek**</span><span class="sxs-lookup"><span data-stu-id="f0a46-367">**RunDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-368">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="f0a46-368">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-370">Entero positivo o negativo que se usa junto con **RunDay** para indicar el día de la semana o el mes en el que se procesa el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-370">A positive or negative integer used in conjunction with **RunDay** to indicate the day of the week or month on which the job is processed.</span></span> <span data-ttu-id="f0a46-371">Vea la descripción de la propiedad **RunDay** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f0a46-371">See the description of the **RunDay** property for more information.</span></span> <span data-ttu-id="f0a46-372">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-372">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="f0a46-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="f0a46-373"><span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Viernes** (6)</span><span class="sxs-lookup"><span data-stu-id="f0a46-374"><span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Jueves** (5)</span><span class="sxs-lookup"><span data-stu-id="f0a46-375"><span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a46-376"><span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Martes** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a46-377"><span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lunes** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a46-378"><span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a46-379"><span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a46-380"><span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domingo** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a46-381"><span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Sunday** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lunes** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a46-382"><span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Monday** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Martes** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a46-383"><span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Tuesday** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Miércoles** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a46-384"><span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Wednesday** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Jueves** (5)</span><span class="sxs-lookup"><span data-stu-id="f0a46-385"><span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Thursday** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Viernes** (6)</span><span class="sxs-lookup"><span data-stu-id="f0a46-386"><span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Friday** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sábado** (7)</span><span class="sxs-lookup"><span data-stu-id="f0a46-387"><span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Saturday** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0a46-388">**RunMonth**</span><span class="sxs-lookup"><span data-stu-id="f0a46-388">**RunMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-389">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f0a46-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-391">Mes en el que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-391">The month during which the job should be processed.</span></span> <span data-ttu-id="f0a46-392">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-392">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

<dl> <dt>

<span data-ttu-id="f0a46-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Enero** (0)</span><span class="sxs-lookup"><span data-stu-id="f0a46-393"><span id="January"></span><span id="january"></span><span id="JANUARY"></span>**January** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Febrero** (1)</span><span class="sxs-lookup"><span data-stu-id="f0a46-394"><span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**February** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**Marzo** (2)</span><span class="sxs-lookup"><span data-stu-id="f0a46-395"><span id="March"></span><span id="march"></span><span id="MARCH"></span>**March** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**Abril** (3)</span><span class="sxs-lookup"><span data-stu-id="f0a46-396"><span id="April"></span><span id="april"></span><span id="APRIL"></span>**April** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**Mayo** (4)</span><span class="sxs-lookup"><span data-stu-id="f0a46-397"><span id="May"></span><span id="may"></span><span id="MAY"></span>**May** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**Junio** (5)</span><span class="sxs-lookup"><span data-stu-id="f0a46-398"><span id="June"></span><span id="june"></span><span id="JUNE"></span>**June** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**Julio** (6)</span><span class="sxs-lookup"><span data-stu-id="f0a46-399"><span id="July"></span><span id="july"></span><span id="JULY"></span>**July** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)</span><span class="sxs-lookup"><span data-stu-id="f0a46-400"><span id="August"></span><span id="august"></span><span id="AUGUST"></span>**August** (7)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Septiembre** (8)</span><span class="sxs-lookup"><span data-stu-id="f0a46-401"><span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**September** (8)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Octubre** (9)</span><span class="sxs-lookup"><span data-stu-id="f0a46-402"><span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**October** (9)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Noviembre** (10)</span><span class="sxs-lookup"><span data-stu-id="f0a46-403"><span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**November** (10)</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Diciembre** (11)</span><span class="sxs-lookup"><span data-stu-id="f0a46-404"><span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**December** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0a46-405">**RunStartInterval**</span><span class="sxs-lookup"><span data-stu-id="f0a46-405">**RunStartInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-406">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-408">El intervalo de tiempo después de medianoche en el momento en que se debe procesar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-408">The time interval after midnight when the job should be processed.</span></span> <span data-ttu-id="f0a46-409">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-409">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-410">**ScheduledStartTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-410">**ScheduledStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-411">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-411">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-413">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-413">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-414">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-414">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-415">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-415">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-416">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-417">La hora a la que comenzó el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-417">The time that the job began.</span></span> <span data-ttu-id="f0a46-418">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-418">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-419">**Estado**</span><span class="sxs-lookup"><span data-stu-id="f0a46-419">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-420">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0a46-420">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-421">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-422">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="f0a46-422">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-423">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f0a46-423">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-424">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f0a46-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-426">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="f0a46-426">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="f0a46-427">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="f0a46-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-428">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="f0a46-428">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-429">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-431">Cantidad de tiempo, en minutos, que el trabajo se conserva una vez finalizada la ejecución, ya sea correctamente o con errores en esa ejecución.</span><span class="sxs-lookup"><span data-stu-id="f0a46-431">The amount of time, in minutes, that the job is retained after it has finished executing, either succeeding or failing in that execution.</span></span> <span data-ttu-id="f0a46-432">El trabajo debe permanecer en vigor durante un período de tiempo, independientemente del valor de la propiedad **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="f0a46-432">The job must remain in existence for some period of time regardless of the value of the **DeleteOnCompletion** property.</span></span> <span data-ttu-id="f0a46-433">El valor predeterminado es cinco minutos.</span><span class="sxs-lookup"><span data-stu-id="f0a46-433">The default is five minutes.</span></span> <span data-ttu-id="f0a46-434">Esta propiedad se hereda de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))y siempre está establecida en 00000000000500.000000:000.</span><span class="sxs-lookup"><span data-stu-id="f0a46-434">This property is inherited from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)), and it is always set to 00000000000500.000000:000.</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-435">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="f0a46-435">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-436">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-436">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-437">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-438">La hora a la que se modificó por última vez el estado de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f0a46-438">The time at which the virtual machine's state was last modified.</span></span> <span data-ttu-id="f0a46-439">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f0a46-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-440">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="f0a46-440">**TimeSubmitted**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-441">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-441">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-442">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-443">La hora a la que se envió el trabajo.</span><span class="sxs-lookup"><span data-stu-id="f0a46-443">The time that the job was submitted.</span></span> <span data-ttu-id="f0a46-444">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-444">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> <dt>

<span data-ttu-id="f0a46-445">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-445">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0a46-446">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f0a46-446">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f0a46-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0a46-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f0a46-448">Hora a la que el trabajo no es válido o se debe detener.</span><span class="sxs-lookup"><span data-stu-id="f0a46-448">The time at which the job is not valid or should be stopped.</span></span> <span data-ttu-id="f0a46-449">Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).</span><span class="sxs-lookup"><span data-stu-id="f0a46-449">This property is inherited from [**CIM\_Job**](/windows/desktop/CIMWin32Prov/cim-job).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0a46-450">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0a46-450">Remarks</span></span>

<span data-ttu-id="f0a46-451">El acceso a la clase **MSVM \_ StorageJob** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="f0a46-451">Access to the **Msvm\_StorageJob** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f0a46-452">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f0a46-452">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0a46-453">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0a46-453">Requirements</span></span>



| <span data-ttu-id="f0a46-454">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0a46-454">Requirement</span></span> | <span data-ttu-id="f0a46-455">Value</span><span class="sxs-lookup"><span data-stu-id="f0a46-455">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0a46-456">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0a46-456">Minimum supported client</span></span><br/> | <span data-ttu-id="f0a46-457">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0a46-457">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f0a46-458">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0a46-458">Minimum supported server</span></span><br/> | <span data-ttu-id="f0a46-459">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0a46-459">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0a46-460">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0a46-460">Namespace</span></span><br/>                | <span data-ttu-id="f0a46-461">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f0a46-461">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f0a46-462">MOF</span><span class="sxs-lookup"><span data-stu-id="f0a46-462">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0a46-463"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-463"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0a46-464">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0a46-464">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0a46-465"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f0a46-465"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f0a46-466">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0a46-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0a46-467">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="f0a46-467">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> <dt>

<span data-ttu-id="f0a46-468">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f0a46-468">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f0a46-469">Clases de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="f0a46-469">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

