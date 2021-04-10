---
description: 'Más información acerca de: JetBackupInstance (función)'
title: Función JetBackupInstance
TOCTitle: JetBackupInstance Function
ms:assetid: 82486441-5037-440b-8632-038e953ad870
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269318(v=EXCHG.10)
ms:contentKeyID: 32765608
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBackupInstanceW
- JetBackupInstanceA
- JetBackupInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fab20676267333ae8f60e4fe4f07d98a8b45e88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153775"
---
# <a name="jetbackupinstance-function"></a><span data-ttu-id="77849-103">Función JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="77849-103">JetBackupInstance Function</span></span>


<span data-ttu-id="77849-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77849-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbackupinstance-function"></a><span data-ttu-id="77849-105">Función JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="77849-105">JetBackupInstance Function</span></span>

<span data-ttu-id="77849-106">La función **JetBackupInstance** realiza una copia de seguridad de secuencias de una instancia, incluidas todas las bases de datos adjuntas, en un directorio.</span><span class="sxs-lookup"><span data-stu-id="77849-106">The **JetBackupInstance** function performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="77849-107">Con varios métodos de copia de seguridad admitidos por el motor de, esta es la función más sencilla y encapsulada.</span><span class="sxs-lookup"><span data-stu-id="77849-107">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="77849-108">**Windows XP: JetBackupInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77849-108">**Windows XP:  JetBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szBackupPath,
      __in          JET_GRBIT grbit,
      __in          JET_PFNSTATUS pfnStatus
    );
