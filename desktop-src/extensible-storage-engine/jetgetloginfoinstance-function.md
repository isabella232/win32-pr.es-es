---
description: 'Más información acerca de: JetGetLogInfoInstance (función)'
title: JetGetLogInfoInstance función)
TOCTitle: JetGetLogInfoInstance Function
ms:assetid: 505500b1-2827-43f1-a0fe-5e84e00b0260
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269246(v=EXCHG.10)
ms:contentKeyID: 32765548
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance
- JetGetLogInfoInstanceW
- JetGetLogInfoInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2056859bdce13dfdc28d4cbbf8716925d5bc1cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707187"
---
# <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="c2f10-103">JetGetLogInfoInstance función)</span><span class="sxs-lookup"><span data-stu-id="c2f10-103">JetGetLogInfoInstance Function</span></span>


<span data-ttu-id="c2f10-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c2f10-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance-function"></a><span data-ttu-id="c2f10-105">JetGetLogInfoInstance función)</span><span class="sxs-lookup"><span data-stu-id="c2f10-105">JetGetLogInfoInstance Function</span></span>

<span data-ttu-id="c2f10-106">La función **JetGetLogInfoInstance** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar en una instancia los nombres de los archivos de revisión de la base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c2f10-106">The **JetGetLogInfoInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="c2f10-107">Estos archivos se pueden abrir posteriormente mediante [JetOpenFile](./jetopenfile-function.md) y leer con [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="c2f10-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="c2f10-108">**Windows XP: JetGetLogInfoInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c2f10-108">**Windows XP:  JetGetLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="c2f10-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2f10-109">Parameters</span></span>

<span data-ttu-id="c2f10-110">*repetición*</span><span class="sxs-lookup"><span data-stu-id="c2f10-110">*instance*</span></span>

<span data-ttu-id="c2f10-111">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c2f10-111">The instance to use for this call.</span></span>

<span data-ttu-id="c2f10-112">En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="c2f10-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="c2f10-113">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="c2f10-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="c2f10-114">En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="c2f10-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="c2f10-115">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="c2f10-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="c2f10-116">*szz*</span><span class="sxs-lookup"><span data-stu-id="c2f10-116">*szz*</span></span>

<span data-ttu-id="c2f10-117">Búfer de salida que recibirá la lista de cadenas terminadas en null que describen el conjunto de archivos de revisión de la base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c2f10-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="c2f10-118">La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="c2f10-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="c2f10-119">Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="c2f10-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="c2f10-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="c2f10-120">*cbMax*</span></span>

<span data-ttu-id="c2f10-121">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="c2f10-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="c2f10-122">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="c2f10-122">*pcbActual*</span></span>

<span data-ttu-id="c2f10-123">Recibe la cantidad real de datos de cadena recibidos en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="c2f10-123">Receives the actual amount of string data received in the output buffer.</span></span>

### <a name="return-value"></a><span data-ttu-id="c2f10-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2f10-124">Return Value</span></span>

<span data-ttu-id="c2f10-125">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="c2f10-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c2f10-126">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c2f10-126">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2f10-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c2f10-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="c2f10-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2f10-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c2f10-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c2f10-130">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c2f10-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f10-131">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="c2f10-131">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="c2f10-132">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="c2f10-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="c2f10-133">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c2f10-133">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-134">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="c2f10-134">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="c2f10-135">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="c2f10-135">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f10-136">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="c2f10-136">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="c2f10-137">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="c2f10-137">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="c2f10-138">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="c2f10-138">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="c2f10-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="c2f10-140">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c2f10-140">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="c2f10-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> devolverá este error si hay identificadores de archivo pendientes creados con <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para la instancia.</span><span class="sxs-lookup"><span data-stu-id="c2f10-141"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f10-142">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c2f10-142">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c2f10-143">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="c2f10-143">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="c2f10-144">Esto puede ocurrir para <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="c2f10-144">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-145">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="c2f10-145">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="c2f10-146">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="c2f10-146">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f10-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="c2f10-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="c2f10-148">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c2f10-148">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-149">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="c2f10-149">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="c2f10-150">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c2f10-150">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f10-151">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="c2f10-151">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="c2f10-152">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="c2f10-152">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-153">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="c2f10-153">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="c2f10-154">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="c2f10-154">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c2f10-155">Si se ejecuta correctamente, la información solicitada en el conjunto de archivos de revisión de la base de datos y en los archivos de registro de transacciones que debe formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida cuando se proporcionen.</span><span class="sxs-lookup"><span data-stu-id="c2f10-155">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="c2f10-156">El equipo de estado de copia de seguridad se verá avanzado de modo que ya no se permita la copia de seguridad de los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="c2f10-156">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="c2f10-157">Solo se permite abrir archivos de revisión de base de datos y archivos de registro de transacciones para la copia de seguridad más allá de este punto.</span><span class="sxs-lookup"><span data-stu-id="c2f10-157">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="c2f10-158">En caso de error, el estado de los búferes de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="c2f10-158">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="c2f10-159">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="c2f10-159">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c2f10-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2f10-160">Remarks</span></span>

<span data-ttu-id="c2f10-161">Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c2f10-161">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="c2f10-162">La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y utilizar esa información para determinar si la lista se truncó.</span><span class="sxs-lookup"><span data-stu-id="c2f10-162">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c2f10-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2f10-163">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-164"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c2f10-164"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f10-165">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c2f10-165">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f10-166"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c2f10-166"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f10-167">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c2f10-167">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-168"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c2f10-168"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f10-169">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c2f10-169">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f10-170"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="c2f10-170"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f10-171">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c2f10-171">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2f10-172"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c2f10-172"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f10-173">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c2f10-173">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2f10-174"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c2f10-174"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c2f10-175">Se implementa como <strong>JetGetLogInfoInstanceW</strong> (Unicode) y <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c2f10-175">Implemented as <strong>JetGetLogInfoInstanceW</strong> (Unicode) and <strong>JetGetLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c2f10-176">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c2f10-176">See Also</span></span>

[<span data-ttu-id="c2f10-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c2f10-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c2f10-178">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="c2f10-178">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="c2f10-179">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="c2f10-179">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="c2f10-180">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="c2f10-180">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="c2f10-181">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="c2f10-181">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="c2f10-182">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="c2f10-182">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="c2f10-183">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="c2f10-183">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="c2f10-184">JetStopService</span><span class="sxs-lookup"><span data-stu-id="c2f10-184">JetStopService</span></span>](./jetstopservice-function.md)
