---
description: 'Más información acerca de: JetOSSnapshotFreeze (función)'
title: Función JetOSSnapshotFreeze
TOCTitle: JetOSSnapshotFreeze Function
ms:assetid: 8dfbff20-199e-4d89-a33c-ae8e39b11ec1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269332(v=EXCHG.10)
ms:contentKeyID: 32765622
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotFreezeA
- JetOSSnapshotFreezeW
- JetOSSnapshotFreeze
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb6ea9a4a3145c0c4b3c3caeb3214b299ea1be85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278041"
---
# <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="17fce-103">Función JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="17fce-103">JetOSSnapshotFreeze Function</span></span>


<span data-ttu-id="17fce-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="17fce-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotfreeze-function"></a><span data-ttu-id="17fce-105">Función JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="17fce-105">JetOSSnapshotFreeze Function</span></span>

<span data-ttu-id="17fce-106">La función **JetOSSnapshotFreeze** inicia una instantánea.</span><span class="sxs-lookup"><span data-stu-id="17fce-106">The **JetOSSnapshotFreeze** function starts a snapshot.</span></span> <span data-ttu-id="17fce-107">Mientras la instantánea está en curso, no se puede llevar a cabo ninguna actividad de escritura en disco por parte del motor.</span><span class="sxs-lookup"><span data-stu-id="17fce-107">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="17fce-108">**Windows XP:**  **JetOSSnapshotFreeze** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="17fce-108">**Windows XP:**  **JetOSSnapshotFreeze** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotFreeze(
      __in          const JET_OSSNAPID snapId,
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="17fce-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17fce-109">Parameters</span></span>

<span data-ttu-id="17fce-110">*snapId*</span><span class="sxs-lookup"><span data-stu-id="17fce-110">*snapId*</span></span>

<span data-ttu-id="17fce-111">Identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="17fce-111">The identifier of the snapshot session.</span></span>

<span data-ttu-id="17fce-112">*pcInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="17fce-112">*pcInstanceInfo*</span></span>

<span data-ttu-id="17fce-113">El número de instancias que se están ejecutando actualmente en el motor que forman parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="17fce-113">The number of instances currently running in the engine that are part of the snapshot session.</span></span>

<span data-ttu-id="17fce-114">*paInstanceInfo*</span><span class="sxs-lookup"><span data-stu-id="17fce-114">*paInstanceInfo*</span></span>

<span data-ttu-id="17fce-115">Matriz de estructuras, una para cada instancia en ejecución que forma parte de la sesión de instantáneas, que describe la instancia y las bases de datos que forman parte de ella.</span><span class="sxs-lookup"><span data-stu-id="17fce-115">An array of structures, one for each running instance that is part of the snapshot session, describing the instance and the databases that are part of it.</span></span>

<span data-ttu-id="17fce-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="17fce-116">*grbit*</span></span>

<span data-ttu-id="17fce-117">Opciones de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="17fce-117">The options for this call.</span></span> <span data-ttu-id="17fce-118">Este parámetro está reservado para uso futuro y el único valor válido admitido es 0.</span><span class="sxs-lookup"><span data-stu-id="17fce-118">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="17fce-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17fce-119">Return Value</span></span>

<span data-ttu-id="17fce-120">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="17fce-120">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="17fce-121">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="17fce-121">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17fce-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="17fce-122">Return code</span></span></p></th>
<th><p><span data-ttu-id="17fce-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="17fce-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17fce-124">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="17fce-124">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="17fce-125">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="17fce-125">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fce-126">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="17fce-126">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="17fce-127">Los punteros proporcionados para los parámetros de salida son NULL, la sesión de instantáneas no es válida o el parámetro <em>grbit</em> no es válido.</span><span class="sxs-lookup"><span data-stu-id="17fce-127">The pointers provided for the output parameters are NULL, the snapshot session is invalid, or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fce-128">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="17fce-128">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="17fce-129">La sesión de instantáneas no está en el estado adecuado para iniciar una inmovilización (por ejemplo, una inmovilización anterior produjo un error en esta sesión antes).</span><span class="sxs-lookup"><span data-stu-id="17fce-129">The snapshot session is not in the appropriate state to start a freeze (for example, a previous freeze failed on this session before).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fce-130">JET_errOSSnapshotNotAllowed</span><span class="sxs-lookup"><span data-stu-id="17fce-130">JET_errOSSnapshotNotAllowed</span></span></p></td>
<td><p><span data-ttu-id="17fce-131">El motor no está en un estado en el que se pueda realizar una instantánea.</span><span class="sxs-lookup"><span data-stu-id="17fce-131">The engine is not in a state in which a snapshot can be performed.</span></span> <span data-ttu-id="17fce-132">Ya hay una o más copias de seguridad de streaming en curso, o una o varias instancias están pasando por pasos de recuperación o finalizando.</span><span class="sxs-lookup"><span data-stu-id="17fce-132">Either one or more streaming backups is already in progress, or one or more instances are going through recovery steps or terminating.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fce-133">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="17fce-133">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="17fce-134">El identificador de la sesión de instantáneas no es válido.</span><span class="sxs-lookup"><span data-stu-id="17fce-134">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fce-135">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="17fce-135">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="17fce-136">Error de la función debido a una condición de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="17fce-136">The function failed due to an out-of-memory condition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fce-137">JET_errOutOfThreads</span><span class="sxs-lookup"><span data-stu-id="17fce-137">JET_errOutOfThreads</span></span></p></td>
<td><p><span data-ttu-id="17fce-138">Error de la función porque no se pudo iniciar un nuevo subproceso que realiza la inmovilización.</span><span class="sxs-lookup"><span data-stu-id="17fce-138">The function failed because a new thread doing the freeze failed to start.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17fce-139">Si esta función se ejecuta correctamente, no habrá ningún IOs de escritura emitido para los archivos de base de datos o para los archivos de registro que forman parte de las instancias que están inmovilizadas.</span><span class="sxs-lookup"><span data-stu-id="17fce-139">If this function succeeds, there will not be any write IOs issued for the database files or for the log files that are part of instances that are frozen.</span></span> <span data-ttu-id="17fce-140">Además, la información de la instancia se rellena correctamente y se debe liberar más adelante llamando a [JetFreeBuffer](./jetfreebuffer-function.md) con el puntero a la matriz de información de instancia que se devolvió.</span><span class="sxs-lookup"><span data-stu-id="17fce-140">Also, the instance information will be properly filled and it must be freed later on by calling [JetFreeBuffer](./jetfreebuffer-function.md) with the pointer to the instance info array that was returned.</span></span>

<span data-ttu-id="17fce-141">Si se produce un error en esta función, el motor seguirá ejecutándose de forma habitual con la e/s que se produce como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="17fce-141">If this function fails, the engine will keep running normally with the IOs occurring as usual.</span></span> <span data-ttu-id="17fce-142">No es necesario llamar a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) si se produce un error en la inmovilización.</span><span class="sxs-lookup"><span data-stu-id="17fce-142">There is no need to call [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) if the freeze fails.</span></span> <span data-ttu-id="17fce-143">Además, la información de la instancia no se rellenará, por lo que no es necesario liberar este recurso.</span><span class="sxs-lookup"><span data-stu-id="17fce-143">Also, the instance information will not be filled so there is no need to free this resource.</span></span>

