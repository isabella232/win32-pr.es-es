---
title: Estado de llamada asincrónica
description: En esta página se describe el estado de la llamada asincrónica para las llamadas RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903887"
---
# <a name="asynchronous-call-state"></a><span data-ttu-id="1630a-103">Estado de llamada asincrónica</span><span class="sxs-lookup"><span data-stu-id="1630a-103">Asynchronous Call State</span></span>

<span data-ttu-id="1630a-104">En esta página se describe el estado de la llamada asincrónica para las llamadas RPC.</span><span class="sxs-lookup"><span data-stu-id="1630a-104">This page describes the Asynchronous Call State for RPC calls.</span></span>

## <a name="client-behavior"></a><span data-ttu-id="1630a-105">Comportamiento del cliente</span><span class="sxs-lookup"><span data-stu-id="1630a-105">Client Behavior</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1630a-106">Estado</span><span class="sxs-lookup"><span data-stu-id="1630a-106">State</span></span></th>
<th><span data-ttu-id="1630a-107">Nombre del estado</span><span class="sxs-lookup"><span data-stu-id="1630a-107">State name</span></span></th>
<th><span data-ttu-id="1630a-108">Acción</span><span class="sxs-lookup"><span data-stu-id="1630a-108">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1630a-109">C</span><span class="sxs-lookup"><span data-stu-id="1630a-109">C</span></span></td>
<td><span data-ttu-id="1630a-110">Hacer la llamada</span><span class="sxs-lookup"><span data-stu-id="1630a-110">Make the call</span></span></td>
<td><span data-ttu-id="1630a-111">Hacer que la RPC</span><span class="sxs-lookup"><span data-stu-id="1630a-111">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="1630a-112">En caso de éxito, vaya al estado WComp</span><span class="sxs-lookup"><span data-stu-id="1630a-112">On success go to state WComp</span></span></li>
<li><span data-ttu-id="1630a-113">Al final de la excepción</span><span class="sxs-lookup"><span data-stu-id="1630a-113">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="1630a-114">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="1630a-114">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1630a-115">Poder</span><span class="sxs-lookup"><span data-stu-id="1630a-115">Can</span></span></td>
<td><span data-ttu-id="1630a-116">Cancelar la llamada</span><span class="sxs-lookup"><span data-stu-id="1630a-116">Cancel the call</span></span></td>
<td><span data-ttu-id="1630a-117">Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>ir a WComp</span><span class="sxs-lookup"><span data-stu-id="1630a-117">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1630a-118">WComp</span><span class="sxs-lookup"><span data-stu-id="1630a-118">WComp</span></span></td>
<td><span data-ttu-id="1630a-119">Esperar a que finalice</span><span class="sxs-lookup"><span data-stu-id="1630a-119">Wait for completion</span></span></td>
<td><span data-ttu-id="1630a-120">Espere a que se reciba la notificación de notificationCall complete</span><span class="sxs-lookup"><span data-stu-id="1630a-120">Wait for notificationCall-complete notification should be received</span></span><br/> <span data-ttu-id="1630a-121">Ir a comp</span><span class="sxs-lookup"><span data-stu-id="1630a-121">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1630a-122">Comp</span><span class="sxs-lookup"><span data-stu-id="1630a-122">Comp</span></span></td>
<td><span data-ttu-id="1630a-123">Completion</span><span class="sxs-lookup"><span data-stu-id="1630a-123">Completion</span></span></td>
<td><span data-ttu-id="1630a-124">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final</span><span class="sxs-lookup"><span data-stu-id="1630a-124">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1630a-125">End</span><span class="sxs-lookup"><span data-stu-id="1630a-125">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a><span data-ttu-id="1630a-126">Comportamiento del servidor</span><span class="sxs-lookup"><span data-stu-id="1630a-126">Server Behavior</span></span>



| <span data-ttu-id="1630a-127">Estado</span><span class="sxs-lookup"><span data-stu-id="1630a-127">State</span></span> | <span data-ttu-id="1630a-128">Nombre del estado</span><span class="sxs-lookup"><span data-stu-id="1630a-128">State name</span></span>     | <span data-ttu-id="1630a-129">Acción</span><span class="sxs-lookup"><span data-stu-id="1630a-129">Action</span></span>                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1630a-130">D</span><span class="sxs-lookup"><span data-stu-id="1630a-130">D</span></span>     | <span data-ttu-id="1630a-131">Dispatch</span><span class="sxs-lookup"><span data-stu-id="1630a-131">Dispatch</span></span>       | <span data-ttu-id="1630a-132">La llamada se envía mediante el runtimeProcess de RPC</span><span class="sxs-lookup"><span data-stu-id="1630a-132">The call is dispatched by the RPC runtimeProcess</span></span><br/> <span data-ttu-id="1630a-133">Ir a comp</span><span class="sxs-lookup"><span data-stu-id="1630a-133">Go to Comp</span></span><br/> <span data-ttu-id="1630a-134">Para producir un error irrecuperable (mientras se ejecuta en el subproceso RPC): generar excepción; ir al final</span><span class="sxs-lookup"><span data-stu-id="1630a-134">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="1630a-135">Para que se produzca un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="1630a-135">To fail gracefully: go to A</span></span><br/> |
| <span data-ttu-id="1630a-136">A</span><span class="sxs-lookup"><span data-stu-id="1630a-136">A</span></span>     | <span data-ttu-id="1630a-137">Anular la llamada</span><span class="sxs-lookup"><span data-stu-id="1630a-137">Abort the call</span></span> | <span data-ttu-id="1630a-138">Llamar a [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)ir al final</span><span class="sxs-lookup"><span data-stu-id="1630a-138">Call [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="1630a-139">Comp</span><span class="sxs-lookup"><span data-stu-id="1630a-139">Comp</span></span>  | <span data-ttu-id="1630a-140">Completion</span><span class="sxs-lookup"><span data-stu-id="1630a-140">Completion</span></span>     | <span data-ttu-id="1630a-141">Problema [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)ir al final</span><span class="sxs-lookup"><span data-stu-id="1630a-141">Issue [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Go to End</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="1630a-142">End</span><span class="sxs-lookup"><span data-stu-id="1630a-142">End</span></span>   |                |                                                                                                                                                                                                                     |



 

 

 





