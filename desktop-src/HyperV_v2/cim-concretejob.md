---
description: Una versión concreta de la \_ clase de trabajo CIM. Esta clase representa una unidad de trabajo de instancias genéricas que se va a ejecutar, como un lote o un trabajo de impresión.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 949d7c85643919f784a82e7722c9d49a9d9d2e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687046"
---
# <a name="cim_concretejob-class"></a><span data-ttu-id="61bfa-104">\_Clase ConcreteJob de CIM</span><span class="sxs-lookup"><span data-stu-id="61bfa-104">CIM\_ConcreteJob class</span></span>

<span data-ttu-id="61bfa-105">Una versión concreta de la clase de [**\_ trabajo CIM**](cim-job.md) .</span><span class="sxs-lookup"><span data-stu-id="61bfa-105">A concrete version of the [**CIM\_Job**](cim-job.md) class.</span></span> <span data-ttu-id="61bfa-106">Esta clase representa una unidad de trabajo de instancias genéricas que se va a ejecutar, como un lote o un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="61bfa-106">This class represent a generic instantiable unit of work to run, such as a batch or a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="61bfa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61bfa-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a><span data-ttu-id="61bfa-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="61bfa-108">Members</span></span>

<span data-ttu-id="61bfa-109">La clase **CIM \_ ConcreteJob** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="61bfa-109">The **CIM\_ConcreteJob** class has these types of members:</span></span>

