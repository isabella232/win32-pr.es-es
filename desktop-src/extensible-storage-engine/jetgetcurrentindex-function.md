---
description: 'Más información acerca de: JetGetCurrentIndex (función)'
title: JetGetCurrentIndex función)
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716511"
---
# <a name="jetgetcurrentindex-function"></a><span data-ttu-id="b09cf-103">JetGetCurrentIndex función)</span><span class="sxs-lookup"><span data-stu-id="b09cf-103">JetGetCurrentIndex Function</span></span>


<span data-ttu-id="b09cf-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b09cf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetcurrentindex-function"></a><span data-ttu-id="b09cf-105">JetGetCurrentIndex función)</span><span class="sxs-lookup"><span data-stu-id="b09cf-105">JetGetCurrentIndex Function</span></span>

<span data-ttu-id="b09cf-106">La función **JetGetCurrentIndex** determina el nombre del índice actual de un cursor determinado.</span><span class="sxs-lookup"><span data-stu-id="b09cf-106">The **JetGetCurrentIndex** function determines the name of the current index of a given cursor.</span></span> <span data-ttu-id="b09cf-107">Este nombre también se usa para volver a seleccionar más adelante dicho índice como el índice actual mediante [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="b09cf-107">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="b09cf-108">También se puede usar para detectar las propiedades de ese índice mediante [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="b09cf-108">It can also be used to discover the properties of that index using [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a><span data-ttu-id="b09cf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b09cf-109">Parameters</span></span>

<span data-ttu-id="b09cf-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b09cf-110">*sesid*</span></span>

<span data-ttu-id="b09cf-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="b09cf-111">The session to use for this call.</span></span>

<span data-ttu-id="b09cf-112">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="b09cf-112">*tableid*</span></span>

<span data-ttu-id="b09cf-113">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="b09cf-113">The cursor to use for this call.</span></span>

<span data-ttu-id="b09cf-114">*szIndexName*</span><span class="sxs-lookup"><span data-stu-id="b09cf-114">*szIndexName*</span></span>

<span data-ttu-id="b09cf-115">Búfer de salida que recibe el nombre del índice actual del cursor.</span><span class="sxs-lookup"><span data-stu-id="b09cf-115">The output buffer that receives the name of the current index of the cursor.</span></span>

<span data-ttu-id="b09cf-116">*cchIndexName*</span><span class="sxs-lookup"><span data-stu-id="b09cf-116">*cchIndexName*</span></span>

<span data-ttu-id="b09cf-117">Tamaño máximo en caracteres del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b09cf-117">The maximum size in characters of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="b09cf-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b09cf-118">Return Value</span></span>

<span data-ttu-id="b09cf-119">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="b09cf-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b09cf-120">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b09cf-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b09cf-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b09cf-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="b09cf-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b09cf-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b09cf-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b09cf-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b09cf-124">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b09cf-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b09cf-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b09cf-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b09cf-126">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b09cf-126">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b09cf-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b09cf-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b09cf-128">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="b09cf-128">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="b09cf-129">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b09cf-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b09cf-130">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b09cf-130">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b09cf-131">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b09cf-131">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b09cf-132">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b09cf-132">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b09cf-133">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b09cf-133">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b09cf-134">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b09cf-134">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b09cf-135">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b09cf-135">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="b09cf-136">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b09cf-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b09cf-137">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b09cf-137">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b09cf-138">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b09cf-138">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b09cf-139">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="b09cf-139">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="b09cf-140">La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir el nombre de índice completo.</span><span class="sxs-lookup"><span data-stu-id="b09cf-140">The operation completed successfully, but the output buffer was too small to receive the entire index name.</span></span></p>
<p><span data-ttu-id="b09cf-141">El búfer de salida se ha rellenado con tantos nombres de índice como quepan.</span><span class="sxs-lookup"><span data-stu-id="b09cf-141">The output buffer has been filled with as much of the index name as would fit.</span></span> <span data-ttu-id="b09cf-142">Si el búfer de salida tiene al menos un carácter de longitud, la cadena en el búfer de salida se terminará en NULL.</span><span class="sxs-lookup"><span data-stu-id="b09cf-142">If the output buffer is at least one character in length then the string in that output buffer will be null terminated.</span></span></p>
<p><span data-ttu-id="b09cf-143"><strong>Nota:  </strong> Este error no se devolverá si cchIndexName es cero.</span><span class="sxs-lookup"><span data-stu-id="b09cf-143"><strong>Note  </strong>This error will not be returned if cchIndexName is zero.</span></span> <span data-ttu-id="b09cf-144">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b09cf-144">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b09cf-145">Si se ejecuta correctamente, se devolverá el nombre del índice actual del cursor especificado en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b09cf-145">On success, the name of the current index of the given cursor will be returned in the output buffer.</span></span> <span data-ttu-id="b09cf-146">Si se devuelve JET_wrnBufferTruncated, el búfer de salida contendrá tantos el nombre del índice como quepan en el espacio proporcionado.</span><span class="sxs-lookup"><span data-stu-id="b09cf-146">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the index name as will fit in the space provided.</span></span> <span data-ttu-id="b09cf-147">Si el búfer de salida tiene al menos un carácter de longitud, la cadena devuelta en el búfer terminará en NULL.</span><span class="sxs-lookup"><span data-stu-id="b09cf-147">If the output buffer is at least one character in length then the string returned in that buffer will be null terminated.</span></span> <span data-ttu-id="b09cf-148">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b09cf-148">No change to the database state will occur.</span></span>

<span data-ttu-id="b09cf-149">En caso de error, el estado del búfer de salida será undefined.</span><span class="sxs-lookup"><span data-stu-id="b09cf-149">On failure, the state of the output buffer will be undefined.</span></span> <span data-ttu-id="b09cf-150">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b09cf-150">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b09cf-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b09cf-151">Remarks</span></span>

<span data-ttu-id="b09cf-152">Si no hay ningún índice actual para el cursor, se devolverá una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="b09cf-152">If there is no current index for the cursor then an empty string will be returned.</span></span> <span data-ttu-id="b09cf-153">Esto puede ocurrir cuando el cursor está en el índice clúster de la tabla y no se ha definido ningún índice principal.</span><span class="sxs-lookup"><span data-stu-id="b09cf-153">This can happen when the cursor is on the clustered index of the table and no primary index was defined.</span></span> <span data-ttu-id="b09cf-154">Este índice se conoce como el índice secuencial de la tabla y no tiene ninguna definición.</span><span class="sxs-lookup"><span data-stu-id="b09cf-154">This index is known as the sequential index of the table and has no definition.</span></span> <span data-ttu-id="b09cf-155">En cualquier caso, si se establece el índice actual en una cadena vacía mediante [JetSetCurrentIndex](./jetsetcurrentindex-function.md) , se seleccionará el índice clúster independientemente de la presencia de una definición de índice principal.</span><span class="sxs-lookup"><span data-stu-id="b09cf-155">In any case, setting the current index to an empty string using [JetSetCurrentIndex](./jetsetcurrentindex-function.md) will select the clustered index regardless of the presence of a primary index definition.</span></span>

<span data-ttu-id="b09cf-156">Hay un error importante en esta función que está presente en todas las versiones.</span><span class="sxs-lookup"><span data-stu-id="b09cf-156">There is an important bug in this function that is present in all releases.</span></span> <span data-ttu-id="b09cf-157">Si el búfer de salida es demasiado pequeño para recibir el nombre de índice completo y el búfer de salida tiene al menos un carácter de longitud, JET_wrnBufferTruncated no se devolverá.</span><span class="sxs-lookup"><span data-stu-id="b09cf-157">If the output buffer is too small to receive the entire index name and the output buffer is at least one character in length then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="b09cf-158">Se devolverá JET_errSuccess en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b09cf-158">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="b09cf-159">Para evitar este problema, el búfer de salida debe tener siempre al menos JET_cbNameMost + 1 (65) caracteres de longitud.</span><span class="sxs-lookup"><span data-stu-id="b09cf-159">To avoid this issue, the output buffer should always be at least JET_cbNameMost + 1 (65) characters in length.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b09cf-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b09cf-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b09cf-161"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b09cf-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b09cf-162">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b09cf-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b09cf-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b09cf-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b09cf-164">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b09cf-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b09cf-165"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b09cf-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b09cf-166">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b09cf-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b09cf-167"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="b09cf-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b09cf-168">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b09cf-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b09cf-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b09cf-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b09cf-170">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b09cf-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b09cf-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="b09cf-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="b09cf-172">Se implementa como <strong>JetGetCurrentIndexW</strong> (Unicode) y <strong>JetGetCurrentIndexA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="b09cf-172">Implemented as <strong>JetGetCurrentIndexW</strong> (Unicode) and <strong>JetGetCurrentIndexA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b09cf-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b09cf-173">See Also</span></span>

[<span data-ttu-id="b09cf-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b09cf-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b09cf-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b09cf-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b09cf-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b09cf-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b09cf-177">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="b09cf-177">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="b09cf-178">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="b09cf-178">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
