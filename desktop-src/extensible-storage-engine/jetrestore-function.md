---
description: 'Más información acerca de: JetRestore (función)'
title: Función JetRestore
TOCTitle: JetRestore Function
ms:assetid: cdfb8823-6260-46f2-adfc-77e2512a68fd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294093(v=EXCHG.10)
ms:contentKeyID: 32765708
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRestore
- JetRestoreW
- JetRestoreA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ed164bb6775150f9745cb0e6d9b158a5f03f146
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104004003"
---
# <a name="jetrestore-function"></a><span data-ttu-id="a719c-103">Función JetRestore</span><span class="sxs-lookup"><span data-stu-id="a719c-103">JetRestore Function</span></span>


<span data-ttu-id="a719c-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a719c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetrestore-function"></a><span data-ttu-id="a719c-105">Función JetRestore</span><span class="sxs-lookup"><span data-stu-id="a719c-105">JetRestore Function</span></span>

<span data-ttu-id="a719c-106">La función **JetRestore** restaura y recupera una copia de seguridad de streaming de una instancia, incluidas todas las bases de datos adjuntas.</span><span class="sxs-lookup"><span data-stu-id="a719c-106">The **JetRestore** function restores and recovers a streaming backup of an instance, including all the attached databases.</span></span> <span data-ttu-id="a719c-107">Esta función es principalmente para la compatibilidad con versiones anteriores de Windows 2000 y los motores de base de datos anteriores, donde solo se permite una instancia de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="a719c-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="a719c-108">En este caso, la instancia activa es la instancia de que se restaura.</span><span class="sxs-lookup"><span data-stu-id="a719c-108">In this case, the active instance is the instance that is restored.</span></span> <span data-ttu-id="a719c-109">Con **JetRestore**, no se puede especificar la ubicación de las bases de datos restauradas.</span><span class="sxs-lookup"><span data-stu-id="a719c-109">With **JetRestore**, the location for the restored databases cannot be specified.</span></span>