-   [<span data-ttu-id="61bfa-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="61bfa-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="61bfa-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61bfa-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="61bfa-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="61bfa-112">Methods</span></span>

<span data-ttu-id="61bfa-113">La clase **CIM \_ ConcreteJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="61bfa-113">The **CIM\_ConcreteJob** class has these methods.</span></span>



| <span data-ttu-id="61bfa-114">Método</span><span class="sxs-lookup"><span data-stu-id="61bfa-114">Method</span></span>                                                           | <span data-ttu-id="61bfa-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="61bfa-115">Description</span></span>                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="61bfa-116">**GetError**</span><span class="sxs-lookup"><span data-stu-id="61bfa-116">**GetError**</span></span>](cim-concretejob-geterror.md)                     | <span data-ttu-id="61bfa-117">Recupera información de error para el estado operativo de un trabajo concreto.</span><span class="sxs-lookup"><span data-stu-id="61bfa-117">Retrieves error information for the operational status of a concrete job.</span></span><br/> |
| [<span data-ttu-id="61bfa-118">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="61bfa-118">**RequestStateChange**</span></span>](cim-concretejob-requeststatechange.md) | <span data-ttu-id="61bfa-119">Solicita el cambio de estado especificado a un trabajo concreto.</span><span class="sxs-lookup"><span data-stu-id="61bfa-119">Requests the specified state change to a concrete job.</span></span><br/>                    |



 

### <a name="properties"></a><span data-ttu-id="61bfa-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61bfa-120">Properties</span></span>

<span data-ttu-id="61bfa-121">La clase **CIM \_ ConcreteJob** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="61bfa-121">The **CIM\_ConcreteJob** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61bfa-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61bfa-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bfa-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="61bfa-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61bfa-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bfa-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bfa-125">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span><span class="sxs-lookup"><span data-stu-id="61bfa-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="61bfa-126">Identifica de forma única y opaca una instancia de esta clase dentro del ámbito del espacio de nombres contenedor.</span><span class="sxs-lookup"><span data-stu-id="61bfa-126">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="61bfa-127">Con el fin de garantizar la unicidad dentro del espacio de nombres, el valor de la propiedad **InstanceID** debe construirse en el patrón siguiente: *OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="61bfa-127">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="61bfa-128">*OrgID* debe incluir un nombre con copyright, marca registrada o de otro tipo que sea propiedad de la entidad empresarial que define el **InstanceID**, o bien un identificador registrado asignado por una entidad global reconocida.</span><span class="sxs-lookup"><span data-stu-id="61bfa-128">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="61bfa-129">Este patrón es similar a la estructura de los nombres de clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="61bfa-129">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="61bfa-130">Además, para garantizar la exclusividad, el primer signo de dos puntos en **InstanceID** debe estar entre el *OrgID* y el *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="61bfa-130">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="61bfa-131">Por lo tanto, el *OrgID* no debe contener un signo de dos puntos (': ').</span><span class="sxs-lookup"><span data-stu-id="61bfa-131">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="61bfa-132">La entidad de negocio elige *LocalID* y no se debe volver a usar para identificar distintos elementos del mundo real subyacentes.</span><span class="sxs-lookup"><span data-stu-id="61bfa-132">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="61bfa-133">Si no se usa el patrón anterior, la entidad de definición debe asegurarse de que el valor **InstanceID** resultante no se vuelva a usar en las propiedades **InstanceID** producidas por este proveedor u otros proveedores para este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="61bfa-133">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="61bfa-134">En el caso de las instancias definidas por el grupo de tareas de administración distribuida (DMTF), el patrón debe usarse con el valor de *OrgID* establecido en CIM.</span><span class="sxs-lookup"><span data-stu-id="61bfa-134">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="61bfa-135">**JobState**</span><span class="sxs-lookup"><span data-stu-id="61bfa-135">**JobState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bfa-136">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61bfa-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61bfa-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bfa-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61bfa-138">El estado operativo del trabajo y la transición entre estos Estados.</span><span class="sxs-lookup"><span data-stu-id="61bfa-138">The operational state of the job, and the transition between those states.</span></span>

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span data-ttu-id="61bfa-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**Nuevo** (2)</span><span class="sxs-lookup"><span data-stu-id="61bfa-139"><span id="New"></span><span id="new"></span><span id="NEW"></span>**New** (2)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-140">nunca se ha iniciado el trabajo.</span><span class="sxs-lookup"><span data-stu-id="61bfa-140">the job has never been started.</span></span>

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="61bfa-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="61bfa-141"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-142">El trabajo se está pasando de los Estados "nuevo", "suspendido" o "servicio" al estado "en ejecución".</span><span class="sxs-lookup"><span data-stu-id="61bfa-142">The job is moving from the 'New', 'Suspended', or 'Service' states into the 'Running' state.</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="61bfa-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (4)</span><span class="sxs-lookup"><span data-stu-id="61bfa-143"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (4)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-144">El trabajo se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="61bfa-144">The Job is running.</span></span>

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="61bfa-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (5)</span><span class="sxs-lookup"><span data-stu-id="61bfa-145"><span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspended** (5)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-146">El trabajo se ha detenido, pero se puede reiniciar sin problemas.</span><span class="sxs-lookup"><span data-stu-id="61bfa-146">The Job is stopped, but can be restarted in a seamless manner.</span></span>

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span data-ttu-id="61bfa-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (6)</span><span class="sxs-lookup"><span data-stu-id="61bfa-147"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (6)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-148">El trabajo se está pasando a un estado "completado", "terminado" o "eliminado".</span><span class="sxs-lookup"><span data-stu-id="61bfa-148">The job is moving to a 'Completed', 'Terminated', or 'Killed' state.</span></span>

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span data-ttu-id="61bfa-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (7)</span><span class="sxs-lookup"><span data-stu-id="61bfa-149"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (7)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-150">El trabajo se ha completado con normalidad.</span><span class="sxs-lookup"><span data-stu-id="61bfa-150">The job has completed normally.</span></span>

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span data-ttu-id="61bfa-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminada** (8)</span><span class="sxs-lookup"><span data-stu-id="61bfa-151"><span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminated** (8)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-152">El trabajo se ha detenido mediante una solicitud de cambio de estado ' Finalizar '.</span><span class="sxs-lookup"><span data-stu-id="61bfa-152">The job has been stopped by a 'Terminate' state change request.</span></span> <span data-ttu-id="61bfa-153">El trabajo y todos sus procesos subyacentes finalizan y se pueden reiniciar (es específico del trabajo) solo como un nuevo trabajo.</span><span class="sxs-lookup"><span data-stu-id="61bfa-153">The job and all its underlying processes are ended and can be restarted (this is job-specific) only as a new job.</span></span>

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span data-ttu-id="61bfa-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Eliminado** (9)</span><span class="sxs-lookup"><span data-stu-id="61bfa-154"><span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Killed** (9)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-155">La solicitud de cambio de estado "Kill" detuvo el trabajo.</span><span class="sxs-lookup"><span data-stu-id="61bfa-155">The job has been stopped by a 'Kill' state change request.</span></span> <span data-ttu-id="61bfa-156">Es posible que los procesos subyacentes hayan dejado de ejecutarse y que sea necesario realizar una limpieza para liberar recursos.</span><span class="sxs-lookup"><span data-stu-id="61bfa-156">Underlying processes might have been left running, and cleanup might be required to free up resources.</span></span>

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span data-ttu-id="61bfa-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Excepción** (10)</span><span class="sxs-lookup"><span data-stu-id="61bfa-157"><span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exception** (10)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-158">El trabajo está en un estado anómalo que podría ser indicativo de una condición de error.</span><span class="sxs-lookup"><span data-stu-id="61bfa-158">The Job is in an abnormal state that might be indicative of an error condition.</span></span> <span data-ttu-id="61bfa-159">El estado real puede mostrarse a través de objetos específicos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="61bfa-159">Actual status might be displayed though job-specific objects.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="61bfa-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio** (11)</span><span class="sxs-lookup"><span data-stu-id="61bfa-160"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (11)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-161">El trabajo está en un estado específico del proveedor que admite la detección de problemas, la resolución o ambos.</span><span class="sxs-lookup"><span data-stu-id="61bfa-161">The Job is in a vendor-specific state that supports problem discovery, or resolution, or both</span></span>

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span data-ttu-id="61bfa-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Consulta pendiente** (12)</span><span class="sxs-lookup"><span data-stu-id="61bfa-162"><span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Query Pending** (12)</span></span>


</dt> <dd>

<span data-ttu-id="61bfa-163">Esperar a que un cliente resuelva una consulta.</span><span class="sxs-lookup"><span data-stu-id="61bfa-163">Waiting for a client to resolve a query.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="61bfa-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (13.. 32767)</span><span class="sxs-lookup"><span data-stu-id="61bfa-164"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (13..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="61bfa-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="61bfa-165"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="61bfa-166">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="61bfa-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bfa-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="61bfa-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61bfa-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bfa-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bfa-169">Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre")</span><span class="sxs-lookup"><span data-stu-id="61bfa-169">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="61bfa-170">Nombre descriptivo de la instancia.</span><span class="sxs-lookup"><span data-stu-id="61bfa-170">The user-friendly name of the instance.</span></span> <span data-ttu-id="61bfa-171">Además, el nombre descriptivo se puede usar como una propiedad para una búsqueda o una consulta.</span><span class="sxs-lookup"><span data-stu-id="61bfa-171">In addition, the user-friendly name can be used as a property for a search or query.</span></span>

