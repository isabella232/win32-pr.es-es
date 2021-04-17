---
description: 'Más información acerca de: JetGetLogInfoInstance2 (función)'
title: JetGetLogInfoInstance2 función)
TOCTitle: JetGetLogInfoInstance2 Function
ms:assetid: 50fdae92-611c-4dbf-846e-86cc836a23db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269247(v=EXCHG.10)
ms:contentKeyID: 32765549
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLogInfoInstance2W
- JetGetLogInfoInstance2
- JetGetLogInfoInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f58a04c49a82604fb5ded09b6328e9e03df7963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697242"
---
# <a name="jetgetloginfoinstance2-function"></a><span data-ttu-id="8a2aa-103">JetGetLogInfoInstance2 función)</span><span class="sxs-lookup"><span data-stu-id="8a2aa-103">JetGetLogInfoInstance2 Function</span></span>


<span data-ttu-id="8a2aa-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8a2aa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetloginfoinstance2-function"></a><span data-ttu-id="8a2aa-105">JetGetLogInfoInstance2 función)</span><span class="sxs-lookup"><span data-stu-id="8a2aa-105">JetGetLogInfoInstance2 Function</span></span>

<span data-ttu-id="8a2aa-106">La función **JetGetLogInfoInstance2** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar en una instancia los nombres de los archivos de revisión de la base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-106">The **JetGetLogInfoInstance2** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database patch files and transaction log files that should become part of the backup file set.</span></span> <span data-ttu-id="8a2aa-107">Estos archivos se pueden abrir posteriormente mediante [JetOpenFile](./jetopenfile-function.md) y leer con [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="8a2aa-107">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

<span data-ttu-id="8a2aa-108">**Windows XP: JetGetLogInfoInstance2** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-108">**Windows XP:  JetGetLogInfoInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetLogInfoInstance2(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in_out_opt  JET_LOGINFO* pLogInfo
    );
```

### <a name="parameters"></a><span data-ttu-id="8a2aa-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a2aa-109">Parameters</span></span>

<span data-ttu-id="8a2aa-110">*repetición*</span><span class="sxs-lookup"><span data-stu-id="8a2aa-110">*instance*</span></span>

<span data-ttu-id="8a2aa-111">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-111">The instance to use for this call.</span></span>

<span data-ttu-id="8a2aa-112">En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-112">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="8a2aa-113">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="8a2aa-114">En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-114">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="8a2aa-115">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="8a2aa-116">*szz*</span><span class="sxs-lookup"><span data-stu-id="8a2aa-116">*szz*</span></span>

<span data-ttu-id="8a2aa-117">Búfer de salida que recibirá la lista de cadenas terminadas en null que describen el conjunto de archivos de revisión de la base de datos y los archivos de registro de transacciones que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-117">The output buffer that will receive the list of null terminated strings describing the set of database patch files and transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="8a2aa-118">La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-118">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="8a2aa-119">Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-119">Each null terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="8a2aa-120">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="8a2aa-120">*cbMax*</span></span>

<span data-ttu-id="8a2aa-121">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-121">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="8a2aa-122">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="8a2aa-122">*pcbActual*</span></span>

<span data-ttu-id="8a2aa-123">Recibe la cantidad real de datos de cadena recibidos en el búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-123">Receives the actual amount of string data received in the output buffer.</span></span>

<span data-ttu-id="8a2aa-124">*pLogInfo*</span><span class="sxs-lookup"><span data-stu-id="8a2aa-124">*pLogInfo*</span></span>

<span data-ttu-id="8a2aa-125">Recibe información estructurada sobre los archivos de registro de transacciones que debe formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-125">Receives structured information on the transaction log files that should be a part of the backup file set.</span></span>

<span data-ttu-id="8a2aa-126">Cuando este parámetro no está presente, se supone que su valor es NULL.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-126">When this parameter is not present, its value is presumed to be NULL.</span></span>

### <a name="return-value"></a><span data-ttu-id="8a2aa-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a2aa-127">Return Value</span></span>

<span data-ttu-id="8a2aa-128">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-128">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8a2aa-129">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8a2aa-129">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8a2aa-130">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8a2aa-130">Return code</span></span></p></th>
<th><p><span data-ttu-id="8a2aa-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a2aa-131">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-132">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8a2aa-132">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-133">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-133">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2aa-134">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="8a2aa-134">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-135">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-135">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="8a2aa-136">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-136">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-137">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="8a2aa-137">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-138">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-138">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2aa-139">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="8a2aa-139">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-140">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-140">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="8a2aa-141">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-141">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-142">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="8a2aa-142">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-143">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-143">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="8a2aa-144"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> devolverá este error si hay identificadores de archivo pendientes creados con <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para la instancia.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-144"><a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> will return this error if there are any outstanding file handles created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2aa-145">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="8a2aa-145">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-146">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-146">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="8a2aa-147">Esto puede ocurrir para <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="8a2aa-147">This can happen for <a href="gg294055(v=exchg.10).md">JetGetLogInfo</a> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-148">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="8a2aa-148">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-149">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-149">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2aa-150">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="8a2aa-150">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-151">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-151">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-152">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="8a2aa-152">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-153">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-153">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2aa-154">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="8a2aa-154">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-155">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-155">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-156">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="8a2aa-156">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="8a2aa-157">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-157">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8a2aa-158">Si se ejecuta correctamente, la información solicitada en el conjunto de archivos de revisión de la base de datos y en los archivos de registro de transacciones que debe formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida cuando se proporcionen.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-158">On success, the requested information on the set of database patch files and transaction log files that should be part of the backup file set will be placed in the output buffers where provided.</span></span> <span data-ttu-id="8a2aa-159">El equipo de estado de copia de seguridad se verá avanzado de modo que ya no se permita la copia de seguridad de los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-159">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="8a2aa-160">Solo se permite abrir archivos de revisión de base de datos y archivos de registro de transacciones para la copia de seguridad más allá de este punto.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-160">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="8a2aa-161">En caso de error, el estado de los búferes de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-161">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="8a2aa-162">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-162">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="8a2aa-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a2aa-163">Remarks</span></span>

<span data-ttu-id="8a2aa-164">Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-164">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="8a2aa-165">La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y utilizar esa información para determinar si la lista se truncó.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-165">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="8a2aa-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a2aa-166">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-167"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8a2aa-167"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2aa-168">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-168">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2aa-169"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8a2aa-169"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2aa-170">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-170">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-171"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8a2aa-171"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2aa-172">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-172">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2aa-173"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="8a2aa-173"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2aa-174">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-174">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8a2aa-175"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8a2aa-175"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2aa-176">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8a2aa-176">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8a2aa-177"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8a2aa-177"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8a2aa-178">Se implementa como <strong>JetGetLogInfoInstance2W</strong> (Unicode) y <strong>JetGetLogInfoInstance2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8a2aa-178">Implemented as <strong>JetGetLogInfoInstance2W</strong> (Unicode) and <strong>JetGetLogInfoInstance2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8a2aa-179">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a2aa-179">See Also</span></span>

[<span data-ttu-id="8a2aa-180">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8a2aa-180">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8a2aa-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="8a2aa-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="8a2aa-182">JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="8a2aa-182">JET_LOGINFO</span></span>](./jet-loginfo-structure.md)  
[<span data-ttu-id="8a2aa-183">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="8a2aa-183">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="8a2aa-184">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="8a2aa-184">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="8a2aa-185">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="8a2aa-185">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="8a2aa-186">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="8a2aa-186">JetStopBackup</span></span>](./jetstopbackup-function.md)
