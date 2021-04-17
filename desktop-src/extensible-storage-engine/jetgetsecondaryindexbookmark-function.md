---
description: 'Más información acerca de: JetGetSecondaryIndexBookmark (función)'
title: JetGetSecondaryIndexBookmark función)
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d86b875037982a18ebb9d488c3a05b3123002b06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716163"
---
# <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="c8d1e-103">JetGetSecondaryIndexBookmark función)</span><span class="sxs-lookup"><span data-stu-id="c8d1e-103">JetGetSecondaryIndexBookmark Function</span></span>


<span data-ttu-id="c8d1e-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c8d1e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetsecondaryindexbookmark-function"></a><span data-ttu-id="c8d1e-105">JetGetSecondaryIndexBookmark función)</span><span class="sxs-lookup"><span data-stu-id="c8d1e-105">JetGetSecondaryIndexBookmark Function</span></span>

<span data-ttu-id="c8d1e-106">La función **JetGetSecondaryIndexBookmark** recupera un marcador especial para la entrada de índice secundario en la posición actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-106">The **JetGetSecondaryIndexBookmark** function retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="c8d1e-107">Este marcador se puede usar para volver a colocar eficazmente ese cursor en la misma entrada de índice mediante [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span><span class="sxs-lookup"><span data-stu-id="c8d1e-107">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md).</span></span> <span data-ttu-id="c8d1e-108">Esto es muy útil cuando se cambia la posición en un índice secundario que contiene claves duplicadas o que contiene varias entradas de índice para el mismo registro.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-108">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="c8d1e-109">**Windows XP: JetGetSecondaryIndexBookmark** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-109">**Windows XP:  JetGetSecondaryIndexBookmark** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c8d1e-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8d1e-110">Parameters</span></span>

<span data-ttu-id="c8d1e-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-111">*sesid*</span></span>

<span data-ttu-id="c8d1e-112">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-112">The session to use for this call.</span></span>

<span data-ttu-id="c8d1e-113">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-113">*tableid*</span></span>

<span data-ttu-id="c8d1e-114">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-114">The cursor to use for this call.</span></span>

<span data-ttu-id="c8d1e-115">*pvSecondaryKey*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-115">*pvSecondaryKey*</span></span>

<span data-ttu-id="c8d1e-116">Búfer de salida que recibe la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-116">The output buffer that receives the secondary key.</span></span>

<span data-ttu-id="c8d1e-117">*cbSecondaryKeyMax*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-117">*cbSecondaryKeyMax*</span></span>

<span data-ttu-id="c8d1e-118">Tamaño máximo, en bytes, del búfer de salida de la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-118">The maximum size, in bytes, of the output buffer for the secondary key.</span></span>

<span data-ttu-id="c8d1e-119">*pcbSecondaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-119">*pcbSecondaryKeyActual*</span></span>

<span data-ttu-id="c8d1e-120">Recibe el tamaño real en bytes de la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-120">Receives the actual size in bytes of the secondary key.</span></span>

<span data-ttu-id="c8d1e-121">Si este parámetro es NULL, no se devolverá el tamaño real de la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-121">If this parameter is NULL, the actual size of the secondary key will not be returned.</span></span>

<span data-ttu-id="c8d1e-122">Si el búfer de salida es demasiado pequeño, se seguirá devolviendo el tamaño real de la clave secundaria.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-122">If the output buffer is too small, the actual size of the secondary key will still be returned.</span></span> <span data-ttu-id="c8d1e-123">Esto significa que este número será mayor que el tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-123">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="c8d1e-124">*pvPrimaryBookmark*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-124">*pvPrimaryBookmark*</span></span>

<span data-ttu-id="c8d1e-125">Búfer de salida que recibe el marcador de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-125">The output buffer that receives the primary key bookmark.</span></span>

<span data-ttu-id="c8d1e-126">*cbPrimaryBookmarkMax*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-126">*cbPrimaryBookmarkMax*</span></span>

<span data-ttu-id="c8d1e-127">Tamaño máximo, en bytes, del búfer de salida para el marcador de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-127">The maximum size, in bytes, of the output buffer for the primary key bookmark.</span></span>

<span data-ttu-id="c8d1e-128">*pcbPrimaryKeyActual*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-128">*pcbPrimaryKeyActual*</span></span>

<span data-ttu-id="c8d1e-129">Recibe el tamaño real, en bytes, del marcador de la clave principal.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-129">Receives the actual size, in bytes, of the primary key bookmark.</span></span>

<span data-ttu-id="c8d1e-130">Si este parámetro es NULL, no se devolverá el tamaño real del marcador de clave principal.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-130">If this parameter is NULL then the actual size of the primary key bookmark will not be returned.</span></span>

<span data-ttu-id="c8d1e-131">Si el búfer de salida es demasiado pequeño, se seguirá devolviendo el tamaño real del marcador de clave principal.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-131">If the output buffer is too small, the actual size of the primary key bookmark will still be returned.</span></span> <span data-ttu-id="c8d1e-132">Esto significa que este número será mayor que el tamaño del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-132">That means that this number will be larger than the size of the output buffer.</span></span>

