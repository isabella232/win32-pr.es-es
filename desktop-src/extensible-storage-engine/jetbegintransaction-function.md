---
description: 'Más información acerca de: JetBeginTransaction (función)'
title: Función JetBeginTransaction
TOCTitle: JetBeginTransaction Function
ms:assetid: c5b2f9d7-157d-431d-a292-009c43773a9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294083(v=EXCHG.10)
ms:contentKeyID: 32765698
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd5986d2e9e8e3c65fa472f37e8d92c4afbb4803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360132"
---
# <a name="jetbegintransaction-function"></a><span data-ttu-id="4b0cf-103">Función JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="4b0cf-103">JetBeginTransaction Function</span></span>


<span data-ttu-id="4b0cf-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4b0cf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction-function"></a><span data-ttu-id="4b0cf-105">Función JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="4b0cf-105">JetBeginTransaction Function</span></span>

<span data-ttu-id="4b0cf-106">La función **JetBeginTransaction** hace que una sesión escriba una transacción y cree un nuevo punto de retorno.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-106">The **JetBeginTransaction** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="4b0cf-107">Esta función se puede llamar más de una vez en una sola sesión para provocar la creación de puntos de almacenamiento adicionales.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-107">This function can be called more than once on a single session to cause the creation of additional save points.</span></span> <span data-ttu-id="4b0cf-108">Estos puntos de almacenamiento se pueden usar para conservar o descartar cambios de forma selectiva en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-108">These save points can be used to selectively keep or discard changes to the state of the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction(
      __in          JET_SESID sesid
    );