> [!Note]  
> <span data-ttu-id="61bfa-172">El nombre no tiene que ser único en el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="61bfa-172">The name does not have to be unique within the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="61bfa-173">**TimeBeforeRemoval**</span><span class="sxs-lookup"><span data-stu-id="61bfa-173">**TimeBeforeRemoval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bfa-174">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61bfa-174">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61bfa-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="61bfa-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="61bfa-176">Calificadores: [ **obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="61bfa-176">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="61bfa-177">Indica cuánto tiempo se conserva un trabajo completado.</span><span class="sxs-lookup"><span data-stu-id="61bfa-177">Indicates how long a completed job is retained.</span></span> <span data-ttu-id="61bfa-178">El valor predeterminado es "00000000000500.000000:000" (cinco minutos).</span><span class="sxs-lookup"><span data-stu-id="61bfa-178">The default value is "00000000000500.000000:000" (five minutes).</span></span>

</dd> <dt>

<span data-ttu-id="61bfa-179">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="61bfa-179">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bfa-180">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61bfa-180">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61bfa-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bfa-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61bfa-182">Fecha u hora en que cambió por última vez el estado del trabajo.</span><span class="sxs-lookup"><span data-stu-id="61bfa-182">The date or time when the state of the job last changed.</span></span>

> [!Note]  
> <span data-ttu-id="61bfa-183">Si el estado del trabajo no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo cero.</span><span class="sxs-lookup"><span data-stu-id="61bfa-183">If the state of the Job has not changed and this property is populated, then it must be set to a zero interval value.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61bfa-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61bfa-184">Requirements</span></span>



| <span data-ttu-id="61bfa-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="61bfa-185">Requirement</span></span> | <span data-ttu-id="61bfa-186">Value</span><span class="sxs-lookup"><span data-stu-id="61bfa-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61bfa-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61bfa-187">Minimum supported client</span></span><br/> | <span data-ttu-id="61bfa-188">Windows 8</span><span class="sxs-lookup"><span data-stu-id="61bfa-188">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="61bfa-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61bfa-189">Minimum supported server</span></span><br/> | <span data-ttu-id="61bfa-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61bfa-190">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="61bfa-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="61bfa-191">Namespace</span></span><br/>                | <span data-ttu-id="61bfa-192">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="61bfa-192">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="61bfa-193">MOF</span><span class="sxs-lookup"><span data-stu-id="61bfa-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61bfa-194"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61bfa-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61bfa-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61bfa-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61bfa-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61bfa-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61bfa-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="61bfa-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61bfa-198">**Trabajo de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="61bfa-198">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