<span data-ttu-id="c8d1e-133">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c8d1e-133">*grbit*</span></span>

<span data-ttu-id="c8d1e-134">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-134">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="c8d1e-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8d1e-135">Return Value</span></span>

<span data-ttu-id="c8d1e-136">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c8d1e-137">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c8d1e-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8d1e-138">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c8d1e-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="c8d1e-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="c8d1e-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8d1e-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c8d1e-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-141">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8d1e-142">JET_errBufferTooSmall</span><span class="sxs-lookup"><span data-stu-id="c8d1e-142">JET_errBufferTooSmall</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-143">La operación se completó correctamente, pero uno de los búferes de salida era demasiado pequeño para recibir los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-143">The operation completed successfully, but one of the output buffers was too small to receive the requested data.</span></span></p>
<p><span data-ttu-id="c8d1e-144">El búfer de salida se ha rellenado con tanta parte del marcador como quepa.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-144">The output buffer has been filled with as much of the bookmark as would fit.</span></span> <span data-ttu-id="c8d1e-145">También se ha devuelto el tamaño real del marcador, si se solicita.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-145">The actual size of the bookmark has also been returned, if requested.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8d1e-146">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c8d1e-146">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-147">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-147">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8d1e-148">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c8d1e-148">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-149">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-149">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c8d1e-150">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8d1e-151">JET_errNoCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="c8d1e-151">JET_errNoCurrentIndex</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-152">El cursor no está actualmente en un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-152">The cursor is not currently on a secondary index.</span></span></p>
<p><span data-ttu-id="c8d1e-153">No es significativo recuperar un marcador de índice secundario cuando el cursor no está utilizando actualmente un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-153">It is not meaningful to retrieve a secondary index bookmark when the cursor is not currently using a secondary index.</span></span> <span data-ttu-id="c8d1e-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> debe usarse cuando el cursor no está en un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-154"><a href="gg269221(v=exchg.10).md">JetGetBookmark</a> should be used when the cursor is not on a secondary index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8d1e-155">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="c8d1e-155">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-156">El cursor no está situado en un registro.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-156">The cursor is not positioned on a record.</span></span></p>
<p><span data-ttu-id="c8d1e-157">Esto puede ocurrir por diversos motivos.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-157">This can happen for many different reasons.</span></span> <span data-ttu-id="c8d1e-158">Por ejemplo, esto ocurrirá si el cursor está situado actualmente después del último registro en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-158">For example, this will happen if the cursor is currently positioned after the last record on the current index.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8d1e-159">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c8d1e-159">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-160">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-160">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8d1e-161">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c8d1e-161">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-162">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-162">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8d1e-163">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c8d1e-163">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-164">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-164">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="c8d1e-165">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-165">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8d1e-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c8d1e-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c8d1e-167">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-167">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c8d1e-168">Si se ejecuta correctamente, se devolverá el marcador de índice secundario para la entrada de índice en la posición actual de un cursor en los búferes de salida.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-168">On success, the secondary index bookmark for the index entry at the current position of a cursor will be returned in the output buffers.</span></span> <span data-ttu-id="c8d1e-169">No se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-169">No change to the database state will occur.</span></span>

<span data-ttu-id="c8d1e-170">En caso de error, el estado de los búferes de salida y el tamaño real del marcador de índice secundario será undefined, a menos que se devuelva JET_errBufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-170">On failure, the state of the output buffers and the actual size of the secondary index bookmark will be undefined unless JET_errBufferTooSmall was returned.</span></span> <span data-ttu-id="c8d1e-171">En el caso de que se devuelva JET_errBufferTooSmall, los búferes de salida contendrán tanto del marcador de índice secundario como quepan en el espacio proporcionado y el tamaño real del marcador de índice secundario será preciso.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-171">In the event that JET_errBufferTooSmall is returned, the output buffers will contain as much of the secondary index bookmark as will fit in the space provided and the actual size of the secondary index bookmark will be accurate.</span></span> <span data-ttu-id="c8d1e-172">En cualquier caso, no se producirá ningún cambio en el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-172">In any case, no change to the database state will occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c8d1e-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8d1e-173">Remarks</span></span>

