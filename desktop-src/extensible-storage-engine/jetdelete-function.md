---
description: 'Más información acerca de: JetDelete (función)'
title: Función JetDelete
TOCTitle: JetDelete Function
ms:assetid: 807de5ba-2f4b-4779-ab29-a1f094beecc1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269315(v=EXCHG.10)
ms:contentKeyID: 32765605
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDelete
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f3422bc623bbd4f0cc99365df51bb797100811c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648537"
---
# <a name="jetdelete-function"></a><span data-ttu-id="1809a-103">Función JetDelete</span><span class="sxs-lookup"><span data-stu-id="1809a-103">JetDelete Function</span></span>


<span data-ttu-id="1809a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1809a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdelete-function"></a><span data-ttu-id="1809a-105">Función JetDelete</span><span class="sxs-lookup"><span data-stu-id="1809a-105">JetDelete Function</span></span>

<span data-ttu-id="1809a-106">La función **JetDelete** elimina el registro actual de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1809a-106">The **JetDelete** function deletes the current record in a database table.</span></span>

```cpp
    JET_ERR JET_API JetDelete(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="1809a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1809a-107">Parameters</span></span>

<span data-ttu-id="1809a-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="1809a-108">*sesid*</span></span>

<span data-ttu-id="1809a-109">Contexto de sesión de base de datos que se usará para la llamada de API.</span><span class="sxs-lookup"><span data-stu-id="1809a-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="1809a-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="1809a-110">*tableid*</span></span>

<span data-ttu-id="1809a-111">Cursor en una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1809a-111">The cursor on a database table.</span></span> <span data-ttu-id="1809a-112">Se eliminará la fila actual.</span><span class="sxs-lookup"><span data-stu-id="1809a-112">The current row will be deleted.</span></span>

### <a name="return-value"></a><span data-ttu-id="1809a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1809a-113">Return Value</span></span>

<span data-ttu-id="1809a-114">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="1809a-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="1809a-115">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1809a-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1809a-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1809a-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="1809a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1809a-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1809a-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="1809a-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="1809a-119">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1809a-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-120">JET_errCallbackFailed</span><span class="sxs-lookup"><span data-stu-id="1809a-120">JET_errCallbackFailed</span></span></p></td>
<td><p><span data-ttu-id="1809a-121">Error en la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1809a-121">The callback function failed in some manner.</span></span> <span data-ttu-id="1809a-122">Por ejemplo, las infracciones de acceso de las funciones de devolución de llamada se detectan y traducen en JET_errCallbackFailed.</span><span class="sxs-lookup"><span data-stu-id="1809a-122">For example, access violations in callback functions are caught and translated into JET_errCallbackFailed.</span></span> <span data-ttu-id="1809a-123">Este error solo lo devolverá Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1809a-123">This error will only be returned by Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="1809a-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="1809a-125">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="1809a-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-126">JET_errIllegalOperation</span><span class="sxs-lookup"><span data-stu-id="1809a-126">JET_errIllegalOperation</span></span></p></td>
<td><p><span data-ttu-id="1809a-127">El cursor especificado por <em>TABLEID</em> no admite la eliminación.</span><span class="sxs-lookup"><span data-stu-id="1809a-127">The cursor specified by <em>tableid</em> does not support deletion.</span></span> <span data-ttu-id="1809a-128">Consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1809a-128">See the Remarks section.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="1809a-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="1809a-130">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="1809a-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="1809a-131">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1809a-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="1809a-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="1809a-133">El cursor especificado por <em>TABLEID</em> no está en un registro.</span><span class="sxs-lookup"><span data-stu-id="1809a-133">The cursor specified by <em>tableid</em> is not on a record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-134">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="1809a-134">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="1809a-135">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="1809a-135">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="1809a-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="1809a-137">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="1809a-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-138">JET_errPermissionDenied</span><span class="sxs-lookup"><span data-stu-id="1809a-138">JET_errPermissionDenied</span></span></p></td>
<td><p><span data-ttu-id="1809a-139">El motor de base de datos no tiene permisos suficientes para eliminar el registro.</span><span class="sxs-lookup"><span data-stu-id="1809a-139">The database engine does not have sufficient permissions to delete the record.</span></span> <span data-ttu-id="1809a-140">Esto puede ocurrir si el archivo de base de datos se abrió con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1809a-140">This may happen if the database file was opened with read-only access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-141">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="1809a-141">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="1809a-142">Existe un búfer de actualización (vea <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>), pero no todos los cambios realizados en las columnas de tipo JET_coltypLongText y/o las columnas de tipo JET_coltypLongBinary se pueden revertir.</span><span class="sxs-lookup"><span data-stu-id="1809a-142">An update buffer (see <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a>) exists, but not all of the changes made to columns of type JET_coltypLongText and/or columns of type JET_coltypLongBinary could be rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-143">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="1809a-143">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="1809a-144">No es válido utilizar la misma sesión desde más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="1809a-144">It is illegal to use the same session from more than one thread at the same time.</span></span> <span data-ttu-id="1809a-145">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1809a-145">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="1809a-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="1809a-147">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="1809a-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-148">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="1809a-148">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="1809a-149">La transacción es una transacción de solo lectura y no admite eliminaciones.</span><span class="sxs-lookup"><span data-stu-id="1809a-149">The transaction is a read-only transaction, and does not support deletes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-150">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="1809a-150">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="1809a-151">No se pudo realizar la operación porque no hay suficiente memoria para conservar la información transaccional acerca de la actualización.</span><span class="sxs-lookup"><span data-stu-id="1809a-151">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-152">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="1809a-152">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="1809a-153">Otra sesión ha bloqueado previamente el registro para su actualización.</span><span class="sxs-lookup"><span data-stu-id="1809a-153">Another session has previously locked the record for update.</span></span> <span data-ttu-id="1809a-154">Se producirá un error en la actualización intentada por esta sesión.</span><span class="sxs-lookup"><span data-stu-id="1809a-154">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1809a-155">Si se ejecuta correctamente, la moneda se deja justo antes del Registro siguiente.</span><span class="sxs-lookup"><span data-stu-id="1809a-155">On success, the currency is left just before the next record.</span></span> <span data-ttu-id="1809a-156">Si el registro eliminado fue el último de la tabla, la moneda se deja al final de la tabla (es decir, después del último registro).</span><span class="sxs-lookup"><span data-stu-id="1809a-156">If the deleted record was the last in the table, the currency is left at the end of the table (that is, after the new last record).</span></span> <span data-ttu-id="1809a-157">Si el registro eliminado era el único registro de la tabla, la moneda se establece en el principio.</span><span class="sxs-lookup"><span data-stu-id="1809a-157">If the deleted record was the only record in the table, the currency is set to the beginning.</span></span>

<span data-ttu-id="1809a-158">Los índices adecuados se actualizan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="1809a-158">The appropriate indexes are automatically updated.</span></span>

<span data-ttu-id="1809a-159">Si se prepara una actualización (mediante [JetPrepareUpdate](./jetprepareupdate-function.md)), se cancelará.</span><span class="sxs-lookup"><span data-stu-id="1809a-159">If an update is prepared (using [JetPrepareUpdate](./jetprepareupdate-function.md)), it will be canceled.</span></span> <span data-ttu-id="1809a-160">Se restablecerá el búfer de actualización.</span><span class="sxs-lookup"><span data-stu-id="1809a-160">The update buffer will be reset.</span></span>

<span data-ttu-id="1809a-161">En caso de error, la moneda permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="1809a-161">On failure, the currency remains unchanged.</span></span> <span data-ttu-id="1809a-162">Si se prepara una actualización (consulte [JetPrepareUpdate](./jetprepareupdate-function.md)), se puede restablecer el búfer de actualización.</span><span class="sxs-lookup"><span data-stu-id="1809a-162">If an update is prepared (see [JetPrepareUpdate](./jetprepareupdate-function.md)), the update buffer may be reset.</span></span>

#### <a name="remarks"></a><span data-ttu-id="1809a-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1809a-163">Remarks</span></span>

<span data-ttu-id="1809a-164">No todas las tablas admiten la eliminación de filas.</span><span class="sxs-lookup"><span data-stu-id="1809a-164">Not all tables support deletion of rows.</span></span> <span data-ttu-id="1809a-165">Normalmente, una tabla temporal no admite la eliminación de filas.</span><span class="sxs-lookup"><span data-stu-id="1809a-165">A temporary table does not normally support deletion of rows.</span></span> <span data-ttu-id="1809a-166">La eliminación de registros puede estar habilitada en tablas temporales por muchas razones, algunas de las cuales son:</span><span class="sxs-lookup"><span data-stu-id="1809a-166">Deletion of records may be enabled on temporary tables for many reasons, some of which are:</span></span>

  - <span data-ttu-id="1809a-167">Se especificó JET_bitTTUpdatable durante la creación.</span><span class="sxs-lookup"><span data-stu-id="1809a-167">JET_bitTTUpdatable was specified during creation.</span></span>

  - <span data-ttu-id="1809a-168">Las tablas temporales grandes pueden admitir la eliminación si se crearon con JET_bitTTScrollable o JET_bitTTIndexed.</span><span class="sxs-lookup"><span data-stu-id="1809a-168">Large temporary tables can support deletion if they were created with JET_bitTTScrollable or JET_bitTTIndexed.</span></span> <span data-ttu-id="1809a-169">El umbral en el que una tabla temporal se convierte en "grande" es actualmente de 64 kilobytes, pero se puede cambiar en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="1809a-169">The threshold at which a temporary table becomes "large" is currently 64 kilobytes, but it may be changed in future releases.</span></span>

<span data-ttu-id="1809a-170">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1809a-170">Windows XP and later.</span></span> <span data-ttu-id="1809a-171">Las funciones de devolución de llamada se pueden invocar mediante **JetDelete**, incluidos JET_cbtypBeforeDelete y JET_cbtypAfterDelete.</span><span class="sxs-lookup"><span data-stu-id="1809a-171">Callback functions can be invoked by **JetDelete**, including JET_cbtypBeforeDelete and JET_cbtypAfterDelete.</span></span>

<span data-ttu-id="1809a-172">Es importante entender el impacto de realizar un gran número de operaciones de actualización dentro de una única transacción.</span><span class="sxs-lookup"><span data-stu-id="1809a-172">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="1809a-173">El motor de base de datos debe realizar el seguimiento de cada actualización de la base de datos en el almacén de versiones.</span><span class="sxs-lookup"><span data-stu-id="1809a-173">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="1809a-174">El almacén de versiones contiene un registro en directo de todas las versiones de cada entrada de registro o índice de la base de datos que pueden verse en todas las transacciones activas.</span><span class="sxs-lookup"><span data-stu-id="1809a-174">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="1809a-175">Estas versiones se utilizan para admitir el control de simultaneidad con varias versiones que usa el motor de base de datos para admitir transacciones que usan el aislamiento de instantánea.</span><span class="sxs-lookup"><span data-stu-id="1809a-175">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="1809a-176">Una vez que el motor de base de datos haya agotado los recursos usados para almacenar estas versiones, ya no podrá aceptar más cambios hasta que algunas transacciones hayan concluido para permitir la recuperación de estos recursos.</span><span class="sxs-lookup"><span data-stu-id="1809a-176">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="1809a-177">Cuando el motor está en este estado, se producirá un error en todas las actualizaciones con JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1809a-177">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="1809a-178">Los recursos disponibles para el motor de base de datos para almacenar estas versiones se pueden controlar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con *JET_paramMaxVerPages* y *JET_paramGlobalMinVerPages*.</span><span class="sxs-lookup"><span data-stu-id="1809a-178">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with *JET_paramMaxVerPages* and *JET_paramGlobalMinVerPages*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="1809a-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1809a-179">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1809a-180"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="1809a-180"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1809a-181">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1809a-181">Requires Windows Vista, Windows XP or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-182"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1809a-182"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1809a-183">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1809a-183">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-184"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1809a-184"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1809a-185">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="1809a-185">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1809a-186"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="1809a-186"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="1809a-187">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="1809a-187">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1809a-188"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="1809a-188"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="1809a-189">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="1809a-189">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="1809a-190">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1809a-190">See Also</span></span>

[<span data-ttu-id="1809a-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="1809a-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="1809a-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="1809a-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="1809a-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="1809a-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="1809a-194">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="1809a-194">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="1809a-195">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="1809a-195">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="1809a-196">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="1809a-196">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
