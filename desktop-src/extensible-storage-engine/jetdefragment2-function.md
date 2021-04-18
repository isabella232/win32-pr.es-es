---
description: 'Más información acerca de: JetDefragment2 (función)'
title: JetDefragment2 función)
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
ms.openlocfilehash: 8064ae996831f61869d74ff1fd7c0f2222257b85
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105721555"
---
# <a name="jetdefragment2-function"></a><span data-ttu-id="e0272-103">JetDefragment2 función)</span><span class="sxs-lookup"><span data-stu-id="e0272-103">JetDefragment2 Function</span></span>


<span data-ttu-id="e0272-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0272-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment2-function"></a><span data-ttu-id="e0272-105">JetDefragment2 función)</span><span class="sxs-lookup"><span data-stu-id="e0272-105">JetDefragment2 Function</span></span>

<span data-ttu-id="e0272-106">La función **JetDefragment2** inicia y detiene las tareas de desfragmentación de bases de datos que mejoran la organización de datos en una base de datos, con un parámetro de devolución de llamada disponible para informar del progreso de la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-106">The **JetDefragment2** function starts and stops database defragmentation tasks which improves data organization within a database, with a callback parameter available to report the progress of the defragmentation.</span></span> <span data-ttu-id="e0272-107">Esto se hace para limitar el crecimiento de la base de datos mediante la asignación de disco existente de forma más eficaz en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e0272-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="e0272-108">También puede reducir el espacio de trabajo asegurándose de que los datos se empaquetan con mayor precisión.</span><span class="sxs-lookup"><span data-stu-id="e0272-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="e0272-109">Por último, puede mejorar el rendimiento de la aplicación al acelerar las operaciones comunes a través de una mejor organización de datos.</span><span class="sxs-lookup"><span data-stu-id="e0272-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="e0272-110">**Windows XP:**  **JetDefragment2** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0272-110">**Windows XP:**  **JetDefragment2** is introduced in Windows XP.</span></span>

<span data-ttu-id="e0272-111">**JetDefragment2** también contiene un parámetro de función de devolución de llamada que se usa para informar sobre el progreso del proceso de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-111">**JetDefragment2** also contains a callback function parameter that is used to report on the progress of the defragmentation process.</span></span>

<span data-ttu-id="e0272-112">La desfragmentación de bases de datos es una operación en línea y no interrumpe la actividad normal de la base de datos, como operaciones de consulta o actualizaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="e0272-112">Database defragmentation is an online operation and does not interrupt regular database activity such as query operations or data updates.</span></span> <span data-ttu-id="e0272-113">**JetDefragment2** tampoco realiza una copia de todos los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="e0272-113">**JetDefragment2** also does not make a copy of all existing data.</span></span> <span data-ttu-id="e0272-114">En su lugar, desfragmenta una base de datos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e0272-114">Instead, it defragments a database in place.</span></span> <span data-ttu-id="e0272-115">Por último, **JetDefragment2** recupera el espacio interno de la base de datos para su reutilización, pero no libera espacio sobrante en el sistema de archivos del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e0272-115">Lastly, **JetDefragment2** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="e0272-116">El formato resultante de los datos puede ser mucho más eficaz, pero no suele ser óptimo.</span><span class="sxs-lookup"><span data-stu-id="e0272-116">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="e0272-117">La desfragmentación se limita a liberar páginas de base de datos para que se vuelvan a usar, que contienen datos que ya se han eliminado lógicamente.</span><span class="sxs-lookup"><span data-stu-id="e0272-117">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="e0272-118">La desfragmentación también hace que las páginas de base de datos estén disponibles para su reutilización en algunos casos mediante la combinación de datos de dos páginas cuando quepa en una sola página.</span><span class="sxs-lookup"><span data-stu-id="e0272-118">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="e0272-119">Esta operación es diferente de [JetCompact](./jetcompact-function.md) , que realiza una copia de una base de datos de solo lectura en una forma muy óptima.</span><span class="sxs-lookup"><span data-stu-id="e0272-119">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

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

### <a name="parameters"></a><span data-ttu-id="e0272-120">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0272-120">Parameters</span></span>

<span data-ttu-id="e0272-121">*sesid*</span><span class="sxs-lookup"><span data-stu-id="e0272-121">*sesid*</span></span>

<span data-ttu-id="e0272-122">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e0272-122">The session to use for this call.</span></span>

<span data-ttu-id="e0272-123">*DBID*</span><span class="sxs-lookup"><span data-stu-id="e0272-123">*dbid*</span></span>

<span data-ttu-id="e0272-124">Base de datos que se va a desfragmentar.</span><span class="sxs-lookup"><span data-stu-id="e0272-124">The database to defragment.</span></span>

<span data-ttu-id="e0272-125">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="e0272-125">*szTableName*</span></span>

