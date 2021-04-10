---
description: 'Más información acerca de: JetGetBookmark (función)'
title: JetGetBookmark función)
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a27ce474a8f021ff9039a07d7542b194e72e262a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156808"
---
# <a name="jetgetbookmark-function"></a><span data-ttu-id="b9b33-103">JetGetBookmark función)</span><span class="sxs-lookup"><span data-stu-id="b9b33-103">JetGetBookmark Function</span></span>


<span data-ttu-id="b9b33-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b9b33-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetbookmark-function"></a><span data-ttu-id="b9b33-105">JetGetBookmark función)</span><span class="sxs-lookup"><span data-stu-id="b9b33-105">JetGetBookmark Function</span></span>

<span data-ttu-id="b9b33-106">La función **JetGetBookmark** recupera el marcador para el registro que está asociado a la entrada de índice en la posición actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="b9b33-106">The **JetGetBookmark** function retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="b9b33-107">Este marcador se puede usar para volver a colocar el cursor en el mismo registro mediante [JetGoToBookmark](./jetgotobookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9b33-107">This bookmark can then be used to reposition that cursor back to the same record using [JetGoToBookmark](./jetgotobookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="b9b33-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9b33-108">Parameters</span></span>

<span data-ttu-id="b9b33-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="b9b33-109">*sesid*</span></span>

<span data-ttu-id="b9b33-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="b9b33-110">The session to use for this call.</span></span>

<span data-ttu-id="b9b33-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="b9b33-111">*tableid*</span></span>

<span data-ttu-id="b9b33-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="b9b33-112">The cursor to use for this call.</span></span>

<span data-ttu-id="b9b33-113">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="b9b33-113">*pvBookmark*</span></span>

<span data-ttu-id="b9b33-114">Búfer de salida que recibe el marcador.</span><span class="sxs-lookup"><span data-stu-id="b9b33-114">The output buffer that receives the bookmark.</span></span>

<span data-ttu-id="b9b33-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="b9b33-115">*cbMax*</span></span>

<span data-ttu-id="b9b33-116">Tamaño máximo, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b9b33-116">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="b9b33-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="b9b33-117">*pcbActual*</span></span>

<span data-ttu-id="b9b33-118">Tamaño real, en bytes, del marcador.</span><span class="sxs-lookup"><span data-stu-id="b9b33-118">The actual size, in bytes, of the bookmark.</span></span>

<span data-ttu-id="b9b33-119">Si este parámetro es **null** , no se devolverá el tamaño real del marcador.</span><span class="sxs-lookup"><span data-stu-id="b9b33-119">If this parameter is **NULL** then the actual size of the bookmark will not be returned.</span></span>

<span data-ttu-id="b9b33-120">Si el búfer de salida es demasiado pequeño, se seguirá devolviendo el tamaño real del marcador.</span><span class="sxs-lookup"><span data-stu-id="b9b33-120">If the output buffer is too small, the actual size of the bookmark will still be returned.</span></span> <span data-ttu-id="b9b33-121">Esto significa que este número será mayor que el tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b9b33-121">That means that this number will be larger than the size of the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="b9b33-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9b33-122">Return Value</span></span>

<span data-ttu-id="b9b33-123">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="b9b33-123">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b9b33-124">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b9b33-124">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9b33-125">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b9b33-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="b9b33-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9b33-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b33-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b9b33-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b9b33-128">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b9b33-128">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b33-129">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="b9b33-129">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="b9b33-130">La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir todo el marcador.</span><span class="sxs-lookup"><span data-stu-id="b9b33-130">The operation completed successfully, but the output buffer was too small to receive the entire bookmark.</span></span> <span data-ttu-id="b9b33-131">El búfer de salida se ha rellenado con tanta parte del marcador como quepa.</span><span class="sxs-lookup"><span data-stu-id="b9b33-131">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="b9b33-132">También se ha devuelto el tamaño real del marcador, si se solicita.</span><span class="sxs-lookup"><span data-stu-id="b9b33-132">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b33-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b9b33-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b9b33-134">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b9b33-134">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b33-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b9b33-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b9b33-136">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="b9b33-136">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b9b33-137"><strong>Windows XP:  </strong> Estos valores devueltos se introdujeron en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b9b33-137"><strong>Windows XP:  </strong>This return values is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b33-138">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="b9b33-138">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="b9b33-139">El cursor no está situado en un registro.</span><span class="sxs-lookup"><span data-stu-id="b9b33-139">The cursor is not positioned on a record.</span></span> <span data-ttu-id="b9b33-140">Esto puede ocurrir por diversos motivos.</span><span class="sxs-lookup"><span data-stu-id="b9b33-140">This can happen for many different reasons.</span></span> <span data-ttu-id="b9b33-141">Por ejemplo, esto ocurrirá si el cursor se coloca después del último registro en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="b9b33-141">For example, this will happen if the cursor is positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b33-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b9b33-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b9b33-143">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="b9b33-143">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b33-144">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b9b33-144">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b9b33-145">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b9b33-145">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b33-146">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="b9b33-146">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="b9b33-147">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="b9b33-147">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="b9b33-148"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b9b33-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b33-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b9b33-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b9b33-150">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b9b33-150">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9b33-151">Si esta función se ejecuta correctamente, el marcador del registro asociado a la entrada de índice en la posición actual de un cursor se devolverá en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="b9b33-151">If this function succeeds, the bookmark for the record that is associated with the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="b9b33-152">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b9b33-152">No change to the database state will occur.</span></span>

<span data-ttu-id="b9b33-153">Si se produce un error en esta función, el estado del búfer de salida y del tamaño real del marcador será undefined, a menos que se devuelva JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="b9b33-153">If this function fails, the state of the output buffer and the actual size of the bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="b9b33-154">En caso de que se devuelva JET_errBufferTooSmall, el búfer de salida contendrá tantos del marcador como quepan en el espacio proporcionado y el tamaño real del marcador será preciso.</span><span class="sxs-lookup"><span data-stu-id="b9b33-154">In the event that JET_errBufferTooSmall is returned, the output buffer will contain as much of the bookmark as will fit in the space provided and the actual size of the bookmark will be accurate.</span></span> <span data-ttu-id="b9b33-155">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="b9b33-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b9b33-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b9b33-156">Remarks</span></span>

<span data-ttu-id="b9b33-157">Por lo general, los marcadores se deben tratar como fragmentos opacos de datos.</span><span class="sxs-lookup"><span data-stu-id="b9b33-157">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="b9b33-158">No se realiza ningún intento de aprovechar la estructura interna de estos datos.</span><span class="sxs-lookup"><span data-stu-id="b9b33-158">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="b9b33-159">Sin embargo, se cumplen las siguientes condiciones de todos los marcadores ESENT:</span><span class="sxs-lookup"><span data-stu-id="b9b33-159">However, the following conditions are true of all ESENT bookmarks:</span></span>

  - <span data-ttu-id="b9b33-160">Un marcador identifica de forma única un registro en una tabla determinada.</span><span class="sxs-lookup"><span data-stu-id="b9b33-160">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="b9b33-161">El marcador de un registro no cambiará durante el período de duración de dicho registro.</span><span class="sxs-lookup"><span data-stu-id="b9b33-161">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="b9b33-162">El marcador de un registro es igual que la clave de ese registro en el índice principal de la tabla que contiene ese registro.</span><span class="sxs-lookup"><span data-stu-id="b9b33-162">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="b9b33-163">Si no se define ningún índice principal sobre esa tabla, el motor de base de datos creará su propio marcador para el registro.</span><span class="sxs-lookup"><span data-stu-id="b9b33-163">If no primary index is defined over that table the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="b9b33-164">Los marcadores se pueden comparar entre sí mediante la función [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su orden relativo en el índice principal sobre la tabla de los registros de origen.</span><span class="sxs-lookup"><span data-stu-id="b9b33-164">Bookmarks can be compared against each other using the [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) function to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="b9b33-165">Si no se define ningún índice principal sobre esa tabla, no es significativo usar el orden relativo de los marcadores de esa tabla.</span><span class="sxs-lookup"><span data-stu-id="b9b33-165">If no primary index is defined over that table, it is not meaningful to use the relative ordering of bookmarks from that table.</span></span>

  - <span data-ttu-id="b9b33-166">No tiene sentido comparar los marcadores de los registros de diferentes tablas entre sí.</span><span class="sxs-lookup"><span data-stu-id="b9b33-166">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="b9b33-167">Un marcador siempre es menor o igual que JET_cbBookmarkMost (256) bytes de longitud, antes de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b9b33-167">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length, prior to Windows Vista.</span></span>
    
<span data-ttu-id="b9b33-168">**Windows Vista:** En Windows Vista y versiones posteriores, los marcadores pueden ser mayores que JET_cbBookmarkMost (256) bytes.</span><span class="sxs-lookup"><span data-stu-id="b9b33-168">**Windows Vista:** On Windows Vista and later releases, bookmarks can be larger than JET_cbBookmarkMost (256) bytes.</span></span> <span data-ttu-id="b9b33-169">El tamaño máximo de un marcador es igual al valor actual de JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="b9b33-169">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b9b33-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9b33-170">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9b33-171"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b9b33-171"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b33-172">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b9b33-172">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b33-173"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b9b33-173"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b33-174">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b9b33-174">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b33-175"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b9b33-175"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b33-176">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b9b33-176">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9b33-177"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="b9b33-177"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b33-178">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b9b33-178">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9b33-179"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b9b33-179"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b9b33-180">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b9b33-180">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b9b33-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b9b33-181">See Also</span></span>

[<span data-ttu-id="b9b33-182">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b9b33-182">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b9b33-183">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b9b33-183">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="b9b33-184">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b9b33-184">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="b9b33-185">JetGoToBookmark</span><span class="sxs-lookup"><span data-stu-id="b9b33-185">JetGoToBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="b9b33-186">JetStopService</span><span class="sxs-lookup"><span data-stu-id="b9b33-186">JetStopService</span></span>](./jetstopservice-function.md)  
<span data-ttu-id="b9b33-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="b9b33-187">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
