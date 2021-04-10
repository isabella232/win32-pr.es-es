---
description: 'Más información acerca de: JetOSSnapshotEnd (función)'
title: JetOSSnapshotEnd función)
TOCTitle: JetOSSnapshotEnd Function
ms:assetid: f7f4db8b-8e40-48d7-bc7b-0c80d0d0f77f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294136(v=EXCHG.10)
ms:contentKeyID: 32765750
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotEnd
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1237de9af0b1b75f645346fc30a128a1b8e907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153772"
---
# <a name="jetossnapshotend-function"></a><span data-ttu-id="e32a8-103">JetOSSnapshotEnd función)</span><span class="sxs-lookup"><span data-stu-id="e32a8-103">JetOSSnapshotEnd Function</span></span>


<span data-ttu-id="e32a8-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e32a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotend-function"></a><span data-ttu-id="e32a8-105">JetOSSnapshotEnd función)</span><span class="sxs-lookup"><span data-stu-id="e32a8-105">JetOSSnapshotEnd Function</span></span>

<span data-ttu-id="e32a8-106">La función **JetOSSnapshotEnd** notifica al motor que la sesión de instantáneas ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="e32a8-106">The **JetOSSnapshotEnd** function notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="e32a8-107">**Windows Vista:**  **JetOSSnapshotEnd** se presentó en Windows Vista:.</span><span class="sxs-lookup"><span data-stu-id="e32a8-107">**Windows Vista:**  **JetOSSnapshotEnd** is introduced in Windows Vista:.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotEnd(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="e32a8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e32a8-108">Parameters</span></span>

<span data-ttu-id="e32a8-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="e32a8-109">*snapId*</span></span>

<span data-ttu-id="e32a8-110">Identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="e32a8-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="e32a8-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="e32a8-111">*grbit*</span></span>

<span data-ttu-id="e32a8-112">Opciones de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e32a8-112">The options for this call.</span></span> <span data-ttu-id="e32a8-113">Este parámetro puede tener una combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="e32a8-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e32a8-114">Value</span><span class="sxs-lookup"><span data-stu-id="e32a8-114">Value</span></span></p></th>
<th><p><span data-ttu-id="e32a8-115">Significado</span><span class="sxs-lookup"><span data-stu-id="e32a8-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e32a8-116">0</span><span class="sxs-lookup"><span data-stu-id="e32a8-116">0</span></span></p></td>
<td><p><span data-ttu-id="e32a8-117">Finalización correcta de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="e32a8-117">The successful end of the snapshot session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e32a8-118">JET_bitAbortSnapshot</span><span class="sxs-lookup"><span data-stu-id="e32a8-118">JET_bitAbortSnapshot</span></span></p></td>
<td><p><span data-ttu-id="e32a8-119">Se anuló la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="e32a8-119">The snapshot session aborted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e32a8-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e32a8-120">Return Value</span></span>

<span data-ttu-id="e32a8-121">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="e32a8-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="e32a8-122">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e32a8-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e32a8-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e32a8-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="e32a8-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e32a8-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e32a8-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="e32a8-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="e32a8-126">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e32a8-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e32a8-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="e32a8-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="e32a8-128">Una de las opciones solicitadas no es válida, se usa incorrectamente o no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="e32a8-128">One of the options requested is invalid, used incorrectly, or not implemented.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e32a8-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="e32a8-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="e32a8-130">Ya hay una sesión de instantánea en curso.</span><span class="sxs-lookup"><span data-stu-id="e32a8-130">A snapshot session is already in progress.</span></span> <span data-ttu-id="e32a8-131">Esto no está permitido.</span><span class="sxs-lookup"><span data-stu-id="e32a8-131">This is not allowed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e32a8-132">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="e32a8-132">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="e32a8-133">El identificador de la sesión de instantáneas no es válido.</span><span class="sxs-lookup"><span data-stu-id="e32a8-133">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e32a8-134">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="e32a8-134">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="e32a8-135">La sesión de instantáneas tenía un tiempo de espera interno antes de que se produjera esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e32a8-135">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="e32a8-136">Como resultado, las operaciones de e/s devueltas a la normalidad antes de que se realizara esta llamada.</span><span class="sxs-lookup"><span data-stu-id="e32a8-136">As a result, the IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e32a8-137">Si esta función se ejecuta correctamente, se completará una sesión de instantáneas y se reanudará el comportamiento normal del motor.</span><span class="sxs-lookup"><span data-stu-id="e32a8-137">If this function succeeds, a snapshot session will complete and the normal engine behavior will resume.</span></span> <span data-ttu-id="e32a8-138">Se puede iniciar una nueva sesión de instantáneas más adelante.</span><span class="sxs-lookup"><span data-stu-id="e32a8-138">A new snapshot session can be started later.</span></span>

<span data-ttu-id="e32a8-139">Si se produce un error en esta función, el código devuelto JET_errOSSnapshotTimeOut devuelve y la sesión de instantáneas actual finaliza pero no se respeta internamente la inmovilización de IOs durante el período de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="e32a8-139">If this function fails, the JET_errOSSnapshotTimeOut return code returns and the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span> <span data-ttu-id="e32a8-140">En el caso de todos los demás errores, no se cambiará el estado de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="e32a8-140">For all other errors, the snapshot session state will not be changed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="e32a8-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e32a8-141">Remarks</span></span>

<span data-ttu-id="e32a8-142">Solo se llama a esta función si se llamó a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) con JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="e32a8-142">This function is called only if [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) was called with JET_bitContinueAfterThaw.</span></span>

<span data-ttu-id="e32a8-143">La sesión de instantánea debe completarse para que tenga lugar la comprobación de la instantánea y el truncamiento del registro.</span><span class="sxs-lookup"><span data-stu-id="e32a8-143">The snapshot session must complete for the snapshot verification and log truncation to take place.</span></span> <span data-ttu-id="e32a8-144">Se generarán entradas del registro de eventos para los distintos pasos de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="e32a8-144">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="e32a8-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e32a8-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e32a8-146"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="e32a8-146"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e32a8-147">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e32a8-147">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e32a8-148"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="e32a8-148"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e32a8-149">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e32a8-149">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e32a8-150"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="e32a8-150"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e32a8-151">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="e32a8-151">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e32a8-152"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="e32a8-152"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="e32a8-153">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="e32a8-153">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e32a8-154"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="e32a8-154"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="e32a8-155">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="e32a8-155">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="e32a8-156">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e32a8-156">See Also</span></span>

[<span data-ttu-id="e32a8-157">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="e32a8-157">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="e32a8-158">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="e32a8-158">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="e32a8-159">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="e32a8-159">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="e32a8-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="e32a8-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
