---
description: 'Más información acerca de: JetEscrowUpdate (función)'
title: Función JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706889"
---
# <a name="jetescrowupdate-function"></a><span data-ttu-id="e19df-103">Función JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="e19df-103">JetEscrowUpdate Function</span></span>


<span data-ttu-id="e19df-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e19df-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetescrowupdate-function"></a><span data-ttu-id="e19df-105">Función JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="e19df-105">JetEscrowUpdate Function</span></span>

<span data-ttu-id="e19df-106">La función **JetEscrowUpdate** realiza una operación de suma atómica en una columna.</span><span class="sxs-lookup"><span data-stu-id="e19df-106">The **JetEscrowUpdate** function performs an atomic addition operation on one column.</span></span> <span data-ttu-id="e19df-107">Esta función permite que varias sesiones actualicen el mismo registro simultáneamente sin conflictos.</span><span class="sxs-lookup"><span data-stu-id="e19df-107">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e19df-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e19df-108">Parameters</span></span>

<span data-ttu-id="e19df-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e19df-109">*sesid*</span></span>

<span data-ttu-id="e19df-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e19df-110">The session to use for this call.</span></span>

<span data-ttu-id="e19df-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="e19df-111">*tableid*</span></span>

<span data-ttu-id="e19df-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e19df-112">The cursor to use for this call.</span></span>

<span data-ttu-id="e19df-113">*columnid*</span><span class="sxs-lookup"><span data-stu-id="e19df-113">*columnid*</span></span>

<span data-ttu-id="e19df-114">*Columnid* de la columna que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="e19df-114">The *columnid* of the column to be updated.</span></span>

<span data-ttu-id="e19df-115">*FV*</span><span class="sxs-lookup"><span data-stu-id="e19df-115">*pv*</span></span>

<span data-ttu-id="e19df-116">Un puntero a un búfer que contiene el addend de la columna.</span><span class="sxs-lookup"><span data-stu-id="e19df-116">A pointer to a buffer containing the addend for the column.</span></span>

<span data-ttu-id="e19df-117">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="e19df-117">*cbMax*</span></span>

<span data-ttu-id="e19df-118">Tamaño del búfer que contiene el addend.</span><span class="sxs-lookup"><span data-stu-id="e19df-118">The size of the buffer containing the addend.</span></span>

<span data-ttu-id="e19df-119">*pvOld*</span><span class="sxs-lookup"><span data-stu-id="e19df-119">*pvOld*</span></span>

<span data-ttu-id="e19df-120">Búfer de salida que recibirá el valor actual de la columna tal y como se almacena en la base de datos (se omite el control de versiones).</span><span class="sxs-lookup"><span data-stu-id="e19df-120">The output buffer that will receive the current value of the column as stored in the database (versioning is ignored).</span></span>

<span data-ttu-id="e19df-121">*cbOldMax*</span><span class="sxs-lookup"><span data-stu-id="e19df-121">*cbOldMax*</span></span>

<span data-ttu-id="e19df-122">Tamaño máximo del búfer de salida que recibirá el valor actual de la columna.</span><span class="sxs-lookup"><span data-stu-id="e19df-122">The maximum size of the output buffer that will receive the current value of the column.</span></span> <span data-ttu-id="e19df-123">Actualmente solo se admite JET_coltypLong, por lo que el búfer debe tener 4 bytes o tener una longitud de 0 bytes.</span><span class="sxs-lookup"><span data-stu-id="e19df-123">Currently only JET_coltypLong is supported, so the buffer must either be 4 bytes or 0 bytes in length.</span></span> <span data-ttu-id="e19df-124">Si *pvOld* es null, *cbOldMax* debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="e19df-124">If *pvOld* is NULL then *cbOldMax* should be 0.</span></span>

<span data-ttu-id="e19df-125">*pcbOldActual*</span><span class="sxs-lookup"><span data-stu-id="e19df-125">*pcbOldActual*</span></span>

