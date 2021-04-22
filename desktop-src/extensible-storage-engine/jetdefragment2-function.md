---
description: 'Más información sobre: JetDefragment2 (Función)'
title: JetDefragment2 (Función)
TOCTitle: JetDefragment2 Function
ms:assetid: cfb190cf-8bd3-4479-a6a1-7c0c9e8c74ca
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294095(v=EXCHG.10)
ms:contentKeyID: 32765710
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragment2
- JetDefragment2A
- JetDefragment2W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bcde8d55032d2e07466668b5a4d96b9a447d843
ms.sourcegitcommit: 35baf9ba19918a38c4ca8714f88c004af0c6f518
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107838809"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="f00cb-103">JetDefragment2 (Función)</span><span class="sxs-lookup"><span data-stu-id="f00cb-103">JetDefragment2 Function</span></span>


<span data-ttu-id="f00cb-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f00cb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="f00cb-105">JetDefragment2 (Función)</span><span class="sxs-lookup"><span data-stu-id="f00cb-105">JetDefragment2 Function</span></span>

<span data-ttu-id="f00cb-106">La **función JetDefragment2** inicia y detiene las tareas de desfragmentación de la base de datos, lo que mejora la organización de datos dentro de una base de datos, con un parámetro de devolución de llamada disponible para informar del progreso de la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="f00cb-107">Esto se hace para limitar el crecimiento de la base de datos mediante el uso de la asignación de disco existente de forma más eficaz dentro de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f00cb-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="f00cb-108">También puede reducir el conjunto de trabajo asegurándose de que los datos están más empaquetados.</span><span class="sxs-lookup"><span data-stu-id="f00cb-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="f00cb-109">Por último, puede mejorar el rendimiento de la aplicación acelerando las operaciones comunes a través de una mejor organización de datos.</span><span class="sxs-lookup"><span data-stu-id="f00cb-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="f00cb-110">**Windows XP:**  **JetDefragment2** se introdujo en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f00cb-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="f00cb-111">**JetDefragment2 también** contiene un parámetro de función de devolución de llamada que se usa para informar sobre el progreso del proceso de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="f00cb-112">La desfragmentación de bases de datos es una operación en línea y no interrumpe la actividad normal de la base de datos, como las operaciones de consulta o las actualizaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="f00cb-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="f00cb-113">**JetDefragment2** tampoco realiza una copia de todos los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="f00cb-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="f00cb-114">En su lugar, desfragmenta una base de datos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f00cb-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="f00cb-115">Por último, **JetDefragment2** recupera el espacio interno de la base de datos para volver a usarlo, pero no libera espacio excesivo en el sistema de archivos del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f00cb-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="f00cb-116">El formato resultante de los datos puede ser mucho más eficaz, pero no suele ser óptimo.</span><span class="sxs-lookup"><span data-stu-id="f00cb-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="f00cb-117">La desfragmentación se limita a liberar páginas de base de datos para volver a usar que contienen datos que ya se han eliminado lógicamente.</span><span class="sxs-lookup"><span data-stu-id="f00cb-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="f00cb-118">La desfragmentación también hace que las páginas de base de datos estén disponibles para su uso de nuevo en algunos casos mediante la combinación de datos de dos páginas cuando caben en una sola página.</span><span class="sxs-lookup"><span data-stu-id="f00cb-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="f00cb-119">Esta operación es diferente de [JetCompact,](./jetcompact-function.md) que convierte una copia de una base de datos de solo lectura en un formato muy óptimo.</span><span class="sxs-lookup"><span data-stu-id="f00cb-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
JET_ERR JET_API JetDefragment2(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          JET_PCSTR szTableName,
  __out_opt     unsigned long* pcPasses,
  __out_opt     unsigned long* pcSeconds,
  __in          JET_CALLBACK callback,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="f00cb-120">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f00cb-120">Parameters</span></span>

<span data-ttu-id="f00cb-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="f00cb-121">*sesid*</span></span>

<span data-ttu-id="f00cb-122">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="f00cb-122">The session to use for this call.</span></span>

<span data-ttu-id="f00cb-123">*Dbid*</span><span class="sxs-lookup"><span data-stu-id="f00cb-123">*dbid*</span></span>

<span data-ttu-id="f00cb-124">Base de datos que se desfragmenta.</span><span class="sxs-lookup"><span data-stu-id="f00cb-124">The database to defragment.</span></span>

<span data-ttu-id="f00cb-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="f00cb-125">*szTableName*</span></span>

<span data-ttu-id="f00cb-126">A *veces se requiere szTableName* y, a veces, está prohibido:</span><span class="sxs-lookup"><span data-stu-id="f00cb-126">Sometimes *szTableName* is required, and sometimes it is forbidden:</span></span>

| <span data-ttu-id="f00cb-127">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f00cb-127">*grbit*</span></span> | <span data-ttu-id="f00cb-128">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="f00cb-128">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="f00cb-129">Debe ser `NULL`.</span><span class="sxs-lookup"><span data-stu-id="f00cb-129">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="f00cb-130">Especifica el nombre de la tabla o el árbol B que se va a desfragmentar.</span><span class="sxs-lookup"><span data-stu-id="f00cb-130">Specifies the name of the table/BTree to defragment.</span></span> |
| <span data-ttu-id="f00cb-131">*Otro*</span><span class="sxs-lookup"><span data-stu-id="f00cb-131">*other*</span></span> | <span data-ttu-id="f00cb-132">Debe ser `NULL`.</span><span class="sxs-lookup"><span data-stu-id="f00cb-132">Must be `NULL`.</span></span> |
 
<span data-ttu-id="f00cb-133">La desfragmentación se realiza para toda la base de datos descrita por el identificador de base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="f00cb-133">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="f00cb-134">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="f00cb-134">*pcPasses*</span></span>

<span data-ttu-id="f00cb-135">Al iniciar una tarea de desfragmentación en línea, este parámetro de entrada opcional establece el número máximo de pases de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-135">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="f00cb-136">Al detener una tarea de desfragmentación en línea, este búfer de salida opcional se establece en el número de pases realizados.</span><span class="sxs-lookup"><span data-stu-id="f00cb-136">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="f00cb-137">Cuando este parámetro se establece en NULL, el número de pases de desfragmentación en línea es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="f00cb-137">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="f00cb-138">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="f00cb-138">*pcSeconds*</span></span>

<span data-ttu-id="f00cb-139">Al iniciar una tarea de desfragmentación en línea, este parámetro de entrada opcional establece el tiempo máximo para la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-139">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="f00cb-140">Al detener una tarea de desfragmentación en línea, este búfer de salida opcional se establece en el período de tiempo utilizado para la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-140">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="f00cb-141">Cuando este parámetro se establece en NULL o *si pcSeconds* apunta a un valor negativo, el tiempo máximo para la desfragmentación es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="f00cb-141">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="f00cb-142">*devolución de llamada*</span><span class="sxs-lookup"><span data-stu-id="f00cb-142">*callback*</span></span>

<span data-ttu-id="f00cb-143">Función de devolución de llamada que llama periódicamente a la desfragmentación para informar del progreso.</span><span class="sxs-lookup"><span data-stu-id="f00cb-143">Callback function that defragmentation calls regularly to report progress.</span></span>

| <span data-ttu-id="f00cb-144">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f00cb-144">*grbit*</span></span> | <span data-ttu-id="f00cb-145">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="f00cb-145">*szTableName*</span></span> |
| --- | --- |
| `JET_bitDefragmentBTreeBatch` | <span data-ttu-id="f00cb-146">Debe ser `NULL`.</span><span class="sxs-lookup"><span data-stu-id="f00cb-146">Must be `NULL`.</span></span> |
| `JET_bitDefragmentBTree` | <span data-ttu-id="f00cb-147">Debe ser `NULL`.</span><span class="sxs-lookup"><span data-stu-id="f00cb-147">Must be `NULL`.</span></span> |
| <span data-ttu-id="f00cb-148">*Otro*</span><span class="sxs-lookup"><span data-stu-id="f00cb-148">*other*</span></span> | <span data-ttu-id="f00cb-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f00cb-149">Optional.</span></span>


<span data-ttu-id="f00cb-150">*grbit*</span><span class="sxs-lookup"><span data-stu-id="f00cb-150">*grbit*</span></span>

<span data-ttu-id="f00cb-151">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="f00cb-151">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f00cb-152">Value</span><span class="sxs-lookup"><span data-stu-id="f00cb-152">Value</span></span></p></th>
<th><p><span data-ttu-id="f00cb-153">Significado</span><span class="sxs-lookup"><span data-stu-id="f00cb-153">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-154">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="f00cb-154">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="f00cb-155">Esta opción se usa para desfragmentar la parte de espacio disponible de la asignación de espacio de base de datos ese.</span><span class="sxs-lookup"><span data-stu-id="f00cb-155">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="f00cb-156">El espacio de base de datos se divide en dos tipos: espacio de propiedad y espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="f00cb-156">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="f00cb-157">El espacio de propiedad se asigna a una tabla o índice, mientras que el espacio disponible está listo para su uso dentro de la tabla o el índice, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f00cb-157">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="f00cb-158">El espacio disponible es mucho más dinámico en el comportamiento y requiere desfragmentación en línea más que los datos de espacio o tabla o índice en propiedad.</span><span class="sxs-lookup"><span data-stu-id="f00cb-158">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-159">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="f00cb-159">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="f00cb-160">Esta opción se usa para iniciar una nueva tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-160">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-161">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="f00cb-161">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="f00cb-162">Esta opción se usa para detener una tarea de desfragmentación iniciada existente.</span><span class="sxs-lookup"><span data-stu-id="f00cb-162">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-163">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="f00cb-163">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="f00cb-164">Esta opción se usa para desfragmentar un árbol B, especificado por szTableName.</span><span class="sxs-lookup"><span data-stu-id="f00cb-164">This option is used to defrag a B-Tree, specified by szTableName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-165">JET_bitDefragmentBTreeBatch</span><span class="sxs-lookup"><span data-stu-id="f00cb-165">JET_bitDefragmentBTreeBatch</span></span></p></td>
<td><p><span data-ttu-id="f00cb-166">Esta opción se usa para llamar a OLD2 en toda la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f00cb-166">This option is used to call OLD2 on the entire database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f00cb-167">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f00cb-167">Return Value</span></span>

<span data-ttu-id="f00cb-168">Esta función devuelve el [JET_ERR](./jet-err.md) tipo de datos con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="f00cb-168">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="f00cb-169">Para obtener más información sobre los posibles errores de ESE, vea [Errores extensibles del motor](./extensible-storage-engine-errors.md) de almacenamiento y Parámetros de control de [errores.](./error-handling-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="f00cb-169">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f00cb-170">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f00cb-170">Return code</span></span></p></th>
<th><p><span data-ttu-id="f00cb-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="f00cb-171">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-172">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="f00cb-172">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="f00cb-173">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f00cb-173">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-174">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="f00cb-174">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="f00cb-175">No es posible completar la operación porque toda la actividad de la instancia asociada a la sesión ha dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="f00cb-175">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-176">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="f00cb-176">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="f00cb-177">La base de datos elegida para la desfragmentación es de solo lectura y no se puede actualizar de ninguna manera, incluida la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-177">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="f00cb-178">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="f00cb-179">La sesión dada está en el estado preparado para confirmarse y no puede iniciar nuevas actualizaciones hasta que se confirme o revierte la transacción actual.</span><span class="sxs-lookup"><span data-stu-id="f00cb-179">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-180">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="f00cb-180">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="f00cb-181">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error grave que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="f00cb-181">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="f00cb-182">Este error solo lo devolverán Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f00cb-182">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-183">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="f00cb-183">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="f00cb-184">El identificador de base de datos especificado no coincide con una base de datos conocida de la instancia.</span><span class="sxs-lookup"><span data-stu-id="f00cb-184">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-185">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="f00cb-185">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="f00cb-186">No es posible completar la operación porque la instancia asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="f00cb-186">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-187">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="f00cb-187">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="f00cb-188">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="f00cb-188">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-189">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="f00cb-189">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="f00cb-190">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="f00cb-190">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="f00cb-191">Este error solo lo devolverán Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="f00cb-191">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-192">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="f00cb-192">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="f00cb-193">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="f00cb-193">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-194">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="f00cb-194">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="f00cb-195">La sesión determinada solo tiene privilegios de solo lectura y no puede iniciar una tarea que pueda realizar una actualización, incluida la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-195">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-196">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="f00cb-196">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="f00cb-197">Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="f00cb-197">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-198">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="f00cb-198">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="f00cb-199">La JET_bitDefragmentBatchStart se ha pasado, pero una tarea de desfragmentación ya está ejecutando la desfragmentación en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="f00cb-199">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-200">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="f00cb-200">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="f00cb-201">Se ha JET_bitDefragmentBatchStop la opción de desfragmentación, pero actualmente no se está ejecutando ninguna tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-201">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f00cb-202">Si se realiza correctamente, se realiza la acción solicitada de iniciar una tarea de desfragmentación para un determinado dato con opciones determinadas, o bien se realiza la acción de detener una tarea de desfragmentación existente.</span><span class="sxs-lookup"><span data-stu-id="f00cb-202">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="f00cb-203">En caso de error, no se realiza la acción solicitada de iniciar o detener un trabajo de desfragmentación en línea.</span><span class="sxs-lookup"><span data-stu-id="f00cb-203">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="f00cb-204">No se producen otros efectos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f00cb-204">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f00cb-205">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f00cb-205">Remarks</span></span>

<span data-ttu-id="f00cb-206">La desfragmentación en línea se controla mediante una configuración de parámetros, así como mediante esta API.</span><span class="sxs-lookup"><span data-stu-id="f00cb-206">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="f00cb-207">El valor predeterminado del parámetro del sistema es JET_OnlineDefragAll, lo que significa que la desfragmentación está habilitada para todas las estructuras de datos admitidas.</span><span class="sxs-lookup"><span data-stu-id="f00cb-207">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="f00cb-208">Sin embargo, con [JetSetSystemParameter](./jetsetsystemparameter-function.md), es posible deshabilitar la desfragmentación en línea o habilitarla de forma selectiva solo para árboles de espacio de base de datos, solo bases de datos, solo archivos de streaming o cualquier combinación de estas opciones.</span><span class="sxs-lookup"><span data-stu-id="f00cb-208">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="f00cb-209">Si la configuración del sistema para la desfragmentación en línea es una configuración obsoleta, **JetDefragment2** tratará la configuración como JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="f00cb-209">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="f00cb-210">Puede haber como máximo una tarea en ejecución para cada base de datos.</span><span class="sxs-lookup"><span data-stu-id="f00cb-210">There can at most be one task running for each database.</span></span> <span data-ttu-id="f00cb-211">La tarea se ejecuta como un subproceso en el proceso que hospeda ese.</span><span class="sxs-lookup"><span data-stu-id="f00cb-211">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="f00cb-212">La sesión utilizada para iniciar la tarea de desfragmentación en línea se puede usar posteriormente para las operaciones de base de datos mientras la tarea de desfragmentación continúa, porque la tarea de desfragmentación asigna su propia sesión.</span><span class="sxs-lookup"><span data-stu-id="f00cb-212">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="f00cb-213">La sesión dada solo se usa para comprobar los permisos asociados a la sesión de inicio de la tarea y no se usa realmente para las propias operaciones de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="f00cb-213">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f00cb-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f00cb-214">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-215"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f00cb-215"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f00cb-216">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f00cb-216">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-217"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="f00cb-217"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f00cb-218">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f00cb-218">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-219"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f00cb-219"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f00cb-220">Declarado en Esent.h.</span><span class="sxs-lookup"><span data-stu-id="f00cb-220">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-221"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="f00cb-221"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="f00cb-222">Use ESENT.lib.</span><span class="sxs-lookup"><span data-stu-id="f00cb-222">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f00cb-223"><strong>Dll</strong></span><span class="sxs-lookup"><span data-stu-id="f00cb-223"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="f00cb-224">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="f00cb-224">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f00cb-225"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="f00cb-225"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="f00cb-226">Se implementa <strong>como JetDefragment2W</strong> (Unicode) y <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f00cb-226">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="f00cb-227">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f00cb-227">See Also</span></span>

[<span data-ttu-id="f00cb-228">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="f00cb-228">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="f00cb-229">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f00cb-229">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f00cb-230">JetCompact</span><span class="sxs-lookup"><span data-stu-id="f00cb-230">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="f00cb-231">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="f00cb-231">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="f00cb-232">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="f00cb-232">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="f00cb-233">JetStopService</span><span class="sxs-lookup"><span data-stu-id="f00cb-233">JetStopService</span></span>](./jetstopservice-function.md)
