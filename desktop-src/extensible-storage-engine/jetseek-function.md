---
description: 'Más información acerca de: JetSeek (función)'
title: JetSeek función)
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707177"
---
# <a name="jetseek-function"></a><span data-ttu-id="61a8b-103">JetSeek función)</span><span class="sxs-lookup"><span data-stu-id="61a8b-103">JetSeek Function</span></span>


<span data-ttu-id="61a8b-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="61a8b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetseek-function"></a><span data-ttu-id="61a8b-105">JetSeek función)</span><span class="sxs-lookup"><span data-stu-id="61a8b-105">JetSeek Function</span></span>

<span data-ttu-id="61a8b-106">La función **JetSeek** coloca de forma eficaz un cursor en una entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada.</span><span class="sxs-lookup"><span data-stu-id="61a8b-106">The **JetSeek** function efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="61a8b-107">Una clave de búsqueda se debe haber construido previamente mediante [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="61a8b-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="61a8b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61a8b-108">Parameters</span></span>

<span data-ttu-id="61a8b-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="61a8b-109">*sesid*</span></span>

<span data-ttu-id="61a8b-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="61a8b-110">The session to use for this call.</span></span>

<span data-ttu-id="61a8b-111">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="61a8b-111">*tableid*</span></span>

<span data-ttu-id="61a8b-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="61a8b-112">The cursor to use for this call.</span></span>

<span data-ttu-id="61a8b-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="61a8b-113">*grbit*</span></span>

<span data-ttu-id="61a8b-114">Grupo de bits que contiene las opciones que se van a utilizar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="61a8b-114">A group of bits that contain the options to be used for this call.</span></span> <span data-ttu-id="61a8b-115">*Grbit* debe ser distinto de cero y debe incluir uno o varios de los valores enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="61a8b-115">*Grbit* must be nonzero and must include one or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61a8b-116">Value</span><span class="sxs-lookup"><span data-stu-id="61a8b-116">Value</span></span></p></th>
<th><p><span data-ttu-id="61a8b-117">Significado</span><span class="sxs-lookup"><span data-stu-id="61a8b-117">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-118">JET_bitCheckUniqueness</span><span class="sxs-lookup"><span data-stu-id="61a8b-118">JET_bitCheckUniqueness</span></span></p></td>
<td><p><span data-ttu-id="61a8b-119">Se devolverá un código de error especial, JET_wrnUniqueKey, si se puede determinar de forma económica que hay exactamente una entrada de índice que coincide con la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-119">A special error code, JET_wrnUniqueKey, will be returned if it can be cheaply determined that there is exactly one index entry that matches the search key.</span></span></p>
<p><span data-ttu-id="61a8b-120">Esta opción se omite a menos que también se especifique JET_bitSeekEQ.</span><span class="sxs-lookup"><span data-stu-id="61a8b-120">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p>
<p><span data-ttu-id="61a8b-121">Esta opción solo está disponible en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61a8b-121">This option is only available on Windows Server 2003 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-122">JET_bitSeekEQ</span><span class="sxs-lookup"><span data-stu-id="61a8b-122">JET_bitSeekEQ</span></span></p></td>
<td><p><span data-ttu-id="61a8b-123">El cursor se colocará en la entrada de índice más cercana al inicio del índice que coincida exactamente con la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-123">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span> <span data-ttu-id="61a8b-124">El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de dicho índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-124">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="61a8b-125">El inicio del índice no es el mismo que el extremo inferior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-125">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="61a8b-126">No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín.</span><span class="sxs-lookup"><span data-stu-id="61a8b-126">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-127">JET_bitSeekGE</span><span class="sxs-lookup"><span data-stu-id="61a8b-127">JET_bitSeekGE</span></span></p></td>
<td><p><span data-ttu-id="61a8b-128">El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-128">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="61a8b-129">El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de dicho índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-129">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="61a8b-130">El inicio del índice no es el mismo que el extremo inferior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-130">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="61a8b-131">No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar las entradas de índice más cercanas al final del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-131">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-132">JET_bitSeekGT</span><span class="sxs-lookup"><span data-stu-id="61a8b-132">JET_bitSeekGT</span></span></p></td>
<td><p><span data-ttu-id="61a8b-133">El cursor se colocará en la entrada de índice más cercana al inicio del índice que sea mayor que una entrada de índice que coincida exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-133">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="61a8b-134">El inicio del índice es la entrada de índice que se encuentra al pasar al primer registro de dicho índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-134">The start of the index is the index entry that is found when moving to the first record in that index.</span></span> <span data-ttu-id="61a8b-135">El inicio del índice no es el mismo que el extremo inferior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-135">The start of the index is not the same as the low end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="61a8b-136">No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-136">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-137">JET_bitSeekLE</span><span class="sxs-lookup"><span data-stu-id="61a8b-137">JET_bitSeekLE</span></span></p></td>
<td><p><span data-ttu-id="61a8b-138">El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor o igual que una entrada de índice que coincida exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-138">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="61a8b-139">El final del índice es la entrada de índice que se encuentra al pasar al último registro de dicho índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-139">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="61a8b-140">El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-140">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="61a8b-141">No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-141">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-142">JET_bitSeekLT</span><span class="sxs-lookup"><span data-stu-id="61a8b-142">JET_bitSeekLT</span></span></p></td>
<td><p><span data-ttu-id="61a8b-143">El cursor se colocará en la entrada de índice más cercana al final del índice que sea menor que una entrada de índice que coincida exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-143">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span> <span data-ttu-id="61a8b-144">El final del índice es la entrada de índice que se encuentra al pasar al último registro de dicho índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-144">The end of the index is the index entry that is found when moving to the last record in that index.</span></span> <span data-ttu-id="61a8b-145">El final del índice no es el mismo que el extremo superior del índice, que puede cambiar en función del criterio de ordenación de las columnas de clave del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-145">The end of the index is not the same as the high end of the index, which can change depending on the sort order of the key columns in the index.</span></span></p>
<p><span data-ttu-id="61a8b-146">No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar las entradas de índice más cercanas al final del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-146">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-147">JET_bitSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="61a8b-147">JET_bitSetIndexRange</span></span></p></td>
<td><p><span data-ttu-id="61a8b-148">Se configurará automáticamente un intervalo de índice para todas las claves que coincidan exactamente con la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-148">An index range will automatically be setup for all keys that exactly match the search key.</span></span> <span data-ttu-id="61a8b-149">El intervalo de índice resultante es idéntico al que se habría creado mediante una llamada a <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> con las opciones JET_bitRangeInclusive y JET_bitRangeUpperLimit.</span><span class="sxs-lookup"><span data-stu-id="61a8b-149">The resulting index range is identical to one that would have otherwise been created by a call to <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> with the JET_bitRangeInclusive and JET_bitRangeUpperLimit options.</span></span> <span data-ttu-id="61a8b-150">Vea <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="61a8b-150">See <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> for more information.</span></span></p>
<p><span data-ttu-id="61a8b-151">Este es un método práctico para detectar todas las entradas de índice que coinciden con los mismos criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-151">This is a convenient method for discovering all the index entries that match the same search criteria.</span></span></p>
<p><span data-ttu-id="61a8b-152">Esta opción se omite a menos que también se especifique JET_bitSeekEQ.</span><span class="sxs-lookup"><span data-stu-id="61a8b-152">This option is ignored unless JET_bitSeekEQ is also specified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="61a8b-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61a8b-153">Return Value</span></span>

<span data-ttu-id="61a8b-154">Esta función permite que se devuelvan los [JET_ERRs](./jet-err.md) definidos en esta API.</span><span class="sxs-lookup"><span data-stu-id="61a8b-154">This function allows for the return of any [JET_ERRs](./jet-err.md) that are defined in this API.</span></span> <span data-ttu-id="61a8b-155">Para obtener más información acerca de los errores de jet, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="61a8b-155">For more information about Jet errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61a8b-156">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="61a8b-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="61a8b-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="61a8b-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="61a8b-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="61a8b-159">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="61a8b-159">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="61a8b-160">En el caso de <strong>JetSeek</strong>, esto significa que se ha encontrado una entrada de índice que coincide exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-160">For <strong>JetSeek</strong>, this means that an index entry was found that exactly matched the search criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-161">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="61a8b-161">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="61a8b-162">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="61a8b-162">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-163">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="61a8b-163">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="61a8b-164">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="61a8b-164">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="61a8b-165">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61a8b-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-166">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="61a8b-166">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="61a8b-167">No hay ninguna clave de búsqueda actual para el cursor.</span><span class="sxs-lookup"><span data-stu-id="61a8b-167">There is no current search key for the cursor.</span></span> <span data-ttu-id="61a8b-168"><strong>JetSeek</strong> requiere que el cursor tenga una clave de búsqueda válida porque la usará para los criterios de búsqueda utilizados para buscar entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-168"><strong>JetSeek</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-169">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="61a8b-169">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="61a8b-170">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="61a8b-170">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-171">JET_errRecordNotFound</span><span class="sxs-lookup"><span data-stu-id="61a8b-171">JET_errRecordNotFound</span></span></p></td>
<td><p><span data-ttu-id="61a8b-172">No se encontró ninguna entrada de índice que coincida con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-172">No index entry was found that matched the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="61a8b-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="61a8b-174">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="61a8b-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-175">JET_wrnSeekNotEqual</span><span class="sxs-lookup"><span data-stu-id="61a8b-175">JET_wrnSeekNotEqual</span></span></p></td>
<td><p><span data-ttu-id="61a8b-176">Se encontró una entrada de índice que coincidía con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-176">An index entry was found that matched the search criteria.</span></span> <span data-ttu-id="61a8b-177">Sin embargo, esa entrada de índice no era una coincidencia exacta.</span><span class="sxs-lookup"><span data-stu-id="61a8b-177">However, that index entry was not an exact match.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-178">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="61a8b-178">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="61a8b-179">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="61a8b-179">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="61a8b-180">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61a8b-180">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-181">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="61a8b-181">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="61a8b-182">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="61a8b-182">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-183">JET_wrnUniqueKey</span><span class="sxs-lookup"><span data-stu-id="61a8b-183">JET_wrnUniqueKey</span></span></p></td>
<td><p><span data-ttu-id="61a8b-184">Se encontró exactamente una entrada de índice que coincide exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-184">Exactly one index entry was found that exactly matched the search criteria.</span></span> <span data-ttu-id="61a8b-185">Este error solo se devolverá si se especificó JET_bitSeekCheckUniqueness y era barato determinar que la entrada de índice coincidente era la única entrada de índice que coincide exactamente con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-185">This error will only be returned if JET_bitSeekCheckUniqueness was specified and it was cheap to determine that the matching index entry was the only index entry that exactly matches the search criteria.</span></span></p>
<p><span data-ttu-id="61a8b-186">Este error solo lo devolverán Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61a8b-186">This error will only be returned by Windows Server 2003 and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61a8b-187">Si se ejecuta correctamente, el cursor se colocará en una entrada de índice que coincida con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="61a8b-187">On success, the cursor will be positioned at an index entry that matches the search criteria.</span></span> <span data-ttu-id="61a8b-188">Si se ha preparado un registro para la actualización, la actualización se cancelará.</span><span class="sxs-lookup"><span data-stu-id="61a8b-188">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="61a8b-189">Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="61a8b-189">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="61a8b-190">Si se ha construido una clave de búsqueda para el cursor, esa clave de búsqueda se eliminará.</span><span class="sxs-lookup"><span data-stu-id="61a8b-190">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="61a8b-191">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="61a8b-191">No change to the database state will occur.</span></span> <span data-ttu-id="61a8b-192">Cuando varias entradas de índice tienen el mismo valor, siempre se selecciona la entrada más cercana al inicio del índice.</span><span class="sxs-lookup"><span data-stu-id="61a8b-192">When multiple index entries have the same value, the entry closest to the start of the index is always selected.</span></span>

<span data-ttu-id="61a8b-193">En caso de error, la posición del cursor permanecerá sin cambios a menos que se devuelva JET_errRecordNotFound.</span><span class="sxs-lookup"><span data-stu-id="61a8b-193">On failure, the position of the cursor will remain unchanged unless JET_errRecordNotFound was returned.</span></span> <span data-ttu-id="61a8b-194">En ese caso, el cursor se colocará donde la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada habría sido.</span><span class="sxs-lookup"><span data-stu-id="61a8b-194">In that case, the cursor will be positioned where the index entry that matched the search criteria specified by the search key in that cursor and the specified inequality would have been.</span></span> <span data-ttu-id="61a8b-195">El cursor se puede mover en relación con esa posición, pero aún no se encuentra en una entrada de índice válida.</span><span class="sxs-lookup"><span data-stu-id="61a8b-195">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="61a8b-196">Si se ha preparado un registro para la actualización, la actualización se cancelará.</span><span class="sxs-lookup"><span data-stu-id="61a8b-196">If a record has been prepared for update, then that update will be canceled.</span></span> <span data-ttu-id="61a8b-197">Si hay un intervalo de índice en vigor, se cancelará ese intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="61a8b-197">If an index range is in effect, that index range will be canceled.</span></span> <span data-ttu-id="61a8b-198">Si se ha construido una clave de búsqueda para el cursor, esa clave de búsqueda se eliminará.</span><span class="sxs-lookup"><span data-stu-id="61a8b-198">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="61a8b-199">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="61a8b-199">No change to the database state will occur.</span></span>

#### <a name="requirements"></a><span data-ttu-id="61a8b-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61a8b-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="61a8b-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="61a8b-202">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="61a8b-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="61a8b-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="61a8b-204">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="61a8b-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="61a8b-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="61a8b-206">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="61a8b-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a8b-207"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="61a8b-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="61a8b-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="61a8b-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61a8b-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="61a8b-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="61a8b-210">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="61a8b-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="61a8b-211">Consulte también</span><span class="sxs-lookup"><span data-stu-id="61a8b-211">See Also</span></span>

[<span data-ttu-id="61a8b-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="61a8b-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="61a8b-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="61a8b-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="61a8b-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="61a8b-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="61a8b-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="61a8b-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="61a8b-216">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="61a8b-216">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="61a8b-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="61a8b-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="61a8b-218">JetStopService</span><span class="sxs-lookup"><span data-stu-id="61a8b-218">JetStopService</span></span>](./jetstopservice-function.md)
