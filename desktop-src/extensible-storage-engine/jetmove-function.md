---
description: 'Más información acerca de: JetMove (función)'
title: Función JetMove
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e42cb2258d373f8c4edb96309c6db0853eab4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275189"
---
# <a name="jetmove-function"></a><span data-ttu-id="77d41-103">Función JetMove</span><span class="sxs-lookup"><span data-stu-id="77d41-103">JetMove Function</span></span>


<span data-ttu-id="77d41-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77d41-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetmove-function"></a><span data-ttu-id="77d41-105">Función JetMove</span><span class="sxs-lookup"><span data-stu-id="77d41-105">JetMove Function</span></span>

<span data-ttu-id="77d41-106">La función **JetMove** coloca un cursor al principio o al final de un índice y recorre las entradas de ese índice hacia delante o hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="77d41-106">The **JetMove** function positions a cursor at the start or end of an index and traverses the entries in that index either forward or backward.</span></span> <span data-ttu-id="77d41-107">También es posible desplazar el cursor hacia delante o hacia atrás en el índice actual en un número especificado de entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-107">It is also possible to move the cursor forward or backward on the current index by a specified number of index entries.</span></span> <span data-ttu-id="77d41-108">Otro enfoque es limitar artificialmente las entradas de índice que se pueden enumerar mediante **JetMove** mediante la configuración de un intervalo de índice en el cursor mediante [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="77d41-108">Another approach is to artificially limit the index entries that can be enumerated using **JetMove** by setting up an index range on the cursor using [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="77d41-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77d41-109">Parameters</span></span>

<span data-ttu-id="77d41-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="77d41-110">*sesid*</span></span>

<span data-ttu-id="77d41-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="77d41-111">The session to use for this call.</span></span>

<span data-ttu-id="77d41-112">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="77d41-112">*tableid*</span></span>

<span data-ttu-id="77d41-113">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="77d41-113">The cursor to use for this call.</span></span>

<span data-ttu-id="77d41-114">*Gallo*</span><span class="sxs-lookup"><span data-stu-id="77d41-114">*cRow*</span></span>

<span data-ttu-id="77d41-115">Desplazamiento arbitrario que indica el movimiento deseado del cursor en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="77d41-115">An arbitrary offset that indicates the desired movement of the cursor on the current index.</span></span>

