---
description: 'Más información acerca de: JetEndExternalBackupInstance2 (función)'
title: JetEndExternalBackupInstance2 función)
TOCTitle: JetEndExternalBackupInstance2 Function
ms:assetid: a30961f7-a1fb-44fe-881a-d46bf8f743b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294047(v=EXCHG.10)
ms:contentKeyID: 32765646
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndExternalBackupInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e719885cc61ff3f3193046b632e9969b8d660f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706711"
---
# <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="b897a-103">JetEndExternalBackupInstance2 función)</span><span class="sxs-lookup"><span data-stu-id="b897a-103">JetEndExternalBackupInstance2 Function</span></span>


<span data-ttu-id="b897a-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b897a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetendexternalbackupinstance2-function"></a><span data-ttu-id="b897a-105">JetEndExternalBackupInstance2 función)</span><span class="sxs-lookup"><span data-stu-id="b897a-105">JetEndExternalBackupInstance2 Function</span></span>

<span data-ttu-id="b897a-106">La función **JetEndExternalBackupInstance2** finaliza una sesión de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="b897a-106">The **JetEndExternalBackupInstance2** function ends an external backup session.</span></span> <span data-ttu-id="b897a-107">Esta API es la última API en una serie de API a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</span><span class="sxs-lookup"><span data-stu-id="b897a-107">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="b897a-108">**Windows XP: JetEndExternalBackupInstance2** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b897a-108">**Windows XP:  JetEndExternalBackupInstance2** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetEndExternalBackupInstance2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="b897a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b897a-109">Parameters</span></span>

<span data-ttu-id="b897a-110">*repetición*</span><span class="sxs-lookup"><span data-stu-id="b897a-110">*instance*</span></span>

<span data-ttu-id="b897a-111">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="b897a-111">The instance to use for this call.</span></span>

<span data-ttu-id="b897a-112">**Windows 2000:** En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="b897a-112">**Windows 2000:** For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="b897a-113">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="b897a-113">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="b897a-114">**Windows XP:** En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="b897a-114">**Windows XP:** For Windows XP and later releases, the API variant that does not accept this parameter can only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="b897a-115">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="b897a-115">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="b897a-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="b897a-116">*grbit*</span></span>

<span data-ttu-id="b897a-117">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="b897a-117">A group of bits that specifies zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b897a-118">Value</span><span class="sxs-lookup"><span data-stu-id="b897a-118">Value</span></span></p></th>
<th><p><span data-ttu-id="b897a-119">Significado</span><span class="sxs-lookup"><span data-stu-id="b897a-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b897a-120">JET_bitBackupEndAbort</span><span class="sxs-lookup"><span data-stu-id="b897a-120">JET_bitBackupEndAbort</span></span><br />
<span data-ttu-id="b897a-121">0x0002</span><span class="sxs-lookup"><span data-stu-id="b897a-121">0x0002</span></span></p></td>
<td><p><span data-ttu-id="b897a-122">La aplicación cliente está anulando la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b897a-122">The client application is aborting the backup.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b897a-123">JET_bitBackupEndNormal</span><span class="sxs-lookup"><span data-stu-id="b897a-123">JET_bitBackupEndNormal</span></span><br />
<span data-ttu-id="b897a-124">0x0001</span><span class="sxs-lookup"><span data-stu-id="b897a-124">0x0001</span></span></p></td>
<td><p><span data-ttu-id="b897a-125">La aplicación cliente finalizó la copia de seguridad por completo y termina normalmente.</span><span class="sxs-lookup"><span data-stu-id="b897a-125">The client application finished the backup completely, and is ending normally.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b897a-126">JET_bitBackupTruncateDone</span><span class="sxs-lookup"><span data-stu-id="b897a-126">JET_bitBackupTruncateDone</span></span><br />
<span data-ttu-id="b897a-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="b897a-127">0x0100</span></span></p></td>
<td><p><span data-ttu-id="b897a-128"><strong>Windows Vista:  </strong> JET_bitBackupTruncateDone se introduce en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b897a-128"><strong>Windows Vista:  </strong>JET_bitBackupTruncateDone is introduced in Windows Vista.</span></span></p>
<p><span data-ttu-id="b897a-129">El motor puede marcar los encabezados de la base de datos según corresponda (por ejemplo, una copia de seguridad completa completada), aunque no se haya completado la llamada a TRUNCATE.</span><span class="sxs-lookup"><span data-stu-id="b897a-129">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="b897a-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b897a-130">Return Value</span></span>

