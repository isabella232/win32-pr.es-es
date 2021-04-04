---
description: 'Más información acerca de: JetRetrieveKey (función)'
title: Función JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083333"
---
# <a name="jetretrievekey-function"></a><span data-ttu-id="7e9b6-103">Función JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="7e9b6-103">JetRetrieveKey Function</span></span>


<span data-ttu-id="7e9b6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7e9b6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetretrievekey-function"></a><span data-ttu-id="7e9b6-105">Función JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="7e9b6-105">JetRetrieveKey Function</span></span>

<span data-ttu-id="7e9b6-106">La función **JetRetrieveKey** recupera la clave de la entrada de índice en la posición actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-106">The **JetRetrieveKey** function retrieves the key for the index entry at the current position of a cursor.</span></span> <span data-ttu-id="7e9b6-107">Estas claves se crean mediante llamadas a [JetMakeKey](./jetmakekey-function.md).</span><span class="sxs-lookup"><span data-stu-id="7e9b6-107">Such keys are constructed by calls to [JetMakeKey](./jetmakekey-function.md).</span></span> <span data-ttu-id="7e9b6-108">La clave recuperada se puede usar para devolver eficazmente ese cursor a la misma entrada de índice mediante una llamada a [JetSeek](./jetseek-function.md).</span><span class="sxs-lookup"><span data-stu-id="7e9b6-108">The retrieved key can then be used to efficiently return that cursor to the same index entry by a call to [JetSeek](./jetseek-function.md).</span></span>

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="7e9b6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e9b6-109">Parameters</span></span>

<span data-ttu-id="7e9b6-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="7e9b6-110">*sesid*</span></span>

<span data-ttu-id="7e9b6-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-111">The session to use for this call.</span></span>

<span data-ttu-id="7e9b6-112">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="7e9b6-112">*tableid*</span></span>

<span data-ttu-id="7e9b6-113">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-113">The cursor to use for this call.</span></span>

<span data-ttu-id="7e9b6-114">*pvData*</span><span class="sxs-lookup"><span data-stu-id="7e9b6-114">*pvData*</span></span>

<span data-ttu-id="7e9b6-115">Búfer de salida que recibirá la clave.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-115">The output buffer that will receive the key.</span></span>

<span data-ttu-id="7e9b6-116">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="7e9b6-116">*cbMax*</span></span>

<span data-ttu-id="7e9b6-117">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-117">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="7e9b6-118">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="7e9b6-118">*pcbActual*</span></span>

<span data-ttu-id="7e9b6-119">Recibe el tamaño real en bytes de la clave.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-119">Receives the actual size in bytes of the key.</span></span>

<span data-ttu-id="7e9b6-120">Si este parámetro es NULL, no se devolverá el tamaño real de la clave.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-120">If this parameter is NULL then the actual size of the key will not be returned.</span></span>

<span data-ttu-id="7e9b6-121">Si el búfer de salida es demasiado pequeño, se seguirá devolviendo el tamaño real de la clave.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-121">If the output buffer is too small, then the actual size of the key will still be returned.</span></span> <span data-ttu-id="7e9b6-122">Esto significa que este número será mayor que el tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-122">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="7e9b6-123">*grbit*</span><span class="sxs-lookup"><span data-stu-id="7e9b6-123">*grbit*</span></span>

<span data-ttu-id="7e9b6-124">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-124">A group of bits that contain the options to be used for this call, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e9b6-125">Value</span><span class="sxs-lookup"><span data-stu-id="7e9b6-125">Value</span></span></p></th>
<th><p><span data-ttu-id="7e9b6-126">Significado</span><span class="sxs-lookup"><span data-stu-id="7e9b6-126">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-127">JET_bitRetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="7e9b6-127">JET_bitRetrieveCopy</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-128">Cuando se especifica, el motor devolverá la clave de búsqueda para el cursor.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-128">When specified, the engine will return the search key for the cursor.</span></span> <span data-ttu-id="7e9b6-129">La clave de búsqueda se basa en una o varias llamadas anteriores a <a href="gg269329(v=exchg.10).md">JetMakeKey</a> con el fin de buscar esa clave con <a href="gg294103(v=exchg.10).md">JetSeek</a> o establecer un intervalo de índice mediante <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-129">The search key is built up using one or more prior calls to <a href="gg269329(v=exchg.10).md">JetMakeKey</a> for the purposes of seeking to that key using <a href="gg294103(v=exchg.10).md">JetSeek</a> or setting an index range using <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="7e9b6-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e9b6-130">Return Value</span></span>

