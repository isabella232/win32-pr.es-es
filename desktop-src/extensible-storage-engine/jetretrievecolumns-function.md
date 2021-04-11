---
description: 'Más información acerca de: JetRetrieveColumns (función)'
title: Función JetRetrieveColumns
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 515be3a36932c9a56843f51d2e1b32a41ca94e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278935"
---
# <a name="jetretrievecolumns-function"></a><span data-ttu-id="57dc6-103">Función JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="57dc6-103">JetRetrieveColumns Function</span></span>


<span data-ttu-id="57dc6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="57dc6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievecolumns-function"></a><span data-ttu-id="57dc6-105">Función JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="57dc6-105">JetRetrieveColumns Function</span></span>

<span data-ttu-id="57dc6-106">La función **JetRetrieveColumns** Recupera varios valores de columna del registro actual en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="57dc6-106">The **JetRetrieveColumns** function retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="57dc6-107">Una matriz de estructuras [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) se utiliza para describir el conjunto de valores de columna que se va a recuperar y para describir los búferes de salida de cada valor de columna que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="57dc6-107">An array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a><span data-ttu-id="57dc6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57dc6-108">Parameters</span></span>

<span data-ttu-id="57dc6-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="57dc6-109">*sesid*</span></span>

<span data-ttu-id="57dc6-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="57dc6-110">The session to use for this call.</span></span>

<span data-ttu-id="57dc6-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="57dc6-111">*tableid*</span></span>

<span data-ttu-id="57dc6-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="57dc6-112">The cursor to use for this call.</span></span>

<span data-ttu-id="57dc6-113">*pretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="57dc6-113">*pretrievecolumn*</span></span>

<span data-ttu-id="57dc6-114">Puntero a una matriz de una o varias estructuras de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="57dc6-114">A pointer to an array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="57dc6-115">Cada estructura incluye descripciones de qué valor de columna recuperar y dónde almacenar los datos devueltos.</span><span class="sxs-lookup"><span data-stu-id="57dc6-115">Each structure includes descriptions of which column value to retrieve and where to store returned data.</span></span>

<span data-ttu-id="57dc6-116">*cretrievecolumn*</span><span class="sxs-lookup"><span data-stu-id="57dc6-116">*cretrievecolumn*</span></span>

<span data-ttu-id="57dc6-117">El número de estructuras [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) en la matriz dada por *pretrievecolumn*.</span><span class="sxs-lookup"><span data-stu-id="57dc6-117">The number of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures in the array given by *pretrievecolumn*.</span></span>

### <a name="return-value"></a><span data-ttu-id="57dc6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57dc6-118">Return Value</span></span>

