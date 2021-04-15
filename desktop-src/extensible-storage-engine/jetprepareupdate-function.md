---
description: 'Más información acerca de: JetPrepareUpdate (función)'
title: JetPrepareUpdate función)
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649277"
---
# <a name="jetprepareupdate-function"></a><span data-ttu-id="a55ab-103">JetPrepareUpdate función)</span><span class="sxs-lookup"><span data-stu-id="a55ab-103">JetPrepareUpdate Function</span></span>


<span data-ttu-id="a55ab-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a55ab-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetprepareupdate-function"></a><span data-ttu-id="a55ab-105">JetPrepareUpdate función)</span><span class="sxs-lookup"><span data-stu-id="a55ab-105">JetPrepareUpdate Function</span></span>

<span data-ttu-id="a55ab-106">La función **JetPrepareUpdate** es la primera operación de realizar una actualización, con el fin de insertar un nuevo registro o reemplazar un registro existente con nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="a55ab-106">The **JetPrepareUpdate** function is the first operation in performing an update, for the purposes of inserting a new record or replacing an existing record with new values.</span></span> <span data-ttu-id="a55ab-107">Las actualizaciones se realizan llamando a **JetPrepareUpdate**, llamando a [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) cero o más veces y finalmente llamando a [JetUpdate](./jetupdate-function.md) para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="a55ab-107">Updates are done by calling **JetPrepareUpdate**, then calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) zero or more times and finally by calling [JetUpdate](./jetupdate-function.md) to complete the operation.</span></span> <span data-ttu-id="a55ab-108">**JetPrepareUpdate** y [JetUpdate](./jetupdate-function.md) establecen los límites para una operación de actualización y son importantes para tener solo el estado de actualización final de un registro escrito en los índices.</span><span class="sxs-lookup"><span data-stu-id="a55ab-108">**JetPrepareUpdate** and [JetUpdate](./jetupdate-function.md) set the boundaries for an update operation and are important in having only the final update state of a record entered into indexes.</span></span> <span data-ttu-id="a55ab-109">Esto es más eficaz, pero también es necesario en los casos en los que los datos deben coincidir con un estado válido a través de más de en la operación de establecer columna.</span><span class="sxs-lookup"><span data-stu-id="a55ab-109">This is both more efficient, but also required in cases where data must match a valid state through more than on set column operation.</span></span>

<span data-ttu-id="a55ab-110">Hay algunas opciones diferentes para insertar o reemplazar registros y se describen con más detalle a continuación.</span><span class="sxs-lookup"><span data-stu-id="a55ab-110">There are a few different options for inserting or replacing records and they are described in more detail below.</span></span>

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a><span data-ttu-id="a55ab-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a55ab-111">Parameters</span></span>

<span data-ttu-id="a55ab-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a55ab-112">*sesid*</span></span>

<span data-ttu-id="a55ab-113">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a55ab-113">The session to use for this call.</span></span>

<span data-ttu-id="a55ab-114">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="a55ab-114">*tableid*</span></span>

<span data-ttu-id="a55ab-115">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a55ab-115">The cursor to use for this call.</span></span>

<span data-ttu-id="a55ab-116">*porcentaje*</span><span class="sxs-lookup"><span data-stu-id="a55ab-116">*prep*</span></span>

