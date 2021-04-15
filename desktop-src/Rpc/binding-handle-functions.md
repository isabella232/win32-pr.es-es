---
title: Funciones de identificador de enlace
description: La tabla siguiente contiene la lista de rutinas en tiempo de ejecución de RPC que operan en los identificadores de enlace y especifica el tipo de identificador de enlace permitido.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676109"
---
# <a name="binding-handle-functions"></a><span data-ttu-id="5761f-103">Funciones de identificador de enlace</span><span class="sxs-lookup"><span data-stu-id="5761f-103">Binding Handle Functions</span></span>

<span data-ttu-id="5761f-104">La tabla siguiente contiene la lista de rutinas en tiempo de ejecución de RPC que operan en los identificadores de enlace y especifica el tipo de identificador de enlace permitido.</span><span class="sxs-lookup"><span data-stu-id="5761f-104">The following table contains the list of RPC run-time routines that operate on binding handles and specifies the type of binding handle allowed.</span></span>



| <span data-ttu-id="5761f-105">Rutina</span><span class="sxs-lookup"><span data-stu-id="5761f-105">Routine</span></span>                                                            | <span data-ttu-id="5761f-106">Argumento de entrada</span><span class="sxs-lookup"><span data-stu-id="5761f-106">Input argument</span></span>   | <span data-ttu-id="5761f-107">Argumento de salida</span><span class="sxs-lookup"><span data-stu-id="5761f-107">Output argument</span></span> |
|--------------------------------------------------------------------|------------------|-----------------|
| [<span data-ttu-id="5761f-108">**RpcBindingCopy**</span><span class="sxs-lookup"><span data-stu-id="5761f-108">**RpcBindingCopy**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | <span data-ttu-id="5761f-109">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-109">Server</span></span>           | <span data-ttu-id="5761f-110">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-110">Server</span></span>          |
| [<span data-ttu-id="5761f-111">**RpcBindingFree**</span><span class="sxs-lookup"><span data-stu-id="5761f-111">**RpcBindingFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | <span data-ttu-id="5761f-112">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-112">Server</span></span>           | <span data-ttu-id="5761f-113">None</span><span class="sxs-lookup"><span data-stu-id="5761f-113">None</span></span>            |
| [<span data-ttu-id="5761f-114">**RpcBindingFromStringBinding**</span><span class="sxs-lookup"><span data-stu-id="5761f-114">**RpcBindingFromStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | <span data-ttu-id="5761f-115">None</span><span class="sxs-lookup"><span data-stu-id="5761f-115">None</span></span>             | <span data-ttu-id="5761f-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-116">Server</span></span>          |
| [<span data-ttu-id="5761f-117">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="5761f-117">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | <span data-ttu-id="5761f-118">Remoto</span><span class="sxs-lookup"><span data-stu-id="5761f-118">Client</span></span>           | <span data-ttu-id="5761f-119">None</span><span class="sxs-lookup"><span data-stu-id="5761f-119">None</span></span>            |
| [<span data-ttu-id="5761f-120">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="5761f-120">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | <span data-ttu-id="5761f-121">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-121">Server</span></span>           | <span data-ttu-id="5761f-122">None</span><span class="sxs-lookup"><span data-stu-id="5761f-122">None</span></span>            |
| [<span data-ttu-id="5761f-123">**RpcBindingInqObject**</span><span class="sxs-lookup"><span data-stu-id="5761f-123">**RpcBindingInqObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | <span data-ttu-id="5761f-124">Servidor o cliente</span><span class="sxs-lookup"><span data-stu-id="5761f-124">Server or client</span></span> | <span data-ttu-id="5761f-125">None</span><span class="sxs-lookup"><span data-stu-id="5761f-125">None</span></span>            |
| [<span data-ttu-id="5761f-126">**RpcBindingReset**</span><span class="sxs-lookup"><span data-stu-id="5761f-126">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | <span data-ttu-id="5761f-127">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-127">Server</span></span>           | <span data-ttu-id="5761f-128">None</span><span class="sxs-lookup"><span data-stu-id="5761f-128">None</span></span>            |
| [<span data-ttu-id="5761f-129">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="5761f-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | <span data-ttu-id="5761f-130">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-130">Server</span></span>           | <span data-ttu-id="5761f-131">None</span><span class="sxs-lookup"><span data-stu-id="5761f-131">None</span></span>            |
| [<span data-ttu-id="5761f-132">**RpcBindingSetObject**</span><span class="sxs-lookup"><span data-stu-id="5761f-132">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | <span data-ttu-id="5761f-133">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-133">Server</span></span>           | <span data-ttu-id="5761f-134">None</span><span class="sxs-lookup"><span data-stu-id="5761f-134">None</span></span>            |
| [<span data-ttu-id="5761f-135">**RpcBindingToStringBinding**</span><span class="sxs-lookup"><span data-stu-id="5761f-135">**RpcBindingToStringBinding**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | <span data-ttu-id="5761f-136">Servidor o cliente</span><span class="sxs-lookup"><span data-stu-id="5761f-136">Server or client</span></span> | <span data-ttu-id="5761f-137">None</span><span class="sxs-lookup"><span data-stu-id="5761f-137">None</span></span>            |
| [<span data-ttu-id="5761f-138">**RpcBindingVectorFree**</span><span class="sxs-lookup"><span data-stu-id="5761f-138">**RpcBindingVectorFree**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | <span data-ttu-id="5761f-139">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-139">Server</span></span>           | <span data-ttu-id="5761f-140">None</span><span class="sxs-lookup"><span data-stu-id="5761f-140">None</span></span>            |
| [<span data-ttu-id="5761f-141">**RpcNsBindingExport**</span><span class="sxs-lookup"><span data-stu-id="5761f-141">**RpcNsBindingExport**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | <span data-ttu-id="5761f-142">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-142">Server</span></span>           | <span data-ttu-id="5761f-143">None</span><span class="sxs-lookup"><span data-stu-id="5761f-143">None</span></span>            |
| [<span data-ttu-id="5761f-144">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="5761f-144">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | <span data-ttu-id="5761f-145">None</span><span class="sxs-lookup"><span data-stu-id="5761f-145">None</span></span>             | <span data-ttu-id="5761f-146">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-146">Server</span></span>          |
| [<span data-ttu-id="5761f-147">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="5761f-147">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | <span data-ttu-id="5761f-148">None</span><span class="sxs-lookup"><span data-stu-id="5761f-148">None</span></span>             | <span data-ttu-id="5761f-149">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-149">Server</span></span>          |
| [<span data-ttu-id="5761f-150">**RpcNsBindingSelect**</span><span class="sxs-lookup"><span data-stu-id="5761f-150">**RpcNsBindingSelect**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | <span data-ttu-id="5761f-151">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-151">Server</span></span>           | <span data-ttu-id="5761f-152">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-152">Server</span></span>          |
| [<span data-ttu-id="5761f-153">**RpcServerInqBindings**</span><span class="sxs-lookup"><span data-stu-id="5761f-153">**RpcServerInqBindings**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | <span data-ttu-id="5761f-154">None</span><span class="sxs-lookup"><span data-stu-id="5761f-154">None</span></span>             | <span data-ttu-id="5761f-155">Servidor</span><span class="sxs-lookup"><span data-stu-id="5761f-155">Server</span></span>          |



 

 

 




