---
description: 'Más información acerca de: JetUpdate2 (función)'
title: Función JetUpdate2
TOCTitle: JetUpdate2 Function
ms:assetid: 125f372c-9c4c-4be8-b0df-bbf53d79e90b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269190(v=EXCHG.10)
ms:contentKeyID: 32765493
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetUpdate2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc08b26ebff33a68654ed33a2cb0539af1fa2a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809007"
---
# <a name="jetupdate2-function"></a><span data-ttu-id="dcde9-103">Función JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="dcde9-103">JetUpdate2 Function</span></span>


<span data-ttu-id="dcde9-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dcde9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetupdate2-function"></a><span data-ttu-id="dcde9-105">Función JetUpdate2</span><span class="sxs-lookup"><span data-stu-id="dcde9-105">JetUpdate2 Function</span></span>

<span data-ttu-id="dcde9-106">La función **JetUpdate2** realiza una operación de actualización que incluye la inserción de una nueva fila en una tabla o la actualización de una fila existente.</span><span class="sxs-lookup"><span data-stu-id="dcde9-106">The **JetUpdate2** function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="dcde9-107">Esta función contiene una lista de opciones de *grbit* que se pueden establecer al realizar una actualización.</span><span class="sxs-lookup"><span data-stu-id="dcde9-107">This function contains a list of *grbit* options that can be set while performing an update.</span></span> <span data-ttu-id="dcde9-108">La eliminación de una fila de tabla se realiza mediante una llamada a [JetDelete](./jetdelete-function.md).</span><span class="sxs-lookup"><span data-stu-id="dcde9-108">Deleting a table row is performed by calling [JetDelete](./jetdelete-function.md).</span></span>

<span data-ttu-id="dcde9-109">**Windows server 2003: JetUpdate2** se incorporó en windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dcde9-109">**Windows Server 2003:  JetUpdate2** is introduced in Windows Server 2003.</span></span>