<span data-ttu-id="e0272-126">Parámetro sin usar.</span><span class="sxs-lookup"><span data-stu-id="e0272-126">Unused parameter.</span></span> <span data-ttu-id="e0272-127">La desfragmentación se realiza para toda la base de datos descrita por el identificador de base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="e0272-127">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="e0272-128">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="e0272-128">*pcPasses*</span></span>

<span data-ttu-id="e0272-129">Al iniciar una tarea de desfragmentación con conexión, este parámetro de entrada opcional establece el número máximo de pasos de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-129">When starting an online defragmentation task, this optional input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="e0272-130">Al detener una tarea de desfragmentación en línea, este búfer de salida opcional se establece en el número de pasos realizados.</span><span class="sxs-lookup"><span data-stu-id="e0272-130">When stopping an online defragmentation task, this optional output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="e0272-131">Cuando este parámetro se establece en NULL, el número de pases de desfragmentación en línea es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="e0272-131">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="e0272-132">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="e0272-132">*pcSeconds*</span></span>

<span data-ttu-id="e0272-133">Al iniciar una tarea de desfragmentación con conexión, este parámetro de entrada opcional establece el tiempo máximo de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-133">When starting an online defragmentation task, this optional input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="e0272-134">Al detener una tarea de desfragmentación en línea, este búfer de salida opcional se establece en el período de tiempo utilizado para la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-134">When stopping an online defragmentation task, this optional output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="e0272-135">Cuando este parámetro se establece en NULL o si *pcSeconds* apunta a un valor negativo, el tiempo máximo para la desfragmentación es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="e0272-135">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="e0272-136">*devolución de llamada*</span><span class="sxs-lookup"><span data-stu-id="e0272-136">*callback*</span></span>

<span data-ttu-id="e0272-137">Función de devolución de llamada que la desfragmentación llama regularmente para informar del progreso.</span><span class="sxs-lookup"><span data-stu-id="e0272-137">Callback function that defragmentation calls regularly to report progress.</span></span>

<span data-ttu-id="e0272-138">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e0272-138">*grbit*</span></span>

<span data-ttu-id="e0272-139">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="e0272-139">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0272-140">Value</span><span class="sxs-lookup"><span data-stu-id="e0272-140">Value</span></span></p></th>
<th><p><span data-ttu-id="e0272-141">Significado</span><span class="sxs-lookup"><span data-stu-id="e0272-141">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0272-142">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="e0272-142">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="e0272-143">Esta opción se usa para desfragmentar la parte de espacio disponible de la asignación de espacio de base de datos de ESE.</span><span class="sxs-lookup"><span data-stu-id="e0272-143">This option is used to defragment the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="e0272-144">El espacio de la base de datos se divide en dos tipos, espacio de propiedad y espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="e0272-144">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="e0272-145">El espacio de propiedad se asigna a una tabla o un índice mientras que el espacio disponible está listo para su uso en la tabla o el índice, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e0272-145">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="e0272-146">El espacio disponible es mucho más dinámico en el comportamiento y requiere una desfragmentación en línea más que el espacio de propiedad o los datos de la tabla o el índice.</span><span class="sxs-lookup"><span data-stu-id="e0272-146">Available space is much more dynamic in behavior and requires online defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-147">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="e0272-147">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="e0272-148">Esta opción se usa para iniciar una nueva tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-148">This option is used to start a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-149">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="e0272-149">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="e0272-150">Esta opción se usa para detener una tarea de desfragmentación iniciada existente.</span><span class="sxs-lookup"><span data-stu-id="e0272-150">This option is used to stop an existing started defragmentation task.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-151">JET_bitDefragmentBTree</span><span class="sxs-lookup"><span data-stu-id="e0272-151">JET_bitDefragmentBTree</span></span></p></td>
<td><p><span data-ttu-id="e0272-152">Esta opción se usa para desfragmentar un árbol B.</span><span class="sxs-lookup"><span data-stu-id="e0272-152">This option is used to defrag a B-Tree.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e0272-153">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0272-153">Return Value</span></span>

