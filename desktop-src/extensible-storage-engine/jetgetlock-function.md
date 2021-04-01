---
description: 'Más información acerca de: JetGetLock (función)'
title: JetGetLock función)
TOCTitle: JetGetLock Function
ms:assetid: cebf0789-3d31-4ae8-9b23-dcf5e34e98fc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294094(v=EXCHG.10)
ms:contentKeyID: 32765709
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLock
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5757616214336de25ce30ca49755ac229b10afbe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104157280"
---
# <a name="jetgetlock-function"></a><span data-ttu-id="49d04-103">JetGetLock función)</span><span class="sxs-lookup"><span data-stu-id="49d04-103">JetGetLock Function</span></span>


<span data-ttu-id="49d04-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49d04-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetlock-function"></a><span data-ttu-id="49d04-105">JetGetLock función)</span><span class="sxs-lookup"><span data-stu-id="49d04-105">JetGetLock Function</span></span>

<span data-ttu-id="49d04-106">La función **JetGetLock** proporciona un medio para reservar explícitamente la capacidad de actualizar una fila, un bloqueo de escritura o impedir explícitamente que una fila se actualice en cualquier otra sesión, bloqueo de lectura.</span><span class="sxs-lookup"><span data-stu-id="49d04-106">The **JetGetLock** function provides a means to explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="49d04-107">Normalmente, los bloqueos de escritura de filas se adquieren implícitamente como resultado de la actualización de filas.</span><span class="sxs-lookup"><span data-stu-id="49d04-107">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="49d04-108">Normalmente, los bloqueos de lectura no son necesarios debido a las versiones de registros.</span><span class="sxs-lookup"><span data-stu-id="49d04-108">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="49d04-109">Sin embargo, en algunos casos, una transacción puede desear bloquear explícitamente una fila para aplicar la serialización o asegurarse de que una operación subsiguiente se realizará correctamente en virtud de que ya se han realizado los bloqueos necesarios.</span><span class="sxs-lookup"><span data-stu-id="49d04-109">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed by virtue that required locks have already been taken.</span></span>

