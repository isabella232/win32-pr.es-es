---
description: 'Más información acerca de: JetGetAttachInfoInstance (función)'
title: JetGetAttachInfoInstance función)
TOCTitle: JetGetAttachInfoInstance Function
ms:assetid: 978e7817-0720-42fc-a5c1-46e4d44239f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269350(v=EXCHG.10)
ms:contentKeyID: 32765637
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetAttachInfoInstanceW
- JetGetAttachInfoInstanceA
- JetGetAttachInfoInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28abf76632f147b6e909c1b8fb036062d5d3af74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910245"
---
# <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="4a0b0-103">JetGetAttachInfoInstance función)</span><span class="sxs-lookup"><span data-stu-id="4a0b0-103">JetGetAttachInfoInstance Function</span></span>


<span data-ttu-id="4a0b0-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4a0b0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetattachinfoinstance-function"></a><span data-ttu-id="4a0b0-105">JetGetAttachInfoInstance función)</span><span class="sxs-lookup"><span data-stu-id="4a0b0-105">JetGetAttachInfoInstance Function</span></span>

<span data-ttu-id="4a0b0-106">La función **JetGetAttachInfoInstance** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) para consultar los nombres de los archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-106">The **JetGetAttachInfoInstance** function is used during a backup initiated by [JetBeginExternalBackupInstance](./jetbeginexternalbackupinstance-function.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="4a0b0-107">Solo se tendrán en cuenta las bases de datos que estén adjuntas actualmente a la instancia mediante [JetAttachDatabase](./jetattachdatabase-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4a0b0-107">Only databases that are currently attached to the instance using [JetAttachDatabase](./jetattachdatabase-function.md) will be considered.</span></span> <span data-ttu-id="4a0b0-108">Estos archivos se pueden abrir posteriormente mediante [JetOpenFileInstance](./jetopenfileinstance-function.md) y leer con [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="4a0b0-108">These files may subsequently be opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) and read using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="4a0b0-109">**Windows XP: JetGetAttachInfoInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-109">**Windows XP:  JetGetAttachInfoInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetGetAttachInfoInstance(
      __in          JET_INSTANCE instance,
      __out_opt     tchar* szz,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a><span data-ttu-id="4a0b0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a0b0-110">Parameters</span></span>

<span data-ttu-id="4a0b0-111">*repetición*</span><span class="sxs-lookup"><span data-stu-id="4a0b0-111">*instance*</span></span>

<span data-ttu-id="4a0b0-112">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-112">The instance to use for this call.</span></span>

<span data-ttu-id="4a0b0-113">En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-113">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="4a0b0-114">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-114">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="4a0b0-115">En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-115">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="4a0b0-116">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-116">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="4a0b0-117">*szz*</span><span class="sxs-lookup"><span data-stu-id="4a0b0-117">*szz*</span></span>

<span data-ttu-id="4a0b0-118">Búfer de salida que recibe la lista de cadenas terminadas en null que describen el conjunto de archivos de base de datos que debe formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-118">The output buffer that receives the list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="4a0b0-119">La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-119">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="4a0b0-120">Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-120">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<span data-ttu-id="4a0b0-121">*cbMax*</span><span class="sxs-lookup"><span data-stu-id="4a0b0-121">*cbMax*</span></span>

<span data-ttu-id="4a0b0-122">Tamaño máximo en bytes del búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-122">The maximum size in bytes of the output buffer.</span></span>

<span data-ttu-id="4a0b0-123">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="4a0b0-123">*pcbActual*</span></span>

<span data-ttu-id="4a0b0-124">Puntero al búfer de salida que recibe la cantidad real de datos de cadena.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-124">Pointer to the output buffer that receives the actual amount of string data.</span></span>

### <a name="return-value"></a><span data-ttu-id="4a0b0-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a0b0-125">Return Value</span></span>

