---
description: 'Más información acerca de: JetUpdate (función)'
title: Función JetUpdate
TOCTitle: JetUpdate Function
ms:assetid: 6c9a53d0-46bc-403b-bdba-9020e023c14a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269288(v=EXCHG.10)
ms:contentKeyID: 32765580
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38e17c5bc5ac32ab3b904456f2d97aa465fca670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908112"
---
# <a name="jetupdate-function"></a><span data-ttu-id="bd3b1-103">Función JetUpdate</span><span class="sxs-lookup"><span data-stu-id="bd3b1-103">JetUpdate Function</span></span>


<span data-ttu-id="bd3b1-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bd3b1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate-function"></a><span data-ttu-id="bd3b1-105">Función JetUpdate</span><span class="sxs-lookup"><span data-stu-id="bd3b1-105">JetUpdate Function</span></span>

<span data-ttu-id="bd3b1-106">La función **JetUpdate** realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-106">The **JetUpdate** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="bd3b1-107">La eliminación de una fila de tabla se realiza mediante una llamada a [JetDelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd3b1-107">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="bd3b1-108">**JetUpdate** es el último paso para realizar una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-108">**JetUpdate** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="bd3b1-109">La actualización se inicia llamando a [JetPrepareUpdate](./jetprepareupdate-function.md) y llamando a [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o varias veces para establecer el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-109">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="bd3b1-110">Por último, se llama a **JetUpdate** para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-110">Finally, **JetUpdate** is called to complete the update operation.</span></span> <span data-ttu-id="bd3b1-111">Los índices solo se actualizan mediante **JetUpdate** o [JetUpdate2](./jetupdate2-function.md)y no durante [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="bd3b1-111">Indexes are updated only by **JetUpdate** or [JetUpdate2](./jetupdate2-function.md), and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="bd3b1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd3b1-112">Parameters</span></span>

<span data-ttu-id="bd3b1-113">*sesid*</span><span class="sxs-lookup"><span data-stu-id="bd3b1-113">*sesid*</span></span>

<span data-ttu-id="bd3b1-114">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-114">The session to use for this call.</span></span>

<span data-ttu-id="bd3b1-115">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="bd3b1-115">*tableid*</span></span>

<span data-ttu-id="bd3b1-116">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-116">The cursor to use for this call.</span></span>

<span data-ttu-id="bd3b1-117">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="bd3b1-117">*pvBookmark*</span></span>

<span data-ttu-id="bd3b1-118">Puntero a un marcador devuelto para una fila insertada.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-118">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="bd3b1-119">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="bd3b1-119">*cbBookmark*</span></span>

<span data-ttu-id="bd3b1-120">Tamaño del búfer al que apunta *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-120">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="bd3b1-121">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="bd3b1-121">*pcbActual*</span></span>

<span data-ttu-id="bd3b1-122">Tamaño devuelto del marcador de la fila insertada que se devuelve en *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-122">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

### <a name="return-value"></a><span data-ttu-id="bd3b1-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd3b1-123">Return Value</span></span>