<span data-ttu-id="7e9b6-131">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="7e9b6-132">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7e9b6-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e9b6-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7e9b6-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="7e9b6-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e9b6-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="7e9b6-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-136">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9b6-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="7e9b6-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-138">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="7e9b6-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-140">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="7e9b6-141">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9b6-142">JET_errKeyNotMade</span><span class="sxs-lookup"><span data-stu-id="7e9b6-142">JET_errKeyNotMade</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-143">No hay ninguna clave de búsqueda actual para el cursor.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-143">There is no current search key for the cursor.</span></span> <span data-ttu-id="7e9b6-144">Esto ocurrirá para <strong>JetRetrieveKey</strong> si se especifica JET_bitRetrieveCopy y no se ha construido una clave de búsqueda para este cursor mediante una llamada anterior a <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-144">This will happen for <strong>JetRetrieveKey</strong> if JET_bitRetrieveCopy is specified and a search key has not been constructed for this cursor using a prior call to <a href="gg269329(v=exchg.10).md">JetMakeKey</a>.</span></span> <span data-ttu-id="7e9b6-145">La clave de búsqueda se eliminará mediante una llamada anterior a cualquier API de navegación en el cursor que no sea <a href="gg294117(v=exchg.10).md">JetMove</a>.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-145">The search key will be deleted by a prior call to any navigational API on the cursor other than <a href="gg294117(v=exchg.10).md">JetMove</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-146">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="7e9b6-146">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-147">El cursor no está situado en un registro.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-147">The cursor is not positioned on a record.</span></span> <span data-ttu-id="7e9b6-148">Esto puede ocurrir por diversos motivos.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-148">This can happen for many different reasons.</span></span> <span data-ttu-id="7e9b6-149">Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-149">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9b6-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="7e9b6-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-151">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="7e9b6-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-153">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9b6-154">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="7e9b6-154">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-155">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-155">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="7e9b6-156">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-156">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-157">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="7e9b6-157">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-158">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-158">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9b6-159">JET_wrnBufferTruncated</span><span class="sxs-lookup"><span data-stu-id="7e9b6-159">JET_wrnBufferTruncated</span></span></p></td>
<td><p><span data-ttu-id="7e9b6-160">La operación se completó correctamente, pero el búfer de salida era demasiado pequeño para recibir toda la clave.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-160">The operation completed successfully, but the output buffer was too small to receive the entire key.</span></span> <span data-ttu-id="7e9b6-161">El búfer de salida se ha rellenado con la gran parte de la clave que cabría.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-161">The output buffer has been filled with as much of the key as would fit.</span></span> <span data-ttu-id="7e9b6-162">También se ha devuelto el tamaño real de la clave, si se solicita.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-162">The actual size of the key has also been returned, if requested.</span></span></p>
<p><span data-ttu-id="7e9b6-163"><strong>Nota:</strong>   Este error no se devolverá si se especifica JET_bitRetrieveCopy.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-163"><strong>Note</strong>   This error will not be returned if JET_bitRetrieveCopy is specified.</span></span> <span data-ttu-id="7e9b6-164">Vea la sección Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-164">Please see the Remarks section for more information.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7e9b6-165">Si se ejecuta correctamente, la clave de la entrada de índice en la posición actual de un cursor se devolverá en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-165">On success, the key for the index entry at the current position of a cursor will be returned in the output buffer.</span></span> <span data-ttu-id="7e9b6-166">Si se devuelve JET_wrnBufferTruncated, el búfer de salida contendrá la mayor parte de la clave que quepa en el espacio proporcionado y el tamaño real de la clave será preciso.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-166">If JET_wrnBufferTruncated is returned then the output buffer will contain as much of the key as will fit in the space provided and the actual size of the key will be accurate.</span></span> <span data-ttu-id="7e9b6-167">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-167">No change to the database state will occur.</span></span>

<span data-ttu-id="7e9b6-168">En caso de error, el estado del búfer de salida y el tamaño real de la clave serán indefinidos.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-168">On failure, the state of the output buffer and the actual size of the key will be undefined.</span></span> <span data-ttu-id="7e9b6-169">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-169">No change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="7e9b6-170">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e9b6-170">Remarks</span></span>

