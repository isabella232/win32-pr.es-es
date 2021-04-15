---
description: 'Más información acerca de: JetBeginExternalBackup (función)'
title: JetBeginExternalBackup función)
TOCTitle: JetBeginExternalBackup Function
ms:assetid: 702e6cbf-4648-40f2-b2eb-6194759d4cde
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269292(v=EXCHG.10)
ms:contentKeyID: 32765584
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d410adb592c3d56d2f9880ec809749396318258a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669713"
---
# <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="9d175-103">JetBeginExternalBackup función)</span><span class="sxs-lookup"><span data-stu-id="9d175-103">JetBeginExternalBackup Function</span></span>


<span data-ttu-id="9d175-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9d175-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetbeginexternalbackup-function"></a><span data-ttu-id="9d175-105">JetBeginExternalBackup función)</span><span class="sxs-lookup"><span data-stu-id="9d175-105">JetBeginExternalBackup Function</span></span>

<span data-ttu-id="9d175-106">La función **JetBeginExternalBackup** inicia una copia de seguridad externa mientras el motor y la base de datos están en línea y activos.</span><span class="sxs-lookup"><span data-stu-id="9d175-106">The **JetBeginExternalBackup** function initiates an external backup while the engine and database is online and active.</span></span> <span data-ttu-id="9d175-107">**JetBeginExternalBackup** es el primero de una serie de funciones a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</span><span class="sxs-lookup"><span data-stu-id="9d175-107">**JetBeginExternalBackup** is the first in a series of functions that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="9d175-108">Se puede utilizar una copia de seguridad externa para implementar copias de seguridad completas, incrementales o diferenciales.</span><span class="sxs-lookup"><span data-stu-id="9d175-108">An external backup can be used to implement full, incremental, or differential backups.</span></span>

<span data-ttu-id="9d175-109">La copia de seguridad será aproximada, en la que la copia de seguridad será coherente con un único punto en el tiempo en el historial de transacciones, pero no es posible controlar el punto exacto en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="9d175-109">The backup will be fuzzy, in that the backup will be consistent to a single point in time in the transaction history, but controlling the exact point in time is not possible.</span></span>

