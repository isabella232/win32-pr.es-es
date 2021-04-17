---
description: 'Más información acerca de: JetDupCursor (función)'
title: Función JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 590b9b08c5386aaf1cd2dd541ac496a5fa0871d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716821"
---
# <a name="jetdupcursor-function"></a><span data-ttu-id="653ee-103">Función JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="653ee-103">JetDupCursor Function</span></span>


<span data-ttu-id="653ee-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="653ee-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdupcursor-function"></a><span data-ttu-id="653ee-105">Función JetDupCursor</span><span class="sxs-lookup"><span data-stu-id="653ee-105">JetDupCursor Function</span></span>

<span data-ttu-id="653ee-106">La función **JetDupCursor** duplica un cursor abierto y devuelve un identificador al cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="653ee-106">The **JetDupCursor** function duplicates an open cursor and returns a handle to the duplicated cursor.</span></span> <span data-ttu-id="653ee-107">Si el cursor que se duplicó era un cursor de solo lectura, el cursor duplicado también es un cursor de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="653ee-107">If the cursor that was duplicated was a read-only cursor then the duplicated cursor is also a read-only cursor.</span></span> <span data-ttu-id="653ee-108">Cualquier estado relacionado con la creación de una clave de búsqueda o la actualización de un registro no se copia en el cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="653ee-108">Any state related to constructing a search key or updating a record is not copied into the duplicated cursor.</span></span> <span data-ttu-id="653ee-109">Además, la ubicación del cursor original no se duplica en el cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="653ee-109">In addition, the location of the original cursor is not duplicated into the duplicated cursor.</span></span> <span data-ttu-id="653ee-110">El cursor duplicado siempre se abre en el índice clúster y su ubicación siempre está en la primera fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="653ee-110">The duplicated cursor is always opened on the clustered index and its location is always on the first row of the table.</span></span>

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="653ee-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="653ee-111">Parameters</span></span>

<span data-ttu-id="653ee-112">*sesid*</span><span class="sxs-lookup"><span data-stu-id="653ee-112">*sesid*</span></span>

<span data-ttu-id="653ee-113">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="653ee-113">The session to use for this call.</span></span>

<span data-ttu-id="653ee-114">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="653ee-114">*tableid*</span></span>

<span data-ttu-id="653ee-115">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="653ee-115">The cursor to use for this call.</span></span>

<span data-ttu-id="653ee-116">*ptableid*</span><span class="sxs-lookup"><span data-stu-id="653ee-116">*ptableid*</span></span>

<span data-ttu-id="653ee-117">Puntero a *TABLEID*.</span><span class="sxs-lookup"><span data-stu-id="653ee-117">Pointer to *tableid*.</span></span>

<span data-ttu-id="653ee-118">*grbit*</span><span class="sxs-lookup"><span data-stu-id="653ee-118">*grbit*</span></span>

<span data-ttu-id="653ee-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="653ee-119">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="653ee-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="653ee-120">Return Value</span></span>

<span data-ttu-id="653ee-121">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="653ee-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="653ee-122">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="653ee-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="653ee-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="653ee-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="653ee-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="653ee-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="653ee-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="653ee-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="653ee-126">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="653ee-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="653ee-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="653ee-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="653ee-128">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="653ee-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="653ee-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="653ee-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="653ee-130">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="653ee-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="653ee-131">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="653ee-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="653ee-132">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="653ee-132">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="653ee-133">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="653ee-133">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="653ee-134">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="653ee-134">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="653ee-135">No existen recursos de cursor disponibles.</span><span class="sxs-lookup"><span data-stu-id="653ee-135">No available cursor resources exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="653ee-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="653ee-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="653ee-137">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="653ee-137">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="653ee-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="653ee-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="653ee-139">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="653ee-139">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="653ee-140">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="653ee-140">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="653ee-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="653ee-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="653ee-142">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="653ee-142">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="653ee-143">Si se ejecuta correctamente, *ptableid* se establece en un cursor duplicado.</span><span class="sxs-lookup"><span data-stu-id="653ee-143">On success, *ptableid* is set to a duplicated cursor.</span></span>

