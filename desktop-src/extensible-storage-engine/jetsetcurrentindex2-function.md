---
description: 'Más información acerca de: JetSetCurrentIndex2 (función)'
title: Función JetSetCurrentIndex2
TOCTitle: JetSetCurrentIndex2 Function
ms:assetid: da94465e-bd35-45c2-9ccc-1d2e8c34aa9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294110(v=EXCHG.10)
ms:contentKeyID: 32765725
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex2W
- JetSetCurrentIndex2A
- JetSetCurrentIndex2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c95e665b549fff82e0beaaca9682329217ebb0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714966"
---
# <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="c08d2-103">Función JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="c08d2-103">JetSetCurrentIndex2 Function</span></span>


<span data-ttu-id="c08d2-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c08d2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetcurrentindex2-function"></a><span data-ttu-id="c08d2-105">Función JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="c08d2-105">JetSetCurrentIndex2 Function</span></span>

<span data-ttu-id="c08d2-106">La función **JetSetCurrentIndex2** establece el índice actual de un cursor que define qué registros de una tabla están visibles para ese cursor y el orden en que aparecen seleccionando el conjunto de entradas de índice que se van a usar para exponer esos registros.</span><span class="sxs-lookup"><span data-stu-id="c08d2-106">The **JetSetCurrentIndex2** function sets the current index of a cursor that defines which records in a table are visible to that cursor and the order in which they appear by selecting the set of index entries to use to expose those records.</span></span>

