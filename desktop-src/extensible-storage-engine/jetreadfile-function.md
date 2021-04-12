---
description: 'Más información acerca de: JetReadFile (función)'
title: JetReadFile función)
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277857"
---
# <a name="jetreadfile-function"></a><span data-ttu-id="2a395-103">JetReadFile función)</span><span class="sxs-lookup"><span data-stu-id="2a395-103">JetReadFile Function</span></span>


<span data-ttu-id="2a395-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2a395-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfile-function"></a><span data-ttu-id="2a395-105">JetReadFile función)</span><span class="sxs-lookup"><span data-stu-id="2a395-105">JetReadFile Function</span></span>

<span data-ttu-id="2a395-106">La función **JetReadFile** recupera el contenido de un archivo abierto con [JetOpenFile](./jetopenfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="2a395-106">The **JetReadFile** function retrieves the contents of a file opened with [JetOpenFile](./jetopenfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="2a395-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a395-107">Parameters</span></span>

<span data-ttu-id="2a395-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="2a395-108">*hfFile*</span></span>

<span data-ttu-id="2a395-109">Identificador del archivo que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="2a395-109">The handle of the file to be read.</span></span>

<span data-ttu-id="2a395-110">*FV*</span><span class="sxs-lookup"><span data-stu-id="2a395-110">*pv*</span></span>

<span data-ttu-id="2a395-111">Búfer de salida que recibirá los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="2a395-111">Output buffer that will receive the file data.</span></span>

<span data-ttu-id="2a395-112">*CB*</span><span class="sxs-lookup"><span data-stu-id="2a395-112">*cb*</span></span>

<span data-ttu-id="2a395-113">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="2a395-113">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="2a395-114">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="2a395-114">*pcbActual*</span></span>

<span data-ttu-id="2a395-115">Recibe la cantidad real de datos de archivo recuperados.</span><span class="sxs-lookup"><span data-stu-id="2a395-115">Receives the actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="2a395-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a395-116">Return Value</span></span>

<span data-ttu-id="2a395-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="2a395-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2a395-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2a395-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a395-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2a395-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="2a395-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a395-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a395-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2a395-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2a395-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2a395-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a395-123">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="2a395-123">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="2a395-124">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2a395-124">The operation failed because the current external backup has been aborted by a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span> <span data-ttu-id="2a395-125">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2a395-125">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a395-126">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2a395-126">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2a395-127">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2a395-127">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a395-128">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2a395-128">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2a395-129">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-129">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="2a395-130">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2a395-130">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a395-131">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2a395-131">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2a395-132">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="2a395-132">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="2a395-133">Esto puede ocurrir para <strong>JetReadFile</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="2a395-133">This can happen for <strong>JetReadFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="2a395-134">El identificador de instancia especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="2a395-134">The specified instance handle is invalid.</span></span> <span data-ttu-id="2a395-135">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2a395-135">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="2a395-136">El tamaño del búfer de salida no es múltiplo del tamaño de página de la base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="2a395-136">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="2a395-137">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2a395-137">Windows XP and later releases.</span></span></p></li>
<li><p><span data-ttu-id="2a395-138">El tamaño del búfer de salida es inferior a tres páginas de base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) y se trata de la primera llamada a <strong>JetReadFile</strong> para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="2a395-138">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) and this is the first call to <strong>JetReadFile</strong> for the specified handle.</span></span> <span data-ttu-id="2a395-139">Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2a395-139">Windows XP and later releases.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a395-140">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="2a395-140">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="2a395-141">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="2a395-141">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a395-142">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2a395-142">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2a395-143">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="2a395-143">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a395-144">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="2a395-144">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="2a395-145">No se pudo realizar la operación porque se detectaron daños en los datos no recuperables al leer una página de base de datos de un archivo de base de datos o un archivo de revisión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-145">The operation failed because non-recoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a395-146">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="2a395-146">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="2a395-147">No se pudo realizar la operación porque se detectaron daños en los datos no recuperables al leer un archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="2a395-147">The operation failed because non-recoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="2a395-148">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2a395-148">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a395-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2a395-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2a395-150">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="2a395-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a395-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="2a395-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="2a395-152">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="2a395-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a395-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2a395-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2a395-154">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="2a395-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a395-155">Si se ejecuta correctamente, el siguiente fragmento de datos del archivo se leerá en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="2a395-155">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="2a395-156">También se devolverá el número real de bytes recuperados.</span><span class="sxs-lookup"><span data-stu-id="2a395-156">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="2a395-157">El desplazamiento de archivo en el que se producirá la siguiente lectura será avanzado en esta cantidad.</span><span class="sxs-lookup"><span data-stu-id="2a395-157">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="2a395-158">En caso de error, el estado del búfer de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="2a395-158">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="2a395-159">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="2a395-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="2a395-160">En Windows XP y versiones posteriores, la copia de seguridad no se cancelará si se produce un error al leer un archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-160">On Windows XP and later releases, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="2a395-161">Sin embargo, se cancelará la copia de seguridad de ese archivo de base de datos y el identificador correspondiente se cerrará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2a395-161">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2a395-162">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a395-162">Remarks</span></span>

