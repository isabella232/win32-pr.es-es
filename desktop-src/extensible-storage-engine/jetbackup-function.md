---
description: 'Más información acerca de: JetBackup (función)'
title: Función JetBackup
TOCTitle: JetBackup Function
ms:assetid: afff995f-378a-4e67-b522-d5eafcbad57e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294058(v=EXCHG.10)
ms:contentKeyID: 32765673
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupA
- JetBackup
- JetBackupW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f225053df36ebe98bc890a8e036d84ee31b6b154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717169"
---
# <a name="jetbackup-function"></a><span data-ttu-id="d39bd-103">Función JetBackup</span><span class="sxs-lookup"><span data-stu-id="d39bd-103">JetBackup Function</span></span>


<span data-ttu-id="d39bd-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d39bd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackup-function"></a><span data-ttu-id="d39bd-105">Función JetBackup</span><span class="sxs-lookup"><span data-stu-id="d39bd-105">JetBackup Function</span></span>

<span data-ttu-id="d39bd-106">La función **JetBackup** crea una copia de seguridad de la base de datos mientras la base de datos está en línea.</span><span class="sxs-lookup"><span data-stu-id="d39bd-106">The **JetBackup** function creates a backup of the database while the database is online.</span></span> <span data-ttu-id="d39bd-107">Esta función es principalmente para la compatibilidad con versiones anteriores de Windows 2000 y los motores de base de datos anteriores, donde solo se permite una instancia de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="d39bd-107">This function is primarily for backwards compatibility with Windows 2000 and earlier database engines, where only one instance of a database is allowed.</span></span> <span data-ttu-id="d39bd-108">En este caso, la instancia activa es la instancia de la que se realiza una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-108">In this case, the active instance is the instance that is backed up.</span></span>