<span data-ttu-id="e19df-126">Recibe la cantidad real de datos de valor sin formato recibidos en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="e19df-126">Receives the actual amount of raw value data received in the output buffer.</span></span>

<span data-ttu-id="e19df-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e19df-127">*grbit*</span></span>

<span data-ttu-id="e19df-128">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="e19df-128">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e19df-129">Value</span><span class="sxs-lookup"><span data-stu-id="e19df-129">Value</span></span></p></th>
<th><p><span data-ttu-id="e19df-130">Significado</span><span class="sxs-lookup"><span data-stu-id="e19df-130">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e19df-131">JET_bitEscrowNoRollback</span><span class="sxs-lookup"><span data-stu-id="e19df-131">JET_bitEscrowNoRollback</span></span></p></td>
<td><p><span data-ttu-id="e19df-132">Incluso si la sesión que realiza la actualización de custodia tiene la reversión de la transacción, esta actualización no se deshará.</span><span class="sxs-lookup"><span data-stu-id="e19df-132">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="e19df-133">Tenga en cuenta que, dado que es posible que las entradas de registro no se vacíen en el disco, es posible que se pierdan actualizaciones recientes de custodia realizadas con esta marca si se produce un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="e19df-133">Note that as the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e19df-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e19df-134">Return Value</span></span>

<span data-ttu-id="e19df-135">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="e19df-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e19df-136">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e19df-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e19df-137">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e19df-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="e19df-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="e19df-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e19df-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e19df-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e19df-140">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e19df-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-141">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="e19df-141">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="e19df-142">El cursor tiene una actualización preparada con <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span><span class="sxs-lookup"><span data-stu-id="e19df-142">The cursor has an update prepared with <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-143">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e19df-143">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e19df-144">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e19df-144">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-145">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e19df-145">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e19df-146">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="e19df-146">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e19df-147">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e19df-147">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-148">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="e19df-148">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="e19df-149">Se ha pasado un tamaño de búfer no válido.</span><span class="sxs-lookup"><span data-stu-id="e19df-149">An invalid buffer size has been passed in.</span></span> <span data-ttu-id="e19df-150">Actualmente solo se admite JET_coltypLong, por lo que el búfer debe ser de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="e19df-150">Currently only JET_coltypLong is supported, so the buffer must be 4 bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="e19df-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="e19df-152">Se ha especificado una columna no válida.</span><span class="sxs-lookup"><span data-stu-id="e19df-152">An invalid column has been specified.</span></span> <span data-ttu-id="e19df-153">La columna se debe crear con JET_bitColumnEscrowUpdate especificado.</span><span class="sxs-lookup"><span data-stu-id="e19df-153">The column must be created with JET_bitColumnEscrowUpdate specified.</span></span> <span data-ttu-id="e19df-154">Solo las columnas fijas de JET_coltypLong pueden especificarse como de actualización de custodia.</span><span class="sxs-lookup"><span data-stu-id="e19df-154">Only fixed columns of JET_coltypLong can be specified as escrow updateable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="e19df-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="e19df-156">El cursor debe estar en un registro para actualizar una columna.</span><span class="sxs-lookup"><span data-stu-id="e19df-156">Cursor must be on a record in order to update a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-157">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="e19df-157">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="e19df-158">Las actualizaciones de custodia solo las pueden realizar sesiones en una transacción.</span><span class="sxs-lookup"><span data-stu-id="e19df-158">Escrow updates can only be performed by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e19df-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e19df-160">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e19df-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-161">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="e19df-161">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="e19df-162">El cursor no puede ser de solo lectura y actualizar un registro.</span><span class="sxs-lookup"><span data-stu-id="e19df-162">Cursor cannot be read only and update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-163">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e19df-163">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e19df-164">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e19df-164">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-165">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e19df-165">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e19df-166">No se puede usar la misma sesión desde más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e19df-166">The same session cannot be used from more than one thread at the same time.</span></span> <span data-ttu-id="e19df-167">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e19df-167">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-168">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e19df-168">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e19df-169">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e19df-169">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-170">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="e19df-170">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e19df-171">La sesión debe tener permisos de escritura para actualizar un registro.</span><span class="sxs-lookup"><span data-stu-id="e19df-171">Session must have write permissions to update a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-172">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-172">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e19df-173">El error devuelto cuando se solicita una actualización en conflicto.</span><span class="sxs-lookup"><span data-stu-id="e19df-173">The error returned when a conflicting update is requested.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="e19df-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e19df-174">Remarks</span></span>

