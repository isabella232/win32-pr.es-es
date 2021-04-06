---
description: 'Más información acerca de: JetGotoSecondaryIndexBookmark (función)'
title: JetGotoSecondaryIndexBookmark función)
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002113"
---
# <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="aae97-103">JetGotoSecondaryIndexBookmark función)</span><span class="sxs-lookup"><span data-stu-id="aae97-103">JetGotoSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="aae97-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="aae97-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotosecondaryindexbookmark-function"></a><span data-ttu-id="aae97-105">JetGotoSecondaryIndexBookmark función)</span><span class="sxs-lookup"><span data-stu-id="aae97-105">JetGotoSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="aae97-106">La función **JetGotoSecondaryIndexBookmark** coloca un cursor en una entrada de índice que está asociada al marcador de índice secundario especificado.</span><span class="sxs-lookup"><span data-stu-id="aae97-106">The **JetGotoSecondaryIndexBookmark** function positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="aae97-107">El marcador de índice secundario debe usarse con el mismo índice en la misma tabla desde la que se recuperó originalmente.</span><span class="sxs-lookup"><span data-stu-id="aae97-107">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="aae97-108">El marcador de índice secundario de una entrada de índice se puede recuperar mediante **JetGotoSecondaryIndexBookmark**.</span><span class="sxs-lookup"><span data-stu-id="aae97-108">The secondary index bookmark for an index entry can be retrieved using **JetGotoSecondaryIndexBookmark**.</span></span>

<span data-ttu-id="aae97-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aae97-109">**Windows XP:**  **JetGotoSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="aae97-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aae97-110">Parameters</span></span>

<span data-ttu-id="aae97-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="aae97-111">*sesid*</span></span>

<span data-ttu-id="aae97-112">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="aae97-112">The session to use for this call.</span></span>

<span data-ttu-id="aae97-113">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="aae97-113">*tableid*</span></span>

<span data-ttu-id="aae97-114">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="aae97-114">The cursor to use for this call.</span></span>

<span data-ttu-id="aae97-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="aae97-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="aae97-116">Búfer que contiene la clave secundaria que se va a usar para colocar el cursor.</span><span class="sxs-lookup"><span data-stu-id="aae97-116">The buffer that contains the secondary key to use to position the cursor.</span></span>

<span data-ttu-id="aae97-117">*cbSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="aae97-117">*cbSecondaryKey*</span></span>

<span data-ttu-id="aae97-118">Tamaño de la clave secundaria en el búfer.</span><span class="sxs-lookup"><span data-stu-id="aae97-118">The size of the secondary key in the buffer.</span></span>

<span data-ttu-id="aae97-119">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="aae97-119">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="aae97-120">Búfer que contiene el marcador de la clave principal que se va a usar para colocar el cursor.</span><span class="sxs-lookup"><span data-stu-id="aae97-120">The buffer that contains the primary key bookmark to use to position the cursor.</span></span>

<span data-ttu-id="aae97-121">*cbPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="aae97-121">*cbPrimaryBookmark*</span></span>

<span data-ttu-id="aae97-122">Tamaño del marcador de la clave principal en el búfer.</span><span class="sxs-lookup"><span data-stu-id="aae97-122">The size of the primary key bookmark in the buffer.</span></span>

<span data-ttu-id="aae97-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="aae97-123">*grbit*</span></span>

<span data-ttu-id="aae97-124">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="aae97-124">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aae97-125">Value</span><span class="sxs-lookup"><span data-stu-id="aae97-125">Value</span></span></p></th>
<th><p><span data-ttu-id="aae97-126">Significado</span><span class="sxs-lookup"><span data-stu-id="aae97-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aae97-127">JET_bitBookmarkPermitVirtualCurrency</span><span class="sxs-lookup"><span data-stu-id="aae97-127">JET_bitBookmarkPermitVirtualCurrency</span></span></p></td>
<td><p><span data-ttu-id="aae97-128">En caso de que ya no se pueda encontrar la entrada de índice, el cursor se dejará situado donde esa entrada de índice se haya encontrado previamente.</span><span class="sxs-lookup"><span data-stu-id="aae97-128">In the event that the index entry can no longer be found, the cursor will be left positioned where that index entry was previously found.</span></span> <span data-ttu-id="aae97-129">La operación todavía producirá un error con JET_errRecordDeleted; sin embargo, será posible moverse a la entrada de índice siguiente o anterior en relación con la entrada de índice que ahora falta.</span><span class="sxs-lookup"><span data-stu-id="aae97-129">The operation will still fail with JET_errRecordDeleted; however, it will be possible to move to the next or previous index entry relative to the index entry that is now missing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="aae97-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aae97-130">Return Value</span></span>

