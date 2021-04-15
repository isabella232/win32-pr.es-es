---
description: 'Más información acerca de: JetGetAttachInfo (función)'
title: Función JetGetAttachInfo
TOCTitle: JetGetAttachInfo Function
ms:assetid: 6b1392f3-f40a-4eb0-aea8-1508b23ed649
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269286(v=EXCHG.10)
ms:contentKeyID: 32765578
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfo
- JetGetAttachInfoA
- JetGetAttachInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa1e51931c11e0fce0b18c0c102c4d54c0b47976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649201"
---
# <a name="jetgetattachinfo-function"></a><span data-ttu-id="969c3-103">Función JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="969c3-103">JetGetAttachInfo Function</span></span>


<span data-ttu-id="969c3-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="969c3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfo-function"></a><span data-ttu-id="969c3-105">Función JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="969c3-105">JetGetAttachInfo Function</span></span>

<span data-ttu-id="969c3-106">La función **JetGetAttachInfo** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para consultar los nombres de los archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="969c3-106">The **JetGetAttachInfo** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="969c3-107">Solo se tendrán en cuenta las bases de datos adjuntas actualmente a la instancia mediante [JetAttachDatabase](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="969c3-107">Only databases currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="969c3-108">Estos archivos se pueden abrir posteriormente mediante [JetOpenFile](./jetopenfile-function.md) y leer con [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="969c3-108">These files may subsequently be opened using [JetOpenFile](./jetopenfile-function.md) and read using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfo(
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="969c3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="969c3-109">Parameters</span></span>

<span data-ttu-id="969c3-110">*szz*</span><span class="sxs-lookup"><span data-stu-id="969c3-110">*szz*</span></span>

<span data-ttu-id="969c3-111">Búfer de salida que recibe la lista de cadenas terminadas en null que describen el conjunto de archivos de base de datos que debe formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="969c3-111">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="969c3-112">La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="969c3-112">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="969c3-113">Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="969c3-113">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="969c3-114">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="969c3-114">*cbMax*</span></span>

<span data-ttu-id="969c3-115">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="969c3-115">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="969c3-116">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="969c3-116">*pcbActual*</span></span>

<span data-ttu-id="969c3-117">Puntero al búfer de salida que recibió la cantidad real de datos de cadena.</span><span class="sxs-lookup"><span data-stu-id="969c3-117">Pointer to the output buffer that received the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="969c3-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="969c3-118">Return Value</span></span>

<span data-ttu-id="969c3-119">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="969c3-119">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="969c3-120">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="969c3-120">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="969c3-121">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="969c3-121">Return code</span></span></p></th>
<th><p><span data-ttu-id="969c3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="969c3-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="969c3-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="969c3-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="969c3-124">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="969c3-124">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="969c3-125">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="969c3-125">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="969c3-126">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="969c3-126">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="969c3-127">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="969c3-127">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="969c3-128">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="969c3-128">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="969c3-129">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="969c3-129">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="969c3-130">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="969c3-130">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="969c3-131">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="969c3-131">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="969c3-132">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="969c3-132">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="969c3-133">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="969c3-133">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="969c3-134">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="969c3-134">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="969c3-135"><strong>JetGetAttachInfo</strong> devolverá este error si la copia de seguridad actual no es una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="969c3-135"><strong>JetGetAttachInfo</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="969c3-136">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="969c3-136">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="969c3-137">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="969c3-137">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="969c3-138">Esto puede ocurrir para <strong>JetGetAttachInfo</strong> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="969c3-138">This can happen for <strong>JetGetAttachInfo</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="969c3-139">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="969c3-139">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="969c3-140">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="969c3-140">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="969c3-141">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="969c3-141">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="969c3-142">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="969c3-142">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="969c3-143">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="969c3-143">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="969c3-144">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="969c3-144">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="969c3-145">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="969c3-145">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="969c3-146">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="969c3-146">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="969c3-147">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="969c3-147">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="969c3-148">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="969c3-148">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="969c3-149">Si se ejecuta correctamente, la información solicitada en el conjunto de archivos de base de datos que debe formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida, siempre que se proporcionen.</span><span class="sxs-lookup"><span data-stu-id="969c3-149">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="969c3-150">En caso de error, el estado de los búferes de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="969c3-150">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="969c3-151">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="969c3-151">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="969c3-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="969c3-152">Remarks</span></span>

<span data-ttu-id="969c3-153">Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="969c3-153">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="969c3-154">La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y utilizar esa información para determinar si la lista se truncó.</span><span class="sxs-lookup"><span data-stu-id="969c3-154">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="969c3-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="969c3-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="969c3-156"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="969c3-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="969c3-157">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="969c3-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="969c3-158"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="969c3-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="969c3-159">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="969c3-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="969c3-160"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="969c3-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="969c3-161">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="969c3-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="969c3-162"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="969c3-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="969c3-163">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="969c3-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="969c3-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="969c3-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="969c3-165">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="969c3-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="969c3-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="969c3-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="969c3-167">Se implementa como <strong>JetGetAttachInfoW</strong> (Unicode) y <strong>JetGetAttachInfoA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="969c3-167">Implemented as <strong>JetGetAttachInfoW</strong> (Unicode) and <strong>JetGetAttachInfoA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="969c3-168">Consulte también</span><span class="sxs-lookup"><span data-stu-id="969c3-168">See Also</span></span>

[<span data-ttu-id="969c3-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="969c3-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="969c3-170">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="969c3-170">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="969c3-171">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="969c3-171">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="969c3-172">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="969c3-172">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="969c3-173">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="969c3-173">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="969c3-174">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="969c3-174">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="969c3-175">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="969c3-175">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="969c3-176">JetStopService</span><span class="sxs-lookup"><span data-stu-id="969c3-176">JetStopService</span></span>](./jetstopservice-function.md)