<span data-ttu-id="2a395-163">Cualquier llamada a **JetReadFile** con un identificador que ya ha devuelto todos los datos del archivo subyacente (como una llamada anterior devolvió menos bytes que el tamaño del búfer de salida) siempre se realizará correctamente pero devolverá cero bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-163">Any call to **JetReadFile** using a handle that has already returned all the data in the underlying file (such as a previous call returned less bytes than the size of the output buffer) will always succeed but return zero bytes of data.</span></span>

<span data-ttu-id="2a395-164">Se debe usar un búfer de salida grande para maximizar el rendimiento de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2a395-164">A large output buffer should be used to maximize backup performance.</span></span> <span data-ttu-id="2a395-165">Es posible que se requiera algún experimento para encontrar el equilibrio adecuado entre el consumo de recursos y el rendimiento de una situación determinada.</span><span class="sxs-lookup"><span data-stu-id="2a395-165">Some experimentation may be required to find the right tradeoff between resource consumption and throughput for a given situation.</span></span> <span data-ttu-id="2a395-166">En cualquier caso, el búfer de salida no debe ser inferior a 64 KB.</span><span class="sxs-lookup"><span data-stu-id="2a395-166">The output buffer should be no smaller than 64KB in any case.</span></span>

<span data-ttu-id="2a395-167">No se admiten varias llamadas simultáneas a **JetReadFile** con el mismo identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="2a395-167">Multiple concurrent calls to **JetReadFile** using the same file handle are not supported.</span></span> <span data-ttu-id="2a395-168">Esto significa que no es posible poner en cola varios búferes para lectura simultáneamente en el mismo archivo para lograr un alto rendimiento secuencial.</span><span class="sxs-lookup"><span data-stu-id="2a395-168">This means that it is not possible to queue several buffers for read concurrently against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="2a395-169">En su lugar, se debe usar un único búfer grande.</span><span class="sxs-lookup"><span data-stu-id="2a395-169">A single large buffer should be used instead.</span></span>

<span data-ttu-id="2a395-170">Si la instancia de está configurada de modo que la limpieza de páginas de la base de datos está habilitada (vea JET_paramZeroDatabaseDuringBackup en parámetros del sistema), los datos eliminados se quitarán de la base de datos como un efecto secundario de una llamada a **JetReadFile** en el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-170">If the instance is configured such that database page scrubbing is enabled (see JET_paramZeroDatabaseDuringBackup in System Parameters) then deleted data will be removed from the database as a side effect of a call to **JetReadFile** against the database file.</span></span>

