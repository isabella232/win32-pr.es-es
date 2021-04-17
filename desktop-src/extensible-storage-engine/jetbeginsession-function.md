---
description: 'Más información acerca de: JetBeginSession (función)'
title: Función JetBeginSession
TOCTitle: JetBeginSession Function
ms:assetid: f1c33b78-f2d1-44ea-8ec9-94b729b94e24
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294131(v=EXCHG.10)
ms:contentKeyID: 32765745
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginSessionA
- JetBeginSession
- JetBeginSessionW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfe0cf06e86b19d16284b704697c65b1f38a167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716965"
---
# <a name="jetbeginsession-function"></a><span data-ttu-id="41c51-103">Función JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="41c51-103">JetBeginSession Function</span></span>


<span data-ttu-id="41c51-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="41c51-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginsession-function"></a><span data-ttu-id="41c51-105">Función JetBeginSession</span><span class="sxs-lookup"><span data-stu-id="41c51-105">JetBeginSession Function</span></span>

<span data-ttu-id="41c51-106">La función **JetBeginSession** inicia una sesión e inicializa y devuelve un identificador de sesión de ESE ([JET_SESID](./jet-sesid.md)).</span><span class="sxs-lookup"><span data-stu-id="41c51-106">The **JetBeginSession** function starts a session and initializes and returns an ESE session handle ([JET_SESID](./jet-sesid.md)).</span></span> <span data-ttu-id="41c51-107">Las sesiones controlan todo el acceso a la base de datos y se usan para controlar el ámbito de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="41c51-107">Sessions control all access to the database and are used to control the scope of transactions.</span></span> <span data-ttu-id="41c51-108">La sesión se puede usar para iniciar, confirmar o anular transacciones.</span><span class="sxs-lookup"><span data-stu-id="41c51-108">The session can be used to begin, commit, or abort transactions.</span></span> <span data-ttu-id="41c51-109">La sesión también se utiliza para adjuntar, crear o abrir una base de datos.</span><span class="sxs-lookup"><span data-stu-id="41c51-109">The session is also used to attach, create, or open a database.</span></span> <span data-ttu-id="41c51-110">La sesión se utiliza como contexto para todas las operaciones DDL y DML.</span><span class="sxs-lookup"><span data-stu-id="41c51-110">The session is used as the context for all DDL and DML operations.</span></span> <span data-ttu-id="41c51-111">Para aumentar la simultaneidad y el acceso en paralelo a la base de datos, se pueden iniciar varias sesiones.</span><span class="sxs-lookup"><span data-stu-id="41c51-111">To increase concurrency and parallel access to the database, multiple sessions can be begun.</span></span>

```cpp
    JET_ERR JET_API JetBeginSession(
      __in          JET_INSTANCE instance,
      __out         JET_SESID* psesid,
      __in_opt      JET_PCSTR szUserName,
      __in_opt      JET_PCSTR szPassword
    );
```

### <a name="parameters"></a><span data-ttu-id="41c51-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41c51-112">Parameters</span></span>

<span data-ttu-id="41c51-113">*repetición*</span><span class="sxs-lookup"><span data-stu-id="41c51-113">*instance*</span></span>

<span data-ttu-id="41c51-114">Instancia de base de datos que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="41c51-114">The database instance to use for this call.</span></span>

<span data-ttu-id="41c51-115">*psesid*</span><span class="sxs-lookup"><span data-stu-id="41c51-115">*psesid*</span></span>

<span data-ttu-id="41c51-116">Puntero a la variable que el identificador de la sesión inicializa si la devolución es correcta.</span><span class="sxs-lookup"><span data-stu-id="41c51-116">Pointer to the variable that the session handle initializes on successful return.</span></span>

<span data-ttu-id="41c51-117">*szUserName*</span><span class="sxs-lookup"><span data-stu-id="41c51-117">*szUserName*</span></span>

<span data-ttu-id="41c51-118">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="41c51-118">This parameter is reserved.</span></span>

<span data-ttu-id="41c51-119">*szPassword*</span><span class="sxs-lookup"><span data-stu-id="41c51-119">*szPassword*</span></span>

<span data-ttu-id="41c51-120">Este parámetro está reservado.</span><span class="sxs-lookup"><span data-stu-id="41c51-120">This parameter is reserved.</span></span>

### <a name="return-value"></a><span data-ttu-id="41c51-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41c51-121">Return Value</span></span>