<span data-ttu-id="bd3b1-124">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bd3b1-125">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bd3b1-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd3b1-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bd3b1-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="bd3b1-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd3b1-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bd3b1-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-129">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-130">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="bd3b1-130">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-131">El búfer especificado para el marcador de registro no es lo suficientemente grande como para almacenar el marcador de registro.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-131">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-132">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bd3b1-132">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-133">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-133">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-134">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="bd3b1-134">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-135">Igual que JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-135">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-136">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="bd3b1-136">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-137">La operación de actualización requiere el crecimiento del archivo de base de datos o la asignación del archivo de registro, pero la unidad de disco donde reside el archivo de base de datos o la serie de registro está llena.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-137">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="bd3b1-138">Como alternativa, el archivo de base de datos se encuentra en un volumen con formato FAT32 y el archivo de base de datos ya está 4GBytes, el límite por archivo para FAT32.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-138">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bd3b1-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-140">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="bd3b1-141"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-141"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="bd3b1-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-143">El parámetro <em>Prep</em> proporcionado en la función <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> no es una marca válida.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-143">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-144">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="bd3b1-144">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-145">Una clave de índice para este registro es un duplicado de otra clave de índice para otro registro que ya está en la tabla y el índice no permite duplicados.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-145">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-146">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="bd3b1-146">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-147">El registro insertado o actualizado tiene uno o más índices para los que la clave generada habría superado el tamaño máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-147">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="bd3b1-148">Como resultado, la operación no ha podido evitar el truncamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-148">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-149">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="bd3b1-149">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-150">El registro insertado o actualizado tiene una columna de varios valores indizada con dos o más valores que son idénticos en el tamaño de la clave de longitud máxima establecido para el índice.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-150">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="bd3b1-151">Como resultado, el registro tiene dos entradas idénticas en el índice que no son válidas.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-151">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bd3b1-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-153">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-153">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-154">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="bd3b1-154">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-155">Una o más columnas del registro que se van a insertar o en el estado actualizado de un registro que se va a reemplazar es <strong>null</strong> , lo que infringe la restricción definida para esas columnas.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-155">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-156">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="bd3b1-156">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-157">Uno o más índices están definidos para no permitir una clave <strong>null</strong> y el estado insertado o actualizado de un registro que se está reemplazando infringe esta restricción definida.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-157">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-158">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="bd3b1-158">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-159">Una operación de reemplazo de registro ha actualizado la clave principal.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-159">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="bd3b1-160">Las actualizaciones de las columnas de clave principal se deben realizar a través de la eliminación del registro existente e inserción de un nuevo registro con los datos deseados.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-160">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bd3b1-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-162">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="bd3b1-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-164">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-164">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="bd3b1-165"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-165"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bd3b1-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-167">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-168">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="bd3b1-168">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-169">No es válido intentar una actualización cuando se encuentra dentro del ámbito de una transacción de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-169">It is illegal to attempt an update when inside the scope of a read only transaction.</span></span> <span data-ttu-id="bd3b1-170">Una transacción de solo lectura es una transacción que se ha iniciado mediante una llamada a <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> con JET_bitTransactionReadOnly.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-170">A read only transaction is a transaction that has been started using a call to <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> with JET_bitTransactionReadOnly.</span></span></p>
<p><span data-ttu-id="bd3b1-171"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-171"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-172">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="bd3b1-172">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-173">Se llamó a <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> con JET_prepCancel pero el cursor no estaba en el estado preparado.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-173"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-174">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="bd3b1-174">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-175">No se pudo realizar la operación porque no hay suficiente memoria para conservar la información transaccional acerca de la actualización.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-175">The operation failed because there is not enough memory to retain transactional information about the update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-176">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="bd3b1-176">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="bd3b1-177">Otra sesión ha bloqueado previamente el registro para su actualización.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-177">Another session has previously locked the record for update.</span></span> <span data-ttu-id="bd3b1-178">Se producirá un error en la actualización intentada por esta sesión.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-178">The update attempted by this session will fail.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bd3b1-179">Si se ejecuta correctamente, se completa la operación de actualización abierta en el cursor.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-179">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="bd3b1-180">Si se define una columna de incremento automático para la tabla, este valor se establece para los registros insertados.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-180">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="bd3b1-181">Si se define una columna de versión para la tabla, su valor se inicializa para los registros recién insertados o se incrementa cada vez que se reemplaza un registro.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-181">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="bd3b1-182">Se actualizan todos los índices, incluidos los índices agrupados y no clúster.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-182">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="bd3b1-183">En caso de error, no se realiza ningún cambio de ningún tipo en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-183">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="bd3b1-184">Antes de que se haya llamado a las funciones de devolución de llamada Insert y Before, no se habrá llamado a las devoluciones de llamada Insert y After Replace, ya que este último no puede hacer que se produzca un error en una actualización.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-184">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="bd3b1-185">El búfer de copia del cursor se deja en su estado preparado, por lo que existe la oportunidad de corregir incrementalmente los problemas que provocaron errores y volver a intentar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-185">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bd3b1-186">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd3b1-186">Remarks</span></span>

