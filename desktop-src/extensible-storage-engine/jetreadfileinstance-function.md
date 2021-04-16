---
description: 'Más información acerca de: JetReadFileInstance (función)'
title: Función JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539971"
---
# <a name="jetreadfileinstance-function"></a><span data-ttu-id="fa7ab-103">Función JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="fa7ab-103">JetReadFileInstance Function</span></span>


<span data-ttu-id="fa7ab-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fa7ab-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetreadfileinstance-function"></a><span data-ttu-id="fa7ab-105">Función JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="fa7ab-105">JetReadFileInstance Function</span></span>

<span data-ttu-id="fa7ab-106">La función **JetReadFileInstance** recupera el contenido de un archivo abierto con la función [JetOpenFileInstance](./jetopenfileinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="fa7ab-106">The **JetReadFileInstance** function retrieves the contents of a file opened with the [JetOpenFileInstance](./jetopenfileinstance-function.md) function.</span></span>

<span data-ttu-id="fa7ab-107">**Windows XP**:   **JetReadFileInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-107">**Windows XP**:   **JetReadFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a><span data-ttu-id="fa7ab-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa7ab-108">Parameters</span></span>

<span data-ttu-id="fa7ab-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="fa7ab-109">*instance*</span></span>

<span data-ttu-id="fa7ab-110">Instancia de que se va a usar para una llamada de API determinada.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-110">The instance to use for a particular API call.</span></span>

<span data-ttu-id="fa7ab-111">Tenga en cuenta que para Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-111">Note that for Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="fa7ab-112">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="fa7ab-113">En Windows XP y versiones posteriores, puede llamar a la variante de API que no acepta este parámetro solo cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000) en casos en los que solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-113">For Windows XP and later releases, you can call the API variant that does not accept this parameter only when the engine is in legacy mode (Windows 2000 compatibility mode) in cases where only one instance is supported.</span></span> <span data-ttu-id="fa7ab-114">De lo contrario, se producirá un error en la operación y se devolverá el error JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-114">Otherwise, the operation will fail and return the JET_errRunningInMultiInstanceMode error.</span></span>

<span data-ttu-id="fa7ab-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="fa7ab-115">*hfFile*</span></span>

<span data-ttu-id="fa7ab-116">Identificador del archivo que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-116">The handle of the file to be read.</span></span>

<span data-ttu-id="fa7ab-117">*FV*</span><span class="sxs-lookup"><span data-stu-id="fa7ab-117">*pv*</span></span>

<span data-ttu-id="fa7ab-118">Búfer de salida que recibirá los datos del archivo.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-118">The output buffer that will receive the file data.</span></span>

<span data-ttu-id="fa7ab-119">*CB*</span><span class="sxs-lookup"><span data-stu-id="fa7ab-119">*cb*</span></span>

<span data-ttu-id="fa7ab-120">Tamaño máximo, en bytes, del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-120">The maximum size, in bytes, of the output buffer.</span></span>

<span data-ttu-id="fa7ab-121">*impreso*</span><span class="sxs-lookup"><span data-stu-id="fa7ab-121">*pcb*</span></span>

<span data-ttu-id="fa7ab-122">La cantidad real de datos de archivo recuperados.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-122">The actual amount of file data retrieved.</span></span>

### <a name="return-value"></a><span data-ttu-id="fa7ab-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa7ab-123">Return Value</span></span>

<span data-ttu-id="fa7ab-124">Esta función facilita la devolución de los tipos de datos [JET_ERR](./jet-err.md) definidos en la API del motor de almacenamiento extensible (ese).</span><span class="sxs-lookup"><span data-stu-id="fa7ab-124">This function facilitates the return of any [JET_ERR](./jet-err.md) data types that are defined in the Extensible Storage Engine (ESE) API.</span></span> <span data-ttu-id="fa7ab-125">Para obtener más información acerca de los errores de JET, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fa7ab-125">For more information about JET errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa7ab-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fa7ab-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="fa7ab-127">Significado</span><span class="sxs-lookup"><span data-stu-id="fa7ab-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fa7ab-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-129">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa7ab-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="fa7ab-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-131">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a la función <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="fa7ab-131">The operation failed because the current external backup has been aborted by a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span> <span data-ttu-id="fa7ab-132">Este error solo se devolverá en Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-132">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-133">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fa7ab-133">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-134">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a la función <a href="gg269240(v=exchg.10).md">JetStopService</a> .</span><span class="sxs-lookup"><span data-stu-id="fa7ab-134">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to the <a href="gg269240(v=exchg.10).md">JetStopService</a> function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa7ab-135">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fa7ab-135">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-136">No es posible completar la operación porque la instancia asociada a la sesión ha detectado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-136">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error requiring that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="fa7ab-137">Este error solo se devolverá en Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-137">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-138">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fa7ab-138">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-139">Uno de los parámetros especificados contenía un valor inesperado o un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-139">One of the specified parameters contained either an unexpected value or a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="fa7ab-140">Esto puede ocurrir para la función <strong>JetReadFileInstance</strong> cuando se produce cualquiera de las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="fa7ab-140">This can happen for the <strong>JetReadFileInstance</strong> function when any of the following occurs:</span></span></p>
<ul>
<li><p><span data-ttu-id="fa7ab-141">El identificador de instancia especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-141">The specified instance handle is invalid.</span></span> <span data-ttu-id="fa7ab-142">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-142">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="fa7ab-143">El tamaño del búfer de salida no es múltiplo del tamaño de página de la base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="fa7ab-143">The output buffer size is not a multiple of the database page size (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>).</span></span> <span data-ttu-id="fa7ab-144">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-144">Windows XP and later Windows versions.</span></span></p></li>
<li><p><span data-ttu-id="fa7ab-145">El tamaño del búfer de salida es inferior a tres páginas de base de datos (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), y esta es la primera llamada a la función <strong>JetReadFileInstance</strong> para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-145">The output buffer size is smaller than three database pages (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), and this is the first call to the <strong>JetReadFileInstance</strong> function for the specified handle.</span></span> <span data-ttu-id="fa7ab-146">Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-146">Windows XP and later Windows versions.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa7ab-147">JET_errLogReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="fa7ab-147">JET_errLogReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-148">No se pudo realizar la operación porque se detectaron daños en los datos irrecuperables al leer un archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-148">The operation failed because unrecoverable data corruption was detected while reading a transaction log file.</span></span> <span data-ttu-id="fa7ab-149">Este error solo se devolverá en Windows XP y versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-149">This error will be returned only by Windows XP and later Windows versions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="fa7ab-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-151">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa7ab-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fa7ab-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-153">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-153">It is not possible to complete the operation because the instance associated with this session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-154">JET_errReadVerifyFailure</span><span class="sxs-lookup"><span data-stu-id="fa7ab-154">JET_errReadVerifyFailure</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-155">No se pudo realizar la operación porque se detectaron daños en los datos irrecuperables al leer una página de base de datos de un archivo de base de datos o un archivo de revisión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-155">The operation failed because unrecoverable data corruption was detected while reading a database page from a database file or database patch file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa7ab-156">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fa7ab-156">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-157">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-157">It is not possible to complete the operation because a restore operation is in progress on the instance associated with this session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-158">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="fa7ab-158">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-159">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000) en un caso en el que solo se admite una instancia, pero ya existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-159">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) in a case where only one instance is supported but multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa7ab-160">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fa7ab-160">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-161">No es posible completar la operación porque se está cerrando la instancia asociada a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-161">It is not possible to complete the operation because the instance associated with this session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fa7ab-162">Si se ejecuta correctamente, el siguiente fragmento de datos del archivo se leerá en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-162">On success, the next chunk of data from the file will be read into the output buffer.</span></span> <span data-ttu-id="fa7ab-163">También se devolverá el número real de bytes recuperados.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-163">The actual number of bytes retrieved will also be returned.</span></span> <span data-ttu-id="fa7ab-164">El desplazamiento de archivo en el que se producirá la siguiente lectura será avanzado en esta cantidad.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-164">The file offset at which the next read will occur will be advanced by this amount.</span></span>

