---
description: 'Más información acerca de: JetRestore2 (función)'
title: Función JetRestore2
TOCTitle: JetRestore2 Function
ms:assetid: 7f7fc2e3-727a-43e4-8497-64ff56d92b9f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269313(v=EXCHG.10)
ms:contentKeyID: 32765603
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore2
- JetRestore2A
- JetRestore2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb297aac0bc26e50bba519206eff346abb7943c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707180"
---
# <a name="jetrestore2-function"></a><span data-ttu-id="fe6f6-103">Función JetRestore2</span><span class="sxs-lookup"><span data-stu-id="fe6f6-103">JetRestore2 Function</span></span>


<span data-ttu-id="fe6f6-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fe6f6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore2-function"></a><span data-ttu-id="fe6f6-105">Función JetRestore2</span><span class="sxs-lookup"><span data-stu-id="fe6f6-105">JetRestore2 Function</span></span>

<span data-ttu-id="fe6f6-106">**JetRestore2** restaura y recupera una copia de seguridad de streaming de una instancia, incluidas todas las bases de datos adjuntas.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-106">The **JetRestore2** restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="fe6f6-107">Esta función es principalmente para la compatibilidad con versiones anteriores de Windows 2000 y los motores de base de datos anteriores, donde solo se permite una instancia de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="fe6f6-108">En este caso, la instancia activa es la instancia de que se restaura.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-108">In this case, the active instance is the instance that is restored.</span></span>