<span data-ttu-id="4a0b0-126">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-126">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4a0b0-127">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4a0b0-127">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a0b0-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4a0b0-128">Return code</span></span></p></th>
<th><p><span data-ttu-id="4a0b0-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a0b0-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-130">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4a0b0-130">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-131">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-131">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a0b0-132">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="4a0b0-132">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-133">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-133">The operation failed because the current external backup has been aborted by a call to <a href="gg269309(v=exchg.10).md">JetStopBackupInstance</a>.</span></span> <span data-ttu-id="4a0b0-134">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-134">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-135">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="4a0b0-135">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-136">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-136">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a0b0-137">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="4a0b0-137">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-138">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-138">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="4a0b0-139">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-139">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-140">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="4a0b0-140">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-141">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-141">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="4a0b0-142"><strong>JetGetAttachInfoInstance</strong> devolverá este error si la copia de seguridad actual no es una copia de seguridad completa.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-142"><strong>JetGetAttachInfoInstance</strong> will return this error if the current backup is not a full backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a0b0-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="4a0b0-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-144">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-144">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="4a0b0-145">Esto puede ocurrir para <strong>JetGetAttachInfoInstance</strong> cuando el identificador de instancia especificado no es válido (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="4a0b0-145">This can happen for <strong>JetGetAttachInfoInstance</strong> when the specified instance handle is invalid (Windows XP and later releases).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-146">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="4a0b0-146">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-147">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-147">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a0b0-148">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="4a0b0-148">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-149">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-149">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-150">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="4a0b0-150">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-151">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-151">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a0b0-152">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="4a0b0-152">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-153">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-153">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-154">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="4a0b0-154">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="4a0b0-155">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-155">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4a0b0-156">Si se ejecuta correctamente, la información solicitada en el conjunto de archivos de base de datos que debe formar parte del conjunto de archivos de copia de seguridad se colocará en los búferes de salida, siempre que se proporcionen.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-156">On success, the requested information on the set of database files that should be part of the backup file set will be placed in the output buffers where provided.</span></span>

<span data-ttu-id="4a0b0-157">En caso de error, el estado de los búferes de salida es indefinido.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-157">On failure, the state of the output buffers is undefined.</span></span> <span data-ttu-id="4a0b0-158">El error producirá la cancelación de todo el proceso de copia de seguridad de la instancia.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-158">The failure will result in the cancellation of the entire backup process for the instance.</span></span>

#### <a name="remarks"></a><span data-ttu-id="4a0b0-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a0b0-159">Remarks</span></span>

<span data-ttu-id="4a0b0-160">Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-160">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span> <span data-ttu-id="4a0b0-161">La aplicación siempre debe proporcionar un búfer para recibir el tamaño real de esta lista y utilizar esa información para determinar si la lista se truncó.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-161">The application should always provide a buffer to receive the actual size of this list and use that information to determine if the list was truncated.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4a0b0-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a0b0-162">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-163"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4a0b0-163"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4a0b0-164">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-164">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a0b0-165"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4a0b0-165"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4a0b0-166">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-166">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-167"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4a0b0-167"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4a0b0-168">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-168">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a0b0-169"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="4a0b0-169"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4a0b0-170">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-170">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a0b0-171"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="4a0b0-171"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4a0b0-172">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4a0b0-172">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a0b0-173"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="4a0b0-173"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="4a0b0-174">Se implementa como <strong>JetGetAttachInfoInstanceW</strong> (Unicode) y <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="4a0b0-174">Implemented as <strong>JetGetAttachInfoInstanceW</strong> (Unicode) and <strong>JetGetAttachInfoInstanceA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4a0b0-175">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4a0b0-175">See Also</span></span>

[<span data-ttu-id="4a0b0-176">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4a0b0-176">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4a0b0-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4a0b0-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="4a0b0-178">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="4a0b0-178">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="4a0b0-179">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="4a0b0-179">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="4a0b0-180">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="4a0b0-180">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="4a0b0-181">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="4a0b0-181">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="4a0b0-182">JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="4a0b0-182">JetStopBackupInstance</span></span>](./jetstopbackupinstance-function.md)  
[<span data-ttu-id="4a0b0-183">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="4a0b0-183">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