<span data-ttu-id="77d41-116">Además de los desplazamientos estándar, este parámetro también se puede establecer con una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="77d41-116">In addition to standard offsets, this parameter can also be set with one of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77d41-117">Value</span><span class="sxs-lookup"><span data-stu-id="77d41-117">Value</span></span></p></th>
<th><p><span data-ttu-id="77d41-118">Significado</span><span class="sxs-lookup"><span data-stu-id="77d41-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77d41-119">JET_MoveFirst</span><span class="sxs-lookup"><span data-stu-id="77d41-119">JET_MoveFirst</span></span></p></td>
<td><p><span data-ttu-id="77d41-120">Mueve el cursor a la primera entrada del índice en el índice (si existe).</span><span class="sxs-lookup"><span data-stu-id="77d41-120">Moves the cursor to the first index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="77d41-121"><strong>Nota:</strong>   El valor literal de-2147483648 se utiliza para denotar esta opción.</span><span class="sxs-lookup"><span data-stu-id="77d41-121"><strong>Note</strong>   The literal value of -2147483648 is used to denote this option.</span></span> <span data-ttu-id="77d41-122">No utilice este valor como un desplazamiento normal o se puede producir un comportamiento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="77d41-122">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d41-123">JET_MoveLast</span><span class="sxs-lookup"><span data-stu-id="77d41-123">JET_MoveLast</span></span></p></td>
<td><p><span data-ttu-id="77d41-124">Mueve el cursor a la última entrada del índice en el índice (si existe).</span><span class="sxs-lookup"><span data-stu-id="77d41-124">Moves the cursor to the last index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="77d41-125"><strong>Nota:</strong>   El valor literal de 2147483647 se utiliza para denotar esta opción.</span><span class="sxs-lookup"><span data-stu-id="77d41-125"><strong>Note</strong>   The literal value of 2147483647 is used to denote this option.</span></span> <span data-ttu-id="77d41-126">No utilice este valor como un desplazamiento normal o se puede producir un comportamiento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="77d41-126">Do not use this value as an ordinary offset or unintended behavior may result.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d41-127">JET_MoveNext</span><span class="sxs-lookup"><span data-stu-id="77d41-127">JET_MoveNext</span></span></p></td>
<td><p><span data-ttu-id="77d41-128">Mueve el cursor a la entrada de índice siguiente en el índice (si existe).</span><span class="sxs-lookup"><span data-stu-id="77d41-128">Moves the cursor to the next index entry in the index (if one exists).</span></span> <span data-ttu-id="77d41-129">Este valor es exactamente igual a un desplazamiento normal de + 1.</span><span class="sxs-lookup"><span data-stu-id="77d41-129">This value is exactly equal to an ordinary offset of +1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d41-130">JET_MovePrevious</span><span class="sxs-lookup"><span data-stu-id="77d41-130">JET_MovePrevious</span></span></p></td>
<td><p><span data-ttu-id="77d41-131">Mueve el cursor a la entrada de índice anterior en el índice (si existe).</span><span class="sxs-lookup"><span data-stu-id="77d41-131">Moves the cursor to the previous index entry in the index (if one exists).</span></span></p>
<p><span data-ttu-id="77d41-132">Este valor es exactamente igual a un desplazamiento normal de-1, o 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="77d41-132">This value is exactly equal to an ordinary offset of -1, or 0 (Zero).</span></span></p>
<p><span data-ttu-id="77d41-133">El cursor permanece en la posición lógica actual y se probará la existencia de la entrada de índice correspondiente a esa posición lógica.</span><span class="sxs-lookup"><span data-stu-id="77d41-133">The cursor remains at the current logical position and the existence of the index entry that corresponds to that logical position will be tested.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77d41-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="77d41-134">*grbit*</span></span>

<span data-ttu-id="77d41-135">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="77d41-135">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77d41-136">Value</span><span class="sxs-lookup"><span data-stu-id="77d41-136">Value</span></span></p></th>
<th><p><span data-ttu-id="77d41-137">Significado</span><span class="sxs-lookup"><span data-stu-id="77d41-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77d41-138">JET_bitMoveKeyNE</span><span class="sxs-lookup"><span data-stu-id="77d41-138">JET_bitMoveKeyNE</span></span></p></td>
<td><p><span data-ttu-id="77d41-139">Mueve el cursor hacia delante o hacia atrás por el número de entradas de índice necesarias para omitir el número solicitado de valores de clave de índice encontrados en el índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-139">Moves the cursor forward or backward by the number of index entries required to skip the requested number of index key values encountered in the index.</span></span> <span data-ttu-id="77d41-140">Esto tiene el efecto de contraer las entradas de índice con valores de clave duplicados en una sola entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-140">This has the effect of collapsing index entries with duplicate key values into a single index entry.</span></span> <span data-ttu-id="77d41-141">Normalmente, un desplazamiento moverá el cursor por el número especificado de entradas de índice, independientemente de sus valores de clave.</span><span class="sxs-lookup"><span data-stu-id="77d41-141">Ordinarily, an offset will move the cursor by the specified number of index entries regardless of their key values.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="77d41-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77d41-142">Return Value</span></span>

