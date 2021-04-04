---
title: Estado de canalización asincrónica
description: En esta página se describe el estado de la canalización asincrónica para las llamadas RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077325"
---
# <a name="asynchronous-pipe-state"></a><span data-ttu-id="43a5c-103">Estado de canalización asincrónica</span><span class="sxs-lookup"><span data-stu-id="43a5c-103">Asynchronous Pipe State</span></span>

<span data-ttu-id="43a5c-104">En esta página se describe el estado de la canalización asincrónica para las llamadas RPC.</span><span class="sxs-lookup"><span data-stu-id="43a5c-104">This page describes the Asynchronous Pipe State for RPC calls.</span></span>

## <a name="in-pipe"></a><span data-ttu-id="43a5c-105">EN canalización</span><span class="sxs-lookup"><span data-stu-id="43a5c-105">IN Pipe</span></span>

<span data-ttu-id="43a5c-106">Comportamiento del cliente</span><span class="sxs-lookup"><span data-stu-id="43a5c-106">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43a5c-107">Estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-107">State</span></span></th>
<th><span data-ttu-id="43a5c-108">Nombre de estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-108">State Name</span></span></th>
<th><span data-ttu-id="43a5c-109">Acción</span><span class="sxs-lookup"><span data-stu-id="43a5c-109">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43a5c-110">C</span><span class="sxs-lookup"><span data-stu-id="43a5c-110">C</span></span></td>
<td><span data-ttu-id="43a5c-111">Hacer la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-111">Make the call</span></span></td>
<td><span data-ttu-id="43a5c-112">Hacer que la RPC</span><span class="sxs-lookup"><span data-stu-id="43a5c-112">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="43a5c-113">En caso de éxito, vaya a estado WS</span><span class="sxs-lookup"><span data-stu-id="43a5c-113">On success go to state WS</span></span></li>
<li><span data-ttu-id="43a5c-114">Al final de la excepción</span><span class="sxs-lookup"><span data-stu-id="43a5c-114">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="43a5c-115">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-115">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-116">P</span><span class="sxs-lookup"><span data-stu-id="43a5c-116">P</span></span></td>
<td><span data-ttu-id="43a5c-117">Inserción</span><span class="sxs-lookup"><span data-stu-id="43a5c-117">Push</span></span></td>
<td><span data-ttu-id="43a5c-118">Hacer una inserciones</span><span class="sxs-lookup"><span data-stu-id="43a5c-118">Make a push</span></span>
<ul>
<li><span data-ttu-id="43a5c-119">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-119">On failure go to End</span></span></li>
<li><span data-ttu-id="43a5c-120">En caso de éxito, vaya a WS</span><span class="sxs-lookup"><span data-stu-id="43a5c-120">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="43a5c-121">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-121">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-122">WS</span><span class="sxs-lookup"><span data-stu-id="43a5c-122">WS</span></span></td>
<td><span data-ttu-id="43a5c-123">Esperar envío</span><span class="sxs-lookup"><span data-stu-id="43a5c-123">Wait for Send</span></span></td>
<td><span data-ttu-id="43a5c-124">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-124">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-125">Si se produce un error al recibir una notificación, puede</span><span class="sxs-lookup"><span data-stu-id="43a5c-125">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="43a5c-126">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y es necesario enviar más datos, vaya a P</span><span class="sxs-lookup"><span data-stu-id="43a5c-126">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="43a5c-127">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y no es necesario enviar más datos, vaya a NP</span><span class="sxs-lookup"><span data-stu-id="43a5c-127">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="43a5c-128">Si se recibe un error <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="43a5c-128">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="43a5c-129">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-129">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-130">NP</span><span class="sxs-lookup"><span data-stu-id="43a5c-130">NP</span></span></td>
<td><span data-ttu-id="43a5c-131">Inserciones nulas</span><span class="sxs-lookup"><span data-stu-id="43a5c-131">Null Push</span></span></td>
<td><span data-ttu-id="43a5c-132">Inserte 0 bytes (inserciones nulas)</span><span class="sxs-lookup"><span data-stu-id="43a5c-132">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="43a5c-133">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-133">On failure go to End</span></span></li>
<li><span data-ttu-id="43a5c-134">En caso de éxito, vaya a WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-134">On success go to WComp</span></span></li>
</ul>
<span data-ttu-id="43a5c-135">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-135">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-136">Poder</span><span class="sxs-lookup"><span data-stu-id="43a5c-136">Can</span></span></td>
<td><span data-ttu-id="43a5c-137">Cancelar la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-137">Cancel the Call</span></span></td>
<td><span data-ttu-id="43a5c-138">Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>ir a WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-138">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-139">WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-139">WComp</span></span></td>
<td><span data-ttu-id="43a5c-140">Esperar a que finalice</span><span class="sxs-lookup"><span data-stu-id="43a5c-140">Wait for Completion</span></span></td>
<td><span data-ttu-id="43a5c-141">Espere a que se reciba la notificación de notificationCall complete.</span><span class="sxs-lookup"><span data-stu-id="43a5c-141">Wait for notificationCall-complete notification should be received.</span></span><br/> <span data-ttu-id="43a5c-142">Ir a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-142">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-143">Comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-143">Comp</span></span></td>
<td><span data-ttu-id="43a5c-144">Completion</span><span class="sxs-lookup"><span data-stu-id="43a5c-144">Completion</span></span></td>
<td><span data-ttu-id="43a5c-145">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-145">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-146">End</span><span class="sxs-lookup"><span data-stu-id="43a5c-146">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="43a5c-147">Comportamiento del servidor</span><span class="sxs-lookup"><span data-stu-id="43a5c-147">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43a5c-148">Estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-148">State</span></span></th>
<th><span data-ttu-id="43a5c-149">Nombre de estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-149">State Name</span></span></th>
<th><span data-ttu-id="43a5c-150">Acción</span><span class="sxs-lookup"><span data-stu-id="43a5c-150">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43a5c-151">D</span><span class="sxs-lookup"><span data-stu-id="43a5c-151">D</span></span></td>
<td><span data-ttu-id="43a5c-152">Dispatch</span><span class="sxs-lookup"><span data-stu-id="43a5c-152">Dispatch</span></span></td>
<td><span data-ttu-id="43a5c-153">La llamada se envía mediante el tiempo de ejecución de RPC Go a P</span><span class="sxs-lookup"><span data-stu-id="43a5c-153">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="43a5c-154">Para producir un error irrecuperable (mientras se ejecuta en el subproceso RPC): generar excepción; ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-154">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="43a5c-155">Para que se produzca un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-155">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-156">P</span><span class="sxs-lookup"><span data-stu-id="43a5c-156">P</span></span></td>
<td><span data-ttu-id="43a5c-157">Extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-157">Pull</span></span></td>
<td><span data-ttu-id="43a5c-158">Crear una extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-158">Make a pull</span></span>
<ul>
<li><span data-ttu-id="43a5c-159">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-159">On failure go to End</span></span></li>
<li><span data-ttu-id="43a5c-160">En caso de éxito y finalización sincrónica con bytes distintos de cero, lea Go to P</span><span class="sxs-lookup"><span data-stu-id="43a5c-160">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="43a5c-161">En caso de éxito y finalización sincrónica con cero bytes leídos (extracción nula) vaya a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-161">On success and synchronous completion with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="43a5c-162">En caso de éxito y finalización asincrónica (se devuelve ERROR_IO_PENDING) vaya a WP</span><span class="sxs-lookup"><span data-stu-id="43a5c-162">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="43a5c-163">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-163">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-164">WP</span><span class="sxs-lookup"><span data-stu-id="43a5c-164">WP</span></span></td>
<td><span data-ttu-id="43a5c-165">Esperar a la extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-165">Wait for Pull</span></span></td>
<td><span data-ttu-id="43a5c-166">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-166">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-167">En caso de error al obtener una finalización, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-167">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="43a5c-168">Si se recibe un error de <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , vaya a un</span><span class="sxs-lookup"><span data-stu-id="43a5c-168">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="43a5c-169">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con una lectura de bytes distinta de cero, vaya a P</span><span class="sxs-lookup"><span data-stu-id="43a5c-169">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="43a5c-170">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con cero bytes leídos (extracción nula) vaya a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-170">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="43a5c-171">Si se recibe un error, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-171">If a failure is received go to A</span></span></li>
</ul>
<span data-ttu-id="43a5c-172">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-172">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-173">A</span><span class="sxs-lookup"><span data-stu-id="43a5c-173">A</span></span></td>
<td><span data-ttu-id="43a5c-174">Anular la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-174">Abort the Call</span></span></td>
<td><span data-ttu-id="43a5c-175">Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-175">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-176">Comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-176">Comp</span></span></td>
<td><span data-ttu-id="43a5c-177">Completion</span><span class="sxs-lookup"><span data-stu-id="43a5c-177">Completion</span></span></td>
<td><span data-ttu-id="43a5c-178">Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-178">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-179">End</span><span class="sxs-lookup"><span data-stu-id="43a5c-179">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a><span data-ttu-id="43a5c-180">Canalización de salida</span><span class="sxs-lookup"><span data-stu-id="43a5c-180">OUT Pipe</span></span>

