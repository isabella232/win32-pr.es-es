---
description: 'Más información acerca de: JetIndexRecordCount (función)'
title: JetIndexRecordCount función)
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539979"
---
# <a name="jetindexrecordcount-function"></a><span data-ttu-id="02e1d-103">JetIndexRecordCount función)</span><span class="sxs-lookup"><span data-stu-id="02e1d-103">JetIndexRecordCount Function</span></span>


<span data-ttu-id="02e1d-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="02e1d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetindexrecordcount-function"></a><span data-ttu-id="02e1d-105">JetIndexRecordCount función)</span><span class="sxs-lookup"><span data-stu-id="02e1d-105">JetIndexRecordCount Function</span></span>

<span data-ttu-id="02e1d-106">La función **JetIndexRecordCount** cuenta el número de entradas en el índice actual desde la posición actual hacia delante.</span><span class="sxs-lookup"><span data-stu-id="02e1d-106">The **JetIndexRecordCount** function counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="02e1d-107">La posición actual se incluye en el recuento.</span><span class="sxs-lookup"><span data-stu-id="02e1d-107">The current position is included in the count.</span></span> <span data-ttu-id="02e1d-108">El recuento puede ser mayor que el número total de registros de la tabla si el índice actual está sobre una columna de varios valores y las instancias de la columna tienen varios valores.</span><span class="sxs-lookup"><span data-stu-id="02e1d-108">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="02e1d-109">Si la tabla está vacía, se devolverá 0 para el recuento.</span><span class="sxs-lookup"><span data-stu-id="02e1d-109">If the table is empty, then 0 will be returned for the count.</span></span>

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a><span data-ttu-id="02e1d-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02e1d-110">Parameters</span></span>

<span data-ttu-id="02e1d-111">*sesid*</span><span class="sxs-lookup"><span data-stu-id="02e1d-111">*sesid*</span></span>

<span data-ttu-id="02e1d-112">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="02e1d-112">The session to use for this call.</span></span>

<span data-ttu-id="02e1d-113">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="02e1d-113">*tableid*</span></span>

<span data-ttu-id="02e1d-114">Cursor que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="02e1d-114">The cursor to use for this call.</span></span>

<span data-ttu-id="02e1d-115">*pcrec*</span><span class="sxs-lookup"><span data-stu-id="02e1d-115">*pcrec*</span></span>

<span data-ttu-id="02e1d-116">El puntero a un valor Long sin signo para recibir el recuento.</span><span class="sxs-lookup"><span data-stu-id="02e1d-116">The pointer to an unsigned long value to receive the count.</span></span>

<span data-ttu-id="02e1d-117">*crecMax*</span><span class="sxs-lookup"><span data-stu-id="02e1d-117">*crecMax*</span></span>

<span data-ttu-id="02e1d-118">Número máximo de registros que se van a contar.</span><span class="sxs-lookup"><span data-stu-id="02e1d-118">The maximum number of records to count.</span></span> <span data-ttu-id="02e1d-119">Un valor de *crecMax* de 0 indica que el recuento es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="02e1d-119">A *crecMax* value of 0 indicates that the count is unlimited.</span></span>

### <a name="return-value"></a><span data-ttu-id="02e1d-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02e1d-120">Return Value</span></span>