#### <a name="remarks"></a><span data-ttu-id="17fce-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17fce-144">Remarks</span></span>

<span data-ttu-id="17fce-145">Durante el período de inmovilización, no habrá ninguna e/s de escritura emitida a las bases de datos adjuntas ni a los registros de transacciones, aunque es posible que se emitan e/s de escritura para las bases de datos temporales o los archivos de streaming.</span><span class="sxs-lookup"><span data-stu-id="17fce-145">During the freeze period, there will not be any write IOs issued to the attached databases or the transaction logs, although there might be write IOs issued to the temporary databases or streaming files.</span></span>

<span data-ttu-id="17fce-146">El estado en el que las bases de datos y los archivos de registro estarán durante la inmovilización (el estado en el que los archivos se encontrarían en una imagen de instantánea de volumen) serán de tal modo que se pueda realizar una recuperación normal si esos archivos se restauran más adelante.</span><span class="sxs-lookup"><span data-stu-id="17fce-146">The state in which the databases and the log files will be during the freeze (the state in which the files would be in a Volume Snapshot image) will be such that a normal recovery will be possible if those files are restored later.</span></span>

<span data-ttu-id="17fce-147">Dado que no hay operaciones de escritura durante el período de inmovilización, es posible que las llamadas de API normales en el motor se detengan durante ese intervalo.</span><span class="sxs-lookup"><span data-stu-id="17fce-147">Because there are no write operations during the freeze period, normal API calls into the engine might be stalled for that interval.</span></span> <span data-ttu-id="17fce-148">La aplicación cliente debe ser capaz de controlar las llamadas API que podrían tardar más tiempo si se produce una inmovilización.</span><span class="sxs-lookup"><span data-stu-id="17fce-148">The client application must be able to handle API calls that might take longer then normal if a freeze occurs.</span></span>

<span data-ttu-id="17fce-149">Debido a los posibles efectos descritos anteriormente, hay un tiempo de espera interno después del cual la sesión de instantáneas detendrá la fase de inmovilización aunque no se llame a las API que realizan la reanudación o anulación.</span><span class="sxs-lookup"><span data-stu-id="17fce-149">Due to the possible effects described above, there is an internal timeout after which the snapshot session will stop the freeze phase even if the APIs doing the thaw or abort were not called.</span></span> <span data-ttu-id="17fce-150">El valor del tiempo de espera se puede cambiar mediante el parámetro del sistema [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="17fce-150">The value of the timeout can be changed using the [JET_paramOSSnapshotTimeout](./backup-and-restore-parameters.md) system parameter.</span></span> <span data-ttu-id="17fce-151">Tenga en cuenta que el intervalo de inmovilización típico está en el intervalo de 10 segundos con el tiempo de espera predeterminado en unos 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="17fce-151">Note that the typical freeze interval is in the range of 10 seconds with the default timeout somewhere around 60 seconds.</span></span>

#### <a name="requirements"></a><span data-ttu-id="17fce-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17fce-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17fce-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="17fce-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="17fce-154">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="17fce-154">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fce-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="17fce-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="17fce-156">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="17fce-156">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fce-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="17fce-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="17fce-158">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="17fce-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fce-159"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="17fce-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="17fce-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="17fce-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fce-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="17fce-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="17fce-162">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="17fce-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fce-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="17fce-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="17fce-164">Se implementa como <strong>JetOSSnapshotFreezeW</strong> (Unicode) y <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="17fce-164">Implemented as <strong>JetOSSnapshotFreezeW</strong> (Unicode) and <strong>JetOSSnapshotFreezeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="17fce-165">Consulte también</span><span class="sxs-lookup"><span data-stu-id="17fce-165">See Also</span></span>

[<span data-ttu-id="17fce-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="17fce-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="17fce-167">JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="17fce-167">JET_INSTANCE_INFO</span></span>](./jet-instance-info-structure.md)  
[<span data-ttu-id="17fce-168">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="17fce-168">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="17fce-169">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="17fce-169">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="17fce-170">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="17fce-170">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="17fce-171">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="17fce-171">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="17fce-172">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="17fce-172">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
