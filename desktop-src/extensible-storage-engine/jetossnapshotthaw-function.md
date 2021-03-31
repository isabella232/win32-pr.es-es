---
description: 'Más información acerca de: JetOSSnapshotThaw (función)'
title: JetOSSnapshotThaw función)
TOCTitle: JetOSSnapshotThaw Function
ms:assetid: 3b001113-6299-4082-ab15-461f2e33e996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269229(v=EXCHG.10)
ms:contentKeyID: 32765531
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotThaw
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da7d5037cfc6b9a5f001dede57581127e4de60b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913558"
---
# <a name="jetossnapshotthaw-function"></a><span data-ttu-id="c3629-103">JetOSSnapshotThaw función)</span><span class="sxs-lookup"><span data-stu-id="c3629-103">JetOSSnapshotThaw Function</span></span>


<span data-ttu-id="c3629-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c3629-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotthaw-function"></a><span data-ttu-id="c3629-105">JetOSSnapshotThaw función)</span><span class="sxs-lookup"><span data-stu-id="c3629-105">JetOSSnapshotThaw Function</span></span>

<span data-ttu-id="c3629-106">La función **JetOSSnapshotThaw** notifica al motor de que puede reanudar las operaciones de e/s normales después de un período de inmovilización y una instantánea correcta.</span><span class="sxs-lookup"><span data-stu-id="c3629-106">The **JetOSSnapshotThaw** function notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="c3629-107">**Windows XP:**  **JetOSSnapshotThaw** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3629-107">**Windows XP:**  **JetOSSnapshotThaw** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotThaw(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="c3629-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3629-108">Parameters</span></span>

<span data-ttu-id="c3629-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="c3629-109">*snapId*</span></span>

<span data-ttu-id="c3629-110">Identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="c3629-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="c3629-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="c3629-111">*grbit*</span></span>

<span data-ttu-id="c3629-112">Este parámetro está reservado para uso futuro y el único valor válido admitido es 0.</span><span class="sxs-lookup"><span data-stu-id="c3629-112">This parameter is reserved for future use and the only valid value supported is 0.</span></span>

### <a name="return-value"></a><span data-ttu-id="c3629-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3629-113">Return Value</span></span>

<span data-ttu-id="c3629-114">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="c3629-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c3629-115">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c3629-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c3629-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c3629-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="c3629-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3629-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3629-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c3629-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c3629-119">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c3629-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3629-120">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c3629-120">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c3629-121">La sesión de instantáneas no es válida o el parámetro <em>grbit</em> no es válido.</span><span class="sxs-lookup"><span data-stu-id="c3629-121">The snapshot session is invalid or the <em>grbit</em> parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3629-122">JET_errOSSnapshotTimeOut</span><span class="sxs-lookup"><span data-stu-id="c3629-122">JET_errOSSnapshotTimeOut</span></span></p></td>
<td><p><span data-ttu-id="c3629-123">La sesión de instantáneas tenía un tiempo de espera interno antes de que se produjera esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c3629-123">The snapshot session had an internal timeout before this call occurred.</span></span> <span data-ttu-id="c3629-124">Por lo tanto, las operaciones de e/s devolvían a normal antes de que se realizara esta llamada.</span><span class="sxs-lookup"><span data-stu-id="c3629-124">Consequently, IO operations returned to normal before this call was made.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3629-125">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="c3629-125">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="c3629-126">El identificador de la sesión de instantáneas no es válido.</span><span class="sxs-lookup"><span data-stu-id="c3629-126">The identifier for snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c3629-127">Si esta función se ejecuta correctamente, finaliza una sesión de instantáneas y se reanuda el comportamiento normal del motor.</span><span class="sxs-lookup"><span data-stu-id="c3629-127">If this function succeeds, a snapshot session ends and the normal engine behavior resumes.</span></span> <span data-ttu-id="c3629-128">Se puede iniciar una nueva sesión de instantáneas más adelante.</span><span class="sxs-lookup"><span data-stu-id="c3629-128">A new snapshot session can be started later.</span></span>

<span data-ttu-id="c3629-129">Si se produce un error en esta función, la sesión de instantáneas actual finaliza pero no se respeta internamente la inmovilización de IOs durante el período de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="c3629-129">If this function fails, the current snapshot session ends but the freeze of IOs during the snapshot period was not respected internally.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c3629-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3629-130">Remarks</span></span>

<span data-ttu-id="c3629-131">Se generarán entradas del registro de eventos para los distintos pasos de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="c3629-131">Event log entries will be generated for the different steps of the snapshot.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c3629-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3629-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3629-133"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c3629-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c3629-134">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3629-134">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3629-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c3629-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c3629-136">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c3629-136">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3629-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c3629-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c3629-138">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c3629-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3629-139"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="c3629-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c3629-140">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c3629-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3629-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c3629-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c3629-142">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c3629-142">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c3629-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c3629-143">See Also</span></span>

[<span data-ttu-id="c3629-144">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c3629-144">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c3629-145">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="c3629-145">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="c3629-146">JetOSSnapshotAbort</span><span class="sxs-lookup"><span data-stu-id="c3629-146">JetOSSnapshotAbort</span></span>](./jetossnapshotabort-function.md)  
[<span data-ttu-id="c3629-147">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="c3629-147">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="c3629-148">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="c3629-148">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)