<span data-ttu-id="b897a-131">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="b897a-131">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="b897a-132">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b897a-132">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b897a-133">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b897a-133">Return code</span></span></p></th>
<th><p><span data-ttu-id="b897a-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="b897a-134">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b897a-135">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="b897a-135">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="b897a-136">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b897a-136">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b897a-137">JET_errBackupAbortByCaller</span><span class="sxs-lookup"><span data-stu-id="b897a-137">JET_errBackupAbortByCaller</span></span></p></td>
<td><p><span data-ttu-id="b897a-138"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b897a-138"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="b897a-139">El autor de la llamada finalizó una copia de seguridad en medio de la secuencia de copia de seguridad sin señalar la intención con <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="b897a-139">The caller terminated a backup in the middle of the backup sequence without signaling the intention with <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span> <span data-ttu-id="b897a-140">Este error se debe a un error en el cliente de copia de seguridad en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b897a-140">This error is result of a bug in the backup client in Windows Server 2003 and later.</span></span> <span data-ttu-id="b897a-141">En Windows XP, este error se devuelve para una terminación intencionada de la secuencia de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="b897a-141">In Windows XP this error is returned for an intentional termination of the external backup sequence.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b897a-142">JET_errBackupAbortByServer</span><span class="sxs-lookup"><span data-stu-id="b897a-142">JET_errBackupAbortByServer</span></span></p></td>
<td><p><span data-ttu-id="b897a-143"><strong>Windows Server 2003:  </strong> Este valor devuelto se introduce en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b897a-143"><strong>Windows Server 2003:  </strong>This return value is introduced in Windows Server 2003.</span></span></p>
<p><span data-ttu-id="b897a-144">No se pudo realizar la operación porque la copia de seguridad externa actual se ha anulado mediante una llamada a <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span><span class="sxs-lookup"><span data-stu-id="b897a-144">The operation failed because the current external backup has been aborted by a call to <a href="gg294067(v=exchg.10).md">JetStopBackup</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b897a-145">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="b897a-145">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="b897a-146">No se puede completar la operación porque todas las actividades de la instancia que está asociada a la sesión han dejado de funcionar como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="b897a-146">The operation cannot complete because all activity on the instance that is associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b897a-147">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="b897a-147">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="b897a-148"><strong>Windows XP:  </strong> Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b897a-148"><strong>Windows XP:  </strong>This return value is introduced in Windows XP.</span></span></p>
<p><span data-ttu-id="b897a-149">No se puede completar la operación porque la instancia asociada a la sesión encontró un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="b897a-149">The operation cannot complete because the instance that is associated with the session encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b897a-150">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="b897a-150">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="b897a-151">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="b897a-151">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b897a-152">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="b897a-152">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="b897a-153">No se puede completar la operación porque la instancia de asociada a la sesión aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="b897a-153">The operation cannot complete because the instance that is associated with the session has not yet been initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b897a-154">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="b897a-154">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="b897a-155">No se puede completar la operación porque hay una operación de restauración en curso en la instancia que está asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b897a-155">The operation cannot complete because a restore operation is in progress on the instance that is associated with the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b897a-156">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="b897a-156">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="b897a-157">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="b897a-157">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b897a-158">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="b897a-158">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="b897a-159">No se puede completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="b897a-159">The operation cannot complete because the instance that is associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b897a-160">Si la función se ejecuta correctamente, la copia de seguridad externa era correcta.</span><span class="sxs-lookup"><span data-stu-id="b897a-160">If the function succeeds, the external backup was a success.</span></span> <span data-ttu-id="b897a-161">Success indica que todos los archivos (por ejemplo, bases de datos y registros) que son adecuados para el tipo de copia de seguridad (especificado en [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) se recuperaron del motor de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b897a-161">Success indicates that all files (for example, databases and logs) that are appropriate for the type of backup (specified in [JetBeginExternalBackup](./jetbeginexternalbackup-function.md)) were retrieved from the backup engine.</span></span> <span data-ttu-id="b897a-162">Los archivos de copia de seguridad se pueden recuperar con recuperación de hardware ([JetExternalRestore](./jetexternalrestore-function.md)).</span><span class="sxs-lookup"><span data-stu-id="b897a-162">The backed up files can be recovered with hard recovery ([JetExternalRestore](./jetexternalrestore-function.md)).</span></span>

<span data-ttu-id="b897a-163">Si se produce un error en esta función, normalmente finaliza la copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="b897a-163">If this function fails, the external backup usually ends.</span></span> <span data-ttu-id="b897a-164">El error significa que la copia de seguridad no es válida debido a un error de uso del cliente o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b897a-164">Failure means that the backup is invalid because of a client or an application usage error.</span></span> <span data-ttu-id="b897a-165">Es importante comprobar el código de retorno de esta API para comprobar que la secuencia de copia de seguridad se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b897a-165">It is important to check the return code for this API to verify that the backup sequence was successful.</span></span>