```cpp
    JET_ERR JET_API JetBeginExternalBackup(
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="9d175-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d175-110">Parameters</span></span>

<span data-ttu-id="9d175-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="9d175-111">*grbit*</span></span>

<span data-ttu-id="9d175-112">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="9d175-112">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d175-113">Value</span><span class="sxs-lookup"><span data-stu-id="9d175-113">Value</span></span></p></th>
<th><p><span data-ttu-id="9d175-114">Significado</span><span class="sxs-lookup"><span data-stu-id="9d175-114">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d175-115">JET_bitBackupAtomic</span><span class="sxs-lookup"><span data-stu-id="9d175-115">JET_bitBackupAtomic</span></span></p></td>
<td><p><span data-ttu-id="9d175-116">Esta marca está en desuso.</span><span class="sxs-lookup"><span data-stu-id="9d175-116">This flag is deprecated.</span></span> <span data-ttu-id="9d175-117">El uso de este bit producirá JET_errInvalidgrbit devuelto.</span><span class="sxs-lookup"><span data-stu-id="9d175-117">Usage of this bit will result in JET_errInvalidgrbit being returned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-118">JET_bitBackupIncremental</span><span class="sxs-lookup"><span data-stu-id="9d175-118">JET_bitBackupIncremental</span></span></p></td>
<td><p><span data-ttu-id="9d175-119">Crea una copia de seguridad incremental en lugar de una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="9d175-119">Creates an incremental backup as opposed to a full backup.</span></span> <span data-ttu-id="9d175-120">Esto significa que solo se realizará una copia de seguridad de los archivos de registro desde la última copia de seguridad completa o incremental.</span><span class="sxs-lookup"><span data-stu-id="9d175-120">This means that only the log files since the last full or incremental backup will be backed up.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-121">JET_bitBackupSnapshot</span><span class="sxs-lookup"><span data-stu-id="9d175-121">JET_bitBackupSnapshot</span></span></p></td>
<td><p><span data-ttu-id="9d175-122">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="9d175-122">Reserved for future use.</span></span> <span data-ttu-id="9d175-123">Definido para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9d175-123">Defined for Windows XP.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="9d175-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d175-124">Return Value</span></span>

<span data-ttu-id="9d175-125">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="9d175-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="9d175-126">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9d175-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d175-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9d175-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="9d175-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d175-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d175-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="9d175-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="9d175-130">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d175-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-131">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="9d175-131">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="9d175-132">Si ya está en curso una copia de seguridad externa o de instantáneas, se devolverá este error hasta que se llame a <strong>JetBeginExternalBackup</strong> (o a una de las variantes de este).</span><span class="sxs-lookup"><span data-stu-id="9d175-132">If an external backup or snapshot backup is already in process, this error will be returned, until <strong>JetBeginExternalBackup</strong> (or one of the variants of it) is called.</span></span> <span data-ttu-id="9d175-133">ESE solo permite una copia de seguridad en línea a la vez.</span><span class="sxs-lookup"><span data-stu-id="9d175-133">ESE allows only one online backup at a time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-134">JET_errBackupNotAllowedYet</span><span class="sxs-lookup"><span data-stu-id="9d175-134">JET_errBackupNotAllowedYet</span></span></p></td>
<td><p><span data-ttu-id="9d175-135">La instancia o el motor de base de datos está en recuperación o en una fase de cierre o finalización.</span><span class="sxs-lookup"><span data-stu-id="9d175-135">The instance or database engine is either in recovery or in a shutdown or termination phase.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-136">JET_errCheckpointCorrupt</span><span class="sxs-lookup"><span data-stu-id="9d175-136">JET_errCheckpointCorrupt</span></span></p></td>
<td><p><span data-ttu-id="9d175-137">En una copia de seguridad completa, no se pudo leer el archivo de punto de comprobación o no se pudo comprobar el archivo.</span><span class="sxs-lookup"><span data-stu-id="9d175-137">On a full backup, the checkpoint file could not be read, or the file could not be verified.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-138">JET_errCheckpointFileNotFound</span><span class="sxs-lookup"><span data-stu-id="9d175-138">JET_errCheckpointFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="9d175-139">En una copia de seguridad completa, no se encontró el archivo de punto de comprobación.</span><span class="sxs-lookup"><span data-stu-id="9d175-139">On a full backup, the checkpoint file could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-140">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="9d175-140">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="9d175-141">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="9d175-141">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-142">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="9d175-142">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="9d175-143">No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="9d175-143">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="9d175-144"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9d175-144"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-145">JET_errInvalidBackup</span><span class="sxs-lookup"><span data-stu-id="9d175-145">JET_errInvalidBackup</span></span></p></td>
<td><p><span data-ttu-id="9d175-146">El registro circular está habilitado y el tipo de copia de seguridad especificado es JET_bitBackupIncremental.</span><span class="sxs-lookup"><span data-stu-id="9d175-146">Circular logging is enabled and the backup type specified is JET_bitBackupIncremental.</span></span> <span data-ttu-id="9d175-147">Consulte <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> en los <strong>errores del registro de transacciones</strong> para obtener información sobre cómo controlar el registro circular o no circular.</span><span class="sxs-lookup"><span data-stu-id="9d175-147">See <a href="gg269235(v=exchg.10).md">JET_paramCircularLog</a> in the <strong>Transaction Log Errors</strong> for information about how to control circular or non-circular logging.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-148">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="9d175-148">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="9d175-149">Uno o varios de los miembros de <em>grbit</em> no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="9d175-149">One or more of the <em>grbit</em> members was invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-150">JET_errLoggingDisabled</span><span class="sxs-lookup"><span data-stu-id="9d175-150">JET_errLoggingDisabled</span></span></p></td>
<td><p><span data-ttu-id="9d175-151">La recuperación o el registro están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="9d175-151">Recovery or logging is disabled.</span></span> <span data-ttu-id="9d175-152">No se puede realizar una copia de seguridad en línea si el registro está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9d175-152">You cannot do an online backup if logging is disabled.</span></span> <span data-ttu-id="9d175-153">Para obtener más información sobre el registro y la recuperación, vea <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span><span class="sxs-lookup"><span data-stu-id="9d175-153">For more information about logging and recovery, see <a href="gg269235(v=exchg.10).md">JET_paramRecovery</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-154">JET_errLogWriteFail</span><span class="sxs-lookup"><span data-stu-id="9d175-154">JET_errLogWriteFail</span></span></p></td>
<td><p><span data-ttu-id="9d175-155">El motor ha dejado de escribir en la unidad de registro debido a que el registro está lleno o errores de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="9d175-155">The engine has stopped writing to the log drive, due to log being full or disk IO errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-156">JET_errMissingFullBackup</span><span class="sxs-lookup"><span data-stu-id="9d175-156">JET_errMissingFullBackup</span></span></p></td>
<td><p><span data-ttu-id="9d175-157">Se especificó la copia de seguridad incremental (con JET_bitBackupIncremental) y nunca se realizó una copia de seguridad completa para una de las bases de datos adjuntas del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="9d175-157">The incremental backup was specified (with JET_bitBackupIncremental), and never was a full backup taken for one of the attached databases for the logging set.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-158">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="9d175-158">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="9d175-159">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="9d175-159">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-160">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="9d175-160">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="9d175-161">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="9d175-161">The operation failed because not enough memory could be allocated to complete it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-162">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="9d175-162">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="9d175-163">No se puede completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9d175-163">The operation cannot complete because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-164">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="9d175-164">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="9d175-165">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="9d175-165">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-166">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="9d175-166">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="9d175-167">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="9d175-167">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9d175-168">Si la función se ejecuta correctamente, se inicia una copia de seguridad externa y se inicializa el motor de estado de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d175-168">If the function succeeds, an external backup is initiated and the backup state engine is initialized.</span></span> <span data-ttu-id="9d175-169">Ahora se puede llamar a las API subsiguientes para completar la secuencia de copia de seguridad externa y la secuencia o leer el archivo de base de datos, el archivo de revisión de la base de datos (si se admite) y el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="9d175-169">Subsequent APIs can now be called to complete the external backup sequence and stream or read off the database file, the database patch file (if supported), and the log file.</span></span> <span data-ttu-id="9d175-170">Se puede registrar un evento de que se ha iniciado una copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="9d175-170">An event can be logged that an external backup has begun.</span></span>

<span data-ttu-id="9d175-171">Si se produce un error en la función, no se iniciará la sesión de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d175-171">If the function fails, the backup session will not be initiated.</span></span> <span data-ttu-id="9d175-172">Si hay otra sesión de copia de seguridad en curso, no se cancelará.</span><span class="sxs-lookup"><span data-stu-id="9d175-172">If another backup session is in progress, it will not be cancelled.</span></span>

#### <a name="remarks"></a><span data-ttu-id="9d175-173">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d175-173">Remarks</span></span>

<span data-ttu-id="9d175-174">El proceso de copia de seguridad externo (tal y como lo inició **JetBeginExternalBackup**) está diseñado para permitir una copia de seguridad en línea de transacción aproximada de toda la instancia en un dispositivo de destino como un flujo.</span><span class="sxs-lookup"><span data-stu-id="9d175-174">The external backup process (as started by **JetBeginExternalBackup**) is designed to allow a fuzzy transaction online backup of the entire instance to a target device as a stream.</span></span> <span data-ttu-id="9d175-175">La copia de seguridad contendrá todos los archivos de base de datos que están asociados a la instancia de mediante [JetAttachDatabase](./jetattachdatabase-function.md) (para una copia de seguridad completa), seguidos de los archivos de revisión de la base de datos asociados (si se admiten) y, por último, los archivos de registro de transacciones que se generaron durante el proceso de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d175-175">The backup will contain all the database files that are attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) (for a full backup), followed by their associated database patch files (if supported), and finally by the transaction log files that were generated during the backup process.</span></span> <span data-ttu-id="9d175-176">El resultado final será un conjunto de archivos que se pueden restaurar a partir de la secuencia, posiblemente combinados con los archivos de registro y de base de datos existentes, y, por último, recuperarse a un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="9d175-176">The end result will be a set of files that can be restored from the stream, possibly combined with existing database and log files, and finally recovered to a consistent state.</span></span>

<span data-ttu-id="9d175-177">El orden general de las operaciones de una copia de seguridad completa consta de las siguientes llamadas.</span><span class="sxs-lookup"><span data-stu-id="9d175-177">The general order of operations for a full backup consists of the following calls.</span></span> <span data-ttu-id="9d175-178">En primer lugar, se llama a **JetBeginExternalBackup** para iniciar el proceso de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d175-178">First, **JetBeginExternalBackup** is called to start the backup process.</span></span> <span data-ttu-id="9d175-179">A continuación, se llama a [JetGetAttachInfo](./jetgetattachinfo-function.md) para obtener la lista de bases de datos que se adjuntan a la instancia de de la que es necesario hacer una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d175-179">Then, [JetGetAttachInfo](./jetgetattachinfo-function.md) is called to get the list of databases that are attached to the instance that needs to be backed up.</span></span> <span data-ttu-id="9d175-180">Para cada una de estas bases de datos, se llama a [JetOpenFile](./jetopenfile-function.md) , seguido de una serie de llamadas a [JetReadFile](./jetreadfile-function.md) y, a continuación, mediante una llamada a [JetCloseFile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="9d175-180">For each of these databases, [JetOpenFile](./jetopenfile-function.md) is called, followed by a number of [JetReadFile](./jetreadfile-function.md) calls, and then by a call to [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="9d175-181">A continuación, se llama a [JetGetLogInfo](./jetgetloginfo-function.md) para obtener una lista de los archivos de registro y revisión de la base de datos de los que se va a hacer una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d175-181">Then, [JetGetLogInfo](./jetgetloginfo-function.md) is called to get a list of database patch and log files to be backed up.</span></span> <span data-ttu-id="9d175-182">Para cada uno de estos archivos, se realiza otra secuencia de llamadas a [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md)y [JetCloseFile](./jetclosefile-function.md) .</span><span class="sxs-lookup"><span data-stu-id="9d175-182">For each of these files, another sequence of [JetOpenFile](./jetopenfile-function.md), [JetReadFile](./jetreadfile-function.md), and [JetCloseFile](./jetclosefile-function.md) calls are made.</span></span> <span data-ttu-id="9d175-183">A continuación, se eliminan los archivos de registro de transacciones no deseados con [JetTruncateLog](./jettruncatelog-function.md).</span><span class="sxs-lookup"><span data-stu-id="9d175-183">Then, any undesired transaction log files are deleted using [JetTruncateLog](./jettruncatelog-function.md).</span></span> <span data-ttu-id="9d175-184">Por último, la copia de seguridad finaliza mediante una llamada a [JetEndExternalBackup](./jetendexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="9d175-184">Finally, the backup is ended by a call to [JetEndExternalBackup](./jetendexternalbackup-function.md).</span></span>

<span data-ttu-id="9d175-185">También es posible modificar este conjunto de pasos para realizar una copia de seguridad incremental de la instancia.</span><span class="sxs-lookup"><span data-stu-id="9d175-185">It is also possible to modify this set of steps to perform an incremental backup of the instance.</span></span> <span data-ttu-id="9d175-186">Una copia de seguridad incremental enumera y realiza copias de seguridad de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="9d175-186">An incremental backup enumerates and backs up log files.</span></span> <span data-ttu-id="9d175-187">Las copias de seguridad incrementales solo son posibles si el registro circular no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9d175-187">Incremental backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="9d175-188">También es posible modificar este conjunto de pasos para permitir que se realicen copias de seguridad diferenciales posteriores de la instancia.</span><span class="sxs-lookup"><span data-stu-id="9d175-188">It is also possible to modify this set of steps to allow subsequent differential backups of the instance to be performed.</span></span> <span data-ttu-id="9d175-189">Para realizar una copia de seguridad diferencial, no llame a [JetTruncateLog](./jettruncatelog-function.md) en la copia de seguridad completa o incremental anterior.</span><span class="sxs-lookup"><span data-stu-id="9d175-189">To perform a differential backup, do not call [JetTruncateLog](./jettruncatelog-function.md) in the previous full or incremental backup.</span></span> <span data-ttu-id="9d175-190">Al no llamar a [JetTruncateLog](./jettruncatelog-function.md), las copias de seguridad posteriores se habilitan para que sean diferenciales con respecto a la última copia de seguridad completa o incremental.</span><span class="sxs-lookup"><span data-stu-id="9d175-190">By not calling [JetTruncateLog](./jettruncatelog-function.md), you enable subsequent backups to be differential with respect to the last full or incremental backup.</span></span> <span data-ttu-id="9d175-191">Las copias de seguridad diferenciales solo son posibles si el registro circular no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9d175-191">Differential backups are only possible if circular logging is not enabled.</span></span>

<span data-ttu-id="9d175-192">El archivo de revisión de la base de datos es un archivo auxiliar especial que se usa para almacenar imágenes de páginas de base de datos en determinadas circunstancias durante la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9d175-192">The database patch file is a special auxiliary file that is used to store database page images under certain circumstances during the backup.</span></span> <span data-ttu-id="9d175-193">Este archivo debe estar presente en la misma ubicación que su base de datos asociada durante una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="9d175-193">This file must be present in the same location as its associated database during a restore operation.</span></span> <span data-ttu-id="9d175-194">Este archivo solo se utiliza en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9d175-194">This file is only used in Windows 2000.</span></span> <span data-ttu-id="9d175-195">Como resultado, todas las aplicaciones escritas para funcionar en Windows 2000 y otras versiones deben admitir archivos de revisión de base de datos, si están presentes, pero tampoco deben generar errores si no están presentes.</span><span class="sxs-lookup"><span data-stu-id="9d175-195">As a result, any application that is written to work against Windows 2000 and other releases must support database patch files, if they are present, but also must not fail if they are not present.</span></span>

#### <a name="requirements"></a><span data-ttu-id="9d175-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d175-196">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d175-197"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9d175-197"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9d175-198">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9d175-198">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-199"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9d175-199"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9d175-200">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9d175-200">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-201"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9d175-201"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9d175-202">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="9d175-202">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d175-203"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="9d175-203"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="9d175-204">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="9d175-204">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d175-205"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="9d175-205"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="9d175-206">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="9d175-206">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="9d175-207">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9d175-207">See Also</span></span>

[<span data-ttu-id="9d175-208">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="9d175-208">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="9d175-209">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="9d175-209">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="9d175-210">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="9d175-210">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="9d175-211">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="9d175-211">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="9d175-212">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="9d175-212">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="9d175-213">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="9d175-213">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="9d175-214">JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="9d175-214">JetEndExternalBackup</span></span>](./jetendexternalbackup-function.md)  
[<span data-ttu-id="9d175-215">JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="9d175-215">JetEndExternalBackupInstance2</span></span>](./jetendexternalbackupinstance2-function.md)  
[<span data-ttu-id="9d175-216">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="9d175-216">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="9d175-217">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="9d175-217">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="9d175-218">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="9d175-218">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="9d175-219">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="9d175-219">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="9d175-220">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="9d175-220">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="9d175-221">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="9d175-221">JetTruncateLog</span></span>](./jettruncatelog-function.md)
