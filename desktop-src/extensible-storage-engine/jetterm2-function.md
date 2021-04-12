---
description: 'Más información acerca de: JetTerm2 (función)'
title: Función JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154564"
---
# <a name="jetterm2-function"></a><span data-ttu-id="30925-103">Función JetTerm2</span><span class="sxs-lookup"><span data-stu-id="30925-103">JetTerm2 Function</span></span>


<span data-ttu-id="30925-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="30925-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetterm2-function"></a><span data-ttu-id="30925-105">Función JetTerm2</span><span class="sxs-lookup"><span data-stu-id="30925-105">JetTerm2 Function</span></span>

<span data-ttu-id="30925-106">La función **JetTerm2** inicia el cierre de una instancia de que [JetInit](./jetinit-function.md)ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="30925-106">The **JetTerm2** function initiates the shutdown of an instance that has been initialized by [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="30925-107">**JetTerm2** también puede destruir una instancia no inicializada creada por [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="30925-107">**JetTerm2** can also destroy an uninitialized instance that was created by [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="30925-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30925-108">Parameters</span></span>

<span data-ttu-id="30925-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="30925-109">*instance*</span></span>

<span data-ttu-id="30925-110">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="30925-110">The instance to use for this call.</span></span>

<span data-ttu-id="30925-111">**Windows 2000:**  Este parámetro se omite y siempre debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="30925-111">**Windows 2000:**  This parameter is ignored and should always be **NULL**.</span></span>

<span data-ttu-id="30925-112">**Windows XP y versiones posteriores:**  Este parámetro está sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="30925-112">**Windows XP and later releases:**  This parameter is overloaded.</span></span> <span data-ttu-id="30925-113">Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser **null** o contener la instancia real devuelta por [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="30925-113">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, then this parameter might be **NULL** or might contain the actual instance that is returned by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="30925-114">Si el motor está funcionando en modo de varias instancias, este parámetro debe ser un puntero a una instancia de creada mediante [JetCreateInstance](./jetcreateinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="30925-114">If the engine is operating in multi-instance mode, then this parameter must be a pointer to an instance that was created using [JetCreateInstance](./jetcreateinstance-function.md).</span></span>

<span data-ttu-id="30925-115">*grbit*</span><span class="sxs-lookup"><span data-stu-id="30925-115">*grbit*</span></span>

<span data-ttu-id="30925-116">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="30925-116">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30925-117">Value</span><span class="sxs-lookup"><span data-stu-id="30925-117">Value</span></span></p></th>
<th><p><span data-ttu-id="30925-118">Significado</span><span class="sxs-lookup"><span data-stu-id="30925-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30925-119">JET_bitTermComplete</span><span class="sxs-lookup"><span data-stu-id="30925-119">JET_bitTermComplete</span></span></p></td>
<td><p><span data-ttu-id="30925-120">Solicita que la instancia se cierre sin problemas.</span><span class="sxs-lookup"><span data-stu-id="30925-120">Requests that the instance be shut down cleanly.</span></span> <span data-ttu-id="30925-121">Cualquier trabajo de limpieza opcional que se haría normalmente en segundo plano en tiempo de ejecución se completa inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="30925-121">Any optional cleanup work that would ordinarily be done in the background at run time is completed immediately.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30925-122">JET_bitTermAbrupt</span><span class="sxs-lookup"><span data-stu-id="30925-122">JET_bitTermAbrupt</span></span></p></td>
<td><p><span data-ttu-id="30925-123">Solicita que la instancia se cierre lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="30925-123">Requests that the instance be shut down as quickly as possible.</span></span> <span data-ttu-id="30925-124">Se abandona cualquier trabajo opcional que normalmente se realizaría en segundo plano en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="30925-124">Any optional work that would ordinarily be done in the background at run time is abandoned.</span></span></p>
<p><span data-ttu-id="30925-125"><strong>Nota:</strong>  Esta opción puede provocar una pérdida temporal o permanente de espacio en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="30925-125"><strong>Note</strong>  This option can cause temporary or permanent space loss in the database.</span></span> <span data-ttu-id="30925-126">Este espacio perdido siempre se puede recuperar a través de una desfragmentación sin conexión de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="30925-126">This lost space can always be recovered through an offline defragmentation of the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30925-127">JET_bitTermStopBackup</span><span class="sxs-lookup"><span data-stu-id="30925-127">JET_bitTermStopBackup</span></span></p></td>
<td><p><span data-ttu-id="30925-128">Solicita que se cierre la instancia incluso si actualmente hay una copia de seguridad en curso.</span><span class="sxs-lookup"><span data-stu-id="30925-128">Requests that the instance be shut down even if there is currently a backup in progress.</span></span> <span data-ttu-id="30925-129">Normalmente, una copia de seguridad pendiente provocaría un error de <a href="gg269298(v=exchg.10).md">JetTerm</a> con JET_errBackupInProgress.</span><span class="sxs-lookup"><span data-stu-id="30925-129">Ordinarily, a pending backup would cause <a href="gg269298(v=exchg.10).md">JetTerm</a> to fail with JET_errBackupInProgress.</span></span> <span data-ttu-id="30925-130">Cuando este parámetro no está presente, se supone que su valor es JET_bitTermAbrupt.</span><span class="sxs-lookup"><span data-stu-id="30925-130">When this parameter is not present, its value is presumed to be JET_bitTermAbrupt.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30925-131">JET_bitTermDirty</span><span class="sxs-lookup"><span data-stu-id="30925-131">JET_bitTermDirty</span></span></p></td>
<td><p><span data-ttu-id="30925-132">Solicita que se cierre la instancia con todas las bases de datos adjuntas que quedan en un estado sucio.</span><span class="sxs-lookup"><span data-stu-id="30925-132">Requests that the instance be shut down with all the attached databases left in a dirty state.</span></span></p>
<p><span data-ttu-id="30925-133">Windows 7: JET_bitTermDirty se introduce en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="30925-133">Windows 7: JET_bitTermDirty is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="30925-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30925-134">Return Value</span></span>

<span data-ttu-id="30925-135">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="30925-135">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="30925-136">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30925-136">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30925-137">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="30925-137">Return code</span></span></p></th>
<th><p><span data-ttu-id="30925-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="30925-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30925-139">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="30925-139">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="30925-140">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="30925-140">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30925-141">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="30925-141">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="30925-142">No se puede completar la operación porque hay una operación de copia de seguridad en curso en la instancia.</span><span class="sxs-lookup"><span data-stu-id="30925-142">The operation cannot complete because a backup operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30925-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="30925-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="30925-144">Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios parámetros produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="30925-144">One of the parameters that was provided contained an unexpected value, or the combination of several parameters yielded an unexpected result.</span></span> <span data-ttu-id="30925-145"><a href="gg269298(v=exchg.10).md">JetTerm</a> devolverá este error cuando el motor está en modo de varias instancias y cuando <em>pinstance</em> hace referencia a una instancia no válida.</span><span class="sxs-lookup"><span data-stu-id="30925-145">This error will be returned by <a href="gg269298(v=exchg.10).md">JetTerm</a> when the engine is in multi-instance mode and when <em>pinstance</em> refers to an invalid instance.</span></span></p>
<p><span data-ttu-id="30925-146"><strong>Windows XP:</strong>  Este valor devuelto se introduce en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="30925-146"><strong>Windows XP:</strong>  This return value is introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30925-147">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="30925-147">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="30925-148">No se puede completar la operación porque la instancia aún no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="30925-148">The operation cannot complete because the instance has not yet been initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30925-149">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="30925-149">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="30925-150">No se puede completar la operación porque la instancia se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="30925-150">The operation cannot complete because the instance is being shut down.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30925-151">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="30925-151">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="30925-152">No es posible completar la operación porque hay una operación de restauración en curso en la instancia.</span><span class="sxs-lookup"><span data-stu-id="30925-152">It is not possible to complete the operation because a restore operation is in progress on the instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30925-153">JET_errTooManyActiveUsers</span><span class="sxs-lookup"><span data-stu-id="30925-153">JET_errTooManyActiveUsers</span></span></p></td>
<td><p><span data-ttu-id="30925-154">No se puede cerrar la instancia porque actualmente hay sesiones con transacciones activas para la instancia especificada.</span><span class="sxs-lookup"><span data-stu-id="30925-154">The instance cannot be shut down because there are currently sessions with active transactions for the specified instance.</span></span> <span data-ttu-id="30925-155">Este error solo se produce si se usa el JET_bitTermComplete.</span><span class="sxs-lookup"><span data-stu-id="30925-155">This error occurs only if the JET_bitTermComplete is used.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="30925-156">Si esta función se ejecuta correctamente, se cerrará la instancia especificada.</span><span class="sxs-lookup"><span data-stu-id="30925-156">If this function succeeds, the specified instance will be shut down.</span></span> <span data-ttu-id="30925-157">El identificador de instancia también se cerrará y no estará disponible para ninguna API que tome un identificador de instancia.</span><span class="sxs-lookup"><span data-stu-id="30925-157">The instance handle will also be closed and made unavailable to any API that takes an instance handle.</span></span> <span data-ttu-id="30925-158">También se cerrarán todos los demás objetos asociados a la instancia de, como sesiones.</span><span class="sxs-lookup"><span data-stu-id="30925-158">All other objects that are associated with the instance, such as sessions, will also be closed.</span></span> <span data-ttu-id="30925-159">El estado del archivo de punto de comprobación, los archivos de registro de transacciones y los archivos de base de datos adjuntos a la instancia se modificarán durante el proceso de cierre.</span><span class="sxs-lookup"><span data-stu-id="30925-159">The state of the checkpoint file, transaction log files, and the database files attached to the instance will be modified during the shutdown process.</span></span>

<span data-ttu-id="30925-160">Si se produce un error en esta función como resultado de un error de uso, la instancia permanece en un estado inicializado y no cambia nada.</span><span class="sxs-lookup"><span data-stu-id="30925-160">If this function fails as a result of a usage error, then the instance remains in an initialized state and nothing changes.</span></span> <span data-ttu-id="30925-161">De lo contrario, la instancia se sigue cerrando según lo establecido en el caso de éxito.</span><span class="sxs-lookup"><span data-stu-id="30925-161">Otherwise, the instance is still shut down as stated for the success case.</span></span> <span data-ttu-id="30925-162">La diferencia es que la instancia de deberá pasar a través de la recuperación de bloqueos la próxima vez que se inicialice.</span><span class="sxs-lookup"><span data-stu-id="30925-162">The difference is that the instance will need to go through crash recovery when it is next initialized.</span></span> <span data-ttu-id="30925-163">El motor intentará vaciar tantos datos como sea posible para minimizar la cantidad de recuperación necesaria.</span><span class="sxs-lookup"><span data-stu-id="30925-163">The engine will try to flush as much data as possible to minimize the amount of recovery that is required.</span></span> <span data-ttu-id="30925-164">Conceptualmente, un error de [JetTerm](./jetterm-function.md) no es diferente de un bloqueo del proceso.</span><span class="sxs-lookup"><span data-stu-id="30925-164">Conceptually, such a failure of [JetTerm](./jetterm-function.md) is no different than a process crash.</span></span>

#### <a name="remarks"></a><span data-ttu-id="30925-165">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30925-165">Remarks</span></span>

<span data-ttu-id="30925-166">Vea [JetTerm](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="30925-166">See [JetTerm](./jetterm-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="30925-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30925-167">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30925-168"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="30925-168"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="30925-169">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="30925-169">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30925-170"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="30925-170"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="30925-171">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="30925-171">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30925-172"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="30925-172"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="30925-173">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="30925-173">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30925-174"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="30925-174"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="30925-175">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="30925-175">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30925-176"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="30925-176"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="30925-177">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="30925-177">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="30925-178">Consulte también</span><span class="sxs-lookup"><span data-stu-id="30925-178">See Also</span></span>

[<span data-ttu-id="30925-179">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="30925-179">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="30925-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="30925-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="30925-181">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="30925-181">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="30925-182">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="30925-182">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="30925-183">JetInit</span><span class="sxs-lookup"><span data-stu-id="30925-183">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="30925-184">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="30925-184">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="30925-185">JetTerm</span><span class="sxs-lookup"><span data-stu-id="30925-185">JetTerm</span></span>](./jetterm-function.md)
