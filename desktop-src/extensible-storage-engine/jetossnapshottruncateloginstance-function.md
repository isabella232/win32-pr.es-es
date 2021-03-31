---
description: 'Más información acerca de: JetOSSnapshotTruncateLogInstance (función)'
title: JetOSSnapshotTruncateLogInstance función)
TOCTitle: JetOSSnapshotTruncateLogInstance Function
ms:assetid: ddc51957-5b89-4abf-9193-c34ef626a63e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294115(v=EXCHG.10)
ms:contentKeyID: 32765729
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLogInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cef30d012c28c809bb35d59a82fd596ba69bd175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808426"
---
# <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="af1b1-103">JetOSSnapshotTruncateLogInstance función)</span><span class="sxs-lookup"><span data-stu-id="af1b1-103">JetOSSnapshotTruncateLogInstance Function</span></span>


<span data-ttu-id="af1b1-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="af1b1-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncateloginstance-function"></a><span data-ttu-id="af1b1-105">JetOSSnapshotTruncateLogInstance función)</span><span class="sxs-lookup"><span data-stu-id="af1b1-105">JetOSSnapshotTruncateLogInstance Function</span></span>

<span data-ttu-id="af1b1-106">La función **JetOSSnapshotTruncateLogInstance** trunca el registro de una instancia especificada durante una sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="af1b1-106">The **JetOSSnapshotTruncateLogInstance** function truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="af1b1-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="af1b1-107">**Windows Vista:**  **JetOSSnapshotTruncateLogInstance** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLogInstance(
      __in          const JET_OSSNAPID snapId,
      __in          JET_INSTANCE instance,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="af1b1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af1b1-108">Parameters</span></span>

<span data-ttu-id="af1b1-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="af1b1-109">*snapId*</span></span>

<span data-ttu-id="af1b1-110">Identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="af1b1-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="af1b1-111">*repetición*</span><span class="sxs-lookup"><span data-stu-id="af1b1-111">*instance*</span></span>

<span data-ttu-id="af1b1-112">Instancia de que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="af1b1-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="af1b1-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="af1b1-113">*grbit*</span></span>

<span data-ttu-id="af1b1-114">Opciones de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="af1b1-114">The options for this call.</span></span> <span data-ttu-id="af1b1-115">Este parámetro puede tener una combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="af1b1-115">This parameter can have a combination of the following values.</span></span>

<span data-ttu-id="af1b1-116">*grbit* puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="af1b1-116">*grbit* can be one of the following values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af1b1-117">Value</span><span class="sxs-lookup"><span data-stu-id="af1b1-117">Value</span></span></p></th>
<th><p><span data-ttu-id="af1b1-118">Significado</span><span class="sxs-lookup"><span data-stu-id="af1b1-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af1b1-119">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="af1b1-119">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="af1b1-120">Todas las bases de datos están adjuntas para que el motor de almacenamiento pueda calcular y realizar el truncamiento del registro.</span><span class="sxs-lookup"><span data-stu-id="af1b1-120">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af1b1-121">0 (cero)</span><span class="sxs-lookup"><span data-stu-id="af1b1-121">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="af1b1-122">No se producirá ningún truncamiento.</span><span class="sxs-lookup"><span data-stu-id="af1b1-122">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="af1b1-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af1b1-123">Return Value</span></span>

<span data-ttu-id="af1b1-124">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="af1b1-124">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="af1b1-125">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="af1b1-125">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="af1b1-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="af1b1-126">Return code</span></span></p></th>
<th><p><span data-ttu-id="af1b1-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="af1b1-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af1b1-128">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="af1b1-128">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="af1b1-129">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="af1b1-129">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af1b1-130">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="af1b1-130">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="af1b1-131">El parámetro <em>grbit</em> no es válido.</span><span class="sxs-lookup"><span data-stu-id="af1b1-131">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af1b1-132">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="af1b1-132">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="af1b1-133">La sesión de instantáneas no está en el estado en el que puede producirse un truncamiento.</span><span class="sxs-lookup"><span data-stu-id="af1b1-133">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="af1b1-134">Las posibles causas son:</span><span class="sxs-lookup"><span data-stu-id="af1b1-134">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="af1b1-135">La llamada se completa después de que se agote el tiempo de espera de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="af1b1-135">The call completes after the snapshot session timed out.</span></span></p></li>
<li><p><span data-ttu-id="af1b1-136">La sesión se especificó como instantánea de copia.</span><span class="sxs-lookup"><span data-stu-id="af1b1-136">The session was specified as a copy snapshot.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="af1b1-137">Si esta función se ejecuta correctamente, se truncarán los archivos de registro de una o todas las instancias que forman parte de la sesión de instantáneas, si es posible.</span><span class="sxs-lookup"><span data-stu-id="af1b1-137">If this function succeeds, the log files for one or all of the instances that are part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="af1b1-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af1b1-138">Remarks</span></span>

<span data-ttu-id="af1b1-139">Solo se debe llamar a esta función si la instantánea se creó con la opción JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="af1b1-139">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="af1b1-140">De lo contrario, la sesión de instantánea finaliza después de la llamada a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="af1b1-140">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span>

#### <a name="requirements"></a><span data-ttu-id="af1b1-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af1b1-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af1b1-142"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="af1b1-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="af1b1-143">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="af1b1-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af1b1-144"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="af1b1-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="af1b1-145">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="af1b1-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af1b1-146"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="af1b1-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="af1b1-147">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="af1b1-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af1b1-148"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="af1b1-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="af1b1-149">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="af1b1-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af1b1-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="af1b1-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="af1b1-151">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="af1b1-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="af1b1-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="af1b1-152">See Also</span></span>

[<span data-ttu-id="af1b1-153">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="af1b1-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="af1b1-154">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="af1b1-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="af1b1-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="af1b1-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="af1b1-156">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="af1b1-156">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="af1b1-157">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="af1b1-157">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="af1b1-158">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="af1b1-158">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="af1b1-159">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="af1b1-159">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
