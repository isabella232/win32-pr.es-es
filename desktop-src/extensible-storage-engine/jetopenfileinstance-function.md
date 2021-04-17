---
description: 'Más información acerca de: JetOpenFileInstance (función)'
title: Función JetOpenFileInstance
TOCTitle: JetOpenFileInstance Function
ms:assetid: 44af9549-77ef-48f4-8580-507f7199f281
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269238(v=EXCHG.10)
ms:contentKeyID: 32765540
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileInstanceA
- JetOpenFileInstanceW
- JetOpenFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6065914fcd5b03d8c8b05996d57331a474ad7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697872"
---
# <a name="jetopenfileinstance-function"></a><span data-ttu-id="53da9-103">Función JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-103">JetOpenFileInstance Function</span></span>


<span data-ttu-id="53da9-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="53da9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfileinstance-function"></a><span data-ttu-id="53da9-105">Función JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-105">JetOpenFileInstance Function</span></span>

<span data-ttu-id="53da9-106">La función **JetOpenFileInstance** abre una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones de una instancia activa con el fin de realizar una copia de seguridad aproximada de streaming.</span><span class="sxs-lookup"><span data-stu-id="53da9-106">The **JetOpenFileInstance** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="53da9-107">Posteriormente, los datos de estos archivos se pueden leer a través del controlador devuelto mediante [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="53da9-107">The data from these files can subsequently be read through the returned handle using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span> <span data-ttu-id="53da9-108">El identificador devuelto debe cerrarse mediante [JetCloseFileInstance](./jetclosefileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="53da9-108">The returned handle must be closed using [JetCloseFileInstance](./jetclosefileinstance-function.md).</span></span> <span data-ttu-id="53da9-109">Se debe haber iniciado previamente una copia de seguridad externa de la instancia mediante [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="53da9-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md).</span></span>

<span data-ttu-id="53da9-110">**Windows XP:**  **JetOpenFileInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="53da9-110">**Windows XP:**  **JetOpenFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOpenFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_PCSTR szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="53da9-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="53da9-111">Parameters</span></span>

<span data-ttu-id="53da9-112">*repetición*</span><span class="sxs-lookup"><span data-stu-id="53da9-112">*instance*</span></span>

<span data-ttu-id="53da9-113">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="53da9-113">The instance to use for this call.</span></span>

<span data-ttu-id="53da9-114">En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="53da9-114">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="53da9-115">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="53da9-115">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="53da9-116">En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="53da9-116">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="53da9-117">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="53da9-117">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="53da9-118">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="53da9-118">*szFileName*</span></span>

<span data-ttu-id="53da9-119">Ruta de acceso absoluta o relativa a una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones administrado por la instancia de que se lee para la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="53da9-119">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that is read for backup.</span></span>

<span data-ttu-id="53da9-120">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="53da9-120">*phfFile*</span></span>

<span data-ttu-id="53da9-121">Puntero al búfer de salida que recibe un identificador del archivo que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="53da9-121">Pointer to the output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="53da9-122">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="53da9-122">*pulFileSizeLow*</span></span>

<span data-ttu-id="53da9-123">Puntero al búfer de salida que recibe los 32 bits menos significativos del tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="53da9-123">Pointer to the output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="53da9-124">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="53da9-124">*pulFileSizeHigh*</span></span>

<span data-ttu-id="53da9-125">Puntero al búfer de salida que recibe los 32 bits más significativos del tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="53da9-125">Pointer to the output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="53da9-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="53da9-126">Return Value</span></span>

<span data-ttu-id="53da9-127">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="53da9-127">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="53da9-128">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="53da9-128">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53da9-129">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="53da9-129">Return code</span></span></p></th>
<th><p><span data-ttu-id="53da9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="53da9-130">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53da9-131">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="53da9-131">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="53da9-132">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="53da9-132">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-133">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="53da9-133">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="53da9-134">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="53da9-134">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="53da9-135">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="53da9-135">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-136">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="53da9-136">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="53da9-137">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="53da9-137">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-138">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="53da9-138">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="53da9-139">No se pudo realizar la operación porque no se pudo abrir el archivo solicitado debido a una infracción de uso compartido o a privilegios insuficientes.</span><span class="sxs-lookup"><span data-stu-id="53da9-139">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-140">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="53da9-140">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="53da9-141">No se pudo realizar la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="53da9-141">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="53da9-142">Este error solo lo devolverá Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="53da9-142">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-143">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="53da9-143">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="53da9-144">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="53da9-144">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-145">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="53da9-145">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="53da9-146">No se pudo realizar la operación porque no se encontró la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="53da9-146">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="53da9-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="53da9-148">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="53da9-148">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="53da9-149">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="53da9-149">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-150">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="53da9-150">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="53da9-151">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="53da9-151">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="53da9-152">Esto puede ocurrir para <strong>JetOpenFileInstance</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="53da9-152">This can happen for <strong>JetOpenFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="53da9-153">El identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="53da9-153">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="53da9-154">El parámetro FILENAME especificado es NULL o una cadena de longitud cero (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="53da9-154">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-155">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="53da9-155">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="53da9-156">No se pudo abrir el archivo solicitado para la copia de seguridad porque no se encontró.</span><span class="sxs-lookup"><span data-stu-id="53da9-156">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="53da9-157">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="53da9-157">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-158">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="53da9-158">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="53da9-159">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="53da9-159">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-160">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="53da9-160">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="53da9-161">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="53da9-161">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-162">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="53da9-162">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="53da9-163">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="53da9-163">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="53da9-164"><strong>JetOpenFileInstance</strong> devolverá JET_errOutOfMemory si se intenta abrir otro archivo antes de que <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>haya cerrado el archivo anterior abierto con <strong>JetOpenFileInstance</strong> .</span><span class="sxs-lookup"><span data-stu-id="53da9-164"><strong>JetOpenFileInstance</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFileInstance</strong> has been closed by <a href="gg269270(v=exchg.10).md">JetCloseFileInstance</a>.</span></span> <span data-ttu-id="53da9-165">Actualmente solo se admite un identificador de archivo pendiente.</span><span class="sxs-lookup"><span data-stu-id="53da9-165">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-166">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="53da9-166">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="53da9-167">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="53da9-167">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-168">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="53da9-168">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="53da9-169">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="53da9-169">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-170">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="53da9-170">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="53da9-171">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="53da9-171">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="53da9-172">Si se ejecuta correctamente, se devuelve un identificador al archivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="53da9-172">On success, a handle to the requested file is returned.</span></span> <span data-ttu-id="53da9-173">Si el identificador es para un archivo de base de datos, ese archivo de base de datos se preparará para una copia de seguridad de secuencias, lo que puede dar lugar a la creación de un archivo de revisión de base de datos en la misma ubicación que el archivo de base de datos</span><span class="sxs-lookup"><span data-stu-id="53da9-173">If the handle is for a database file, that database file will be prepared for a streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="53da9-174">El archivo de revisión de la base de datos tiene exactamente la misma ruta de acceso y el mismo nombre que el archivo de base de datos, pero con un. Extensión PAT.</span><span class="sxs-lookup"><span data-stu-id="53da9-174">The database patch file has the exact same path and filename as the database file but with a .PAT extension.</span></span> <span data-ttu-id="53da9-175">También se devolverá el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="53da9-175">The size of the file will also be returned.</span></span>

<span data-ttu-id="53da9-176">En caso de error, el estado de los búferes de salida será undefined.</span><span class="sxs-lookup"><span data-stu-id="53da9-176">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="53da9-177">Un archivo de revisión de base de datos puede crearse temporalmente en el disco y se puede eliminar cualquier archivo existente en la ubicación del archivo de revisión.</span><span class="sxs-lookup"><span data-stu-id="53da9-177">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="53da9-178">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="53da9-178">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="53da9-179">En Windows XP y versiones posteriores, no se cancelará la copia de seguridad si se realiza un intento de hacer una copia de seguridad de una base de datos que no estaba asociada a la instancia en el momento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="53da9-179">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="53da9-180">**ADVERTENCIA**  de  Por motivos de seguridad, es importante tener en cuenta que **JetOpenFileInstance** no comprueba que la ruta de acceso del archivo solicitada esté asociada con el conjunto de archivos de los que se ha realizado una copia de seguridad para la instancia.</span><span class="sxs-lookup"><span data-stu-id="53da9-180">**Warning**  For security reasons, it is important to note that **JetOpenFileInstance** does not verify that the requested file path is associated with the set of files that are backed up for the instance.</span></span> <span data-ttu-id="53da9-181">Como resultado, es posible usar esta función para tener acceso a cualquier archivo que pueda abrir el contexto de seguridad actual del subproceso.</span><span class="sxs-lookup"><span data-stu-id="53da9-181">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="53da9-182">Es imperativo que la aplicación restrinja las rutas de acceso que se pasan a esta función a un conjunto conocido de rutas de acceso de archivos correctas o a la revelación del ataque de información.</span><span class="sxs-lookup"><span data-stu-id="53da9-182">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="53da9-183">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53da9-183">Remarks</span></span>

<span data-ttu-id="53da9-184">Es necesario que los búferes de salida de identificador y tamaño de archivo estén presentes.</span><span class="sxs-lookup"><span data-stu-id="53da9-184">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="53da9-185">Si no están presentes, el motor se bloqueará porque no se validan los parámetros del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="53da9-185">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="53da9-186">En este momento, solo se puede abrir un archivo para copia de seguridad al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="53da9-186">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="53da9-187">**JetOpenFileInstance** no valida el privilegio de copia de seguridad antes de abrir el archivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="53da9-187">**JetOpenFileInstance** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="53da9-188">Es posible que el tamaño del archivo que se va a leer tal como lo indique esta función no coincida con el tamaño del archivo en el disco.</span><span class="sxs-lookup"><span data-stu-id="53da9-188">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="53da9-189">En Windows XP y versiones posteriores, se puede anexar información adicional a un archivo de base de datos utilizado por el motor de base de datos durante una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="53da9-189">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="53da9-190">Como tal, la aplicación solo debe confiar en el tamaño de archivo devuelto por **JetOpenFileInstance** o en el número real de bytes de datos devueltos por [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="53da9-190">As such, the application should only rely on the file size returned by **JetOpenFileInstance** or on the actual number of bytes of data returned by [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="53da9-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53da9-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53da9-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="53da9-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="53da9-193">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="53da9-193">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="53da9-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="53da9-195">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="53da9-195">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="53da9-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="53da9-197">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="53da9-197">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-198"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="53da9-198"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="53da9-199">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="53da9-199">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53da9-200"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="53da9-200"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="53da9-201">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="53da9-201">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53da9-202"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="53da9-202"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="53da9-203">Se implementa como <strong>JetOpenFileInstanceW</strong> (Unicode) y <strong>JetOpenFileInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="53da9-203">Implemented as <strong>JetOpenFileInstanceW</strong> (Unicode) and <strong>JetOpenFileInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="53da9-204">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53da9-204">See Also</span></span>

[<span data-ttu-id="53da9-205">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="53da9-205">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="53da9-206">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="53da9-206">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="53da9-207">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="53da9-207">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="53da9-208">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="53da9-208">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="53da9-209">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-209">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="53da9-210">JetCloseFileInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-210">JetCloseFileInstance</span></span>](./jetclosefileinstance-function.md)  
[<span data-ttu-id="53da9-211">JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-211">JetGetAttachInfoInstance</span></span>](./jetgetattachinfoinstance-function.md)  
[<span data-ttu-id="53da9-212">JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-212">JetGetLogInfoInstance</span></span>](./jetgetloginfoinstance-function.md)  
[<span data-ttu-id="53da9-213">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-213">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="53da9-214">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-214">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="53da9-215">JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="53da9-215">JetTruncateLogInstance</span></span>](./jettruncateloginstance-function.md)
