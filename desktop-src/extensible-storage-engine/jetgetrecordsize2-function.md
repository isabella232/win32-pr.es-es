---
description: 'Más información acerca de: JetGetRecordSize2 (función)'
title: JetGetRecordSize2 función)
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717233"
---
# <a name="jetgetrecordsize2-function"></a><span data-ttu-id="7d125-103">JetGetRecordSize2 función)</span><span class="sxs-lookup"><span data-stu-id="7d125-103">JetGetRecordSize2 Function</span></span>


<span data-ttu-id="7d125-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7d125-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetrecordsize2-function"></a><span data-ttu-id="7d125-105">JetGetRecordSize2 función)</span><span class="sxs-lookup"><span data-stu-id="7d125-105">JetGetRecordSize2 Function</span></span>

<span data-ttu-id="7d125-106">La función **JetGetRecordSize2** recupera información de tamaño del registro de la ubicación deseada.</span><span class="sxs-lookup"><span data-stu-id="7d125-106">The **JetGetRecordSize2** function retrieves record size information from the desired location.</span></span>

<span data-ttu-id="7d125-107">**Windows 7: JetGetRecordSize2** se incluye en el sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7d125-107">**Windows 7:  JetGetRecordSize2** is introduced in the Windows 7 operating system.</span></span>

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7d125-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d125-108">Parameters</span></span>

<span data-ttu-id="7d125-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7d125-109">*sesid*</span></span>

<span data-ttu-id="7d125-110">Identifica el contexto de la sesión de base de datos que se utilizará para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="7d125-110">Identifies the database session context that will be used for the API call.</span></span>

<span data-ttu-id="7d125-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="7d125-111">*tableid*</span></span>

<span data-ttu-id="7d125-112">Identifica la tabla o el cursor que se utilizará para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="7d125-112">Identifies the table or cursor that will be used for the API call.</span></span> <span data-ttu-id="7d125-113">El cursor debe estar colocado en un registro o tener una actualización preparada.</span><span class="sxs-lookup"><span data-stu-id="7d125-113">The cursor must be positioned on a record, or have an update prepared.</span></span>

<span data-ttu-id="7d125-114">*precsize*</span><span class="sxs-lookup"><span data-stu-id="7d125-114">*precsize*</span></span>