```cpp
    JET_ERR JET_API JetSetCurrentIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c08d2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c08d2-107">Parameters</span></span>

<span data-ttu-id="c08d2-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c08d2-108">*sesid*</span></span>

<span data-ttu-id="c08d2-109">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c08d2-109">The session to use for this call.</span></span>

<span data-ttu-id="c08d2-110">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="c08d2-110">*tableid*</span></span>

<span data-ttu-id="c08d2-111">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c08d2-111">The cursor to use for this call.</span></span>

<span data-ttu-id="c08d2-112">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="c08d2-112">*szIndexName*</span></span>

<span data-ttu-id="c08d2-113">Nombre del índice que se va a seleccionar para el cursor.</span><span class="sxs-lookup"><span data-stu-id="c08d2-113">The name of the index to be selected for the cursor.</span></span>

<span data-ttu-id="c08d2-114">Si este parámetro es NULL o una cadena vacía, se seleccionará el índice clúster.</span><span class="sxs-lookup"><span data-stu-id="c08d2-114">If this parameter is NULL or an empty string then the clustered index will be selected.</span></span> <span data-ttu-id="c08d2-115">Si se define un índice principal para la tabla, ese índice se seleccionará porque es el mismo que el índice clúster.</span><span class="sxs-lookup"><span data-stu-id="c08d2-115">If a primary index is defined for the table then that index will be selected because it is the same as the clustered index.</span></span> <span data-ttu-id="c08d2-116">Si no hay ningún índice principal definido para la tabla, se seleccionará el índice secuencial.</span><span class="sxs-lookup"><span data-stu-id="c08d2-116">If no primary index is defined for the table then the sequential index will be selected.</span></span> <span data-ttu-id="c08d2-117">El índice secuencial no tiene ninguna definición de índice.</span><span class="sxs-lookup"><span data-stu-id="c08d2-117">The sequential index has no index definition.</span></span> <span data-ttu-id="c08d2-118">Vea [JetCreateIndex](./jetcreateindex-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c08d2-118">See [JetCreateIndex](./jetcreateindex-function.md) for more information.</span></span>

<span data-ttu-id="c08d2-119">Si *pindexid* no es null, se omitirá el nombre del índice y el índice se seleccionará por su ID. de índice.</span><span class="sxs-lookup"><span data-stu-id="c08d2-119">If *pindexid* is not NULL then the index name will be ignored and the index will be selected by its index ID.</span></span>

<span data-ttu-id="c08d2-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c08d2-120">*grbit*</span></span>

<span data-ttu-id="c08d2-121">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="c08d2-121">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c08d2-122">Value</span><span class="sxs-lookup"><span data-stu-id="c08d2-122">Value</span></span></p></th>
<th><p><span data-ttu-id="c08d2-123">Significado</span><span class="sxs-lookup"><span data-stu-id="c08d2-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-124">JET_bitMoveFirst</span><span class="sxs-lookup"><span data-stu-id="c08d2-124">JET_bitMoveFirst</span></span></p></td>
<td><p><span data-ttu-id="c08d2-125">Esta opción indica que el cursor se debe colocar en la primera entrada del índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c08d2-125">This option indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="c08d2-126">Si el índice clúster se selecciona (índice principal o índice secuencial) y el índice actual es un índice secundario, se supone JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="c08d2-126">If the clustered index is being selected (primary index or sequential index) and the current index is a secondary index then JET_bitMoveFirst is assumed.</span></span> <span data-ttu-id="c08d2-127">Si se selecciona el índice actual, esta opción se omite y no se realiza ningún cambio en la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="c08d2-127">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-128">JET_bitNoMove</span><span class="sxs-lookup"><span data-stu-id="c08d2-128">JET_bitNoMove</span></span></p></td>
<td><p><span data-ttu-id="c08d2-129">Esta opción indica que el cursor se debe colocar en la entrada de índice del nuevo índice correspondiente al registro asociado a la entrada de índice en la posición actual del cursor en el índice anterior.</span><span class="sxs-lookup"><span data-stu-id="c08d2-129">This option indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p>
<p><span data-ttu-id="c08d2-130">Si la definición del nuevo índice contiene al menos una columna de clave de varios valores, la entrada de índice de destino es ambigua.</span><span class="sxs-lookup"><span data-stu-id="c08d2-130">If the definition for the new index contains at least one multi-valued key column then the destination index entry is ambiguous.</span></span> <span data-ttu-id="c08d2-131">En este caso, el valor de <em>itagSequence</em> especificado se usa para seleccionar qué valor de la columna de clave múltiple con varios valores más importante se usa para colocar el cursor.</span><span class="sxs-lookup"><span data-stu-id="c08d2-131">In this case, the specified <em>itagSequence</em> is used to select which multi-value of the most significant multi-valued key column is used to position the cursor.</span></span> <span data-ttu-id="c08d2-132">Solo es necesario pasar un solo <em>itagSequence</em> , incluso en el caso de varias columnas de clave de varios valores, ya que el motor solo expande todos los valores de la columna de clave con varios valores más significativa.</span><span class="sxs-lookup"><span data-stu-id="c08d2-132">It is only necessary to pass a single <em>itagSequence</em> even in the case of multiple multi-valued key columns because the engine only expands all values for the most significant multi-valued key column.</span></span> <span data-ttu-id="c08d2-133">Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c08d2-133">See <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> for more details.</span></span></p>
<p><span data-ttu-id="c08d2-134">Si se especifica JET_bitMoveFirst, se omite esta opción.</span><span class="sxs-lookup"><span data-stu-id="c08d2-134">If JET_bitMoveFirst is specified then this option is ignored.</span></span></p>
<p><span data-ttu-id="c08d2-135">Si se selecciona el índice actual, esta opción se omite y no se realiza ningún cambio en la posición del cursor.</span><span class="sxs-lookup"><span data-stu-id="c08d2-135">If the current index is being selected then this option is ignored and no change to the cursor position is made.</span></span> <span data-ttu-id="c08d2-136">Cuando este parámetro no está presente, se supone que su valor es JET_bitMoveFirst.</span><span class="sxs-lookup"><span data-stu-id="c08d2-136">When this parameter is not present, its value is presumed to be JET_bitMoveFirst.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="c08d2-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c08d2-137">Return Value</span></span>

<span data-ttu-id="c08d2-138">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="c08d2-138">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c08d2-139">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c08d2-139">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c08d2-140">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c08d2-140">Return code</span></span></p></th>
<th><p><span data-ttu-id="c08d2-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="c08d2-141">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-142">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c08d2-142">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c08d2-143">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c08d2-143">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-144">JET_errBadItagSequence</span><span class="sxs-lookup"><span data-stu-id="c08d2-144">JET_errBadItagSequence</span></span></p></td>
<td><p><span data-ttu-id="c08d2-145">Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ningún valor para la primera columna de clave de varios valores en la nueva definición para el índice que corresponde al número de secuencia especificado.</span><span class="sxs-lookup"><span data-stu-id="c08d2-145">A secondary index is being selected with the JET_bitNoMove option and there is no value for the first multi-valued key column in the new definition for the index that corresponds to the specified sequence number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c08d2-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c08d2-147">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c08d2-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c08d2-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c08d2-149">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="c08d2-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c08d2-150">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c08d2-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-151">JET_errInvalidIndexId</span><span class="sxs-lookup"><span data-stu-id="c08d2-151">JET_errInvalidIndexId</span></span></p></td>
<td><p><span data-ttu-id="c08d2-152">El contenido del ID. de índice no era válido o expiró y debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="c08d2-152">The contents of the index ID were not valid or have expired and need to be refreshed.</span></span> <span data-ttu-id="c08d2-153">Esto puede ocurrir para <strong>JetSetCurrentIndex2</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="c08d2-153">This can happen for <strong>JetSetCurrentIndex2</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="c08d2-154">pindexid- &gt; cbStruct no tiene el tamaño esperado (Windows Server 2003 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="c08d2-154">pindexid-&gt;cbStruct is not of the expected size (Windows Server 2003 and later releases).</span></span></p></li>
<li><p><span data-ttu-id="c08d2-155">El motor se ha cerrado desde que se ha capturado el ID. de índice.</span><span class="sxs-lookup"><span data-stu-id="c08d2-155">The engine has been shut down since the index ID was fetched.</span></span></p></li>
<li><p><span data-ttu-id="c08d2-156">Todos los cursores que hacen referencia a la tabla que contiene el índice correspondiente al ID. de índice se han cerrado y el motor ha expulsado la definición del índice de la caché de esquema.</span><span class="sxs-lookup"><span data-stu-id="c08d2-156">All cursors referencing the table containing the index corresponding to the index ID have been closed and the engine has evicted the definition for the index from the schema cache.</span></span></p></li>
<li><p><span data-ttu-id="c08d2-157">El ID. de índice se está usando con un cursor abierto en la tabla equivocada.</span><span class="sxs-lookup"><span data-stu-id="c08d2-157">The index ID is being used with a cursor opened on the wrong table.</span></span></p></li>
<li><p><span data-ttu-id="c08d2-158">El índice se ha quitado o aún no está visible para la sesión.</span><span class="sxs-lookup"><span data-stu-id="c08d2-158">The index has been dropped or is not yet visible to the session.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-159">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="c08d2-159">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="c08d2-160">Uno de los nombres de objeto especificados no era válido.</span><span class="sxs-lookup"><span data-stu-id="c08d2-160">One of the specified object names was invalid.</span></span> <span data-ttu-id="c08d2-161">Todos los nombres de objeto deben cumplir el mismo conjunto de reglas.</span><span class="sxs-lookup"><span data-stu-id="c08d2-161">All object names must conform to the same set of rules.</span></span> <span data-ttu-id="c08d2-162">Estas reglas son:</span><span class="sxs-lookup"><span data-stu-id="c08d2-162">These rules are as follows:</span></span></p>
<ul>
<li><p><span data-ttu-id="c08d2-163">Los nombres de objeto deben estar compuestos por caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="c08d2-163">Object names must be composed of ASCII characters.</span></span></p></li>
<li><p><span data-ttu-id="c08d2-164">Los nombres de objeto deben tener al menos un carácter de longitud.</span><span class="sxs-lookup"><span data-stu-id="c08d2-164">Object names must be at least one character in length.</span></span></p></li>
<li><p><span data-ttu-id="c08d2-165">Los nombres de objeto no pueden superar JET_cbNameMost (64) caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="c08d2-165">Object names may not exceed JET_cbNameMost (64) characters in length.</span></span></p></li>
<li><p><span data-ttu-id="c08d2-166">Los nombres de objeto no pueden comenzar con un espacio.</span><span class="sxs-lookup"><span data-stu-id="c08d2-166">Object names may not begin with a space.</span></span></p></li>
<li><p><span data-ttu-id="c08d2-167">Los nombres de objeto no pueden contener caracteres de control ASCII (de 0x00 a 0x1F).</span><span class="sxs-lookup"><span data-stu-id="c08d2-167">Object names may not contain ASCII control characters (0x00 through 0x1F).</span></span></p></li>
<li><p><span data-ttu-id="c08d2-168">Los nombres de objeto no pueden contener un carácter de exclamación (!), punto (.), corchete de apertura ([) o corchete de cierre (]).</span><span class="sxs-lookup"><span data-stu-id="c08d2-168">Object names may not contain an exclamation point (!), period (.), left bracket ([), or right bracket (]) character.</span></span></p></li>
<li><p><span data-ttu-id="c08d2-169">Una vez validada, solo se usará la parte de la cadena hasta el primer espacio (si existe) para el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="c08d2-169">Once validated, only the portion of the string up to the first space (if any) will be used for the object name.</span></span> <span data-ttu-id="c08d2-170">Esto significa que los nombres de objeto no pueden contener un espacio.</span><span class="sxs-lookup"><span data-stu-id="c08d2-170">This effectively means that object names may not contain a space either.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-171">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c08d2-171">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c08d2-172">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="c08d2-172">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="c08d2-173">Esto puede ocurrir para <strong>JetSetCurrentIndex2</strong> cuando <em>PINDEXID</em> no es NULL y pindexid- &gt; cbStruct no tiene el tamaño esperado (Windows XP y versiones anteriores).</span><span class="sxs-lookup"><span data-stu-id="c08d2-173">This can happen for <strong>JetSetCurrentIndex2</strong> when <em>pindexid</em> is not NULL and pindexid-&gt;cbStruct is not of the expected size (Windows XP and earlier releases).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-174">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="c08d2-174">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="c08d2-175">Se selecciona un índice secundario con la opción JET_bitNoMove y no hay ninguna entrada de índice en el nuevo índice que se corresponda con el registro asociado a la entrada de índice en la posición actual del cursor en el índice anterior.</span><span class="sxs-lookup"><span data-stu-id="c08d2-175">A secondary index is being selected with the JET_bitNoMove option and there is no index entry in the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-176">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c08d2-176">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c08d2-177">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c08d2-177">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-178">JET_errOutOfCursors</span><span class="sxs-lookup"><span data-stu-id="c08d2-178">JET_errOutOfCursors</span></span></p></td>
<td><p><span data-ttu-id="c08d2-179">El motor ha agotado el grupo de recursos usado para abrir cursores.</span><span class="sxs-lookup"><span data-stu-id="c08d2-179">The engine has exhausted its pool of resources used to open cursors.</span></span> <span data-ttu-id="c08d2-180">El número máximo de cursores que se pueden abrir en cualquier momento se controla mediante <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span><span class="sxs-lookup"><span data-stu-id="c08d2-180">The maximum number of cursors that can be opened at any one time is controlled using <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>.</span></span> <span data-ttu-id="c08d2-181">Vea <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="c08d2-181">See <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for more information.</span></span> <span data-ttu-id="c08d2-182">Esto puede ocurrir para <strong>JetSetCurrentIndex2</strong> cuando se ha seleccionado un índice secundario y el motor no puede abrir un cursor interno para usar ese índice.</span><span class="sxs-lookup"><span data-stu-id="c08d2-182">This can happen for <strong>JetSetCurrentIndex2</strong> when a secondary index has been selected and the engine cannot open an internal cursor to use that index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-183">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c08d2-183">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c08d2-184">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c08d2-184">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-185">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c08d2-185">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c08d2-186">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c08d2-186">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c08d2-187">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c08d2-187">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-188">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c08d2-188">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c08d2-189">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c08d2-189">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c08d2-190">Si se ejecuta correctamente, el índice actual del cursor se establece en el índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="c08d2-190">On success, the current index of the cursor is set to the requested index.</span></span> <span data-ttu-id="c08d2-191">Ahora se pueden buscar entradas de índice mediante [JetSeek](./jetseek-function.md) según la definición de índice del índice solicitado.</span><span class="sxs-lookup"><span data-stu-id="c08d2-191">Index entries may now be sought using [JetSeek](./jetseek-function.md) according to the index definition of the requested index.</span></span> <span data-ttu-id="c08d2-192">Las entradas de índice también se pueden enumerar mediante [JetMove](./jetmove-function.md) en el orden especificado por la definición del índice.</span><span class="sxs-lookup"><span data-stu-id="c08d2-192">Index entries may also be enumerated using [JetMove](./jetmove-function.md) in the order specified by that index definition.</span></span> <span data-ttu-id="c08d2-193">La posición actual del cursor se establece en la primera entrada de índice del índice (JET_bitMoveFirst) o en una entrada de índice específica relacionada con la posición actual del cursor en el índice anterior (JET_bitNoMove).</span><span class="sxs-lookup"><span data-stu-id="c08d2-193">The current position of the cursor is either set to the first index entry on the index (JET_bitMoveFirst) or to a specific index entry that is related to the current position of the cursor on the old index (JET_bitNoMove).</span></span> <span data-ttu-id="c08d2-194">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c08d2-194">No change to the database state will occur.</span></span>

<span data-ttu-id="c08d2-195">En caso de error, el índice actual y la posición actual del cursor se encuentran en un estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="c08d2-195">On failure, the current index and current position of the cursor are in an undefined state.</span></span> <span data-ttu-id="c08d2-196">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c08d2-196">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c08d2-197">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c08d2-197">Remarks</span></span>

<span data-ttu-id="c08d2-198">Si la sugerencia de ID. de índice está obsoleta, la API simplemente produce un error.</span><span class="sxs-lookup"><span data-stu-id="c08d2-198">If the index ID hint is stale then the API simply fails.</span></span> <span data-ttu-id="c08d2-199">No hay ninguna reserva al nombre de texto del índice en este caso, ya que podría esperar.</span><span class="sxs-lookup"><span data-stu-id="c08d2-199">There is no fallback to the text name of the index in this case as one might expect.</span></span> <span data-ttu-id="c08d2-200">Esta reserva debe realizarse manualmente mediante el autor de la llamada de la API.</span><span class="sxs-lookup"><span data-stu-id="c08d2-200">This fallback must be done manually by the caller of the API.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c08d2-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c08d2-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-202"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c08d2-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c08d2-203">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c08d2-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c08d2-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c08d2-205">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c08d2-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c08d2-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c08d2-207">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c08d2-207">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-208"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="c08d2-208"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c08d2-209">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c08d2-209">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c08d2-210"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c08d2-210"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c08d2-211">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c08d2-211">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c08d2-212"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c08d2-212"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c08d2-213">Se implementa como <strong>JetSetCurrentIndex2W</strong> (Unicode) y <strong>JetSetCurrentIndex2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c08d2-213">Implemented as <strong>JetSetCurrentIndex2W</strong> (Unicode) and <strong>JetSetCurrentIndex2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c08d2-214">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c08d2-214">See Also</span></span>

[<span data-ttu-id="c08d2-215">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c08d2-215">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c08d2-216">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c08d2-216">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c08d2-217">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c08d2-217">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c08d2-218">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c08d2-218">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c08d2-219">JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="c08d2-219">JET_INDEXID</span></span>](./jet-indexid-structure.md)  
[<span data-ttu-id="c08d2-220">JetCreateIndex</span><span class="sxs-lookup"><span data-stu-id="c08d2-220">JetCreateIndex</span></span>](./jetcreateindex-function.md)  
[<span data-ttu-id="c08d2-221">JetGetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="c08d2-221">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)  
[<span data-ttu-id="c08d2-222">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c08d2-222">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="c08d2-223">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c08d2-223">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="c08d2-224">JetMove</span><span class="sxs-lookup"><span data-stu-id="c08d2-224">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="c08d2-225">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="c08d2-225">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="c08d2-226">JetSeek</span><span class="sxs-lookup"><span data-stu-id="c08d2-226">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="c08d2-227">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c08d2-227">JetStopService</span></span>](./jetstopservice-function.md)
