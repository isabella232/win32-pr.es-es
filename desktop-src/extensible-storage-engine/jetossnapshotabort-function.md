---
description: 'Más información acerca de: JetOSSnapshotAbort (función)'
title: JetOSSnapshotAbort función)
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716603"
---
# <a name="jetossnapshotabort-function"></a><span data-ttu-id="46cbe-103">JetOSSnapshotAbort función)</span><span class="sxs-lookup"><span data-stu-id="46cbe-103">JetOSSnapshotAbort Function</span></span>


<span data-ttu-id="46cbe-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="46cbe-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetossnapshotabort-function"></a><span data-ttu-id="46cbe-105">JetOSSnapshotAbort función)</span><span class="sxs-lookup"><span data-stu-id="46cbe-105">JetOSSnapshotAbort Function</span></span>

<span data-ttu-id="46cbe-106">La función **JetOSSnapshotAbort** notifica al motor de que puede reanudar las operaciones de e/s normales después de que finalice un periodo de inmovilización con una instantánea con errores.</span><span class="sxs-lookup"><span data-stu-id="46cbe-106">The **JetOSSnapshotAbort** function notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="46cbe-107">**Windows server 2003:**  **JetOSSnapshotAbort** se incorporó en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="46cbe-107">**Windows Server 2003:**  **JetOSSnapshotAbort** is introduced in Windows Server 2003.</span></span>

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="46cbe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46cbe-108">Parameters</span></span>

<span data-ttu-id="46cbe-109">*snapId*</span><span class="sxs-lookup"><span data-stu-id="46cbe-109">*snapId*</span></span>

<span data-ttu-id="46cbe-110">Identificador de la sesión de instantánea.</span><span class="sxs-lookup"><span data-stu-id="46cbe-110">The identifier of the snapshot session.</span></span>

<span data-ttu-id="46cbe-111">*grbit*</span><span class="sxs-lookup"><span data-stu-id="46cbe-111">*grbit*</span></span>

<span data-ttu-id="46cbe-112">Opciones de esta llamada.</span><span class="sxs-lookup"><span data-stu-id="46cbe-112">The options for this call.</span></span> <span data-ttu-id="46cbe-113">Este parámetro se reserva para uso futuro y el único valor válido admitido es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="46cbe-113">This parameter is reserved for future use and the only valid value supported is 0 (zero).</span></span>

### <a name="return-value"></a><span data-ttu-id="46cbe-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46cbe-114">Return Value</span></span>

<span data-ttu-id="46cbe-115">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="46cbe-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="46cbe-116">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="46cbe-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="46cbe-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="46cbe-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="46cbe-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="46cbe-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46cbe-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="46cbe-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="46cbe-120">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="46cbe-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46cbe-121">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="46cbe-121">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="46cbe-122">La sesión de instantáneas no es válida o el parámetro grbit no es válido.</span><span class="sxs-lookup"><span data-stu-id="46cbe-122">The snapshot session is invalid or the grbit parameter is invalid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46cbe-123">JET_errOSSnapshotInvalidSnapId</span><span class="sxs-lookup"><span data-stu-id="46cbe-123">JET_errOSSnapshotInvalidSnapId</span></span></p></td>
<td><p><span data-ttu-id="46cbe-124">El identificador de la sesión de instantáneas no es válido.</span><span class="sxs-lookup"><span data-stu-id="46cbe-124">The identifier for the snapshot session is not valid.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="46cbe-125">Si esta función se ejecuta correctamente, finalizará la sesión de instantáneas y se reanudará el comportamiento normal del motor.</span><span class="sxs-lookup"><span data-stu-id="46cbe-125">If this function succeeds, the snapshot session will end and the normal engine behavior will resume.</span></span> <span data-ttu-id="46cbe-126">Se puede iniciar una nueva sesión de instantáneas en un momento posterior.</span><span class="sxs-lookup"><span data-stu-id="46cbe-126">A new snapshot session can be started at a later point.</span></span>

<span data-ttu-id="46cbe-127">Si se produce un error en esta función, la sesión de instantáneas no se anulará.</span><span class="sxs-lookup"><span data-stu-id="46cbe-127">If this function fails, the snapshot session will not be aborted.</span></span>

#### <a name="remarks"></a><span data-ttu-id="46cbe-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46cbe-128">Remarks</span></span>

<span data-ttu-id="46cbe-129">Se debe llamar a esta función en lugar de a [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para informar al motor de que la instantánea se ha anulado por razones que no están relacionadas con el motor.</span><span class="sxs-lookup"><span data-stu-id="46cbe-129">This function should be called instead of [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) to inform the engine that the snapshot was aborted for reasons that don't relate to the engine.</span></span> <span data-ttu-id="46cbe-130">Esta información se puede usar más adelante para ayudar a emitir mensajes de registro de eventos acerca de la sesión de instantáneas o para ayudar a determinar otras acciones adecuadas.</span><span class="sxs-lookup"><span data-stu-id="46cbe-130">This information can be used later to help issue event log messages about the snapshot session or to help determine other appropriate actions.</span></span>

#### <a name="requirements"></a><span data-ttu-id="46cbe-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46cbe-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="46cbe-132"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="46cbe-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="46cbe-133">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="46cbe-133">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46cbe-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="46cbe-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="46cbe-135">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="46cbe-135">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46cbe-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="46cbe-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="46cbe-137">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="46cbe-137">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="46cbe-138"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="46cbe-138"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="46cbe-139">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="46cbe-139">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="46cbe-140"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="46cbe-140"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="46cbe-141">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="46cbe-141">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="46cbe-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="46cbe-142">See Also</span></span>

[<span data-ttu-id="46cbe-143">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="46cbe-143">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="46cbe-144">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="46cbe-144">JET_OSSNAPID</span></span>](./jet-ossnapid.md)  
[<span data-ttu-id="46cbe-145">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="46cbe-145">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="46cbe-146">JetOSSnapshotPrepare</span><span class="sxs-lookup"><span data-stu-id="46cbe-146">JetOSSnapshotPrepare</span></span>](./jetossnapshotprepare-function.md)  
[<span data-ttu-id="46cbe-147">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="46cbe-147">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