<span data-ttu-id="41c51-122">Esta función permite que se devuelvan los [JET_ERR](./jet-err.md)s definidos en esta API.</span><span class="sxs-lookup"><span data-stu-id="41c51-122">This function allows for the return of any [JET_ERR](./jet-err.md)s that are defined in this API.</span></span> <span data-ttu-id="41c51-123">Para obtener más información acerca de los errores de jet, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="41c51-123">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41c51-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="41c51-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="41c51-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="41c51-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41c51-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="41c51-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="41c51-127">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="41c51-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41c51-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="41c51-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="41c51-129">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="41c51-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41c51-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="41c51-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="41c51-131">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="41c51-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="41c51-132">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="41c51-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41c51-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="41c51-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="41c51-134">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="41c51-134">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41c51-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="41c51-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="41c51-136">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="41c51-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41c51-137">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="41c51-137">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="41c51-138">No se pudo realizar la operación porque no se pudo asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="41c51-138">The operation failed because memory could not be allocated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41c51-139">JET_errOutOfSessions</span><span class="sxs-lookup"><span data-stu-id="41c51-139">JET_errOutOfSessions</span></span></p></td>
<td><p><span data-ttu-id="41c51-140">El número de sesiones que el motor permitirá que se inicie el cliente es limitado.</span><span class="sxs-lookup"><span data-stu-id="41c51-140">The number of sessions the engine will allow the client to start is limited.</span></span> <span data-ttu-id="41c51-141">Este valor se puede cambiar mediante <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> con la constante JET_paramMaxSessions.</span><span class="sxs-lookup"><span data-stu-id="41c51-141">This value can be changed using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> with the JET_paramMaxSessions constant.</span></span> <span data-ttu-id="41c51-142">El número predeterminado de sesiones es 16.</span><span class="sxs-lookup"><span data-stu-id="41c51-142">The default number of sessions is 16.</span></span> <span data-ttu-id="41c51-143">Consulte <a href="gg294139(v=exchg.10).md">parámetros del sistema</a> para obtener más información sobre JET_paramMaxSessions.</span><span class="sxs-lookup"><span data-stu-id="41c51-143">See <a href="gg294139(v=exchg.10).md">System Parameters</a> for details about JET_paramMaxSessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41c51-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="41c51-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="41c51-145">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="41c51-145">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41c51-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="41c51-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="41c51-147">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="41c51-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="41c51-148">Si se ejecuta correctamente, el identificador de sesión se inicializa y se puede usar para las operaciones de base de datos.</span><span class="sxs-lookup"><span data-stu-id="41c51-148">On success, the session handle is initialized, and may be used for database operations.</span></span>

<span data-ttu-id="41c51-149">En caso de error, no hay sesiones disponibles o no se pudo inicializar una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="41c51-149">On failure, there are no available sessions or a new session was unable to be initialized.</span></span>

#### <a name="remarks"></a><span data-ttu-id="41c51-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41c51-150">Remarks</span></span>

<span data-ttu-id="41c51-151">Se debe prestar especial atención al usar sesiones en diferentes subprocesos.</span><span class="sxs-lookup"><span data-stu-id="41c51-151">Careful attention must be used when using sessions across different threads.</span></span> <span data-ttu-id="41c51-152">Una sesión realiza un seguimiento del subproceso en el que se usó durante [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md)o [JetRollback](./jetrollback-function.md), y producirá un error si se utiliza en varios subprocesos con una transacción abierta.</span><span class="sxs-lookup"><span data-stu-id="41c51-152">A session tracks which thread it was used on during [JetBeginTransaction](./jetbegintransaction-function.md), [JetCommitTransaction](./jetcommittransaction-function.md), or [JetRollback](./jetrollback-function.md), and it will throw an error if used on multiple threads with an open transaction.</span></span> <span data-ttu-id="41c51-153">[JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) puede cambiar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="41c51-153">The [JetResetSessionContext](./jetresetsessioncontext-function.md), [JetSetSessionContext](./jetsetsessioncontext-function.md) can change this behavior.</span></span> <span data-ttu-id="41c51-154">Dado que la sesión sigue siendo un contexto serializado, y no se pueden realizar varias operaciones de base de datos en una sola sesión simultáneamente, solo en serie.</span><span class="sxs-lookup"><span data-stu-id="41c51-154">Since the session is still a serialized context, and multiple database operations cannot be performed on a single session concurrently, only serially.</span></span> <span data-ttu-id="41c51-155">Sin embargo, puede usar varias sesiones para lograr el acceso simultáneo a las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="41c51-155">However, you can use multiple sessions to achieve concurrent database access.</span></span> <span data-ttu-id="41c51-156">Las sesiones se pueden usar dentro de una transacción en todos los subprocesos estableciendo y restableciendo los contextos de la sesión.</span><span class="sxs-lookup"><span data-stu-id="41c51-156">Sessions can be used inside a transaction across threads by setting and resetting the session contexts.</span></span>

<span data-ttu-id="41c51-157">El identificador de sesión debe cerrarse con [JetEndSession](./jetendsession-function.md).</span><span class="sxs-lookup"><span data-stu-id="41c51-157">The session handle should be closed with [JetEndSession](./jetendsession-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="41c51-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c51-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41c51-159"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="41c51-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="41c51-160">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="41c51-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41c51-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="41c51-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="41c51-162">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="41c51-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41c51-163"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="41c51-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="41c51-164">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="41c51-164">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41c51-165"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="41c51-165"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="41c51-166">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="41c51-166">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41c51-167"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="41c51-167"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="41c51-168">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="41c51-168">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41c51-169"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="41c51-169"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="41c51-170">Se implementa como <strong>JetBeginSessionW</strong> (Unicode) y <strong>JetBeginSessionA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="41c51-170">Implemented as <strong>JetBeginSessionW</strong> (Unicode) and <strong>JetBeginSessionA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="41c51-171">Consulte también</span><span class="sxs-lookup"><span data-stu-id="41c51-171">See Also</span></span>

[<span data-ttu-id="41c51-172">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="41c51-172">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="41c51-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="41c51-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="41c51-174">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="41c51-174">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="41c51-175">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="41c51-175">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="41c51-176">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="41c51-176">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="41c51-177">JetDupSession</span><span class="sxs-lookup"><span data-stu-id="41c51-177">JetDupSession</span></span>](./jetdupsession-function.md)  
[<span data-ttu-id="41c51-178">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="41c51-178">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="41c51-179">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="41c51-179">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="41c51-180">JetRollback</span><span class="sxs-lookup"><span data-stu-id="41c51-180">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="41c51-181">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="41c51-181">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="41c51-182">JetStopService</span><span class="sxs-lookup"><span data-stu-id="41c51-182">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="41c51-183">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="41c51-183">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
