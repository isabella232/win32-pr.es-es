---
description: 'Más información acerca de: JetDefragment (función)'
title: JetDefragment función)
TOCTitle: JetDefragment Function
ms:assetid: 8215fd00-f1b8-4ebd-8d55-9bce11d7dc9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269317(v=EXCHG.10)
ms:contentKeyID: 32765607
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDefragmentA
- JetDefragment
- JetDefragmentW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88495f90e726f8c28128a6456566124f23a17381
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361586"
---
# <a name="jetdefragment-function"></a><span data-ttu-id="9610f-103">JetDefragment función)</span><span class="sxs-lookup"><span data-stu-id="9610f-103">JetDefragment Function</span></span>


<span data-ttu-id="9610f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9610f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdefragment-function"></a><span data-ttu-id="9610f-105">JetDefragment función)</span><span class="sxs-lookup"><span data-stu-id="9610f-105">JetDefragment Function</span></span>

<span data-ttu-id="9610f-106">La función **JetDefragment** inicia y detiene las tareas de desfragmentación de bases de datos que mejoran la organización de datos en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="9610f-106">The **JetDefragment** function starts and stops database defragmentation tasks that improves data organization within a database.</span></span> <span data-ttu-id="9610f-107">Esto se hace para limitar el crecimiento de la base de datos mediante la asignación de disco existente de forma más eficaz en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9610f-107">This is done to limit database growth by using existing disk allocation more efficiently within the database.</span></span> <span data-ttu-id="9610f-108">También puede reducir el espacio de trabajo asegurándose de que los datos se empaquetan con mayor precisión.</span><span class="sxs-lookup"><span data-stu-id="9610f-108">It can also reduce working set by ensuring that data is more closely packed.</span></span> <span data-ttu-id="9610f-109">Por último, puede mejorar el rendimiento de la aplicación al acelerar las operaciones comunes a través de una mejor organización de datos.</span><span class="sxs-lookup"><span data-stu-id="9610f-109">Lastly, it can improve application performance by speeding common operations through better data organization.</span></span>

<span data-ttu-id="9610f-110">La desfragmentación de bases de datos es una operación en línea y no interrumpe la actividad normal de la base de datos, como operaciones de consulta o actualizaciones de datos.</span><span class="sxs-lookup"><span data-stu-id="9610f-110">Database defragmentation is an online operation and does not interrupt regular database activity, such as query operations or data updates.</span></span> <span data-ttu-id="9610f-111">**JetDefragment** tampoco realiza una copia de todos los datos existentes.</span><span class="sxs-lookup"><span data-stu-id="9610f-111">**JetDefragment** also does not make a copy of all existing data.</span></span> <span data-ttu-id="9610f-112">En su lugar, desfragmenta una base de datos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="9610f-112">Instead, it defragments a database in place.</span></span> <span data-ttu-id="9610f-113">Por último, **JetDefragment** recupera el espacio interno de la base de datos para su reutilización, pero no libera espacio sobrante en el sistema de archivos del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9610f-113">Lastly, **JetDefragment** recovers internal database space for re-use but does not release excess space to the operating system file system.</span></span>

<span data-ttu-id="9610f-114">El formato resultante de los datos puede ser mucho más eficaz, pero no suele ser óptimo.</span><span class="sxs-lookup"><span data-stu-id="9610f-114">The resulting format of the data can be much more efficient but is not generally optimal.</span></span> <span data-ttu-id="9610f-115">La desfragmentación se limita a liberar páginas de base de datos para que se vuelvan a usar, que contienen datos que ya se han eliminado lógicamente.</span><span class="sxs-lookup"><span data-stu-id="9610f-115">Defragmentation is limited to releasing database pages for re-use which contain data that has already been logically deleted.</span></span> <span data-ttu-id="9610f-116">La desfragmentación también hace que las páginas de base de datos estén disponibles para su reutilización en algunos casos mediante la combinación de datos de dos páginas cuando quepa en una sola página.</span><span class="sxs-lookup"><span data-stu-id="9610f-116">Defragmentation also makes database pages available for re-use in some cases by combining data from two pages when it can fit on a single page.</span></span>

<span data-ttu-id="9610f-117">Esta operación es diferente de [JetCompact](./jetcompact-function.md) , que realiza una copia de una base de datos de solo lectura en una forma muy óptima.</span><span class="sxs-lookup"><span data-stu-id="9610f-117">This operation is different from [JetCompact](./jetcompact-function.md) which makes a copy of a read-only database into a highly optimal form.</span></span>

