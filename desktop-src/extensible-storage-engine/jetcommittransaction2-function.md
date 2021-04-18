---
description: 'Más información acerca de: JetCommitTransaction2 (función)'
title: JetCommitTransaction2 función)
TOCTitle: JetCommitTransaction2 Function
ms:assetid: 55b89f8e-7073-4fc2-bf97-103b4bc45e1c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835041(v=EXCHG.10)
ms:contentKeyID: 49894663
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCommitTransaction2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24dfecd091de027f51ed8f69c0441fbc7cbd57af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716964"
---
# <a name="jetcommittransaction2-function"></a><span data-ttu-id="5e55f-103">JetCommitTransaction2 función)</span><span class="sxs-lookup"><span data-stu-id="5e55f-103">JetCommitTransaction2 Function</span></span>


<span data-ttu-id="5e55f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5e55f-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="5e55f-105">La función **JetCommitTransaction2** confirma los cambios realizados en el estado de la base de datos durante el punto de almacenamiento actual y los migra al punto de almacenamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="5e55f-105">The **JetCommitTransaction2** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="5e55f-106">Si se confirma el punto de almacenamiento más externo, los cambios realizados durante ese punto de almacenamiento se confirmarán en el estado de la base de datos y la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-106">If the outermost save point is committed, the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="5e55f-107">La función **JetCommitTransaction2** se presentó en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5e55f-107">The **JetCommitTransaction2** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetCommitTransaction2(
  __in          JET_SESID sesid,
  __in          JET_GRBIT grbit,
  __in          DWORD cmsecDurableCommit,
  __out         JET_COMMIT_ID pCommitID
);
```

### <a name="parameters"></a><span data-ttu-id="5e55f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e55f-108">Parameters</span></span>

<span data-ttu-id="5e55f-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="5e55f-109">*sesid*</span></span>

<span data-ttu-id="5e55f-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="5e55f-110">The session to use for this call.</span></span>

<span data-ttu-id="5e55f-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="5e55f-111">*grbit*</span></span>

<span data-ttu-id="5e55f-112">Grupo de bits que especifica cero o más de los valores enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e55f-112">A group of bits that specify zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e55f-113">Value</span><span class="sxs-lookup"><span data-stu-id="5e55f-113">Value</span></span></p></th>
<th><p><span data-ttu-id="5e55f-114">Significado</span><span class="sxs-lookup"><span data-stu-id="5e55f-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="5e55f-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="5e55f-116">La transacción se confirma normalmente, pero esta API no espera a que la transacción se vacíe en el archivo de registro de transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5e55f-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="5e55f-117">Esto reduce drásticamente la duración de una operación de confirmación a costa de la durabilidad.</span><span class="sxs-lookup"><span data-stu-id="5e55f-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="5e55f-118">Cualquier transacción que no se vacíe en el registro antes de un bloqueo se anulará automáticamente durante la recuperación tras el bloqueo durante la siguiente llamada a la función <a href="gg294068(v=exchg.10).md">JetInit</a> .</span><span class="sxs-lookup"><span data-stu-id="5e55f-118">Any transaction that is not flushed to the log before a crash will automatically be aborted during crash recovery during the next call to the <a href="gg294068(v=exchg.10).md">JetInit</a> function.</span></span></p>
<p><span data-ttu-id="5e55f-119">Si se especifican JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="5e55f-120">Si esta llamada a <strong>JetCommitTransaction2</strong> no coincide con la primera llamada a la función <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para esta sesión, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-120">If this call to <strong>JetCommitTransaction2</strong> does not match the first call to the <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> function for this session, this option is ignored.</span></span> <span data-ttu-id="5e55f-121">Esto se debe a que la acción final que se produce en el punto de almacenamiento más externo es el factor determinante de si toda la transacción se confirma realmente en el disco.</span><span class="sxs-lookup"><span data-stu-id="5e55f-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e55f-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="5e55f-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="5e55f-123">Todas las transacciones confirmadas previamente por cualquier sesión que todavía no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5e55f-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="5e55f-124">Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5e55f-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="5e55f-125">Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="5e55f-126">Esta opción no se puede usar en combinación con ninguna otra opción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="5e55f-127">Esta opción está disponible en las versiones del sistema operativo Windows Server a partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5e55f-127">This option is available in versions of the Windows Server operating system starting with Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="5e55f-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="5e55f-129">Si la sesión ha confirmado previamente alguna transacción y aún no se ha vaciado en el archivo de registro de transacciones, se deben vaciar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="5e55f-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="5e55f-130">Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="5e55f-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="5e55f-131">Esto resulta útil si la aplicación ha confirmado previamente varias transacciones mediante JET_bitCommitLazyFlush y ahora desea vaciar todas ellas en el disco.</span><span class="sxs-lookup"><span data-stu-id="5e55f-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="5e55f-132">Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="5e55f-133">Esta opción no se puede usar en combinación con ninguna otra opción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5e55f-134">*cmsecDurableCommit*</span><span class="sxs-lookup"><span data-stu-id="5e55f-134">*cmsecDurableCommit*</span></span>

<span data-ttu-id="5e55f-135">La duración de la confirmación de una transacción diferida.</span><span class="sxs-lookup"><span data-stu-id="5e55f-135">The duration to commit a lazy transaction.</span></span>

<span data-ttu-id="5e55f-136">*pCommitID*</span><span class="sxs-lookup"><span data-stu-id="5e55f-136">*pCommitID*</span></span>

<span data-ttu-id="5e55f-137">El ID. de confirmación asociado a este registro de confirmación.</span><span class="sxs-lookup"><span data-stu-id="5e55f-137">The Commit-ID associated with this commit record.</span></span>

### <a name="return-value"></a><span data-ttu-id="5e55f-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e55f-138">Return value</span></span>

<span data-ttu-id="5e55f-139">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e55f-139">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="5e55f-140">Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5e55f-140">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e55f-141">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5e55f-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="5e55f-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e55f-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5e55f-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5e55f-144">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e55f-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e55f-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5e55f-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5e55f-146">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a la función <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="5e55f-146">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5e55f-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5e55f-148">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="5e55f-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="5e55f-149">Este error solo lo devolverán las versiones del sistema operativo Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e55f-149">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e55f-150">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="5e55f-150">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="5e55f-151">Una de las opciones solicitadas no era válida o no se implementó.</span><span class="sxs-lookup"><span data-stu-id="5e55f-151">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="5e55f-152">Este error lo devolverá la función <strong>JetCommitTransaction2</strong> cuando se produzca lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5e55f-152">This error will be returned by the <strong>JetCommitTransaction2</strong> function when the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="5e55f-153">Se ha especificado un <em>grbit</em> no válido.</span><span class="sxs-lookup"><span data-stu-id="5e55f-153">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="5e55f-154">Se especificó JET_bitWaitLastLevel0Commit en combinación con otro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="5e55f-154">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="5e55f-155">Se especificó JET_bitWaitAllLevel0Commit en combinación con otro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="5e55f-155">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-156">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5e55f-156">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5e55f-157">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5e55f-157">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e55f-158">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="5e55f-158">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="5e55f-159">No se pudo realizar la operación porque la sesión especificada no está en una transacción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-159">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5e55f-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5e55f-161">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5e55f-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e55f-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="5e55f-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="5e55f-163">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="5e55f-163">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="5e55f-164">Este error solo lo devolverán las versiones del sistema operativo Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5e55f-164">This error will only be returned by versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5e55f-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5e55f-166">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5e55f-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5e55f-167">Si se ejecuta correctamente, se confirmarán los cambios realizados en la base de datos durante el punto de almacenamiento actual para la sesión dada y se finalizará el punto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="5e55f-167">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="5e55f-168">Si finalizó el último punto de retorno de la sesión, la transacción se vaciará opcionalmente en el archivo de registro de transacciones y la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-168">If the last save point for the session was ended, the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="5e55f-169">En caso de error, el estado transaccional de la sesión permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="5e55f-169">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="5e55f-170">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5e55f-170">No change to the database state will occur.</span></span> <span data-ttu-id="5e55f-171">La aplicación debe llamar a la función [JetRollback](./jetrollback-function.md) para anular la transacción.</span><span class="sxs-lookup"><span data-stu-id="5e55f-171">The application should call the [JetRollback](./jetrollback-function.md) function to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5e55f-172">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e55f-172">Remarks</span></span>

<span data-ttu-id="5e55f-173">Debe haber una llamada a **JetCommitTransaction2** o [JetRollback](./jetrollback-function.md) para que coincida con cada llamada a [JetBeginTransaction](./jetbegintransaction-function.md) para una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="5e55f-173">There must be one call to **JetCommitTransaction2** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5e55f-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e55f-174">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-175"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5e55f-175"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5e55f-176">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5e55f-176">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e55f-177"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5e55f-177"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5e55f-178">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="5e55f-178">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-179"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5e55f-179"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5e55f-180">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5e55f-180">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e55f-181"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="5e55f-181"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5e55f-182">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5e55f-182">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e55f-183"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5e55f-183"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5e55f-184">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5e55f-184">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5e55f-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e55f-185">See also</span></span>

[<span data-ttu-id="5e55f-186">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5e55f-186">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5e55f-187">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="5e55f-187">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="5e55f-188">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="5e55f-188">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="5e55f-189">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="5e55f-189">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="5e55f-190">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="5e55f-190">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="5e55f-191">JetRollback</span><span class="sxs-lookup"><span data-stu-id="5e55f-191">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="5e55f-192">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5e55f-192">JetStopService</span></span>](./jetstopservice-function.md)