#### <a name="remarks"></a><span data-ttu-id="b897a-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b897a-166">Remarks</span></span>

<span data-ttu-id="b897a-167">Si el motor está configurado para registrar eventos, se registra un evento para indicar la resolución de la copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="b897a-167">If the engine is configured to log events, an event is logged to indicate the resolution of the external backup.</span></span>

<span data-ttu-id="b897a-168">Si la secuencia de copia de seguridad no se completa en orden y con una llamada correcta a [JetEndExternalBackup](./jetendexternalbackup-function.md), las copias de seguridad incrementales subsiguientes podrían contener más datos de los esperados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b897a-168">If the backup sequence is not completed in order and with a successful call to [JetEndExternalBackup](./jetendexternalbackup-function.md), subsequent incremental backups might contain more data than the application anticipated.</span></span>

<span data-ttu-id="b897a-169">Para obtener más información sobre la secuencia de API de copia de seguridad externa, vea [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span><span class="sxs-lookup"><span data-stu-id="b897a-169">For more information about the external backup API sequence, see [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).</span></span>

<span data-ttu-id="b897a-170">Antes de Windows Vista, si no se realizó el truncamiento del registro, el motor consideró que la copia de seguridad era una copia de seguridad de copia.</span><span class="sxs-lookup"><span data-stu-id="b897a-170">Before Windows Vista, if the log truncation was not done, the engine considered that the backup was a copy backup.</span></span> <span data-ttu-id="b897a-171">Sin embargo, la copia de seguridad puede ser una copia de seguridad normal para la que no se ha realizado el truncamiento (por ejemplo, si hay bases de datos desasociadas).</span><span class="sxs-lookup"><span data-stu-id="b897a-171">However, the backup might be a normal backup for which truncation was not done (for example, if there are detached databases).</span></span> <span data-ttu-id="b897a-172">La opción JET_bitBackupTruncateDone se puede usar para informar al motor sobre esto y permitir las modificaciones de encabezado de base de datos apropiadas.</span><span class="sxs-lookup"><span data-stu-id="b897a-172">The JET_bitBackupTruncateDone option can be used to inform the engine about this and allow appropriate database header modifications.</span></span>

#### <a name="requirements"></a><span data-ttu-id="b897a-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b897a-173">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b897a-174"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b897a-174"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b897a-175">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b897a-175">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b897a-176"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b897a-176"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b897a-177">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b897a-177">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b897a-178"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b897a-178"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b897a-179">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b897a-179">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b897a-180"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="b897a-180"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="b897a-181">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="b897a-181">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b897a-182"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="b897a-182"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="b897a-183">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="b897a-183">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="b897a-184">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b897a-184">See Also</span></span>

[<span data-ttu-id="b897a-185">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="b897a-185">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="b897a-186">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="b897a-186">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="b897a-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="b897a-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="b897a-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="b897a-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="b897a-189">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="b897a-189">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="b897a-190">JetBeginExternalBackup</span><span class="sxs-lookup"><span data-stu-id="b897a-190">JetBeginExternalBackup</span></span>](./jetbeginexternalbackup-function.md)  
[<span data-ttu-id="b897a-191">JetBeginExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="b897a-191">JetBeginExternalBackupInstance</span></span>](./jetbeginexternalbackupinstance-function.md)  
[<span data-ttu-id="b897a-192">JetCloseFile</span><span class="sxs-lookup"><span data-stu-id="b897a-192">JetCloseFile</span></span>](./jetclosefile-function.md)  
[<span data-ttu-id="b897a-193">JetExternalRestore</span><span class="sxs-lookup"><span data-stu-id="b897a-193">JetExternalRestore</span></span>](./jetexternalrestore-function.md)  
[<span data-ttu-id="b897a-194">JetGetAttachInfo</span><span class="sxs-lookup"><span data-stu-id="b897a-194">JetGetAttachInfo</span></span>](./jetgetattachinfo-function.md)  
[<span data-ttu-id="b897a-195">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="b897a-195">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="b897a-196">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="b897a-196">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="b897a-197">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="b897a-197">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="b897a-198">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="b897a-198">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="b897a-199">JetStopBackup</span><span class="sxs-lookup"><span data-stu-id="b897a-199">JetStopBackup</span></span>](./jetstopbackup-function.md)  
[<span data-ttu-id="b897a-200">JetStopService</span><span class="sxs-lookup"><span data-stu-id="b897a-200">JetStopService</span></span>](./jetstopservice-function.md)  
[<span data-ttu-id="b897a-201">JetTruncateLog</span><span class="sxs-lookup"><span data-stu-id="b897a-201">JetTruncateLog</span></span>](./jettruncatelog-function.md)
