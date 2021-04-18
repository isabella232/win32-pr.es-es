---
description: 'Más información acerca de: JetComputeStats (función)'
title: JetComputeStats función)
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279396"
---
# <a name="jetcomputestats-function"></a><span data-ttu-id="c16cf-103">JetComputeStats función)</span><span class="sxs-lookup"><span data-stu-id="c16cf-103">JetComputeStats Function</span></span>


<span data-ttu-id="c16cf-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c16cf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetcomputestats-function"></a><span data-ttu-id="c16cf-105">JetComputeStats función)</span><span class="sxs-lookup"><span data-stu-id="c16cf-105">JetComputeStats Function</span></span>

<span data-ttu-id="c16cf-106">La función **JetComputeStats** recorre cada índice de una tabla para calcular exactamente el número de entradas de un índice y el número de claves distintas de un índice.</span><span class="sxs-lookup"><span data-stu-id="c16cf-106">The **JetComputeStats** function walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="c16cf-107">Esta información, junto con el número de páginas de base de datos asignadas para un índice y la hora actual del cálculo, se almacena en los metadatos de índice de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c16cf-107">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="c16cf-108">Estos datos se pueden recuperar posteriormente con operaciones de información.</span><span class="sxs-lookup"><span data-stu-id="c16cf-108">This data can be subsequently retrieved with information operations.</span></span>

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a><span data-ttu-id="c16cf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c16cf-109">Parameters</span></span>

<span data-ttu-id="c16cf-110">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c16cf-110">*sesid*</span></span>

<span data-ttu-id="c16cf-111">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c16cf-111">The session to use for this call.</span></span>

<span data-ttu-id="c16cf-112">*TABLEID*</span><span class="sxs-lookup"><span data-stu-id="c16cf-112">*tableid*</span></span>

<span data-ttu-id="c16cf-113">Cursor que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c16cf-113">The cursor that will be used for this call.</span></span> <span data-ttu-id="c16cf-114">Describe la tabla en la que se van a calcular las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="c16cf-114">Describes the table to compute statistics on.</span></span>

### <a name="return-value"></a><span data-ttu-id="c16cf-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c16cf-115">Return Value</span></span>

<span data-ttu-id="c16cf-116">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="c16cf-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c16cf-117">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c16cf-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c16cf-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c16cf-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="c16cf-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c16cf-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c16cf-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c16cf-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c16cf-121">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c16cf-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c16cf-122">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c16cf-122">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c16cf-123">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c16cf-123">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c16cf-124">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c16cf-124">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c16cf-125">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="c16cf-125">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="c16cf-126">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c16cf-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c16cf-127">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c16cf-127">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c16cf-128">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c16cf-128">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c16cf-129">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c16cf-129">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c16cf-130">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c16cf-130">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c16cf-131">JET_errRollbackError</span><span class="sxs-lookup"><span data-stu-id="c16cf-131">JET_errRollbackError</span></span></p></td>
<td><p><span data-ttu-id="c16cf-132">Se produjo un error que requiere que esta operación revierta todos los cambios, pero no se pudo revertir la transacción.</span><span class="sxs-lookup"><span data-stu-id="c16cf-132">An error occurred requiring this operation to rollback all changes, but the transaction rollback itself failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c16cf-133">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="c16cf-133">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="c16cf-134">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c16cf-134">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="c16cf-135">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c16cf-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c16cf-136">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c16cf-136">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c16cf-137">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c16cf-137">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c16cf-138">En caso de éxito, las estadísticas actualizadas se almacenan en los catálogos de base de datos de la tabla descrita con el cursor especificado.</span><span class="sxs-lookup"><span data-stu-id="c16cf-138">On success, up-to-date statistics are stored in the database catalogs for the table described with the given cursor.</span></span>

<span data-ttu-id="c16cf-139">En caso de error, no se realiza ninguna actualización de ningún tipo en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c16cf-139">On failure, no updates of any kind are made to the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c16cf-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c16cf-140">Remarks</span></span>

<span data-ttu-id="c16cf-141">Esta operación puede consumir recursos, ya que todos los índices de una tabla se deben recorrer en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="c16cf-141">This operation can be resource consuming since each index in a table must be walked in its entirety.</span></span> <span data-ttu-id="c16cf-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) se puede usar para obtener una estimación aproximada del número de entradas de un índice, pero no puede calcular por sí misma el número de valores distintos de un índice.</span><span class="sxs-lookup"><span data-stu-id="c16cf-142">[JetGetRecordPosition](./jetgetrecordposition-function.md) can be used to get a rough estimate of the number of entries in an index, but it cannot by itself estimate the number of distinct values in an index.</span></span>

<span data-ttu-id="c16cf-143">Los datos calculados por esta operación empiezan a quedar obsoletos y la tabla se actualiza posteriormente.</span><span class="sxs-lookup"><span data-stu-id="c16cf-143">The data computed by this operation begins to become out of date and the table is subsequently updated.</span></span>

<span data-ttu-id="c16cf-144">Las actualizaciones de la base de datos realizadas por **JetComputeStats** se realizan de manera diferida.</span><span class="sxs-lookup"><span data-stu-id="c16cf-144">Updates to the database made by **JetComputeStats** are made in a lazy fashion.</span></span> <span data-ttu-id="c16cf-145">Esto significa que no se adjuntará ningún vaciado de registro por esta operación y un bloqueo del sistema posterior a una devolución de JET_errSuccess por parte de **JetComputeStats** puede hacer que se pierdan estas actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="c16cf-145">This means that no log flush will be accompanied by this operation and a system crash subsequent to a return of JET_errSuccess by **JetComputeStats** can still cause these updates to be lost.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c16cf-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c16cf-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c16cf-147"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c16cf-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c16cf-148">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c16cf-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c16cf-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c16cf-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c16cf-150">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c16cf-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c16cf-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c16cf-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c16cf-152">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c16cf-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c16cf-153"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="c16cf-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c16cf-154">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c16cf-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c16cf-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c16cf-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c16cf-156">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c16cf-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c16cf-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c16cf-157">See Also</span></span>

[<span data-ttu-id="c16cf-158">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c16cf-158">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c16cf-159">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c16cf-159">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c16cf-160">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c16cf-160">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c16cf-161">JetGetRecordPosition</span><span class="sxs-lookup"><span data-stu-id="c16cf-161">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)  
[<span data-ttu-id="c16cf-162">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="c16cf-162">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="c16cf-163">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c16cf-163">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="c16cf-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c16cf-164">JetStopService</span></span>](./jetstopservice-function.md)