<span data-ttu-id="77d41-143">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="77d41-143">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="77d41-144">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="77d41-144">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77d41-145">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="77d41-145">Return code</span></span></p></th>
<th><p><span data-ttu-id="77d41-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="77d41-146">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77d41-147">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="77d41-147">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="77d41-148">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="77d41-148">The operation completed successfully.</span></span> <span data-ttu-id="77d41-149">En el caso de <strong>JetMove</strong>, esto significa que se encontró una entrada de índice en la ubicación o el desplazamiento solicitado en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="77d41-149">For <strong>JetMove</strong>, this means that an index entry was found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d41-150">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="77d41-150">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="77d41-151">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="77d41-151">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d41-152">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="77d41-152">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="77d41-153">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="77d41-153">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="77d41-154"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77d41-154"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d41-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="77d41-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="77d41-156">El cursor no está actualmente situado en una entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-156">The cursor is not currently positioned on an index entry.</span></span> <span data-ttu-id="77d41-157">En el caso de <strong>JetMove</strong>, esto significa que no se encontró una entrada de índice en la ubicación o el desplazamiento solicitado en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="77d41-157">For <strong>JetMove</strong>, this means that an index entry was not found at the requested location or offset on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d41-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="77d41-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="77d41-159">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="77d41-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d41-160">JET_errRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="77d41-160">JET_errRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="77d41-161">El cursor está actualmente colocado lógicamente en una entrada de índice que corresponde a un registro que se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="77d41-161">The cursor is currently logically positioned on an index entry that corresponds to a record that has been deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d41-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="77d41-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="77d41-163">No se puede completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="77d41-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d41-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="77d41-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="77d41-165">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="77d41-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="77d41-166"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77d41-166"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d41-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="77d41-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="77d41-168">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="77d41-168">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77d41-169">Si esta función se ejecuta correctamente, el cursor se colocará en una entrada de índice que coincida con la ubicación o el desplazamiento solicitados.</span><span class="sxs-lookup"><span data-stu-id="77d41-169">If this function succeeds, the cursor will be positioned at an index entry that matches the requested location or offset.</span></span> <span data-ttu-id="77d41-170">Si se ha preparado un registro para la actualización, la actualización se cancelará.</span><span class="sxs-lookup"><span data-stu-id="77d41-170">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="77d41-171">Si hay un intervalo de índice en vigor y se ha especificado JET_MoveFirst o JET_MoveLast, se cancelará dicho intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="77d41-171">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="77d41-172">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="77d41-172">No change to the database state will occur.</span></span>

<span data-ttu-id="77d41-173">Si se produce un error en esta función, la posición del cursor permanecerá sin cambios a menos que se devuelva JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="77d41-173">If this function fails, the position of the cursor will remain unchanged unless JET_errNoCurrentRecord was returned.</span></span> <span data-ttu-id="77d41-174">En ese caso, el cursor se colocará donde habría sido la entrada de índice que coincide con la ubicación o el desplazamiento solicitado.</span><span class="sxs-lookup"><span data-stu-id="77d41-174">In that case, the cursor will be positioned where the index entry that matches the requested location or offset would have been.</span></span> <span data-ttu-id="77d41-175">El cursor se puede mover en relación con esa posición, pero aún no se encuentra en una entrada de índice válida.</span><span class="sxs-lookup"><span data-stu-id="77d41-175">The cursor can be moved relative to that position but is still not on a valid index entry.</span></span> <span data-ttu-id="77d41-176">Si se ha preparado un registro para la actualización, la actualización se cancelará.</span><span class="sxs-lookup"><span data-stu-id="77d41-176">If a record has been prepared for update, that update will be canceled.</span></span> <span data-ttu-id="77d41-177">Si hay un intervalo de índice en vigor y se ha especificado JET_MoveFirst o JET_MoveLast, se cancelará dicho intervalo de índices.</span><span class="sxs-lookup"><span data-stu-id="77d41-177">If an index range is in effect and JET_MoveFirst or JET_MoveLast was specified, that index range will be canceled.</span></span> <span data-ttu-id="77d41-178">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="77d41-178">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="77d41-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77d41-179">Remarks</span></span>