<span data-ttu-id="a55ab-117">Las opciones que se pueden usar para preparar una actualización, que incluyen lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a55ab-117">The options that can be used to prepare for an update, which include the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a55ab-118">Value</span><span class="sxs-lookup"><span data-stu-id="a55ab-118">Value</span></span></p></th>
<th><p><span data-ttu-id="a55ab-119">Significado</span><span class="sxs-lookup"><span data-stu-id="a55ab-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-120">JET_prepCancel</span><span class="sxs-lookup"><span data-stu-id="a55ab-120">JET_prepCancel</span></span></p></td>
<td><p><span data-ttu-id="a55ab-121">Esta marca hace que <strong>JetPrepareUpdate</strong> cancele la actualización de este cursor.</span><span class="sxs-lookup"><span data-stu-id="a55ab-121">This flag causes <strong>JetPrepareUpdate</strong> to cancel the update for this cursor.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-122">JET_prepInsert</span><span class="sxs-lookup"><span data-stu-id="a55ab-122">JET_prepInsert</span></span></p></td>
<td><p><span data-ttu-id="a55ab-123">Esta marca hace que el cursor se prepare para una inserción de un nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="a55ab-123">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="a55ab-124">Todos los datos se inicializan en el estado predeterminado del registro.</span><span class="sxs-lookup"><span data-stu-id="a55ab-124">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="a55ab-125">Si la tabla tiene una columna de incremento automático, se asigna un nuevo valor a este registro independientemente de si la actualización se realiza en última instancia, si se produce un error o se cancela.</span><span class="sxs-lookup"><span data-stu-id="a55ab-125">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-126">JET_prepInsertCopy</span><span class="sxs-lookup"><span data-stu-id="a55ab-126">JET_prepInsertCopy</span></span></p></td>
<td><p><span data-ttu-id="a55ab-127">Esta marca hace que el cursor se prepare para una inserción de una copia del registro existente.</span><span class="sxs-lookup"><span data-stu-id="a55ab-127">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="a55ab-128">Debe haber un registro actual si se usa esta opción.</span><span class="sxs-lookup"><span data-stu-id="a55ab-128">There must be a current record if this option is used.</span></span> <span data-ttu-id="a55ab-129">El estado inicial del nuevo registro se copia del registro actual.</span><span class="sxs-lookup"><span data-stu-id="a55ab-129">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="a55ab-130">Los valores Long que se almacenan fuera de registro se copian de manera virtual.</span><span class="sxs-lookup"><span data-stu-id="a55ab-130">Long values that are stored off-record are virtually copied.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-131">JET_prepInsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="a55ab-131">JET_prepInsertCopyDeleteOriginal</span></span></p></td>
<td><p><span data-ttu-id="a55ab-132">Esta marca hace que el cursor se prepare para una inserción del mismo registro, y una eliminación o el registro original.</span><span class="sxs-lookup"><span data-stu-id="a55ab-132">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="a55ab-133">Se utiliza en casos en los que la clave principal ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="a55ab-133">It is used in cases in which the primary key has changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-134">JET_prepReplace</span><span class="sxs-lookup"><span data-stu-id="a55ab-134">JET_prepReplace</span></span></p></td>
<td><p><span data-ttu-id="a55ab-135">Esta marca hace que el cursor se prepare para un reemplazo del registro actual.</span><span class="sxs-lookup"><span data-stu-id="a55ab-135">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="a55ab-136">Si la tabla tiene una columna de versión, la columna versión se establece en el valor siguiente en su secuencia.</span><span class="sxs-lookup"><span data-stu-id="a55ab-136">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="a55ab-137">Si esta actualización no se completa, el valor de versión del registro no se verá afectado.</span><span class="sxs-lookup"><span data-stu-id="a55ab-137">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="a55ab-138">Se realiza un bloqueo de actualización en el registro para evitar que otras sesiones actualicen este registro antes de que se complete esta sesión.</span><span class="sxs-lookup"><span data-stu-id="a55ab-138">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-139">JET_prepReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="a55ab-139">JET_prepReplaceNoLock</span></span></p></td>
<td><p><span data-ttu-id="a55ab-140">Esta marca es similar a JET_prepReplace, pero no se realiza ningún bloqueo para evitar que otras sesiones actualicen este registro.</span><span class="sxs-lookup"><span data-stu-id="a55ab-140">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="a55ab-141">En su lugar, esta sesión puede recibir JET_errWriteConflict cuando llama a <a href="gg269288(v=exchg.10).md">JetUpdate</a> para completar la actualización.</span><span class="sxs-lookup"><span data-stu-id="a55ab-141">Instead, this session may receive JET_errWriteConflict when it calls <a href="gg269288(v=exchg.10).md">JetUpdate</a> to complete the update.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a55ab-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a55ab-142">Return Value</span></span>

