---
description: 'Más información acerca de: JetInit2 (función)'
title: Función JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00cc3402567a7c1342e78d3c84a1d6cfca8ab4d8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104004002"
---
# <a name="jetinit2-function"></a><span data-ttu-id="0bf71-103">Función JetInit2</span><span class="sxs-lookup"><span data-stu-id="0bf71-103">JetInit2 Function</span></span>


<span data-ttu-id="0bf71-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0bf71-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetinit2-function"></a><span data-ttu-id="0bf71-105">Función JetInit2</span><span class="sxs-lookup"><span data-stu-id="0bf71-105">JetInit2 Function</span></span>

<span data-ttu-id="0bf71-106">La función **JetInit2** coloca el motor de base de datos en un estado en el que pueda admitir el uso de aplicaciones de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="0bf71-106">The **JetInit2** function puts the database engine into a state where it can support application use of database files.</span></span> <span data-ttu-id="0bf71-107">El motor ya debe estar configurado correctamente para la inicialización mediante [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0bf71-107">The engine must already be properly configured for initialization using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="0bf71-108">La recuperación tras bloqueo de la base de datos se realiza automáticamente como parte del proceso de inicialización.</span><span class="sxs-lookup"><span data-stu-id="0bf71-108">Database crash recovery is performed automatically as a part of the initialization process.</span></span>

<span data-ttu-id="0bf71-109">**Windows XP:**  **JetInit2** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0bf71-109">**Windows XP:**  **JetInit2** is introduced in Windows XP.</span></span>

<span data-ttu-id="0bf71-110">Esta función está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="0bf71-110">This function is obsolete.</span></span> <span data-ttu-id="0bf71-111">Use [JetInit3](./jetinit3-function.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="0bf71-111">Use [JetInit3](./jetinit3-function.md) instead.</span></span>

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="0bf71-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0bf71-112">Parameters</span></span>

<span data-ttu-id="0bf71-113">*pinstance*</span><span class="sxs-lookup"><span data-stu-id="0bf71-113">*pinstance*</span></span>

<span data-ttu-id="0bf71-114">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="0bf71-114">The instance to use for this call.</span></span>

<span data-ttu-id="0bf71-115">En Windows 2000, este parámetro se omite y siempre debe ser NULL.</span><span class="sxs-lookup"><span data-stu-id="0bf71-115">For Windows 2000, this parameter is ignored and should always be NULL.</span></span>

<span data-ttu-id="0bf71-116">En Windows XP y versiones posteriores, el uso de este parámetro depende del modo de funcionamiento del motor.</span><span class="sxs-lookup"><span data-stu-id="0bf71-116">For Windows XP and later releases, the use of this parameter depends on the operating mode of the engine.</span></span> <span data-ttu-id="0bf71-117">Si el motor está funcionando en modo heredado (modo de compatibilidad de Windows 2000) donde solo se admite una instancia, este parámetro puede ser NULL o se puede establecer en un búfer de salida válido que contenga NULL o JET_instanceNil que devuelva el identificador de instancia global creado como un efecto secundario de la inicialización.</span><span class="sxs-lookup"><span data-stu-id="0bf71-117">If the engine is operating in legacy mode (Windows 2000 compatibility mode) where only one instance is supported, this parameter may either be NULL or it may be set to a valid output buffer containing NULL or JET_instanceNil which returns the global instance handle created as a side effect of the initialization.</span></span> <span data-ttu-id="0bf71-118">Este identificador de instancia se puede pasar a cualquier otra API que toma una instancia.</span><span class="sxs-lookup"><span data-stu-id="0bf71-118">This instance handle can then be passed to any other API that takes an instance.</span></span> <span data-ttu-id="0bf71-119">Si el motor está funcionando en modo de varias instancias, este parámetro debe establecerse en un búfer de entrada válido que contenga el identificador de instancia devuelto por el [JetCreateInstance](./jetcreateinstance-function.md) que se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="0bf71-119">If the engine is operating in multi-instance mode, this parameter must be set to a valid input buffer that contains the instance handle returned by the [JetCreateInstance](./jetcreateinstance-function.md) that is being initialized.</span></span>

<span data-ttu-id="0bf71-120">*grbit*</span><span class="sxs-lookup"><span data-stu-id="0bf71-120">*grbit*</span></span>

<span data-ttu-id="0bf71-121">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="0bf71-121">A group of bits specifying zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bf71-122">Value</span><span class="sxs-lookup"><span data-stu-id="0bf71-122">Value</span></span></p></th>
<th><p><span data-ttu-id="0bf71-123">Significado</span><span class="sxs-lookup"><span data-stu-id="0bf71-123">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bf71-124">JET_bitReplayReplicatedLogFiles</span><span class="sxs-lookup"><span data-stu-id="0bf71-124">JET_bitReplayReplicatedLogFiles</span></span></p></td>
<td><p><span data-ttu-id="0bf71-125">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0bf71-125">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bf71-126">JET_bitCreateSFSVolumeIfNotExist</span><span class="sxs-lookup"><span data-stu-id="0bf71-126">JET_bitCreateSFSVolumeIfNotExist</span></span></p></td>
<td><p><span data-ttu-id="0bf71-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0bf71-127">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bf71-128">JET_bitReplayIgnoreMissingDB</span><span class="sxs-lookup"><span data-stu-id="0bf71-128">JET_bitReplayIgnoreMissingDB</span></span></p></td>
<td><p><span data-ttu-id="0bf71-129">Esta opción permite al usuario ejecutar la recuperación en un conjunto de archivos de registro, sin que estén presentes todas las bases de datos, que se adjuntaron en un punto del conjunto de registros.</span><span class="sxs-lookup"><span data-stu-id="0bf71-129">This option allows the user to run recovery on a set of log files, without all of the databases being present, that were attached at one point of the log set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bf71-130">JET_bitRecoveryWithoutUndo</span><span class="sxs-lookup"><span data-stu-id="0bf71-130">JET_bitRecoveryWithoutUndo</span></span></p></td>
<td><p><span data-ttu-id="0bf71-131">Realiza la recuperación, pero se detiene en la fase de deshacer.</span><span class="sxs-lookup"><span data-stu-id="0bf71-131">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="0bf71-132">Esto permite que se copien y se apliquen registros de transacciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="0bf71-132">This allows additional transaction logs to copied in and applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bf71-133">JET_bitTruncateLogsAfterRecovery</span><span class="sxs-lookup"><span data-stu-id="0bf71-133">JET_bitTruncateLogsAfterRecovery</span></span></p></td>
<td><p><span data-ttu-id="0bf71-134">En la recuperación de software correcta, trunque los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="0bf71-134">On successful soft recovery, truncate log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bf71-135">JET_bitReplayMissingMapEntryDB</span><span class="sxs-lookup"><span data-stu-id="0bf71-135">JET_bitReplayMissingMapEntryDB</span></span></p></td>
<td><p><span data-ttu-id="0bf71-136">Falta la entrada de asignación de base de datos predeterminada en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="0bf71-136">Missing database map entry default to same location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bf71-137">JET_bitReplayIgnoreLostLogs</span><span class="sxs-lookup"><span data-stu-id="0bf71-137">JET_bitReplayIgnoreLostLogs</span></span></p></td>
<td><p><span data-ttu-id="0bf71-138">Omitir los registros perdidos desde el final de la secuencia de registro.</span><span class="sxs-lookup"><span data-stu-id="0bf71-138">Ignore logs lost from the end of the log stream.</span></span></p>
<p><span data-ttu-id="0bf71-139"><strong>Windows 7: JET_bitReplayIgnoreLostLogs</strong> se introduce en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0bf71-139"><strong>Windows 7:JET_bitReplayIgnoreLostLogs</strong> is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0bf71-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0bf71-140">Return Value</span></span>

<span data-ttu-id="0bf71-141">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="0bf71-141">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="0bf71-142">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0bf71-142">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>


#### <a name="remarks"></a><span data-ttu-id="0bf71-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bf71-143">Remarks</span></span>

<span data-ttu-id="0bf71-144">Una instancia de se debe inicializar con una llamada a **JetInit2** para que pueda ser utilizada por cualquier cosa que no sea [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="0bf71-144">An instance must be initialized with a call to **JetInit2** before it can be used by anything other than [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="0bf71-145">Una instancia de se destruye mediante una llamada a la función [JetTerm](./jetterm-function.md) , incluso si esa instancia nunca se inicializó con [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="0bf71-145">An instance is destroyed by a call to the [JetTerm](./jetterm-function.md) function, even if that instance was never initialized using [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="0bf71-146">Una instancia es la unidad de capacidad de recuperación del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="0bf71-146">An instance is the unit of recoverability for the database engine.</span></span> <span data-ttu-id="0bf71-147">Controla el ciclo de vida de todos los archivos utilizados para proteger la integridad de los datos en un conjunto de archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="0bf71-147">It controls the life cycle of all the files used to protect the integrity of the data in a set of database files.</span></span> <span data-ttu-id="0bf71-148">Estos archivos incluyen el archivo de punto de comprobación y los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="0bf71-148">These files include the checkpoint file and the transaction log files.</span></span>

<span data-ttu-id="0bf71-149">Si la recuperación se está ejecutando en un conjunto de registros, para el que no todas las bases de datos están presentes (lo que devolverá el error JET_errAttachedDatabaseMismatch en circunstancias normales) y el cliente desea que la recuperación continúe a pesar de las bases de datos que faltan, el JET_ bitReplayIgnoreMissingDB se usa para continuar la recuperación de las bases de datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="0bf71-149">If recovery is running on a set of logs, for which not all databases is present (which will return the error JET_errAttachedDatabaseMismatch under normal circumstances), and the client wishes recovery to continue despite missing databases, the JET_ bitReplayIgnoreMissingDB is used to continue recovery for the available databases.</span></span>

<span data-ttu-id="0bf71-150">Vea la sección Comentarios en [JetInit](./jetinit-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0bf71-150">See the Remarks section in [JetInit](./jetinit-function.md) for more information.</span></span>

#### <a name="requirements"></a><span data-ttu-id="0bf71-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bf71-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bf71-152"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="0bf71-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0bf71-153">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0bf71-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bf71-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0bf71-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0bf71-155">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0bf71-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bf71-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0bf71-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0bf71-157">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="0bf71-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bf71-158"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="0bf71-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="0bf71-159">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="0bf71-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bf71-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="0bf71-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="0bf71-161">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="0bf71-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="0bf71-162">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0bf71-162">See Also</span></span>

[<span data-ttu-id="0bf71-163">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="0bf71-163">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="0bf71-164">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="0bf71-164">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="0bf71-165">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="0bf71-165">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="0bf71-166">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0bf71-166">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="0bf71-167">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="0bf71-167">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="0bf71-168">JetInit</span><span class="sxs-lookup"><span data-stu-id="0bf71-168">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="0bf71-169">JetInit3</span><span class="sxs-lookup"><span data-stu-id="0bf71-169">JetInit3</span></span>](./jetinit3-function.md)  
[<span data-ttu-id="0bf71-170">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="0bf71-170">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="0bf71-171">Parámetros de recursos</span><span class="sxs-lookup"><span data-stu-id="0bf71-171">Resource Parameters</span></span>](./resource-parameters.md)
