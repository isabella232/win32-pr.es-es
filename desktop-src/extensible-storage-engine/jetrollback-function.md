---
description: 'Más información acerca de: JetRollback (función)'
title: JetRollback función)
TOCTitle: JetRollback Function
ms:assetid: 685c51f4-8fe4-47cc-8a8e-c42014431b8b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269273(v=EXCHG.10)
ms:contentKeyID: 32765575
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRollback
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eda0c8947e9609717bbb3f1a16999b450d7e4882
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707178"
---
# <a name="jetrollback-function"></a><span data-ttu-id="aed47-103">JetRollback función)</span><span class="sxs-lookup"><span data-stu-id="aed47-103">JetRollback Function</span></span>


<span data-ttu-id="aed47-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="aed47-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrollback-function"></a><span data-ttu-id="aed47-105">JetRollback función)</span><span class="sxs-lookup"><span data-stu-id="aed47-105">JetRollback Function</span></span>

<span data-ttu-id="aed47-106">La función **JetRollback** deshace los cambios realizados en el estado de la base de datos y vuelve al último punto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="aed47-106">The **JetRollback** function undoes the changes made to the state of the database and returns to the last save point.</span></span> <span data-ttu-id="aed47-107">**JetRollback** también cerrará los cursores abiertos durante el punto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="aed47-107">**JetRollback** will also close any cursors opened during the save point.</span></span> <span data-ttu-id="aed47-108">Si el punto de almacenamiento más externo se deshace, la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="aed47-108">If the outermost save point is undone, the session will exit the transaction.</span></span>

```cpp
    JET_ERR JET_API JetRollback(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="aed47-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aed47-109">Parameters</span></span>

<span data-ttu-id="aed47-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="aed47-110">*sesid*</span></span>

<span data-ttu-id="aed47-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="aed47-111">The session to use for this call.</span></span>

<span data-ttu-id="aed47-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="aed47-112">*grbit*</span></span>

<span data-ttu-id="aed47-113">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="aed47-113">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aed47-114">Value</span><span class="sxs-lookup"><span data-stu-id="aed47-114">Value</span></span></p></th>
<th><p><span data-ttu-id="aed47-115">Significado</span><span class="sxs-lookup"><span data-stu-id="aed47-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aed47-116">JET_bitRollbackAll</span><span class="sxs-lookup"><span data-stu-id="aed47-116">JET_bitRollbackAll</span></span></p></td>
<td><p><span data-ttu-id="aed47-117">Esta opción solicita que se deshagan todos los cambios realizados en el estado de la base de datos durante todos los puntos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="aed47-117">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="aed47-118">Como resultado, la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="aed47-118">As a result, the session will exit the transaction.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="aed47-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aed47-119">Return Value</span></span>

<span data-ttu-id="aed47-120">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="aed47-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="aed47-121">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="aed47-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aed47-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="aed47-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="aed47-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="aed47-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aed47-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="aed47-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="aed47-125">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="aed47-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed47-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="aed47-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="aed47-127">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="aed47-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed47-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="aed47-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="aed47-129">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="aed47-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="aed47-130">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="aed47-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed47-131">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="aed47-131">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="aed47-132">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="aed47-132">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed47-133">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="aed47-133">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="aed47-134">No se pudo realizar la operación porque la sesión especificada no está en una transacción.</span><span class="sxs-lookup"><span data-stu-id="aed47-134">The operation failed because the given session is not in a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed47-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="aed47-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="aed47-136">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="aed47-136">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed47-137">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="aed47-137">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="aed47-138">No se pudieron revertir los cambios debido a un error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="aed47-138">It was not possible to rollback the changes due to a fatal error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed47-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="aed47-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="aed47-140">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="aed47-140">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="aed47-141">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="aed47-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed47-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="aed47-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="aed47-143">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="aed47-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aed47-144">Si se ejecuta correctamente, se desharán los cambios realizados en la base de datos durante el punto de almacenamiento actual para la sesión dada y se finalizará el punto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="aed47-144">On success, any changes made to the database during the current save point for the given session will be undone and that save point will be ended.</span></span> <span data-ttu-id="aed47-145">Si finalizó el último punto de retorno de la sesión, la sesión finalizará la transacción.</span><span class="sxs-lookup"><span data-stu-id="aed47-145">If the last save point for the session was ended then the session will exit the transaction.</span></span>

<span data-ttu-id="aed47-146">En caso de error, el estado transaccional de la sesión permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="aed47-146">On failure, the transactional state of the session will remain unchanged.</span></span> <span data-ttu-id="aed47-147">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="aed47-147">No change to the database state will occur.</span></span> <span data-ttu-id="aed47-148">Un error durante la reversión se considera un error grave de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="aed47-148">A failure during rollback is considered to be a catastrophic database error.</span></span>

#### <a name="remarks"></a><span data-ttu-id="aed47-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aed47-149">Remarks</span></span>

<span data-ttu-id="aed47-150">Debe haber una llamada a [JetCommitTransaction](./jetcommittransaction-function.md) o **JetRollback** para que coincida con cada llamada a [JetBeginTransaction](./jetbegintransaction-function.md) para una sesión determinada.</span><span class="sxs-lookup"><span data-stu-id="aed47-150">There must be one call to [JetCommitTransaction](./jetcommittransaction-function.md) or **JetRollback** to match every call to [JetBeginTransaction](./jetbegintransaction-function.md) for a given session.</span></span>

<span data-ttu-id="aed47-151">Si se abrió algún cursor (por ejemplo, mediante [JetOpenTable](./jetopentable-function.md)) durante un punto de retorno que se va a revertir, se cerrará ese cursor.</span><span class="sxs-lookup"><span data-stu-id="aed47-151">If any cursors were opened (using [JetOpenTable](./jetopentable-function.md), for example) during a save point that is being rolled back then that cursor will be closed.</span></span>

#### <a name="requirements"></a><span data-ttu-id="aed47-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aed47-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aed47-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="aed47-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aed47-154">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="aed47-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed47-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="aed47-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aed47-156">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="aed47-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed47-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="aed47-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aed47-158">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="aed47-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aed47-159"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="aed47-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="aed47-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="aed47-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aed47-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="aed47-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="aed47-162">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="aed47-162">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="aed47-163">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aed47-163">See Also</span></span>

[<span data-ttu-id="aed47-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="aed47-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="aed47-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="aed47-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="aed47-166">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="aed47-166">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="aed47-167">JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="aed47-167">JetBeginTransaction</span></span>](./jetbegintransaction-function.md)  
[<span data-ttu-id="aed47-168">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="aed47-168">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)