<span data-ttu-id="dcde9-110">**JetUpdate2** es el último paso para realizar una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="dcde9-110">**JetUpdate2** is the final step in performing an insert or an update.</span></span> <span data-ttu-id="dcde9-111">La actualización se inicia llamando a [JetPrepareUpdate](./jetprepareupdate-function.md) y llamando a [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md) una o varias veces para establecer el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="dcde9-111">The update is begun by calling [JetPrepareUpdate](./jetprepareupdate-function.md) and then by calling [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md) one or more times to set the record state.</span></span> <span data-ttu-id="dcde9-112">Por último, se llama a **JetUpdate2** para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="dcde9-112">Finally, **JetUpdate2** is called to complete the update operation.</span></span> <span data-ttu-id="dcde9-113">Los índices solo se actualizan mediante [JetUpdate](./jetupdate-function.md) o **JetUpdate2** y no durante [JetSetColumn](./jetsetcolumn-function.md) o [JetSetColumns](./jetsetcolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="dcde9-113">Indexes are updated only by [JetUpdate](./jetupdate-function.md) or **JetUpdate2**, and not during [JetSetColumn](./jetsetcolumn-function.md) or [JetSetColumns](./jetsetcolumns-function.md).</span></span>

```cpp
    JET_ERR JET_API JetUpdate2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbBookmark,
      __out_opt     unsigned long* pcbActual,
      __in            const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="dcde9-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcde9-114">Parameters</span></span>

<span data-ttu-id="dcde9-115">*sesid*</span><span class="sxs-lookup"><span data-stu-id="dcde9-115">*sesid*</span></span>

<span data-ttu-id="dcde9-116">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="dcde9-116">The session to use for this call.</span></span>

<span data-ttu-id="dcde9-117">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="dcde9-117">*tableid*</span></span>

<span data-ttu-id="dcde9-118">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="dcde9-118">The cursor to use for this call.</span></span>

<span data-ttu-id="dcde9-119">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="dcde9-119">*pvBookmark*</span></span>

<span data-ttu-id="dcde9-120">Puntero a un marcador devuelto para una fila insertada.</span><span class="sxs-lookup"><span data-stu-id="dcde9-120">Pointer to a returned bookmark for an inserted row.</span></span>

<span data-ttu-id="dcde9-121">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="dcde9-121">*cbBookmark*</span></span>

<span data-ttu-id="dcde9-122">Tamaño del búfer al que apunta *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="dcde9-122">Size of the buffer pointed to by *pvBookmark*.</span></span>

<span data-ttu-id="dcde9-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="dcde9-123">*pcbActual*</span></span>

<span data-ttu-id="dcde9-124">Tamaño devuelto del marcador de la fila insertada que se devuelve en *pvBookmark*.</span><span class="sxs-lookup"><span data-stu-id="dcde9-124">The returned size of the bookmark for the inserted row returned in *pvBookmark*.</span></span>

<span data-ttu-id="dcde9-125">*grbit*</span><span class="sxs-lookup"><span data-stu-id="dcde9-125">*grbit*</span></span>

<span data-ttu-id="dcde9-126">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="dcde9-126">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcde9-127">Value</span><span class="sxs-lookup"><span data-stu-id="dcde9-127">Value</span></span></p></th>
<th><p><span data-ttu-id="dcde9-128">Significado</span><span class="sxs-lookup"><span data-stu-id="dcde9-128">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-129">JET_bitUpdateCheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="dcde9-129">JET_bitUpdateCheckESE97Compatibility</span></span></p></td>
<td><p><span data-ttu-id="dcde9-130">Esta marca hace que la actualización devuelva un error si la actualización no hubiera sido posible en la versión de Windows 2000 de ESE, que aplicó un número máximo menor de instancias de columna multivalor en cada registro que en versiones posteriores de ESE.</span><span class="sxs-lookup"><span data-stu-id="dcde9-130">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="dcde9-131">Esto solo es importante para las aplicaciones que desean replicar datos entre aplicaciones hospedadas en Windows 2000 y aplicaciones hospedadas en Windows Server 2003 o versiones posteriores de ESE.</span><span class="sxs-lookup"><span data-stu-id="dcde9-131">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows Server 2003, or later versions of ESE.</span></span> <span data-ttu-id="dcde9-132">No debe ser necesario para la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="dcde9-132">It should not be necessary for most applications.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="dcde9-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcde9-133">Return Value</span></span>

<span data-ttu-id="dcde9-134">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="dcde9-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="dcde9-135">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="dcde9-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcde9-136">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dcde9-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="dcde9-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcde9-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="dcde9-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="dcde9-139">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="dcde9-139">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-140">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="dcde9-140">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="dcde9-141">El búfer especificado para el marcador de registro no es lo suficientemente grande como para almacenar el marcador de registro.</span><span class="sxs-lookup"><span data-stu-id="dcde9-141">The given buffer for the record bookmark is not sufficiently large enough to store the record bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-142">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="dcde9-142">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="dcde9-143">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="dcde9-143">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-144">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="dcde9-144">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="dcde9-145">La operación de actualización requiere el crecimiento del archivo de base de datos o la asignación del archivo de registro, pero la unidad de disco donde reside el archivo de base de datos o la serie de registro está llena.</span><span class="sxs-lookup"><span data-stu-id="dcde9-145">The update operation requires database file growth, or log file allocation, but the disk drive where the database file or log series resides is full.</span></span> <span data-ttu-id="dcde9-146">Como alternativa, el archivo de base de datos se encuentra en un volumen con formato FAT32 y el archivo de base de datos ya está 4GBytes, el límite por archivo para FAT32.</span><span class="sxs-lookup"><span data-stu-id="dcde9-146">Alternatively, the database file is on a FAT32 formatted volume and the database file is already 4GBytes, the per file limit for FAT32.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="dcde9-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="dcde9-148">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="dcde9-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="dcde9-149"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcde9-149"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="dcde9-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="dcde9-151">El parámetro <em>Prep</em> proporcionado en la función <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> no es una marca válida.</span><span class="sxs-lookup"><span data-stu-id="dcde9-151">The given <em>prep</em> parameter in the <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> function is not a valid flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-152">JET_errKeyDuplicate</span><span class="sxs-lookup"><span data-stu-id="dcde9-152">JET_errKeyDuplicate</span></span></p></td>
<td><p><span data-ttu-id="dcde9-153">Una clave de índice para este registro es un duplicado de otra clave de índice para otro registro que ya está en la tabla y el índice no permite duplicados.</span><span class="sxs-lookup"><span data-stu-id="dcde9-153">An index key for this record is a duplicate of another index key for another record already in the table and the index does not allow duplicates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-154">JET_errKeyTruncated</span><span class="sxs-lookup"><span data-stu-id="dcde9-154">JET_errKeyTruncated</span></span></p></td>
<td><p><span data-ttu-id="dcde9-155">El registro insertado o actualizado tiene uno o más índices para los que la clave generada habría superado el tamaño máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="dcde9-155">The inserted or updated record has one or more indices for which the generated key would have exceeded the maximum allowable size.</span></span> <span data-ttu-id="dcde9-156">Como resultado, la operación no ha podido evitar el truncamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="dcde9-156">As a result, the operation has failed to prevent key truncation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-157">JET_errMultiValuedIndexViolation</span><span class="sxs-lookup"><span data-stu-id="dcde9-157">JET_errMultiValuedIndexViolation</span></span></p></td>
<td><p><span data-ttu-id="dcde9-158">El registro insertado o actualizado tiene una columna de varios valores indizada con dos o más valores que son idénticos en el tamaño de la clave de longitud máxima establecido para el índice.</span><span class="sxs-lookup"><span data-stu-id="dcde9-158">The inserted or updated record has an indexed multi-value column with two or more values that are identical within the maximum length key size set for the index.</span></span> <span data-ttu-id="dcde9-159">Como resultado, el registro tiene dos entradas idénticas en el índice que no son válidas.</span><span class="sxs-lookup"><span data-stu-id="dcde9-159">As a result, the record has two identical entries in the index which is invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="dcde9-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="dcde9-161">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dcde9-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-162">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="dcde9-162">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="dcde9-163">Una o más columnas del registro que se van a insertar o en el estado actualizado de un registro que se va a reemplazar es <strong>null</strong> , lo que infringe la restricción definida para esas columnas.</span><span class="sxs-lookup"><span data-stu-id="dcde9-163">One or more columns in the record to be inserted or in the updated state of a record being replace is <strong>NULL</strong> which violates the defined constraint for those columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-164">JET_errNullKeyDisallowed</span><span class="sxs-lookup"><span data-stu-id="dcde9-164">JET_errNullKeyDisallowed</span></span></p></td>
<td><p><span data-ttu-id="dcde9-165">Uno o más índices están definidos para no permitir una clave <strong>null</strong> y el estado insertado o actualizado de un registro que se está reemplazando infringe esta restricción definida.</span><span class="sxs-lookup"><span data-stu-id="dcde9-165">One or more indexes are defined not to allow a <strong>NULL</strong> key and the inserted or updated state of a record being replaced violates this defined constraint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-166">JET_errRecordPrimaryChanged</span><span class="sxs-lookup"><span data-stu-id="dcde9-166">JET_errRecordPrimaryChanged</span></span></p></td>
<td><p><span data-ttu-id="dcde9-167">Una operación de reemplazo de registro ha actualizado la clave principal.</span><span class="sxs-lookup"><span data-stu-id="dcde9-167">A record replacement operation has updated the primary key.</span></span> <span data-ttu-id="dcde9-168">Las actualizaciones de las columnas de clave principal se deben realizar a través de la eliminación del registro existente e inserción de un nuevo registro con los datos deseados.</span><span class="sxs-lookup"><span data-stu-id="dcde9-168">Updates to primary key columns must be done through deleting the existing record and inserting a new record with the desired data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-169">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="dcde9-169">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="dcde9-170">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dcde9-170">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-171">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="dcde9-171">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="dcde9-172">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="dcde9-172">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="dcde9-173"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dcde9-173"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-174">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="dcde9-174">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="dcde9-175">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="dcde9-175">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-176">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="dcde9-176">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="dcde9-177">Se llamó a <a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> con JET_prepCancel pero el cursor no estaba en el estado preparado.</span><span class="sxs-lookup"><span data-stu-id="dcde9-177"><a href="gg269339(v=exchg.10).md">JetPrepareUpdate</a> was called with JET_prepCancel but the cursor was not in the prepared state.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-178">JET_errWriteConflict</span><span class="sxs-lookup"><span data-stu-id="dcde9-178">JET_errWriteConflict</span></span></p></td>
<td><p><span data-ttu-id="dcde9-179">Una operación de reemplazo de registros para la que aún no se ha asignado un bloqueo de escritura puede producir un conflicto de escritura en el momento de la actualización.</span><span class="sxs-lookup"><span data-stu-id="dcde9-179">A record replacement operation for which a write lock was not already allocated can encounter a write conflict at the time of update.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="dcde9-180">Si se ejecuta correctamente, se completa la operación de actualización abierta en el cursor.</span><span class="sxs-lookup"><span data-stu-id="dcde9-180">On success, the open update operation on the cursor is completed.</span></span> <span data-ttu-id="dcde9-181">Si se define una columna de incremento automático para la tabla, este valor se establece para los registros insertados.</span><span class="sxs-lookup"><span data-stu-id="dcde9-181">If an auto-increment column is defined for the table, then this value is set for inserted records.</span></span> <span data-ttu-id="dcde9-182">Si se define una columna de versión para la tabla, su valor se inicializa para los registros recién insertados o se incrementa cada vez que se reemplaza un registro.</span><span class="sxs-lookup"><span data-stu-id="dcde9-182">If a version column is defined for the table, then its value is initialized for newly inserted records, or incremented each time a record is replaced.</span></span> <span data-ttu-id="dcde9-183">Se actualizan todos los índices, incluidos los índices agrupados y no clúster.</span><span class="sxs-lookup"><span data-stu-id="dcde9-183">All indexes, including clustered and non-clustered indexes are updated.</span></span>

<span data-ttu-id="dcde9-184">En caso de error, no se realiza ningún cambio de ningún tipo en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="dcde9-184">On failure, no changes of any kind are made to the database.</span></span> <span data-ttu-id="dcde9-185">Antes de que se haya llamado a las funciones de devolución de llamada Insert y Before, no se habrá llamado a las devoluciones de llamada Insert y After Replace, ya que este último no puede hacer que se produzca un error en una actualización.</span><span class="sxs-lookup"><span data-stu-id="dcde9-185">Before insert and before replace callback functions may have been called, but after insert and after replace callbacks will not have been called, since the latter cannot cause an update to fail.</span></span> <span data-ttu-id="dcde9-186">El búfer de copia del cursor se deja en su estado preparado, por lo que existe la oportunidad de corregir incrementalmente los problemas que provocaron errores y volver a intentar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="dcde9-186">The cursor copy buffer is left in its prepared state, so that the opportunity exists to incrementally correct the problems that caused errors and retry the update operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="dcde9-187">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcde9-187">Remarks</span></span>

<span data-ttu-id="dcde9-188">Las limitaciones de tamaño de registro se aplican mediante [JetSetColumn](./jetsetcolumn-function.md)y no en general por [JetUpdate](./jetupdate-function.md).</span><span class="sxs-lookup"><span data-stu-id="dcde9-188">Record size limitations are enforced by [JetSetColumn](./jetsetcolumn-function.md), and not in general by [JetUpdate](./jetupdate-function.md).</span></span> <span data-ttu-id="dcde9-189">La única excepción es cuando se utiliza la marca de compatibilidad de JET_bitUpdateCheckESE97Compatibility.</span><span class="sxs-lookup"><span data-stu-id="dcde9-189">The only exception is when the JET_bitUpdateCheckESE97Compatibility compatibility flag is being used.</span></span> <span data-ttu-id="dcde9-190">En este caso, se comprueba el registro completo, ya que una operación individual de [JetSetColumn](./jetsetcolumn-function.md) que superó el límite se puede compensar mediante una llamada subsiguiente a [JetSetColumn](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="dcde9-190">In this case, the whole record is checked since an individual [JetSetColumn](./jetsetcolumn-function.md) operation that exceeded the limit may be compensated by a subsequent call to [JetSetColumn](./jetsetcolumn-function.md).</span></span>

<span data-ttu-id="dcde9-191">Vea la sección Comentarios en [JetUpdate](./jetupdate-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="dcde9-191">See the Remarks section in [JetUpdate](./jetupdate-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="dcde9-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcde9-192">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-193"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="dcde9-193"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="dcde9-194">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dcde9-194">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-195"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="dcde9-195"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="dcde9-196">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dcde9-196">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-197"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="dcde9-197"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="dcde9-198">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="dcde9-198">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcde9-199"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="dcde9-199"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="dcde9-200">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="dcde9-200">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcde9-201"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="dcde9-201"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="dcde9-202">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="dcde9-202">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="dcde9-203">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dcde9-203">See Also</span></span>

[<span data-ttu-id="dcde9-204">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="dcde9-204">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="dcde9-205">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="dcde9-205">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="dcde9-206">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="dcde9-206">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="dcde9-207">JetDelete</span><span class="sxs-lookup"><span data-stu-id="dcde9-207">JetDelete</span></span>](./jetdelete-function.md)  
[<span data-ttu-id="dcde9-208">JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="dcde9-208">JetPrepareUpdate</span></span>](./jetprepareupdate-function.md)  
[<span data-ttu-id="dcde9-209">JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="dcde9-209">JetRegisterCallback</span></span>](./jetregistercallback-function.md)  
[<span data-ttu-id="dcde9-210">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="dcde9-210">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="dcde9-211">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="dcde9-211">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="dcde9-212">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="dcde9-212">JetSetColumn</span></span>](./jetsetcolumn-function.md)  
[<span data-ttu-id="dcde9-213">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="dcde9-213">JetSetColumns</span></span>](./jetsetcolumns-function.md)