<span data-ttu-id="43a5c-181">Comportamiento del cliente</span><span class="sxs-lookup"><span data-stu-id="43a5c-181">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43a5c-182">Estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-182">State</span></span></th>
<th><span data-ttu-id="43a5c-183">Nombre de estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-183">State Name</span></span></th>
<th><span data-ttu-id="43a5c-184">Acción</span><span class="sxs-lookup"><span data-stu-id="43a5c-184">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43a5c-185">C</span><span class="sxs-lookup"><span data-stu-id="43a5c-185">C</span></span></td>
<td><span data-ttu-id="43a5c-186">Hacer la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-186">Make the call</span></span></td>
<td><span data-ttu-id="43a5c-187">Hacer que la RPC</span><span class="sxs-lookup"><span data-stu-id="43a5c-187">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="43a5c-188">En caso de éxito, vaya a P</span><span class="sxs-lookup"><span data-stu-id="43a5c-188">On success go to P</span></span></li>
<li><span data-ttu-id="43a5c-189">En caso de error, vaya a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-189">On failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="43a5c-190">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-190">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-191">P</span><span class="sxs-lookup"><span data-stu-id="43a5c-191">P</span></span></td>
<td><span data-ttu-id="43a5c-192">Extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-192">Pull</span></span></td>
<td><span data-ttu-id="43a5c-193">Crear una extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-193">Make a pull</span></span>
<ul>
<li><span data-ttu-id="43a5c-194">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-194">On failure go to End</span></span></li>
<li><span data-ttu-id="43a5c-195">En caso de éxito y finalización sincrónica con bytes distintos de cero, lea Go to P</span><span class="sxs-lookup"><span data-stu-id="43a5c-195">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="43a5c-196">En caso de éxito y finalización sincrónica con cero bytes leídos (extracción nula), vaya a WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-196">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="43a5c-197">En caso de éxito y finalización asincrónica (se devuelve ERROR_IO_PENDING) vaya a WP</span><span class="sxs-lookup"><span data-stu-id="43a5c-197">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="43a5c-198">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-198">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-199">WP</span><span class="sxs-lookup"><span data-stu-id="43a5c-199">WP</span></span></td>
<td><span data-ttu-id="43a5c-200">Esperar a la extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-200">Wait for Pull</span></span></td>
<td><span data-ttu-id="43a5c-201">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-201">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-202">En caso de error al obtener una finalización, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-202">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="43a5c-203">Si se recibe un error <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , ir a puede</span><span class="sxs-lookup"><span data-stu-id="43a5c-203">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="43a5c-204">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con una lectura de bytes distinta de cero, vaya a P</span><span class="sxs-lookup"><span data-stu-id="43a5c-204">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="43a5c-205">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con cero bytes leídos (extracción nula) vaya a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-205">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="43a5c-206">Si se recibe un error, puede</span><span class="sxs-lookup"><span data-stu-id="43a5c-206">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="43a5c-207">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-207">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-208">Poder</span><span class="sxs-lookup"><span data-stu-id="43a5c-208">Can</span></span></td>
<td><span data-ttu-id="43a5c-209">Cancelar la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-209">Cancel the Call</span></span></td>
<td><span data-ttu-id="43a5c-210">Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>ir a WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-210">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-211">WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-211">WComp</span></span></td>
<td><span data-ttu-id="43a5c-212">Esperar a que finalice</span><span class="sxs-lookup"><span data-stu-id="43a5c-212">Wait for Completion</span></span></td>
<td><span data-ttu-id="43a5c-213">Esperar notificación.</span><span class="sxs-lookup"><span data-stu-id="43a5c-213">Wait for notification.</span></span> <span data-ttu-id="43a5c-214">Se debe recibir la notificación de llamada completa.</span><span class="sxs-lookup"><span data-stu-id="43a5c-214">Call-complete notification should be received.</span></span><br/> <span data-ttu-id="43a5c-215">Ir a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-215">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-216">Comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-216">Comp</span></span></td>
<td><span data-ttu-id="43a5c-217">Completion</span><span class="sxs-lookup"><span data-stu-id="43a5c-217">Completion</span></span></td>
<td><span data-ttu-id="43a5c-218">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-218">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-219">End</span><span class="sxs-lookup"><span data-stu-id="43a5c-219">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="43a5c-220">Comportamiento del servidor</span><span class="sxs-lookup"><span data-stu-id="43a5c-220">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43a5c-221">Estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-221">State</span></span></th>
<th><span data-ttu-id="43a5c-222">Nombre de estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-222">State Name</span></span></th>
<th><span data-ttu-id="43a5c-223">Acción</span><span class="sxs-lookup"><span data-stu-id="43a5c-223">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43a5c-224">D</span><span class="sxs-lookup"><span data-stu-id="43a5c-224">D</span></span></td>
<td><span data-ttu-id="43a5c-225">Dispatch</span><span class="sxs-lookup"><span data-stu-id="43a5c-225">Dispatch</span></span></td>
<td><span data-ttu-id="43a5c-226">La llamada se envía mediante el tiempo de ejecución de RPC Go a P</span><span class="sxs-lookup"><span data-stu-id="43a5c-226">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="43a5c-227">Para producir un error irrecuperable (mientras se ejecuta en el subproceso RPC): generar excepción; ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-227">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="43a5c-228">Para que se produzca un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-228">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-229">P</span><span class="sxs-lookup"><span data-stu-id="43a5c-229">P</span></span></td>
<td><span data-ttu-id="43a5c-230">Inserción</span><span class="sxs-lookup"><span data-stu-id="43a5c-230">Push</span></span></td>
<td><span data-ttu-id="43a5c-231">Hacer una inserciones</span><span class="sxs-lookup"><span data-stu-id="43a5c-231">Make a push</span></span>
<ul>
<li><span data-ttu-id="43a5c-232">En caso de éxito, vaya a WP</span><span class="sxs-lookup"><span data-stu-id="43a5c-232">On success go to WP</span></span></li>
<li><span data-ttu-id="43a5c-233">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-233">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="43a5c-234">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-234">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-235">WP</span><span class="sxs-lookup"><span data-stu-id="43a5c-235">WP</span></span></td>
<td><span data-ttu-id="43a5c-236">Esperar a la inserciones</span><span class="sxs-lookup"><span data-stu-id="43a5c-236">Wait for Push</span></span></td>
<td><span data-ttu-id="43a5c-237">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-237">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-238">En caso de error al obtener una finalización, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-238">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="43a5c-239">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y es necesario enviar más datos, vaya a P</span><span class="sxs-lookup"><span data-stu-id="43a5c-239">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="43a5c-240">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y no es necesario enviar más datos, vaya a NP</span><span class="sxs-lookup"><span data-stu-id="43a5c-240">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="43a5c-241">Si se recibe un error de la comp.</span><span class="sxs-lookup"><span data-stu-id="43a5c-241">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="43a5c-242">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-242">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-243">NP</span><span class="sxs-lookup"><span data-stu-id="43a5c-243">NP</span></span></td>
<td><span data-ttu-id="43a5c-244">Inserciones nulas</span><span class="sxs-lookup"><span data-stu-id="43a5c-244">Null Push</span></span></td>
<td><span data-ttu-id="43a5c-245">Inserte 0 bytes</span><span class="sxs-lookup"><span data-stu-id="43a5c-245">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="43a5c-246">en caso de éxito, vaya a WNP</span><span class="sxs-lookup"><span data-stu-id="43a5c-246">on success go to WNP</span></span></li>
<li><span data-ttu-id="43a5c-247">en caso de error, vaya a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-247">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="43a5c-248">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-248">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-249">PERSISTENTE</span><span class="sxs-lookup"><span data-stu-id="43a5c-249">WNP</span></span></td>
<td><span data-ttu-id="43a5c-250">Esperar una inserciones nulas</span><span class="sxs-lookup"><span data-stu-id="43a5c-250">Wait for Null Push</span></span></td>
<td><span data-ttu-id="43a5c-251">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-251">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-252">En caso de error al obtener una finalización, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-252">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="43a5c-253">Si se recibe un error de la comp.</span><span class="sxs-lookup"><span data-stu-id="43a5c-253">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="43a5c-254">Si se ha recibido un éxito</span><span class="sxs-lookup"><span data-stu-id="43a5c-254">If a success is received go Comp</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-255">A</span><span class="sxs-lookup"><span data-stu-id="43a5c-255">A</span></span></td>
<td><span data-ttu-id="43a5c-256">Anular la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-256">Abort the Call</span></span></td>
<td><span data-ttu-id="43a5c-257">Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-257">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-258">Comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-258">Comp</span></span></td>
<td><span data-ttu-id="43a5c-259">Completion</span><span class="sxs-lookup"><span data-stu-id="43a5c-259">Completion</span></span></td>
<td><span data-ttu-id="43a5c-260">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-260">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-261">End</span><span class="sxs-lookup"><span data-stu-id="43a5c-261">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a><span data-ttu-id="43a5c-262">Canalización de salida</span><span class="sxs-lookup"><span data-stu-id="43a5c-262">IN-OUT Pipe</span></span>

