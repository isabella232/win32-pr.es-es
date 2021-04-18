---
description: 'Más información acerca de: JetSetCurrentIndex3 (función)'
title: Función JetSetCurrentIndex3
TOCTitle: JetSetCurrentIndex3 Function
ms:assetid: 50050bd3-4b74-4be7-985c-754ced8aded1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269244(v=EXCHG.10)
ms:contentKeyID: 32765546
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex3A
- JetSetCurrentIndex3W
- JetSetCurrentIndex3
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b97aa356d44ab72f7cd240a42351d9962777ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715029"
---
# <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="a48ad-103">Función JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="a48ad-103">JetSetCurrentIndex3 Function</span></span>


<span data-ttu-id="a48ad-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a48ad-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex3-function"></a><span data-ttu-id="a48ad-105">Función JetSetCurrentIndex3</span><span class="sxs-lookup"><span data-stu-id="a48ad-105">JetSetCurrentIndex3 Function</span></span>

<span data-ttu-id="a48ad-106">La función **JetSetCurrentIndex3** se usa para establecer el índice actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="a48ad-106">The **JetSetCurrentIndex3** function is used to set the current index of a cursor.</span></span> <span data-ttu-id="a48ad-107">El índice actual de un cursor define qué registros de una tabla son visibles para ese cursor y el orden en que aparecen seleccionando el conjunto de entradas de índice que se van a usar para exponer esos registros.</span><span class="sxs-lookup"><span data-stu-id="a48ad-107">The current index of a cursor defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a><span data-ttu-id="a48ad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a48ad-108">Parameters</span></span>

<span data-ttu-id="a48ad-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="a48ad-109">*sesid*</span></span>

<span data-ttu-id="a48ad-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a48ad-110">The session to use for this call.</span></span>

<span data-ttu-id="a48ad-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="a48ad-111">*tableid*</span></span>

<span data-ttu-id="a48ad-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a48ad-112">The cursor to use for this call.</span></span>

<span data-ttu-id="a48ad-113">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="a48ad-113">*szIndexName*</span></span>

