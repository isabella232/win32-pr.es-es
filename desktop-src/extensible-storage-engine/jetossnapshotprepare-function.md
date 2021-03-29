---
description: 'Más información acerca de: JetOSSnapshotPrepare (función)'
title: Función JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ccf9a5b21ccb9a4f94ba5aa4f995e4bb9017bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648535"
---
# <a name="jetossnapshotprepare-function"></a><span data-ttu-id="2cdc8-103">Función JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="2cdc8-103">JetOSSnapshotPrepare Function</span></span>


<span data-ttu-id="2cdc8-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2cdc8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepare-function"></a><span data-ttu-id="2cdc8-105">Función JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="2cdc8-105">JetOSSnapshotPrepare Function</span></span>

<span data-ttu-id="2cdc8-106">La función **JetOSSnapshotPrepare** inicia los preparativos para una sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-106">The **JetOSSnapshotPrepare** function begins the preparations for a snapshot session.</span></span> <span data-ttu-id="2cdc8-107">Una sesión de instantáneas es un breve intervalo de tiempo en el que el motor no emite ninguna e/s de escritura en el disco, de modo que el motor puede participar en una sesión de instantáneas de volumen (cuando está controlada por un escritor de instantáneas).</span><span class="sxs-lookup"><span data-stu-id="2cdc8-107">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="2cdc8-108">**Windows XP:**  **JetOSSnapshotPrepare** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-108">**Windows XP:**  **JetOSSnapshotPrepare** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="2cdc8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cdc8-109">Parameters</span></span>

<span data-ttu-id="2cdc8-110">*psnapId*</span><span class="sxs-lookup"><span data-stu-id="2cdc8-110">*psnapId*</span></span>

<span data-ttu-id="2cdc8-111">Identificador de la sesión de instantáneas que se va a iniciar.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-111">The identifier of the snapshot session to be started.</span></span>

<span data-ttu-id="2cdc8-112">*grbit*</span><span class="sxs-lookup"><span data-stu-id="2cdc8-112">*grbit*</span></span>

<span data-ttu-id="2cdc8-113">Opciones de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-113">The options for this call.</span></span> <span data-ttu-id="2cdc8-114">Este parámetro puede tener una combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-114">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cdc8-115">Value</span><span class="sxs-lookup"><span data-stu-id="2cdc8-115">Value</span></span></p></th>
<th><p><span data-ttu-id="2cdc8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="2cdc8-116">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cdc8-117">0</span><span class="sxs-lookup"><span data-stu-id="2cdc8-117">0</span></span></p></td>
<td><p><span data-ttu-id="2cdc8-118">Instantánea normal.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-118">Normal snapshot.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cdc8-119">JET_bitIncrementalSnapshot</span><span class="sxs-lookup"><span data-stu-id="2cdc8-119">JET_bitIncrementalSnapshot</span></span></p></td>
<td><p><span data-ttu-id="2cdc8-120">Solo se tomarán los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-120">Only log files will be taken.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cdc8-121">JET_bitCopySnapshot</span><span class="sxs-lookup"><span data-stu-id="2cdc8-121">JET_bitCopySnapshot</span></span></p></td>
<td><p><span data-ttu-id="2cdc8-122">Una instantánea de copia (normal o incremental) sin truncamiento del registro.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-122">A copy snapshot (normal or incremental) with no log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cdc8-123">JET_bitContinueAfterThaw</span><span class="sxs-lookup"><span data-stu-id="2cdc8-123">JET_bitContinueAfterThaw</span></span></p></td>
<td><p><span data-ttu-id="2cdc8-124">La sesión de instantáneas se produce después de <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> y requerirá una llamada a la función <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> .</span><span class="sxs-lookup"><span data-stu-id="2cdc8-124">The snapshot session occurs after <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> and will require a <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> function call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cdc8-125">JET_bitExplicitPrepare</span><span class="sxs-lookup"><span data-stu-id="2cdc8-125">JET_bitExplicitPrepare</span></span></p></td>
<td><p><span data-ttu-id="2cdc8-126">No se preparará ninguna instancia de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-126">No instances will be prepared by default.</span></span></p>
<p><span data-ttu-id="2cdc8-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare se presenta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-127"><strong>Windows 7:</strong>  JET_bitExplicitPrepare is introduced in Windows 7.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="2cdc8-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cdc8-128">Return Value</span></span>