<span data-ttu-id="43a5c-263">Comportamiento del cliente</span><span class="sxs-lookup"><span data-stu-id="43a5c-263">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43a5c-264">Estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-264">State</span></span></th>
<th><span data-ttu-id="43a5c-265">Nombre de estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-265">State Name</span></span></th>
<th><span data-ttu-id="43a5c-266">Acción</span><span class="sxs-lookup"><span data-stu-id="43a5c-266">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43a5c-267">C</span><span class="sxs-lookup"><span data-stu-id="43a5c-267">C</span></span></td>
<td><span data-ttu-id="43a5c-268">Hacer la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-268">Make the call</span></span></td>
<td><span data-ttu-id="43a5c-269">Hacer que la RPC</span><span class="sxs-lookup"><span data-stu-id="43a5c-269">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="43a5c-270">En caso de éxito, vaya a WS</span><span class="sxs-lookup"><span data-stu-id="43a5c-270">On success go to WS</span></span></li>
<li><span data-ttu-id="43a5c-271">Al final de la excepción</span><span class="sxs-lookup"><span data-stu-id="43a5c-271">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="43a5c-272">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-272">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-273">PS</span><span class="sxs-lookup"><span data-stu-id="43a5c-273">PS</span></span></td>
<td><span data-ttu-id="43a5c-274">Inserción</span><span class="sxs-lookup"><span data-stu-id="43a5c-274">Push</span></span></td>
<td><span data-ttu-id="43a5c-275">Hacer una inserciones</span><span class="sxs-lookup"><span data-stu-id="43a5c-275">Make a push</span></span>
<ul>
<li><span data-ttu-id="43a5c-276">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-276">On failure go to End</span></span></li>
<li><span data-ttu-id="43a5c-277">En caso de éxito, vaya a WS</span><span class="sxs-lookup"><span data-stu-id="43a5c-277">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="43a5c-278">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-278">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-279">WS</span><span class="sxs-lookup"><span data-stu-id="43a5c-279">WS</span></span></td>
<td><span data-ttu-id="43a5c-280">Esperar envío</span><span class="sxs-lookup"><span data-stu-id="43a5c-280">Wait for Send</span></span></td>
<td><span data-ttu-id="43a5c-281">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-281">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-282">Si se produce un error al recibir una notificación, puede</span><span class="sxs-lookup"><span data-stu-id="43a5c-282">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="43a5c-283">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y es necesario enviar más datos, vaya a PS</span><span class="sxs-lookup"><span data-stu-id="43a5c-283">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="43a5c-284">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y no es necesario enviar más datos, vaya a NP</span><span class="sxs-lookup"><span data-stu-id="43a5c-284">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="43a5c-285">Si se recibe un error <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="43a5c-285">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="43a5c-286">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-286">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-287">NP</span><span class="sxs-lookup"><span data-stu-id="43a5c-287">NP</span></span></td>
<td><span data-ttu-id="43a5c-288">Inserciones nulas</span><span class="sxs-lookup"><span data-stu-id="43a5c-288">Null Push</span></span></td>
<td><span data-ttu-id="43a5c-289">Inserte 0 bytes (inserciones nulas)</span><span class="sxs-lookup"><span data-stu-id="43a5c-289">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="43a5c-290">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-290">On failure go to End</span></span></li>
<li><span data-ttu-id="43a5c-291">En caso de éxito, vaya a PL</span><span class="sxs-lookup"><span data-stu-id="43a5c-291">On success go to PL</span></span></li>
</ul>
<span data-ttu-id="43a5c-292">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-292">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-293">PL</span><span class="sxs-lookup"><span data-stu-id="43a5c-293">PL</span></span></td>
<td><span data-ttu-id="43a5c-294">Extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-294">Pull</span></span></td>
<td><span data-ttu-id="43a5c-295">Crear una extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-295">Make a pull</span></span>
<ul>
<li><span data-ttu-id="43a5c-296">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-296">On failure go to End</span></span></li>
<li><span data-ttu-id="43a5c-297">En caso de éxito y finalización sincrónica con bytes distintos de cero, lea Go to PL</span><span class="sxs-lookup"><span data-stu-id="43a5c-297">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="43a5c-298">En caso de éxito y finalización sincrónica con cero bytes leídos (extracción nula), vaya a WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-298">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="43a5c-299">En caso de éxito y finalización asincrónica (se devuelve ERROR_IO_PENDING) vaya a WPL</span><span class="sxs-lookup"><span data-stu-id="43a5c-299">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="43a5c-300">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-300">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-301">WPL</span><span class="sxs-lookup"><span data-stu-id="43a5c-301">WPL</span></span></td>
<td><span data-ttu-id="43a5c-302">Esperar a la extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-302">Wait for Pull</span></span></td>
<td><span data-ttu-id="43a5c-303">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-303">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-304">En caso de error al obtener una finalización, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-304">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="43a5c-305">Si se recibe un error <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , ir a puede</span><span class="sxs-lookup"><span data-stu-id="43a5c-305">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="43a5c-306">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con bytes de lectura distintos de cero, vaya a PL</span><span class="sxs-lookup"><span data-stu-id="43a5c-306">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="43a5c-307">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con cero bytes leídos, vaya a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-307">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to Comp</span></span></li>
<li><span data-ttu-id="43a5c-308">Si se recibe un error, puede</span><span class="sxs-lookup"><span data-stu-id="43a5c-308">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="43a5c-309">En error: ir a</span><span class="sxs-lookup"><span data-stu-id="43a5c-309">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-310">Poder</span><span class="sxs-lookup"><span data-stu-id="43a5c-310">Can</span></span></td>
<td><span data-ttu-id="43a5c-311">Cancelar la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-311">Cancel the Call</span></span></td>
<td><span data-ttu-id="43a5c-312">Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>ir a WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-312">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-313">WComp</span><span class="sxs-lookup"><span data-stu-id="43a5c-313">WComp</span></span></td>
<td><span data-ttu-id="43a5c-314">Esperar a que finalice</span><span class="sxs-lookup"><span data-stu-id="43a5c-314">Wait for Completion</span></span></td>
<td><span data-ttu-id="43a5c-315">Esperar notificación.</span><span class="sxs-lookup"><span data-stu-id="43a5c-315">Wait for notification.</span></span> <span data-ttu-id="43a5c-316">Se debe recibir la notificación de CallComplete.</span><span class="sxs-lookup"><span data-stu-id="43a5c-316">CallComplete notification should be received.</span></span><br/> <span data-ttu-id="43a5c-317">Ir a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-317">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-318">Comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-318">Comp</span></span></td>
<td><span data-ttu-id="43a5c-319">Completion</span><span class="sxs-lookup"><span data-stu-id="43a5c-319">Completion</span></span></td>
<td><span data-ttu-id="43a5c-320">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-320">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-321">End</span><span class="sxs-lookup"><span data-stu-id="43a5c-321">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="43a5c-322">Comportamiento del servidor</span><span class="sxs-lookup"><span data-stu-id="43a5c-322">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43a5c-323">Estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-323">State</span></span></th>
<th><span data-ttu-id="43a5c-324">Nombre de estado</span><span class="sxs-lookup"><span data-stu-id="43a5c-324">State Name</span></span></th>
<th><span data-ttu-id="43a5c-325">Acción</span><span class="sxs-lookup"><span data-stu-id="43a5c-325">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43a5c-326">D</span><span class="sxs-lookup"><span data-stu-id="43a5c-326">D</span></span></td>
<td><span data-ttu-id="43a5c-327">Dispatch</span><span class="sxs-lookup"><span data-stu-id="43a5c-327">Dispatch</span></span></td>
<td><span data-ttu-id="43a5c-328">La llamada se envía mediante el runtimeGo de RPC a PL</span><span class="sxs-lookup"><span data-stu-id="43a5c-328">The call is dispatched by the RPC runtimeGo to PL</span></span><br/> <span data-ttu-id="43a5c-329">Para producir un error irrecuperable (mientras se ejecuta en el subproceso RPC): generar excepción; ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-329">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="43a5c-330">Para que se produzca un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-330">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-331">PL</span><span class="sxs-lookup"><span data-stu-id="43a5c-331">PL</span></span></td>
<td><span data-ttu-id="43a5c-332">Extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-332">Pull</span></span></td>
<td><span data-ttu-id="43a5c-333">Crear una extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-333">Make a pull</span></span>
<ul>
<li><span data-ttu-id="43a5c-334">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-334">On failure go to End</span></span></li>
<li><span data-ttu-id="43a5c-335">En caso de éxito y finalización sincrónica con bytes distintos de cero, lea Go to PL</span><span class="sxs-lookup"><span data-stu-id="43a5c-335">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="43a5c-336">En caso de éxito y finalización sincrónica con cero bytes leídos (extracción nula), vaya a PS</span><span class="sxs-lookup"><span data-stu-id="43a5c-336">On success and synchronous completion with zero bytes read (null pull) go to PS</span></span></li>
<li><span data-ttu-id="43a5c-337">En caso de éxito y finalización asincrónica (se devuelve ERROR_IO_PENDING) vaya a WPL</span><span class="sxs-lookup"><span data-stu-id="43a5c-337">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="43a5c-338">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-338">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-339">WPL</span><span class="sxs-lookup"><span data-stu-id="43a5c-339">WPL</span></span></td>
<td><span data-ttu-id="43a5c-340">Esperar a la extracción</span><span class="sxs-lookup"><span data-stu-id="43a5c-340">Wait for Pull</span></span></td>
<td><span data-ttu-id="43a5c-341">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-341">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-342">En caso de error al obtener una finalización, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-342">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="43a5c-343">Si se recibe un error de <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , vaya a un</span><span class="sxs-lookup"><span data-stu-id="43a5c-343">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="43a5c-344">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con bytes de lectura distintos de cero, vaya a PL</span><span class="sxs-lookup"><span data-stu-id="43a5c-344">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="43a5c-345">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con cero bytes leídos, vaya a PS</span><span class="sxs-lookup"><span data-stu-id="43a5c-345">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to PS</span></span></li>
<li><span data-ttu-id="43a5c-346">Si se recibe un error, vaya A</span><span class="sxs-lookup"><span data-stu-id="43a5c-346">If a failure is received go A</span></span></li>
</ul>
<span data-ttu-id="43a5c-347">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-347">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-348">PS</span><span class="sxs-lookup"><span data-stu-id="43a5c-348">PS</span></span></td>
<td><span data-ttu-id="43a5c-349">Inserción</span><span class="sxs-lookup"><span data-stu-id="43a5c-349">Push</span></span></td>
<td><span data-ttu-id="43a5c-350">Hacer una inserciones</span><span class="sxs-lookup"><span data-stu-id="43a5c-350">Make a push</span></span>
<ul>
<li><span data-ttu-id="43a5c-351">En caso de éxito, vaya a WPS</span><span class="sxs-lookup"><span data-stu-id="43a5c-351">On success go to WPS</span></span></li>
<li><span data-ttu-id="43a5c-352">En caso de error, ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-352">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="43a5c-353">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-353">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-354">WPS</span><span class="sxs-lookup"><span data-stu-id="43a5c-354">WPS</span></span></td>
<td><span data-ttu-id="43a5c-355">Esperar a la inserciones</span><span class="sxs-lookup"><span data-stu-id="43a5c-355">Wait for Push</span></span></td>
<td><span data-ttu-id="43a5c-356">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-356">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-357">En caso de error al obtener una finalización, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-357">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="43a5c-358">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y es necesario enviar más datos, vaya a PS</span><span class="sxs-lookup"><span data-stu-id="43a5c-358">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="43a5c-359">Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y no es necesario enviar más datos, vaya a NP</span><span class="sxs-lookup"><span data-stu-id="43a5c-359">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="43a5c-360">Si se recibe un error de la comp.</span><span class="sxs-lookup"><span data-stu-id="43a5c-360">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="43a5c-361">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-361">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-362">NP</span><span class="sxs-lookup"><span data-stu-id="43a5c-362">NP</span></span></td>
<td><span data-ttu-id="43a5c-363">Inserciones nulas</span><span class="sxs-lookup"><span data-stu-id="43a5c-363">Null Push</span></span></td>
<td><span data-ttu-id="43a5c-364">Inserte 0 bytes</span><span class="sxs-lookup"><span data-stu-id="43a5c-364">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="43a5c-365">en caso de éxito, vaya a WNP</span><span class="sxs-lookup"><span data-stu-id="43a5c-365">on success go to WNP</span></span></li>
<li><span data-ttu-id="43a5c-366">en caso de error, vaya a comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-366">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="43a5c-367">Para generar un error: vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-367">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-368">PERSISTENTE</span><span class="sxs-lookup"><span data-stu-id="43a5c-368">WNP</span></span></td>
<td><span data-ttu-id="43a5c-369">Esperar una inserciones nulas</span><span class="sxs-lookup"><span data-stu-id="43a5c-369">Wait for Null Push</span></span></td>
<td><span data-ttu-id="43a5c-370">Esperar notificación</span><span class="sxs-lookup"><span data-stu-id="43a5c-370">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="43a5c-371">En caso de error al obtener una finalización, vaya a</span><span class="sxs-lookup"><span data-stu-id="43a5c-371">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="43a5c-372">Si se recibe un error de la comp.</span><span class="sxs-lookup"><span data-stu-id="43a5c-372">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="43a5c-373">Si se ha recibido un éxito</span><span class="sxs-lookup"><span data-stu-id="43a5c-373">If a success is received go Comp</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-374">A</span><span class="sxs-lookup"><span data-stu-id="43a5c-374">A</span></span></td>
<td><span data-ttu-id="43a5c-375">Anular la llamada</span><span class="sxs-lookup"><span data-stu-id="43a5c-375">Abort the Call</span></span></td>
<td><span data-ttu-id="43a5c-376">Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-376">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43a5c-377">Comp</span><span class="sxs-lookup"><span data-stu-id="43a5c-377">Comp</span></span></td>
<td><span data-ttu-id="43a5c-378">Completion</span><span class="sxs-lookup"><span data-stu-id="43a5c-378">Completion</span></span></td>
<td><span data-ttu-id="43a5c-379">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir al final</span><span class="sxs-lookup"><span data-stu-id="43a5c-379">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43a5c-380">End</span><span class="sxs-lookup"><span data-stu-id="43a5c-380">End</span></span></td>


</tr>
</tbody>
</table>



 

 

 





