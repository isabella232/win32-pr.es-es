---
description: 'Más información acerca de: JetInit3 (función)'
title: Función JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361683"
---
# <a name="jetinit3-function"></a><span data-ttu-id="52db1-103">Función JetInit3</span><span class="sxs-lookup"><span data-stu-id="52db1-103">JetInit3 Function</span></span>


<span data-ttu-id="52db1-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="52db1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit3-function"></a><span data-ttu-id="52db1-105">Función JetInit3</span><span class="sxs-lookup"><span data-stu-id="52db1-105">JetInit3 Function</span></span>

<span data-ttu-id="52db1-106">La función **JetInit3** coloca el motor de base de datos en un estado en el que puede admitir el uso de aplicaciones de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="52db1-106">The **JetInit3** function puts the database engine into a state in which it can support application use of database files.</span></span> <span data-ttu-id="52db1-107">El motor ya debe estar configurado correctamente para la inicialización, lo que se realiza mediante la función [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="52db1-107">The engine must already be properly configured for initialization, which you accomplish by using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span> <span data-ttu-id="52db1-108">Tenga en cuenta que la recuperación tras bloqueo de la base de datos se produce automáticamente como parte del proceso de inicialización.</span><span class="sxs-lookup"><span data-stu-id="52db1-108">Note that database crash recovery occurs automatically as a part of the initialization process.</span></span>

<span data-ttu-id="52db1-109">**Windows Vista:**  **JetInit3** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52db1-109">**Windows Vista:**  **JetInit3** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="52db1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52db1-110">Parameters</span></span>

<span data-ttu-id="52db1-111">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="52db1-111">*pinstance*</span></span>

<span data-ttu-id="52db1-112">La instancia de que se usa para una llamada determinada.</span><span class="sxs-lookup"><span data-stu-id="52db1-112">The instance that you use for a particular call.</span></span> <span data-ttu-id="52db1-113">El uso de este parámetro depende del modo de funcionamiento del motor.</span><span class="sxs-lookup"><span data-stu-id="52db1-113">The use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="52db1-114">Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000), en el que solo se admite una instancia, puede establecer este parámetro en **null** o en un búfer de salida válido que contenga **null** o JET_instanceNil, que devuelve el identificador de instancia global creado como efecto secundario de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="52db1-114">If the engine is operating in legacy mode (Windows 2000 compatibility mode), in which only one instance is supported, you can set this parameter either to **NULL** or to a valid output buffer containing either **NULL** or JET_instanceNil, which returns the global instance handle created as a side-effect of the initialization.</span></span> <span data-ttu-id="52db1-115">Este identificador de instancia se puede pasar a cualquier otra API que toma una instancia.</span><span class="sxs-lookup"><span data-stu-id="52db1-115">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="52db1-116">Si el motor está funcionando en modo de varias instancias, debe establecer este parámetro en un búfer de entrada válido que contenga el identificador de instancia devuelto por la función [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="52db1-116">If the engine is operating in multi-instance mode, you must set this parameter to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) function that is being initialized.</span></span>

<span data-ttu-id="52db1-117">*prstInfo*</span><span class="sxs-lookup"><span data-stu-id="52db1-117">*prstInfo*</span></span>

<span data-ttu-id="52db1-118">Parámetros de recuperación adicionales que se usan para reasignar las bases de datos durante la recuperación, para establecer la posición en la que se detendrá la recuperación o para determinar el estado de recuperación actual.</span><span class="sxs-lookup"><span data-stu-id="52db1-118">Additional recovery parameters used for remapping databases during recovery, for setting the position where recovery will stop, or for determining the current recovery status.</span></span>

<span data-ttu-id="52db1-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="52db1-119">*grbit*</span></span>

