---
description: 'Más información acerca de: JetTruncateLog (función)'
title: JetTruncateLog función)
TOCTitle: JetTruncateLog Function
ms:assetid: 60cbf563-4228-452a-9b20-c7b1330c4514
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269263(v=EXCHG.10)
ms:contentKeyID: 32765565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e196a1570f769d8ae2619e962521bb181d506d63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809008"
---
# <a name="jettruncatelog-function"></a><span data-ttu-id="b7991-103">JetTruncateLog función)</span><span class="sxs-lookup"><span data-stu-id="b7991-103">JetTruncateLog Function</span></span>


<span data-ttu-id="b7991-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b7991-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncatelog-function"></a><span data-ttu-id="b7991-105">JetTruncateLog función)</span><span class="sxs-lookup"><span data-stu-id="b7991-105">JetTruncateLog Function</span></span>

<span data-ttu-id="b7991-106">La función **JetTruncateLog** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para eliminar los archivos de registro de transacciones que ya no se necesitarán una vez que la copia de seguridad actual se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7991-106">The **JetTruncateLog** function is used during a backup that is initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLog(void);
```

### <a name="parameters"></a><span data-ttu-id="b7991-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7991-107">Parameters</span></span>

<span data-ttu-id="b7991-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b7991-108">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="b7991-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b7991-109">Return Value</span></span>

<span data-ttu-id="b7991-110">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="b7991-110">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b7991-111">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b7991-111">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7991-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b7991-112">Return code</span></span></p></th>
<th><p><span data-ttu-id="b7991-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7991-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7991-114">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b7991-114">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b7991-115">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7991-115">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7991-116">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="b7991-116">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="b7991-117">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="b7991-117">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p>
<p><span data-ttu-id="b7991-118"><strong>Windows Server 2003:</strong>  Este valor devuelto se introduce en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b7991-118"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7991-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b7991-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b7991-120">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b7991-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7991-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b7991-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b7991-122">No se puede completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="b7991-122">The operation cannot complete because the instance that is associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="b7991-123"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7991-123"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7991-124">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="b7991-124">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="b7991-125">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b7991-125">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="b7991-126"><strong>JetTruncateLog</strong> devolverá este error si hay identificadores de archivo pendientes creados con <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para la instancia.</span><span class="sxs-lookup"><span data-stu-id="b7991-126"><strong>JetTruncateLog</strong> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7991-127">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="b7991-127">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="b7991-128">Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios parámetros produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="b7991-128">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="b7991-129">Esto puede ocurrir para <strong>JetTruncateLog</strong> cuando el identificador de instancia especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7991-129">This can happen for <strong>JetTruncateLog</strong> when the specified instance handle is invalid.</span></span></p>
<p><span data-ttu-id="b7991-130"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7991-130"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7991-131">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="b7991-131">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="b7991-132">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="b7991-132">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7991-133">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b7991-133">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b7991-134">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="b7991-134">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7991-135">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b7991-135">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b7991-136">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b7991-136">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7991-137">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="b7991-137">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="b7991-138">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="b7991-138">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7991-139">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b7991-139">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b7991-140">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b7991-140">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b7991-141">Si esta función se ejecuta correctamente, se elimina el conjunto de archivos de registro de transacciones que ya no se necesitarán una vez que se complete correctamente la copia de seguridad actual.</span><span class="sxs-lookup"><span data-stu-id="b7991-141">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="b7991-142">El equipo de estado de copia de seguridad se verá avanzado de modo que ya no se permita la copia de seguridad de los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="b7991-142">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="b7991-143">Solo se permite abrir archivos de revisión de base de datos y archivos de registro de transacciones para la copia de seguridad más allá de este punto.</span><span class="sxs-lookup"><span data-stu-id="b7991-143">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="b7991-144">Si se produce un error en esta función, el equipo de estado de copia de seguridad puede ser avanzado, de modo que ya no se permite la copia de seguridad de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="b7991-144">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="b7991-145">Es posible que se elimine un número de archivos de registro de transacciones que sea menor que el número deseado, pero siempre se eliminarán del más antiguo al más joven.</span><span class="sxs-lookup"><span data-stu-id="b7991-145">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b7991-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7991-146">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7991-147"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b7991-147"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b7991-148">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b7991-148">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7991-149"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b7991-149"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b7991-150">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b7991-150">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7991-151"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b7991-151"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b7991-152">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b7991-152">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7991-153"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="b7991-153"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b7991-154">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b7991-154">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7991-155"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b7991-155"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b7991-156">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b7991-156">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b7991-157">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b7991-157">See Also</span></span>

[<span data-ttu-id="b7991-158">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="b7991-158">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="b7991-159">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="b7991-159">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="b7991-160">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b7991-160">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b7991-161">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b7991-161">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b7991-162">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="b7991-162">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="b7991-163">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="b7991-163">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="b7991-164">JetStopService</span><span class="sxs-lookup"><span data-stu-id="b7991-164">JetStopService</span></span>](./jetstopservice-function.md)