<span data-ttu-id="a55ab-143">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="a55ab-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a55ab-144">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a55ab-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a55ab-145">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a55ab-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="a55ab-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="a55ab-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a55ab-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a55ab-148">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a55ab-148">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-149">JET_errAlreadyPrepared</span><span class="sxs-lookup"><span data-stu-id="a55ab-149">JET_errAlreadyPrepared</span></span></p></td>
<td><p><span data-ttu-id="a55ab-150">Se llamó a <strong>JetPrepareUpdate</strong> con una marca válida para Prep pero no JET_prepCancel y el cursor ya estaba en el estado preparado.</span><span class="sxs-lookup"><span data-stu-id="a55ab-150"><strong>JetPrepareUpdate</strong> was called with a valid flag for prep but not JET_prepCancel and the cursor was already in the prepared state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-151">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a55ab-151">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a55ab-152">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a55ab-152">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-153">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a55ab-153">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a55ab-154">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="a55ab-154">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="a55ab-155">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a55ab-155">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a55ab-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a55ab-157">La marca de preparación especificada no es una marca válida.</span><span class="sxs-lookup"><span data-stu-id="a55ab-157">The given prep flag is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a55ab-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a55ab-159">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a55ab-159">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-160">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="a55ab-160">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="a55ab-161">Se llamó a <strong>JetPrepareUpdate</strong> para reemplazar un registro que tenía columnas SLV.</span><span class="sxs-lookup"><span data-stu-id="a55ab-161"><strong>JetPrepareUpdate</strong> was called to replace a record which had SLV columns.</span></span> <span data-ttu-id="a55ab-162">Columnas SLV.</span><span class="sxs-lookup"><span data-stu-id="a55ab-162">SLV columns.</span></span> <span data-ttu-id="a55ab-163">Tenga en cuenta que las columnas de SLV son una característica no diseñada para el uso general.</span><span class="sxs-lookup"><span data-stu-id="a55ab-163">Please note that SLV columns are a feature not intended for general usage.</span></span> <span data-ttu-id="a55ab-164">Esta característica se usa para admitir la infraestructura de Microsoft Exchange y no está pensada para usarse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a55ab-164">This feature is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a55ab-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a55ab-166">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a55ab-166">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-167">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="a55ab-167">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="a55ab-168">Se llamó a <strong>JetPrepareUpdate</strong> con JET_prepCancel pero no se pudieron revertir todos los cambios realizados en las columnas de tipo JET_coltypLongText y/o las columnas de tipo JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="a55ab-168"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but could not rollback all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a55ab-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a55ab-170">Esta marca no se puede usar con la misma sesión desde más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a55ab-170">This flag cannot be used with the same session from more than one thread at the same time.</span></span> <span data-ttu-id="a55ab-171">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a55ab-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a55ab-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a55ab-173">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a55ab-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-174">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="a55ab-174">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="a55ab-175">Se llamó a <strong>JetPrepareUpdate</strong> con JET_prepCancel pero el cursor no estaba en el estado preparado.</span><span class="sxs-lookup"><span data-stu-id="a55ab-175"><strong>JetPrepareUpdate</strong> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a55ab-176">Si se ejecuta correctamente, el cursor cambia al estado preparado para el propósito de la actualización deseada, o en el caso de JET_prepCancel, el cursor se revierte al estado no preparado y se descartan los cambios.</span><span class="sxs-lookup"><span data-stu-id="a55ab-176">On success, the cursor is changed to the prepared state for the purpose of the desired update, or in the case of JET_prepCancel, the cursor is reverted to the non-prepared state and any changes are discarded.</span></span>

<span data-ttu-id="a55ab-177">En caso de error, el estado del cursor se deja sin modificar.</span><span class="sxs-lookup"><span data-stu-id="a55ab-177">On failure, the cursor state is left unchanged.</span></span> <span data-ttu-id="a55ab-178">Si el error se JET_errRollbackError, el estado del cursor cambia al estado no preparado pero no se han revertido todos los cambios.</span><span class="sxs-lookup"><span data-stu-id="a55ab-178">If the failure was JET_errRollbackError then the cursor state is changed to the non-prepared state but not all of the changes have been reverted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a55ab-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a55ab-179">Remarks</span></span>