```cpp
    JET_ERR JET_API JetDefragment(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __out_opt     unsigned long* pcPasses,
      __out_opt     unsigned long* pcSeconds,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9610f-118">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9610f-118">Parameters</span></span>

<span data-ttu-id="9610f-119">*sesid*</span><span class="sxs-lookup"><span data-stu-id="9610f-119">*sesid*</span></span>

<span data-ttu-id="9610f-120">Sesión que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="9610f-120">The session to use for this call.</span></span>

<span data-ttu-id="9610f-121">*DBID*</span><span class="sxs-lookup"><span data-stu-id="9610f-121">*dbid*</span></span>

<span data-ttu-id="9610f-122">Base de datos que se va a desfragmentar.</span><span class="sxs-lookup"><span data-stu-id="9610f-122">The database that will be defragmented.</span></span>

<span data-ttu-id="9610f-123">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="9610f-123">*szTableName*</span></span>

<span data-ttu-id="9610f-124">Parámetro sin usar.</span><span class="sxs-lookup"><span data-stu-id="9610f-124">Unused parameter.</span></span> <span data-ttu-id="9610f-125">La desfragmentación se realiza para toda la base de datos descrita por el identificador de base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="9610f-125">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<span data-ttu-id="9610f-126">*pcPasses*</span><span class="sxs-lookup"><span data-stu-id="9610f-126">*pcPasses*</span></span>

<span data-ttu-id="9610f-127">Al iniciar una tarea de desfragmentación con conexión, este parámetro de entrada establece el número máximo de pasos de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-127">When starting an online defragmentation task, this input parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="9610f-128">Al detener una tarea de desfragmentación con conexión, este búfer de salida se establece en el número de pasos realizados.</span><span class="sxs-lookup"><span data-stu-id="9610f-128">When stopping an online defragmentation task, this output buffer is set to the number of passes performed.</span></span>

<span data-ttu-id="9610f-129">Cuando este parámetro se establece en NULL, el número de pases de desfragmentación en línea es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="9610f-129">When this parameter is set to NULL, the number of online defragmentation passes is unlimited.</span></span>

<span data-ttu-id="9610f-130">*pcSeconds*</span><span class="sxs-lookup"><span data-stu-id="9610f-130">*pcSeconds*</span></span>

<span data-ttu-id="9610f-131">Al iniciar una tarea de desfragmentación con conexión, este parámetro de entrada establece el tiempo máximo de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-131">When starting an online defragmentation task, this input parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="9610f-132">Al detener una tarea de desfragmentación en línea, este búfer de salida se establece en el período de tiempo utilizado para la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-132">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<span data-ttu-id="9610f-133">Cuando este parámetro se establece en NULL o si *pcSeconds* apunta a un valor negativo, el tiempo máximo para la desfragmentación es ilimitado.</span><span class="sxs-lookup"><span data-stu-id="9610f-133">When this parameter is set to NULL or if *pcSeconds* points to a negative value, the maximum time for defragmentation is unlimited.</span></span>

<span data-ttu-id="9610f-134">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9610f-134">*grbit*</span></span>

<span data-ttu-id="9610f-135">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="9610f-135">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9610f-136">Value</span><span class="sxs-lookup"><span data-stu-id="9610f-136">Value</span></span></p></th>
<th><p><span data-ttu-id="9610f-137">Significado</span><span class="sxs-lookup"><span data-stu-id="9610f-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9610f-138">JET_bitDefragmentAvailSpaceTreesOnly</span><span class="sxs-lookup"><span data-stu-id="9610f-138">JET_bitDefragmentAvailSpaceTreesOnly</span></span></p></td>
<td><p><span data-ttu-id="9610f-139">Desfragmenta la parte de espacio disponible de la asignación de espacio de la base de datos de ESE.</span><span class="sxs-lookup"><span data-stu-id="9610f-139">Defragments the available space portion of ESE database space allocation.</span></span> <span data-ttu-id="9610f-140">El espacio de la base de datos se divide en dos tipos, espacio de propiedad y espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="9610f-140">Database space is divided into two types, owned space and available space.</span></span> <span data-ttu-id="9610f-141">El espacio de propiedad se asigna a una tabla o un índice mientras que el espacio disponible está listo para su uso en la tabla o el índice, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9610f-141">Owned space is allocated to a table or index while available space is ready for use within the table or index, respectively.</span></span> <span data-ttu-id="9610f-142">El espacio disponible es mucho más dinámico en el comportamiento y requiere una desfragmentación en línea más que el espacio de propiedad o los datos de la tabla o el índice.</span><span class="sxs-lookup"><span data-stu-id="9610f-142">Available space is much more dynamic in behavior and requires on-line defragmentation more so than owned space or table or index data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-143">JET_bitDefragmentBatchStart</span><span class="sxs-lookup"><span data-stu-id="9610f-143">JET_bitDefragmentBatchStart</span></span></p></td>
<td><p><span data-ttu-id="9610f-144">Inicia una nueva tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-144">Starts a new defragmentation task.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-145">JET_bitDefragmentBatchStop</span><span class="sxs-lookup"><span data-stu-id="9610f-145">JET_bitDefragmentBatchStop</span></span></p></td>
<td><p><span data-ttu-id="9610f-146">Detiene una tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-146">Stops a defragmentation task.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9610f-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9610f-147">Return Value</span></span>

<span data-ttu-id="9610f-148">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="9610f-148">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9610f-149">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9610f-149">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9610f-150">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9610f-150">Return code</span></span></p></th>
<th><p><span data-ttu-id="9610f-151">Descripción</span><span class="sxs-lookup"><span data-stu-id="9610f-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9610f-152">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9610f-152">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9610f-153">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9610f-153">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-154">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9610f-154">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9610f-155">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9610f-155">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-156">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="9610f-156">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9610f-157">La base de datos elegida para la desfragmentación es de solo lectura y no se puede actualizar de ningún modo, incluida la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-157">The database chosen for defragmentation is read only and cannot be updated in any way, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span><span class="sxs-lookup"><span data-stu-id="9610f-158">JET_errDistributedTransactionAlreadyPreparedToCommit</span></span></p></td>
<td><p><span data-ttu-id="9610f-159">La sesión determinada está en el estado preparado para confirmar y no puede iniciar nuevas actualizaciones hasta que la transacción actual se confirma o se revierte.</span><span class="sxs-lookup"><span data-stu-id="9610f-159">The given session is in the prepared to commit state, and cannot begin new updates until the current transaction is committed or rolled back.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-160">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9610f-160">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9610f-161">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="9610f-161">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="9610f-162">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9610f-162">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-163">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="9610f-163">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="9610f-164">El identificador de base de datos especificado no coincide con una base de datos conocida en la instancia.</span><span class="sxs-lookup"><span data-stu-id="9610f-164">The given database ID does not match a known database in the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-165">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9610f-165">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9610f-166">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9610f-166">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-167">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9610f-167">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9610f-168">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9610f-168">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-169">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="9610f-169">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="9610f-170">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="9610f-170">The same session cannot be used for more than one thread at the same time.</span></span> <span data-ttu-id="9610f-171">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9610f-171">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-172">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9610f-172">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9610f-173">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9610f-173">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-174">JET_errTransReadOnly</span><span class="sxs-lookup"><span data-stu-id="9610f-174">JET_errTransReadOnly</span></span></p></td>
<td><p><span data-ttu-id="9610f-175">La sesión determinada solo tiene privilegios de solo lectura y no puede iniciar una tarea que pueda realizar una actualización, incluida la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-175">The given session has read-only privileges only and cannot start a task that may perform an update, including defragmentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-176">JET_errVersionStoreOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="9610f-176">JET_errVersionStoreOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="9610f-177">Este error se producirá cuando el tamaño configurado del almacén de versiones no sea suficiente para contener todas las actualizaciones pendientes.</span><span class="sxs-lookup"><span data-stu-id="9610f-177">This error will occur when the configured size of the version store is insufficient to hold all outstanding updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-178">JET_wrnDefragAlreadyRunning</span><span class="sxs-lookup"><span data-stu-id="9610f-178">JET_wrnDefragAlreadyRunning</span></span></p></td>
<td><p><span data-ttu-id="9610f-179">Se ha pasado la opción de JET_bitDefragmentBatchStart pero una tarea de desfragmentación ya está ejecutando la desfragmentación en la base de datos dada.</span><span class="sxs-lookup"><span data-stu-id="9610f-179">The JET_bitDefragmentBatchStart option has been passed but a defragmentation task is already running defragmentation on the given database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-180">JET_wrnDefragNotRunning</span><span class="sxs-lookup"><span data-stu-id="9610f-180">JET_wrnDefragNotRunning</span></span></p></td>
<td><p><span data-ttu-id="9610f-181">Se pasó la opción de JET_bitDefragmentBatchStop, pero no se está ejecutando ninguna tarea de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-181">The JET_bitDefragmentBatchStop option has been passed, but no defragmentation task is currently running.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9610f-182">Si se ejecuta correctamente, se realiza la acción solicitada de iniciar una tarea de desfragmentación para un determinado dato con opciones determinadas, o bien se realiza la acción de detener una tarea de desfragmentación existente.</span><span class="sxs-lookup"><span data-stu-id="9610f-182">On success, the requested action of either starting a defragmentation task for a given data with given options is performed, or the action of stopping an existing defragmentation task is performed.</span></span>

<span data-ttu-id="9610f-183">En caso de error, no se realiza la acción solicitada de iniciar o detener un trabajo de desfragmentación en línea.</span><span class="sxs-lookup"><span data-stu-id="9610f-183">On failure, the requested action of either starting or stopping an online defragmentation job is not done.</span></span> <span data-ttu-id="9610f-184">No se produce ningún otro efecto secundario.</span><span class="sxs-lookup"><span data-stu-id="9610f-184">No other side effects occur.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9610f-185">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9610f-185">Remarks</span></span>

<span data-ttu-id="9610f-186">La desfragmentación con conexión se controla a través de una configuración de parámetros, así como de esta API.</span><span class="sxs-lookup"><span data-stu-id="9610f-186">Online defragmentation is controlled both by a parameter setting, as well as by this API.</span></span> <span data-ttu-id="9610f-187">El valor predeterminado del parámetro System es JET_OnlineDefragAll, lo que significa que la desfragmentación está habilitada para todas las estructuras de datos compatibles.</span><span class="sxs-lookup"><span data-stu-id="9610f-187">The default system parameter value is JET_OnlineDefragAll, which means defragmentation is enabled for all supported data structures.</span></span> <span data-ttu-id="9610f-188">Sin embargo, el uso de [JetSetSystemParameter](./jetsetsystemparameter-function.md)es posible deshabilitar la desfragmentación en línea o habilitarla de forma selectiva solo para los árboles de espacio de base de datos, solo para las bases de datos, archivos de streaming o cualquier combinación de estas opciones.</span><span class="sxs-lookup"><span data-stu-id="9610f-188">However, using [JetSetSystemParameter](./jetsetsystemparameter-function.md), it is possible to disable online defragmentation, or to selectively enable it for database space trees only, databases only, streaming files only or any combination of these options.</span></span> <span data-ttu-id="9610f-189">Si la configuración del sistema para desfragmentación en línea se establece en una configuración obsoleta, **JetDefragment** tratará la configuración como JET_OnlineDefragAll.</span><span class="sxs-lookup"><span data-stu-id="9610f-189">If the system setting for online defragmentation is set to an obsolete setting, **JetDefragment** will treat the setting as JET_OnlineDefragAll.</span></span>

<span data-ttu-id="9610f-190">Puede haber como máximo una tarea que se ejecute para cada base de datos.</span><span class="sxs-lookup"><span data-stu-id="9610f-190">There can at most be one task running for each database.</span></span> <span data-ttu-id="9610f-191">La tarea se ejecuta como un subproceso en el proceso que hospeda ESE.</span><span class="sxs-lookup"><span data-stu-id="9610f-191">The task runs as a thread in the process hosting ESE.</span></span>

<span data-ttu-id="9610f-192">La sesión utilizada para iniciar la tarea de desfragmentación con conexión se puede utilizar posteriormente para las operaciones de base de datos mientras la tarea de desfragmentación continúa, porque la tarea de desfragmentación asigna su propia sesión.</span><span class="sxs-lookup"><span data-stu-id="9610f-192">The session used to start the online defragmentation task can be subsequently used for database operations while the defragmentation task continues, because the defragmentation task allocates its own session.</span></span> <span data-ttu-id="9610f-193">La sesión determinada solo se usa para comprobar los permisos asociados a la sesión de inicio de la tarea y no se usa realmente para las propias operaciones de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="9610f-193">The given session is only used to check the permissions associated with the task starting session and is not actually used for the defragmentation operations themselves.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9610f-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9610f-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9610f-195"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9610f-195"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9610f-196">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9610f-196">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-197"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9610f-197"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9610f-198">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9610f-198">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-199"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9610f-199"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9610f-200">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="9610f-200">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-201"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="9610f-201"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9610f-202">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9610f-202">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9610f-203"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9610f-203"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9610f-204">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9610f-204">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9610f-205"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="9610f-205"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="9610f-206">Se implementa como <strong>JetDefragmentW</strong> (Unicode) y <strong>JetDefragmentA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="9610f-206">Implemented as <strong>JetDefragmentW</strong> (Unicode) and <strong>JetDefragmentA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9610f-207">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9610f-207">See Also</span></span>

[<span data-ttu-id="9610f-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9610f-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9610f-209">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="9610f-209">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="9610f-210">JetCompact</span><span class="sxs-lookup"><span data-stu-id="9610f-210">JetCompact</span></span>](./jetcompact-function.md)  
[<span data-ttu-id="9610f-211">JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="9610f-211">JetDefragment2</span></span>](./jetdefragment2-function.md)  
[<span data-ttu-id="9610f-212">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="9610f-212">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="9610f-213">JetStopService</span><span class="sxs-lookup"><span data-stu-id="9610f-213">JetStopService</span></span>](./jetstopservice-function.md)