<span data-ttu-id="52db1-120">Grupo de bits que especifica cero o más de las opciones enumeradas y definidas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="52db1-120">A group of bits that specifies zero or more of the options listed and defined in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52db1-121">Value</span><span class="sxs-lookup"><span data-stu-id="52db1-121">Value</span></span></p></th>
<th><p><span data-ttu-id="52db1-122">Significado</span><span class="sxs-lookup"><span data-stu-id="52db1-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52db1-123">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="52db1-123">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="52db1-124">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="52db1-124">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52db1-125">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="52db1-125">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="52db1-126">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="52db1-126">This value is reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52db1-127">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="52db1-127">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="52db1-128">Este valor permite al usuario ejecutar la recuperación en un conjunto de archivos de registro, incluso en ausencia de las bases de datos que se adjuntaron al archivo de registro establecido en algún momento.</span><span class="sxs-lookup"><span data-stu-id="52db1-128">This value enables the user to run recovery on a set of log files, even in the absence of the databases that were attached to the log file set at some point.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52db1-129">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="52db1-129">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="52db1-130">Este valor permite al usuario realizar la recuperación, pero solo hasta (y sin incluir) la fase de deshacer.</span><span class="sxs-lookup"><span data-stu-id="52db1-130">This value enables the user to perform recovery, but only up to (and not including) the Undo phase.</span></span> <span data-ttu-id="52db1-131">Con este valor, se pueden copiar y aplicar registros de transacciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="52db1-131">Using this value, additional transaction logs can be copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52db1-132">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="52db1-132">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="52db1-133">Este valor hace que se trunquen los archivos de registro durante una recuperación de software correcta.</span><span class="sxs-lookup"><span data-stu-id="52db1-133">This value causes log files to be truncated during a successful soft recovery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52db1-134">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="52db1-134">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="52db1-135">Este valor hace que la entrada de asignación de base de datos que falta se encuentre en la misma ubicación de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="52db1-135">This value causes a missing database map entry to default to the same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52db1-136">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="52db1-136">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="52db1-137">Este valor hace que se omitan los registros perdidos desde el final de la secuencia de registro durante una recuperación.</span><span class="sxs-lookup"><span data-stu-id="52db1-137">This value causes logs lost from the end of the log stream to be ignored during a recovery.</span></span></p>
<p><span data-ttu-id="52db1-138"><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> se introduce en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52db1-138"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="52db1-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52db1-139">Return Value</span></span>