```cpp
JET_ERR JET_API JetGetLock(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="49d04-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49d04-110">Parameters</span></span>

<span data-ttu-id="49d04-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="49d04-111">*sesid*</span></span>

<span data-ttu-id="49d04-112">La sesión que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="49d04-112">The session that will be used for this call.</span></span>

<span data-ttu-id="49d04-113">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="49d04-113">*tableid*</span></span>

<span data-ttu-id="49d04-114">Cursor que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="49d04-114">The cursor that will be used for this call.</span></span>

<span data-ttu-id="49d04-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="49d04-115">*grbit*</span></span>

<span data-ttu-id="49d04-116">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="49d04-116">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49d04-117">Value</span><span class="sxs-lookup"><span data-stu-id="49d04-117">Value</span></span></p></th>
<th><p><span data-ttu-id="49d04-118">Significado</span><span class="sxs-lookup"><span data-stu-id="49d04-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49d04-119">JET_bitReadLock</span><span class="sxs-lookup"><span data-stu-id="49d04-119">JET_bitReadLock</span></span></p></td>
<td><p><span data-ttu-id="49d04-120">Esta marca hace que se adquiera un bloqueo de lectura en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="49d04-120">This flag causes a read lock to be acquired on the current record.</span></span> <span data-ttu-id="49d04-121">Los bloqueos de lectura son incompatibles con los bloqueos de escritura que ya se encuentran en otras sesiones, pero son compatibles con los bloqueos de lectura retenidos por otras sesiones.</span><span class="sxs-lookup"><span data-stu-id="49d04-121">Read locks are incompatible with write locks already held by other sessions but are compatible with read locks held by other sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-122">JET_bitWriteLock</span><span class="sxs-lookup"><span data-stu-id="49d04-122">JET_bitWriteLock</span></span></p></td>
<td><p><span data-ttu-id="49d04-123">Esta marca hace que se adquiera un bloqueo de escritura en el registro actual.</span><span class="sxs-lookup"><span data-stu-id="49d04-123">This flag causes a write lock to be acquired on the current record.</span></span> <span data-ttu-id="49d04-124">Los bloqueos de escritura no son compatibles con los bloqueos de lectura o escritura retenidos por otras sesiones, pero son compatibles con los bloqueos de lectura retenidos por la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="49d04-124">Write locks are not compatible with write or read locks held by other sessions but are compatible with read locks held by the same session.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="49d04-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49d04-125">Return Value</span></span>

<span data-ttu-id="49d04-126">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="49d04-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="49d04-127">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="49d04-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49d04-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="49d04-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="49d04-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="49d04-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49d04-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="49d04-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="49d04-131">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="49d04-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="49d04-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="49d04-133">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="49d04-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d04-134">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="49d04-134">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="49d04-135">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="49d04-135">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="49d04-136">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="49d04-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-137">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="49d04-137">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="49d04-138">El <em>grbit</em> determinado no es JET_bitReadLock ni JET_bitWriteLock.</span><span class="sxs-lookup"><span data-stu-id="49d04-138">The given <em>grbit</em> is neither JET_bitReadLock or JET_bitWriteLock.</span></span> <span data-ttu-id="49d04-139">Debe ser una de estas dos marcas.</span><span class="sxs-lookup"><span data-stu-id="49d04-139">It must be one of these two flags.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d04-140">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="49d04-140">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="49d04-141">El cursor debe estar en un registro para adquirir un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="49d04-141">Cursor must be on a record in order to acquire a lock.</span></span> <span data-ttu-id="49d04-142">Los bloqueos están siempre en los registros.</span><span class="sxs-lookup"><span data-stu-id="49d04-142">Locks are always on records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-143">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="49d04-143">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="49d04-144">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="49d04-144">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d04-145">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="49d04-145">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="49d04-146">Solo las sesiones de una transacción pueden adquirir bloqueos.</span><span class="sxs-lookup"><span data-stu-id="49d04-146">Locks can only be acquired by sessions in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-147">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="49d04-147">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="49d04-148">El cursor no puede ser de solo lectura y adquirir un bloqueo de escritura.</span><span class="sxs-lookup"><span data-stu-id="49d04-148">Cursor cannot be read only and acquire a write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d04-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="49d04-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="49d04-150">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="49d04-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-151">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="49d04-151">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="49d04-152">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="49d04-152">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="49d04-153">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="49d04-153">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d04-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="49d04-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="49d04-155">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="49d04-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-156">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="49d04-156">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="49d04-157">La sesión debe tener permisos de escritura para adquirir el bloqueo de escritura.</span><span class="sxs-lookup"><span data-stu-id="49d04-157">Session must have write permissions to acquire write lock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d04-158">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="49d04-158">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="49d04-159">El error devuelto cuando se solicita un bloqueo conflictivo.</span><span class="sxs-lookup"><span data-stu-id="49d04-159">The error returned when a conflicting lock is requested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49d04-160">En caso de éxito, la sesión ha adquirido el bloqueo solicitado.</span><span class="sxs-lookup"><span data-stu-id="49d04-160">On success, session has acquired requested lock.</span></span>

<span data-ttu-id="49d04-161">En caso de error, la sesión no ha adquirido el bloqueo solicitado.</span><span class="sxs-lookup"><span data-stu-id="49d04-161">On failure, session has not acquired requested lock.</span></span>

#### <a name="remarks"></a><span data-ttu-id="49d04-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49d04-162">Remarks</span></span>

<span data-ttu-id="49d04-163">No se pueden adquirir bloqueos de escritura con sesiones o cursores que tengan permisos de solo lectura, aunque la sesión y el cursor no realicen en última instancia una operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="49d04-163">Write locks cannot be acquired with sessions or cursors that have read-only permissions, even if the session and cursor ultimately do not perform an update operation.</span></span> <span data-ttu-id="49d04-164">Tanto la sesión como el cursor deben tener privilegios de escritura para poder adquirir un bloqueo de escritura.</span><span class="sxs-lookup"><span data-stu-id="49d04-164">Both the session and the cursor must have write privileges in order to acquire a write lock.</span></span>

<span data-ttu-id="49d04-165">Los bloqueos de lectura y escritura son un medio de bloqueo pesimista.</span><span class="sxs-lookup"><span data-stu-id="49d04-165">Read and write locks are a means of pessimistic locking.</span></span> <span data-ttu-id="49d04-166">El bloqueo pesimista espera que varias sesiones simultáneas entren en conflicto y adquieran bloqueos de antemano para asegurarse de que sus operaciones se realizan correctamente.</span><span class="sxs-lookup"><span data-stu-id="49d04-166">Pessimistic locking expects multiple concurrent sessions to conflict and acquire locks in advance to ensure that their operations succeed.</span></span>

<span data-ttu-id="49d04-167">La mayoría de las operaciones serán serializables en virtud de los bloqueos tomados implícitamente.</span><span class="sxs-lookup"><span data-stu-id="49d04-167">Most operations will be serializable by virtue of locks implicitly taken.</span></span> <span data-ttu-id="49d04-168">Sin embargo, algunas operaciones no lo serán.</span><span class="sxs-lookup"><span data-stu-id="49d04-168">However, some operations will not.</span></span> <span data-ttu-id="49d04-169">Para ilustrar esto, tenga en cuenta las dos transacciones.</span><span class="sxs-lookup"><span data-stu-id="49d04-169">To illustrate this, consider the two transactions,</span></span>

<span data-ttu-id="49d04-170">T1: R (A), U (B)</span><span class="sxs-lookup"><span data-stu-id="49d04-170">T1 : R(A), U(B)</span></span>

<span data-ttu-id="49d04-171">T2: R (B), U (A)</span><span class="sxs-lookup"><span data-stu-id="49d04-171">T2 : R(B), U(A)</span></span>

<span data-ttu-id="49d04-172">El control de versiones de nivel de registro garantiza que cada transacción cuando se ejecute simultáneamente verá los valores originales de A y B. No hay ningún orden de serie de ejecución que pueda producir los mismos resultados para A y B en caso de que los resultados dependan de los datos leídos.</span><span class="sxs-lookup"><span data-stu-id="49d04-172">Record level versioning will ensure that each transaction when executed concurrently will see the original values for A and B. There is no serial order of execution that could produce the same results for A and B in the case that the results are dependent upon the data read.</span></span> <span data-ttu-id="49d04-173">Para que la aplicación pueda hacer que esta transacción sea serializable, debe adquirir un bloqueo de lectura explícito en y B en cada transacción cuando se lee el valor.</span><span class="sxs-lookup"><span data-stu-id="49d04-173">In order for the application to make this transaction serializable, it should acquire an explicit read lock on A and B in each transaction when the value is read.</span></span>

#### <a name="requirements"></a><span data-ttu-id="49d04-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49d04-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49d04-175"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="49d04-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="49d04-176">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="49d04-176">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-177"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="49d04-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="49d04-178">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="49d04-178">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d04-179"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="49d04-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="49d04-180">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="49d04-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49d04-181"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="49d04-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="49d04-182">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="49d04-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49d04-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="49d04-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="49d04-184">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="49d04-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="49d04-185">Consulte también</span><span class="sxs-lookup"><span data-stu-id="49d04-185">See Also</span></span>

[<span data-ttu-id="49d04-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="49d04-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="49d04-187">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="49d04-187">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="49d04-188">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="49d04-188">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="49d04-189">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="49d04-189">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="49d04-190">JetStopService</span><span class="sxs-lookup"><span data-stu-id="49d04-190">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="49d04-191">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="49d04-191">JetUpdate</span></span>](./jetupdate-function.md)
