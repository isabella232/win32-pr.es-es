---
description: 'Más información acerca de: JetCommitTransaction (función)'
title: Función JetCommitTransaction
TOCTitle: JetCommitTransaction Function
ms:assetid: 140ca76a-b3a7-4ae8-bc7e-73941fbfc759
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269191(v=EXCHG.10)
ms:contentKeyID: 32765494
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCommitTransaction
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2fe42891aa916a428d63fb68c99f42f38e78993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002895"
---
# <a name="jetcommittransaction-function"></a><span data-ttu-id="45f67-103">Función JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="45f67-103">JetCommitTransaction Function</span></span>


<span data-ttu-id="45f67-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="45f67-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcommittransaction-function"></a><span data-ttu-id="45f67-105">Función JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="45f67-105">JetCommitTransaction Function</span></span>

<span data-ttu-id="45f67-106">La función **JetCommitTransaction** confirma los cambios realizados en el estado de la base de datos durante el punto de almacenamiento actual y los migra al punto de almacenamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="45f67-106">The **JetCommitTransaction** function commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="45f67-107">Si se confirma el punto de almacenamiento más externo, los cambios realizados durante ese punto de almacenamiento se confirmarán en el estado de la base de datos y la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="45f67-107">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetCommitTransaction(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="45f67-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45f67-108">Parameters</span></span>

<span data-ttu-id="45f67-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="45f67-109">*sesid*</span></span>

<span data-ttu-id="45f67-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="45f67-110">The session to use for this call.</span></span>

<span data-ttu-id="45f67-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="45f67-111">*grbit*</span></span>

<span data-ttu-id="45f67-112">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="45f67-112">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45f67-113">Value</span><span class="sxs-lookup"><span data-stu-id="45f67-113">Value</span></span></p></th>
<th><p><span data-ttu-id="45f67-114">Significado</span><span class="sxs-lookup"><span data-stu-id="45f67-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45f67-115">JET_bitCommitLazyFlush</span><span class="sxs-lookup"><span data-stu-id="45f67-115">JET_bitCommitLazyFlush</span></span></p></td>
<td><p><span data-ttu-id="45f67-116">La transacción se confirma normalmente, pero esta API no espera a que la transacción se vacíe en el archivo de registro de transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="45f67-116">The transaction is committed normally but this API does not wait for the transaction to be flushed to the transaction log file before returning to the caller.</span></span> <span data-ttu-id="45f67-117">Esto reduce drásticamente la duración de una operación de confirmación a costa de la durabilidad.</span><span class="sxs-lookup"><span data-stu-id="45f67-117">This drastically reduces the duration of a commit operation at the cost of durability.</span></span> <span data-ttu-id="45f67-118">Cualquier transacción que no se vacíe en el registro antes de un bloqueo se anulará automáticamente durante la recuperación tras el bloqueo durante la siguiente llamada a <a href="gg294068(v=exchg.10).md">JetInit</a>.</span><span class="sxs-lookup"><span data-stu-id="45f67-118">Any transaction that is not flushed to the log before a crash will be automatically aborted during crash recovery during the next call to <a href="gg294068(v=exchg.10).md">JetInit</a>.</span></span></p>
<p><span data-ttu-id="45f67-119">Si se especifican JET_bitWaitLastLevel0Commit o JET_bitWaitAllLevel0Commit, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="45f67-119">If JET_bitWaitLastLevel0Commit or JET_bitWaitAllLevel0Commit are specified, this option is ignored.</span></span></p>
<p><span data-ttu-id="45f67-120">Si esta llamada a <strong>JetCommitTransaction</strong> no coincide con la primera llamada a <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> para esta sesión, se omitirá esta opción.</span><span class="sxs-lookup"><span data-stu-id="45f67-120">If this call to <strong>JetCommitTransaction</strong> does not match the first call to <a href="gg294083(v=exchg.10).md">JetBeginTransaction</a> for this session, this option is ignored.</span></span> <span data-ttu-id="45f67-121">Esto se debe a que la acción final que se produce en el punto de almacenamiento más externo es el factor determinante de si toda la transacción se confirma realmente en el disco.</span><span class="sxs-lookup"><span data-stu-id="45f67-121">This is because the final action that occurs on the outermost save point is the determining factor in whether the entire transaction is actually committed to disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45f67-122">JET_bitWaitAllLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="45f67-122">JET_bitWaitAllLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="45f67-123">Todas las transacciones confirmadas previamente por cualquier sesión que todavía no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="45f67-123">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="45f67-124">Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="45f67-124">This API will wait until the transactions have been flushed before returning to the caller.</span></span></p>
<p><span data-ttu-id="45f67-125">Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="45f67-125">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="45f67-126">Esta opción no se puede usar en combinación con ninguna otra opción.</span><span class="sxs-lookup"><span data-stu-id="45f67-126">This option cannot be used in combination with any other option.</span></span></p>
<p><span data-ttu-id="45f67-127">Esta opción solo está disponible en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="45f67-127">This option is only available as of Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45f67-128">JET_bitWaitLastLevel0Commit</span><span class="sxs-lookup"><span data-stu-id="45f67-128">JET_bitWaitLastLevel0Commit</span></span></p></td>
<td><p><span data-ttu-id="45f67-129">Si la sesión ha confirmado previamente alguna transacción y aún no se ha vaciado en el archivo de registro de transacciones, se deben vaciar inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="45f67-129">If the session has previously committed any transactions and they have not yet been flushed to the transaction log file, they should be flushed immediately.</span></span> <span data-ttu-id="45f67-130">Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="45f67-130">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="45f67-131">Esto resulta útil si la aplicación ha confirmado previamente varias transacciones mediante JET_bitCommitLazyFlush y ahora desea vaciar todas ellas en el disco.</span><span class="sxs-lookup"><span data-stu-id="45f67-131">This is useful if the application has previously committed several transactions using JET_bitCommitLazyFlush and now wants to flush all of them to disk.</span></span></p>
<p><span data-ttu-id="45f67-132">Esta opción puede usarse incluso si la sesión no está actualmente en una transacción.</span><span class="sxs-lookup"><span data-stu-id="45f67-132">This option may be used even if the session is not currently in a transaction.</span></span></p>
<p><span data-ttu-id="45f67-133">Esta opción no se puede usar en combinación con ninguna otra opción.</span><span class="sxs-lookup"><span data-stu-id="45f67-133">This option cannot be used in combination with any other option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="45f67-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45f67-134">Return Value</span></span>

<span data-ttu-id="45f67-135">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="45f67-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="45f67-136">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="45f67-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45f67-137">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="45f67-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="45f67-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="45f67-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45f67-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="45f67-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="45f67-140">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="45f67-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45f67-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="45f67-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="45f67-142">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="45f67-142">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45f67-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="45f67-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="45f67-144">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="45f67-144">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="45f67-145">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="45f67-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45f67-146">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="45f67-146">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="45f67-147">Una de las opciones solicitadas no era válida o no se implementó.</span><span class="sxs-lookup"><span data-stu-id="45f67-147">One of the options requested was invalid or not implemented.</span></span> <span data-ttu-id="45f67-148">Este error lo devolverá <strong>JetCommitTransaction</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="45f67-148">This error will be returned by <strong>JetCommitTransaction</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="45f67-149">Se ha especificado un <em>grbit</em> no válido.</span><span class="sxs-lookup"><span data-stu-id="45f67-149">An illegal <em>grbit</em> is specified.</span></span></p></li>
<li><p><span data-ttu-id="45f67-150">Se especificó JET_bitWaitLastLevel0Commit en combinación con otro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="45f67-150">JET_bitWaitLastLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
<li><p><span data-ttu-id="45f67-151">Se especificó JET_bitWaitAllLevel0Commit en combinación con otro <em>grbit</em>.</span><span class="sxs-lookup"><span data-stu-id="45f67-151">JET_bitWaitAllLevel0Commit was specified in combination with another <em>grbit</em>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45f67-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="45f67-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="45f67-153">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="45f67-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45f67-154">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="45f67-154">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="45f67-155">No se pudo realizar la operación porque la sesión especificada no está en una transacción.</span><span class="sxs-lookup"><span data-stu-id="45f67-155">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45f67-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="45f67-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="45f67-157">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="45f67-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45f67-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="45f67-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="45f67-159">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="45f67-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="45f67-160">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="45f67-160">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45f67-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="45f67-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="45f67-162">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="45f67-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="45f67-163">Si se ejecuta correctamente, se confirmarán los cambios realizados en la base de datos durante el punto de almacenamiento actual para la sesión dada y se finalizará el punto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="45f67-163">On success, any changes made to the database during the current save point for the given session will be committed and that save point will be ended.</span></span> <span data-ttu-id="45f67-164">Si finalizó el último punto de retorno de la sesión, la transacción se vaciará opcionalmente en el archivo de registro de transacciones y la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="45f67-164">If the last save point for the session was ended then the transaction will optionally be flushed to the transaction log file and the session will exit the transaction.</span></span>

<span data-ttu-id="45f67-165">En caso de error, el estado transaccional de la sesión permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="45f67-165">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="45f67-166">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="45f67-166">No change to the database state will occur.</span></span> <span data-ttu-id="45f67-167">La aplicación debe llamar a [JetRollback](./jetrollback-function.md) para anular la transacción.</span><span class="sxs-lookup"><span data-stu-id="45f67-167">The application should call [JetRollback](./jetrollback-function.md) to abort the transaction.</span></span>

#### <a name="remarks"></a><span data-ttu-id="45f67-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45f67-168">Remarks</span></span>

<span data-ttu-id="45f67-169">Debe haber una llamada a **JetCommitTransaction** o [JetRollback](./jetrollback-function.md) para que coincida con cada llamada a [JetBeginTransaction](./jetbegintransaction-function.md) para una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="45f67-169">There must be one call to **JetCommitTransaction** or [JetRollback](./jetrollback-function.md) to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

#### <a name="requirements"></a><span data-ttu-id="45f67-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45f67-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45f67-171"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="45f67-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="45f67-172">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="45f67-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45f67-173"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="45f67-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="45f67-174">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="45f67-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45f67-175"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="45f67-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="45f67-176">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="45f67-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45f67-177"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="45f67-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="45f67-178">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="45f67-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45f67-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="45f67-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="45f67-180">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="45f67-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="45f67-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="45f67-181">See Also</span></span>

[<span data-ttu-id="45f67-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="45f67-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="45f67-183">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="45f67-183">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="45f67-184">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="45f67-184">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="45f67-185">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="45f67-185">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="45f67-186">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="45f67-186">JetCommitTransaction</span></span>]()  
[<span data-ttu-id="45f67-187">JetRollback</span><span class="sxs-lookup"><span data-stu-id="45f67-187">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="45f67-188">JetStopService</span><span class="sxs-lookup"><span data-stu-id="45f67-188">JetStopService</span></span>](./jetstopservice-function.md)