<span data-ttu-id="02e1d-121">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="02e1d-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="02e1d-122">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="02e1d-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02e1d-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="02e1d-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="02e1d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="02e1d-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02e1d-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="02e1d-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="02e1d-126">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="02e1d-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e1d-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="02e1d-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="02e1d-128">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="02e1d-128">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e1d-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="02e1d-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="02e1d-130">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="02e1d-130">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="02e1d-131"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02e1d-131"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e1d-132">JET_errNoCurrentRecord</span><span class="sxs-lookup"><span data-stu-id="02e1d-132">JET_errNoCurrentRecord</span></span></p></td>
<td><p><span data-ttu-id="02e1d-133">El cursor no está actualmente en un registro y la tabla no está vacía.</span><span class="sxs-lookup"><span data-stu-id="02e1d-133">The cursor is not currently on a record and the table is not empty.</span></span></p>
<p><span data-ttu-id="02e1d-134"><strong>Windows XP, Windows server 2003, windows 2000 Server y windows 2000 Professional:</strong>  Si el cursor está situado en un índice vacío o en un intervalo de índices, <strong>JetIndexRecordCount</strong> devuelve erróneamente JET_errNoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="02e1d-134"><strong>Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:</strong>  If the cursor is positioned on an empty index or index range then <strong>JetIndexRecordCount</strong> erroneously returns JET_errNoCurrentRecord.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e1d-135">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="02e1d-135">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="02e1d-136">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="02e1d-136">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e1d-137">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="02e1d-137">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="02e1d-138">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="02e1d-138">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e1d-139">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="02e1d-139">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="02e1d-140">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="02e1d-140">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="02e1d-141"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02e1d-141"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e1d-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="02e1d-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="02e1d-143">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="02e1d-143">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02e1d-144">Si esta función se ejecuta correctamente, el número exacto de entradas de índice, incluida la posición actual y hasta *crecMax* (si no es 0), se devuelve en la unsigned Long a la que apunta *pcrec*.</span><span class="sxs-lookup"><span data-stu-id="02e1d-144">If this function succeeds, the exact number of index entries including the current position and up to *crecMax* (if it is not 0), is returned in the unsigned long pointed to by *pcrec*.</span></span>

<span data-ttu-id="02e1d-145">Si se produce un error en esta función, no se realiza ningún cambio en la memoria asignada en *precpos*.</span><span class="sxs-lookup"><span data-stu-id="02e1d-145">If this function fails, no changes are made to memory allocated at *precpos*.</span></span>

#### <a name="remarks"></a><span data-ttu-id="02e1d-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02e1d-146">Remarks</span></span>

<span data-ttu-id="02e1d-147">Si la tabla no está vacía, el cursor se debe colocar en el registro desde el que se va a iniciar el recuento.</span><span class="sxs-lookup"><span data-stu-id="02e1d-147">If the table is not empty, then the cursor should be positioned onto the record from which to begin the count.</span></span> <span data-ttu-id="02e1d-148">El recuento incluirá este registro y recuento hasta el límite especificado en *crecMax*.</span><span class="sxs-lookup"><span data-stu-id="02e1d-148">The count will include this record, and count forward up to the given limit in *crecMax*.</span></span> <span data-ttu-id="02e1d-149">Si *crecMax* es 0, la operación seguirá contando hasta el final del índice.</span><span class="sxs-lookup"><span data-stu-id="02e1d-149">If *crecMax* is 0 then the operation will continue counting until the end of the index.</span></span>

<span data-ttu-id="02e1d-150">Los intervalos de índice se pueden usar para construir limitaciones de final de índice artificiales para el recuento.</span><span class="sxs-lookup"><span data-stu-id="02e1d-150">Index ranges can be used to construct artificial end-of-index limitations for the count.</span></span> <span data-ttu-id="02e1d-151">De esta manera, los subintervalos de un índice se pueden contar exactamente.</span><span class="sxs-lookup"><span data-stu-id="02e1d-151">In this way, subranges of an index can be counted exactly.</span></span> <span data-ttu-id="02e1d-152">El cursor debe colocarse en la primera fila del intervalo.</span><span class="sxs-lookup"><span data-stu-id="02e1d-152">The cursor should be positioned to the first row in the range.</span></span> <span data-ttu-id="02e1d-153">Se debe crear el final de la clave de intervalo y, a continuación, se debe usar [JetSetIndexRange](./jetsetindexrange-function.md) para establecer el intervalo superior, ya sea de forma inclusiva o exclusiva.</span><span class="sxs-lookup"><span data-stu-id="02e1d-153">The end of the range key should be made and then [JetSetIndexRange](./jetsetindexrange-function.md) should be used to set the upper range, either inclusively or exclusively.</span></span> <span data-ttu-id="02e1d-154">Por último, se debe llamar a **JetIndexRecordCount** para contar exactamente el intervalo.</span><span class="sxs-lookup"><span data-stu-id="02e1d-154">Lastly, **JetIndexRecordCount** should be called to exactly count the range.</span></span>