<span data-ttu-id="653ee-144">En caso de error, no se realiza ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="653ee-144">On failure, no changes are made.</span></span> <span data-ttu-id="653ee-145">El estado de *TABLEID* no se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="653ee-145">The state of *tableid* is unchanged.</span></span>

#### <a name="remarks"></a><span data-ttu-id="653ee-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="653ee-146">Remarks</span></span>

<span data-ttu-id="653ee-147">El cursor duplicado no ha copiado todo el estado del cursor.</span><span class="sxs-lookup"><span data-stu-id="653ee-147">The duplicated cursor does not have the entire cursor state copied.</span></span> <span data-ttu-id="653ee-148">La ubicación del cursor duplicado, incluido el índice actual, es normalmente diferente del cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="653ee-148">The location of the duplicated cursor, including the current index, is usually different from the given cursor.</span></span> <span data-ttu-id="653ee-149">Siempre se devuelve el cursor duplicado en el índice clúster y en la primera fila de la tabla.</span><span class="sxs-lookup"><span data-stu-id="653ee-149">The duplicated cursor is always returned on the clustered index and on the first row in the table.</span></span> <span data-ttu-id="653ee-150">Si la tabla está vacía, el cursor duplicado no se encuentra en ninguna fila.</span><span class="sxs-lookup"><span data-stu-id="653ee-150">If the table is empty, the duplicated cursor is not on any row.</span></span>

<span data-ttu-id="653ee-151">Las tablas abiertas con **JetDupCursor** normalmente se deben cerrar con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="653ee-151">Tables opened with **JetDupCursor** should usually be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="653ee-152">La excepción a esta regla se produce cuando se llama a **JetDupCursor** en una transacción y se revierte la transacción (con [JetRollback](./jetrollback-function.md)).</span><span class="sxs-lookup"><span data-stu-id="653ee-152">The exception to this rule happens when **JetDupCursor** is called in a transaction and the transaction is rolled back (with [JetRollback](./jetrollback-function.md)).</span></span> <span data-ttu-id="653ee-153">Cuando se revierte una transacción, el cursor se cierra automáticamente.</span><span class="sxs-lookup"><span data-stu-id="653ee-153">When rolling back a transaction, the cursor is automatically closed.</span></span> <span data-ttu-id="653ee-154">En este caso, es un error cerrar la tabla con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="653ee-154">In this case, it is an error to close the table with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="653ee-155">[JET_paramMaxOpenTables](./resource-parameters.md)puede ver directamente el número de tablas que se pueden abrir simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="653ee-155">The number of tables that can be opened simultaneously is affected directly by [JET_paramMaxOpenTables](./resource-parameters.md).</span></span> <span data-ttu-id="653ee-156">Consulte [parámetros del sistema](./extensible-storage-engine-system-parameters.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="653ee-156">See [System Parameters](./extensible-storage-engine-system-parameters.md) for details.</span></span>

#### <a name="requirements"></a><span data-ttu-id="653ee-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="653ee-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="653ee-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="653ee-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="653ee-159">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="653ee-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="653ee-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="653ee-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="653ee-161">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="653ee-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="653ee-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="653ee-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="653ee-163">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="653ee-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="653ee-164"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="653ee-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="653ee-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="653ee-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="653ee-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="653ee-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="653ee-167">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="653ee-167">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="653ee-168">Consulte también</span><span class="sxs-lookup"><span data-stu-id="653ee-168">See Also</span></span>

[<span data-ttu-id="653ee-169">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="653ee-169">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="653ee-170">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="653ee-170">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="653ee-171">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="653ee-171">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="653ee-172">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="653ee-172">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="653ee-173">JetRollback</span><span class="sxs-lookup"><span data-stu-id="653ee-173">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="653ee-174">JetStopService</span><span class="sxs-lookup"><span data-stu-id="653ee-174">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="653ee-175">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="653ee-175">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