<span data-ttu-id="aae97-131">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="aae97-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="aae97-132">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="aae97-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aae97-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="aae97-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="aae97-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="aae97-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aae97-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="aae97-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="aae97-136">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="aae97-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aae97-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="aae97-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="aae97-138">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="aae97-138">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aae97-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="aae97-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="aae97-140">No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="aae97-140">The operation cannot complete because is because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="aae97-141"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aae97-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aae97-142">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="aae97-142">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="aae97-143">El marcador de índice secundario proporcionado no era válido.</span><span class="sxs-lookup"><span data-stu-id="aae97-143">The secondary index bookmark that was provided was invalid.</span></span> <span data-ttu-id="aae97-144">Este error puede deberse a que la clave secundaria es cero o el puntero del búfer de clave secundaria es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="aae97-144">This error might have occurred because the secondary key is zero or the secondary key buffer pointer is <strong>NULL</strong>.</span></span> <span data-ttu-id="aae97-145">Este error se produce porque</span><span class="sxs-lookup"><span data-stu-id="aae97-145">This error occurs because</span></span></p>
<ul>
<li><p><span data-ttu-id="aae97-146">El índice secundario actual no tiene una restricción de unicidad y el tamaño del marcador proporcionado es cero.</span><span class="sxs-lookup"><span data-stu-id="aae97-146">The current secondary index does not have a uniqueness constraint and the size of the provided bookmark is zero.</span></span></p></li>
<li><p><span data-ttu-id="aae97-147">El puntero de búfer de marcador es <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="aae97-147">The bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aae97-148">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="aae97-148">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="aae97-149">El cursor no está actualmente en un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="aae97-149">The cursor is not currently on a secondary index.</span></span> <span data-ttu-id="aae97-150">No es significativo ir a un marcador de índice secundario cuando el cursor no está utilizando actualmente un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="aae97-150">It is not meaningful to go to a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="aae97-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> debe usarse cuando el cursor no está en un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="aae97-151"><a href="gg294053(v=exchg.10).md">JetGotoBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aae97-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="aae97-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="aae97-153">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="aae97-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aae97-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="aae97-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="aae97-155">No se encontró la entrada de índice asociada al marcador de índice secundario.</span><span class="sxs-lookup"><span data-stu-id="aae97-155">The index entry that is associated with the secondary index bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aae97-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="aae97-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="aae97-157">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="aae97-157">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aae97-158">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="aae97-158">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="aae97-159">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="aae97-159">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="aae97-160"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aae97-160"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aae97-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="aae97-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="aae97-162">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="aae97-162">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aae97-163">Si esta función se ejecuta correctamente, el cursor se colocará en una entrada de índice asociada al marcador de índice secundario especificado.</span><span class="sxs-lookup"><span data-stu-id="aae97-163">If this function succeeds, the cursor will be positioned at an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="aae97-164">Si se ha preparado un registro para la actualización, la actualización se cancelará.</span><span class="sxs-lookup"><span data-stu-id="aae97-164">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="aae97-165">Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="aae97-165">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="aae97-166">Si se ha creado una clave de búsqueda para el cursor que se va a usar, se eliminará la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="aae97-166">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="aae97-167">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="aae97-167">No change to the database state will occur.</span></span>

<span data-ttu-id="aae97-168">Si se produce un error en esta función, la posición del cursor permanece inalterada a menos que se devuelva JET_errRecordDeleted y se especifique JET_bitBookmarkPermitVirtualCurrency.</span><span class="sxs-lookup"><span data-stu-id="aae97-168">If this function fails, the position of the cursor remains unchanged unless JET_errRecordDeleted is returned and JET_bitBookmarkPermitVirtualCurrency is specified.</span></span> <span data-ttu-id="aae97-169">En ese caso, el cursor se colocará donde habría sido la entrada de índice asociada al marcador de índice secundario especificado.</span><span class="sxs-lookup"><span data-stu-id="aae97-169">In that case, the cursor will be positioned where the index entry that is associated with the specified secondary index bookmark would have been.</span></span> <span data-ttu-id="aae97-170">El cursor se puede mover con respecto a esa posición, pero todavía no está en una entrada de índice válida.</span><span class="sxs-lookup"><span data-stu-id="aae97-170">The cursor can be moved relative to that position, but is still not on a valid index entry.</span></span>

<span data-ttu-id="aae97-171">Si se ha preparado un registro para la actualización, la actualización se cancelará.</span><span class="sxs-lookup"><span data-stu-id="aae97-171">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="aae97-172">Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="aae97-172">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="aae97-173">Si se ha creado una clave de búsqueda para el cursor que se va a usar, se eliminará la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="aae97-173">If a search key has been constructed for the cursor to use, that search key will be deleted.</span></span> <span data-ttu-id="aae97-174">En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="aae97-174">In any case, no change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="aae97-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aae97-175">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aae97-176"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="aae97-176"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="aae97-177">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aae97-177">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aae97-178"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="aae97-178"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="aae97-179">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aae97-179">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aae97-180"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="aae97-180"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="aae97-181">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="aae97-181">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aae97-182"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="aae97-182"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="aae97-183">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="aae97-183">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aae97-184"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="aae97-184"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="aae97-185">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="aae97-185">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="aae97-186">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aae97-186">See Also</span></span>

[<span data-ttu-id="aae97-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="aae97-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="aae97-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="aae97-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="aae97-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="aae97-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="aae97-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="aae97-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="aae97-191">JetGetSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="aae97-191">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)  
[<span data-ttu-id="aae97-192">JetGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="aae97-192">JetGotoBookmark</span></span>](./jetgotobookmark-function.md)  
[<span data-ttu-id="aae97-193">JetStopService</span><span class="sxs-lookup"><span data-stu-id="aae97-193">JetStopService</span></span>](./jetstopservice-function.md)
