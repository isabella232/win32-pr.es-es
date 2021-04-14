---
description: 'Más información acerca de: JetOSSnapshotPrepareInstance (función)'
title: JetOSSnapshotPrepareInstance función)
TOCTitle: JetOSSnapshotPrepareInstance Function
ms:assetid: b4f06342-633f-47c6-be32-64ec058920fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294064(v=EXCHG.10)
ms:contentKeyID: 32765679
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepareInstance
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc5179a55aabfa3324e3caab7005f4abe437a6d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104424551"
---
# <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="d4cbb-103">JetOSSnapshotPrepareInstance función)</span><span class="sxs-lookup"><span data-stu-id="d4cbb-103">JetOSSnapshotPrepareInstance Function</span></span>


<span data-ttu-id="d4cbb-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d4cbb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotprepareinstance-function"></a><span data-ttu-id="d4cbb-105">JetOSSnapshotPrepareInstance función)</span><span class="sxs-lookup"><span data-stu-id="d4cbb-105">JetOSSnapshotPrepareInstance Function</span></span>

<span data-ttu-id="d4cbb-106">La función **JetOSSnapshotPrepareInstance** selecciona una instancia específica para que forme parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-106">The **JetOSSnapshotPrepareInstance** function selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="d4cbb-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** se presentó en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-107">**Windows Vista:** **JetOSSnapshotPrepareInstance** was introduced in Windows Vista.</span></span>

```cpp
JET_ERR JET_API JetOSSnapshotPrepareInstance(
  __in          JET_OSSNAPID snapId,
  __in          JET_INSTANCE instance,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="d4cbb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4cbb-108">Parameters</span></span>

<span data-ttu-id="d4cbb-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="d4cbb-109">*snapId*</span></span>

<span data-ttu-id="d4cbb-110">Identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="d4cbb-111">*repetición*</span><span class="sxs-lookup"><span data-stu-id="d4cbb-111">*instance*</span></span>

<span data-ttu-id="d4cbb-112">Instancia de que se utilizará para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-112">The instance that will be used for this call.</span></span>

<span data-ttu-id="d4cbb-113">*grbit*</span><span class="sxs-lookup"><span data-stu-id="d4cbb-113">*grbit*</span></span>

<span data-ttu-id="d4cbb-114">Opciones de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-114">The options for this call.</span></span> <span data-ttu-id="d4cbb-115">Este parámetro se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-115">This parameter is reserved for future use.</span></span> <span data-ttu-id="d4cbb-116">El único valor válido es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="d4cbb-116">The only valid value is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="d4cbb-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4cbb-117">Return Value</span></span>

<span data-ttu-id="d4cbb-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d4cbb-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d4cbb-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4cbb-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d4cbb-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="d4cbb-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4cbb-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4cbb-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d4cbb-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d4cbb-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4cbb-124">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="d4cbb-124">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="d4cbb-125">El puntero de identificador de instantánea es <strong>null</strong> o el parámetro <em>grbit</em> no es válido.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-125">The snapshot id pointer is <strong>NULL</strong> or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4cbb-126">JET_errOSSnapshotInvalidSequence</span><span class="sxs-lookup"><span data-stu-id="d4cbb-126">JET_errOSSnapshotInvalidSequence</span></span></p></td>
<td><p><span data-ttu-id="d4cbb-127">Ya hay una sesión de instantánea en curso.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-127">A snapshot session is already in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4cbb-128">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="d4cbb-128">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="d4cbb-129">El identificador de la sesión de instantáneas no es válido.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-129">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d4cbb-130">Si esta función se ejecuta correctamente, la instancia especificada formará parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-130">If this function succeeds, the specified instance will be part of the snapshot session.</span></span>

<span data-ttu-id="d4cbb-131">Si se produce un error en esta función, no se produce ningún cambio en el estado del motor.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-131">If this function fails, no change in the engine state occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="d4cbb-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4cbb-132">Remarks</span></span>

<span data-ttu-id="d4cbb-133">La llamada de secuencia de API normal es: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), seguido, opcionalmente, de una o varias llamadas a **JetOSSnapshotPrepareInstance** y, después, por [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span><span class="sxs-lookup"><span data-stu-id="d4cbb-133">The normal API sequence call is: [JetOSSnapshotPrepare](./jetossnapshotprepare-function.md), optionally followed by one or more calls to **JetOSSnapshotPrepareInstance**, then followed by [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md).</span></span> <span data-ttu-id="d4cbb-134">Una vez que se inicia la inmovilización, puede terminarse mediante [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span><span class="sxs-lookup"><span data-stu-id="d4cbb-134">Once the freeze is started, it can be terminated using [JetOSSnapshotThaw](./jetossnapshotthaw-function.md).</span></span> <span data-ttu-id="d4cbb-135">En cualquier momento después de la preparación, la sesión de instantáneas puede terminar repentinamente con [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span><span class="sxs-lookup"><span data-stu-id="d4cbb-135">At any time after the prepare, the snapshot session can be abruptly terminated with [JetOSSnapshotAbort](./jetossnapshotabort-function.md).</span></span> <span data-ttu-id="d4cbb-136">Se generarán entradas del registro de eventos para los distintos pasos de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-136">Event log entries will be generated for the different steps of the snapshot.</span></span>

<span data-ttu-id="d4cbb-137">Si no se llama a **JetOSSnapshotPrepareInstance** entre el inicio de la sesión ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) y el momento de la inmovilización ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), todas las instancias en ejecución del motor se inmovilizarán y pasarán a formar parte de la sesión de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-137">If **JetOSSnapshotPrepareInstance** is not called between the start of the session ([JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)) and the freeze moment ([JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)), all the running instances in the engine will freeze and become part of the snapshot session.</span></span> <span data-ttu-id="d4cbb-138">Esto se produce por dos motivos:</span><span class="sxs-lookup"><span data-stu-id="d4cbb-138">This occurs for two reasons:</span></span>

  - <span data-ttu-id="d4cbb-139">Simplifica el código para los usuarios que deseen todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-139">It simplifies the code for users who want all instances.</span></span>

  - <span data-ttu-id="d4cbb-140">Permite la compatibilidad con versiones anteriores de las API de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-140">It allows backward compatibility for the callers of the snapshot APIs.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d4cbb-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4cbb-141">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4cbb-142"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d4cbb-142"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d4cbb-143">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-143">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4cbb-144"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d4cbb-144"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d4cbb-145">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-145">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4cbb-146"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d4cbb-146"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d4cbb-147">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-147">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4cbb-148"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="d4cbb-148"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d4cbb-149">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-149">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d4cbb-150"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d4cbb-150"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d4cbb-151">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d4cbb-151">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d4cbb-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d4cbb-152">See Also</span></span>

[<span data-ttu-id="d4cbb-153">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="d4cbb-153">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="d4cbb-154">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="d4cbb-154">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="d4cbb-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d4cbb-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d4cbb-156">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="d4cbb-156">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="d4cbb-157">JetOSSnapshotEnd</span><span class="sxs-lookup"><span data-stu-id="d4cbb-157">JetOSSnapshotEnd</span></span>](./jetossnapshotend-function.md)  
[<span data-ttu-id="d4cbb-158">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="d4cbb-158">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="d4cbb-159">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="d4cbb-159">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="d4cbb-160">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="d4cbb-160">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