```

### <a name="parameters"></a><span data-ttu-id="4b0cf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b0cf-109">Parameters</span></span>

<span data-ttu-id="4b0cf-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="4b0cf-110">*sesid*</span></span>

<span data-ttu-id="4b0cf-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-111">The session to use for this call.</span></span>

### <a name="return-value"></a><span data-ttu-id="4b0cf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b0cf-112">Return Value</span></span>

<span data-ttu-id="4b0cf-113">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4b0cf-114">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4b0cf-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b0cf-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4b0cf-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="4b0cf-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b0cf-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b0cf-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4b0cf-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4b0cf-118">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-118">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b0cf-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4b0cf-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4b0cf-120">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-120">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b0cf-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4b0cf-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4b0cf-122">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-122">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="4b0cf-123">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-123">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b0cf-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4b0cf-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4b0cf-125">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-125">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b0cf-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4b0cf-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4b0cf-127">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-127">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b0cf-128">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="4b0cf-128">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="4b0cf-129">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-129">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="4b0cf-130">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b0cf-131">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4b0cf-131">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4b0cf-132">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-132">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b0cf-133">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="4b0cf-133">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="4b0cf-134">No se puede iniciar una nueva transacción porque la sesión ya está en la profundidad máxima del punto de almacenamiento permitida por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-134">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4b0cf-135">Si se ejecuta correctamente, la sesión proporcionada estará dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-135">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="4b0cf-136">Si la sesión se encontraba anteriormente en una transacción, se creará un nuevo punto de retorno.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-136">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="4b0cf-137">En caso de error, el estado transaccional de la sesión permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-137">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="4b0cf-138">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-138">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4b0cf-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b0cf-139">Remarks</span></span>

<span data-ttu-id="4b0cf-140">El motor de base de datos proporciona un modelo de aislamiento de instantánea para sus transacciones.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-140">The database engine provides a snapshot isolation model for its transactions.</span></span> <span data-ttu-id="4b0cf-141">Esto significa que, cuando una sesión entra en un estado transaccional, la sesión verá toda la base de datos en el momento en que se inicia la transacción.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-141">This means that, when a session first enters into a transactional state, the session will see the entire database frozen in time at the start of the transaction.</span></span> <span data-ttu-id="4b0cf-142">Una sesión no tiene que leer bloquear los datos porque siempre puede tener acceso a la versión adecuada de los datos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-142">A session does not need to read lock any data because it can always access the appropriate version of that data.</span></span> <span data-ttu-id="4b0cf-143">Esto significa que una sesión que está actualizando los datos nunca impedirá que una sesión diferente Lea los datos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-143">This means that a session that is updating data will never block a different session from reading that data.</span></span>

<span data-ttu-id="4b0cf-144">Otra implicación del uso del aislamiento de instantánea es el modelo de bloqueo que se usa para las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-144">Another implication of the use of snapshot isolation is the locking model used for updates.</span></span> <span data-ttu-id="4b0cf-145">El motor de base de datos adjudicará un bloqueo de escritura en un determinado dato a la primera sesión que lo solicite.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-145">The database engine will award a write lock on a given piece of data to the first session that requests it.</span></span> <span data-ttu-id="4b0cf-146">Este bloqueo de escritura se libera cuando la transacción se confirma o se anula completamente de forma que la sesión ya no se encuentra en una transacción.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-146">This write lock is released when the transaction is either committed or aborted completely such that the session is no longer in a transaction.</span></span> <span data-ttu-id="4b0cf-147">Mientras una sesión mantiene un bloqueo de escritura, cualquier otra sesión que solicite el mismo bloqueo de escritura no se bloqueará hasta que el bloqueo de escritura esté disponible.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-147">While a session holds a write lock, any other session that requests the same write lock will not block until the write lock is available.</span></span> <span data-ttu-id="4b0cf-148">En su lugar, se producirá un error inmediato en esa segunda sesión con JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-148">Rather, that second session will immediately fail with JET_errWriteConflict.</span></span> <span data-ttu-id="4b0cf-149">Para resolver este conflicto, la segunda sesión debe anular (o confirmar) completamente su transacción, esperar un pequeño período de tiempo para que la primera sesión confirme o anule su transacción y, a continuación, vuelva a iniciarla.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-149">To resolve this conflict, the second session must abort (or commit) its transaction completely, wait some small period of time for the first session to commit or abort its transaction, and then start all over again.</span></span>

<span data-ttu-id="4b0cf-150">En cuanto a la compatibilidad con el aislamiento de instantánea, el motor de base de datos almacena todas las versiones de todos los datos modificados en la memoria desde el momento en que se inició por primera vez la transacción activa más antigua en cualquier sesión.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-150">In support of snapshot isolation, the database engine stores all versions of all modified data in memory since the time when the oldest active transaction on any session was first started.</span></span> <span data-ttu-id="4b0cf-151">Esto tiene implicaciones importantes para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-151">This has important implications for your application.</span></span> <span data-ttu-id="4b0cf-152">Cualquier comportamiento que cause un gran número de versiones para compilar en memoria puede hacer que la instancia agote su tamaño máximo de almacén de versiones (consulte [JET_paramMaxVerPages](./resource-parameters.md) en [parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="4b0cf-152">Any behavior that causes a large number of versions to build up in memory may cause the instance to exhaust its maximum version store size (see [JET_paramMaxVerPages](./resource-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md) for more information).</span></span> <span data-ttu-id="4b0cf-153">Este comportamiento incluye, pero no se limita a las actualizaciones muy grandes en una única transacción y transacciones de ejecución muy prolongada.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-153">Such behavior includes, but is not limited to very large updates in a single transaction and very long running transactions.</span></span> <span data-ttu-id="4b0cf-154">Como resultado, es muy importante configurar correctamente el tamaño del almacén de versiones para la carga transaccional esperada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-154">As a result, it is very important to properly configure the version store size for the expected transactional load of the application.</span></span> <span data-ttu-id="4b0cf-155">También es importante tener mucho cuidado para limitar el número de actualizaciones realizadas en una sola transacción.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-155">It is also important to take great care to limit the number of updates performed in a single transaction.</span></span> <span data-ttu-id="4b0cf-156">Además, es importante que las transacciones sean lo más cortas posible en situaciones de carga elevada.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-156">Furthermore, it is important to make transactions as short in duration as possible under high load scenarios.</span></span>

<span data-ttu-id="4b0cf-157">Se recomienda encarecidamente que la aplicación esté siempre en el contexto de una transacción al llamar a las API de ESE que recuperan o actualizan los datos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-157">It is highly recommended that the application always be in the context of a transaction when calling ESE APIs that retrieve or update data.</span></span> <span data-ttu-id="4b0cf-158">Si no se hace esto, el motor de base de datos ajustará automáticamente cada llamada de API de ESE tipo en una transacción en nombre de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-158">If this is not done, the database engine will automatically wrap each ESE API call of this type in a transaction on behalf of the application.</span></span> <span data-ttu-id="4b0cf-159">El costo de estas transacciones muy cortas puede agregarse rápidamente en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-159">The cost of these very short transactions can add up quickly in some cases.</span></span>

<span data-ttu-id="4b0cf-160">El comportamiento predeterminado del motor es restringir el uso de una sesión al mismo subproceso desde el momento en que se realiza la primera llamada a **JetBeginTransaction** hasta el momento en que se realiza la llamada coincidente a [JetCommitTransaction](./jetcommittransaction-function.md) o [JetRollback](./jetrollback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4b0cf-160">The default behavior of the engine is to restrict the use of a session to the same thread from the time the first call to **JetBeginTransaction** is made until the time when the matching call to [JetCommitTransaction](./jetcommittransaction-function.md) or [JetRollback](./jetrollback-function.md) is made.</span></span> <span data-ttu-id="4b0cf-161">Este comportamiento se puede cambiar para quitar esta restricción mediante la configuración de un contexto de sesión personalizado mediante [JetSetSessionContext](./jetsetsessioncontext-function.md) y [JetResetSessionContext](./jetresetsessioncontext-function.md).</span><span class="sxs-lookup"><span data-stu-id="4b0cf-161">This behavior can be changed to remove this restriction by setting a custom session context using [JetSetSessionContext](./jetsetsessioncontext-function.md) and [JetResetSessionContext](./jetresetsessioncontext-function.md).</span></span>

<span data-ttu-id="4b0cf-162">El motor de base de datos también admite modificaciones de esquema transaccionales.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-162">The database engine also supports transactional schema modifications.</span></span> <span data-ttu-id="4b0cf-163">Por ejemplo, se puede iniciar una nueva transacción, crear una tabla, agregar algunas columnas, crear un índice o dos y, después, anular la transacción.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-163">For example, it is possible to begin a new transaction, create a table, add a few columns, create an index or two, and then abort the transaction.</span></span> <span data-ttu-id="4b0cf-164">Los elementos de esquema que se acaban de agregar se quitarán de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-164">The schema elements that were just added will be removed from the database.</span></span> <span data-ttu-id="4b0cf-165">También es posible mezclar las modificaciones de esquema y las actualizaciones de bases de datos normales en la misma transacción.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-165">It is also possible to mix schema modifications and ordinary database updates in the same transaction.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4b0cf-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b0cf-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b0cf-167"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4b0cf-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4b0cf-168">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b0cf-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4b0cf-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4b0cf-170">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b0cf-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4b0cf-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4b0cf-172">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b0cf-173"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="4b0cf-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4b0cf-174">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b0cf-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4b0cf-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4b0cf-176">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4b0cf-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4b0cf-177">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4b0cf-177">See Also</span></span>

[<span data-ttu-id="4b0cf-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4b0cf-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4b0cf-179">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="4b0cf-179">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="4b0cf-180">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="4b0cf-180">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="4b0cf-181">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="4b0cf-181">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="4b0cf-182">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="4b0cf-182">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="4b0cf-183">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="4b0cf-183">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="4b0cf-184">JetRollback</span><span class="sxs-lookup"><span data-stu-id="4b0cf-184">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="4b0cf-185">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="4b0cf-185">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="4b0cf-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="4b0cf-186">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="4b0cf-187">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="4b0cf-187">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