<span data-ttu-id="7e9b6-171">Por lo general, las claves se deben tratar como fragmentos opacos de datos.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-171">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="7e9b6-172">No se realiza ningún intento de aprovechar la estructura interna de estos datos.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-172">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="7e9b6-173">Sin embargo, se pueden conocer las siguientes propiedades de todas las claves de ESENT:</span><span class="sxs-lookup"><span data-stu-id="7e9b6-173">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="7e9b6-174">Las claves se pueden comparar entre sí mediante la función [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) para establecer su orden relativo en el índice de origen en la tabla de las entradas de índice de origen.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-174">Keys may be compared against each other using [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) function to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="7e9b6-175">No tiene sentido comparar las claves de las entradas de índice de distintos índices entre sí.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-175">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="7e9b6-176">Una clave siempre es menor o igual que JET_cbKeyMost (255) bytes de longitud antes de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-176">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="7e9b6-177">En Windows Vista y versiones posteriores, las claves pueden ser más grandes.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-177">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="7e9b6-178">El tamaño máximo de una clave es igual al valor actual de JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-178">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

<span data-ttu-id="7e9b6-179">Además de las propiedades anteriores de las claves ESENT en general, es importante tener en cuenta que una clave de búsqueda es diferente de la clave para una entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-179">In addition to the above properties of ESENT keys in general, it is important to note that a search key is different from the key for an index entry.</span></span> <span data-ttu-id="7e9b6-180">En concreto, una clave de búsqueda puede ser más larga que una clave normal.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-180">Specifically, a search key may be longer than an ordinary key.</span></span> <span data-ttu-id="7e9b6-181">Esta longitud adicional se produce cuando se utiliza una opción de carácter comodín al construir la clave de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-181">This extra length occurs when a wildcard option is used while constructing the search key.</span></span> <span data-ttu-id="7e9b6-182">Vea [JetMakeKey](./jetmakekey-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-182">See [JetMakeKey](./jetmakekey-function.md) for more information.</span></span>

<span data-ttu-id="7e9b6-183">Hay un error importante en esta API que está presente en todas las versiones.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-183">There is an important bug in this API that is present in all releases.</span></span> <span data-ttu-id="7e9b6-184">Si la clave de búsqueda se solicita mediante el uso de JET_bitRetrieveCopy y el búfer de salida es demasiado pequeño para recibir toda la clave, no se devolverá JET_wrnBufferTruncated.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-184">If the search key is requested using the use of JET_bitRetrieveCopy and the output buffer is too small to receive the entire key then JET_wrnBufferTruncated will NOT be returned.</span></span> <span data-ttu-id="7e9b6-185">Se devolverá JET_errSuccess en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-185">JET_errSuccess will be returned instead.</span></span> <span data-ttu-id="7e9b6-186">Es importante comprobar que el tamaño real de la clave tal y como se devuelve mediante *pcbActual* es menor o igual que el tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-186">It is important to verify that the actual size of the key as returned using *pcbActual* is less than or equal to the size of the output buffer.</span></span> <span data-ttu-id="7e9b6-187">Si el tamaño real es mayor que el tamaño del búfer de salida, el llamador de **JetRetrieveKey** debe reaccionar como si se devolvieran JET_wrnBufferTruncated en su lugar.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-187">If the actual size is larger than the size of the output buffer, then the caller of **JetRetrieveKey** should react as if JET_wrnBufferTruncated were returned instead.</span></span>

#### <a name="requirements"></a><span data-ttu-id="7e9b6-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e9b6-188">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-189"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7e9b6-189"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7e9b6-190">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-190">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9b6-191"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7e9b6-191"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7e9b6-192">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-192">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-193"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7e9b6-193"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7e9b6-194">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-194">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e9b6-195"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="7e9b6-195"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="7e9b6-196">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-196">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e9b6-197"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="7e9b6-197"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="7e9b6-198">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="7e9b6-198">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="7e9b6-199">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e9b6-199">See Also</span></span>

[<span data-ttu-id="7e9b6-200">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="7e9b6-200">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="7e9b6-201">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7e9b6-201">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7e9b6-202">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="7e9b6-202">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="7e9b6-203">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7e9b6-203">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7e9b6-204">JetMakeKey</span><span class="sxs-lookup"><span data-stu-id="7e9b6-204">JetMakeKey</span></span>](./jetmakekey-function.md)  
[<span data-ttu-id="7e9b6-205">JetSeek</span><span class="sxs-lookup"><span data-stu-id="7e9b6-205">JetSeek</span></span>](./jetseek-function.md)  
[<span data-ttu-id="7e9b6-206">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="7e9b6-206">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
