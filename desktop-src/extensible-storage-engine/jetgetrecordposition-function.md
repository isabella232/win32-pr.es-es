---
description: 'Más información acerca de: JetGetRecordPosition (función)'
title: Función JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082746"
---
# <a name="jetgetrecordposition-function"></a><span data-ttu-id="25217-103">Función JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="25217-103">JetGetRecordPosition Function</span></span>


<span data-ttu-id="25217-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="25217-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordposition-function"></a><span data-ttu-id="25217-105">Función JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="25217-105">JetGetRecordPosition Function</span></span>

<span data-ttu-id="25217-106">La función **JetGetRecordPosition** devuelve la posición fraccionaria del registro actual en el índice actual en forma de estructura de [JET_RECPOS](./jet-recpos-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="25217-106">The **JetGetRecordPosition** function returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-structure.md) structure.</span></span> <span data-ttu-id="25217-107">Esta estructura describe las posiciones fraccionarias en términos de un número aproximado de entradas de índice antes del registro actual y un número total aproximado de entradas en el índice.</span><span class="sxs-lookup"><span data-stu-id="25217-107">This structure describes fractional positions in terms of an approximate number of index entries before the current record and an approximate total number of entries in the index.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a><span data-ttu-id="25217-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25217-108">Parameters</span></span>

<span data-ttu-id="25217-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="25217-109">*sesid*</span></span>

<span data-ttu-id="25217-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="25217-110">The session to use for this call.</span></span>

<span data-ttu-id="25217-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="25217-111">*tableid*</span></span>

<span data-ttu-id="25217-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="25217-112">The cursor to use for this call.</span></span>

<span data-ttu-id="25217-113">*precpos*</span><span class="sxs-lookup"><span data-stu-id="25217-113">*precpos*</span></span>

<span data-ttu-id="25217-114">La descripción de la fracción que se va a usar para obtener la posición del registro actual en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="25217-114">The description of the fraction to use in getting the position of the current record in the current index.</span></span>

<span data-ttu-id="25217-115">*cbRecpos*</span><span class="sxs-lookup"><span data-stu-id="25217-115">*cbRecpos*</span></span>

<span data-ttu-id="25217-116">Tamaño de la memoria asignada en *precpos*.</span><span class="sxs-lookup"><span data-stu-id="25217-116">The size of memory allocated at *precpos*.</span></span>

### <a name="return-value"></a><span data-ttu-id="25217-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25217-117">Return Value</span></span>

<span data-ttu-id="25217-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="25217-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="25217-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="25217-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25217-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="25217-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="25217-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="25217-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25217-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="25217-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="25217-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="25217-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25217-124">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="25217-124">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="25217-125">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="25217-125">It is not possible to complete the operation because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25217-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="25217-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="25217-127">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="25217-127">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25217-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="25217-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="25217-129">No se puede completar esta operación porque la instancia, asociada a la sesión, encontró un error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="25217-129">This operation cannot complete because the instance, associated with the session, encountered a fatal error.</span></span> <span data-ttu-id="25217-130">Es necesario revocar el acceso a todos los datos con el fin de proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="25217-130">It is required that access to all data be revoked in order to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="25217-131"><strong>Windows 2000:</strong>  Este error no lo devolverá el sistema operativo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="25217-131"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25217-132">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="25217-132">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="25217-133">El tamaño de la memoria asignada en <em>precpos</em> no es suficiente.</span><span class="sxs-lookup"><span data-stu-id="25217-133">The size of the allocated memory at <em>precpos</em> is not a sufficient size.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25217-134">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="25217-134">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="25217-135">El cursor no está actualmente en un registro y no puede devolver una posición.</span><span class="sxs-lookup"><span data-stu-id="25217-135">The cursor is not currently on a record and cannot return a position.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25217-136">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="25217-136">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="25217-137">No es posible completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="25217-137">It is not possible to complete the operation because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25217-138">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="25217-138">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="25217-139">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="25217-139">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="25217-140"><strong>Windows 2000:</strong>  Este error no lo devolverá el sistema operativo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="25217-140"><strong>Windows 2000:</strong>  This error will not be returned by the Windows 2000 operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25217-141">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="25217-141">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="25217-142">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="25217-142">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25217-143">Si se ejecuta correctamente, se devuelve el número aproximado de entradas de índice que preceden al registro actual del índice en precpos- \> centriesLT.</span><span class="sxs-lookup"><span data-stu-id="25217-143">On success, the approximate number of index entries preceding the current record in the index are returned in precpos-\>centriesLT.</span></span> <span data-ttu-id="25217-144">se devuelve 1 en precpos- \> centriesInRange.</span><span class="sxs-lookup"><span data-stu-id="25217-144">1 is returned in precpos-\>centriesInRange.</span></span> <span data-ttu-id="25217-145">El número aproximado de entradas en el índice se devuelve en precpos- \> centriesTotal.</span><span class="sxs-lookup"><span data-stu-id="25217-145">The approximate number of entries in the index is returned in precpos-\>centriesTotal.</span></span>