<span data-ttu-id="57dc6-119">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="57dc6-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="57dc6-120">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="57dc6-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="57dc6-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="57dc6-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="57dc6-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="57dc6-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="57dc6-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="57dc6-124">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="57dc6-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-125">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="57dc6-125">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="57dc6-126">Se pasó un valor de número de secuencia de columna con varios valores no válido en pretinfo- &gt; itagSequence.</span><span class="sxs-lookup"><span data-stu-id="57dc6-126">An invalid multi-valued column sequence number value has been passed in pretinfo-&gt;itagSequence.</span></span> <span data-ttu-id="57dc6-127">Los valores válidos para los números de secuencia de valores de columna con varios valores son 1 o superior.</span><span class="sxs-lookup"><span data-stu-id="57dc6-127">Valid values for the multi-valued column value sequence numbers are 1 or greater.</span></span> <span data-ttu-id="57dc6-128">Un valor de 0 (cero) es válido para esta función, pero no es válido para <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="57dc6-128">A value of 0 (zero) is valid for this function but is invalid for <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-129">JET_errBadColumnId</span><span class="sxs-lookup"><span data-stu-id="57dc6-129">JET_errBadColumnId</span></span></p></td>
<td><p><span data-ttu-id="57dc6-130">El ID. de columna especificado está fuera de los límites legales de un identificador de columna.</span><span class="sxs-lookup"><span data-stu-id="57dc6-130">The column ID given is outside the legal limits of a column ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="57dc6-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="57dc6-132">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="57dc6-132">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-133">JET_errColumnNotFound</span><span class="sxs-lookup"><span data-stu-id="57dc6-133">JET_errColumnNotFound</span></span></p></td>
<td><p><span data-ttu-id="57dc6-134">La columna descrita por el <em>columnid</em> determinado no existe en la tabla.</span><span class="sxs-lookup"><span data-stu-id="57dc6-134">The column described by the given <em>columnid</em> does not exist in the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-135">JET_errIndexTuplesCannotRetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="57dc6-135">JET_errIndexTuplesCannotRetrieveFromIndex</span></span></p></td>
<td><p><span data-ttu-id="57dc6-136">Las columnas indizadas como subcadenas no se pueden recuperar del índice, puesto que solo una pequeña parte de la columna está presente normalmente en cada entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="57dc6-136">Columns indexed as substrings cannot be retrieved from the index, since only a small portion of the column is typically present in each index entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-137">JET_errInvalidBufferSize</span><span class="sxs-lookup"><span data-stu-id="57dc6-137">JET_errInvalidBufferSize</span></span></p></td>
<td><p><span data-ttu-id="57dc6-138">En algunos casos, el búfer proporcionado para la columna de recuperación debe tener el tamaño suficiente para poder devolver cualquier cantidad de valor de columna.</span><span class="sxs-lookup"><span data-stu-id="57dc6-138">In some cases, the buffer given for the retrieve column must be sufficiently sized in order to return any amount of the column value.</span></span> <span data-ttu-id="57dc6-139">Por ejemplo, las columnas actualizables de custodia se ajustan para ser coherentes con el contexto transaccional de la sesión de llamada y este ajuste requiere el búfer proporcionado por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="57dc6-139">For example, escrow updatable columns are adjusted to be consistent for the transactional context of the calling session and this adjustment requires the buffer provided by the caller.</span></span> <span data-ttu-id="57dc6-140">Si se proporciona espacio en búfer insuficiente, se devuelve JET_errInvalidBufferSize y no se devuelve ningún dato de columna.</span><span class="sxs-lookup"><span data-stu-id="57dc6-140">If insufficient buffer space is supplied, then JET_errInvalidBufferSize is returned and no column data whatsoever is returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-141">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="57dc6-141">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="57dc6-142">Las opciones proporcionadas son desconocidas o una combinación no válida de valores de bits conocidos.</span><span class="sxs-lookup"><span data-stu-id="57dc6-142">The options supplied are unknown or an illegal combination of known bit settings.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="57dc6-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="57dc6-144">Uno o varios de los parámetros especificados no son correctos.</span><span class="sxs-lookup"><span data-stu-id="57dc6-144">One or more of the parameters given is incorrect.</span></span> <span data-ttu-id="57dc6-145">Esto puede ocurrir si retinfo. cbStruct es más pequeño que el tamaño de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span><span class="sxs-lookup"><span data-stu-id="57dc6-145">This can happen if the retinfo.cbStruct is smaller that the size of <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-146">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="57dc6-146">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="57dc6-147">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="57dc6-147">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="57dc6-148"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="57dc6-148"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-149">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="57dc6-149">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="57dc6-150">El cursor no está situado en un registro.</span><span class="sxs-lookup"><span data-stu-id="57dc6-150">The cursor is not positioned on a record.</span></span> <span data-ttu-id="57dc6-151">Esto puede ocurrir por diversos motivos.</span><span class="sxs-lookup"><span data-stu-id="57dc6-151">This can happen for many different reasons.</span></span> <span data-ttu-id="57dc6-152">Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="57dc6-152">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="57dc6-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="57dc6-154">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="57dc6-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-155">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="57dc6-155">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="57dc6-156">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="57dc6-156">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-157">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="57dc6-157">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="57dc6-158">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="57dc6-158">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="57dc6-159"><strong>Windows XP:</strong>  Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="57dc6-159"><strong>Windows XP:</strong>  This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="57dc6-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="57dc6-161">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="57dc6-161">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-162">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="57dc6-162">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="57dc6-163">No se pudo recuperar el valor de columna completo porque el búfer especificado es menor que el tamaño de la columna.</span><span class="sxs-lookup"><span data-stu-id="57dc6-163">The entire column value could not be retrieved because the given buffer is smaller than the size of the column.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="57dc6-164">Si se ejecuta correctamente, se devuelven los datos de columnas y el tamaño de columna en los búferes proporcionados descritos en la matriz de estructuras [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="57dc6-164">On success, columns data and column size are returned in provided buffers described in array of [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structures.</span></span> <span data-ttu-id="57dc6-165">Si un *itagSequence* se ha establecido en 0 (cero) para indicar que se desea el número de instancias de un campo con varios valores en lugar de los datos de la columna, el número de instancias de una columna con varios valores se devuelve en el propio campo *itagSequence* .</span><span class="sxs-lookup"><span data-stu-id="57dc6-165">If an *itagSequence* was set to 0 (zero) to indicate that the number of instances of a multi-valued field was desired instead of column data, then the number of instances of a multi-valued column is returned in the *itagSequence* field itself.</span></span> <span data-ttu-id="57dc6-166">Cada estructura de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) tiene un campo de error que contiene advertencias para la columna recuperada.</span><span class="sxs-lookup"><span data-stu-id="57dc6-166">Each [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure has an error field that contains warnings for the column retrieved.</span></span> <span data-ttu-id="57dc6-167">Si el valor de la columna era **null** , el código de error se establecerá en JET_wrnColumnNull.</span><span class="sxs-lookup"><span data-stu-id="57dc6-167">If the column was **NULL** valued, then the error code will be set to JET_wrnColumnNull.</span></span>

<span data-ttu-id="57dc6-168">En caso de error, la ubicación del cursor se deja sin modificar y no se copia ningún dato en el búfer proporcionado.</span><span class="sxs-lookup"><span data-stu-id="57dc6-168">On failure, the cursor location is left unchanged and no data is copied into the provided buffer.</span></span>

#### <a name="remarks"></a><span data-ttu-id="57dc6-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57dc6-169">Remarks</span></span>

<span data-ttu-id="57dc6-170">**JetRetrieveColumns** admite una característica que [JetRetrieveColumn](./jetretrievecolumn-function.md) no.</span><span class="sxs-lookup"><span data-stu-id="57dc6-170">**JetRetrieveColumns** supports one feature that [JetRetrieveColumn](./jetretrievecolumn-function.md) does not.</span></span> <span data-ttu-id="57dc6-171">Se trata de la capacidad de recuperar el número de instancias de una columna con varios valores.</span><span class="sxs-lookup"><span data-stu-id="57dc6-171">This is the ability to retrieve the number of instances of a multi-valued column.</span></span> <span data-ttu-id="57dc6-172">La finalidad de esta característica es permitir que una aplicación recupere todos los valores de una columna.</span><span class="sxs-lookup"><span data-stu-id="57dc6-172">The purpose of this feature is to allow an application to retrieve all values of a column.</span></span> <span data-ttu-id="57dc6-173">Esto se puede hacer determinando primero el número de valores que tiene una columna.</span><span class="sxs-lookup"><span data-stu-id="57dc6-173">This can be done by first determining the number of values that a column has.</span></span> <span data-ttu-id="57dc6-174">A continuación, se pueden determinar sus longitudes llamando a **JetRetrieveColumns** de nuevo con una [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) estructura asignada para cada valor para determinar la longitud de los datos de la columna.</span><span class="sxs-lookup"><span data-stu-id="57dc6-174">Next, their lengths can be determined by calling **JetRetrieveColumns** again with one [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) structure allocated for each value to determine the length of column data.</span></span> <span data-ttu-id="57dc6-175">Esto se puede hacer pasando los punteros **null**_pvData_ con *cbMax* de 0 (cero) y recuperando la longitud de la columna en *cbActual*.</span><span class="sxs-lookup"><span data-stu-id="57dc6-175">This can be done by passing **NULL**_pvData_ pointers with *cbMax* of 0 (zero) and retrieving the column length in *cbActual*.</span></span> <span data-ttu-id="57dc6-176">La tercera y última llamada se puede realizar con memoria asignada para los datos del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="57dc6-176">The third and last call can be made with allocated memory for the column value data.</span></span>

<span data-ttu-id="57dc6-177">Si alguna columna recuperada se trunca debido a un búfer de longitud insuficiente, la API devolverá JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="57dc6-177">If any column retrieved is truncated due to an insufficient length buffer, then the API will return JET_wrnBufferTruncated.</span></span> <span data-ttu-id="57dc6-178">Sin embargo, otros errores, JET_wrnColumnNull se devuelven solo en el campo error de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="57dc6-178">However, other errors, JET_wrnColumnNull are returned only in the error field in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="57dc6-179">La razón de esto es que las aplicaciones suelen querer asegurarse de que todos los datos se han recuperado y devolver este error de **JetRetrieveColumns** facilita esta comprensión.</span><span class="sxs-lookup"><span data-stu-id="57dc6-179">The reason for this is that applications often want to ensure that all data has been retrieved and returning this error from **JetRetrieveColumns** facilitates this understanding.</span></span>

#### <a name="requirements"></a><span data-ttu-id="57dc6-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57dc6-180">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-181"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="57dc6-181"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="57dc6-182">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="57dc6-182">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-183"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="57dc6-183"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="57dc6-184">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="57dc6-184">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-185"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="57dc6-185"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="57dc6-186">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="57dc6-186">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="57dc6-187"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="57dc6-187"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="57dc6-188">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="57dc6-188">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="57dc6-189"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="57dc6-189"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="57dc6-190">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="57dc6-190">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="57dc6-191">Consulte también</span><span class="sxs-lookup"><span data-stu-id="57dc6-191">See Also</span></span>

[<span data-ttu-id="57dc6-192">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="57dc6-192">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="57dc6-193">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="57dc6-193">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="57dc6-194">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="57dc6-194">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="57dc6-195">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="57dc6-195">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="57dc6-196">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="57dc6-196">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="57dc6-197">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="57dc6-197">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="57dc6-198">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="57dc6-198">JetSetColumns</span></span>](./jetsetcolumns-function.md)
