---
description: 'Más información acerca de: JetGetLogInfo (función)'
title: JetGetLogInfo función)
TOCTitle: JetGetLogInfo Function
ms:assetid: a9d14830-d731-4d47-bdc2-c0660a08678e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294055(v=EXCHG.10)
ms:contentKeyID: 32765665
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoA
- JetGetLogInfoW
- JetGetLogInfo
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c96827be0ac62502e7545a9acb1fe157f3b28fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816339"
---
# <a name="jetgetloginfo-function"></a><span data-ttu-id="fb30d-103">JetGetLogInfo función)</span><span class="sxs-lookup"><span data-stu-id="fb30d-103">JetGetLogInfo Function</span></span>


<span data-ttu-id="fb30d-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fb30d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfo-function"></a><span data-ttu-id="fb30d-105">JetGetLogInfo función)</span><span class="sxs-lookup"><span data-stu-id="fb30d-105">JetGetLogInfo Function</span></span>

<span data-ttu-id="fb30d-106">La función **JetGetLogInfo** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar en una instancia los nombres de los archivos de revisión de la base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fb30d-106">The **JetGetLogInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="fb30d-107">Estos archivos se pueden abrir posteriormente mediante [JetOpenFile](./jetopenfile-function.md) y leer con [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="fb30d-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="fb30d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb30d-108">Parameters</span></span>

<span data-ttu-id="fb30d-109">*szz*</span><span class="sxs-lookup"><span data-stu-id="fb30d-109">*szz*</span></span>

<span data-ttu-id="fb30d-110">Búfer de salida que recibirá la lista de cadenas terminadas en null que describen el conjunto de archivos de revisión de la base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fb30d-110">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="fb30d-111">La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="fb30d-111">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="fb30d-112">Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="fb30d-112">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="fb30d-113">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="fb30d-113">*cbMax*</span></span>

<span data-ttu-id="fb30d-114">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="fb30d-114">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="fb30d-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="fb30d-115">*pcbActual*</span></span>

<span data-ttu-id="fb30d-116">Recibe la cantidad real de datos de cadena recibidos en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="fb30d-116">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="fb30d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb30d-117">Return Value</span></span>

<span data-ttu-id="fb30d-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="fb30d-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="fb30d-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fb30d-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb30d-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fb30d-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="fb30d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb30d-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="fb30d-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="fb30d-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="fb30d-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb30d-124">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="fb30d-124">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="fb30d-125">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="fb30d-125">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="fb30d-126">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fb30d-126">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-127">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="fb30d-127">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="fb30d-128">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="fb30d-128">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb30d-129">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="fb30d-129">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="fb30d-130">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="fb30d-130">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="fb30d-131">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fb30d-131">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-132">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="fb30d-132">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="fb30d-133">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fb30d-133">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="fb30d-134"><strong>JetGetLogInfo</strong> devolverá este error si hay identificadores de archivo pendientes creados con <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para la instancia.</span><span class="sxs-lookup"><span data-stu-id="fb30d-134"><strong>JetGetLogInfo</strong> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb30d-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="fb30d-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="fb30d-136">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="fb30d-136">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="fb30d-137">Esto puede ocurrir para <strong>JetGetLogInfo</strong> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="fb30d-137">This can happen for <strong>JetGetLogInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-138">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="fb30d-138">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="fb30d-139">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="fb30d-139">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb30d-140">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="fb30d-140">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="fb30d-141">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="fb30d-141">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-142">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="fb30d-142">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="fb30d-143">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="fb30d-143">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb30d-144">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="fb30d-144">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="fb30d-145">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="fb30d-145">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-146">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="fb30d-146">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="fb30d-147">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="fb30d-147">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fb30d-148">Si se ejecuta correctamente, la información solicitada en el conjunto de archivos de revisión de la base de datos y en los archivos de registro de transacciones que debe formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida cuando se proporcionen.</span><span class="sxs-lookup"><span data-stu-id="fb30d-148">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="fb30d-149">El equipo de estado de copia de seguridad se verá avanzado de modo que ya no se permita la copia de seguridad de los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="fb30d-149">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="fb30d-150">Solo se permite abrir archivos de revisión de base de datos y archivos de registro de transacciones para la copia de seguridad más allá de este punto.</span><span class="sxs-lookup"><span data-stu-id="fb30d-150">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="fb30d-151">En caso de error, el estado de los búferes de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="fb30d-151">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="fb30d-152">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="fb30d-152">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="fb30d-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb30d-153">Remarks</span></span>

<span data-ttu-id="fb30d-154">Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="fb30d-154">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="fb30d-155">La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y utilizar esa información para determinar si la lista se truncó.</span><span class="sxs-lookup"><span data-stu-id="fb30d-155">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="fb30d-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb30d-156">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-157"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="fb30d-157"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fb30d-158">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fb30d-158">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb30d-159"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="fb30d-159"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fb30d-160">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fb30d-160">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-161"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="fb30d-161"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fb30d-162">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="fb30d-162">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb30d-163"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="fb30d-163"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="fb30d-164">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="fb30d-164">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb30d-165"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="fb30d-165"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="fb30d-166">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="fb30d-166">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb30d-167"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fb30d-167"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fb30d-168">Se implementa como <strong>JetGetLogInfoW</strong> (Unicode) y <strong>JetGetLogInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fb30d-168">Implemented as <strong>JetGetLogInfoW</strong> (Unicode) and <strong>JetGetLogInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="fb30d-169">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fb30d-169">See Also</span></span>

[<span data-ttu-id="fb30d-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fb30d-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fb30d-171">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="fb30d-171">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="fb30d-172">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="fb30d-172">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="fb30d-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="fb30d-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="fb30d-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="fb30d-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="fb30d-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="fb30d-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="fb30d-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="fb30d-176">JetStopBackup</span></span>](./jetstopbackup-function.md)