<span data-ttu-id="a55ab-180">Insertar una copia de un registro es una optimización importante cuando los registros comparten datos de tipo JET_coltypLongText o JET_coltypLongBinary.</span><span class="sxs-lookup"><span data-stu-id="a55ab-180">Inserting a copy of a record is an important optimization when records share data of type JET_coltypLongText and/or JET_coltypLongBinary.</span></span> <span data-ttu-id="a55ab-181">Estos datos se almacenan de forma no grabada cuando son grandes y es posible que varios registros compartan la misma representación física de los datos.</span><span class="sxs-lookup"><span data-stu-id="a55ab-181">This data is stored off-record when large and it is possible for multiple records to share the same physical representation of the data.</span></span> <span data-ttu-id="a55ab-182">En este caso, los datos se pueden actualizar desde cualquier registro, pero si lo hace, se producirán ráfagas de datos de modo que cada registro tenga su propia copia.</span><span class="sxs-lookup"><span data-stu-id="a55ab-182">In this case, the data can be updated from either record, but doing so will cause the data to be burst such that each record has its own copy.</span></span> <span data-ttu-id="a55ab-183">No es posible cambiar los datos en un registro mediante una modificación de otro registro.</span><span class="sxs-lookup"><span data-stu-id="a55ab-183">It is not possible to change data in one record by a modification from another record.</span></span> <span data-ttu-id="a55ab-184">Además, no es posible bloquear una actualización de un registro mediante una actualización de otro registro.</span><span class="sxs-lookup"><span data-stu-id="a55ab-184">Also, it is not possible to block an update of one record by an update of another record.</span></span> <span data-ttu-id="a55ab-185">Se trata de una característica central de ESE y se conoce como bloqueo de nivel de registro.</span><span class="sxs-lookup"><span data-stu-id="a55ab-185">This is a central feature to ESE and is known as Record Level Locking.</span></span>

<span data-ttu-id="a55ab-186">Las operaciones de [JetUpdate](./jetupdate-function.md) que producen un error dejan el cursor en el estado de la preparación de la actualización.</span><span class="sxs-lookup"><span data-stu-id="a55ab-186">[JetUpdate](./jetupdate-function.md) operations which fail leave the cursor in the update prepared state.</span></span> <span data-ttu-id="a55ab-187">Esto es para permitir la corrección de algunos errores, como un valor de columna incorrecto, sin necesidad de volver a crear el estado de actualización.</span><span class="sxs-lookup"><span data-stu-id="a55ab-187">This is to permit correction to some errors, such as a wrong column value, without requiring the update state to be recreated.</span></span> <span data-ttu-id="a55ab-188">Esto significa que, en todos los casos en los que un cursor abandone una actualización, debe llamar explícitamente a **JetPrepareUpdate** con JET_prepCancel.</span><span class="sxs-lookup"><span data-stu-id="a55ab-188">This means that in all cases where a cursor abandons an update, it must explicitly call **JetPrepareUpdate** with JET_prepCancel.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a55ab-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a55ab-189">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-190"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a55ab-190"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a55ab-191">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a55ab-191">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-192"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a55ab-192"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a55ab-193">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a55ab-193">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-194"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a55ab-194"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a55ab-195">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a55ab-195">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a55ab-196"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="a55ab-196"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a55ab-197">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a55ab-197">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a55ab-198"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a55ab-198"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a55ab-199">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a55ab-199">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a55ab-200">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a55ab-200">See Also</span></span>

[<span data-ttu-id="a55ab-201">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a55ab-201">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a55ab-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a55ab-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a55ab-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a55ab-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a55ab-204">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="a55ab-204">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="a55ab-205">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="a55ab-205">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="a55ab-206">JetUpdate</span><span class="sxs-lookup"><span data-stu-id="a55ab-206">JetUpdate</span></span>](./jetupdate-function.md)