<span data-ttu-id="a48ad-114">Nombre del índice que se va a seleccionar para el cursor.</span><span class="sxs-lookup"><span data-stu-id="a48ad-114">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="a48ad-115">Si este parámetro es NULL o una cadena vacía, se seleccionará el índice clúster.</span><span class="sxs-lookup"><span data-stu-id="a48ad-115">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="a48ad-116">Si se define un índice principal para la tabla, ese índice se seleccionará porque es el mismo que el índice clúster.</span><span class="sxs-lookup"><span data-stu-id="a48ad-116">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="a48ad-117">Si no hay ningún índice principal definido para la tabla, se seleccionará el índice secuencial.</span><span class="sxs-lookup"><span data-stu-id="a48ad-117">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="a48ad-118">El índice secuencial no tiene ninguna definición de índice.</span><span class="sxs-lookup"><span data-stu-id="a48ad-118">The sequential index has no index definition.</span></span> <span data-ttu-id="a48ad-119">Vea [JetCreateIndex](./jetcreateindex-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a48ad-119">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="a48ad-120">Si *pindexid* no es null, se omitirá el nombre del índice y el índice se seleccionará por su ID. de índice.</span><span class="sxs-lookup"><span data-stu-id="a48ad-120">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="a48ad-121">*grbit*</span><span class="sxs-lookup"><span data-stu-id="a48ad-121">*grbit*</span></span>

<span data-ttu-id="a48ad-122">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="a48ad-122">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a48ad-123">Value</span><span class="sxs-lookup"><span data-stu-id="a48ad-123">Value</span></span></p></th>
<th><p><span data-ttu-id="a48ad-124">Significado</span><span class="sxs-lookup"><span data-stu-id="a48ad-124">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-125">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="a48ad-125">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="a48ad-126">Esta opción indica que el cursor se debe colocar en la primera entrada del índice especificado.</span><span class="sxs-lookup"><span data-stu-id="a48ad-126">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="a48ad-127">Si el índice clúster se selecciona (índice principal o índice secuencial) y el índice actual es un índice secundario, se supone JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="a48ad-127">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="a48ad-128">Si se selecciona el índice actual, esta opción se omite y no se realiza ningún cambio en la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="a48ad-128">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-129">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="a48ad-129">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="a48ad-130">Esta opción indica que el cursor se debe colocar en la entrada de índice del nuevo índice correspondiente al registro asociado a la entrada de índice en la posición actual del cursor en el índice anterior.</span><span class="sxs-lookup"><span data-stu-id="a48ad-130">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="a48ad-131">Si la definición del nuevo índice contiene al menos una columna de clave de varios valores, la entrada de índice de destino es ambigua.</span><span class="sxs-lookup"><span data-stu-id="a48ad-131">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="a48ad-132">En este caso, el valor de <em>itagSequence</em> especificado se usa para seleccionar qué valor de la columna de clave múltiple con varios valores más importante se usa para colocar el cursor.</span><span class="sxs-lookup"><span data-stu-id="a48ad-132">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="a48ad-133">Solo es necesario pasar un solo <em>itagSequence</em> , incluso en el caso de varias columnas de clave de varios valores, ya que el motor solo expande todos los valores de la columna de clave con varios valores más significativa.</span><span class="sxs-lookup"><span data-stu-id="a48ad-133">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="a48ad-134">Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a48ad-134">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="a48ad-135">Si se especifica JET_bitMoveFirst, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="a48ad-135">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="a48ad-136">Si se selecciona el índice actual, esta opción se omite y no se realiza ningún cambio en la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="a48ad-136">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="a48ad-137">Cuando este parámetro no está presente, se supone que su valor es JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="a48ad-137">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a48ad-138">*itagSequence*</span><span class="sxs-lookup"><span data-stu-id="a48ad-138">*itagSequence*</span></span>

<span data-ttu-id="a48ad-139">Número de secuencia del valor de la columna con varios valores que se usará para colocar el cursor en el nuevo índice.</span><span class="sxs-lookup"><span data-stu-id="a48ad-139">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span>

<span data-ttu-id="a48ad-140">Este parámetro solo se utiliza junto con JET_bitNoMove.</span><span class="sxs-lookup"><span data-stu-id="a48ad-140">This parameter is only used in conjunction with JET_bitNoMove.</span></span> <span data-ttu-id="a48ad-141">Vea la descripción de esta opción para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="a48ad-141">See the description of this option for more details.</span></span>

<span data-ttu-id="a48ad-142">Cuando este parámetro no está presente o se establece en cero, se supone que su valor es 1.</span><span class="sxs-lookup"><span data-stu-id="a48ad-142">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

### <a name="return-value"></a><span data-ttu-id="a48ad-143">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a48ad-143">Return Value</span></span>

<span data-ttu-id="a48ad-144">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="a48ad-144">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a48ad-145">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a48ad-145">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a48ad-146">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a48ad-146">Return code</span></span></p></th>
<th><p><span data-ttu-id="a48ad-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="a48ad-147">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-148">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a48ad-148">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a48ad-149">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a48ad-149">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-150">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="a48ad-150">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="a48ad-151">Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ningún valor para la primera columna de clave de varios valores en la definición del nuevo índice que corresponde al número de secuencia especificado.</span><span class="sxs-lookup"><span data-stu-id="a48ad-151">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new index's definition that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-152">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="a48ad-152">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="a48ad-153">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="a48ad-153">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-154">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="a48ad-154">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="a48ad-155">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="a48ad-155">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="a48ad-156">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a48ad-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-157">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="a48ad-157">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="a48ad-158">El contenido del ID. de índice no era válido o expiró y debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="a48ad-158">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="a48ad-159">Esto puede ocurrir para <strong>JetSetCurrentIndex3</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="a48ad-159">This can happen for <strong>JetSetCurrentIndex3</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="a48ad-160">pindexid- &gt; cbStruct no tiene el tamaño esperado (Windows Server 2003 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="a48ad-160">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="a48ad-161">El motor se ha cerrado desde que se ha capturado el ID. de índice.</span><span class="sxs-lookup"><span data-stu-id="a48ad-161">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="a48ad-162">Todos los cursores que hacen referencia a la tabla que contiene el índice correspondiente al ID. de índice se han cerrado y el motor ha expulsado la definición de ese índice de la caché de esquema.</span><span class="sxs-lookup"><span data-stu-id="a48ad-162">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for that index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="a48ad-163">El ID. de índice se está usando con un cursor abierto en la tabla equivocada.</span><span class="sxs-lookup"><span data-stu-id="a48ad-163">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="a48ad-164">El índice se ha quitado o aún no está visible para la sesión.</span><span class="sxs-lookup"><span data-stu-id="a48ad-164">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-165">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="a48ad-165">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="a48ad-166">Uno de los nombres de objeto especificados no era válido.</span><span class="sxs-lookup"><span data-stu-id="a48ad-166">One of the specified object names was invalid.</span></span> <span data-ttu-id="a48ad-167">Todos los nombres de objeto deben cumplir el mismo conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="a48ad-167">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="a48ad-168">Estas reglas son:</span><span class="sxs-lookup"><span data-stu-id="a48ad-168">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="a48ad-169">Los nombres de objeto deben estar compuestos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="a48ad-169">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="a48ad-170">Los nombres de objeto deben tener al menos un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="a48ad-170">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="a48ad-171">Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="a48ad-171">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="a48ad-172">Los nombres de objeto no pueden comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="a48ad-172">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="a48ad-173">Los nombres de objeto no pueden contener caracteres de control ASCII (de 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="a48ad-173">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="a48ad-174">Los nombres de objeto no pueden contener un carácter de exclamación (!), punto (.), corchete de apertura ([) o corchete de cierre (]).</span><span class="sxs-lookup"><span data-stu-id="a48ad-174">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="a48ad-175">Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si existe) para el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="a48ad-175">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="a48ad-176">Esto significa que los nombres de objeto no pueden contener un espacio.</span><span class="sxs-lookup"><span data-stu-id="a48ad-176">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-177">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a48ad-177">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a48ad-178">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="a48ad-178">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="a48ad-179">Esto puede ocurrir para <strong>JetSetCurrentIndex3</strong> cuando <em>PINDEXID</em> no es NULL y pindexid- &gt; cbStruct no tiene el tamaño esperado (Windows XP y versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="a48ad-179">This can happen for <strong>JetSetCurrentIndex3</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-180">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="a48ad-180">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="a48ad-181">Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ninguna entrada de índice en el nuevo índice que se corresponda con el registro asociado a la entrada de índice en la posición actual del cursor en el índice anterior.</span><span class="sxs-lookup"><span data-stu-id="a48ad-181">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-182">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="a48ad-182">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="a48ad-183">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a48ad-183">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-184">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="a48ad-184">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="a48ad-185">El motor ha agotado el grupo de recursos usado para abrir cursores.</span><span class="sxs-lookup"><span data-stu-id="a48ad-185">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="a48ad-186">El número máximo de cursores que se pueden abrir en cualquier momento se controla mediante <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="a48ad-186">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="a48ad-187">Vea <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a48ad-187">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="a48ad-188">Esto puede ocurrir para <strong>JetSetCurrentIndex3</strong> cuando se ha seleccionado un índice secundario y el motor no puede abrir un cursor interno para usar ese índice.</span><span class="sxs-lookup"><span data-stu-id="a48ad-188">This can happen for <strong>JetSetCurrentIndex3</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-189">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="a48ad-189">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="a48ad-190">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a48ad-190">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-191">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="a48ad-191">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="a48ad-192">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a48ad-192">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="a48ad-193">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a48ad-193">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-194">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="a48ad-194">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="a48ad-195">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="a48ad-195">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a48ad-196">Si se ejecuta correctamente, el índice actual del cursor se establece en el índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="a48ad-196">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="a48ad-197">Ahora se pueden buscar entradas de índice mediante [JetSeek](./jetseek-function.md) según la definición de índice del índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="a48ad-197">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="a48ad-198">Las entradas de índice también se pueden enumerar mediante [JetMove](./jetmove-function.md) en el orden especificado por la definición del índice.</span><span class="sxs-lookup"><span data-stu-id="a48ad-198">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="a48ad-199">La posición actual del cursor se establece en la primera entrada de índice del índice (JET_bitMoveFirst) o en una entrada de índice específica relacionada con la posición actual del cursor en el índice anterior (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="a48ad-199">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="a48ad-200">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a48ad-200">No change to the database state will occur.</span></span>

<span data-ttu-id="a48ad-201">En caso de error, el índice actual y la posición actual del cursor se encuentran en un estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="a48ad-201">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="a48ad-202">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a48ad-202">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a48ad-203">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a48ad-203">Remarks</span></span>

<span data-ttu-id="a48ad-204">Si la sugerencia de ID. de índice está obsoleta, la API simplemente produce un error.</span><span class="sxs-lookup"><span data-stu-id="a48ad-204">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="a48ad-205">No hay ninguna reserva al nombre de texto del índice en este caso, ya que podría esperar.</span><span class="sxs-lookup"><span data-stu-id="a48ad-205">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="a48ad-206">Esta reserva debe realizarse manualmente mediante el autor de la llamada de la API.</span><span class="sxs-lookup"><span data-stu-id="a48ad-206">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a48ad-207">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a48ad-207">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-208"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a48ad-208"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a48ad-209">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a48ad-209">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-210"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a48ad-210"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a48ad-211">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a48ad-211">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-212"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a48ad-212"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a48ad-213">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a48ad-213">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-214"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="a48ad-214"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a48ad-215">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a48ad-215">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a48ad-216"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a48ad-216"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a48ad-217">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a48ad-217">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a48ad-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a48ad-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a48ad-219">Se implementa como <strong>JetSetCurrentIndex3W</strong> (Unicode) y <strong>JetSetCurrentIndex3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a48ad-219">Implemented as <strong>JetSetCurrentIndex3W</strong> (Unicode) and <strong>JetSetCurrentIndex3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a48ad-220">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a48ad-220">See Also</span></span>

[<span data-ttu-id="a48ad-221">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a48ad-221">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a48ad-222">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a48ad-222">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a48ad-223">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="a48ad-223">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="a48ad-224">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="a48ad-224">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="a48ad-225">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="a48ad-225">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="a48ad-226">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="a48ad-226">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="a48ad-227">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="a48ad-227">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="a48ad-228">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a48ad-228">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="a48ad-229">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="a48ad-229">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="a48ad-230">JetMove</span><span class="sxs-lookup"><span data-stu-id="a48ad-230">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="a48ad-231">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a48ad-231">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="a48ad-232">JetSeek</span><span class="sxs-lookup"><span data-stu-id="a48ad-232">JetSeek</span></span>](./jetseek-function.md)