<span data-ttu-id="fa7ab-165">En caso de error, el estado del búfer de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-165">On failure, the state of the output buffer is undefined.</span></span> <span data-ttu-id="fa7ab-166">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-166">The failure will result in the cancellation of the entire backup process for the current instance.</span></span> <span data-ttu-id="fa7ab-167">En Windows XP y versiones posteriores de Windows, la copia de seguridad no se cancelará si se produce un error al leer un archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-167">In Windows XP and later Windows versions, the backup will not be canceled if an error occurred while reading a database file.</span></span> <span data-ttu-id="fa7ab-168">Sin embargo, se cancelará la copia de seguridad de ese archivo de base de datos y el identificador correspondiente se cerrará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-168">However, the backup of that database file will still be canceled and the corresponding handle will automatically be closed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fa7ab-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa7ab-169">Remarks</span></span>

<span data-ttu-id="fa7ab-170">Cualquier llamada a la función **JetReadFileInstance** realizada mediante un identificador que ya ha devuelto todos los datos en el archivo subyacente (por ejemplo, si una llamada anterior ha devuelto menos bytes que el tamaño del búfer de salida) siempre se realizará correctamente, pero devolverá cero bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-170">Any call to the **JetReadFileInstance** function made by using a handle that has already returned all the data in the underlying file (such as if a previous call returned fewer bytes than the size of the output buffer) will always succeed but will return zero bytes of data.</span></span>

