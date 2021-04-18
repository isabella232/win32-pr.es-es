---
description: 'Más información acerca de: JetBeginTransaction3 (función)'
title: Función JetBeginTransaction3
TOCTitle: JetBeginTransaction3 Function
ms:assetid: 7f8ed059-0b97-46fa-9925-e46cdcbee6ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835043(v=EXCHG.10)
ms:contentKeyID: 49894665
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetBeginTransaction3
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b263cb18c09df8205a49e1c4a1a683e339803f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714969"
---
# <a name="jetbegintransaction3-function"></a><span data-ttu-id="7a5bf-103">Función JetBeginTransaction3</span><span class="sxs-lookup"><span data-stu-id="7a5bf-103">JetBeginTransaction3 Function</span></span>


<span data-ttu-id="7a5bf-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7a5bf-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="7a5bf-105">La función **JetBeginTransaction3** hace que una sesión escriba una transacción y cree un nuevo punto de retorno.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-105">The **JetBeginTransaction3** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="7a5bf-106">Esta función se puede llamar más de una vez en una sola sesión para crear puntos de almacenamiento adicionales.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-106">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="7a5bf-107">Estos puntos de almacenamiento se pueden usar para conservar o descartar cambios en la base de datos de forma selectiva.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-107">These save points can be used to selectively to keep or discard changes to the database.</span></span>

<span data-ttu-id="7a5bf-108">La función **JetBeginTransaction3** se presentó en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-108">The **JetBeginTransaction3** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetBeginTransaction3(
  __in          JET_SESID sesid,
  __in          int64 trxid,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="7a5bf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a5bf-109">Parameters</span></span>

<span data-ttu-id="7a5bf-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7a5bf-110">*sesid*</span></span>

<span data-ttu-id="7a5bf-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-111">The session to use for this call.</span></span>

<span data-ttu-id="7a5bf-112">*trxid*</span><span class="sxs-lookup"><span data-stu-id="7a5bf-112">*trxid*</span></span>

<span data-ttu-id="7a5bf-113">Un identificador opcional proporcionado por el usuario para identificar la transacción.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-113">An optional identifier supplied by the user to identify the transaction.</span></span>

<span data-ttu-id="7a5bf-114">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7a5bf-114">*grbit*</span></span>

<span data-ttu-id="7a5bf-115">Grupo de bits que especifica cero o más de los valores de la opción de llamada que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-115">A group of bits that that specifies zero or more of the call option values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a5bf-116">Value</span><span class="sxs-lookup"><span data-stu-id="7a5bf-116">Value</span></span></p></th>
<th><p><span data-ttu-id="7a5bf-117">Significado</span><span class="sxs-lookup"><span data-stu-id="7a5bf-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a5bf-118">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="7a5bf-118">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-119">La transacción no modificará la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-119">The transaction will not modify the database.</span></span> <span data-ttu-id="7a5bf-120">Si se intenta realizar una actualización, se producirá un error en la operación con JET_errTransReadOnly código de respuesta.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-120">If an update is attempted, that operation will fail with JET_errTransReadOnly response code.</span></span> <span data-ttu-id="7a5bf-121">Se omite esta opción a menos que se solicite cuando la sesión especificada no está ya en una transacción.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-121">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="7a5bf-122">Esta opción está disponible en las versiones del sistema operativo Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-122">This option is available in versions of the Windows operating system starting with Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7a5bf-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a5bf-123">Return value</span></span>

<span data-ttu-id="7a5bf-124">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-124">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="7a5bf-125">Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7a5bf-125">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a5bf-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7a5bf-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="7a5bf-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a5bf-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a5bf-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7a5bf-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-129">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5bf-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7a5bf-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-131">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a la función <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="7a5bf-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a5bf-132">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7a5bf-132">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-133">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-133">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7a5bf-134">Este código de retorno lo devuelven las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-134">This return code is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5bf-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7a5bf-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-136">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-136">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a5bf-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7a5bf-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-138">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-138">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5bf-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7a5bf-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-140">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="7a5bf-141">Este error lo devuelven las versiones de Windows a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-141">This error is returned by versions of Windows starting with Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a5bf-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7a5bf-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-143">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5bf-144">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="7a5bf-144">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="7a5bf-145">No se puede iniciar una nueva transacción porque la sesión ya está en la profundidad máxima del punto de almacenamiento permitida por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-145">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a5bf-146">Si se ejecuta correctamente, la sesión proporcionada estará dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-146">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="7a5bf-147">Si la sesión estaba previamente dentro de una transacción, se creará un nuevo punto de retorno.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-147">If the session was previously inside a transaction, a new save point will be created.</span></span>

<span data-ttu-id="7a5bf-148">En caso de error, el estado transaccional de la sesión permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-148">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="7a5bf-149">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-149">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7a5bf-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a5bf-150">Remarks</span></span>

<span data-ttu-id="7a5bf-151">Para obtener más información sobre cómo funcionan las transacciones, vea [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="7a5bf-151">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="7a5bf-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a5bf-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a5bf-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7a5bf-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7a5bf-154">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-154">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5bf-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7a5bf-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7a5bf-156">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-156">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a5bf-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7a5bf-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7a5bf-158">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a5bf-159"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="7a5bf-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7a5bf-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a5bf-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7a5bf-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7a5bf-162">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7a5bf-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7a5bf-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a5bf-163">See also</span></span>

[<span data-ttu-id="7a5bf-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7a5bf-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7a5bf-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7a5bf-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7a5bf-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7a5bf-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7a5bf-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="7a5bf-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="7a5bf-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="7a5bf-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="7a5bf-169">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="7a5bf-169">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="7a5bf-170">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="7a5bf-170">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="7a5bf-171">JetRollback</span><span class="sxs-lookup"><span data-stu-id="7a5bf-171">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="7a5bf-172">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="7a5bf-172">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="7a5bf-173">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="7a5bf-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
