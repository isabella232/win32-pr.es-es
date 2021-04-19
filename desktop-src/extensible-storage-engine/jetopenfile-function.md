---
description: 'Más información acerca de: JetOpenFile (función)'
title: Función JetOpenFile
TOCTitle: JetOpenFile Function
ms:assetid: 52f69050-ca1c-4a6b-a188-22bd7cb96bf5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269249(v=EXCHG.10)
ms:contentKeyID: 32765551
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenFileW
- JetOpenFile
- JetOpenFileA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2996ffc46e2f6b37cdfec12cd4ee2fc62efa188a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696218"
---
# <a name="jetopenfile-function"></a><span data-ttu-id="61c1c-103">Función JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="61c1c-103">JetOpenFile Function</span></span>


<span data-ttu-id="61c1c-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="61c1c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopenfile-function"></a><span data-ttu-id="61c1c-105">Función JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="61c1c-105">JetOpenFile Function</span></span>

<span data-ttu-id="61c1c-106">La función **JetOpenFile** abre una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones de una instancia activa con el fin de realizar una copia de seguridad aproximada de streaming.</span><span class="sxs-lookup"><span data-stu-id="61c1c-106">The **JetOpenFile** function opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="61c1c-107">Posteriormente, los datos de estos archivos se pueden leer a través del controlador devuelto mediante [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="61c1c-107">The data from these files can subsequently be read through the returned handle using [JetReadFile](./jetreadfile-function.md).</span></span> <span data-ttu-id="61c1c-108">El identificador devuelto debe cerrarse mediante [JetCloseFile](./jetclosefile-function.md).</span><span class="sxs-lookup"><span data-stu-id="61c1c-108">The returned handle must be closed using [JetCloseFile](./jetclosefile-function.md).</span></span> <span data-ttu-id="61c1c-109">Se debe haber iniciado previamente una copia de seguridad externa de la instancia mediante [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="61c1c-109">An external backup of the instance must have been previously initiated using [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

```cpp
    JET_ERR JET_API JetOpenFile(
      __in          const tchar* szFileName,
      __out         JET_HANDLE* phfFile,
      __out         unsigned long* pulFileSizeLow,
      __out         unsigned long* pulFileSizeHigh
    );
```

### <a name="parameters"></a><span data-ttu-id="61c1c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61c1c-110">Parameters</span></span>

<span data-ttu-id="61c1c-111">*szFileName*</span><span class="sxs-lookup"><span data-stu-id="61c1c-111">*szFileName*</span></span>

<span data-ttu-id="61c1c-112">Ruta de acceso absoluta o relativa a una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones administrado por la instancia de que se leerá para la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="61c1c-112">The relative or absolute path to an attached database, database patch file, or transaction log file managed by the instance that will be read for backup.</span></span>

<span data-ttu-id="61c1c-113">*phfFile*</span><span class="sxs-lookup"><span data-stu-id="61c1c-113">*phfFile*</span></span>

<span data-ttu-id="61c1c-114">Búfer de salida que recibe un identificador del archivo que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="61c1c-114">The output buffer that receives a handle to the file to be read.</span></span>

<span data-ttu-id="61c1c-115">*pulFileSizeLow*</span><span class="sxs-lookup"><span data-stu-id="61c1c-115">*pulFileSizeLow*</span></span>

<span data-ttu-id="61c1c-116">Búfer de salida que recibe los 32 bits menos significativos del tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="61c1c-116">The output buffer that receives the least significant 32 bits of the size of the file.</span></span>

<span data-ttu-id="61c1c-117">*pulFileSizeHigh*</span><span class="sxs-lookup"><span data-stu-id="61c1c-117">*pulFileSizeHigh*</span></span>

<span data-ttu-id="61c1c-118">Búfer de salida que recibe los 32 bits más significativos del tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="61c1c-118">The output buffer that receives the most significant 32 bits of the size of the file.</span></span>

### <a name="return-value"></a><span data-ttu-id="61c1c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61c1c-119">Return Value</span></span>

<span data-ttu-id="61c1c-120">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="61c1c-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="61c1c-121">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="61c1c-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61c1c-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="61c1c-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="61c1c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="61c1c-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="61c1c-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="61c1c-125">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="61c1c-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-126">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="61c1c-126">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="61c1c-127">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="61c1c-127">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="61c1c-128">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61c1c-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-129">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="61c1c-129">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="61c1c-130">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="61c1c-130">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-131">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="61c1c-131">JET_errFileAccessDenied</span></span></p></td>
<td><p><span data-ttu-id="61c1c-132">No se pudo realizar la operación porque no se pudo abrir el archivo solicitado debido a una infracción de uso compartido o a privilegios insuficientes.</span><span class="sxs-lookup"><span data-stu-id="61c1c-132">The operation failed because it could not open the requested file due to a sharing violation or insufficient privileges.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-133">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="61c1c-133">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="61c1c-134">No se pudo realizar la operación porque no se pudo abrir el archivo solicitado porque no se encontró en la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="61c1c-134">The operation failed because it could not open the requested file because it could not be found at the specified path.</span></span> <span data-ttu-id="61c1c-135">Este error solo lo devolverá Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="61c1c-135">This error will only be returned by Windows 2000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="61c1c-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="61c1c-137">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="61c1c-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="61c1c-138">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61c1c-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="61c1c-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="61c1c-140">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="61c1c-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-141">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="61c1c-141">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="61c1c-142">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="61c1c-142">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="61c1c-143">Esto puede ocurrir para <strong>JetOpenFile</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="61c1c-143">This can happen for <strong>JetOpenFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="61c1c-144">El identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="61c1c-144">The specified instance handle is invalid (Windows XP and later releases).</span></span></p></li>
<li><p><span data-ttu-id="61c1c-145">El parámetro FILENAME especificado es NULL o una cadena de longitud cero (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="61c1c-145">The specified filename parameter is NULL or a zero length string (Windows XP and later releases).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-146">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="61c1c-146">JET_errInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="61c1c-147">No se pudo realizar la operación porque no se encontró la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="61c1c-147">The operation failed because the specified path could not be found.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-148">JET_errMissingFileToBackup</span><span class="sxs-lookup"><span data-stu-id="61c1c-148">JET_errMissingFileToBackup</span></span></p></td>
<td><p><span data-ttu-id="61c1c-149">No se pudo abrir el archivo solicitado para la copia de seguridad porque no se encontró.</span><span class="sxs-lookup"><span data-stu-id="61c1c-149">The requested file could not be opened for backup because it could not be found.</span></span> <span data-ttu-id="61c1c-150">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="61c1c-150">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-151">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="61c1c-151">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="61c1c-152">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="61c1c-152">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-153">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="61c1c-153">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="61c1c-154">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="61c1c-154">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-155">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="61c1c-155">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="61c1c-156">No se pudo realizar la operación porque no se pudo asignar suficiente memoria para completarla.</span><span class="sxs-lookup"><span data-stu-id="61c1c-156">The operation failed because not enough memory could be allocated to complete it.</span></span> <span data-ttu-id="61c1c-157"><strong>JetOpenFile</strong> devolverá JET_errOutOfMemory si se intenta abrir otro archivo antes de que <a href="gg294127(v=exchg.10).md">JetCloseFile</a>haya cerrado el archivo anterior abierto con <strong>JetOpenFile</strong> .</span><span class="sxs-lookup"><span data-stu-id="61c1c-157"><strong>JetOpenFile</strong> will return JET_errOutOfMemory if an attempt is made to open another file before the previous file opened using <strong>JetOpenFile</strong> has been closed by <a href="gg294127(v=exchg.10).md">JetCloseFile</a>.</span></span> <span data-ttu-id="61c1c-158">Actualmente solo se admite un identificador de archivo pendiente.</span><span class="sxs-lookup"><span data-stu-id="61c1c-158">Only one outstanding file handle is currently supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-159">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="61c1c-159">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="61c1c-160">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="61c1c-160">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-161">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="61c1c-161">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="61c1c-162">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="61c1c-162">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span> <span data-ttu-id="61c1c-163">JET_errRestoreInProgress no es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="61c1c-163">JET_errRestoreInProgress It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="61c1c-164">Si se ejecuta correctamente, se devolverá un identificador al archivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="61c1c-164">On success, a handle to the requested file will be returned.</span></span> <span data-ttu-id="61c1c-165">Si el identificador es para un archivo de base de datos, ese archivo de base de datos se preparará para la copia de seguridad de transmisión por secuencias, lo que puede dar lugar a la creación de un archivo de revisión de la base de datos en la misma ubicación que el archivo</span><span class="sxs-lookup"><span data-stu-id="61c1c-165">If the handle is for a database file, that database file will be prepared for streaming backup which may result in the creation of a database patch file in the same location as the database file.</span></span> <span data-ttu-id="61c1c-166">El archivo de revisión de la base de datos tiene exactamente la misma ruta de acceso y el mismo nombre que el archivo de base de datos, pero tiene un. Extensión PAT.</span><span class="sxs-lookup"><span data-stu-id="61c1c-166">The database patch file has the exact same path and filename as the database file, but has a .PAT extension.</span></span> <span data-ttu-id="61c1c-167">También se devolverá el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="61c1c-167">The size of the file will also be returned.</span></span>

<span data-ttu-id="61c1c-168">En caso de error, el estado de los búferes de salida será undefined.</span><span class="sxs-lookup"><span data-stu-id="61c1c-168">On failure, the state of the output buffers will be undefined.</span></span> <span data-ttu-id="61c1c-169">Un archivo de revisión de base de datos puede crearse temporalmente en el disco y se puede eliminar cualquier archivo existente en la ubicación del archivo de revisión.</span><span class="sxs-lookup"><span data-stu-id="61c1c-169">A database patch file may be temporarily created on disk and any existing file at the patch file location may be deleted.</span></span> <span data-ttu-id="61c1c-170">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="61c1c-170">The failure will result in the cancellation of the entire backup process for the instance.</span></span> <span data-ttu-id="61c1c-171">En Windows XP y versiones posteriores, no se cancelará la copia de seguridad si se realiza un intento de hacer una copia de seguridad de una base de datos que no estaba asociada a la instancia en el momento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="61c1c-171">On Windows XP and later releases, the backup will not be canceled if an attempt was made to backup a database that was not attached to the instance at the time of the call.</span></span>

<span data-ttu-id="61c1c-172">**ADVERTENCIA**  de  Por motivos de seguridad, es importante tener en cuenta que **JetOpenFile** no comprueba que la ruta de acceso del archivo solicitada esté asociada con el conjunto de archivos de los que se debe realizar una copia de seguridad para la instancia.</span><span class="sxs-lookup"><span data-stu-id="61c1c-172">**Warning**  For security reasons, it is important to note that **JetOpenFile** does not verify that the requested file path is associated with the set of files that should be backed up for the instance.</span></span> <span data-ttu-id="61c1c-173">Como resultado, es posible usar esta función para tener acceso a cualquier archivo que pueda abrir el contexto de seguridad actual del subproceso.</span><span class="sxs-lookup"><span data-stu-id="61c1c-173">As a result, it is possible to use this function to access any file that can be opened by the current security context of the thread.</span></span> <span data-ttu-id="61c1c-174">Es imperativo que la aplicación restrinja las rutas de acceso que se pasan a esta función a un conjunto conocido de rutas de acceso de archivos correctas o a la revelación del ataque de información.</span><span class="sxs-lookup"><span data-stu-id="61c1c-174">It is imperative that the application restrict the paths passed to this function to a known set of good file paths or a disclosure of information attack could be made possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="61c1c-175">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61c1c-175">Remarks</span></span>

<span data-ttu-id="61c1c-176">Es necesario que los búferes de salida de identificador y tamaño de archivo estén presentes.</span><span class="sxs-lookup"><span data-stu-id="61c1c-176">The handle and file size output buffers are required to be present.</span></span> <span data-ttu-id="61c1c-177">Si no están presentes, el motor se bloqueará porque no se validan los parámetros del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="61c1c-177">If they are not present then the engine will crash because the output buffer parameters are not validated.</span></span>

<span data-ttu-id="61c1c-178">En este momento, solo se puede abrir un archivo para copia de seguridad al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="61c1c-178">At this time, only one file can be open for backup at any one time.</span></span>

<span data-ttu-id="61c1c-179">**JetOpenFile** no valida el privilegio de copia de seguridad antes de abrir el archivo solicitado.</span><span class="sxs-lookup"><span data-stu-id="61c1c-179">**JetOpenFile** does not assert the backup privilege prior to opening the requested file.</span></span>

<span data-ttu-id="61c1c-180">Es posible que el tamaño del archivo que se va a leer tal como lo indique esta función no coincida con el tamaño del archivo en el disco.</span><span class="sxs-lookup"><span data-stu-id="61c1c-180">The size of the file to be read as reported by this function may not match the size of the file on disk.</span></span> <span data-ttu-id="61c1c-181">En Windows XP y versiones posteriores, se puede anexar información adicional a un archivo de base de datos utilizado por el motor de base de datos durante una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="61c1c-181">On Windows XP and later releases, extra information may be appended to a database file which is used by the database engine during a restore operation.</span></span> <span data-ttu-id="61c1c-182">Como tal, la aplicación solo debe confiar en el tamaño de archivo devuelto por **JetOpenFile** o en el número real de bytes de datos devueltos por [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="61c1c-182">As such, the application should only rely on the file size returned by **JetOpenFile** or on the actual number of bytes of data returned by [JetReadFile](./jetreadfile-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="61c1c-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61c1c-183">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-184"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="61c1c-184"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="61c1c-185">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="61c1c-185">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-186"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="61c1c-186"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="61c1c-187">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="61c1c-187">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-188"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="61c1c-188"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="61c1c-189">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="61c1c-189">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-190"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="61c1c-190"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="61c1c-191">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="61c1c-191">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61c1c-192"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="61c1c-192"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="61c1c-193">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="61c1c-193">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61c1c-194"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="61c1c-194"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="61c1c-195">Se implementa como <strong>JetOpenFileW</strong> (Unicode) y <strong>JetOpenFileA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="61c1c-195">Implemented as <strong>JetOpenFileW</strong> (Unicode) and <strong>JetOpenFileA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="61c1c-196">Consulte también</span><span class="sxs-lookup"><span data-stu-id="61c1c-196">See Also</span></span>

[<span data-ttu-id="61c1c-197">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="61c1c-197">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="61c1c-198">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="61c1c-198">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="61c1c-199">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="61c1c-199">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="61c1c-200">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="61c1c-200">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="61c1c-201">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="61c1c-201">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="61c1c-202">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="61c1c-202">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="61c1c-203">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="61c1c-203">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="61c1c-204">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="61c1c-204">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="61c1c-205">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="61c1c-205">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="61c1c-206">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="61c1c-206">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="61c1c-207">JetStopService</span><span class="sxs-lookup"><span data-stu-id="61c1c-207">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="61c1c-208">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="61c1c-208">JetTruncateLog</span></span>](./jettruncatelog-function.md)