<span data-ttu-id="02e1d-155">**JetIndexRecordCount** obedece la semántica de las transacciones y devuelve un recuento exacto para esta sesión en particular en su estado transaccional actual.</span><span class="sxs-lookup"><span data-stu-id="02e1d-155">**JetIndexRecordCount** obeys transaction semantics and returns a count that is accurate for this particular session in its current transactional state.</span></span>

<span data-ttu-id="02e1d-156">**JetIndexRecordCount** obtiene acceso a las páginas hoja del índice con el fin de contar exactamente las entradas.</span><span class="sxs-lookup"><span data-stu-id="02e1d-156">**JetIndexRecordCount** accesses index leaf pages in order to exactly count entries.</span></span> <span data-ttu-id="02e1d-157">Por lo tanto, puede realizar una gran cantidad de e/s y puede ser lenta.</span><span class="sxs-lookup"><span data-stu-id="02e1d-157">Consequently, it can perform a great deal of I/O and can be slow.</span></span> <span data-ttu-id="02e1d-158">La limitación de *crecMax* debe usarse para evitar una carga excesiva.</span><span class="sxs-lookup"><span data-stu-id="02e1d-158">The *crecMax* limitation should be used to prevent excessive load.</span></span> <span data-ttu-id="02e1d-159">Si un intervalo es grande, es posible que se pueda contar el intervalo de manera aproximada mediante [JetGetRecordPosition](./jetgetrecordposition-function.md).</span><span class="sxs-lookup"><span data-stu-id="02e1d-159">If a range is large, then it might be possible to count the range in an approximated fashion using [JetGetRecordPosition](./jetgetrecordposition-function.md).</span></span>

<span data-ttu-id="02e1d-160">**Windows XP, Windows server 2003, windows 2000 Server y windows 2000 Professional:**  Si el cursor está situado en un índice vacío o en un intervalo de índices, **JetIndexRecordCount** devuelve erróneamente JET_errNoCurrentRecord en lugar de devolver un recuento de registros de cero.</span><span class="sxs-lookup"><span data-stu-id="02e1d-160">**Windows XP, Windows Server 2003, Windows 2000 Server, and Windows 2000 Professional:**  If the cursor is positioned on an empty index or index range then **JetIndexRecordCount** erroneously returns JET_errNoCurrentRecord rather than returning a record count of zero.</span></span> <span data-ttu-id="02e1d-161">La aplicación debe comprobar si el índice o el intervalo de índices está vacío en este caso.</span><span class="sxs-lookup"><span data-stu-id="02e1d-161">The application should check to see if the index or index range is empty in this case.</span></span>

#### <a name="requirements"></a><span data-ttu-id="02e1d-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02e1d-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02e1d-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="02e1d-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="02e1d-164">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="02e1d-164">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e1d-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="02e1d-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="02e1d-166">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="02e1d-166">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e1d-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="02e1d-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="02e1d-168">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="02e1d-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02e1d-169"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="02e1d-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="02e1d-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="02e1d-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02e1d-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="02e1d-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="02e1d-172">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="02e1d-172">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="02e1d-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="02e1d-173">See Also</span></span>

[<span data-ttu-id="02e1d-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="02e1d-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="02e1d-175">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="02e1d-175">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="02e1d-176">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="02e1d-176">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="02e1d-177">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="02e1d-177">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="02e1d-178">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="02e1d-178">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)  
[<span data-ttu-id="02e1d-179">JetStopService</span><span class="sxs-lookup"><span data-stu-id="02e1d-179">JetStopService</span></span>](./jetstopservice-function.md)