```cpp
    JET_ERR JET_API JetBackup(
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="d39bd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d39bd-109">Parameters</span></span>

<span data-ttu-id="d39bd-110">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="d39bd-110">*szBackupPath*</span></span>

<span data-ttu-id="d39bd-111">Directorio en el que se almacena la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-111">The directory where the backup is stored.</span></span> <span data-ttu-id="d39bd-112">Si la ruta de acceso de copia de seguridad es NULL, la función truncará los registros, si es posible.</span><span class="sxs-lookup"><span data-stu-id="d39bd-112">If the backup path is NULL, the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="d39bd-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d39bd-113">*grbit*</span></span>

<span data-ttu-id="d39bd-114">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="d39bd-114">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d39bd-115">Value</span><span class="sxs-lookup"><span data-stu-id="d39bd-115">Value</span></span></p></th>
<th><p><span data-ttu-id="d39bd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d39bd-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-117">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="d39bd-117">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="d39bd-118">Crea una copia de seguridad completa de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d39bd-118">Creates a full backup of the database.</span></span> <span data-ttu-id="d39bd-119">Esto permite conservar una copia de seguridad existente en el mismo directorio si se produce un error en la nueva copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-119">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-120">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="d39bd-120">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="d39bd-121">Crea una copia de seguridad incremental en lugar de una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="d39bd-121">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="d39bd-122">Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</span><span class="sxs-lookup"><span data-stu-id="d39bd-122">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d39bd-123">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="d39bd-123">*pfnStatus*</span></span>

<span data-ttu-id="d39bd-124">Puntero a la función de devolución de llamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , que proporciona información de notificación sobre el progreso de la operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-124">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="d39bd-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d39bd-125">Return Value</span></span>

<span data-ttu-id="d39bd-126">La función devuelve uno de los códigos de error de [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="d39bd-126">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="d39bd-127">A continuación se muestran los elementos que se devuelven con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="d39bd-127">The following are the most commonly returned.</span></span> <span data-ttu-id="d39bd-128">(Para obtener una lista completa de los errores de esta API, consulte [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md)).</span><span class="sxs-lookup"><span data-stu-id="d39bd-128">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d39bd-129">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d39bd-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="d39bd-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d39bd-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d39bd-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d39bd-132">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d39bd-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-133">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="d39bd-133">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="d39bd-134">Ya hay una copia de seguridad en curso para la misma instancia.</span><span class="sxs-lookup"><span data-stu-id="d39bd-134">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="d39bd-135">No se permiten varias copias de seguridad al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d39bd-135">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-136">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="d39bd-136">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="d39bd-137">La instancia todavía no está lista para la copia de seguridad mientras se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="d39bd-137">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-138">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="d39bd-138">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="d39bd-139">No se puede completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="d39bd-139">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-140">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="d39bd-140">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="d39bd-141">No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="d39bd-141">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="d39bd-142"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d39bd-142"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-143">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="d39bd-143">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="d39bd-144">No se permite una copia de seguridad incremental si el registro circular está activado.</span><span class="sxs-lookup"><span data-stu-id="d39bd-144">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-145">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="d39bd-145">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="d39bd-146">Las opciones especificadas no son válidas.</span><span class="sxs-lookup"><span data-stu-id="d39bd-146">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-147">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d39bd-147">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d39bd-148">Se pasó un parámetro no válido a la API.</span><span class="sxs-lookup"><span data-stu-id="d39bd-148">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-149">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="d39bd-149">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="d39bd-150">La ruta de acceso de destino no existe.</span><span class="sxs-lookup"><span data-stu-id="d39bd-150">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-151">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="d39bd-151">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="d39bd-152">La instancia se está ejecutando sin registro.</span><span class="sxs-lookup"><span data-stu-id="d39bd-152">The instance is running without logging.</span></span> <span data-ttu-id="d39bd-153">No se permite ninguna copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-153">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-154">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="d39bd-154">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="d39bd-155">Se produjo un error de comprobación de la suma de comprobación en un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="d39bd-155">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-156">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="d39bd-156">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="d39bd-157">El registro de la instancia es temporal o está deshabilitado permanentemente debido a un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="d39bd-157">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="d39bd-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="d39bd-159">No se puede completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d39bd-159">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-160">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="d39bd-160">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="d39bd-161">Se produjo un error de comprobación de la suma de comprobación en una página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d39bd-161">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="d39bd-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="d39bd-163">No se puede completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d39bd-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-164">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="d39bd-164">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="d39bd-165">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d39bd-165">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="d39bd-166"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d39bd-166"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-167">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="d39bd-167">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="d39bd-168">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="d39bd-168">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d39bd-169">Si la función se ejecuta correctamente, todos los archivos necesarios para una restauración hasta el momento de la copia de seguridad se incluirán en el directorio de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-169">If the function succeeds, all the files needed for a restore up to the moment of the backup will be contained in the backup directory.</span></span> <span data-ttu-id="d39bd-170">Si se trata de una copia de seguridad completa, los archivos serán los archivos de base de datos y los archivos de registro necesarios para poner la base de datos en un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="d39bd-170">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="d39bd-171">Si se trata de una copia de seguridad incremental, solo se agregarán archivos de registro a los directorios, pero los archivos ya existentes (archivos de registro y bases de datos), junto con los nuevos archivos de registro, se podrán restaurar para devolver la base de datos al estado en que se encontraba en el momento en que comenzó la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-171">If this is an incremental backup, only log files will be added to the directories, but the already existing files (databases and log files), together with the new log files, will be able to be restored to bring the database back to the state it was in at the moment that the backup began.</span></span>

<span data-ttu-id="d39bd-172">Como efecto secundario de la copia de seguridad, se truncarán los archivos de registro que ya no sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="d39bd-172">As a side effect of the backup, the log files which are no longer needed will be truncated.</span></span>

<span data-ttu-id="d39bd-173">Al mismo tiempo, los encabezados de la base de datos se actualizarán con la información cuando se realizó la última copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-173">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="d39bd-174">Si se produce un error en la función, no habrá ningún archivo en el destino del directorio de copia de seguridad, por lo que no será posible realizar ninguna restauración.</span><span class="sxs-lookup"><span data-stu-id="d39bd-174">If the function fails, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="d39bd-175">Al mismo tiempo, los archivos de registro actuales no se truncarán.</span><span class="sxs-lookup"><span data-stu-id="d39bd-175">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d39bd-176">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d39bd-176">Remarks</span></span>

<span data-ttu-id="d39bd-177">Los distintos pasos de la copia de seguridad tendrán entradas del registro de eventos generadas, incluidos los nombres de archivo, el truncamiento del registro y el resultado final de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-177">The different steps of the backup will have Event Log entries generated, including the file names, the log truncation, and the final result of the backup.</span></span>

<span data-ttu-id="d39bd-178">Las copias de seguridad incrementales solo son posibles después de realizar una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="d39bd-178">Incremental backups are possible only after a full backup was taken.</span></span> <span data-ttu-id="d39bd-179">Además, solo se pueden realizar copias de seguridad incrementales si el registro circular está desactivado.</span><span class="sxs-lookup"><span data-stu-id="d39bd-179">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="d39bd-180">Se recomienda que el directorio de copia de seguridad no contenga ningún archivo que no sea el utilizado en la copia de seguridad o que haya agregado una copia de seguridad correcta anterior.</span><span class="sxs-lookup"><span data-stu-id="d39bd-180">It is recommended that the backup directory should not contain any files other than the one used in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="d39bd-181">El directorio de copia de seguridad debe existir a menos que se establezca el parámetro *JET_paramCreatePathIfNotExist* para la instancia.</span><span class="sxs-lookup"><span data-stu-id="d39bd-181">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="d39bd-182">Para obtener más información, vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d39bd-182">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="d39bd-183">La copia de seguridad realizará una comprobación de suma de comprobación en todas las páginas de base de datos usadas y, a partir de Windows Server 2003, también en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="d39bd-183">The backup will do a checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="d39bd-184">Esto ofrece una oportunidad para estimar el estado de la base de datos, incluso para las páginas que no se leen durante las operaciones normales.</span><span class="sxs-lookup"><span data-stu-id="d39bd-184">This gives an opportunity to estimate the health of the database, even for pages which are not read during normal operations.</span></span> <span data-ttu-id="d39bd-185">Si se encuentra algún daño de este tipo, se producirá un error en la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d39bd-185">If any such corruption is encountered, the backup will fail.</span></span>

<span data-ttu-id="d39bd-186">Durante la copia de seguridad, se completará el archivo de registro actual y se generará un nuevo registro.</span><span class="sxs-lookup"><span data-stu-id="d39bd-186">During the backup, the current log file will be finished and a new log will be generated.</span></span> <span data-ttu-id="d39bd-187">De esta manera, todos los archivos de registro necesarios se pueden copiar, ya que el registro actual ya no estará en uso.</span><span class="sxs-lookup"><span data-stu-id="d39bd-187">This way, all of the necessary log files can be copies, because the current log will not be in use anymore.</span></span>

<span data-ttu-id="d39bd-188">Se recomienda encarecidamente que la copia de seguridad no se use para ningún propósito que no sea la copia de seguridad y restauración en el nivel de motor.</span><span class="sxs-lookup"><span data-stu-id="d39bd-188">It is strongly recommended that the backup not be used for any purpose other than the backup and restore at the engine level.</span></span> <span data-ttu-id="d39bd-189">Esto minimizará la posibilidad de obtener errores durante las operaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="d39bd-189">This will minimize the chance of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d39bd-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d39bd-190">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-191"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d39bd-191"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d39bd-192">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d39bd-192">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-193"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d39bd-193"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d39bd-194">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d39bd-194">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-195"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d39bd-195"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d39bd-196">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="d39bd-196">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-197"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="d39bd-197"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d39bd-198">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d39bd-198">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d39bd-199"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d39bd-199"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d39bd-200">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d39bd-200">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d39bd-201"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d39bd-201"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d39bd-202">Se implementa como <strong>JetBackupW</strong> (Unicode) y <strong>JetBackupA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d39bd-202">Implemented as <strong>JetBackupW</strong> (Unicode) and <strong>JetBackupA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d39bd-203">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d39bd-203">See Also</span></span>

[<span data-ttu-id="d39bd-204">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="d39bd-204">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="d39bd-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d39bd-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d39bd-206">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d39bd-206">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d39bd-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="d39bd-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="d39bd-208">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="d39bd-208">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="d39bd-209">JetRestore</span><span class="sxs-lookup"><span data-stu-id="d39bd-209">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="d39bd-210">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="d39bd-210">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="d39bd-211">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="d39bd-211">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="d39bd-212">JetStopService</span><span class="sxs-lookup"><span data-stu-id="d39bd-212">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="d39bd-213">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="d39bd-213">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