<span data-ttu-id="fa7ab-171">Debe usar un búfer de salida grande para maximizar el rendimiento de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-171">You should use a large output buffer to maximize backup performance.</span></span> <span data-ttu-id="fa7ab-172">Es posible que tenga que experimentar para encontrar el equilibrio óptimo entre el consumo de recursos y el rendimiento para una situación determinada.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-172">You might need to experiment to find the optimal tradeoff between resource consumption and throughput for a particular situation.</span></span> <span data-ttu-id="fa7ab-173">En cualquier caso, el búfer de salida no debe ser inferior a 64 KB.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-173">In any case, the output buffer should be no smaller than 64 KB.</span></span> <span data-ttu-id="fa7ab-174">El puntero que se pasa a **JetReadFileInstance** debe estar alineado con un límite de página de memoria (4 KB u 8 KB).</span><span class="sxs-lookup"><span data-stu-id="fa7ab-174">The pointer that you pass to **JetReadFileInstance** must be aligned with a memory page boundary (either 4 KB or 8 KB).</span></span> <span data-ttu-id="fa7ab-175">Para ello, puede llamar a la función **VirtualAlloc** .</span><span class="sxs-lookup"><span data-stu-id="fa7ab-175">You can do this by calling the **VirtualAlloc** function.</span></span>

<span data-ttu-id="fa7ab-176">No se admiten varias llamadas simultáneas a **JetReadFileInstance** realizadas con el mismo identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-176">Multiple concurrent calls to **JetReadFileInstance** made by using the same file handle are not supported.</span></span> <span data-ttu-id="fa7ab-177">Esto significa que no es posible poner en cola varios búferes para la lectura simultánea en el mismo archivo para lograr un alto rendimiento secuencial.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-177">This means that it is not possible to queue several buffers for concurrent reading against the same file to achieve high sequential throughput.</span></span> <span data-ttu-id="fa7ab-178">En su lugar, debe usar un único búfer grande.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-178">You should use a single large buffer instead.</span></span>

<span data-ttu-id="fa7ab-179">Si ha configurado una instancia determinada de modo que la limpieza de páginas de la base de datos esté habilitada (vea el parámetro [JET_paramCircularLog](./transaction-log-parameters.md) en [parámetros del sistema](./extensible-storage-engine-system-parameters.md)), los datos eliminados se quitarán de la base de datos como efecto secundario de una llamada a **JetReadFileInstance** en el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-179">If you have configured a particular instance such that database page scrubbing is enabled (see the [JET_paramCircularLog](./transaction-log-parameters.md) parameter in [System Parameters](./extensible-storage-engine-system-parameters.md)), deleted data will be removed from the database as a side-effect of a call to **JetReadFileInstance** against the database file.</span></span>