<span data-ttu-id="7d125-115">Puntero a un búfer de salida para la estructura de [JET_RECSIZE2](./jet-recsize2-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="7d125-115">A pointer to an output buffer for the [JET_RECSIZE2](./jet-recsize2-structure.md) structure.</span></span>

<span data-ttu-id="7d125-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7d125-116">*grbit*</span></span>

<span data-ttu-id="7d125-117">Se trata de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7d125-117">This is one or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d125-118">Value</span><span class="sxs-lookup"><span data-stu-id="7d125-118">Value</span></span></p></th>
<th><p><span data-ttu-id="7d125-119">Significado</span><span class="sxs-lookup"><span data-stu-id="7d125-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d125-120">JET_bitRecordSizeInCopyBuffer</span><span class="sxs-lookup"><span data-stu-id="7d125-120">JET_bitRecordSizeInCopyBuffer</span></span></p></td>
<td><p><span data-ttu-id="7d125-121">Recupera el tamaño del registro que se encuentra en el búfer de copia preparado para la actualización.</span><span class="sxs-lookup"><span data-stu-id="7d125-121">This retrieves the size of the record that is in the copy buffer prepared for update.</span></span> <span data-ttu-id="7d125-122">De lo contrario <em>, el ID. de</em> reactivación o el cursor deben estar colocados en un registro y se utilizará ese registro.</span><span class="sxs-lookup"><span data-stu-id="7d125-122">Otherwise, the <em>tableid</em> or cursor must be positioned on a record, and that record will be used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d125-123">JET_bitRecordSizeRunningTotal</span><span class="sxs-lookup"><span data-stu-id="7d125-123">JET_bitRecordSizeRunningTotal</span></span></p></td>
<td><p><span data-ttu-id="7d125-124">Cuando se especifica este bit, el <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> no se pone a cero antes de rellenar el contenido, lo que actúa de forma eficaz como acumulación de las estadísticas para varios registros visitados o actualizados.</span><span class="sxs-lookup"><span data-stu-id="7d125-124">When this bit is specified, the <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> is not zeroed before filling the contents, effectively acting as an accumulation of the statistics for multiple records visited or updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d125-125">JET_bitRecordSizeLocal</span><span class="sxs-lookup"><span data-stu-id="7d125-125">JET_bitRecordSizeLocal</span></span></p></td>
<td><p><span data-ttu-id="7d125-126">Esto hace que la API omita los valores largos no intrínsecos.</span><span class="sxs-lookup"><span data-stu-id="7d125-126">This causes the API to ignore non-intrinsic Long Values.</span></span> <span data-ttu-id="7d125-127">Por ejemplo, solo se utilizará el registro local de la página.</span><span class="sxs-lookup"><span data-stu-id="7d125-127">For example, only the local record on the page will be used.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7d125-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d125-128">Return Value</span></span>

<span data-ttu-id="7d125-129">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="7d125-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7d125-130">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7d125-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d125-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7d125-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="7d125-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d125-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d125-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7d125-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7d125-134">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7d125-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d125-135">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="7d125-135">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="7d125-136">Una de las opciones solicitadas no era válida o no se implementó.</span><span class="sxs-lookup"><span data-stu-id="7d125-136">One of the requested options was invalid or not implemented.</span></span> <span data-ttu-id="7d125-137">Este error lo devolverá la función <strong>JetGetRecordSize2</strong> cuando se especifica un <em>grbit</em> no válido.</span><span class="sxs-lookup"><span data-stu-id="7d125-137">This error will be returned by the <strong>JetGetRecordSize2</strong> function when an illegal <em>grbit</em> is specified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d125-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7d125-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7d125-139">No es posible completar la operación porque no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7d125-139">It is not possible to complete the operation because the instance associated with the session has not been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d125-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7d125-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7d125-141">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="7d125-141">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d125-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7d125-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7d125-143">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="7d125-143">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="7d125-144"><strong>Windows XP:  </strong> JET_errInstanceUnavailable solo lo devolverá el sistema operativo Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d125-144"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by the Windows XP operating system and later versions of Windows.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d125-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7d125-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7d125-146">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7d125-146">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d125-147">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7d125-147">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7d125-148">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7d125-148">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d125-149">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7d125-149">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7d125-150">No es válido utilizar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7d125-150">It is illegal to use the same session for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="7d125-151"><strong>Windows XP:  </strong> JET_errInstanceUnavailable solo se devolverán en Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="7d125-151"><strong>Windows XP:  </strong>JET_errInstanceUnavailable will only be returned by Windows XP and later versions of Windows.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d125-152">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="7d125-152">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="7d125-153">Esto puede ocurrir si el cursor se colocó incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="7d125-153">This can happen if the cursor was positioned incorrectly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d125-154">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="7d125-154">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="7d125-155">Si el cursor no se colocó en una transacción, esto puede ocurrir si otro subproceso elimina el registro de esta sesión.</span><span class="sxs-lookup"><span data-stu-id="7d125-155">If the cursor was not positioned in a transaction, this can happen if another thread deletes the record out from under this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d125-156">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="7d125-156">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="7d125-157">Se puede devolver si se ha pasado un valor de<em>Precsize</em> <strong>nulo</strong>.</span><span class="sxs-lookup"><span data-stu-id="7d125-157">This can be returned if a <strong>NULL</strong><em>precsize</em> was passed.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="7d125-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d125-158">Remarks</span></span>

<span data-ttu-id="7d125-159">El tamaño de la clave acumulada en el campo **cbOverhead** de [JET_RECSIZE2](./jet-recsize2-structure.md), se ve afectado por JET_bitRecordSizeInCopyBuffer.</span><span class="sxs-lookup"><span data-stu-id="7d125-159">The size of the key accumulated in the **cbOverhead** field of [JET_RECSIZE2](./jet-recsize2-structure.md), is affected by JET_bitRecordSizeInCopyBuffer.</span></span> <span data-ttu-id="7d125-160">Si se especifica este bit, el tamaño de clave acumulado en el campo **cbOverhead** es el tamaño de clave completo.</span><span class="sxs-lookup"><span data-stu-id="7d125-160">If this bit is specified, the key size accumulated in the **cbOverhead** field is the full key size.</span></span> <span data-ttu-id="7d125-161">Si no se usa este bit, el tamaño de clave acumulado no incluirá ningún tamaño guardado debido a la compresión de prefijo de clave.</span><span class="sxs-lookup"><span data-stu-id="7d125-161">If this bit is not used, the key size accumulated will not include any size saved due to key prefix compression.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7d125-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d125-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d125-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7d125-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7d125-164">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7d125-164">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d125-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7d125-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7d125-166">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7d125-166">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d125-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7d125-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7d125-168">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="7d125-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d125-169"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="7d125-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7d125-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7d125-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d125-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7d125-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7d125-172">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7d125-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7d125-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7d125-173">See Also</span></span>

[<span data-ttu-id="7d125-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7d125-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7d125-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7d125-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7d125-176">JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="7d125-176">JET_RECSIZE</span></span>](./jet-recsize-structure.md)  
[<span data-ttu-id="7d125-177">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7d125-177">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7d125-178">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7d125-178">JET_TABLEID</span></span>](./jet-tableid.md)