<span data-ttu-id="25217-146">En caso de error, no se realiza ningún cambio en la memoria asignada en *precpos*.</span><span class="sxs-lookup"><span data-stu-id="25217-146">On failure, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="25217-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25217-147">Remarks</span></span>

<span data-ttu-id="25217-148">Esta operación devuelve datos variables cuando las actualizaciones se producen de forma continua en la tabla.</span><span class="sxs-lookup"><span data-stu-id="25217-148">This operation returns varying data when updates occur continuously on the table.</span></span> <span data-ttu-id="25217-149">Los cambios en los valores no siempre coincidirán con las expectativas basadas en el conocimiento de las actualizaciones, ya que los valores son aproximaciones basadas en las propiedades físicas del índice.</span><span class="sxs-lookup"><span data-stu-id="25217-149">The changes in the values will not always match expectations based on knowledge of the updates, since the values are approximations based on physical properties of the index.</span></span> <span data-ttu-id="25217-150">El aislamiento transaccional no se aplica a las posiciones de **JetGetRecordPosition** , ya que los valores dependen de las propiedades físicas del índice que no están aisladas de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="25217-150">Transactional isolation does not apply to positions from **JetGetRecordPosition** since the values depend on physical properties of the index that are not transaction isolated.</span></span>

<span data-ttu-id="25217-151">[JET_RECPOS](./jet-recpos-structure.md) no se deben utilizar para describir un registro de una tabla o para cambiar la posición de un registro cerca de un registro existente.</span><span class="sxs-lookup"><span data-stu-id="25217-151">[JET_RECPOS](./jet-recpos-structure.md) should not be used to describe a record within a table or to reposition a record close to an existing record.</span></span> <span data-ttu-id="25217-152">En su lugar, se deben recuperar los marcadores de un registro existente y, a continuación, usar para cambiar la posición del mismo registro.</span><span class="sxs-lookup"><span data-stu-id="25217-152">Instead, bookmarks for an existing record should be retrieved and then used to reposition the same record.</span></span>

#### <a name="requirements"></a><span data-ttu-id="25217-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25217-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25217-154"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="25217-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="25217-155">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="25217-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25217-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="25217-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="25217-157">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="25217-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25217-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="25217-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="25217-159">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="25217-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25217-160"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="25217-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="25217-161">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="25217-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25217-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="25217-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="25217-163">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="25217-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="25217-164">Consulte también</span><span class="sxs-lookup"><span data-stu-id="25217-164">See Also</span></span>

[<span data-ttu-id="25217-165">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="25217-165">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="25217-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="25217-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="25217-167">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="25217-167">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="25217-168">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="25217-168">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="25217-169">JET_RECPOS</span><span class="sxs-lookup"><span data-stu-id="25217-169">JET_RECPOS</span></span>](./jet-recpos-structure.md)  
[<span data-ttu-id="25217-170">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="25217-170">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="25217-171">JetGotoPosition</span><span class="sxs-lookup"><span data-stu-id="25217-171">JetGotoPosition</span></span>](./jetgotoposition-function.md)  
[<span data-ttu-id="25217-172">JetStopService</span><span class="sxs-lookup"><span data-stu-id="25217-172">JetStopService</span></span>](./jetstopservice-function.md)