<span data-ttu-id="fa7ab-180">Es muy importante entender cómo interactúan la copia de seguridad y los datos dañados.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-180">It is very important to understand how backup and data corruption interact.</span></span> <span data-ttu-id="fa7ab-181">Si el motor de base de datos detecta daños en los datos durante una copia de seguridad, se producirá un error en la copia de seguridad de la base de datos afectada o de toda la instancia.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-181">If the database engine detects data corruption during a backup, it will fail the backup of either the affected database or the entire instance.</span></span> <span data-ttu-id="fa7ab-182">Se trata de una decisión de diseño consciente destinada a protegerse contra la pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-182">This is a conscious design decision intended to protect against data loss.</span></span> <span data-ttu-id="fa7ab-183">Si el motor de base de datos permitía que una copia de seguridad se realizara correctamente y hubiera daños en los datos, es posible que una copia de seguridad no dañada anterior se descartase como resultado.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-183">If the database engine allowed a backup to succeed where data corruption was present, it is possible that an older, uncorrupted backup could be discarded as a result.</span></span> <span data-ttu-id="fa7ab-184">Esto sería desafortunado porque después sería posible corregir los datos dañados en la instancia en directo restaurando esa copia de seguridad y reproduciendo todos los archivos de registro de transacciones en esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-184">This would be unfortunate because then it would be possible to fix the data corruption on the live instance by restoring that backup and replaying all the transaction log files against that database.</span></span> <span data-ttu-id="fa7ab-185">En este escenario de pérdida de datos cero se presupone que el registro circular no está habilitado (vea [JET_paramCircularLog](./transaction-log-parameters.md) en [parámetros del sistema](./extensible-storage-engine-system-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="fa7ab-185">This zero-data-loss scenario presumes that circular logging is not enabled (see [JET_paramCircularLog](./transaction-log-parameters.md) in [System Parameters](./extensible-storage-engine-system-parameters.md)).</span></span>

<span data-ttu-id="fa7ab-186">También es importante comprender que los casos de daños en los datos normalmente se detectan primero durante la copia de seguridad de streaming.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-186">It is also important to understand that cases of data corruption are usually first detected during streaming backup.</span></span> <span data-ttu-id="fa7ab-187">Esto se debe a que la copia de seguridad de secuencias es el único proceso que examina rutinariamente cada una de las páginas del archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-187">This is because streaming backup is the only process that routinely scans every single page of the database file.</span></span> <span data-ttu-id="fa7ab-188">También es probable que la copia de seguridad de transmisión por secuencias sea el primer proceso para detectar los primeros síntomas de errores de hardware como manifiestos de errores intermitentes de daños en los datos, debido a la cantidad de datos recuperados por la copia de seguridad y a la velocidad a la que se recuperan los datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-188">It is also likely that streaming backup will be the first process to detect the early signs of hardware failure as manifested by intermittent data corruption errors, because of both the amount of data retrieved by backup and the speed at which that data is retrieved.</span></span>

<span data-ttu-id="fa7ab-189">El motor de base de datos detecta los daños en los datos mediante el uso de sumas de comprobación de bloques.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-189">Data corruption is detected by the database engine through the use of block checksums.</span></span> <span data-ttu-id="fa7ab-190">Estas sumas de comprobación se establecen justo antes de que se escriba una página de base de datos y se comprueban en una lectura de página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-190">These checksums are set just before a database page write and are verified on a database page read.</span></span> <span data-ttu-id="fa7ab-191">Este esquema permite al motor de base de datos determinar que los datos se han dañado en algún momento, pero no permite que el motor de base de datos determine el origen de dichos daños.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-191">This scheme enables the database engine to determine that data has been corrupted at some point, but it does not enable the database engine to determine the source of that corruption.</span></span> <span data-ttu-id="fa7ab-192">Históricamente, las instancias de estos daños en los datos se originaron a partir de orígenes distintos del propio motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-192">Historically, instances of such data corruption have originated from sources other than the database engine itself.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fa7ab-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa7ab-193">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-194">Remoto</span><span class="sxs-lookup"><span data-stu-id="fa7ab-194">Client</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-195">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-195">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa7ab-196">Servidor</span><span class="sxs-lookup"><span data-stu-id="fa7ab-196">Server</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-197">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-197">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-198">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa7ab-198">Header</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-199">Se declara en esent. h.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-199">Is declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa7ab-200">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa7ab-200">Library</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-201">Utiliza ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-201">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa7ab-202">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa7ab-202">DLL</span></span></p></td>
<td><p><span data-ttu-id="fa7ab-203">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fa7ab-203">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fa7ab-204">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fa7ab-204">See Also</span></span>

[<span data-ttu-id="fa7ab-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fa7ab-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fa7ab-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="fa7ab-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="fa7ab-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="fa7ab-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="fa7ab-208">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="fa7ab-208">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="fa7ab-209">JetStopService</span><span class="sxs-lookup"><span data-stu-id="fa7ab-209">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="fa7ab-210">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="fa7ab-210">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
