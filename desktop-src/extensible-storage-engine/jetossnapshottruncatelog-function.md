---
description: 'Más información acerca de: JetOSSnapshotTruncateLog (función)'
title: JetOSSnapshotTruncateLog función)
TOCTitle: JetOSSnapshotTruncateLog Function
ms:assetid: 3df8f5b2-8083-49b7-a325-fd13187f785c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269231(v=EXCHG.10)
ms:contentKeyID: 32765533
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotTruncateLog
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0a3cebd743a3c8cd9a3d86f1f637dcb5b2c9c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648587"
---
# <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="6a0d9-103">JetOSSnapshotTruncateLog función)</span><span class="sxs-lookup"><span data-stu-id="6a0d9-103">JetOSSnapshotTruncateLog Function</span></span>


<span data-ttu-id="6a0d9-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6a0d9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshottruncatelog-function"></a><span data-ttu-id="6a0d9-105">JetOSSnapshotTruncateLog función)</span><span class="sxs-lookup"><span data-stu-id="6a0d9-105">JetOSSnapshotTruncateLog Function</span></span>

<span data-ttu-id="6a0d9-106">La función **JetOSSnapshotTruncateLog** habilita el truncamiento del registro para todas las instancias que forman parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-106">The **JetOSSnapshotTruncateLog** function enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="6a0d9-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-107">**Windows Vista:**  **JetOSSnapshotTruncateLog** is introduced in Windows Vista.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotTruncateLog(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="6a0d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a0d9-108">Parameters</span></span>

<span data-ttu-id="6a0d9-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="6a0d9-109">*snapId*</span></span>

<span data-ttu-id="6a0d9-110">Identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="6a0d9-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="6a0d9-111">*grbit*</span></span>

<span data-ttu-id="6a0d9-112">Opciones de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-112">The options for this call.</span></span> <span data-ttu-id="6a0d9-113">Este parámetro puede tener una combinación de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-113">This parameter can have a combination of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a0d9-114">Value</span><span class="sxs-lookup"><span data-stu-id="6a0d9-114">Value</span></span></p></th>
<th><p><span data-ttu-id="6a0d9-115">Significado</span><span class="sxs-lookup"><span data-stu-id="6a0d9-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a0d9-116">JET_bitAllDatabasesSnapshot</span><span class="sxs-lookup"><span data-stu-id="6a0d9-116">JET_bitAllDatabasesSnapshot</span></span></p></td>
<td><p><span data-ttu-id="6a0d9-117">Todas las bases de datos están adjuntas para que el motor de almacenamiento pueda calcular y realizar el truncamiento del registro.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-117">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a0d9-118">0 (cero)</span><span class="sxs-lookup"><span data-stu-id="6a0d9-118">0 (zero)</span></span></p></td>
<td><p><span data-ttu-id="6a0d9-119">No se producirá ningún truncamiento.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-119">No truncation will occur.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="6a0d9-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a0d9-120">Return Value</span></span>

<span data-ttu-id="6a0d9-121">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="6a0d9-122">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6a0d9-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6a0d9-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6a0d9-123">Return code</span></span></p></th>
<th><p><span data-ttu-id="6a0d9-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a0d9-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a0d9-125">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="6a0d9-125">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="6a0d9-126">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-126">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a0d9-127">JET_errInvalidGrbit</span><span class="sxs-lookup"><span data-stu-id="6a0d9-127">JET_errInvalidGrbit</span></span></p></td>
<td><p><span data-ttu-id="6a0d9-128">El parámetro <em>grbit</em> no es válido.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-128">The <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a0d9-129">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="6a0d9-129">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="6a0d9-130">La sesión de instantáneas no está en el estado en el que puede producirse un truncamiento.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-130">The snapshot session is not in the state in which a truncation can occur.</span></span> <span data-ttu-id="6a0d9-131">Las posibles causas son:</span><span class="sxs-lookup"><span data-stu-id="6a0d9-131">Possible causes are:</span></span></p>
<ul>
<li><p><span data-ttu-id="6a0d9-132">la llamada se realiza después de que se agote el tiempo de espera de la sesión de instantáneas</span><span class="sxs-lookup"><span data-stu-id="6a0d9-132">the call is done after the snapshot session timed-out</span></span></p></li>
<li><p><span data-ttu-id="6a0d9-133">la sesión se especificó como instantánea de copia</span><span class="sxs-lookup"><span data-stu-id="6a0d9-133">the session was specified as a copy snapshot</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6a0d9-134">Si se ejecuta correctamente, se truncarán los archivos de registro de una o todas las instancias que formen parte de la sesión de instantáneas, si es posible.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-134">On success, the log files for one or all the instances part of the snapshot session will be truncated, if possible.</span></span>

#### <a name="remarks"></a><span data-ttu-id="6a0d9-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a0d9-135">Remarks</span></span>

<span data-ttu-id="6a0d9-136">Solo se debe llamar a esta función si la instantánea se creó con la opción JET_bitContinueAfterThaw.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-136">This function should be called only if the snapshot was created with the JET_bitContinueAfterThaw option.</span></span> <span data-ttu-id="6a0d9-137">De lo contrario, la sesión de instantánea habría finalizado después de la llamada a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) .</span><span class="sxs-lookup"><span data-stu-id="6a0d9-137">Otherwise, the snapshot session would have ended after the [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) call.</span></span>

#### <a name="requirements"></a><span data-ttu-id="6a0d9-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a0d9-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6a0d9-139"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="6a0d9-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6a0d9-140">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-140">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a0d9-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6a0d9-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6a0d9-142">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-142">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a0d9-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6a0d9-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6a0d9-144">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6a0d9-145"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="6a0d9-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="6a0d9-146">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6a0d9-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="6a0d9-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="6a0d9-148">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="6a0d9-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="6a0d9-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6a0d9-149">See Also</span></span>

[<span data-ttu-id="6a0d9-150">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="6a0d9-150">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="6a0d9-151">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="6a0d9-151">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="6a0d9-152">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="6a0d9-152">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="6a0d9-153">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="6a0d9-153">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="6a0d9-154">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="6a0d9-154">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="6a0d9-155">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="6a0d9-155">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="6a0d9-156">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="6a0d9-156">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