```cpp
    JET_ERR JET_API JetRestore2(
      __in          JET_PCSTR sz,
      __in_opt      JET_PCSTR szDest,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="fe6f6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe6f6-109">Parameters</span></span>

<span data-ttu-id="fe6f6-110">*SZ*</span><span class="sxs-lookup"><span data-stu-id="fe6f6-110">*sz*</span></span>

<span data-ttu-id="fe6f6-111">La carpeta donde se encuentra la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-111">The folder where the backup is located.</span></span> <span data-ttu-id="fe6f6-112">La copia de seguridad debe haberse generado mediante las API de [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="fe6f6-112">The backup should have been generated using the [JetBackup](./jetbackup-function.md) APIs.</span></span>

<span data-ttu-id="fe6f6-113">*szDest*</span><span class="sxs-lookup"><span data-stu-id="fe6f6-113">*szDest*</span></span>

<span data-ttu-id="fe6f6-114">Nombre de la carpeta donde se copiarán y recuperarán los archivos de base de datos del conjunto de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-114">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="fe6f6-115">Si se establece en NULL (que es el caso del [JetRestore](./jetrestore-function.md)heredado), los archivos de la base de datos se copiarán y recuperarán en su ubicación original.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-115">If this is set to NULL (which is the case for the legacy [JetRestore](./jetrestore-function.md)), the database files will be copied and recovered to their original location.</span></span>

<span data-ttu-id="fe6f6-116">*pfn*</span><span class="sxs-lookup"><span data-stu-id="fe6f6-116">*pfn*</span></span>

<span data-ttu-id="fe6f6-117">Puntero opcional a la función que se llamará como información de notificación sobre el progreso de la operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-117">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="fe6f6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe6f6-118">Return Value</span></span>

<span data-ttu-id="fe6f6-119">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fe6f6-120">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fe6f6-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe6f6-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fe6f6-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="fe6f6-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe6f6-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fe6f6-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-124">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-125">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="fe6f6-125">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-126">No se pudo realizar la operación porque el motor ya está inicializado para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-126">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-127">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="fe6f6-127">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-128">El conjunto de archivos de registro del conjunto de copia de seguridad y de la ruta de acceso del registro actual no coincide.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-128">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fe6f6-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-130">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-130">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="fe6f6-131">Este error lo devolverá <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> cuando el motor está en modo de varias instancias y pinstance hace referencia a una instancia no válida de Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-131">This error will be returned by <a href="gg269306(v=exchg.10).md">JetRestoreInstance</a> when the engine is in multi-instance mode and pinstance refers to an invalid instance Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-132">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="fe6f6-132">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-133">No se pudo realizar la operación porque algunas de las rutas de acceso proporcionadas no son válidas (ruta de acceso de copia de seguridad, ruta de acceso de destino, registro o ruta de acceso del sistema para la instancia).</span><span class="sxs-lookup"><span data-stu-id="fe6f6-133">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-134">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="fe6f6-134">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-135">Se produjo un error en la operación porque el motor está configurado para usar un tamaño de página de base de datos (con <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) que no coincide con el tamaño de página de la base de datos utilizado para crear los archivos de registro de transacciones o las bases de datos asociadas a los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-135">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-136">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="fe6f6-136">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="fe6f6-137">No se pudo realizar la operación porque los parámetros modo de instancia única implícita (modo de compatibilidad de Windows 2000) y el motor ya están en modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-137">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe6f6-138">En caso de éxito, los archivos de base de datos del conjunto de copia de seguridad se restaurarán a su ubicación y la recuperación se ejecutará de forma que las bases de datos estén en un estado de coherencia transaccional limpio.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-138">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="fe6f6-139">La recuperación reproducirá los archivos de registro del conjunto de copia de seguridad y los archivos de registro de la ruta de acceso del registro si estos archivos existen.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-139">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="fe6f6-140">Esta recuperación producirá cambios en el archivo de punto de comprobación, en los archivos de registro de transacciones y en cualquier base de datos a la que hagan referencia esos archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-140">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="fe6f6-141">En caso de error, la instancia permanece en un estado no inicializado.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-141">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="fe6f6-142">Es probable que se haya cambiado el estado de los archivos de registro de transacciones y cualquier base de datos a la que hagan referencia los archivos de registro de transacciones al intentar inicializar la restauración y recuperar las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-142">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fe6f6-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe6f6-143">Remarks</span></span>

<span data-ttu-id="fe6f6-144">El proceso de recuperación volverá a construir las bases de datos adjuntas a la instancia durante la copia de seguridad y guardará los cambios en los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-144">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="fe6f6-145">El resultado serán las bases de datos que son coherentes con las transacciones.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-145">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="fe6f6-146">Si es posible, también guardará en la base de datos los cambios realizados desde que se realizó la copia de seguridad hasta que se haya producido el cambio más reciente en los registros de transacciones.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-146">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="fe6f6-147">Esto sería posible si los registros de transacciones generados desde que se realizó la copia de seguridad siguen presentes en el directorio del registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-147">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="fe6f6-148">Tenga en cuenta que si se ha habilitado el registro circular para la instancia, los registros de transacciones generados se reutilizan de forma que la recuperación pueda guardar los cambios que tuvieron lugar en el momento de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-148">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="fe6f6-149">En cualquier caso, es posible que este proceso tarde bastante tiempo si el número de archivos de registro de transacciones que se van a reproducir en las bases de datos es grande.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-149">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="fe6f6-150">Se debe llamar a las funciones [JetRestore](./jetrestore-function.md) en una instancia de antes de llamar a [JetInit](./jetinit-function.md) para esa instancia.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-150">[JetRestore](./jetrestore-function.md) functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="fe6f6-151">Dado que durante la recuperación se usará un número significativo de páginas de base de datos y registros de transacciones, hay una serie de errores completa que podrían ser devueltos por estas funciones.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-151">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="fe6f6-152">Estos errores pueden ser de errores de asignación de recursos temporales como Jet_errOutOfMemory a errores que representan daños físicos como JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-152">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="fe6f6-153">Estos errores casi siempre están causados por problemas de hardware y, por tanto, no se pueden evitar.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-153">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="fe6f6-154">La administración de archivos indebidos se manifestará normalmente como JET_errMissingLogFile o JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-154">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="fe6f6-155">Estos errores son impidebles por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-155">These errors are preventable by the application.</span></span> <span data-ttu-id="fe6f6-156">La aplicación debe tener cuidado de proteger el repositorio de estos archivos contra la manipulación de las fuerzas externas, como el usuario u otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-156">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="fe6f6-157">Si la aplicación desea destruir una instancia por completo, se deben eliminar todos los archivos asociados a la instancia.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-157">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="fe6f6-158">Entre ellos se incluyen el archivo de punto de comprobación, los archivos de registro de transacciones y cualquier archivo de base de datos asociado a la instancia.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-158">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="fe6f6-159">Los distintos pasos de la recuperación tendrán entradas del registro de eventos generadas que incluyen el progreso de la reproducción del registro de transacciones y el resultado final de la restauración.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-159">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fe6f6-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe6f6-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-161"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-161"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-162">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-162">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-163"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-164">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-164">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-165"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-165"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-166">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-167"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-167"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-168">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-168">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe6f6-169"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-169"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-170">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6f6-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe6f6-171"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fe6f6-171"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fe6f6-172">Se implementa como <strong>JetRestore2W</strong> (Unicode) y <strong>JetRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fe6f6-172">Implemented as <strong>JetRestore2W</strong> (Unicode) and <strong>JetRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fe6f6-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fe6f6-173">See Also</span></span>

[<span data-ttu-id="fe6f6-174">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fe6f6-174">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fe6f6-175">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fe6f6-175">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fe6f6-176">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="fe6f6-176">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="fe6f6-177">JetBackup</span><span class="sxs-lookup"><span data-stu-id="fe6f6-177">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="fe6f6-178">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="fe6f6-178">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="fe6f6-179">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="fe6f6-179">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="fe6f6-180">JetInit</span><span class="sxs-lookup"><span data-stu-id="fe6f6-180">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="fe6f6-181">JetRestore</span><span class="sxs-lookup"><span data-stu-id="fe6f6-181">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="fe6f6-182">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="fe6f6-182">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="fe6f6-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="fe6f6-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