<span data-ttu-id="bd3b1-187">Las funciones de devolución de llamada se pueden registrar para que se llamen antes o después de la inserción, y antes o después de la actualización.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-187">Callback functions can be registered to be called before or after insert, and before or after update.</span></span>

<span data-ttu-id="bd3b1-188">Las limitaciones de tamaño de registro se aplican mediante [JetSetColumn](./jetsetcolumn-function.md)y no en general por **JetUpdate**.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by **JetUpdate**.</span></span>

<span data-ttu-id="bd3b1-189">Es importante entender el impacto de realizar un gran número de operaciones de actualización dentro de una única transacción.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-189">It is important to understand the impact of performing a large number of update operations inside of a single transaction.</span></span> <span data-ttu-id="bd3b1-190">El motor de base de datos debe realizar el seguimiento de cada actualización de la base de datos en el almacén de versiones.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-190">Each update to the database must be tracked by the database engine in the version store.</span></span> <span data-ttu-id="bd3b1-191">El almacén de versiones contiene un registro en directo de todas las versiones de cada entrada de registro o índice de la base de datos que pueden verse en todas las transacciones activas.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-191">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="bd3b1-192">Estas versiones se utilizan para admitir el control de simultaneidad con varias versiones que usa el motor de base de datos para admitir transacciones que usan el aislamiento de instantánea.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-192">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="bd3b1-193">Una vez que el motor de base de datos haya agotado los recursos usados para almacenar estas versiones, ya no podrá aceptar más cambios hasta que algunas transacciones hayan concluido para permitir la recuperación de estos recursos.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-193">Once the database engine has exhausted the resources used to store these versions then it can no longer accept further changes until some transactions have concluded to allow these resources to be reclaimed.</span></span> <span data-ttu-id="bd3b1-194">Cuando el motor está en este estado, se producirá un error en todas las actualizaciones con JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-194">When the engine is in this state, all updates will fail with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="bd3b1-195">Los recursos disponibles para el motor de base de datos para almacenar estas versiones se pueden controlar mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md) con [JET_paramMaxVerPages](./resource-parameters.md) y [JET_paramGlobalMinVerPages](./resource-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bd3b1-195">The resources available to the database engine to store these versions can be controlled using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramMaxVerPages](./resource-parameters.md) and [JET_paramGlobalMinVerPages](./resource-parameters.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="bd3b1-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd3b1-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-197"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bd3b1-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bd3b1-198">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-199"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bd3b1-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bd3b1-200">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-201"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bd3b1-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bd3b1-202">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd3b1-203"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="bd3b1-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bd3b1-204">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd3b1-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bd3b1-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bd3b1-206">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bd3b1-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bd3b1-207">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bd3b1-207">See Also</span></span>

[<span data-ttu-id="bd3b1-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bd3b1-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bd3b1-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="bd3b1-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="bd3b1-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bd3b1-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bd3b1-211">JetDelete</span><span class="sxs-lookup"><span data-stu-id="bd3b1-211">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="bd3b1-212">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="bd3b1-212">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="bd3b1-213">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="bd3b1-213">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="bd3b1-214">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="bd3b1-214">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="bd3b1-215">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="bd3b1-215">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="bd3b1-216">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="bd3b1-216">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="bd3b1-217">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="bd3b1-217">JetSetColumns</span></span>](./jetsetcolumns-function.md)  
[<span data-ttu-id="bd3b1-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="bd3b1-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="bd3b1-219">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="bd3b1-219">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
