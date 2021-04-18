---
description: 'Más información acerca de: JetGetCursorInfo (función)'
title: JetGetCursorInfo función)
TOCTitle: JetGetCursorInfo Function
ms:assetid: e779fa5d-1d7e-46f1-80c9-f7c819279188
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294126(v=EXCHG.10)
ms:contentKeyID: 32765740
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCursorInfo
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7201c37f79f68deead837cdcdd90402e4b2bf1e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659992"
---
# <a name="jetgetcursorinfo-function"></a><span data-ttu-id="e782d-103">JetGetCursorInfo función)</span><span class="sxs-lookup"><span data-stu-id="e782d-103">JetGetCursorInfo Function</span></span>


<span data-ttu-id="e782d-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e782d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcursorinfo-function"></a><span data-ttu-id="e782d-105">JetGetCursorInfo función)</span><span class="sxs-lookup"><span data-stu-id="e782d-105">JetGetCursorInfo Function</span></span>

<span data-ttu-id="e782d-106">La función **JetGetCursorInfo** se usa para determinar si una actualización del registro actual de un cursor producirá un conflicto de escritura, según el estado actual de actualización del registro.</span><span class="sxs-lookup"><span data-stu-id="e782d-106">The **JetGetCursorInfo** function is used to determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="e782d-107">Es posible que se devuelva un conflicto de escritura en última instancia, incluso si **JetGetCursorInfo** devuelve JET_errSuccess, porque otra sesión puede actualizar el registro antes de que la sesión actual pueda actualizar el mismo registro.</span><span class="sxs-lookup"><span data-stu-id="e782d-107">It is possible that a write conflict will ultimately be returned even if **JetGetCursorInfo** returns JET_errSuccess, because another session may update the record before the current session is able to update the same record.</span></span>

