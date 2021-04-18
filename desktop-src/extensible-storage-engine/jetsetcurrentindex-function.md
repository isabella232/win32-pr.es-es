---
description: 'Más información acerca de: JetSetCurrentIndex (función)'
title: Función JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715030"
---
# <a name="jetsetcurrentindex-function"></a><span data-ttu-id="9c04f-103">Función JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="9c04f-103">JetSetCurrentIndex Function</span></span>


<span data-ttu-id="9c04f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9c04f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex-function"></a><span data-ttu-id="9c04f-105">Función JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="9c04f-105">JetSetCurrentIndex Function</span></span>

<span data-ttu-id="9c04f-106">La función **JetSetCurrentIndex** se puede usar para establecer el índice actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="9c04f-106">The **JetSetCurrentIndex** function can be used to set the current index of a cursor.</span></span> <span data-ttu-id="9c04f-107">El índice actual de un cursor define qué registros de una tabla son visibles para ese cursor y el orden en que aparecen seleccionando el conjunto de entradas de índice que se van a usar para exponer esos registros.</span><span class="sxs-lookup"><span data-stu-id="9c04f-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="9c04f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c04f-108">Parameters</span></span>

<span data-ttu-id="9c04f-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9c04f-109">*sesid*</span></span>

<span data-ttu-id="9c04f-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="9c04f-110">The session to use for this call.</span></span>

<span data-ttu-id="9c04f-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="9c04f-111">*tableid*</span></span>

<span data-ttu-id="9c04f-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="9c04f-112">The cursor to use for this call.</span></span>

<span data-ttu-id="9c04f-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="9c04f-113">*szIndexName*</span></span>