<span data-ttu-id="52db1-140">Esta función devuelve el tipo de datos [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="52db1-140">This function returns the [JET_ERR](./jet-err.md) data type with one of the following return codes.</span></span> <span data-ttu-id="52db1-141">Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="52db1-141">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="52db1-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52db1-142">Remarks</span></span>

<span data-ttu-id="52db1-143">Una instancia de se debe inicializar con una llamada a la función **JetInit3** antes de que pueda ser utilizada por cualquier cosa que no sea la función [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="52db1-143">An instance must be initialized with a call to the **JetInit3** function before it can be used by anything other than the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function.</span></span>

<span data-ttu-id="52db1-144">Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó mediante la función [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="52db1-144">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized by using the [JetInit](./jetinit-function.md) function.</span></span> <span data-ttu-id="52db1-145">Una instancia es la unidad de capacidad de recuperación del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="52db1-145">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="52db1-146">Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="52db1-146">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="52db1-147">Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="52db1-147">These files include the checkpoint file and the transaction log files.</span></span> <span data-ttu-id="52db1-148">Tenga en cuenta que no se debe llamar a [JetTerm](./jetterm-function.md) si se produce un error en la función **JetInit3** .</span><span class="sxs-lookup"><span data-stu-id="52db1-148">Note that [JetTerm](./jetterm-function.md) should not be called if the **JetInit3** function fails.</span></span> <span data-ttu-id="52db1-149">Sin embargo, todavía se debe llamar a [JetTerm](./jetterm-function.md) para todas las instancias creadas por **JetCreateInstance2** si nunca se llamó a **JetInit3** o si **JetInit3** se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="52db1-149">However, [JetTerm](./jetterm-function.md) should still be called for all instances created by **JetCreateInstance2** if **JetInit3** was never called or if **JetInit3** succeeds.</span></span>

<span data-ttu-id="52db1-150">Si la recuperación se está ejecutando en un conjunto de registros para el que no están presentes todas las bases de datos relacionadas (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, se usa el error de JET_bitReplayIgnoreMissingDB para continuar la recuperación de las bases de datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="52db1-150">If recovery is running on a set of logs for which not all of the related databases are present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wants recovery to continue despite the missing databases, the JET_bitReplayIgnoreMissingDB error is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="52db1-151">Dado que la recuperación tras bloqueo no suele producirse en el mismo equipo (y con la misma configuración) que en el momento del bloqueo, una base de datos no suele cambiar la ubicación.</span><span class="sxs-lookup"><span data-stu-id="52db1-151">Because crash recovery doesn't usually happen on the same machine (and with the same configuration) as at the time of the crash, a database typically doesn't change location.</span></span> <span data-ttu-id="52db1-152">En algunos escenarios, como el traslado de archivos a una máquina diferente o la restauración de la copia de seguridad de instantáneas en ubicaciones diferentes, esto ya no es así.</span><span class="sxs-lookup"><span data-stu-id="52db1-152">In certain scenarios, such as moving files to a different machine or restoring snapshot backup to different locations, this is no longer true.</span></span> <span data-ttu-id="52db1-153">La función **JetInit3** permite especificar una asignación (mediante las estructuras [JET_RSTINFO](./jet-rstinfo-structure.md) y [JET_RSTMAP](./jet-rstmap-structure.md) ) entre la antigua ubicación de la base de datos y su nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="52db1-153">The **JetInit3** function enables you to specify a mapping (using the [JET_RSTINFO](./jet-rstinfo-structure.md) and [JET_RSTMAP](./jet-rstmap-structure.md) structures) between the old database location and its new location.</span></span> <span data-ttu-id="52db1-154">De hecho, solo necesita la nueva ubicación, siempre y cuando los archivos de base de datos estén presentes en esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="52db1-154">In fact, you need only the new location as long as the database files are present at that location.</span></span> <span data-ttu-id="52db1-155">En cuanto Conozca las ubicaciones de las bases de datos restauradas, la firma de la base de datos se utilizará para identificar la base de datos a través del proceso de restauración.</span><span class="sxs-lookup"><span data-stu-id="52db1-155">As soon as you know the locations of the restored databases, the database signature will be used to identify the database through the restore process.</span></span> <span data-ttu-id="52db1-156">Solo necesitará la ubicación de la base de datos original si necesita volver a crear una base de datos, en cuyo caso se conoce la firma.</span><span class="sxs-lookup"><span data-stu-id="52db1-156">You'll need the original database location only if you need to re-create a database, in which case the signature is known.</span></span>

<span data-ttu-id="52db1-157">Además, si necesita detener una recuperación después de una operación de deshacer, puede especificar una posición de registro determinada en la que se detendrá la recuperación.</span><span class="sxs-lookup"><span data-stu-id="52db1-157">In addition, if you need to stop a recovery after an Undo operation, you can specify a particular log position at which recovery will stop.</span></span> <span data-ttu-id="52db1-158">Tenga en cuenta que esto incluye la capacidad de detenerse al final de una generación de registro determinada si la posición especificada forma parte de la generación pero supera el final del registro real.</span><span class="sxs-lookup"><span data-stu-id="52db1-158">Note that this includes the ability to stop at the end of a particular log generation if the specified position is part of the generation but past the end of the actual log.</span></span>

<span data-ttu-id="52db1-159">Para obtener más información, vea la sección "Comentarios" en el tema [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="52db1-159">For more information, see the "Remarks" section in the [JetInit](./jetinit-function.md) topic.</span></span>

#### <a name="requirements"></a><span data-ttu-id="52db1-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52db1-160">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52db1-161">Remoto</span><span class="sxs-lookup"><span data-stu-id="52db1-161">Client</span></span></p></td>
<td><p><span data-ttu-id="52db1-162">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52db1-162">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52db1-163">Servidor</span><span class="sxs-lookup"><span data-stu-id="52db1-163">Server</span></span></p></td>
<td><p><span data-ttu-id="52db1-164">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="52db1-164">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52db1-165">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52db1-165">Header</span></span></p></td>
<td><p><span data-ttu-id="52db1-166">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="52db1-166">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52db1-167">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52db1-167">Library</span></span></p></td>
<td><p><span data-ttu-id="52db1-168">Utiliza ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="52db1-168">Uses ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52db1-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52db1-169">DLL</span></span></p></td>
<td><p><span data-ttu-id="52db1-170">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="52db1-170">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52db1-171">Unicode</span><span class="sxs-lookup"><span data-stu-id="52db1-171">Unicode</span></span></p></td>
<td><p><span data-ttu-id="52db1-172">Se implementa como <strong>JetInit3W</strong> (Unicode) y <strong>JetInit3A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="52db1-172">Implemented as <strong>JetInit3W</strong> (Unicode) and <strong>JetInit3A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="52db1-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="52db1-173">See Also</span></span>

[<span data-ttu-id="52db1-174">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="52db1-174">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="52db1-175">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="52db1-175">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="52db1-176">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="52db1-176">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="52db1-177">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="52db1-177">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="52db1-178">JET_RSTINFO</span><span class="sxs-lookup"><span data-stu-id="52db1-178">JET_RSTINFO</span></span>](./jet-rstinfo-structure.md)  
[<span data-ttu-id="52db1-179">JET_RSTMAP</span><span class="sxs-lookup"><span data-stu-id="52db1-179">JET_RSTMAP</span></span>](./jet-rstmap-structure.md)  
[<span data-ttu-id="52db1-180">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="52db1-180">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="52db1-181">JetInit</span><span class="sxs-lookup"><span data-stu-id="52db1-181">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="52db1-182">JetInit2</span><span class="sxs-lookup"><span data-stu-id="52db1-182">JetInit2</span></span>](./jetinit2-function.md)  
[<span data-ttu-id="52db1-183">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="52db1-183">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="52db1-184">Parámetros de recursos</span><span class="sxs-lookup"><span data-stu-id="52db1-184">Resource Parameters</span></span>](./resource-parameters.md)
