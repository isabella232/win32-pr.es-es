---
description: 'Más información acerca de: JetExternalRestore (función)'
title: JetExternalRestore función)
TOCTitle: JetExternalRestore Function
ms:assetid: c930689a-3ea6-4c5a-9318-76f519f23343
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294088(v=EXCHG.10)
ms:contentKeyID: 32765703
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetExternalRestoreA
- JetExternalRestore
- JetExternalRestoreW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087949817ac0bcbe2effe2ff136a6ce80084daa2
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105708131"
---
# <a name="jetexternalrestore-function"></a><span data-ttu-id="247ac-103">JetExternalRestore función)</span><span class="sxs-lookup"><span data-stu-id="247ac-103">JetExternalRestore Function</span></span>


<span data-ttu-id="247ac-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="247ac-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetexternalrestore-function"></a><span data-ttu-id="247ac-105">JetExternalRestore función)</span><span class="sxs-lookup"><span data-stu-id="247ac-105">JetExternalRestore Function</span></span>

<span data-ttu-id="247ac-106">La función **JetExternalRestore** restaura una copia de seguridad externa que se tomó con las API de copia de seguridad externas y especifica un intervalo de números de archivo de registro que se van a reproducir durante el proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="247ac-106">The **JetExternalRestore** function restores an external backup that was taken with the external backup APIs and specifies a range of log file numbers to replay during the restore process.</span></span> <span data-ttu-id="247ac-107">Esto se conoce como recuperación de hardware, que es similar a la recuperación de software, pero diferente de la que realiza la función [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="247ac-107">This is known as hard recovery, which is similar to but different than soft recovery as performed by the [JetInit](./jetinit-function.md) function.</span></span>

```cpp
JET_ERR JET_API JetExternalRestore(
  __in          JET_PSTR szCheckpointFilePath,
  __in          JET_PSTR szLogPath,
  __in_opt      JET_RSTMAP* rgrstmap,
  __in          long crstfilemap,
  __in          JET_PSTR szBackupLogPath,
  __in          long genLow,
  __in          long genHigh,
  __in          JET_PFNSTATUS pfn
);
```

### <a name="parameters"></a><span data-ttu-id="247ac-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="247ac-108">Parameters</span></span>

<span data-ttu-id="247ac-109">*szCheckpointFilePath*</span><span class="sxs-lookup"><span data-stu-id="247ac-109">*szCheckpointFilePath*</span></span>

<span data-ttu-id="247ac-110">La ruta de acceso del archivo de punto de comprobación que se va a usar durante la recuperación si *szTargetInstanceCheckpointPath* no se especifica o si ya tiene una instancia activa o en ejecución.</span><span class="sxs-lookup"><span data-stu-id="247ac-110">The path for the checkpoint file to use during recovery if *szTargetInstanceCheckpointPath* is not specified or already has an active or running instance.</span></span>

<span data-ttu-id="247ac-111">*szLogPath*</span><span class="sxs-lookup"><span data-stu-id="247ac-111">*szLogPath*</span></span>

<span data-ttu-id="247ac-112">La ruta de acceso o el directorio de los registros de la fase final (Deshacer) de la recuperación y, posiblemente, de los registros de puesta al día.</span><span class="sxs-lookup"><span data-stu-id="247ac-112">The path or directory for the logs for the final phase (undo) of recovery, and possibly for the roll forward logs.</span></span> <span data-ttu-id="247ac-113">Esta ruta de acceso puede ser la misma que la *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="247ac-113">This path may be the same as the *szBackupLogPath*.</span></span>

<span data-ttu-id="247ac-114">*rgrstmap*</span><span class="sxs-lookup"><span data-stu-id="247ac-114">*rgrstmap*</span></span>

<span data-ttu-id="247ac-115">Se trata de una matriz de estructuras [JET_RSTMAP](./jet-rstmap-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="247ac-115">This is an array of [JET_RSTMAP](./jet-rstmap-structure.md) structures.</span></span> <span data-ttu-id="247ac-116">Se trata de una asignación de nombres de archivo o rutas de acceso de base de datos antiguos y nuevos.</span><span class="sxs-lookup"><span data-stu-id="247ac-116">This is a map of old and new database paths or filenames.</span></span> <span data-ttu-id="247ac-117">Se usa porque las bases de datos pueden tener que recuperarse en una ubicación distinta de la ubicación desde la que se realizó la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="247ac-117">This is used because the databases may need to be recovered to a location other than the location they were backed up from.</span></span> <span data-ttu-id="247ac-118">En el caso de que varias bases de datos se adjunten a un único conjunto de registros, la asignación de restauración puede especificar un subconjunto de bases de datos que se van a restaurar.</span><span class="sxs-lookup"><span data-stu-id="247ac-118">In the case where multiple databases are attached to a single logging set, the restore map can specify a subset of databases to restore.</span></span>

<span data-ttu-id="247ac-119">*crstfilemap*</span><span class="sxs-lookup"><span data-stu-id="247ac-119">*crstfilemap*</span></span>

<span data-ttu-id="247ac-120">El número de entradas en el parámetro de matriz *rgrstmap* .</span><span class="sxs-lookup"><span data-stu-id="247ac-120">The number of entries in the *rgrstmap* array parameter.</span></span>

<span data-ttu-id="247ac-121">*szBackupLogPath*</span><span class="sxs-lookup"><span data-stu-id="247ac-121">*szBackupLogPath*</span></span>

<span data-ttu-id="247ac-122">La ruta de acceso al directorio donde se restauran los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="247ac-122">The path to the directory where the log files are restored.</span></span> <span data-ttu-id="247ac-123">Estos son los registros que se leyeron durante la secuencia de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="247ac-123">These are the logs that were read off during the external backup sequence.</span></span> <span data-ttu-id="247ac-124">Esta ruta de acceso puede ser la misma que la szLogPath.</span><span class="sxs-lookup"><span data-stu-id="247ac-124">This path may be the same as the szLogPath.</span></span>

<span data-ttu-id="247ac-125">*genLow*</span><span class="sxs-lookup"><span data-stu-id="247ac-125">*genLow*</span></span>

<span data-ttu-id="247ac-126">El número de archivo de registro más bajo que se va a reproducir desde *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="247ac-126">The lowest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="247ac-127">Se debe conservar la fidelidad total de una longitud sin signo, pero en las versiones actuales del motor, este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="247ac-127">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="247ac-128">Esto puede cambiar en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="247ac-128">This may change in future versions.</span></span>

<span data-ttu-id="247ac-129">*genHigh*</span><span class="sxs-lookup"><span data-stu-id="247ac-129">*genHigh*</span></span>

<span data-ttu-id="247ac-130">El número de archivo de registro más alto que se va a reproducir desde *szBackupLogPath*.</span><span class="sxs-lookup"><span data-stu-id="247ac-130">The highest log file number that is to be replayed from *szBackupLogPath*.</span></span> <span data-ttu-id="247ac-131">Se debe conservar la fidelidad total de una longitud sin signo, pero en las versiones actuales del motor, este número es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="247ac-131">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="247ac-132">Esto puede cambiar en versiones futuras.</span><span class="sxs-lookup"><span data-stu-id="247ac-132">This may change in future versions.</span></span>

<span data-ttu-id="247ac-133">*pfn*</span><span class="sxs-lookup"><span data-stu-id="247ac-133">*pfn*</span></span>

<span data-ttu-id="247ac-134">Devolución de llamada de estado para informar sobre el progreso de la recuperación.</span><span class="sxs-lookup"><span data-stu-id="247ac-134">The status callback, to report progress of the recovery.</span></span>

### <a name="return-value"></a><span data-ttu-id="247ac-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="247ac-135">Return Value</span></span>

<span data-ttu-id="247ac-136">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="247ac-136">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="247ac-137">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="247ac-137">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="247ac-138">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="247ac-138">Return code</span></span></p></th>
<th><p><span data-ttu-id="247ac-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="247ac-139">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="247ac-140">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="247ac-140">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="247ac-141">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="247ac-141">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247ac-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="247ac-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="247ac-143">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="247ac-143">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247ac-144">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="247ac-144">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="247ac-145">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="247ac-145">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="247ac-146">Esto puede ocurrir para <strong>JetExternalRestore</strong>, y así sucesivamente cuando <em>szTargetCheckpointPath</em> y <em>szTargetInstanceLogPath</em> no se especifican o no se especifican.</span><span class="sxs-lookup"><span data-stu-id="247ac-146">This can happen for <strong>JetExternalRestore</strong>, and so on when the <em>szTargetCheckpointPath</em> and the <em>szTargetInstanceLogPath</em> are either not both specified or not both unspecified.</span></span> <span data-ttu-id="247ac-147">Es decir, deben coincidir y estar especificados o no especificados.</span><span class="sxs-lookup"><span data-stu-id="247ac-147">That is, they must match, and be both specified or both unspecified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247ac-148">JET_errDatabaseCorrupted</span><span class="sxs-lookup"><span data-stu-id="247ac-148">JET_errDatabaseCorrupted</span></span></p></td>
<td><p><span data-ttu-id="247ac-149">Esto indica que la base de datos está dañada o un archivo no reconocido.</span><span class="sxs-lookup"><span data-stu-id="247ac-149">This indicates the database was corrupted, or an unrecognized file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247ac-150">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="247ac-150">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="247ac-151">No se pudo realizar la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="247ac-151">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247ac-152">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="247ac-152">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="247ac-153">No se pudo realizar la operación porque no se encontró la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="247ac-153">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247ac-154">JET_errRestoreOfNonBackupDatabase</span><span class="sxs-lookup"><span data-stu-id="247ac-154">JET_errRestoreOfNonBackupDatabase</span></span></p></td>
<td><p><span data-ttu-id="247ac-155">Se devuelve este error si el archivo de base de datos especificado durante la restauración no es una base de datos de la que se hizo copia de seguridad con copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="247ac-155">This error is returned if the database file specified during restore is not a database that was backed up with external backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247ac-156">JET_errStartingRestoreLogTooHigh</span><span class="sxs-lookup"><span data-stu-id="247ac-156">JET_errStartingRestoreLogTooHigh</span></span></p></td>
<td><p><span data-ttu-id="247ac-157">Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registro por debajo de la que especifica <em>genLow</em> o <em>pLogInfo. ulGenLow</em>.</span><span class="sxs-lookup"><span data-stu-id="247ac-157">This error is returned if one of the log files in the <em>szBackupLogPath</em>, has a log generation below that specified by the <em>genLow</em> or <em>pLogInfo.ulGenLow</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247ac-158">JET_errEndingRestoreLogTooLow</span><span class="sxs-lookup"><span data-stu-id="247ac-158">JET_errEndingRestoreLogTooLow</span></span></p></td>
<td><p><span data-ttu-id="247ac-159">Este error se devuelve si uno de los archivos de registro de <em>szBackupLogPath</em>tiene una generación de registro anterior que se especifica en <em>genHigh</em> o <em>pLogInfo. ulGenHigh</em>.</span><span class="sxs-lookup"><span data-stu-id="247ac-159">This error is returned if one fo the log files in the <em>szBackupLogPath</em>, has a log generation above that specified in <em>genHigh</em> or <em>pLogInfo.ulGenHigh</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247ac-160">JET_errBadRestoreTargetInstance</span><span class="sxs-lookup"><span data-stu-id="247ac-160">JET_errBadRestoreTargetInstance</span></span></p></td>
<td><p><span data-ttu-id="247ac-161">El <em>szTargetInstanceLogPath</em> especificado no pertenece a una instancia inicializada.</span><span class="sxs-lookup"><span data-stu-id="247ac-161">The <em>szTargetInstanceLogPath</em> specified does not belong to an initialized instance.</span></span> <span data-ttu-id="247ac-162">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="247ac-162">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247ac-163">JET_errRunningInOneInstanceMode</span><span class="sxs-lookup"><span data-stu-id="247ac-163">JET_errRunningInOneInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="247ac-164">El motor de base de datos no puede ejecutar la restauración externa o la recuperación de hardware en modo de instancia única.</span><span class="sxs-lookup"><span data-stu-id="247ac-164">The database engine cannot run external restore or hard recovery in single instance mode.</span></span> <span data-ttu-id="247ac-165">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="247ac-165">This error will only be returned in Windows XP and later.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="247ac-166">Si se ejecuta correctamente, todas las bases de datos de *rgrstmap* se recuperan completamente y en un estado limpio o coherente.</span><span class="sxs-lookup"><span data-stu-id="247ac-166">On success, all databases from the *rgrstmap* are completely recovered and in a clean or consistent state.</span></span> <span data-ttu-id="247ac-167">En este momento, la base de datos se puede volver a montar en una instancia existente.</span><span class="sxs-lookup"><span data-stu-id="247ac-167">At this point the database can be remounted to an existing instance.</span></span>

<span data-ttu-id="247ac-168">En caso de error, el motor no pudo recuperar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="247ac-168">On failure, the engine could not recover the database.</span></span> <span data-ttu-id="247ac-169">La base de datos está en un estado no válido y, para volver a intentar la recuperación de hardware, se debe restaurar toda la base de datos.</span><span class="sxs-lookup"><span data-stu-id="247ac-169">The database is in an invalid state, and in order to retry hard recovery the entire database must be restored again.</span></span> <span data-ttu-id="247ac-170">Normalmente, el origen de esta situación es el disco o el registro dañado, o algún otro tipo de administración incorrecta del registro, o un conjunto de registros no continuos.</span><span class="sxs-lookup"><span data-stu-id="247ac-170">Typically, the source of such a situation is disk or log corruption, or some other form of log mismanagement, or a non-continuous log set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="247ac-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="247ac-171">Remarks</span></span>

<span data-ttu-id="247ac-172">Para entender cómo funciona una recuperación "fuerte", debe comprender que hay tres fases de recuperación y que la segunda fase puede tener dos partes.</span><span class="sxs-lookup"><span data-stu-id="247ac-172">To understand how a "hard" recovery works, you must understand that there are three phases of recovery, and the second phase can have two parts.</span></span> <span data-ttu-id="247ac-173">En la fase I, los registros son necesarios para que una base de datos de copia de seguridad sea coherente (o se puede usar un conjunto inicial de registros incrementales).</span><span class="sxs-lookup"><span data-stu-id="247ac-173">In Phase I, logs are required to bring a backed up database to consistency (or an initial set of incremental logs can be used).</span></span> <span data-ttu-id="247ac-174">En la fase II, se consume cualquier registro de puesta al día adicional que esté disponible para que la base de datos sea coherente.</span><span class="sxs-lookup"><span data-stu-id="247ac-174">In Phase II, any additional roll forward logs that are available are consumed to make the database consistent.</span></span> <span data-ttu-id="247ac-175">También hay una reproducción de los registros de puesta al día adicionales.</span><span class="sxs-lookup"><span data-stu-id="247ac-175">There is also a replay of the additional roll forward logs.</span></span> <span data-ttu-id="247ac-176">La fase III es la fase de deshacer de la recuperación.</span><span class="sxs-lookup"><span data-stu-id="247ac-176">Phase III is the undo phase of recovery.</span></span>

<span data-ttu-id="247ac-177">Fase I: se realiza la reproducción del conjunto de registros que se deben restaurar para la base de datos a un estado coherente (o un conjunto inicial de archivos de registro).</span><span class="sxs-lookup"><span data-stu-id="247ac-177">Phase I: The replay of the set of logs that must be restored for the database to be brought to a consistent state (or an initial set of log files) is performed.</span></span> <span data-ttu-id="247ac-178">Básicamente, se trata de la reproducción del conjunto de archivos de registro que no son opcionales para las bases de datos que se están restaurando.</span><span class="sxs-lookup"><span data-stu-id="247ac-178">Basically, this is the replay of the set of log files that are not optional for the databases being restored.</span></span> <span data-ttu-id="247ac-179">Si faltan registros de este intervalo de registros, se producirá un error en la restauración.</span><span class="sxs-lookup"><span data-stu-id="247ac-179">If there are missing logs from this range of logs then the restore will fail.</span></span> <span data-ttu-id="247ac-180">Estos registros deben colocarse en el directorio especificado en el parámetro *szBackupLogPath* .</span><span class="sxs-lookup"><span data-stu-id="247ac-180">These logs should be put in the directory specified in the *szBackupLogPath* parameter.</span></span>

<span data-ttu-id="247ac-181">Fase II: opcionalmente, puede haber algunos conjuntos de archivos de registro que son los archivos de registro de puesta al día que proceden de copias de seguridad incrementales o diferenciales y de los archivos de registro de una instancia activa.</span><span class="sxs-lookup"><span data-stu-id="247ac-181">Phase II: Optionally, there may be some sets of log files that are roll forward log files that come from incremental or differential backups and from the log files of an active instance.</span></span> <span data-ttu-id="247ac-182">En el caso de los archivos de registro de copias de seguridad incrementales o diferenciales, los archivos de registro se pueden colocar en los directorios especificados en los parámetros *szBackupLogPath* o *szTargetInstanceLogPath* , donde el primero es el directorio recomendado.</span><span class="sxs-lookup"><span data-stu-id="247ac-182">In the case of log files from incremental or differential backups, the log files can be placed in the directories specified in either the *szBackupLogPath* or the *szTargetInstanceLogPath* parameters, with the former being the recommended directory.</span></span> <span data-ttu-id="247ac-183">Los registros que se usan para la fase de puesta al día (fase II) deben provienen de la misma serie de registros que se han producido durante la fase I y deben incrementar continuamente los números de registro sin brechas en los registros de la fase I.</span><span class="sxs-lookup"><span data-stu-id="247ac-183">The logs used for the roll forward phase (phase II) should come from the same series of logs played during Phase I and should have continuously incrementing log numbers with no gaps from the Phase I logs.</span></span> <span data-ttu-id="247ac-184">Para reproducir una base de datos que esté totalmente actualizada con los archivos de registro utilizados actualmente por una instancia activa, se deben especificar los parámetros *szTargetInstanceLogPath* y *szTargetInstanceCheckpointPath* .</span><span class="sxs-lookup"><span data-stu-id="247ac-184">To play a database to be fully up to date with the log files currently being used by an active instance, the *szTargetInstanceLogPath* and *szTargetInstanceCheckpointPath* parameters must be specified.</span></span> <span data-ttu-id="247ac-185">Esto se puede hacer incluso mientras otras bases de datos se adjuntan a ese conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="247ac-185">This can be done even while other databases are attached to that log set.</span></span>

<span data-ttu-id="247ac-186">Fase III: en la fase final de la recuperación, las transacciones no confirmadas se revierten, lo que requiere la generación de nuevos archivos de registro y la actualización del archivo de punto de comprobación.</span><span class="sxs-lookup"><span data-stu-id="247ac-186">Phase III: In the final phase of recovery, any uncommitted transactions are rolled back, which requires generating new log files and updating the checkpoint file.</span></span> <span data-ttu-id="247ac-187">Esta fase se conoce a veces como "deshacer".</span><span class="sxs-lookup"><span data-stu-id="247ac-187">This phase is sometimes referred to as "undo".</span></span> <span data-ttu-id="247ac-188">La ruta de acceso del archivo de punto de comprobación que se va a usar durante esta fase es la ruta de acceso análoga a la ubicación del registro de la fase III, es decir, si se usa *szLogPath* para la fase III, se usará *szCheckpointFilePath* si se usa *szTargetInstanceLogPath* para la fase III de recuperación *szTargetInstanceCheckpointPath* .</span><span class="sxs-lookup"><span data-stu-id="247ac-188">The checkpoint file path to use during this phase is the path analogous to the phase III log location, that is, if *szLogPath* is used for Phase III, *szCheckpointFilePath* will be used, if *szTargetInstanceLogPath* is used for phase III of recovery *szTargetInstanceCheckpointPath* will be used.</span></span>

<span data-ttu-id="247ac-189">Para comprender cómo funcionan las rutas de acceso, use este diagrama de flujo:</span><span class="sxs-lookup"><span data-stu-id="247ac-189">To understand how the paths work, use this flow chart:</span></span>

<span data-ttu-id="247ac-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span><span class="sxs-lookup"><span data-stu-id="247ac-190">![ESE_Documentation_ese1](images/Gg294088.ESE_Documentation_ese1(EXCHG.10).gif "ESE_Documentation_ese1")</span></span>

#### <a name="requirements"></a><span data-ttu-id="247ac-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="247ac-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="247ac-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="247ac-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="247ac-193">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="247ac-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247ac-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="247ac-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="247ac-195">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="247ac-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247ac-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="247ac-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="247ac-197">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="247ac-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247ac-198"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="247ac-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="247ac-199">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="247ac-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="247ac-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="247ac-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="247ac-201">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="247ac-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="247ac-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="247ac-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="247ac-203">Se implementa como <strong>JetExternalRestoreW</strong> (Unicode) y <strong>JetExternalRestoreA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="247ac-203">Implemented as <strong>JetExternalRestoreW</strong> (Unicode) and <strong>JetExternalRestoreA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="247ac-204">Consulte también</span><span class="sxs-lookup"><span data-stu-id="247ac-204">See Also</span></span>

[<span data-ttu-id="247ac-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="247ac-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="247ac-206">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="247ac-206">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="247ac-207">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="247ac-207">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="247ac-208">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="247ac-208">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="247ac-209">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="247ac-209">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="247ac-210">JetInit</span><span class="sxs-lookup"><span data-stu-id="247ac-210">JetInit</span></span>](./jetinit-function.md)
