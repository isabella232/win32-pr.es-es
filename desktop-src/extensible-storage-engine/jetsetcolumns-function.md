---
description: 'Más información acerca de: JetSetColumns (función)'
title: Función JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4535b66064c19257f4bb7b51b059453660916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153767"
---
# <a name="jetsetcolumns-function"></a><span data-ttu-id="f2d88-103">Función JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="f2d88-103">JetSetColumns Function</span></span>


<span data-ttu-id="f2d88-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f2d88-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcolumns-function"></a><span data-ttu-id="f2d88-105">Función JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="f2d88-105">JetSetColumns Function</span></span>

<span data-ttu-id="f2d88-106">La función **JetSetColumns** tiene un comportamiento similar al de [JetSetColumn](./jetsetcolumn-function.md) , pero permite que una aplicación establezca varios valores de columna en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="f2d88-106">The **JetSetColumns** function is similar in behavior to [JetSetColumn](./jetsetcolumn-function.md) but allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="f2d88-107">Una matriz de estructuras [JET_SETCOLUMN](./jet-setcolumn-structure.md) se utiliza para describir el conjunto de valores de columna que se va a establecer y para describir los búferes de entrada de cada valor de columna que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f2d88-107">An array of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="f2d88-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2d88-108">Parameters</span></span>

<span data-ttu-id="f2d88-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f2d88-109">*sesid*</span></span>

<span data-ttu-id="f2d88-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="f2d88-110">The session to use for this call.</span></span>

<span data-ttu-id="f2d88-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="f2d88-111">*tableid*</span></span>

<span data-ttu-id="f2d88-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="f2d88-112">The cursor to use for this call.</span></span>

<span data-ttu-id="f2d88-113">*psetcolumn*</span><span class="sxs-lookup"><span data-stu-id="f2d88-113">*psetcolumn*</span></span>