<span data-ttu-id="e0272-154">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="e0272-154">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e0272-155">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e0272-155">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0272-156">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e0272-156">Return code</span></span></p></th>
<th><p><span data-ttu-id="e0272-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0272-157">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0272-158">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e0272-158">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e0272-159">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0272-159">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-160">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="e0272-160">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="e0272-161">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="e0272-161">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-162">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="e0272-162">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e0272-163">La base de datos elegida para la desfragmentación es de solo lectura y no se puede actualizar de ningún modo, incluida la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-163">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="e0272-164">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="e0272-165">La sesión determinada está en el estado preparado para confirmar y no puede iniciar nuevas actualizaciones hasta que la transacción actual se confirma o se revierte.</span><span class="sxs-lookup"><span data-stu-id="e0272-165">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-166">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="e0272-166">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="e0272-167">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="e0272-167">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="e0272-168">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e0272-168">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-169">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="e0272-169">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="e0272-170">El identificador de base de datos especificado no coincide con una base de datos conocida en la instancia.</span><span class="sxs-lookup"><span data-stu-id="e0272-170">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-171">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="e0272-171">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="e0272-172">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e0272-172">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-173">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="e0272-173">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="e0272-174">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e0272-174">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-175">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="e0272-175">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="e0272-176">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e0272-176">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="e0272-177">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e0272-177">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-178">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="e0272-178">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="e0272-179">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="e0272-179">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-180">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="e0272-180">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e0272-181">La sesión determinada solo tiene privilegios de solo lectura y no puede iniciar una tarea que pueda realizar una actualización, incluida la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-181">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-182">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="e0272-182">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="e0272-183">Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="e0272-183">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-184">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="e0272-184">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="e0272-185">Se ha pasado la opción de JET_bitDefragmentBatchStart pero una tarea de desfragmentación ya está ejecutando la desfragmentación en la base de datos dada.</span><span class="sxs-lookup"><span data-stu-id="e0272-185">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-186">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="e0272-186">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="e0272-187">Se pasó la opción de JET_bitDefragmentBatchStop, pero no se está ejecutando ninguna tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-187">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e0272-188">Si se ejecuta correctamente, se realiza la acción solicitada de iniciar una tarea de desfragmentación para un determinado dato con opciones determinadas, o bien se realiza la acción de detener una tarea de desfragmentación existente.</span><span class="sxs-lookup"><span data-stu-id="e0272-188">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="e0272-189">En caso de error, no se realiza la acción solicitada de iniciar o detener un trabajo de desfragmentación en línea.</span><span class="sxs-lookup"><span data-stu-id="e0272-189">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="e0272-190">No se produce ningún otro efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="e0272-190">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e0272-191">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0272-191">Remarks</span></span>

<span data-ttu-id="e0272-192">La desfragmentación con conexión se controla a través de una configuración de parámetros, así como de esta API.</span><span class="sxs-lookup"><span data-stu-id="e0272-192">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="e0272-193">El valor predeterminado del parámetro System es JET_OnlineDefragAll, lo que significa que la desfragmentación está habilitada para todas las estructuras de datos compatibles.</span><span class="sxs-lookup"><span data-stu-id="e0272-193">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="e0272-194">Sin embargo, el uso de [JetSetSystemParameter](./jetsetsystemparameter-function.md)es posible deshabilitar la desfragmentación en línea o habilitarla de forma selectiva solo para los árboles de espacio de base de datos, solo para las bases de datos, archivos de streaming o cualquier combinación de estas opciones.</span><span class="sxs-lookup"><span data-stu-id="e0272-194">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="e0272-195">Si la configuración del sistema para la desfragmentación en línea es un valor obsoleto, **JetDefragment2** tratará la configuración como JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="e0272-195">If the system setting for on-line defragmentation is to an obsolete setting, **JetDefragment2** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="e0272-196">Puede haber como máximo una tarea que se ejecute para cada base de datos.</span><span class="sxs-lookup"><span data-stu-id="e0272-196">There can at most be one task running for each database.</span></span> <span data-ttu-id="e0272-197">La tarea se ejecuta como un subproceso en el proceso que hospeda ESE.</span><span class="sxs-lookup"><span data-stu-id="e0272-197">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="e0272-198">La sesión utilizada para iniciar la tarea de desfragmentación con conexión se puede utilizar posteriormente para las operaciones de base de datos mientras la tarea de desfragmentación continúa, porque la tarea de desfragmentación asigna su propia sesión.</span><span class="sxs-lookup"><span data-stu-id="e0272-198">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="e0272-199">La sesión determinada solo se usa para comprobar los permisos asociados a la sesión de inicio de la tarea y no se usa realmente para las propias operaciones de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="e0272-199">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e0272-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0272-200">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0272-201"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e0272-201"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e0272-202">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0272-202">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-203"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e0272-203"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e0272-204">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e0272-204">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-205"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e0272-205"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e0272-206">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="e0272-206">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-207"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="e0272-207"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e0272-208">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e0272-208">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0272-209"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e0272-209"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e0272-210">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e0272-210">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0272-211"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="e0272-211"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="e0272-212">Se implementa como <strong>JetDefragment2W</strong> (Unicode) y <strong>JetDefragment2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="e0272-212">Implemented as <strong>JetDefragment2W</strong> (Unicode) and <strong>JetDefragment2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e0272-213">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e0272-213">See Also</span></span>

[<span data-ttu-id="e0272-214">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e0272-214">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e0272-215">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e0272-215">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="e0272-216">JetCompact</span><span class="sxs-lookup"><span data-stu-id="e0272-216">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="e0272-217">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="e0272-217">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="e0272-218">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="e0272-218">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="e0272-219">JetStopService</span><span class="sxs-lookup"><span data-stu-id="e0272-219">JetStopService</span></span>](./jetstopservice-function.md)