<span data-ttu-id="9c04f-114">Nombre del índice que se va a seleccionar para el cursor.</span><span class="sxs-lookup"><span data-stu-id="9c04f-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="9c04f-115">Si este parámetro es NULL o una cadena vacía, se seleccionará el índice clúster.</span><span class="sxs-lookup"><span data-stu-id="9c04f-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="9c04f-116">Si se define un índice principal para la tabla, ese índice se seleccionará porque es el mismo que el índice clúster.</span><span class="sxs-lookup"><span data-stu-id="9c04f-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="9c04f-117">Si no hay ningún índice principal definido para la tabla, se seleccionará el índice secuencial.</span><span class="sxs-lookup"><span data-stu-id="9c04f-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="9c04f-118">El índice secuencial no tiene ninguna definición de índice.</span><span class="sxs-lookup"><span data-stu-id="9c04f-118">The sequential index has no index definition.</span></span> <span data-ttu-id="9c04f-119">Vea [JetCreateIndex](./jetcreateindex-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9c04f-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="9c04f-120">Si *pindexid* no es null, se omitirá el nombre del índice y el índice se seleccionará por su ID. de índice.</span><span class="sxs-lookup"><span data-stu-id="9c04f-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

### <a name="return-value"></a><span data-ttu-id="9c04f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c04f-121">Return Value</span></span>

<span data-ttu-id="9c04f-122">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="9c04f-122">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9c04f-123">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9c04f-123">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c04f-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9c04f-124">Return code</span></span></p></th>
<th><p><span data-ttu-id="9c04f-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c04f-125">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-126">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9c04f-126">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9c04f-127">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9c04f-127">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-128">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="9c04f-128">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="9c04f-129">Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ningún valor para la primera columna de clave de varios valores en la definición del nuevo índice que corresponde al número de secuencia especificado.</span><span class="sxs-lookup"><span data-stu-id="9c04f-129">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-130">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9c04f-130">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9c04f-131">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9c04f-131">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-132">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="9c04f-132">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="9c04f-133">El contenido del ID. de índice no era válido o expiró y debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="9c04f-133">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="9c04f-134">Esto puede ocurrir para <strong>JetSetCurrentIndex</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="9c04f-134">This can happen for <strong>JetSetCurrentIndex</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="9c04f-135">pindexid- &gt; cbStruct no tiene el tamaño esperado (Windows Server 2003 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="9c04f-135">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="9c04f-136">El motor se ha cerrado desde que se ha capturado el ID. de índice.</span><span class="sxs-lookup"><span data-stu-id="9c04f-136">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="9c04f-137">Todos los cursores que hacen referencia a la tabla que contiene el índice correspondiente al ID. de índice se han cerrado y el motor ha expulsado la definición de ese índice de la caché de esquema.</span><span class="sxs-lookup"><span data-stu-id="9c04f-137">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted that index's definition from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="9c04f-138">El ID. de índice se está usando con un cursor abierto en la tabla equivocada.</span><span class="sxs-lookup"><span data-stu-id="9c04f-138">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="9c04f-139">El índice se ha quitado o aún no está visible para la sesión.</span><span class="sxs-lookup"><span data-stu-id="9c04f-139">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9c04f-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9c04f-141">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="9c04f-141">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9c04f-142">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9c04f-142">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-143">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="9c04f-143">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="9c04f-144">Uno de los nombres de objeto especificados no era válido.</span><span class="sxs-lookup"><span data-stu-id="9c04f-144">One of the specified object names was invalid.</span></span> <span data-ttu-id="9c04f-145">Todos los nombres de objeto deben cumplir el mismo conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="9c04f-145">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="9c04f-146">Estas reglas son:</span><span class="sxs-lookup"><span data-stu-id="9c04f-146">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="9c04f-147">Los nombres de objeto deben estar compuestos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="9c04f-147">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="9c04f-148">Los nombres de objeto deben tener al menos un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="9c04f-148">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="9c04f-149">Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="9c04f-149">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="9c04f-150">Los nombres de objeto no pueden comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="9c04f-150">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="9c04f-151">Los nombres de objeto no pueden contener caracteres de control ASCII (de 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="9c04f-151">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="9c04f-152">Los nombres de objeto no pueden contener un carácter de exclamación (!), punto (.), corchete de apertura ([) o corchete de cierre (]).</span><span class="sxs-lookup"><span data-stu-id="9c04f-152">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="9c04f-153">Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si existe) para el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="9c04f-153">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="9c04f-154">Esto significa que los nombres de objeto no pueden contener un espacio.</span><span class="sxs-lookup"><span data-stu-id="9c04f-154">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-155">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="9c04f-155">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="9c04f-156">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="9c04f-156">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="9c04f-157">Esto puede ocurrir para <strong>JetSetCurrentIndex</strong> cuando <em>PINDEXID</em> no es NULL y pindexid- &gt; cbStruct no tiene el tamaño esperado (Windows XP y versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="9c04f-157">This can happen for <strong>JetSetCurrentIndex</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-158">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="9c04f-158">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="9c04f-159">Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ninguna entrada de índice en el nuevo índice que se corresponda con el registro asociado a la entrada de índice en la posición actual del cursor en el índice anterior.</span><span class="sxs-lookup"><span data-stu-id="9c04f-159">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9c04f-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9c04f-161">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9c04f-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-162">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="9c04f-162">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="9c04f-163">El motor ha agotado el grupo de recursos usado para abrir cursores.</span><span class="sxs-lookup"><span data-stu-id="9c04f-163">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="9c04f-164">El número máximo de cursores que se pueden abrir en cualquier momento se controla mediante <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="9c04f-164">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="9c04f-165">Vea <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9c04f-165">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="9c04f-166">Esto puede ocurrir para <strong>JetSetCurrentIndex</strong> cuando se ha seleccionado un índice secundario y el motor no puede abrir un cursor interno para usar ese índice.</span><span class="sxs-lookup"><span data-stu-id="9c04f-166">This can happen for <strong>JetSetCurrentIndex</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9c04f-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9c04f-168">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9c04f-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9c04f-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9c04f-170">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="9c04f-170">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="9c04f-171">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9c04f-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9c04f-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9c04f-173">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9c04f-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9c04f-174">Si se ejecuta correctamente, el índice actual del cursor se establece en el índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="9c04f-174">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="9c04f-175">Ahora se pueden buscar entradas de índice mediante [JetSeek](./jetseek-function.md) según la definición de índice del índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="9c04f-175">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="9c04f-176">Las entradas de índice también se pueden enumerar mediante [JetMove](./jetmove-function.md) en el orden especificado por la definición del índice.</span><span class="sxs-lookup"><span data-stu-id="9c04f-176">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="9c04f-177">La posición actual del cursor se establece en la primera entrada de índice del índice (JET_bitMoveFirst) o en una entrada de índice específica relacionada con la posición actual del cursor en el índice anterior (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="9c04f-177">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="9c04f-178">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9c04f-178">No change to the database state will occur.</span></span>

<span data-ttu-id="9c04f-179">En caso de error, el índice actual y la posición actual del cursor se encuentran en un estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="9c04f-179">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="9c04f-180">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9c04f-180">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9c04f-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c04f-181">Remarks</span></span>

<span data-ttu-id="9c04f-182">Si la sugerencia de ID. de índice está obsoleta, la API simplemente produce un error.</span><span class="sxs-lookup"><span data-stu-id="9c04f-182">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="9c04f-183">No hay ninguna reserva al nombre de texto del índice en este caso, ya que podría esperar.</span><span class="sxs-lookup"><span data-stu-id="9c04f-183">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="9c04f-184">Esta reserva debe realizarse manualmente mediante el autor de la llamada de la API.</span><span class="sxs-lookup"><span data-stu-id="9c04f-184">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9c04f-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c04f-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-186"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9c04f-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9c04f-187">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9c04f-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9c04f-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9c04f-189">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9c04f-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9c04f-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9c04f-191">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="9c04f-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-192"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="9c04f-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9c04f-193">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9c04f-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c04f-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9c04f-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9c04f-195">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9c04f-195">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c04f-196"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9c04f-196"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9c04f-197">Se implementa como <strong>JetSetCurrentIndexW</strong> (Unicode) y <strong>JetSetCurrentIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9c04f-197">Implemented as <strong>JetSetCurrentIndexW</strong> (Unicode) and <strong>JetSetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9c04f-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9c04f-198">See Also</span></span>

[<span data-ttu-id="9c04f-199">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9c04f-199">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9c04f-200">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9c04f-200">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9c04f-201">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9c04f-201">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9c04f-202">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="9c04f-202">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="9c04f-203">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="9c04f-203">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="9c04f-204">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="9c04f-204">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="9c04f-205">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="9c04f-205">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="9c04f-206">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9c04f-206">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="9c04f-207">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="9c04f-207">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="9c04f-208">JetMove</span><span class="sxs-lookup"><span data-stu-id="9c04f-208">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="9c04f-209">JetSeek</span><span class="sxs-lookup"><span data-stu-id="9c04f-209">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="9c04f-210">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="9c04f-210">JetSetCurrentIndex</span></span>]()  
[<span data-ttu-id="9c04f-211">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9c04f-211">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9c04f-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="9c04f-212">JetStopService</span></span>](./jetstopservice-function.md)
