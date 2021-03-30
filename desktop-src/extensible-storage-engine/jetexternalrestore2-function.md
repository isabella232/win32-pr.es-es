---
description: 'Más información acerca de: JetExternalRestore2 (función)'
title: Función JetExternalRestore2
TOCTitle: JetExternalRestore2 Function
ms:assetid: 66331be0-7abc-43a0-8b8b-dbdd227c918e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269272(v=EXCHG.10)
ms:contentKeyID: 32765574
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestore2W
- JetExternalRestore2A
- JetExternalRestore2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96314e401a81271f5a71bc056faa95fc1ae0dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002411"
---
# <a name="jetexternalrestore2-function"></a><span data-ttu-id="0b71a-103">Función JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="0b71a-103">JetExternalRestore2 Function</span></span>


<span data-ttu-id="0b71a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0b71a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore2-function"></a><span data-ttu-id="0b71a-105">Función JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="0b71a-105">JetExternalRestore2 Function</span></span>

<span data-ttu-id="0b71a-106">La función **JetExternalRestore2** restaura una copia de seguridad externa que se tomó con las API de copia de seguridad externas y proporciona puntos de control que se utilizan para las operaciones de registro circulares.</span><span class="sxs-lookup"><span data-stu-id="0b71a-106">The **JetExternalRestore2** function restores an external backup that was taken with the external backup APIs and provides checkpoints to use for circular logging operations.</span></span> <span data-ttu-id="0b71a-107">Esto se conoce como recuperación de hardware, que es similar pero diferente a la recuperación de software que realiza la función [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0b71a-107">This is known as hard recovery, which is similar but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

<span data-ttu-id="0b71a-108">**Windows XP: JetExternalRestore2** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b71a-108">**Windows XP:  JetExternalRestore2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetExternalRestore2(
      __in          JET_PSTR szCheckpointFilePath,
      __in          JET_PSTR szLogPath,
      __in_opt      JET_RSTMAP* rgrstmap,
      __in          long crstfilemap,
      __in          JET_PSTR szBackupLogPath,
      __in_out      JET_LOGINFO* pLogInfo,
      __in_opt      JET_PSTR szTargetInstanceName,
      __in_opt      JET_PSTR szTargetInstanceLogPath,
      __in_opt      JET_PSTR szTargetInstanceCheckpointPath,
      __in          JET_PFNSTATUS pfn
    );