<span data-ttu-id="e19df-175">Normalmente, si dos sesiones intentan actualizar un registro simultáneamente, la segunda sesión recibirá un error JET_errWriteConflict a menos que las sesiones se serialicen por completo.</span><span class="sxs-lookup"><span data-stu-id="e19df-175">Normally, if two sessions attempt to update a record simultaneously, the second session will receive a JET_errWriteConflict error unless the sessions are completely serialized.</span></span> <span data-ttu-id="e19df-176">Para serializar dos sesiones que actualizan el mismo registro, la segunda sesión debe iniciar su transacción después de que la primera transacción confirme su transacción.</span><span class="sxs-lookup"><span data-stu-id="e19df-176">To serialize two sessions that update the same record, the second session must start its transaction after the first transaction commits its transaction.</span></span> <span data-ttu-id="e19df-177">Vea [JetBeginTransaction](./jetbegintransaction-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e19df-177">See [JetBeginTransaction](./jetbegintransaction-function.md) for more information.</span></span>

<span data-ttu-id="e19df-178">Se pueden actualizar varias columnas en el mismo registro.</span><span class="sxs-lookup"><span data-stu-id="e19df-178">Multiple columns in the same record can be escrow updated.</span></span> <span data-ttu-id="e19df-179">Las actualizaciones no se ven afectadas.</span><span class="sxs-lookup"><span data-stu-id="e19df-179">The updates do not affect each other.</span></span>

<span data-ttu-id="e19df-180">Solo las operaciones **JetEscrowUpdate** son compatibles entre sí.</span><span class="sxs-lookup"><span data-stu-id="e19df-180">Only **JetEscrowUpdate** operations are compatible with each other.</span></span> <span data-ttu-id="e19df-181">Si dos sesiones diferentes intentan preparar las actualizaciones o eliminar el mismo registro, se generará un conflicto de escritura.</span><span class="sxs-lookup"><span data-stu-id="e19df-181">If two different sessions try to prepare updates or delete the same record, a write conflict will be generated.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p><span data-ttu-id="e19df-182">Sesión B</span><span class="sxs-lookup"><span data-stu-id="e19df-182">Session B</span></span><br /><span data-ttu-id="e19df-183">
<strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="e19df-183">
<strong>JetEscrowUpdate</strong></span></span></p></th>
<th><p><span data-ttu-id="e19df-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span><span class="sxs-lookup"><span data-stu-id="e19df-184"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a></span></span></p></th>
<th><p><span data-ttu-id="e19df-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="e19df-185"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="e19df-186"><strong>JetEscrowUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="e19df-186"><strong>JetEscrowUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="e19df-187">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e19df-187">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e19df-188">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-188">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e19df-189">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-189">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="e19df-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span><span class="sxs-lookup"><span data-stu-id="e19df-190"><a href="gg269288(v=exchg.10).md">JetUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="e19df-191">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-191">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e19df-192">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-192">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e19df-193">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-193">JET_errWriteConflict</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-194">Sesión A</span><span class="sxs-lookup"><span data-stu-id="e19df-194">Session A</span></span></p></td>
<td><p><span data-ttu-id="e19df-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span><span class="sxs-lookup"><span data-stu-id="e19df-195"><a href="gg269315(v=exchg.10).md">JetDelete</a></span></span></p></td>
<td><p><span data-ttu-id="e19df-196">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-196">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e19df-197">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-197">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e19df-198">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e19df-198">JET_errWriteConflict</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e19df-199">Las versiones de las operaciones de custodia se controlan y se deshacen con [JetRollback](./jetrollback-function.md) (a menos que se especifique JET_bitEscrowNoRollback).</span><span class="sxs-lookup"><span data-stu-id="e19df-199">Escrow operations are versioned and are undone using [JetRollback](./jetrollback-function.md) (unless JET_bitEscrowNoRollback was specified).</span></span> <span data-ttu-id="e19df-200">**JetEscrowUpdate** devuelve el valor sin formato de la columna almacenada en la base de datos, porque una aplicación puede querer realizar una acción especial cuando se alcanza un valor de centinela.</span><span class="sxs-lookup"><span data-stu-id="e19df-200">**JetEscrowUpdate** returns the raw value of the column stored in the database, because an application may want to perform a special action when a sentinel value is hit.</span></span> <span data-ttu-id="e19df-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) devuelve la vista con versión correcta de la columna, omitiendo las actualizaciones realizadas por las sesiones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="e19df-201">[JetRetrieveColumn](./jetretrievecolumn-function.md) returns the correctly versioned view of the column, ignoring updates made by concurrent sessions.</span></span>

<span data-ttu-id="e19df-202">Dadas dos sesiones que operan en la misma columna del mismo registro, podemos ver cómo funciona esto.</span><span class="sxs-lookup"><span data-stu-id="e19df-202">Given two sessions operating on the same column of the same record, we can see how this works.</span></span> <span data-ttu-id="e19df-203">Suponga que la columna comienza con un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="e19df-203">Assume the column starts with a value of 0.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e19df-204">Sesión</span><span class="sxs-lookup"><span data-stu-id="e19df-204">Session</span></span></p></th>
<th><p><span data-ttu-id="e19df-205">Operación</span><span class="sxs-lookup"><span data-stu-id="e19df-205">Operation</span></span></p></th>
<th><p><span data-ttu-id="e19df-206">Valor almacenado</span><span class="sxs-lookup"><span data-stu-id="e19df-206">Stored value</span></span></p></th>
<th><p><span data-ttu-id="e19df-207">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e19df-207">Returned value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e19df-208">A</span><span class="sxs-lookup"><span data-stu-id="e19df-208">A</span></span></p></td>
<td><p><span data-ttu-id="e19df-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="e19df-209"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-210">A</span><span class="sxs-lookup"><span data-stu-id="e19df-210">A</span></span></p></td>
<td><p><span data-ttu-id="e19df-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span><span class="sxs-lookup"><span data-stu-id="e19df-211"><a href="gg294083(v=exchg.10).md">JetBeginTransation</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e19df-212">0</span><span class="sxs-lookup"><span data-stu-id="e19df-212">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-213">A</span><span class="sxs-lookup"><span data-stu-id="e19df-213">A</span></span></p></td>
<td><p><span data-ttu-id="e19df-214"><strong>JetEscrowUpdate</strong> (4)</span><span class="sxs-lookup"><span data-stu-id="e19df-214"><strong>JetEscrowUpdate</strong> (4)</span></span></p></td>
<td><p><span data-ttu-id="e19df-215">4</span><span class="sxs-lookup"><span data-stu-id="e19df-215">4</span></span></p></td>
<td><p><span data-ttu-id="e19df-216">0</span><span class="sxs-lookup"><span data-stu-id="e19df-216">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-217">A</span><span class="sxs-lookup"><span data-stu-id="e19df-217">A</span></span></p></td>
<td><p><span data-ttu-id="e19df-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="e19df-218"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e19df-219">4</span><span class="sxs-lookup"><span data-stu-id="e19df-219">4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-220">B</span><span class="sxs-lookup"><span data-stu-id="e19df-220">B</span></span></p></td>
<td><p><span data-ttu-id="e19df-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span><span class="sxs-lookup"><span data-stu-id="e19df-221"><a href="gg294083(v=exchg.10).md">JetBeginTransaction</a></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-222">B</span><span class="sxs-lookup"><span data-stu-id="e19df-222">B</span></span></p></td>
<td><p><span data-ttu-id="e19df-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="e19df-223"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e19df-224">0</span><span class="sxs-lookup"><span data-stu-id="e19df-224">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-225">B</span><span class="sxs-lookup"><span data-stu-id="e19df-225">B</span></span></p></td>
<td><p><span data-ttu-id="e19df-226"><strong>JetEscrowUpdate</strong> (3)</span><span class="sxs-lookup"><span data-stu-id="e19df-226"><strong>JetEscrowUpdate</strong> (3)</span></span></p></td>
<td><p><span data-ttu-id="e19df-227">7</span><span class="sxs-lookup"><span data-stu-id="e19df-227">7</span></span></p></td>
<td><p><span data-ttu-id="e19df-228">4</span><span class="sxs-lookup"><span data-stu-id="e19df-228">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-229">B</span><span class="sxs-lookup"><span data-stu-id="e19df-229">B</span></span></p></td>
<td><p><span data-ttu-id="e19df-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="e19df-230"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e19df-231">3</span><span class="sxs-lookup"><span data-stu-id="e19df-231">3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-232">A</span><span class="sxs-lookup"><span data-stu-id="e19df-232">A</span></span></p></td>
<td><p><span data-ttu-id="e19df-233"><strong>JetEscrowUpdate</strong> (2)</span><span class="sxs-lookup"><span data-stu-id="e19df-233"><strong>JetEscrowUpdate</strong> (2)</span></span></p></td>
<td><p><span data-ttu-id="e19df-234">9</span><span class="sxs-lookup"><span data-stu-id="e19df-234">9</span></span></p></td>
<td><p><span data-ttu-id="e19df-235">7</span><span class="sxs-lookup"><span data-stu-id="e19df-235">7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-236">A</span><span class="sxs-lookup"><span data-stu-id="e19df-236">A</span></span></p></td>
<td><p><span data-ttu-id="e19df-237"><strong>JetEscrowUpdate</strong> (-7)</span><span class="sxs-lookup"><span data-stu-id="e19df-237"><strong>JetEscrowUpdate</strong> (-7)</span></span></p></td>
<td><p><span data-ttu-id="e19df-238">2</span><span class="sxs-lookup"><span data-stu-id="e19df-238">2</span></span></p></td>
<td><p><span data-ttu-id="e19df-239">9</span><span class="sxs-lookup"><span data-stu-id="e19df-239">9</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-240">N</span><span class="sxs-lookup"><span data-stu-id="e19df-240">B</span></span></p></td>
<td><p><span data-ttu-id="e19df-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="e19df-241"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e19df-242">3</span><span class="sxs-lookup"><span data-stu-id="e19df-242">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-243">A</span><span class="sxs-lookup"><span data-stu-id="e19df-243">A</span></span></p></td>
<td><p><span data-ttu-id="e19df-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="e19df-244"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e19df-245">-1</span><span class="sxs-lookup"><span data-stu-id="e19df-245">-1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-246">B</span><span class="sxs-lookup"><span data-stu-id="e19df-246">B</span></span></p></td>
<td><p><span data-ttu-id="e19df-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span><span class="sxs-lookup"><span data-stu-id="e19df-247"><a href="gg269273(v=exchg.10).md">JetRollback</a></span></span></p></td>
<td><p><span data-ttu-id="e19df-248">-1</span><span class="sxs-lookup"><span data-stu-id="e19df-248">-1</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-249">A</span><span class="sxs-lookup"><span data-stu-id="e19df-249">A</span></span></p></td>
<td><p><span data-ttu-id="e19df-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span><span class="sxs-lookup"><span data-stu-id="e19df-250"><a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="e19df-251">-1</span><span class="sxs-lookup"><span data-stu-id="e19df-251">-1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e19df-252">No se recomienda reemplazar un registro de la misma transacción que realiza actualizaciones de custodia a un registro.</span><span class="sxs-lookup"><span data-stu-id="e19df-252">Replacing a record in the same transaction that performs escrow updates to a record is not recommended.</span></span> <span data-ttu-id="e19df-253">En concreto, si se prepara una actualización en un registro con una [JET_TABLEID](./jet-tableid.md) y se usa otro [JET_TABLEID](./jet-tableid.md) para la custodia de la actualización del registro, se perderá el custodia actualizado cuando se llame a [JetUpdate](./jetupdate-function.md) .</span><span class="sxs-lookup"><span data-stu-id="e19df-253">In particular, if an update on a record is prepared with one [JET_TABLEID](./jet-tableid.md) and a different [JET_TABLEID](./jet-tableid.md) is used to escrow update the record then the escrow updated will be lost when [JetUpdate](./jetupdate-function.md) is called.</span></span> <span data-ttu-id="e19df-254">Esto sucede incluso si la columna custodia no se estableció durante la actualización.</span><span class="sxs-lookup"><span data-stu-id="e19df-254">This happens even if the escrow column was not set during the update.</span></span>

<span data-ttu-id="e19df-255">Cuando una columna actualizable de custodia tiene un valor de cero, se puede desencadenar un comportamiento especial.</span><span class="sxs-lookup"><span data-stu-id="e19df-255">When an escrow updateable column has a value of zero, special behavior can be triggered.</span></span> <span data-ttu-id="e19df-256">Este comportamiento solo se produce si una operación **JetEscrowUpdate** hace que la columna tenga un valor de cero.</span><span class="sxs-lookup"><span data-stu-id="e19df-256">This behavior only happens if a **JetEscrowUpdate** operation causes the column to have a value of zero.</span></span> <span data-ttu-id="e19df-257">La acción no se realiza inmediatamente, pero se produce una vez después de la transacción que hizo que la columna tenga un valor de cero confirmaciones.</span><span class="sxs-lookup"><span data-stu-id="e19df-257">The action does not happen immediately, but occurs sometime after the transaction which caused the column to have a value of zero commits.</span></span> <span data-ttu-id="e19df-258">La columna debe tener todavía un valor de cero (es decir, si ninguna otra sesión ha modificado la columna).</span><span class="sxs-lookup"><span data-stu-id="e19df-258">The column must still have a value of zero (that is, if no other sessions have modified the column).</span></span> <span data-ttu-id="e19df-259">Si la columna se creó con JET_bitColumnDeleteOnZero, se eliminará el registro que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="e19df-259">If the column was created with JET_bitColumnDeleteOnZero, the record containing the column will be deleted.</span></span> <span data-ttu-id="e19df-260">Si la columna se creó con JET_bitColumnFinalize, se emitirá una devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="e19df-260">If the column was created with JET_bitColumnFinalize then a callback will be issued.</span></span> <span data-ttu-id="e19df-261">Un bloqueo puede hacer que estas acciones no ocurran, pero el mantenimiento en línea (mediante la función [JetDefragment](./jetdefragment-function.md) ) rehará correctamente las acciones.</span><span class="sxs-lookup"><span data-stu-id="e19df-261">A crash may cause these actions not to happen, but online maintenance (using the [JetDefragment](./jetdefragment-function.md) function) will correctly redo the actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e19df-262">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e19df-262">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e19df-263"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e19df-263"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e19df-264">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e19df-264">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-265"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e19df-265"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e19df-266">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e19df-266">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-267"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e19df-267"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e19df-268">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="e19df-268">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e19df-269"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="e19df-269"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e19df-270">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e19df-270">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e19df-271"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e19df-271"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e19df-272">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e19df-272">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e19df-273">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e19df-273">See Also</span></span>

[<span data-ttu-id="e19df-274">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="e19df-274">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="e19df-275">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e19df-275">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e19df-276">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="e19df-276">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="e19df-277">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e19df-277">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e19df-278">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e19df-278">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e19df-279">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="e19df-279">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="e19df-280">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="e19df-280">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="e19df-281">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="e19df-281">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="e19df-282">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="e19df-282">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="e19df-283">JetRollback</span><span class="sxs-lookup"><span data-stu-id="e19df-283">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="e19df-284">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e19df-284">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="e19df-285">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="e19df-285">JetUpdate</span></span>](./jetupdate-function.md)
