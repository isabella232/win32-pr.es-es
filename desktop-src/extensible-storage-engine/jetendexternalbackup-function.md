---
description: 'Más información acerca de: JetEndExternalBackup (función)'
title: Función JetEndExternalBackup
TOCTitle: JetEndExternalBackup Function
ms:assetid: 058f903b-14b7-44b3-9ec7-7c05c9ec6363
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269176(v=EXCHG.10)
ms:contentKeyID: 32765479
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackup
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 91f3db40fef483114313bbaa5f01e592d860bde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707435"
---
# <a name="jetendexternalbackup-function"></a><span data-ttu-id="5d741-103">Función JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="5d741-103">JetEndExternalBackup Function</span></span>


<span data-ttu-id="5d741-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5d741-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackup-function"></a><span data-ttu-id="5d741-105">Función JetEndExternalBackup</span><span class="sxs-lookup"><span data-stu-id="5d741-105">JetEndExternalBackup Function</span></span>

<span data-ttu-id="5d741-106">La función **JetEndExternalBackup** finaliza una sesión de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="5d741-106">The **JetEndExternalBackup** function ends an external backup session.</span></span> <span data-ttu-id="5d741-107">Esta función es el último elemento de la API en una serie de elementos de la API a los que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</span><span class="sxs-lookup"><span data-stu-id="5d741-107">This function is the last API element in a series of API elements that must be called to execute a successful online (non-VSS based) backup.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackup(void);
```

### <a name="parameters"></a><span data-ttu-id="5d741-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d741-108">Parameters</span></span>

<span data-ttu-id="5d741-109">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5d741-109">This function has no parameters.</span></span>

### <a name="return-value"></a><span data-ttu-id="5d741-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d741-110">Return Value</span></span>

<span data-ttu-id="5d741-111">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="5d741-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="5d741-112">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5d741-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d741-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5d741-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="5d741-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d741-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d741-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="5d741-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="5d741-116">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5d741-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d741-117">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="5d741-117">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="5d741-118">No se puede completar la operación porque la instancia de que está asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="5d741-118">The operation cannot complete because the instance that is associated with the session has not been yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d741-119">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="5d741-119">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="5d741-120">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="5d741-120">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d741-121">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="5d741-121">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="5d741-122"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d741-122"><strong>Windows XP:  </strong>This return value is introduced in Windows XP</span></span></p>
<p><span data-ttu-id="5d741-123">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere el acceso a todos los datos que se revocan para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="5d741-123">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d741-124">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="5d741-124">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d741-125">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5d741-125">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d741-126">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="5d741-126">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="5d741-127">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="5d741-127">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d741-128">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="5d741-128">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="5d741-129">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="5d741-129">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d741-130">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="5d741-130">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="5d741-131"><strong>Windows Server 2003:  </strong> Este valor devuelto se introduce en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5d741-131"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="5d741-132">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="5d741-132">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d741-133">errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="5d741-133">errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="5d741-134"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5d741-134"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="5d741-135">El autor de la llamada finalizó una copia de seguridad en medio de la secuencia de copia de seguridad sin señalar la intención con <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="5d741-135">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="5d741-136">Este error se debe a un error en el cliente de copia de seguridad en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5d741-136">This error is a result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="5d741-137">En Windows XP, este error se devuelve para una terminación intencionada de la secuencia de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="5d741-137">On Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d741-138">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="5d741-138">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="5d741-139">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="5d741-139">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5d741-140">Si esta función se ejecuta correctamente, la copia de seguridad externa era correcta.</span><span class="sxs-lookup"><span data-stu-id="5d741-140">If this function succeeds, the external backup was a success.</span></span> <span data-ttu-id="5d741-141">Success indica que todos los archivos (por ejemplo, bases de datos y registros) que son adecuados para el tipo de copia de seguridad (especificado en [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) se recuperaron del motor de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5d741-141">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="5d741-142">Los archivos de copia de seguridad se pueden recuperar con recuperación de hardware ([JetExternalRestore](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="5d741-142">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="5d741-143">Si se produce un error en esta función, normalmente finaliza la copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="5d741-143">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="5d741-144">El error significa que la copia de seguridad no es válida debido a un error de uso del cliente o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d741-144">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="5d741-145">Es importante comprobar el código de retorno de esta API para comprobar que la secuencia de copia de seguridad se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5d741-145">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="5d741-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d741-146">Remarks</span></span>

<span data-ttu-id="5d741-147">Si el motor está configurado para registrar eventos, se registra un evento para indicar la resolución de la copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="5d741-147">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="5d741-148">Si la secuencia de copia de seguridad no se completa en orden y con una llamada correcta a **JetEndExternalBackup**, las copias de seguridad incrementales subsiguientes podrían contener más datos de los esperados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d741-148">If the backup sequence is not completed in order and with a successful call to **JetEndExternalBackup**, subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="5d741-149">Para obtener más información sobre la secuencia de API de copia de seguridad externa, vea [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="5d741-149">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="5d741-150">Antes de Windows Vista, si no se realizó el truncamiento del registro, el motor consideró que la copia de seguridad era una copia de seguridad de copia.</span><span class="sxs-lookup"><span data-stu-id="5d741-150">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="5d741-151">Sin embargo, la copia de seguridad puede ser una copia de seguridad normal para la que no se ha realizado el truncamiento (por ejemplo, si hay bases de datos desasociadas).</span><span class="sxs-lookup"><span data-stu-id="5d741-151">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="5d741-152">La opción JET_bitBackupTruncateDone se puede usar para informar al motor sobre esto y permitir las modificaciones de encabezado de base de datos apropiadas.</span><span class="sxs-lookup"><span data-stu-id="5d741-152">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="5d741-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d741-153">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d741-154"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="5d741-154"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5d741-155">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="5d741-155">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d741-156"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5d741-156"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5d741-157">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5d741-157">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d741-158"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5d741-158"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5d741-159">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="5d741-159">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d741-160"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="5d741-160"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="5d741-161">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="5d741-161">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d741-162"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="5d741-162"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="5d741-163">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="5d741-163">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="5d741-164">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5d741-164">See Also</span></span>

[<span data-ttu-id="5d741-165">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="5d741-165">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="5d741-166">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="5d741-166">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="5d741-167">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="5d741-167">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="5d741-168">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="5d741-168">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="5d741-169">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="5d741-169">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="5d741-170">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="5d741-170">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="5d741-171">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="5d741-171">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="5d741-172">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="5d741-172">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="5d741-173">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="5d741-173">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="5d741-174">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="5d741-174">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="5d741-175">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="5d741-175">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="5d741-176">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="5d741-176">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="5d741-177">JetStopService</span><span class="sxs-lookup"><span data-stu-id="5d741-177">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="5d741-178">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="5d741-178">JetTruncateLog</span></span>](./jettruncatelog-function.md)
