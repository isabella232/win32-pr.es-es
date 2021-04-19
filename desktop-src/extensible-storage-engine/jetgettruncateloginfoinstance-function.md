---
description: 'Más información acerca de: JetGetTruncateLogInfoInstance (función)'
title: JetGetTruncateLogInfoInstance función)
TOCTitle: JetGetTruncateLogInfoInstance Function
ms:assetid: 1ecb2f2f-2cad-4c55-9296-5e5893b57695
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269199(v=EXCHG.10)
ms:contentKeyID: 32765502
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetTruncateLogInfoInstanceA
- JetGetTruncateLogInfoInstanceW
- JetGetTruncateLogInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d51243ff6ca4b2bbaec77233bbe00437f55e0f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707186"
---
# <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="bb38c-103">JetGetTruncateLogInfoInstance función)</span><span class="sxs-lookup"><span data-stu-id="bb38c-103">JetGetTruncateLogInfoInstance Function</span></span>


<span data-ttu-id="bb38c-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bb38c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgettruncateloginfoinstance-function"></a><span data-ttu-id="bb38c-105">JetGetTruncateLogInfoInstance función)</span><span class="sxs-lookup"><span data-stu-id="bb38c-105">JetGetTruncateLogInfoInstance Function</span></span>

<span data-ttu-id="bb38c-106">La función **JetGetTruncateLogInfoInstance** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar a una instancia los nombres de los archivos de registro de transacciones que se pueden eliminar de forma segura después de que la copia de seguridad se haya completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb38c-106">The **JetGetTruncateLogInfoInstance** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="bb38c-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb38c-107">**Windows XP:**  **JetGetTruncateLogInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetTruncateLogInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="bb38c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb38c-108">Parameters</span></span>

<span data-ttu-id="bb38c-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="bb38c-109">*instance*</span></span>

<span data-ttu-id="bb38c-110">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="bb38c-110">The instance to use for this call.</span></span>

<span data-ttu-id="bb38c-111">*szz*</span><span class="sxs-lookup"><span data-stu-id="bb38c-111">*szz*</span></span>

<span data-ttu-id="bb38c-112">Búfer de salida que recibe la lista de cadenas terminadas en null que describen el conjunto de archivos de registro de transacciones que se pueden eliminar de forma segura después de que la copia de seguridad se haya completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb38c-112">The output buffer that receives the list of null-terminated strings describing the set of transaction log files that can be safely deleted after the backup has been completed successfully.</span></span>

<span data-ttu-id="bb38c-113">La lista de cadenas que se devuelven en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="bb38c-113">The list of strings that are returned in this buffer is in the same format as a multi-string that is used by the registry.</span></span> <span data-ttu-id="bb38c-114">Cada cadena terminada en NULL se devuelve en secuencia y seguido de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="bb38c-114">Each null-terminated string is returned in sequence and followed by a final null terminator.</span></span>

<span data-ttu-id="bb38c-115">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="bb38c-115">*cbMax*</span></span>

<span data-ttu-id="bb38c-116">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="bb38c-116">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="bb38c-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="bb38c-117">*pcbActual*</span></span>

<span data-ttu-id="bb38c-118">Puntero al búfer de salida que recibe la cantidad real de datos de cadena.</span><span class="sxs-lookup"><span data-stu-id="bb38c-118">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="bb38c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb38c-119">Return Value</span></span>