<span data-ttu-id="f2d88-114">Puntero a una matriz de una o varias estructuras de [JET_SETCOLUMN](./jet-setcolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="f2d88-114">A pointer to an array of one or more [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures.</span></span> <span data-ttu-id="f2d88-115">Cada estructura incluye descripciones de los valores de columna que se van a establecer y desde dónde obtener los datos de columna que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="f2d88-115">Each structure includes descriptions of which column value to set and from where to get column data to set.</span></span>

<span data-ttu-id="f2d88-116">*csetcolumn*</span><span class="sxs-lookup"><span data-stu-id="f2d88-116">*csetcolumn*</span></span>

<span data-ttu-id="f2d88-117">El número de estructuras [JET_SETCOLUMN](./jet-setcolumn-structure.md) en la matriz dada por *psetcolumn*.</span><span class="sxs-lookup"><span data-stu-id="f2d88-117">The number of [JET_SETCOLUMN](./jet-setcolumn-structure.md) structures in the array given by *psetcolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="f2d88-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2d88-118">Return Value</span></span>

<span data-ttu-id="f2d88-119">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="f2d88-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f2d88-120">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f2d88-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2d88-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f2d88-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="f2d88-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2d88-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-123">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="f2d88-123">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="f2d88-124">El ID. de columna especificado está fuera de los límites legales de un identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="f2d88-124">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f2d88-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f2d88-126">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f2d88-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-127">JET_errColumnIllegalNull</span><span class="sxs-lookup"><span data-stu-id="f2d88-127">JET_errColumnIllegalNull</span></span></p></td>
<td><p><span data-ttu-id="f2d88-128">Igual que JET_errNullInvalid.</span><span class="sxs-lookup"><span data-stu-id="f2d88-128">Same as JET_errNullInvalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-129">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="f2d88-129">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="f2d88-130">La columna descrita por el <em>columnid</em> determinado no existe en la tabla.</span><span class="sxs-lookup"><span data-stu-id="f2d88-130">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-131">JET_errColumnNotUpdatable</span><span class="sxs-lookup"><span data-stu-id="f2d88-131">JET_errColumnNotUpdatable</span></span></p></td>
<td><p><span data-ttu-id="f2d88-132">Se intentó actualizar un valor Long durante una operación de eliminación de la actualización original.</span><span class="sxs-lookup"><span data-stu-id="f2d88-132">An illegal attempt was made to update a long value during a insert copy delete original update operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-133">JET_errColumnTooBig</span><span class="sxs-lookup"><span data-stu-id="f2d88-133">JET_errColumnTooBig</span></span></p></td>
<td><p><span data-ttu-id="f2d88-134">Los datos de los valores de columna especificados en el búfer de entrada superan el límite de tamaño, ya sea natural para una columna de longitud fija o configurados para columnas binarias o de texto de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="f2d88-134">The given column value data given in the input buffer exceeds the size limitation either natural for a fixed length column or configured for fixed length text or binary columns.</span></span> <span data-ttu-id="f2d88-135">Este error también se devuelve al pasar más de 1024 bytes de datos para una columna larga y al establecer la marca de JET_bitSetIntrinsicLV.</span><span class="sxs-lookup"><span data-stu-id="f2d88-135">This error is also returned when passing more than 1024 bytes of data for a long column and setting the JET_bitSetIntrinsicLV flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f2d88-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f2d88-137">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="f2d88-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f2d88-138">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f2d88-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-139">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="f2d88-139">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="f2d88-140">El tamaño de los datos del valor de la columna dado no coincide con el tipo de datos de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="f2d88-140">The given column value data size does not match what is natural for the fixed length data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-141">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="f2d88-141">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="f2d88-142">Se realizó un intento no válido de actualizar una columna de incremento automático durante una operación de inserción o actualización, o bien para actualizar una columna de versión durante una operación de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="f2d88-142">An illegal attempt was made to update an auto-increment column either during an insert or update operation, or to update a version column during a replace operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-143">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="f2d88-143">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="f2d88-144">Las opciones proporcionadas son desconocidas o una combinación no válida de valores de bits conocidos.</span><span class="sxs-lookup"><span data-stu-id="f2d88-144">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="f2d88-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="f2d88-146">El psetinfo especificado- &gt; cbStruct no es un tamaño válido para la estructura de <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> .</span><span class="sxs-lookup"><span data-stu-id="f2d88-146">The given psetinfo-&gt;cbStruct is not a valid size for the <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-147">JET_errMultiValuedDuplicate</span><span class="sxs-lookup"><span data-stu-id="f2d88-147">JET_errMultiValuedDuplicate</span></span></p></td>
<td><p><span data-ttu-id="f2d88-148">La operación establecer columna intentó crear un valor duplicado y especificó JET_bitSetUniqueMultiValues o JET_bitSetUniqueNormalizedMultiValues.</span><span class="sxs-lookup"><span data-stu-id="f2d88-148">The set column operation attempted to create a duplicate value and specified either JET_bitSetUniqueMultiValues or JET_bitSetUniqueNormalizedMultiValues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-149">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f2d88-149">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f2d88-150">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="f2d88-150">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-151">JET_errNotInTransaction</span><span class="sxs-lookup"><span data-stu-id="f2d88-151">JET_errNotInTransaction</span></span></p></td>
<td><p><span data-ttu-id="f2d88-152">Se intentó actualizar un valor de columna largo cuando la sesión que realiza la llamada no se encontraba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="f2d88-152">An illegal attempt was made to update a long column value when the calling session was not in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-153">JET_errNullInvalid</span><span class="sxs-lookup"><span data-stu-id="f2d88-153">JET_errNullInvalid</span></span></p></td>
<td><p><span data-ttu-id="f2d88-154">Se hizo un intento no válido de establecer una columna que no es NULL en NULL.</span><span class="sxs-lookup"><span data-stu-id="f2d88-154">An illegal attempt was made to set a non-NULL column to NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-155">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="f2d88-155">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="f2d88-156">No se pudo establecer el valor de la columna en el valor del búfer de entrada porque habría hecho que el registro superara su límite de tamaño de página relacionado.</span><span class="sxs-lookup"><span data-stu-id="f2d88-156">The column value could not be set to the value in the input buffer because it would have caused the record to exceed its page size related size limitation.</span></span> <span data-ttu-id="f2d88-157">Las columnas de tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> o <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> pueden almacenarse independientemente de los datos de registro restantes.</span><span class="sxs-lookup"><span data-stu-id="f2d88-157">Columns of type <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> can be stored separately from the remaining record data.</span></span> <span data-ttu-id="f2d88-158">Sin embargo, otras columnas deben almacenarse con el registro y pueden provocar que se supere la limitación del tamaño del registro.</span><span class="sxs-lookup"><span data-stu-id="f2d88-158">However, other columns must be stored with the record and can cause the record size limitation to be exceeded.</span></span> <span data-ttu-id="f2d88-159">Las columnas de tipo Long requieren 5 bytes de espacio en el registro como una vinculación y esto puede provocar que se devuelva JET_errRecordTooBig.</span><span class="sxs-lookup"><span data-stu-id="f2d88-159">Even long columns require 5-bytes of space within the record as a linkage and this too can lead to JET_errRecordTooBig being returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-160">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f2d88-160">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f2d88-161">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="f2d88-161">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-162">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f2d88-162">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f2d88-163">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f2d88-163">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="f2d88-164">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f2d88-164">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-165">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f2d88-165">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f2d88-166">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="f2d88-166">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-167">JET_errUpdateNotPrepared</span><span class="sxs-lookup"><span data-stu-id="f2d88-167">JET_errUpdateNotPrepared</span></span></p></td>
<td><p><span data-ttu-id="f2d88-168">El cursor no está actualmente en proceso de insertar un nuevo registro o actualizar un registro existente.</span><span class="sxs-lookup"><span data-stu-id="f2d88-168">The cursor is not currently in the process of either inserting a new record or updating an existing record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="f2d88-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="f2d88-170">El valor de la columna en el búfer de entrada superó la longitud máxima configurada para una columna de longitud variable y se truncó.</span><span class="sxs-lookup"><span data-stu-id="f2d88-170">The column value in the input buffer exceeded the maximum configured length for a variable length column and was truncated.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f2d88-171">Si se ejecuta correctamente, para cada columna descrita en psetcolumns, la parte deseada del valor de la columna se establece con datos copiados desde el búfer de entrada.</span><span class="sxs-lookup"><span data-stu-id="f2d88-171">On success, for each column described in the psetcolumns, the desired portion of the column value is set with data copied from the input buffer.</span></span> <span data-ttu-id="f2d88-172">Es posible que se haya truncado el conjunto de datos de la columna si se superó la longitud máxima especificada para una columna de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="f2d88-172">The column data set may have been truncated if it exceeded the maximum length specified for a variable length column.</span></span>

<span data-ttu-id="f2d88-173">En caso de error, la ubicación del cursor permanece sin cambios y no se actualiza ningún dato del valor de columna en el búfer de copia.</span><span class="sxs-lookup"><span data-stu-id="f2d88-173">On failure, the cursor location is left unchanged and no column value data is updated in the copy buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f2d88-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2d88-174">Remarks</span></span>

<span data-ttu-id="f2d88-175">Si alguna operación individual de una columna devuelve un error, la operación **JetSetColumns** completa devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="f2d88-175">If any individual set column operation returns an error then the whole **JetSetColumns** operation will return an error.</span></span> <span data-ttu-id="f2d88-176">En general, las advertencias se devuelven en psetcolumns- \> error y no en el código de retorno de esta función.</span><span class="sxs-lookup"><span data-stu-id="f2d88-176">Warnings, in general, are returned in the psetcolumns-\>error and not in the return code from this function.</span></span> <span data-ttu-id="f2d88-177">Sin embargo, si el último conjunto de columnas tiene una advertencia, esta advertencia se devolverá desde **JetSetColumns** .</span><span class="sxs-lookup"><span data-stu-id="f2d88-177">However, if the last column set has a warning, then this warning will be returned from **JetSetColumns** itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f2d88-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2d88-178">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-179"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f2d88-179"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f2d88-180">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f2d88-180">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-181"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f2d88-181"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f2d88-182">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f2d88-182">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-183"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f2d88-183"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f2d88-184">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="f2d88-184">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2d88-185"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="f2d88-185"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f2d88-186">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="f2d88-186">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2d88-187"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="f2d88-187"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f2d88-188">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f2d88-188">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f2d88-189">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f2d88-189">See Also</span></span>

[<span data-ttu-id="f2d88-190">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="f2d88-190">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="f2d88-191">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f2d88-191">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f2d88-192">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f2d88-192">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f2d88-193">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f2d88-193">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f2d88-194">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="f2d88-194">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="f2d88-195">JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="f2d88-195">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)  
[<span data-ttu-id="f2d88-196">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="f2d88-196">JetSetColumn</span></span>](./jetsetcolumn-function.md)