```

### <a name="parameters"></a><span data-ttu-id="0b71a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b71a-109">Parameters</span></span>

<span data-ttu-id="0b71a-110">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="0b71a-110">*szCheckpointFilePath*</span></span>

<span data-ttu-id="0b71a-111">La ruta de acceso del archivo de punto de comprobación que se va a usar durante la recuperación si no se especifica *szTargetInstanceCheckpointPath* o si la ruta de acceso tiene una instancia activa o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="0b71a-111">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or that path has an active or running instance.</span></span>

<span data-ttu-id="0b71a-112">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="0b71a-112">*szLogPath*</span></span>

<span data-ttu-id="0b71a-113">La ruta de acceso o el directorio de los registros de la fase final (Deshacer) de la recuperación y, posiblemente, de los registros de puesta al día.</span><span class="sxs-lookup"><span data-stu-id="0b71a-113">The path or directory for the logs for the final phase (undo) of the recovery and possibly for the roll forward logs.</span></span> <span data-ttu-id="0b71a-114">Esta ruta de acceso puede ser la misma que la *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="0b71a-114">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="0b71a-115">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="0b71a-115">*rgrstmap*</span></span>

<span data-ttu-id="0b71a-116">Se trata de una matriz de estructuras [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="0b71a-116">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="0b71a-117">Se trata de una asignación de nombres de archivo o rutas de acceso de base de datos antiguos y nuevos.</span><span class="sxs-lookup"><span data-stu-id="0b71a-117">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="0b71a-118">Se usa porque las bases de datos pueden tener que recuperarse en una ubicación distinta de la ubicación desde la que se realizó la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0b71a-118">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="0b71a-119">En el caso de que varias bases de datos se adjunten a un único conjunto de registros, la asignación de restauración puede especificar un subconjunto de las bases de datos que se van a restaurar.</span><span class="sxs-lookup"><span data-stu-id="0b71a-119">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of the databases to restore.</span></span>

<span data-ttu-id="0b71a-120">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="0b71a-120">*crstfilemap*</span></span>

<span data-ttu-id="0b71a-121">El número de entradas en el parámetro de matriz *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="0b71a-121">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="0b71a-122">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="0b71a-122">*szBackupLogPath*</span></span>

<span data-ttu-id="0b71a-123">La ruta de acceso al directorio donde se restauran los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="0b71a-123">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="0b71a-124">Estos son los registros que se leyeron durante la secuencia de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="0b71a-124">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="0b71a-125">Esta ruta de acceso puede ser la misma que la *szLogPath*.</span><span class="sxs-lookup"><span data-stu-id="0b71a-125">This path may be the same as the *szLogPath*.</span></span>

<span data-ttu-id="0b71a-126">*pLogInfo*</span><span class="sxs-lookup"><span data-stu-id="0b71a-126">*pLogInfo*</span></span>

<span data-ttu-id="0b71a-127">*PLogInfo* describe varios aspectos de los registros de copia de seguridad que se van a recuperar. este parámetro permite a **JetExternalRestore2** tomar los parámetros *genLow* y *genHigh* explícitos que **JetExternalRestore2** tiene, así como el nombre de registro base, en lugar de un nombre de base de registro supuestamente "edb".</span><span class="sxs-lookup"><span data-stu-id="0b71a-127">The *pLogInfo* describes several aspects of the backup logs to recovery, this parameter allows **JetExternalRestore2** to take the explicit *genLow* and *genHigh* parameters that **JetExternalRestore2** has, as well as the base log name, instead of a presumed log base name of "edb".</span></span>

<span data-ttu-id="0b71a-128">*szTargetInstanceName*</span><span class="sxs-lookup"><span data-stu-id="0b71a-128">*szTargetInstanceName*</span></span>

<span data-ttu-id="0b71a-129">Este parámetro está en desuso y no se puede usar en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0b71a-129">This parameter is deprecated and cannot be used in your application.</span></span>

<span data-ttu-id="0b71a-130">*szTargetInstanceLogPath*</span><span class="sxs-lookup"><span data-stu-id="0b71a-130">*szTargetInstanceLogPath*</span></span>

<span data-ttu-id="0b71a-131">La ruta de acceso para los registros de puesta al día si la ubicación de los registros que le gustaría poner al día se encuentran en un conjunto de registros o una instancia activos.</span><span class="sxs-lookup"><span data-stu-id="0b71a-131">The path for the roll forward logs if the location of the logs you would like to roll forward are in an active logging set or instance.</span></span> <span data-ttu-id="0b71a-132">No debe especificarse si la instancia de de destino utiliza el registro circular.</span><span class="sxs-lookup"><span data-stu-id="0b71a-132">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="0b71a-133">*szTargetInstanceCheckpointPath*</span><span class="sxs-lookup"><span data-stu-id="0b71a-133">*szTargetInstanceCheckpointPath*</span></span>

<span data-ttu-id="0b71a-134">La ruta de acceso del punto de comprobación durante la recuperación si no hay ninguna instancia activa en ejecución en este destino.</span><span class="sxs-lookup"><span data-stu-id="0b71a-134">The path for the checkpoint during recovery if there is no active instance running at this target.</span></span> <span data-ttu-id="0b71a-135">No debe especificarse si la instancia de de destino utiliza el registro circular.</span><span class="sxs-lookup"><span data-stu-id="0b71a-135">This should not be specified if the target instance is using circular logging.</span></span>

<span data-ttu-id="0b71a-136">*pfn*</span><span class="sxs-lookup"><span data-stu-id="0b71a-136">*pfn*</span></span>

<span data-ttu-id="0b71a-137">La devolución de llamada de estado, que informa del progreso de la recuperación.</span><span class="sxs-lookup"><span data-stu-id="0b71a-137">The status callback, which reports the progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="0b71a-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b71a-138">Return Value</span></span>

<span data-ttu-id="0b71a-139">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="0b71a-139">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0b71a-140">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0b71a-140">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0b71a-141">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0b71a-141">Return code</span></span></p></th>
<th><p><span data-ttu-id="0b71a-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b71a-142">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-143">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="0b71a-143">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="0b71a-144">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b71a-144">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b71a-145">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="0b71a-145">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="0b71a-146">El <em>szTargetInstanceLogPath</em> especificado no pertenece a una instancia inicializada.</span><span class="sxs-lookup"><span data-stu-id="0b71a-146">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="0b71a-147">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0b71a-147">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="0b71a-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="0b71a-149">Esto indica que la base de datos está dañada o un archivo no reconocido.</span><span class="sxs-lookup"><span data-stu-id="0b71a-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b71a-150">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="0b71a-150">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="0b71a-151">Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registro anterior que se especifica en <em>genHigh</em> o <em>pLogInfo. ulGenHigh</em>.</span><span class="sxs-lookup"><span data-stu-id="0b71a-151">This error is returned if one for the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-152">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="0b71a-152">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="0b71a-153">No se pudo realizar la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="0b71a-153">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b71a-154">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="0b71a-154">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="0b71a-155">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="0b71a-155">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="0b71a-156">Esto puede ocurrir para <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, y así sucesivamente cuando <em>szTargetCheckpointPath</em> y <em>szTargetInstanceLogPath</em> no se especifican o no se especifican.</span><span class="sxs-lookup"><span data-stu-id="0b71a-156">This can happen for <a href="gg294088(v=exchg.10).md">JetExternalRestore</a>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="0b71a-157">Es decir, deben coincidir y estar especificados o no especificados.</span><span class="sxs-lookup"><span data-stu-id="0b71a-157">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-158">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="0b71a-158">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="0b71a-159">No se pudo realizar la operación porque no se encontró la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="0b71a-159">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b71a-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="0b71a-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="0b71a-161">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="0b71a-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-162">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="0b71a-162">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="0b71a-163">Se devuelve este error si el archivo de base de datos especificado durante la restauración no es una base de datos de la que se hizo copia de seguridad con copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="0b71a-163">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b71a-164">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="0b71a-164">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="0b71a-165">El motor de base de datos no puede ejecutar la restauración externa o la recuperación de hardware en modo de instancia única.</span><span class="sxs-lookup"><span data-stu-id="0b71a-165">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="0b71a-166">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0b71a-166">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-167">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="0b71a-167">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="0b71a-168">Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registro por debajo de la que especifica <em>genLow</em> o <em>pLogInfo. ulGenLow</em>.</span><span class="sxs-lookup"><span data-stu-id="0b71a-168">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b71a-169">Si se ejecuta correctamente, todas las bases de datos de *rgrstmap* se recuperan completamente y en un estado limpio o coherente.</span><span class="sxs-lookup"><span data-stu-id="0b71a-169">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="0b71a-170">En este momento, la base de datos se puede volver a montar en una instancia existente.</span><span class="sxs-lookup"><span data-stu-id="0b71a-170">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="0b71a-171">En caso de error, el motor no pudo recuperar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0b71a-171">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="0b71a-172">La base de datos está en un estado no válido y, para volver a intentar la recuperación de hardware, se debe restaurar toda la base de datos.</span><span class="sxs-lookup"><span data-stu-id="0b71a-172">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="0b71a-173">Normalmente, el origen de esta situación es el disco o el registro dañado, o algún otro tipo de administración incorrecta del registro, o un conjunto de registros no continuos.</span><span class="sxs-lookup"><span data-stu-id="0b71a-173">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="0b71a-174">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b71a-174">Remarks</span></span>

<span data-ttu-id="0b71a-175">Vea [JetExternalRestore](./jetexternalrestore-function.md).</span><span class="sxs-lookup"><span data-stu-id="0b71a-175">See [JetExternalRestore](./jetexternalrestore-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="0b71a-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b71a-176">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-177"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0b71a-177"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0b71a-178">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0b71a-178">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b71a-179"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0b71a-179"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0b71a-180">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0b71a-180">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-181"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0b71a-181"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0b71a-182">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="0b71a-182">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b71a-183"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="0b71a-183"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0b71a-184">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0b71a-184">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b71a-185"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0b71a-185"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0b71a-186">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0b71a-186">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b71a-187"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="0b71a-187"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="0b71a-188">Se implementa como <strong>JetExternalRestore2W</strong> (Unicode) y <strong>JetExternalRestore2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="0b71a-188">Implemented as <strong>JetExternalRestore2W</strong> (Unicode) and <strong>JetExternalRestore2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0b71a-189">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0b71a-189">See Also</span></span>

[<span data-ttu-id="0b71a-190">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0b71a-190">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0b71a-191">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="0b71a-191">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="0b71a-192">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="0b71a-192">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="0b71a-193">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="0b71a-193">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="0b71a-194">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="0b71a-194">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="0b71a-195">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="0b71a-195">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="0b71a-196">JetInit</span><span class="sxs-lookup"><span data-stu-id="0b71a-196">JetInit</span></span>](./jetinit-function.md)
