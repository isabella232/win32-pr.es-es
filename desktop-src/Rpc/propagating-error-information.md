---
title: Propagar información de errores
description: La propagación de la información de error extendida permite a los servidores que reciben un \_ \_ error de RPC S \ o a cualquier otro código de error, para permitir que el tiempo de ejecución de RPC propague la información recibida a sus llamadores.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903736"
---
# <a name="propagating-error-information"></a><span data-ttu-id="102c5-103">Propagar información de errores</span><span class="sxs-lookup"><span data-stu-id="102c5-103">Propagating Error Information</span></span>

<span data-ttu-id="102c5-104">La propagación de la información de error extendida permite a los servidores que reciben un \_ \_ \* error de RPC S, o cualquier otro código de error de este asunto, permitir que el tiempo de ejecución de RPC propague la información recibida a sus llamadores.</span><span class="sxs-lookup"><span data-stu-id="102c5-104">Propagating extended error information allows servers that receive an RPC\_S\_\* error, or any other error code for that matter, to allow the RPC run time to propagate the information it received to its callers.</span></span> <span data-ttu-id="102c5-105">Todo lo que debe hacer el servidor es llamar a [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) o [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) al encontrar un error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="102c5-105">All the server must do is call the [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) or [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) upon encountering a fatal error.</span></span> <span data-ttu-id="102c5-106">El tiempo de ejecución de RPC se encarga de encadenar la información de error extendida, si la hubiera, que provoca el error irrecuperable para notificar el error irrecuperable en sí, siempre que el código de error dado a **RpcRaiseException** o **RpcAsyncAbortCall** sea el mismo que el código de error que produce el error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="102c5-106">The RPC run time takes care of chaining the extended error information, if any, causing the fatal error to report the fatal error itself, as long as the error code given to **RpcRaiseException** or **RpcAsyncAbortCall** is the same as the error code causing the fatal error.</span></span>

 

 




