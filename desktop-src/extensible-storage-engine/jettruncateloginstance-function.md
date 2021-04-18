---
description: 'Más información acerca de: JetTruncateLogInstance (función)'
title: JetTruncateLogInstance función)
TOCTitle: JetTruncateLogInstance Function
ms:assetid: 9b6852c6-a991-4d7b-bc54-49092f788751
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269352(v=EXCHG.10)
ms:contentKeyID: 32765639
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTruncateLogInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7286b97b80c323eb6bba7b9d28057bf45eec3920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715293"
---
# <a name="jettruncateloginstance-function"></a><span data-ttu-id="671bd-103">JetTruncateLogInstance función)</span><span class="sxs-lookup"><span data-stu-id="671bd-103">JetTruncateLogInstance Function</span></span>


<span data-ttu-id="671bd-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="671bd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jettruncateloginstance-function"></a><span data-ttu-id="671bd-105">JetTruncateLogInstance función)</span><span class="sxs-lookup"><span data-stu-id="671bd-105">JetTruncateLogInstance Function</span></span>

<span data-ttu-id="671bd-106">La función **JetTruncateLogInstance** se usa durante una copia de seguridad iniciada por [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) para eliminar los archivos de registro de transacciones que ya no se necesitarán una vez que la copia de seguridad actual se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="671bd-106">The **JetTruncateLogInstance** function is used during a backup initiated by [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="671bd-107">**Windows XP:**  **JetTruncateLogInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="671bd-107">**Windows XP:**  **JetTruncateLogInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetTruncateLogInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="671bd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="671bd-108">Parameters</span></span>

<span data-ttu-id="671bd-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="671bd-109">*instance*</span></span>

<span data-ttu-id="671bd-110">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="671bd-110">The instance to use for this call.</span></span>

<span data-ttu-id="671bd-111">En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="671bd-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="671bd-112">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="671bd-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="671bd-113">En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="671bd-113">For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="671bd-114">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="671bd-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="671bd-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="671bd-115">Return Value</span></span>

<span data-ttu-id="671bd-116">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="671bd-116">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="671bd-117">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="671bd-117">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="671bd-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="671bd-118">Return code</span></span></p></th>
<th><p><span data-ttu-id="671bd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="671bd-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="671bd-120">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="671bd-120">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="671bd-121">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="671bd-121">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671bd-122">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="671bd-122">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="671bd-123"><strong>Windows Server 2003:</strong>  Este valor devuelto se introduce en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="671bd-123"><strong>Windows Server 2003:</strong>  This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="671bd-124">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="671bd-124">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671bd-125">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="671bd-125">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="671bd-126">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="671bd-126">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671bd-127">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="671bd-127">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="671bd-128">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="671bd-128">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span> <span data-ttu-id="671bd-129">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="671bd-129">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671bd-130">JET_errInvalidBackupSequence</span><span class="sxs-lookup"><span data-stu-id="671bd-130">JET_errInvalidBackupSequence</span></span></p></td>
<td><p><span data-ttu-id="671bd-131">No se pudo realizar la operación de copia de seguridad porque se llamó fuera de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="671bd-131">The backup operation failed because it was called out of sequence.</span></span> <span data-ttu-id="671bd-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> devolverá este error si hay identificadores de archivo pendientes creados con <a href="gg269249(v=exchg.10).md">JetOpenFile</a> para la instancia.</span><span class="sxs-lookup"><span data-stu-id="671bd-132"><a href="gg269263(v=exchg.10).md">JetTruncateLog</a> will return this error if there are any outstanding file handles that were created using <a href="gg269249(v=exchg.10).md">JetOpenFile</a> for the instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671bd-133">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="671bd-133">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="671bd-134">Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios parámetros produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="671bd-134">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="671bd-135">Esto puede ocurrir para <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> cuando el identificador de instancia especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="671bd-135">This can happen for <a href="gg269263(v=exchg.10).md">JetTruncateLog</a> when the specified instance handle is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671bd-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="671bd-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="671bd-137">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="671bd-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671bd-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="671bd-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="671bd-139">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="671bd-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671bd-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="671bd-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="671bd-141">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="671bd-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671bd-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="671bd-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="671bd-143">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="671bd-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671bd-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="671bd-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="671bd-145">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="671bd-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="671bd-146">Si esta función se ejecuta correctamente, se elimina el conjunto de archivos de registro de transacciones que ya no se necesitarán una vez que se complete correctamente la copia de seguridad actual.</span><span class="sxs-lookup"><span data-stu-id="671bd-146">If this function succeeds, the set of transaction log files that will no longer be needed once the current backup completes successfully are deleted.</span></span> <span data-ttu-id="671bd-147">El equipo de estado de copia de seguridad se verá avanzado de modo que ya no se permita la copia de seguridad de los archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="671bd-147">The backup state machine will be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="671bd-148">Solo se permite abrir archivos de revisión de base de datos y archivos de registro de transacciones para la copia de seguridad más allá de este punto.</span><span class="sxs-lookup"><span data-stu-id="671bd-148">Only database patch files and transaction log files are permitted to be opened for backup beyond this point.</span></span>

<span data-ttu-id="671bd-149">Si se produce un error en esta función, el equipo de estado de copia de seguridad puede ser avanzado, de modo que ya no se permite la copia de seguridad de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="671bd-149">If this function fails, the backup state machine can be advanced such that the backup of database files is no longer allowed.</span></span> <span data-ttu-id="671bd-150">Es posible que se elimine un número de archivos de registro de transacciones que sea menor que el número deseado, pero siempre se eliminarán del más antiguo al más joven.</span><span class="sxs-lookup"><span data-stu-id="671bd-150">Some number of transaction log files might be deleted that is less than the desired number, but they will always be deleted from oldest to youngest.</span></span>

#### <a name="requirements"></a><span data-ttu-id="671bd-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671bd-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="671bd-152"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="671bd-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="671bd-153">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="671bd-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671bd-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="671bd-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="671bd-155">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="671bd-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671bd-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="671bd-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="671bd-157">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="671bd-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="671bd-158"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="671bd-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="671bd-159">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="671bd-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="671bd-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="671bd-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="671bd-161">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="671bd-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="671bd-162">Consulte también</span><span class="sxs-lookup"><span data-stu-id="671bd-162">See Also</span></span>

[<span data-ttu-id="671bd-163">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="671bd-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="671bd-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="671bd-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="671bd-165">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="671bd-165">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="671bd-166">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="671bd-166">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="671bd-167">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="671bd-167">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="671bd-168">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="671bd-168">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="671bd-169">JetStopService</span><span class="sxs-lookup"><span data-stu-id="671bd-169">JetStopService</span></span>](./jetstopservice-function.md)
