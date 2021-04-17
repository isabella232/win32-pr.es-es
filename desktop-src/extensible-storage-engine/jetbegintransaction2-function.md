---
description: 'Más información acerca de: JetBeginTransaction2 (función)'
title: Función JetBeginTransaction2
TOCTitle: JetBeginTransaction2 Function
ms:assetid: 638af3f1-b342-46bd-9fd0-dc281936355c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269268(v=EXCHG.10)
ms:contentKeyID: 32765570
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginTransaction
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d21bb88301a1f5d30df673a56032ef91c3847599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716676"
---
# <a name="jetbegintransaction2-function"></a><span data-ttu-id="98bc1-103">Función JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="98bc1-103">JetBeginTransaction2 Function</span></span>


<span data-ttu-id="98bc1-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="98bc1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbegintransaction2-function"></a><span data-ttu-id="98bc1-105">Función JetBeginTransaction2</span><span class="sxs-lookup"><span data-stu-id="98bc1-105">JetBeginTransaction2 Function</span></span>

<span data-ttu-id="98bc1-106">La función **JetBeginTransaction2** hace que una sesión escriba una transacción y cree un nuevo punto de retorno.</span><span class="sxs-lookup"><span data-stu-id="98bc1-106">The **JetBeginTransaction2** function causes a session to enter a transaction and create a new save point.</span></span> <span data-ttu-id="98bc1-107">Esta función se puede llamar más de una vez en una sola sesión para crear puntos de almacenamiento adicionales.</span><span class="sxs-lookup"><span data-stu-id="98bc1-107">This function can be called more than once in a single session to create additional save points.</span></span> <span data-ttu-id="98bc1-108">Estos puntos de almacenamiento se pueden usar para conservar o descartar cambios en la base de datos de forma selectiva.</span><span class="sxs-lookup"><span data-stu-id="98bc1-108">These save points can be used to selectively to keep or discard changes to the database.</span></span>

```cpp
    JET_ERR JET_API JetBeginTransaction2(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="98bc1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98bc1-109">Parameters</span></span>

<span data-ttu-id="98bc1-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="98bc1-110">*sesid*</span></span>

<span data-ttu-id="98bc1-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="98bc1-111">The session to use for this call.</span></span>

<span data-ttu-id="98bc1-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="98bc1-112">*grbit*</span></span>

<span data-ttu-id="98bc1-113">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="98bc1-113">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98bc1-114">Value</span><span class="sxs-lookup"><span data-stu-id="98bc1-114">Value</span></span></p></th>
<th><p><span data-ttu-id="98bc1-115">Significado</span><span class="sxs-lookup"><span data-stu-id="98bc1-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98bc1-116">JET_bitTransactionReadOnly</span><span class="sxs-lookup"><span data-stu-id="98bc1-116">JET_bitTransactionReadOnly</span></span></p></td>
<td><p><span data-ttu-id="98bc1-117">La transacción no modificará la base de datos.</span><span class="sxs-lookup"><span data-stu-id="98bc1-117">The transaction will not modify the database.</span></span> <span data-ttu-id="98bc1-118">Si se intenta realizar una actualización, se producirá un error en la operación con JET_errTransReadOnly.</span><span class="sxs-lookup"><span data-stu-id="98bc1-118">If an update is attempted, that operation will fail with JET_errTransReadOnly.</span></span> <span data-ttu-id="98bc1-119">Se omite esta opción a menos que se solicite cuando la sesión especificada no está ya en una transacción.</span><span class="sxs-lookup"><span data-stu-id="98bc1-119">This option is ignored unless it is requested when the given session is not already in a transaction.</span></span> <span data-ttu-id="98bc1-120">Esta opción solo está disponible a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98bc1-120">This option is only available as of Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="98bc1-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98bc1-121">Return Value</span></span>

<span data-ttu-id="98bc1-122">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="98bc1-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="98bc1-123">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="98bc1-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98bc1-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="98bc1-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="98bc1-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="98bc1-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98bc1-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="98bc1-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="98bc1-127">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="98bc1-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98bc1-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="98bc1-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="98bc1-129">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="98bc1-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98bc1-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="98bc1-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="98bc1-131">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="98bc1-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="98bc1-132">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="98bc1-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98bc1-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="98bc1-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="98bc1-134">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98bc1-134">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98bc1-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="98bc1-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="98bc1-136">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98bc1-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98bc1-137">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="98bc1-137">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="98bc1-138">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="98bc1-138">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="98bc1-139">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="98bc1-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98bc1-140">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="98bc1-140">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="98bc1-141">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98bc1-141">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98bc1-142">JET_errTransTooDeep</span><span class="sxs-lookup"><span data-stu-id="98bc1-142">JET_errTransTooDeep</span></span></p></td>
<td><p><span data-ttu-id="98bc1-143">No se puede iniciar una nueva transacción porque la sesión ya está en la profundidad máxima del punto de almacenamiento permitida por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="98bc1-143">A new transaction cannot be started because the session is already at the maximum save point depth allowable by the database engine.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="98bc1-144">Si se ejecuta correctamente, la sesión proporcionada estará dentro de una transacción.</span><span class="sxs-lookup"><span data-stu-id="98bc1-144">On success, the provided session will be inside a transaction.</span></span> <span data-ttu-id="98bc1-145">Si la sesión se encontraba anteriormente en una transacción, se creará un nuevo punto de retorno.</span><span class="sxs-lookup"><span data-stu-id="98bc1-145">If the session was previously inside of a transaction then a new save point will be created.</span></span>

<span data-ttu-id="98bc1-146">En caso de error, el estado transaccional de la sesión permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="98bc1-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="98bc1-147">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="98bc1-147">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="98bc1-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98bc1-148">Remarks</span></span>

<span data-ttu-id="98bc1-149">Para obtener más información sobre cómo funcionan las transacciones, vea [JetBeginTransaction](./jetbegintransaction-function.md).</span><span class="sxs-lookup"><span data-stu-id="98bc1-149">For more information about how transactions work, see [JetBeginTransaction](./jetbegintransaction-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="98bc1-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98bc1-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98bc1-151"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="98bc1-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="98bc1-152">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="98bc1-152">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98bc1-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="98bc1-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="98bc1-154">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="98bc1-154">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98bc1-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="98bc1-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="98bc1-156">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="98bc1-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98bc1-157"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="98bc1-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="98bc1-158">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="98bc1-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98bc1-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="98bc1-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="98bc1-160">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="98bc1-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="98bc1-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98bc1-161">See Also</span></span>

[<span data-ttu-id="98bc1-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="98bc1-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="98bc1-163">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="98bc1-163">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="98bc1-164">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="98bc1-164">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="98bc1-165">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="98bc1-165">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="98bc1-166">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="98bc1-166">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="98bc1-167">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="98bc1-167">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="98bc1-168">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="98bc1-168">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="98bc1-169">JetRollback</span><span class="sxs-lookup"><span data-stu-id="98bc1-169">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="98bc1-170">JetSetSessionContext</span><span class="sxs-lookup"><span data-stu-id="98bc1-170">JetSetSessionContext</span></span>](./jetsetsessioncontext-function.md)  
[<span data-ttu-id="98bc1-171">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="98bc1-171">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
