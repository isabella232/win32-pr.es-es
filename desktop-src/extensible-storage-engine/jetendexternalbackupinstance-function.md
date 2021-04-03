---
description: 'Más información acerca de: JetEndExternalBackupInstance (función)'
title: JetEndExternalBackupInstance función)
TOCTitle: JetEndExternalBackupInstance Function
ms:assetid: 2256f63e-91f5-44ad-b67e-506dd71ffa94
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269204(v=EXCHG.10)
ms:contentKeyID: 32765507
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a017a0dbb4fa2f92c3e43a9dd2ff5649b65ee375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083044"
---
# <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="898ad-103">JetEndExternalBackupInstance función)</span><span class="sxs-lookup"><span data-stu-id="898ad-103">JetEndExternalBackupInstance Function</span></span>


<span data-ttu-id="898ad-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="898ad-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance-function"></a><span data-ttu-id="898ad-105">JetEndExternalBackupInstance función)</span><span class="sxs-lookup"><span data-stu-id="898ad-105">JetEndExternalBackupInstance Function</span></span>

<span data-ttu-id="898ad-106">La función **JetEndExternalBackupInstance** finaliza una sesión de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="898ad-106">The **JetEndExternalBackupInstance** function ends an external backup session.</span></span> <span data-ttu-id="898ad-107">Esta API es la última API en una serie de API a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</span><span class="sxs-lookup"><span data-stu-id="898ad-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="898ad-108">**Windows XP: JetEndExternalBackupInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="898ad-108">**Windows XP:  JetEndExternalBackupInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a><span data-ttu-id="898ad-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="898ad-109">Parameters</span></span>

<span data-ttu-id="898ad-110">*repetición*</span><span class="sxs-lookup"><span data-stu-id="898ad-110">*instance*</span></span>

<span data-ttu-id="898ad-111">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="898ad-111">The instance to use for this call.</span></span>

<span data-ttu-id="898ad-112">**Windows 2000:** En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="898ad-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="898ad-113">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="898ad-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="898ad-114">**Windows XP:** En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="898ad-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="898ad-115">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="898ad-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

### <a name="return-value"></a><span data-ttu-id="898ad-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="898ad-116">Return Value</span></span>

<span data-ttu-id="898ad-117">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="898ad-117">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="898ad-118">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="898ad-118">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="898ad-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="898ad-119">Return code</span></span></p></th>
<th><p><span data-ttu-id="898ad-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="898ad-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="898ad-121">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="898ad-121">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="898ad-122">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="898ad-122">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="898ad-123">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="898ad-123">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="898ad-124"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="898ad-124"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="898ad-125">El autor de la llamada finalizó una copia de seguridad en medio de la secuencia de copia de seguridad sin señalar la intención con <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="898ad-125">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="898ad-126">Este error es el resultado de un error en el cliente de copia de seguridad en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="898ad-126">This error is the result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="898ad-127">En Windows XP, este error se devuelve para una terminación intencionada de la secuencia de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="898ad-127">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="898ad-128">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="898ad-128">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="898ad-129"><strong>Windows Server 2003:  </strong> Este valor devuelto se introduce en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="898ad-129"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="898ad-130">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="898ad-130">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="898ad-131">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="898ad-131">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="898ad-132">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="898ad-132">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="898ad-133">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="898ad-133">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="898ad-134"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="898ad-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="898ad-135">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="898ad-135">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="898ad-136">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="898ad-136">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="898ad-137">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="898ad-137">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="898ad-138">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="898ad-138">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="898ad-139">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="898ad-139">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="898ad-140">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="898ad-140">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="898ad-141">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="898ad-141">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="898ad-142">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="898ad-142">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="898ad-143">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="898ad-143">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="898ad-144">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="898ad-144">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="898ad-145">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="898ad-145">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="898ad-146">Si la función se ejecuta correctamente, la copia de seguridad externa era correcta.</span><span class="sxs-lookup"><span data-stu-id="898ad-146">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="898ad-147">Success indica que todos los archivos (por ejemplo, bases de datos y registros) que son adecuados para el tipo de copia de seguridad (especificado en [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) se recuperaron del motor de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="898ad-147">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="898ad-148">Los archivos de copia de seguridad se pueden recuperar con recuperación de hardware ([JetExternalRestore](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="898ad-148">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="898ad-149">Si se produce un error en esta función, normalmente finaliza la copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="898ad-149">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="898ad-150">El error significa que la copia de seguridad no es válida debido a un error de uso del cliente o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="898ad-150">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="898ad-151">Es importante comprobar el código de retorno de esta API para comprobar que la secuencia de copia de seguridad se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="898ad-151">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="898ad-152">Observaciones</span><span class="sxs-lookup"><span data-stu-id="898ad-152">Remarks</span></span>

<span data-ttu-id="898ad-153">Si el motor está configurado para registrar eventos, se registra un evento para indicar la resolución de la copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="898ad-153">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="898ad-154">Si la secuencia de copia de seguridad no se completa en orden y con una llamada correcta a [JetEndExternalBackup](./jetendexternalbackup-function.md), las copias de seguridad incrementales subsiguientes podrían contener más datos de los esperados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="898ad-154">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="898ad-155">Para obtener más información sobre la secuencia de API de copia de seguridad externa, vea [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="898ad-155">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="898ad-156">Antes de Windows Vista, si no se realizó el truncamiento del registro, el motor consideró que la copia de seguridad era una copia de seguridad de copia.</span><span class="sxs-lookup"><span data-stu-id="898ad-156">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="898ad-157">Sin embargo, la copia de seguridad puede ser una copia de seguridad normal para la que no se ha realizado el truncamiento (por ejemplo, si hay bases de datos desasociadas).</span><span class="sxs-lookup"><span data-stu-id="898ad-157">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="898ad-158">La opción JET_bitBackupTruncateDone se puede usar para informar al motor sobre esto y permitir modificaciones de encabezado de base de datos adecuadas.</span><span class="sxs-lookup"><span data-stu-id="898ad-158">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow proper database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="898ad-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="898ad-159">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="898ad-160"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="898ad-160"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="898ad-161">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="898ad-161">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="898ad-162"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="898ad-162"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="898ad-163">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="898ad-163">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="898ad-164"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="898ad-164"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="898ad-165">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="898ad-165">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="898ad-166"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="898ad-166"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="898ad-167">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="898ad-167">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="898ad-168"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="898ad-168"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="898ad-169">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="898ad-169">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="898ad-170">Consulte también</span><span class="sxs-lookup"><span data-stu-id="898ad-170">See Also</span></span>

[<span data-ttu-id="898ad-171">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="898ad-171">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="898ad-172">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="898ad-172">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="898ad-173">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="898ad-173">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="898ad-174">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="898ad-174">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="898ad-175">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="898ad-175">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="898ad-176">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="898ad-176">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="898ad-177">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="898ad-177">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="898ad-178">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="898ad-178">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="898ad-179">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="898ad-179">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="898ad-180">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="898ad-180">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="898ad-181">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="898ad-181">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="898ad-182">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="898ad-182">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="898ad-183">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="898ad-183">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="898ad-184">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="898ad-184">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="898ad-185">JetStopService</span><span class="sxs-lookup"><span data-stu-id="898ad-185">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="898ad-186">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="898ad-186">JetTruncateLog</span></span>](./jettruncatelog-function.md)