<span data-ttu-id="2a395-171">Es muy importante entender cómo interactúan la copia de seguridad y los datos dañados.</span><span class="sxs-lookup"><span data-stu-id="2a395-171">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="2a395-172">Si el motor de base de datos detecta daños en los datos durante una copia de seguridad, se producirá un error en la copia de seguridad de la base de datos afectada o de toda la instancia.</span><span class="sxs-lookup"><span data-stu-id="2a395-172">If the database engine detects data corruption during a backup then it will either fail the backup of the affected database or of the entire instance.</span></span> <span data-ttu-id="2a395-173">Se trata de una decisión de diseño consciente destinada a protegerse contra la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-173">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="2a395-174">Si el motor de base de datos permitía que una copia de seguridad se realizara correctamente y hubiera daños en los datos, es posible que una copia de seguridad no dañada anterior se descartase como resultado.</span><span class="sxs-lookup"><span data-stu-id="2a395-174">If the database engine allowed a backup to succeed where data corruption was present then it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="2a395-175">Esto sería desafortunado porque sería posible corregir los datos dañados en la instancia en directo restaurando esa copia de seguridad y reproduciendo todos los archivos de registro de transacciones en esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-175">This would be unfortunate because it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="2a395-176">Este escenario de cero pérdida de datos presupone que el registro circular no está habilitado (vea [JET_paramCircularLog](./transaction-log-parameters.md) en [parámetros del sistema](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="2a395-176">This zero data loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="2a395-177">También es importante comprender que, cuando se dañen los datos, la copia de seguridad de transmisión por secuencias es el lugar más probable que se detecte primero.</span><span class="sxs-lookup"><span data-stu-id="2a395-177">It is also important to understand that when data corruption is present streaming backup will be the most likely place that it will first be detected.</span></span> <span data-ttu-id="2a395-178">Esto se debe a que la copia de seguridad de secuencias es el único proceso que examina rutinariamente cada una de las páginas del archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-178">This is the case because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="2a395-179">También es probable que la copia de seguridad de transmisión por secuencias sea el primer proceso para detectar los primeros síntomas de errores de hardware, tal como están manifiestos de errores intermitentes de daños en los datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-179">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors.</span></span> <span data-ttu-id="2a395-180">Esto se debe a la cantidad de datos recuperados por la copia de seguridad, así como a la velocidad a la que se recupera.</span><span class="sxs-lookup"><span data-stu-id="2a395-180">This is due to the amount of data retrieved by backup as well as the speed at which it is retrieved.</span></span>

<span data-ttu-id="2a395-181">El motor de base de datos detecta los daños en los datos mediante el uso de sumas de comprobación de bloques.</span><span class="sxs-lookup"><span data-stu-id="2a395-181">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="2a395-182">Estas sumas de comprobación se establecen justo antes de la escritura de una página de base de datos y se comprueban en una lectura de página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-182">These checksums are set just prior to a database page write and are verified on a database page read.</span></span> <span data-ttu-id="2a395-183">Este esquema permite al motor de base de datos determinar que los datos se han dañado en algún momento, pero no permite que el motor de base de datos determine el origen de dichos daños.</span><span class="sxs-lookup"><span data-stu-id="2a395-183">This scheme enables the database engine to determine that data has been corrupted at some point but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="2a395-184">Históricamente, se encontró que la causa predominante de estos daños proviene de orígenes distintos del propio motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="2a395-184">Historically, the predominant cause of such corruption has been found to come from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2a395-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a395-185">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a395-186"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2a395-186"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2a395-187">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2a395-187">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a395-188"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2a395-188"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2a395-189">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2a395-189">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a395-190"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2a395-190"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2a395-191">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="2a395-191">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a395-192"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="2a395-192"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2a395-193">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2a395-193">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a395-194"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2a395-194"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2a395-195">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2a395-195">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2a395-196">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2a395-196">See Also</span></span>

[<span data-ttu-id="2a395-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2a395-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2a395-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="2a395-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="2a395-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2a395-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2a395-200">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="2a395-200">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="2a395-201">JetStopService</span><span class="sxs-lookup"><span data-stu-id="2a395-201">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="2a395-202">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="2a395-202">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