<span data-ttu-id="c8d1e-174">Por lo general, los marcadores se deben tratar como fragmentos opacos de datos.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-174">Bookmarks should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="c8d1e-175">No se realiza ningún intento de aprovechar la estructura interna de estos datos.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-175">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="c8d1e-176">Sin embargo, se pueden conocer las siguientes propiedades de todos los marcadores de ESENT:</span><span class="sxs-lookup"><span data-stu-id="c8d1e-176">However, the following properties can be known about all ESENT bookmarks:</span></span>

  - <span data-ttu-id="c8d1e-177">Un marcador identifica de forma única un registro en una tabla determinada.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-177">A bookmark uniquely identifies a record in a given table.</span></span>

  - <span data-ttu-id="c8d1e-178">El marcador de un registro no cambiará durante el período de duración de dicho registro.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-178">The bookmark of a record will not change for the lifetime of that record.</span></span>

  - <span data-ttu-id="c8d1e-179">El marcador de un registro es igual que la clave de ese registro en el índice principal de la tabla que contiene ese registro.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-179">The bookmark of a record is the same as the key of that record on the primary index over the table containing that record.</span></span> <span data-ttu-id="c8d1e-180">Si no se define ningún índice principal sobre esa tabla, el motor de base de datos creará su propio marcador para el registro.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-180">If no primary index is defined over that table, the database engine will create its own bookmark for the record.</span></span>

  - <span data-ttu-id="c8d1e-181">Los marcadores se pueden comparar entre sí mediante [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su orden relativo en el índice principal sobre la tabla de los registros de origen.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-181">Bookmarks may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the primary index over the table of the source records.</span></span> <span data-ttu-id="c8d1e-182">Si no se define ningún índice principal sobre esa tabla, el orden relativo de los marcadores de esa tabla no es significativo.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-182">If no primary index is defined over that table, the relative ordering of bookmarks from that table is not meaningful.</span></span>

  - <span data-ttu-id="c8d1e-183">No tiene sentido comparar los marcadores de los registros de diferentes tablas entre sí.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-183">It is meaningless to compare bookmarks of records from different tables against each other.</span></span>

  - <span data-ttu-id="c8d1e-184">Un marcador siempre es menor o igual que JET_cbBookmarkMost (256) bytes de longitud anterior a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-184">A bookmark is always less than or equal to JET_cbBookmarkMost (256) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="c8d1e-185">En Windows Vista y versiones posteriores, los marcadores pueden ser más grandes.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-185">On Windows Vista and later releases, bookmarks can be larger.</span></span> <span data-ttu-id="c8d1e-186">El tamaño máximo de un marcador es igual al valor actual de JET_paramKeyMost + 1.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-186">The maximum size of a bookmark is equal to the current value of JET_paramKeyMost + 1.</span></span>

<span data-ttu-id="c8d1e-187">Por lo general, las claves se deben tratar como fragmentos opacos de datos.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-187">Keys should generally be treated as opaque chunks of data.</span></span> <span data-ttu-id="c8d1e-188">No se realiza ningún intento de aprovechar la estructura interna de estos datos.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-188">No attempt should be made to exploit the internal structure of this data.</span></span> <span data-ttu-id="c8d1e-189">Sin embargo, se pueden conocer las siguientes propiedades de todas las claves de ESENT:</span><span class="sxs-lookup"><span data-stu-id="c8d1e-189">However, the following properties can be known about all ESENT keys:</span></span>

  - <span data-ttu-id="c8d1e-190">Las claves se pueden comparar entre sí mediante [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para establecer su orden relativo en el índice de origen en la tabla de las entradas del índice de origen.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-190">Keys may be compared against each other using [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) to establish their relative ordering in the originating index over the table of the source index entries.</span></span>

  - <span data-ttu-id="c8d1e-191">No tiene sentido comparar las claves de las entradas de índice de distintos índices entre sí.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-191">It is meaningless to compare keys of index entries from different indexes against each other.</span></span>

  - <span data-ttu-id="c8d1e-192">Una clave siempre es menor o igual que JET_cbKeyMost (255) bytes de longitud antes de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-192">A key is always less than or equal to JET_cbKeyMost (255) bytes in length prior to Windows Vista.</span></span> <span data-ttu-id="c8d1e-193">En Windows Vista y versiones posteriores, las claves pueden ser más grandes.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-193">On Windows Vista and later releases, keys can be larger.</span></span> <span data-ttu-id="c8d1e-194">El tamaño máximo de una clave es igual al valor actual de JET_paramKeyMost.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-194">The maximum size of a key is equal to the current value of JET_paramKeyMost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c8d1e-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8d1e-195">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8d1e-196"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c8d1e-196"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c8d1e-197">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-197">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8d1e-198"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c8d1e-198"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c8d1e-199">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-199">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8d1e-200"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c8d1e-200"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c8d1e-201">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-201">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8d1e-202"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="c8d1e-202"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c8d1e-203">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-203">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8d1e-204"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c8d1e-204"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c8d1e-205">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c8d1e-205">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c8d1e-206">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8d1e-206">See Also</span></span>

[<span data-ttu-id="c8d1e-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c8d1e-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c8d1e-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c8d1e-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c8d1e-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c8d1e-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c8d1e-210">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c8d1e-210">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c8d1e-211">JetGetBookmark</span><span class="sxs-lookup"><span data-stu-id="c8d1e-211">JetGetBookmark</span></span>](./jetgetbookmark-function.md)  
[<span data-ttu-id="c8d1e-212">JetGotoSecondaryIndexBookmark</span><span class="sxs-lookup"><span data-stu-id="c8d1e-212">JetGotoSecondaryIndexBookmark</span></span>](./jetgotosecondaryindexbookmark-function.md)  
[<span data-ttu-id="c8d1e-213">JetRetrieveKey</span><span class="sxs-lookup"><span data-stu-id="c8d1e-213">JetRetrieveKey</span></span>](./jetretrievekey-function.md)  
<span data-ttu-id="c8d1e-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="c8d1e-214">[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))</span></span>
