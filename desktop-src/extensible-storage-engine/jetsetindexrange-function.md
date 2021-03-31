---
description: 'Más información acerca de: JetSetIndexRange (función)'
title: Función JetSetIndexRange
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883085633bebf25180c82f0f8917f6fa31fe7304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275561"
---
# <a name="jetsetindexrange-function"></a><span data-ttu-id="d37e9-103">Función JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d37e9-103">JetSetIndexRange Function</span></span>


<span data-ttu-id="d37e9-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d37e9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetindexrange-function"></a><span data-ttu-id="d37e9-105">Función JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d37e9-105">JetSetIndexRange Function</span></span>

<span data-ttu-id="d37e9-106">La función **JetSetIndexRange** limita temporalmente el conjunto de entradas de índice que el cursor puede recorrer con [JetMove](./jetmove-function.md) para que empiecen a partir de la entrada de índice actual y terminen en la entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y los criterios enlazados especificados.</span><span class="sxs-lookup"><span data-stu-id="d37e9-106">The **JetSetIndexRange** function temporarily limits the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria specified by the search key in that cursor and the specified bound criteria.</span></span> <span data-ttu-id="d37e9-107">Una clave de búsqueda se debe haber construido previamente mediante [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="d37e9-107">A search key must have been previously constructed using [JetMakeKey](./jetmakekey-function.md).</span></span>

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="d37e9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d37e9-108">Parameters</span></span>

<span data-ttu-id="d37e9-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d37e9-109">*sesid*</span></span>

<span data-ttu-id="d37e9-110">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="d37e9-110">The session to use for this call.</span></span>

<span data-ttu-id="d37e9-111">*tableidSrc*</span><span class="sxs-lookup"><span data-stu-id="d37e9-111">*tableidSrc*</span></span>

<span data-ttu-id="d37e9-112">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="d37e9-112">The cursor to use for this call.</span></span>

<span data-ttu-id="d37e9-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d37e9-113">*grbit*</span></span>

<span data-ttu-id="d37e9-114">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d37e9-114">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d37e9-115">Value</span><span class="sxs-lookup"><span data-stu-id="d37e9-115">Value</span></span></p></th>
<th><p><span data-ttu-id="d37e9-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d37e9-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-117">JET_bitRangeInclusive</span><span class="sxs-lookup"><span data-stu-id="d37e9-117">JET_bitRangeInclusive</span></span></p></td>
<td><p><span data-ttu-id="d37e9-118">Esta opción o ausencia de esta opción indica los criterios de límite del intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="d37e9-118">This presence or absence of this option indicates the boundary criteria of the index range.</span></span> <span data-ttu-id="d37e9-119">Cuando está presente, esta opción indica que el límite del intervalo de índice es inclusivo.</span><span class="sxs-lookup"><span data-stu-id="d37e9-119">When present, this option indicates that the limit of the index range is inclusive.</span></span> <span data-ttu-id="d37e9-120">Cuando está ausente, esta opción indica que el límite del intervalo de índice es exclusivo.</span><span class="sxs-lookup"><span data-stu-id="d37e9-120">When absent, this option indicates that the limit of the index range is exclusive.</span></span> <span data-ttu-id="d37e9-121">Cuando el límite del intervalo de índice es inclusivo, las entradas de índice que coinciden exactamente con los criterios de búsqueda se incluyen en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="d37e9-121">When the limit of the index range is inclusive then any index entries exactly matching the search criteria are included in the range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-122">JET_bitRangeInstantDuration</span><span class="sxs-lookup"><span data-stu-id="d37e9-122">JET_bitRangeInstantDuration</span></span></p></td>
<td><p><span data-ttu-id="d37e9-123">Esta opción solicita que se quite el intervalo de índice en cuanto se haya establecido.</span><span class="sxs-lookup"><span data-stu-id="d37e9-123">This option requests that the index range be removed as soon as it has been established.</span></span> <span data-ttu-id="d37e9-124">Todos los demás aspectos de la operación permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d37e9-124">All other aspects of the operation remain unchanged.</span></span> <span data-ttu-id="d37e9-125">Esto resulta útil para probar la existencia de entradas de índice que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d37e9-125">This is useful for testing for the existence of index entries that match the search criteria.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-126">JET_bitRangeRemove</span><span class="sxs-lookup"><span data-stu-id="d37e9-126">JET_bitRangeRemove</span></span></p></td>
<td><p><span data-ttu-id="d37e9-127">Esta opción solicita que se cancele un intervalo de índice existente en el cursor.</span><span class="sxs-lookup"><span data-stu-id="d37e9-127">This option requests that an existing index range on the cursor be canceled.</span></span> <span data-ttu-id="d37e9-128">Una vez que se cancele el intervalo de índice, será posible moverse más allá del final del intervalo de índices mediante <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="d37e9-128">Once the index range is canceled, it will be possible to move beyond the end of the index range using <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span> <span data-ttu-id="d37e9-129">Si un intervalo de índice no está ya en vigor, se producirá un error en <strong>JetSetIndexRange</strong> con JET_errInvalidOperation.</span><span class="sxs-lookup"><span data-stu-id="d37e9-129">If an index range is not already in effect, then <strong>JetSetIndexRange</strong> will fail with JET_errInvalidOperation.</span></span></p>
<p><span data-ttu-id="d37e9-130">Cuando se especifica esta opción, se omiten todas las demás opciones.</span><span class="sxs-lookup"><span data-stu-id="d37e9-130">When this option is specified, all other options are ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-131">JET_bitRangeUpperLimit</span><span class="sxs-lookup"><span data-stu-id="d37e9-131">JET_bitRangeUpperLimit</span></span></p></td>
<td><p><span data-ttu-id="d37e9-132">Si se usa esta opción, la clave de búsqueda del cursor representa los criterios de búsqueda para la entrada de índice más cercana al final del índice que coincidirá con el intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="d37e9-132">If this option is used, then the search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span> <span data-ttu-id="d37e9-133">El intervalo de índice se establecerá entre la posición actual del cursor y esta entrada de índice para que se puedan encontrar todas las coincidencias recorriendo en el índice mediante <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MoveNext o un desplazamiento positivo.</span><span class="sxs-lookup"><span data-stu-id="d37e9-133">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking forward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MoveNext or a positive offset.</span></span></p>
<p><span data-ttu-id="d37e9-134">No es significativo usar esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar entradas de índice más cercanas al inicio del índice.</span><span class="sxs-lookup"><span data-stu-id="d37e9-134">It is not meaningful to use this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the start of the index.</span></span></p>
<p><span data-ttu-id="d37e9-135">Si se omite esta opción, la clave de búsqueda del cursor representa los criterios de búsqueda para la entrada de índice más cercana al inicio del índice que coincidirá con el intervalo de índice.</span><span class="sxs-lookup"><span data-stu-id="d37e9-135">If this option is omitted, then the search key in the cursor represents the search criteria for the index entry closest to the start of the index that will match the index range.</span></span> <span data-ttu-id="d37e9-136">El intervalo de índice se establecerá entre la posición actual del cursor y esta entrada de índice para que se puedan encontrar todas las coincidencias recorriendo hacia atrás el índice mediante <a href="gg294117(v=exchg.10).md">JetMove</a> con JET_MovePrevious o un desplazamiento negativo.</span><span class="sxs-lookup"><span data-stu-id="d37e9-136">The index range will be established between the current position of the cursor and this index entry so that all matches can be found by walking backward on the index using <a href="gg294117(v=exchg.10).md">JetMove</a> with JET_MovePrevious or a negative offset.</span></span></p>
<p><span data-ttu-id="d37e9-137">No es significativo omitir esta opción con una clave de búsqueda que se construyó mediante <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con una opción de carácter comodín diseñada para buscar las entradas de índice más cercanas al final del índice.</span><span class="sxs-lookup"><span data-stu-id="d37e9-137">It is not meaningful to omit this option with a search key that was constructed using <a href="gg269329(v=exchg.10).md">JetMakeKey</a> using a wildcard option intended to find index entries closest to the end of the index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="d37e9-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d37e9-138">Return Value</span></span>

<span data-ttu-id="d37e9-139">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="d37e9-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d37e9-140">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d37e9-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d37e9-141">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d37e9-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="d37e9-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="d37e9-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d37e9-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d37e9-144">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d37e9-144">The operation completed successfully.</span></span></p>
<p><span data-ttu-id="d37e9-145">En el caso de <strong>JetSetIndexRange</strong>, esto significa que se ha cancelado un intervalo de índice existente o que hay al menos una entrada de índice dentro del intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="d37e9-145">For <strong>JetSetIndexRange</strong>, this means that either an existing index range was canceled or that there is at least one index entry inside of the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d37e9-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d37e9-147">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d37e9-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d37e9-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d37e9-149">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="d37e9-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d37e9-150">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d37e9-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-151">JET_errInvalidOperation</span><span class="sxs-lookup"><span data-stu-id="d37e9-151">JET_errInvalidOperation</span></span></p></td>
<td><p><span data-ttu-id="d37e9-152"><strong>JetSetIndexRange</strong> devolverá este error cuando se especificó JET_bitRangeRemove y no hay ningún intervalo de índice en vigor.</span><span class="sxs-lookup"><span data-stu-id="d37e9-152">This error will be returned by <strong>JetSetIndexRange</strong> when JET_bitRangeRemove was specified and no index range was in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-153">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="d37e9-153">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="d37e9-154">No hay ninguna clave de búsqueda actual para el cursor.</span><span class="sxs-lookup"><span data-stu-id="d37e9-154">There is no current search key for the cursor.</span></span> <span data-ttu-id="d37e9-155"><strong>JetSetIndexRange</strong> requiere que el cursor tenga una clave de búsqueda válida porque la usará para los criterios de búsqueda utilizados para buscar entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="d37e9-155"><strong>JetSetIndexRange</strong> requires that the cursor have a valid search key because it will use that for the search criteria used to find index entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-156">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="d37e9-156">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="d37e9-157">No hay ningún índice actual para el cursor.</span><span class="sxs-lookup"><span data-stu-id="d37e9-157">There is no current index for the cursor.</span></span> <span data-ttu-id="d37e9-158">Esto ocurrirá para <strong>JetSetIndexRange</strong> si el cursor está en el índice clúster de una tabla, no se ha definido un índice principal.</span><span class="sxs-lookup"><span data-stu-id="d37e9-158">This will happen for <strong>JetSetIndexRange</strong> if the cursor is on the clustered index of a table, a primary index has not been defined.</span></span> <span data-ttu-id="d37e9-159">No se admite la configuración de un intervalo de índice en este tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="d37e9-159">Setting an index range over such an index is not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-160">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="d37e9-160">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="d37e9-161">Este error lo devolverá <strong>JetSetIndexRange</strong> para indicar que no hay entradas de índice dentro del intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="d37e9-161">This error will be returned by <strong>JetSetIndexRange</strong> to indicate that there are no index entries inside the index range.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-162">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d37e9-162">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d37e9-163">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d37e9-163">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-164">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d37e9-164">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d37e9-165">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d37e9-165">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-166">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d37e9-166">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d37e9-167">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d37e9-167">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d37e9-168">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d37e9-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-169">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d37e9-169">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d37e9-170">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d37e9-170">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d37e9-171">Si se realiza correctamente, si se especifica JET_bitRangeRemove, se cancela el intervalo de índice que está actualmente en vigor.</span><span class="sxs-lookup"><span data-stu-id="d37e9-171">On success, if JET_bitRangeRemove is specified, then the index range that is currently in effect is canceled.</span></span> <span data-ttu-id="d37e9-172">Si no se especifica JET_bitRangeRemove y se especifica JET_bitRangeInstantDuration, no habrá ningún intervalo de índice en vigor.</span><span class="sxs-lookup"><span data-stu-id="d37e9-172">If JET_bitRangeRemove is not specified and JET_bitRangeInstantDuration is specified, then no index range is in effect.</span></span> <span data-ttu-id="d37e9-173">Si no se especifica ni JET_bitRangeRemove ni JET_bitRangeInstantDuration, se aplica un nuevo intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="d37e9-173">If neither JET_bitRangeRemove nor JET_bitRangeInstantDuration is specified, then a new index range is in effect.</span></span> <span data-ttu-id="d37e9-174">Este intervalo de índice limitará temporalmente el conjunto de entradas de índice que el cursor puede recorrer con [JetMove](./jetmove-function.md) a los que empiezan en la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d37e9-174">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="d37e9-175">La posición del cursor permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d37e9-175">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="d37e9-176">Si se ha construido una clave de búsqueda para el cursor, esa clave de búsqueda se eliminará.</span><span class="sxs-lookup"><span data-stu-id="d37e9-176">If a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="d37e9-177">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d37e9-177">No change to the database state will occur.</span></span>

<span data-ttu-id="d37e9-178">En caso de error, si no se devuelve JET_errNoCurrentRecord, no habrá ningún intervalo de índice en vigor.</span><span class="sxs-lookup"><span data-stu-id="d37e9-178">On failure, if JET_errNoCurrentRecord is not returned, then no index range is in effect.</span></span> <span data-ttu-id="d37e9-179">Si se devuelve JET_errNoCurrentRecord, se aplica un nuevo intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="d37e9-179">If JET_errNoCurrentRecord is returned, then a new index range is in effect.</span></span> <span data-ttu-id="d37e9-180">Este intervalo de índice limitará temporalmente el conjunto de entradas de índice que el cursor puede recorrer con [JetMove](./jetmove-function.md) a los que empiezan en la entrada de índice actual y terminan en la entrada de índice que coincide con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="d37e9-180">This index range will temporarily limit the set of index entries that the cursor can walk using [JetMove](./jetmove-function.md) to those starting from the current index entry and ending at the index entry that matches the search criteria.</span></span> <span data-ttu-id="d37e9-181">La posición del cursor permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="d37e9-181">The position of the cursor will remain unchanged.</span></span> <span data-ttu-id="d37e9-182">Si se devolvió JET_errNoCurrentRecord y se ha creado una clave de búsqueda para el cursor, esa clave de búsqueda se eliminará.</span><span class="sxs-lookup"><span data-stu-id="d37e9-182">If JET_errNoCurrentRecord was returned and a search key has been constructed for the cursor, then that search key will be deleted.</span></span> <span data-ttu-id="d37e9-183">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d37e9-183">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d37e9-184">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d37e9-184">Remarks</span></span>

<span data-ttu-id="d37e9-185">Un intervalo de índice es volátil y se cancelará automáticamente si se realiza una navegación distinta de [JetMove](./jetmove-function.md) en el cursor.</span><span class="sxs-lookup"><span data-stu-id="d37e9-185">An index range is volatile and will automatically be canceled if any navigation other than [JetMove](./jetmove-function.md) is performed on the cursor.</span></span>

<span data-ttu-id="d37e9-186">Los intervalos de índice solo funcionan en una dirección.</span><span class="sxs-lookup"><span data-stu-id="d37e9-186">Index ranges only work in one direction.</span></span> <span data-ttu-id="d37e9-187">Si se establece un límite superior, solo se impedirá el movimiento hacia delante mediante [JetMove](./jetmove-function.md) con JET_MoveNext o un desplazamiento positivo una vez alcanzado el final del intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="d37e9-187">If an upper limit is established then only forward motion using [JetMove](./jetmove-function.md) with JET_MoveNext or a positive offset will be prevented once the end of the index range has been reached.</span></span> <span data-ttu-id="d37e9-188">Todavía es posible dejar el intervalo de índice en este caso usando [JetMove](./jetmove-function.md) con JET_MovePrevious o un desplazamiento negativo.</span><span class="sxs-lookup"><span data-stu-id="d37e9-188">It is still possible to leave the index range in this case using [JetMove](./jetmove-function.md) with JET_MovePrevious or a negative offset.</span></span> <span data-ttu-id="d37e9-189">Una situación análoga se produce para un límite inferior.</span><span class="sxs-lookup"><span data-stu-id="d37e9-189">An analogous situation occurs for a lower limit.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d37e9-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d37e9-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-191"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d37e9-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d37e9-192">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d37e9-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-193"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d37e9-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d37e9-194">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d37e9-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-195"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d37e9-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d37e9-196">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="d37e9-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d37e9-197"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="d37e9-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d37e9-198">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d37e9-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d37e9-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d37e9-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d37e9-200">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d37e9-200">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d37e9-201">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d37e9-201">See Also</span></span>

[<span data-ttu-id="d37e9-202">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d37e9-202">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d37e9-203">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d37e9-203">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d37e9-204">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d37e9-204">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d37e9-205">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d37e9-205">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d37e9-206">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="d37e9-206">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="d37e9-207">JetMove</span><span class="sxs-lookup"><span data-stu-id="d37e9-207">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="d37e9-208">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="d37e9-208">JetSetIndexRange</span></span>]()  
[<span data-ttu-id="d37e9-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="d37e9-209">JetStopService</span></span>](./jetstopservice-function.md)