<span data-ttu-id="77d41-180">Un cursor puede moverse a dos posiciones especiales mediante **JetMove**, antes y después de la última.</span><span class="sxs-lookup"><span data-stu-id="77d41-180">A cursor can be moved to two special positions using **JetMove**, Before First and After Last.</span></span> <span data-ttu-id="77d41-181">Si el cursor está en la primera entrada de índice de la tabla y se llama a **JetMove** con JET_MovePrevious, se producirá un error en la llamada con JET_errNoCurrentRecord y el cursor se colocará lógicamente antes de la primera entrada del índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-181">If the cursor is on the first index entry in the table and **JetMove** is called with JET_MovePrevious, the call will fail with JET_errNoCurrentRecord and the cursor will be logically positioned before the first entry in the index.</span></span> <span data-ttu-id="77d41-182">Esta posición lógica se mantiene aunque se inserte otra entrada de índice antes de la primera entrada en el índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-182">This logical position is maintained even if another index entry is inserted prior to the first entry in the index.</span></span> <span data-ttu-id="77d41-183">Una situación análoga se produce después de la última relativa al final del índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-183">An analogous situation occurs for After Last relative to the end of the index.</span></span> <span data-ttu-id="77d41-184">Antes de que la primera y la última vez sean más útiles al configurar un intervalo de entradas de índice que se van a recorrer en iteración con **JetMove**, con un modelo de iterador que espera que siempre se mueva al siguiente elemento (o anterior) antes de usar ese elemento.</span><span class="sxs-lookup"><span data-stu-id="77d41-184">Before First and After Last are most useful when setting up a range of index entries to be iterated using **JetMove**, using an iterator model that expects to always move to the next (or previous) element prior to using that element.</span></span>

<span data-ttu-id="77d41-185">El conjunto de entradas de índice que **JetMove** puede visitar puede verse limitado mediante la configuración de un intervalo de índice en el cursor.</span><span class="sxs-lookup"><span data-stu-id="77d41-185">The set of index entries that can be visited by **JetMove** can be limited by setting up an index range on the cursor.</span></span> <span data-ttu-id="77d41-186">Esto resulta útil para las aplicaciones que enumeran un conjunto de entradas de índice que coinciden con criterios simples que se pueden expresar a través de un par de claves de búsqueda compiladas para ese índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-186">This is useful for applications that enumerate a set of index entries that match simple criteria that can be expressed through a pair of search keys built for that index.</span></span> <span data-ttu-id="77d41-187">Para obtener más información, vea [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="77d41-187">For more information, see [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="77d41-188">En las versiones anteriores a Windows Server 2003 SP1, hay un problema en **JetMove** que se produce en algunos casos específicos, que afecta a la aplicación correcta de un intervalo de índice configurado por la función [JetSetIndexRange](./jetsetindexrange-function.md) .</span><span class="sxs-lookup"><span data-stu-id="77d41-188">On releases prior to Windows Server 2003 SP1, there is a problem in **JetMove** that occurs in some specific cases, that affects the correct enforcement of an index range as set up by the [JetSetIndexRange](./jetsetindexrange-function.md) function.</span></span> <span data-ttu-id="77d41-189">Si el cursor se encuentra actualmente antes de la primera entrada de índice y se establece un intervalo de índice con un límite superior que es menor que la primera entrada de índice, la siguiente llamada a **JetMove** irá erróneamente a esa entrada de índice en lugar de a que se produzcan errores con JET_errNoCurrentRecord, según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="77d41-189">If the cursor is currently before the first index entry and an index range is set with an upper limit that is less than the first index entry, the next call to **JetMove** will erroneously go to that index entry instead of failing with JET_errNoCurrentRecord, as expected.</span></span> <span data-ttu-id="77d41-190">Se producirá el mismo error en la situación análoga a partir del final del índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-190">The same error will happen for the analogous situation starting from the end of the index.</span></span> <span data-ttu-id="77d41-191">Esta situación puede producirse en una aplicación que configura un intervalo de índices y navega por él mediante un iterador que espera iniciarse antes de la primera entrada de índice que es miembro del conjunto de entradas que se va a enumerar, en lugar de comenzar en la primera entrada de índice de ese conjunto.</span><span class="sxs-lookup"><span data-stu-id="77d41-191">This situation can occur in an application that sets up an index range and navigates it using an iterator that expects to start before the first index entry that is a member of the set of entries to enumerate, rather than starting on the first index entry of that set.</span></span> <span data-ttu-id="77d41-192">Esta situación también se produce en el caso análogo a partir del final del índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-192">This situation also occurs on the analogous case starting from the end of the index.</span></span> <span data-ttu-id="77d41-193">La solución alternativa es que la aplicación Compruebe manualmente que la entrada de índice adquirida se encuentra dentro del intervalo de índices comparando la clave de la entrada de índice actual (recuperada mediante [JetRetrieveKey](./jetretrievekey-function.md)) con la clave que representa el final del intervalo de índice actual (recuperada mediante [JetRetrieveKey](./jetretrievekey-function.md) con JET_bitRetrieveCopy).</span><span class="sxs-lookup"><span data-stu-id="77d41-193">The workaround is for the application to manually verify that the index entry acquired is inside the index range by comparing the key for the current index entry (retrieved using [JetRetrieveKey](./jetretrievekey-function.md)) with the key representing the end of the current index range (retrieved using [JetRetrieveKey](./jetretrievekey-function.md) using JET_bitRetrieveCopy).</span></span>