```cpp
    JET_ERR JET_API JetGetCursorInfo(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a><span data-ttu-id="e782d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e782d-108">Parameters</span></span>

<span data-ttu-id="e782d-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e782d-109">*sesid*</span></span>

<span data-ttu-id="e782d-110">La sesión que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e782d-110">The session that will be used for this call.</span></span>

<span data-ttu-id="e782d-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="e782d-111">*tableid*</span></span>

<span data-ttu-id="e782d-112">Cursor que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e782d-112">The cursor that will be used for this call.</span></span>

<span data-ttu-id="e782d-113">*pvResult*</span><span class="sxs-lookup"><span data-stu-id="e782d-113">*pvResult*</span></span>

<span data-ttu-id="e782d-114">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e782d-114">Reserved for future use.</span></span>

<span data-ttu-id="e782d-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="e782d-115">*cbMax*</span></span>

<span data-ttu-id="e782d-116">Debe establecerse en 0 (cero); de lo contrario, no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e782d-116">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="e782d-117">Está presente para futuras funciones.</span><span class="sxs-lookup"><span data-stu-id="e782d-117">It is present for future functionality.</span></span>

<span data-ttu-id="e782d-118">*InfoLevel*</span><span class="sxs-lookup"><span data-stu-id="e782d-118">*InfoLevel*</span></span>

<span data-ttu-id="e782d-119">Debe establecerse en 0 (cero); de lo contrario, no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e782d-119">Must be set to 0 (zero), otherwise unused.</span></span> <span data-ttu-id="e782d-120">Está presente para futuras funciones.</span><span class="sxs-lookup"><span data-stu-id="e782d-120">It is present for future functionality.</span></span>

### <a name="return-value"></a><span data-ttu-id="e782d-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e782d-121">Return Value</span></span>

<span data-ttu-id="e782d-122">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="e782d-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e782d-123">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e782d-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e782d-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e782d-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="e782d-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="e782d-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e782d-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e782d-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e782d-127">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e782d-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e782d-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e782d-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e782d-129">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e782d-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e782d-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e782d-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e782d-131">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="e782d-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e782d-132">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e782d-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e782d-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="e782d-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="e782d-134"><em>CbMax</em> no es 0 (cero) o <em>InfoLevel</em> no es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="e782d-134">Either <em>cbMax</em> is not 0 (zero) or <em>InfoLevel</em> is not 0 (zero).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e782d-135">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="e782d-135">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="e782d-136">El cursor no está actualmente en un registro y no se puede devolver información sobre un registro lógico como resultado.</span><span class="sxs-lookup"><span data-stu-id="e782d-136">The cursor is not currently on a record and information on a logical record cannot be returned as a result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e782d-137">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e782d-137">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e782d-138">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e782d-138">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e782d-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e782d-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e782d-140">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e782d-140">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e782d-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e782d-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e782d-142">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e782d-142">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="e782d-143">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e782d-143">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e782d-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e782d-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e782d-145">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e782d-145">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e782d-146">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="e782d-146">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="e782d-147">El registro actual del cursor se ha actualizado en otra sesión y una actualización de este registro en esta sesión producirá un conflicto de escritura.</span><span class="sxs-lookup"><span data-stu-id="e782d-147">The current record of the cursor has been updated by another session and an update of this record by this session will result in a write conflict.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e782d-148">Si se realiza correctamente, esta operación no tiene ningún efecto en la ubicación del cursor, pero solo indica que ninguna otra sesión actualizó actualmente este registro.</span><span class="sxs-lookup"><span data-stu-id="e782d-148">On success, this operation has no effect on the location of the cursor but only indicates that no other session has currently updated this record.</span></span>

<span data-ttu-id="e782d-149">En caso de error, si se devuelve un código de error negativo, no se produce ningún efecto en el cursor o en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e782d-149">On failure, if a negative error code is returned there are no effects to the cursor or the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e782d-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e782d-150">Remarks</span></span>

<span data-ttu-id="e782d-151">Esta operación no afecta al estado del cursor o de los datos.</span><span class="sxs-lookup"><span data-stu-id="e782d-151">This operation does not affect the state of the cursor or the data.</span></span> <span data-ttu-id="e782d-152">Solo devuelve un código de error que describe si se sabe que una actualización del registro actual por la sesión que realiza la llamada da como resultado un JET_errWriteConflict, o se desconoce para devolver JET_errWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="e782d-152">It only returns an error code describing whether an update to the current record by the calling session is known to result in a JET_errWriteConflict, or is unknown to return JET_errWriteConflict.</span></span> <span data-ttu-id="e782d-153">Si otra sesión ya ha actualizado este registro para usarlo, está seguro de que una actualización de este registro en esta sesión producirá un conflicto de escritura.</span><span class="sxs-lookup"><span data-stu-id="e782d-153">If another session has already updated this record to use it is certain that an update of this record by this session will result in a write conflict.</span></span> <span data-ttu-id="e782d-154">Esto será así hasta que esta sesión se confirme o revierta sus transacciones al nivel de transacción 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="e782d-154">This will be true until this session commits or rolls back its transactions to transaction level 0 (zero).</span></span> <span data-ttu-id="e782d-155">Sin embargo, si **JetGetCursorInfo** devuelve JET_errSuccess, sigue siendo posible que otra sesión actualice este registro antes de la sesión actual y, por lo tanto, siga siendo posible que una actualización del registro actual por esta sesión en su transacción actual produzca un conflicto de escritura.</span><span class="sxs-lookup"><span data-stu-id="e782d-155">However, if **JetGetCursorInfo** returns JET_errSuccess, it is still possible for another session to update this record before the current session and thus it is still possible that an update of the current record by this session in its current transaction will result in a write conflict.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e782d-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e782d-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e782d-157"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e782d-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e782d-158">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e782d-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e782d-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e782d-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e782d-160">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="e782d-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e782d-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e782d-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e782d-162">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="e782d-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e782d-163"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="e782d-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e782d-164">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e782d-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e782d-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e782d-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e782d-166">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e782d-166">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e782d-167">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e782d-167">See Also</span></span>

[<span data-ttu-id="e782d-168">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e782d-168">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e782d-169">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e782d-169">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e782d-170">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="e782d-170">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="e782d-171">JetGetLock</span><span class="sxs-lookup"><span data-stu-id="e782d-171">JetGetLock</span></span>](./jetgetlock-function.md)  
[<span data-ttu-id="e782d-172">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="e782d-172">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="e782d-173">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e782d-173">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="e782d-174">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="e782d-174">JetUpdate</span></span>](./jetupdate-function.md)