<span data-ttu-id="bb38c-120">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="bb38c-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="bb38c-121">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bb38c-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb38c-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bb38c-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="bb38c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb38c-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="bb38c-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="bb38c-125">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="bb38c-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb38c-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="bb38c-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="bb38c-127">Uno de los parámetros proporcionados contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="bb38c-127">One of the provided parameters contained an unexpected value or the combination of several parameter values resulted in an unexpected result.</span></span></p>
<p><span data-ttu-id="bb38c-128"><strong>Windows XP y versiones posteriores:</strong>  Esto puede ocurrir para <strong>JetGetTruncateLogInfoInstance</strong> cuando el identificador de instancia especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="bb38c-128"><strong>Windows XP and later:</strong>  This can happen for <strong>JetGetTruncateLogInfoInstance</strong> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="bb38c-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="bb38c-130">No se puede completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="bb38c-130">The operation cannot complete because the instance that is associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb38c-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="bb38c-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="bb38c-132">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="bb38c-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="bb38c-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="bb38c-134">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="bb38c-134">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="bb38c-135"><strong>Windows XP:</strong>  Este valor devuelto se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb38c-135"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb38c-136">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="bb38c-136">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="bb38c-137">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="bb38c-137">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="bb38c-138"><strong>Windows XP:</strong>  Este valor devuelto se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb38c-138"><strong>Windows XP:</strong>  This return value was introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-139">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="bb38c-139">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="bb38c-140">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="bb38c-140">The backup operation failed because it was called out of sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb38c-141">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="bb38c-141">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="bb38c-142">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="bb38c-142">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="bb38c-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="bb38c-144">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="bb38c-144">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb38c-145">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="bb38c-145">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="bb38c-146">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="bb38c-146">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-147"><strong>JetGetTruncateLogInfoInstance</strong></span><span class="sxs-lookup"><span data-stu-id="bb38c-147"><strong>JetGetTruncateLogInfoInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="bb38c-148">Hay identificadores de archivo pendientes que se crearon con <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para la instancia.</span><span class="sxs-lookup"><span data-stu-id="bb38c-148">There are outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bb38c-149">Si esta función se ejecuta correctamente, la información solicitada sobre el conjunto de archivos de registro de transacciones que se puede eliminar de forma segura después de que la copia de seguridad se haya completado correctamente se colocará en los búferes de salida en los que se proporcionan.</span><span class="sxs-lookup"><span data-stu-id="bb38c-149">If this function succeeds, the requested information about the set of transaction log files that can be safely deleted after the backup has been completed successfully will be placed in the output buffers where they are provided.</span></span> <span data-ttu-id="bb38c-150">El equipo de estado de copia de seguridad se verá avanzado de modo que ya no se permita la copia de seguridad de los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb38c-150">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="bb38c-151">Solo se pueden abrir archivos de revisión de base de datos y archivos de registro de transacciones para la copia de seguridad más allá de este punto.</span><span class="sxs-lookup"><span data-stu-id="bb38c-151">Only database patch files and transaction log files can be opened for backup beyond this point.</span></span>

<span data-ttu-id="bb38c-152">Si se produce un error en esta función, el estado de los búferes de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="bb38c-152">If this function fails, the state of the output buffers is undefined.</span></span> <span data-ttu-id="bb38c-153">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="bb38c-153">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="bb38c-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb38c-154">Remarks</span></span>

<span data-ttu-id="bb38c-155">Esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bb38c-155">This API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="bb38c-156">La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y utilizar esa información para determinar si la lista se truncó.</span><span class="sxs-lookup"><span data-stu-id="bb38c-156">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="bb38c-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb38c-157">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-158"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bb38c-158"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bb38c-159">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bb38c-159">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb38c-160"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bb38c-160"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bb38c-161">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bb38c-161">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-162"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bb38c-162"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bb38c-163">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="bb38c-163">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb38c-164"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="bb38c-164"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="bb38c-165">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="bb38c-165">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb38c-166"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="bb38c-166"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="bb38c-167">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="bb38c-167">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb38c-168"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bb38c-168"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bb38c-169">Se implementa como <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) y <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bb38c-169">Implemented as <strong>JetGetTruncateLogInfoInstanceW</strong> (Unicode) and <strong>JetGetTruncateLogInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="bb38c-170">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bb38c-170">See Also</span></span>

[<span data-ttu-id="bb38c-171">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="bb38c-171">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="bb38c-172">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bb38c-172">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="bb38c-173">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="bb38c-173">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="bb38c-174">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="bb38c-174">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="bb38c-175">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="bb38c-175">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="bb38c-176">JetEndSession</span><span class="sxs-lookup"><span data-stu-id="bb38c-176">JetEndSession</span></span>](./jetendsession-function.md)  
[<span data-ttu-id="bb38c-177">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="bb38c-177">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="bb38c-178">JetResetSessionContext</span><span class="sxs-lookup"><span data-stu-id="bb38c-178">JetResetSessionContext</span></span>](./jetresetsessioncontext-function.md)  
[<span data-ttu-id="bb38c-179">JetRollback</span><span class="sxs-lookup"><span data-stu-id="bb38c-179">JetRollback</span></span>](./jetrollback-function.md)  
[<span data-ttu-id="bb38c-180">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="bb38c-180">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="bb38c-181">JetStopService</span><span class="sxs-lookup"><span data-stu-id="bb38c-181">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="bb38c-182">JetTerm</span><span class="sxs-lookup"><span data-stu-id="bb38c-182">JetTerm</span></span>](./jetterm-function.md)  
[<span data-ttu-id="bb38c-183">JetTerm2</span><span class="sxs-lookup"><span data-stu-id="bb38c-183">JetTerm2</span></span>](./jetterm2-function.md)