<span data-ttu-id="77d41-194">Es importante tener cuidado al pasar desplazamientos calculados a **JetMove**.</span><span class="sxs-lookup"><span data-stu-id="77d41-194">It is important to be careful when passing computed offsets to **JetMove**.</span></span> <span data-ttu-id="77d41-195">Si el desplazamiento calculado es menor o igual que JET_MoveFirst, dicho desplazamiento se debe dividir en varias partes, cada una de las cuales se pasa a **JetMove** por separado, pero dentro de una única transacción para obtener el efecto deseado.</span><span class="sxs-lookup"><span data-stu-id="77d41-195">If the computed offset is less than or equal to JET_MoveFirst, that offset must be broken up into multiple pieces, each of which is passed to **JetMove** separately but within a single transaction to get the desired effect.</span></span> <span data-ttu-id="77d41-196">Lo mismo se aplica a los desplazamientos mayores o iguales que JET_MoveNext.</span><span class="sxs-lookup"><span data-stu-id="77d41-196">The same is true for offsets greater than or equal to JET_MoveNext.</span></span> <span data-ttu-id="77d41-197">No es probable que una aplicación se someta a esto en el mundo real, pero es conveniente tener una defensa en este caso dada la semántica muy diferente de JET_MoveFirst y JET_MoveLast a partir de un desplazamiento normal.</span><span class="sxs-lookup"><span data-stu-id="77d41-197">It is unlikely that an application would undergo this in the real world, but it is good to have a defense against this case given the very different semantics of JET_MoveFirst and JET_MoveLast from an ordinary offset.</span></span>

<span data-ttu-id="77d41-198">Cuando se llama a **JetMove** con un desplazamiento muy grande, como cuando el parámetro cRow está establecido en 1000, **JetMove** recorre todas las entradas de índice de 1000 para llegar a la posición final.</span><span class="sxs-lookup"><span data-stu-id="77d41-198">When **JetMove** is called with a very large offset, such as when the cRow parameter is set to 1000, **JetMove** traverses all 1000 index entries to reach the final position.</span></span> <span data-ttu-id="77d41-199">Actualmente, la API de ESE no proporciona una manera eficaz de desplazarse directamente a una entrada de índice determinada por el desplazamiento sin atravesar cada entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="77d41-199">Currently, the ESE API does not provide an efficient way to move directly to a given index entry by offset without traversing each index entry.</span></span>

#### <a name="requirements"></a><span data-ttu-id="77d41-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77d41-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77d41-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="77d41-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77d41-202">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="77d41-202">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d41-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="77d41-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77d41-204">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="77d41-204">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d41-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="77d41-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77d41-206">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="77d41-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77d41-207"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="77d41-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="77d41-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="77d41-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77d41-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="77d41-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="77d41-210">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="77d41-210">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="77d41-211">Consulte también</span><span class="sxs-lookup"><span data-stu-id="77d41-211">See Also</span></span>

[<span data-ttu-id="77d41-212">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="77d41-212">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="77d41-213">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="77d41-213">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="77d41-214">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="77d41-214">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="77d41-215">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="77d41-215">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="77d41-216">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="77d41-216">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
[<span data-ttu-id="77d41-217">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="77d41-217">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