```cpp
JET_ERR JET_API JetRestore(
  __in          JET_PCSTR sz,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="a719c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a719c-110">Parameters</span></span>

<span data-ttu-id="a719c-111">*SZ*</span><span class="sxs-lookup"><span data-stu-id="a719c-111">*sz*</span></span>

<span data-ttu-id="a719c-112">La carpeta donde se encuentra la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a719c-112">The folder where the backup is located.</span></span> <span data-ttu-id="a719c-113">La copia de seguridad debe haberse generado mediante la función [JetBackup](./jetbackup-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a719c-113">The backup should have been generated using the [JetBackup](./jetbackup-function.md) function.</span></span>

<span data-ttu-id="a719c-114">*pfn*</span><span class="sxs-lookup"><span data-stu-id="a719c-114">*pfn*</span></span>

<span data-ttu-id="a719c-115">Puntero opcional a la función que se llamará como información de notificación sobre el progreso de la operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="a719c-115">The optional pointer to the function which will be called as notification information about the progress of the restore operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="a719c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a719c-116">Return Value</span></span>

<span data-ttu-id="a719c-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="a719c-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="a719c-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a719c-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a719c-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a719c-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="a719c-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a719c-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a719c-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a719c-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a719c-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a719c-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a719c-123">JET_errAlreadyInitialized</span><span class="sxs-lookup"><span data-stu-id="a719c-123">JET_errAlreadyInitialized</span></span></p></td>
<td><p><span data-ttu-id="a719c-124">No se pudo realizar la operación porque el motor ya está inicializado para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="a719c-124">The operation failed because the engine is already initialized for this instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a719c-125">JET_errInvalidLogSequence</span><span class="sxs-lookup"><span data-stu-id="a719c-125">JET_errInvalidLogSequence</span></span></p></td>
<td><p><span data-ttu-id="a719c-126">El conjunto de archivos de registro del conjunto de copia de seguridad y de la ruta de acceso del registro actual no coincide.</span><span class="sxs-lookup"><span data-stu-id="a719c-126">The set of log files from the backup set and from the current log path do not match.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a719c-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="a719c-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="a719c-128">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="a719c-128">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a719c-129">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="a719c-129">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="a719c-130">No se pudo realizar la operación porque algunas de las rutas de acceso proporcionadas no son válidas (ruta de acceso de copia de seguridad, ruta de acceso de destino, registro o ruta de acceso del sistema para la instancia).</span><span class="sxs-lookup"><span data-stu-id="a719c-130">The operation failed because some of paths provided are invalid (the backup path, the destination path, the log or system path for the instance).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a719c-131">JET_errPageSizeMismatch</span><span class="sxs-lookup"><span data-stu-id="a719c-131">JET_errPageSizeMismatch</span></span></p></td>
<td><p><span data-ttu-id="a719c-132">Se produjo un error en la operación porque el motor está configurado para usar un tamaño de página de base de datos (con <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) que no coincide con el tamaño de página de la base de datos utilizado para crear los archivos de registro de transacciones o las bases de datos asociadas a los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="a719c-132">The operation failed because the engine is configured to use a database page size (using <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> for <a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) that does not match the database page size used to create the transaction log files or the databases associated with the transaction log files.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a719c-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="a719c-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="a719c-134">No se pudo realizar la operación porque los parámetros modo de instancia única implícita (modo de compatibilidad de Windows 2000) y el motor ya están en modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="a719c-134">The operation failed because the parameters implied single instance mode (Windows 2000 compatibility mode) and the engine is already in multi-instance mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a719c-135">En caso de éxito, los archivos de base de datos del conjunto de copia de seguridad se restaurarán a su ubicación y la recuperación se ejecutará de forma que las bases de datos estén en un estado de coherencia transaccional limpio.</span><span class="sxs-lookup"><span data-stu-id="a719c-135">On success, database files from the backup set will be restored over to their location and recovery will be run such that the databases will be in a clean transactional consistency state.</span></span> <span data-ttu-id="a719c-136">La recuperación reproducirá los archivos de registro del conjunto de copia de seguridad y los archivos de registro de la ruta de acceso del registro si estos archivos existen.</span><span class="sxs-lookup"><span data-stu-id="a719c-136">Recovery will replay the log files from the backup set and the log files from the log path if such files do exists.</span></span> <span data-ttu-id="a719c-137">Esta recuperación producirá cambios en el archivo de punto de comprobación, en los archivos de registro de transacciones y en cualquier base de datos a la que hagan referencia esos archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="a719c-137">This recovery will result in changes to the checkpoint file, the transaction log files, and any databases referenced by those transaction log files.</span></span>

<span data-ttu-id="a719c-138">En caso de error, la instancia permanece en un estado no inicializado.</span><span class="sxs-lookup"><span data-stu-id="a719c-138">On failure, the instance remains in an uninitialized state.</span></span> <span data-ttu-id="a719c-139">Es probable que se haya cambiado el estado de los archivos de registro de transacciones y cualquier base de datos a la que hagan referencia los archivos de registro de transacciones al intentar inicializar la restauración y recuperar las bases de datos.</span><span class="sxs-lookup"><span data-stu-id="a719c-139">The state of the transaction log files and any databases referenced by those transaction log files will likely have been changed in the attempt to initialize the restore and recover the databases.</span></span>

#### <a name="remarks"></a><span data-ttu-id="a719c-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a719c-140">Remarks</span></span>

<span data-ttu-id="a719c-141">El proceso de recuperación volverá a construir las bases de datos adjuntas a la instancia durante la copia de seguridad y guardará los cambios en los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a719c-141">The recovery process will reconstruct the databases attached to the instance during the backup and save the changes back to the database files.</span></span> <span data-ttu-id="a719c-142">El resultado serán las bases de datos que son coherentes con las transacciones.</span><span class="sxs-lookup"><span data-stu-id="a719c-142">The result will be databases that are transaction consistent.</span></span> <span data-ttu-id="a719c-143">Si es posible, también guardará en la base de datos los cambios realizados desde que se realizó la copia de seguridad hasta que se haya producido el cambio más reciente en los registros de transacciones.</span><span class="sxs-lookup"><span data-stu-id="a719c-143">If possible, it will also save to the database the changes done since the backup was taken until the most recent change found in the transaction logs.</span></span> <span data-ttu-id="a719c-144">Esto sería posible si los registros de transacciones generados desde que se realizó la copia de seguridad siguen presentes en el directorio del registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="a719c-144">This would be possible if the transaction logs generated since the backup was taken are still present in the transaction log directory.</span></span> <span data-ttu-id="a719c-145">Tenga en cuenta que si se ha habilitado el registro circular para la instancia, los registros de transacciones generados se reutilizan de forma que la recuperación pueda guardar los cambios que tuvieron lugar en el momento de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a719c-145">Note that if circular logging was enabled for the instance, the transaction logs generated are reused such that the recovery will be able to save the changes which took place up to the backup moment.</span></span> <span data-ttu-id="a719c-146">En cualquier caso, es posible que este proceso tarde bastante tiempo si el número de archivos de registro de transacciones que se van a reproducir en las bases de datos es grande.</span><span class="sxs-lookup"><span data-stu-id="a719c-146">In any case, it is possible for this process to take quite some time if the number of transaction log files to replay against the databases is large.</span></span>

<span data-ttu-id="a719c-147">Se debe llamar a las funciones **JetRestore** en una instancia de antes de llamar a [JetInit](./jetinit-function.md) para esa instancia.</span><span class="sxs-lookup"><span data-stu-id="a719c-147">**JetRestore** functions must be called on an instance before [JetInit](./jetinit-function.md) is called for that instance.</span></span>

<span data-ttu-id="a719c-148">Dado que durante la recuperación se usará un número significativo de páginas de base de datos y registros de transacciones, hay una serie de errores completa que podrían ser devueltos por estas funciones.</span><span class="sxs-lookup"><span data-stu-id="a719c-148">Because during recovery a significant number of database pages and transaction logs will be used, there is an entire series of error which might be returned by these functions.</span></span> <span data-ttu-id="a719c-149">Estos errores pueden ser de errores de asignación de recursos temporales como Jet_errOutOfMemory a errores que representan daños físicos como JET_errReadVerifyFailure, JET_errLogFileCorrupt o JET_errBadPageLink.</span><span class="sxs-lookup"><span data-stu-id="a719c-149">Such errors can be from temporary resource allocation failures like Jet_errOutOfMemory to errors representing physical corruptions like JET_errReadVerifyFailure, JET_errLogFileCorrupt or JET_errBadPageLink.</span></span> <span data-ttu-id="a719c-150">Estos errores casi siempre están causados por problemas de hardware y, por tanto, no se pueden evitar.</span><span class="sxs-lookup"><span data-stu-id="a719c-150">These errors are almost always caused by hardware problems and thus cannot be avoided.</span></span> <span data-ttu-id="a719c-151">La administración de archivos indebidos se manifestará normalmente como JET_errMissingLogFile o JET_errAttachedDatabaseMismatch o JET_errDatabaseSharingViolation o JET_errInvalidLogSequence.</span><span class="sxs-lookup"><span data-stu-id="a719c-151">File mismanagement will manifest itself most often as JET_errMissingLogFile or JET_errAttachedDatabaseMismatch or JET_errDatabaseSharingViolation or JET_errInvalidLogSequence.</span></span> <span data-ttu-id="a719c-152">Estos errores son impidebles por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a719c-152">These errors are preventable by the application.</span></span> <span data-ttu-id="a719c-153">La aplicación debe tener cuidado de proteger el repositorio de estos archivos contra la manipulación de las fuerzas externas, como el usuario u otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a719c-153">The application must be careful to protect the repository of these files from manipulation by outside forces such as the user or other applications.</span></span> <span data-ttu-id="a719c-154">Si la aplicación desea destruir una instancia por completo, se deben eliminar todos los archivos asociados a la instancia.</span><span class="sxs-lookup"><span data-stu-id="a719c-154">If the application desires to destroy an instance entirely then all the files associated with the instance must be deleted.</span></span> <span data-ttu-id="a719c-155">Entre ellos se incluyen el archivo de punto de comprobación, los archivos de registro de transacciones y cualquier archivo de base de datos asociado a la instancia.</span><span class="sxs-lookup"><span data-stu-id="a719c-155">These include the checkpoint file, the transaction log files, and any database files attached to the instance.</span></span>

<span data-ttu-id="a719c-156">Los distintos pasos de la recuperación tendrán entradas del registro de eventos generadas que incluyen el progreso de la reproducción del registro de transacciones y el resultado final de la restauración.</span><span class="sxs-lookup"><span data-stu-id="a719c-156">The different steps of the recovery will have Event Log entries generated including the transaction log replay progress and the final result of the restore.</span></span>

#### <a name="requirements"></a><span data-ttu-id="a719c-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a719c-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a719c-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="a719c-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a719c-159">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="a719c-159">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a719c-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a719c-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a719c-161">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="a719c-161">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a719c-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a719c-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a719c-163">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="a719c-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a719c-164"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="a719c-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a719c-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a719c-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a719c-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="a719c-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a719c-167">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a719c-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a719c-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="a719c-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="a719c-169">Se implementa como <strong>JetRestoreW</strong> (Unicode) y <strong>JetRestoreA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="a719c-169">Implemented as <strong>JetRestoreW</strong> (Unicode) and <strong>JetRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a719c-170">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a719c-170">See Also</span></span>

[<span data-ttu-id="a719c-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a719c-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="a719c-172">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="a719c-172">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="a719c-173">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="a719c-173">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="a719c-174">JetBackup</span><span class="sxs-lookup"><span data-stu-id="a719c-174">JetBackup</span></span>](./jetbackup-function.md)  
[<span data-ttu-id="a719c-175">JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="a719c-175">JetBackupInstance</span></span>](./jetbackupinstance-function.md)  
[<span data-ttu-id="a719c-176">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="a719c-176">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="a719c-177">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="a719c-177">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
