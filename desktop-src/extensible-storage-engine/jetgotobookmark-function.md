---
description: 'Más información acerca de: JetGotoBookmark (función)'
title: JetGotoBookmark función)
TOCTitle: JetGotoBookmark Function
ms:assetid: a9a0aa43-834a-4eec-b47f-8e74d35aa972
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294053(v=EXCHG.10)
ms:contentKeyID: 32765656
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 89dde261648b396bcfc9532911c0d4acd3c88828
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707185"
---
# <a name="jetgotobookmark-function"></a><span data-ttu-id="22996-103">JetGotoBookmark función)</span><span class="sxs-lookup"><span data-stu-id="22996-103">JetGotoBookmark Function</span></span>


<span data-ttu-id="22996-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="22996-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgotobookmark-function"></a><span data-ttu-id="22996-105">JetGotoBookmark función)</span><span class="sxs-lookup"><span data-stu-id="22996-105">JetGotoBookmark Function</span></span>

<span data-ttu-id="22996-106">La función **JetGotoBookmark** coloca un cursor en una entrada de índice para el registro que está asociado al marcador especificado.</span><span class="sxs-lookup"><span data-stu-id="22996-106">The **JetGotoBookmark** function positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="22996-107">El marcador se puede usar con cualquier índice definido en una tabla.</span><span class="sxs-lookup"><span data-stu-id="22996-107">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="22996-108">El marcador de un registro se puede recuperar mediante [JetGetBookmark](./jetgetbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="22996-108">The bookmark for a record can be retrieved using [JetGetBookmark](./jetgetbookmark-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGotoBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvBookmark,
      __in          unsigned long cbBookmark
    );
```

### <a name="parameters"></a><span data-ttu-id="22996-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22996-109">Parameters</span></span>

<span data-ttu-id="22996-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="22996-110">*sesid*</span></span>

<span data-ttu-id="22996-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="22996-111">The session to use for this call.</span></span>

<span data-ttu-id="22996-112">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="22996-112">*tableid*</span></span>

<span data-ttu-id="22996-113">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="22996-113">The cursor to use for this call.</span></span>

<span data-ttu-id="22996-114">*pvBookmark*</span><span class="sxs-lookup"><span data-stu-id="22996-114">*pvBookmark*</span></span>

<span data-ttu-id="22996-115">Búfer que contiene el marcador que se va a usar para colocar el cursor.</span><span class="sxs-lookup"><span data-stu-id="22996-115">The buffer that contains the bookmark to use to position the cursor.</span></span>

<span data-ttu-id="22996-116">*cbBookmark*</span><span class="sxs-lookup"><span data-stu-id="22996-116">*cbBookmark*</span></span>

<span data-ttu-id="22996-117">Tamaño del marcador en el búfer.</span><span class="sxs-lookup"><span data-stu-id="22996-117">The size of the bookmark in the buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="22996-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22996-118">Return Value</span></span>

<span data-ttu-id="22996-119">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="22996-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="22996-120">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="22996-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22996-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="22996-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="22996-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="22996-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22996-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="22996-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="22996-124">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="22996-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22996-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="22996-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="22996-126">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="22996-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22996-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="22996-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="22996-128">No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="22996-128">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="22996-129"><strong>Windows XP:</strong>   Este valor devuelto se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="22996-129"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22996-130">JET_errInvalidBookmark</span><span class="sxs-lookup"><span data-stu-id="22996-130">JET_errInvalidBookmark</span></span></p></td>
<td><p><span data-ttu-id="22996-131">El marcador proporcionado no es válido.</span><span class="sxs-lookup"><span data-stu-id="22996-131">The bookmark that was provided is invalid.</span></span> <span data-ttu-id="22996-132">Esto puede deberse a que el tamaño del marcador es cero o el puntero del búfer del marcador es <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="22996-132">This might have occurred because the size of the bookmark is zero or the bookmark buffer pointer is <strong>NULL</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22996-133">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="22996-133">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="22996-134">El cursor está en un índice secundario y no se encontró ninguna entrada de índice para el registro que está asociado con el marcador.</span><span class="sxs-lookup"><span data-stu-id="22996-134">The cursor is on a secondary index and no index entry could be found for the record that is associated with the bookmark.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22996-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="22996-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="22996-136">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="22996-136">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22996-137">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="22996-137">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="22996-138">No se pudo encontrar el registro asociado al marcador.</span><span class="sxs-lookup"><span data-stu-id="22996-138">The record that is associated with the bookmark could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22996-139">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="22996-139">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="22996-140">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="22996-140">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22996-141">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="22996-141">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="22996-142">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="22996-142">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="22996-143"><strong>Windows XP:</strong>   Este valor devuelto se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="22996-143"><strong>Windows XP:</strong>   This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22996-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="22996-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="22996-145">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="22996-145">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22996-146">Si esta función se ejecuta correctamente, el cursor se colocará en una entrada de índice para el registro asociado al marcador especificado.</span><span class="sxs-lookup"><span data-stu-id="22996-146">If this function succeeds, the cursor will be positioned at an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="22996-147">Si se ha preparado un registro para la actualización, la actualización se cancelará.</span><span class="sxs-lookup"><span data-stu-id="22996-147">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="22996-148">Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="22996-148">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="22996-149">Si se ha construido una clave de búsqueda para el cursor, se eliminará la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="22996-149">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="22996-150">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="22996-150">No change to the database state will occur.</span></span>

<span data-ttu-id="22996-151">Si se produce un error en esta función, la posición del cursor permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="22996-151">If this function fails, the position of the cursor will remain unchanged.</span></span> <span data-ttu-id="22996-152">Si se ha preparado un registro para la actualización, la actualización se cancelará.</span><span class="sxs-lookup"><span data-stu-id="22996-152">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="22996-153">Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="22996-153">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="22996-154">Si se ha construido una clave de búsqueda para el cursor, se eliminará la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="22996-154">If a search key has been constructed for the cursor, that search key will be deleted.</span></span> <span data-ttu-id="22996-155">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="22996-155">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="22996-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22996-156">Remarks</span></span>

<span data-ttu-id="22996-157">Hay dos maneras de usar un marcador para colocar un cursor en un índice.</span><span class="sxs-lookup"><span data-stu-id="22996-157">There are two ways to use a bookmark to position a cursor on an index.</span></span> <span data-ttu-id="22996-158">El primero es usar el marcador para colocarlo directamente en el registro.</span><span class="sxs-lookup"><span data-stu-id="22996-158">The first is to use the bookmark to position on the record directly.</span></span> <span data-ttu-id="22996-159">Esto sucede si el índice actual del cursor es el índice principal.</span><span class="sxs-lookup"><span data-stu-id="22996-159">This occurs when the current index of the cursor is the primary index.</span></span> <span data-ttu-id="22996-160">Esta técnica funciona porque un marcador ESENT es el mismo que el de la clave principal del registro asociado.</span><span class="sxs-lookup"><span data-stu-id="22996-160">This technique works because an ESENT bookmark is the same as the associated record's primary key.</span></span>

<span data-ttu-id="22996-161">La segunda manera de usar un marcador es colocarlo en una entrada de un índice secundario que se corresponda con el registro asociado a dicho marcador.</span><span class="sxs-lookup"><span data-stu-id="22996-161">The second way to use a bookmark is to position it on an entry in a secondary index that corresponds to the record that is associated with that bookmark.</span></span> <span data-ttu-id="22996-162">Durante este proceso, el motor busca el registro real mediante el marcador en el índice principal.</span><span class="sxs-lookup"><span data-stu-id="22996-162">During this process, the engine looks up the actual record using the bookmark on the primary index.</span></span> <span data-ttu-id="22996-163">A continuación, utiliza los datos de registro y la definición de índice secundario para calcular una clave en el índice secundario que apunta al registro.</span><span class="sxs-lookup"><span data-stu-id="22996-163">It then uses the record data and the secondary index definition to compute a key into the secondary index that points to the record.</span></span> <span data-ttu-id="22996-164">A continuación, coloca el cursor en la entrada de índice de esa clave.</span><span class="sxs-lookup"><span data-stu-id="22996-164">It then positions the cursor on the index entry for that key.</span></span> <span data-ttu-id="22996-165">Si el cursor se encuentra actualmente en un índice secundario de una o varias columnas de clave de varios valores, el cursor se colocará en la entrada de índice correspondiente al primer valor múltiple de cada una de esas columnas de clave.</span><span class="sxs-lookup"><span data-stu-id="22996-165">If the cursor is currently on a secondary index over one or more multi-valued key columns, the cursor will be positioned on the index entry corresponding to the first multi-value of each of those key columns.</span></span>

#### <a name="requirements"></a><span data-ttu-id="22996-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22996-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22996-167"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="22996-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="22996-168">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="22996-168">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22996-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="22996-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="22996-170">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="22996-170">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22996-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="22996-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="22996-172">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="22996-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22996-173"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="22996-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="22996-174">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="22996-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22996-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="22996-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="22996-176">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="22996-176">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="22996-177">Consulte también</span><span class="sxs-lookup"><span data-stu-id="22996-177">See Also</span></span>

[<span data-ttu-id="22996-178">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="22996-178">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="22996-179">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="22996-179">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="22996-180">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="22996-180">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="22996-181">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="22996-181">JetGetBookmark</span></span>](./jetgetbookmark-function.md)