```

### <a name="parameters"></a><span data-ttu-id="77849-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77849-109">Parameters</span></span>

<span data-ttu-id="77849-110">*repetición*</span><span class="sxs-lookup"><span data-stu-id="77849-110">*instance*</span></span>

<span data-ttu-id="77849-111">Instancia de la base de datos que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="77849-111">The instance of the database to backup.</span></span>

<span data-ttu-id="77849-112">*szBackupPath*</span><span class="sxs-lookup"><span data-stu-id="77849-112">*szBackupPath*</span></span>

<span data-ttu-id="77849-113">Directorio en el que se almacena la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-113">The directory where the backup is stored.</span></span> <span data-ttu-id="77849-114">Si la ruta de acceso de copia de seguridad es NULL para usar la función, truncará los registros, si es posible.</span><span class="sxs-lookup"><span data-stu-id="77849-114">If the backup path is NULL to use the function will truncate the logs, if possible.</span></span>

<span data-ttu-id="77849-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="77849-115">*grbit*</span></span>

<span data-ttu-id="77849-116">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="77849-116">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77849-117">Value</span><span class="sxs-lookup"><span data-stu-id="77849-117">Value</span></span></p></th>
<th><p><span data-ttu-id="77849-118">Significado</span><span class="sxs-lookup"><span data-stu-id="77849-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77849-119">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="77849-119">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="77849-120">Crea una copia de seguridad completa de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="77849-120">Creates a full backup of the database.</span></span> <span data-ttu-id="77849-121">Esto permite conservar una copia de seguridad existente en el mismo directorio si se produce un error en la nueva copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-121">This allows the preservation of an existing backup in the same directory if the new backup fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-122">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="77849-122">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="77849-123">Crea una copia de seguridad incremental en lugar de una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="77849-123">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="77849-124">Esto significa que solo se realizará una copia de seguridad de los archivos de registro creados desde la última copia de seguridad completa o incremental.</span><span class="sxs-lookup"><span data-stu-id="77849-124">This means that only the log files created since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-125">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="77849-125">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="77849-126">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="77849-126">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77849-127">*pfnStatus*</span><span class="sxs-lookup"><span data-stu-id="77849-127">*pfnStatus*</span></span>

<span data-ttu-id="77849-128">Puntero a la función de devolución de llamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) , que proporciona información de notificación sobre el progreso de la operación de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-128">Pointer to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function, which provides notification information about the progress of the backup operation.</span></span>

### <a name="return-value"></a><span data-ttu-id="77849-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77849-129">Return Value</span></span>

<span data-ttu-id="77849-130">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="77849-130">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="77849-131">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="77849-131">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77849-132">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="77849-132">Return code</span></span></p></th>
<th><p><span data-ttu-id="77849-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="77849-133">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77849-134">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="77849-134">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="77849-135">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="77849-135">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-136">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="77849-136">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="77849-137">Ya hay una copia de seguridad en curso para la misma instancia.</span><span class="sxs-lookup"><span data-stu-id="77849-137">A backup is already in progress for the same instance.</span></span> <span data-ttu-id="77849-138">No se permiten varias copias de seguridad al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="77849-138">Multiple backups are not allowed at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-139">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="77849-139">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="77849-140">La instancia todavía no está lista para la copia de seguridad mientras se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="77849-140">The instance is not ready yet for backup as it is initializing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-141">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="77849-141">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="77849-142">No se puede completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="77849-142">The operation cannot complete because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-143">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="77849-143">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="77849-144">No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="77849-144">The operation cannot complete because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="77849-145"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77849-145"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-146">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="77849-146">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="77849-147">No se permite una copia de seguridad incremental si el registro circular está activado.</span><span class="sxs-lookup"><span data-stu-id="77849-147">An incremental backup is not allowed if circular logging is on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-148">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="77849-148">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="77849-149">Las opciones especificadas no son válidas.</span><span class="sxs-lookup"><span data-stu-id="77849-149">The specified options are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="77849-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="77849-151">Se pasó un parámetro no válido a la API.</span><span class="sxs-lookup"><span data-stu-id="77849-151">An invalid parameter was passed into the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="77849-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="77849-153">La ruta de acceso de destino no existe.</span><span class="sxs-lookup"><span data-stu-id="77849-153">The destination path does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-154">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="77849-154">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="77849-155">La instancia se está ejecutando sin registro.</span><span class="sxs-lookup"><span data-stu-id="77849-155">The instance is running without logging.</span></span> <span data-ttu-id="77849-156">No se permite ninguna copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-156">No backup is allowed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-157">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="77849-157">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="77849-158">Se produjo un error de comprobación de la suma de comprobación en un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="77849-158">There was a checksum verification error on a log file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-159">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="77849-159">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="77849-160">El registro de la instancia es temporal o está deshabilitado permanentemente debido a un error inesperado.</span><span class="sxs-lookup"><span data-stu-id="77849-160">The logging for the instance is temporary or permanently disabled due to an unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-161">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="77849-161">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="77849-162">No se puede completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="77849-162">The operation cannot complete because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-163">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="77849-163">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="77849-164">Se produjo un error de comprobación de la suma de comprobación en una página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="77849-164">There was a checksum verification error on a database page.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-165">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="77849-165">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="77849-166">No se puede completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="77849-166">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-167">JET_errSessionSharingViolation</span><span class="sxs-lookup"><span data-stu-id="77849-167">JET_errSessionSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="77849-168">No se puede usar la misma sesión para más de un subproceso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="77849-168">The same session cannot be used for more than one thread at the same time.</span></span></p>
<p><span data-ttu-id="77849-169"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77849-169"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="77849-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="77849-171">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="77849-171">The operation cannot complete because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77849-172">Una vez que la función devuelve un resultado correcto, se mostrarán todos los archivos necesarios para una restauración hasta el momento de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-172">After the function returns success, in the backup directory all the files needed for a restore up to the moment of the backup will be present.</span></span> <span data-ttu-id="77849-173">Si se trata de una copia de seguridad completa, los archivos serán los archivos de base de datos y los archivos de registro necesarios para poner la base de datos en un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="77849-173">If this is a full backup, the files will be the database files and the log files needed to bring the database to a consistent state.</span></span> <span data-ttu-id="77849-174">Si se trata de una copia de seguridad incremental, solo se agregarán los archivos de registro a los directorios, pero los archivos ya existentes (archivos de registro y bases de datos) junto con los nuevos archivos de registro se podrán restaurar y volver a poner la base de datos al estado en el momento de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-174">If this is an incremental backup, only log files will be added to the directories but the already existing files (databases and log files) together with the new log files will be able to be restored and bring the database back to the state at the moment of the backup.</span></span>

<span data-ttu-id="77849-175">Como efecto secundario de la copia de seguridad, se truncarán los archivos de registro que ya no sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="77849-175">As a side effect of the backup, the log files which are not longer needed will be truncated.</span></span>

<span data-ttu-id="77849-176">Al mismo tiempo, los encabezados de la base de datos se actualizarán con la información cuando se realizó la última copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-176">In the same time, the database headers will be updated with the information when the last backup took place.</span></span>

<span data-ttu-id="77849-177">En caso de error, no habrá ningún archivo en el destino del directorio de copia de seguridad, por lo que no será posible realizar ninguna restauración.</span><span class="sxs-lookup"><span data-stu-id="77849-177">On failure, there will not be any files in the backup directory destination so no restore will be possible.</span></span> <span data-ttu-id="77849-178">Al mismo tiempo, los archivos de registro actuales no se truncarán.</span><span class="sxs-lookup"><span data-stu-id="77849-178">In the same time, the current log files will not be truncated.</span></span>

#### <a name="remarks"></a><span data-ttu-id="77849-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77849-179">Remarks</span></span>

<span data-ttu-id="77849-180">Los distintos pasos de la copia de seguridad tendrán entradas del registro de eventos generadas, incluidos los nombres de archivo, el truncamiento del registro y el resultado final de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-180">The different steps of the backup will have Event Log entries generated including the file names, the log truncation and the final result of the backup.</span></span>

<span data-ttu-id="77849-181">La copia de seguridad incremental solo es posible después de realizar una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="77849-181">Incremental backup are possible only after a full backup was taken.</span></span> <span data-ttu-id="77849-182">Además, solo se pueden realizar copias de seguridad incrementales si el registro circular está desactivado.</span><span class="sxs-lookup"><span data-stu-id="77849-182">Also, incremental backups are possible only if circular logging is turned off.</span></span> <span data-ttu-id="77849-183">Se recomienda que el directorio de copia de seguridad no contenga otros archivos, el implicado en la copia de seguridad o que se agregaron mediante una copia de seguridad correcta anterior.</span><span class="sxs-lookup"><span data-stu-id="77849-183">It is recommended that the backup directory should not contain other files then the one involved in the backup or added by a previous successful backup.</span></span>

<span data-ttu-id="77849-184">El directorio de copia de seguridad debe existir a menos que se establezca el parámetro *JET_paramCreatePathIfNotExist* para la instancia.</span><span class="sxs-lookup"><span data-stu-id="77849-184">The backup directory should exist unless the parameter *JET_paramCreatePathIfNotExist* is set for the instance.</span></span> <span data-ttu-id="77849-185">Para obtener más información, vea [parámetros del sistema](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="77849-185">For information, see [System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="77849-186">La copia de seguridad realizará la comprobación de la suma de comprobación en todas las páginas de base de datos usadas y, a partir de Windows Server 2003, también en los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="77849-186">The backup will do checksum verification on all the used database pages and starting with Windows Server 2003, on the log files as well.</span></span> <span data-ttu-id="77849-187">Esto ofrece una oportunidad para estimar el estado de la base de datos incluso para las páginas que no se leen durante las operaciones normales.</span><span class="sxs-lookup"><span data-stu-id="77849-187">This gives an opportunity to estimate the health of the database even for pages which are not read during normal operations.</span></span> <span data-ttu-id="77849-188">Si se encuentra algún daño de este tipo, se producirá un error en la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="77849-188">If any such corruption will be encountered, the backup will fail.</span></span>

<span data-ttu-id="77849-189">Durante la copia de seguridad, el archivo de registro actual finalizará y se iniciará una nueva generación de registros.</span><span class="sxs-lookup"><span data-stu-id="77849-189">During the backup, the current log file will be finished and we will start a new log generation.</span></span> <span data-ttu-id="77849-190">Esto permitirá copiar los archivos de registro necesarios porque ya no se utilizará el último que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="77849-190">This will allow copying the needed log files because the last needed one will not be in use anymore.</span></span>

<span data-ttu-id="77849-191">Se recomienda encarecidamente que la copia de seguridad no se use para otras otras, y que se restaure en el nivel de motor.</span><span class="sxs-lookup"><span data-stu-id="77849-191">It is strongly recommended that the backup should not be used for other purposed other then the backup and restored at the engine level.</span></span> <span data-ttu-id="77849-192">Esto minimizará el cambio de obtención de errores durante las operaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="77849-192">This will minimize the change of getting errors during the backup and restore operations.</span></span>

#### <a name="requirements"></a><span data-ttu-id="77849-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77849-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77849-194"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="77849-194"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77849-195">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="77849-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-196"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="77849-196"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77849-197">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="77849-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-198"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="77849-198"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77849-199">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="77849-199">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-200"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="77849-200"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="77849-201">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="77849-201">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77849-202"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="77849-202"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="77849-203">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="77849-203">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77849-204"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="77849-204"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="77849-205">Se implementa como <strong>JetBackupInstanceW</strong> (Unicode) y <strong>JetBackupInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="77849-205">Implemented as <strong>JetBackupInstanceW</strong> (Unicode) and <strong>JetBackupInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="77849-206">Consulte también</span><span class="sxs-lookup"><span data-stu-id="77849-206">See Also</span></span>

[<span data-ttu-id="77849-207">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="77849-207">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="77849-208">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="77849-208">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="77849-209">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="77849-209">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="77849-210">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="77849-210">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="77849-211">JetRestore</span><span class="sxs-lookup"><span data-stu-id="77849-211">JetRestore</span></span>](./jetrestore-function.md)  
[<span data-ttu-id="77849-212">JetRestore2</span><span class="sxs-lookup"><span data-stu-id="77849-212">JetRestore2</span></span>](./jetrestore2-function.md)  
[<span data-ttu-id="77849-213">JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="77849-213">JetRestoreInstance</span></span>](./jetrestoreinstance-function.md)  
[<span data-ttu-id="77849-214">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="77849-214">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)  
[<span data-ttu-id="77849-215">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="77849-215">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