<span data-ttu-id="2cdc8-129">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2cdc8-130">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2cdc8-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2cdc8-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2cdc8-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="2cdc8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cdc8-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cdc8-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2cdc8-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2cdc8-134">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cdc8-135">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2cdc8-135">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2cdc8-136">El puntero de identificador de instantánea es NULL o el parámetro <em>grbit</em> no es válido.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-136">The snapshot ID pointer is NULL or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cdc8-137">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="2cdc8-137">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="2cdc8-138">Ya hay una sesión de instantánea en curso y la operación no puede tener más de una sesión de instantáneas en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-138">A snapshot session is already in progress and the operation is not allowed to have more then one snapshot session at any given time.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2cdc8-139">Si esta función se ejecuta correctamente, una sesión de instantáneas podrá iniciarse en cualquier momento con la fase de inmovilización de e/s.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-139">If this function succeeds, a snapshot session will be able to start at any time with the IO freeze phase.</span></span> <span data-ttu-id="2cdc8-140">Se devolverá el identificador de la sesión y se debe usar en las llamadas subsiguientes para la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-140">The identifier for the session will be returned and must be used in the subsequent calls for the snapshot session.</span></span>

<span data-ttu-id="2cdc8-141">Las instancias en ejecución del motor se considerarán parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-141">The running instances of the engine will now be considered part of the snapshot session.</span></span>

<span data-ttu-id="2cdc8-142">**Windows Vista:**  Para especificar un subconjunto diferente de instancias, se puede llamar a [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) .</span><span class="sxs-lookup"><span data-stu-id="2cdc8-142">**Windows Vista:**  To specify a different subset of instances, the [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) can be called.</span></span>

<span data-ttu-id="2cdc8-143">La llamada de secuencia de API normal es: **JetOSSnapshotPrepare**, seguido, opcionalmente, de una o varias llamadas a [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)y, después, por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="2cdc8-143">The normal API sequence call is: **JetOSSnapshotPrepare**, optionally followed by one or more calls to [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="2cdc8-144">Una vez que se inicia la inmovilización, puede terminarse mediante [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="2cdc8-144">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="2cdc8-145">En cualquier momento después de la preparación, la sesión de instantáneas puede terminar repentinamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="2cdc8-145">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span>

<span data-ttu-id="2cdc8-146">Si se especifica JET_bitContinueAfterThaw después de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), se conservará la sesión de instantáneas (aunque se reanudará la e/s).</span><span class="sxs-lookup"><span data-stu-id="2cdc8-146">If JET_bitContinueAfterThaw is specified after [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), the snapshot session will remain (although the I/O will resume).</span></span> <span data-ttu-id="2cdc8-147">Esto habilitará una comprobación de la instantánea y, si es necesario, habilitará el truncamiento del registro mediante [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) y requerirá una llamada a [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span><span class="sxs-lookup"><span data-stu-id="2cdc8-147">This will enable a verification of the snapshot, and if needed, will enable log truncation using [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) and will require a call to [JetOSSnapshotEnd](./jetossnapshotend-function.md).</span></span>

<span data-ttu-id="2cdc8-148">Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-148">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2cdc8-149">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cdc8-149">Remarks</span></span>

<span data-ttu-id="2cdc8-150">Se generarán entradas del registro de eventos para los distintos pasos de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-150">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2cdc8-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cdc8-151">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2cdc8-152"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2cdc8-152"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2cdc8-153">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-153">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cdc8-154"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2cdc8-154"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2cdc8-155">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-155">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cdc8-156"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2cdc8-156"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2cdc8-157">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-157">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2cdc8-158"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="2cdc8-158"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2cdc8-159">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-159">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2cdc8-160"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2cdc8-160"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2cdc8-161">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2cdc8-161">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2cdc8-162">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2cdc8-162">See Also</span></span>

[<span data-ttu-id="2cdc8-163">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2cdc8-163">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2cdc8-164">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="2cdc8-164">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="2cdc8-165">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="2cdc8-165">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="2cdc8-166">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="2cdc8-166">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="2cdc8-167">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="2cdc8-167">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="2cdc8-168">JetOSSnapshotPrepareInstance</span><span class="sxs-lookup"><span data-stu-id="2cdc8-168">JetOSSnapshotPrepareInstance</span></span>](./jetossnapshotprepareinstance-function.md)  
[<span data-ttu-id="2cdc8-169">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="2cdc8-169">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)  
[<span data-ttu-id="2cdc8-170">JetOSSnapshotTruncateLog</span><span class="sxs-lookup"><span data-stu-id="2cdc8-170">JetOSSnapshotTruncateLog</span></span>](./jetossnapshottruncatelog-function.md)
