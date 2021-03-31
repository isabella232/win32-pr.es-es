---
title: Controlar llamadas asincrónicas
description: La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro. El servidor debe realizar un seguimiento de este identificador y usarlo para enviar la respuesta cuando finalice la llamada asincrónica al procedimiento remoto.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418813"
---
# <a name="handling-asynchronous-calls"></a><span data-ttu-id="918a6-104">Controlar llamadas asincrónicas</span><span class="sxs-lookup"><span data-stu-id="918a6-104">Handling Asynchronous Calls</span></span>

<span data-ttu-id="918a6-105">La rutina de administrador de una función asincrónica siempre recibe el identificador asincrónico como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="918a6-105">The manager routine of an asynchronous function always receives the asynchronous handle as the first parameter.</span></span> <span data-ttu-id="918a6-106">El servidor debe realizar un seguimiento de este identificador y usarlo para enviar la respuesta cuando finalice la llamada asincrónica al procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="918a6-106">The server must keep track of this handle and use it to send the reply when the asynchronous remote procedure call finishes.</span></span>

<span data-ttu-id="918a6-107">Si el servidor necesita anular una RPC asincrónica, llama a [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span><span class="sxs-lookup"><span data-stu-id="918a6-107">If the server needs to abort an asynchronous RPC, it calls [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall).</span></span> <span data-ttu-id="918a6-108">Esta función realiza la misma limpieza de servidor que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) y propaga un código de excepción (proporcionado por la aplicación de servidor) al cliente, salvo que no realiza la serialización de los argumentos de salida.</span><span class="sxs-lookup"><span data-stu-id="918a6-108">This function performs the same server-side cleanup as [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) and propagates an exception code (provided by the server application) back to the client, except that it does not perform marshalling of the out arguments.</span></span>

<span data-ttu-id="918a6-109">Para obtener un ejemplo de un procedimiento asincrónico, consulte [enviar la respuesta asincrónica](sending-the-asynchronous-reply.md).</span><span class="sxs-lookup"><span data-stu-id="918a6-109">For an example of an asynchronous procedure, see [Sending the Asynchronous Reply](sending-the-asynchronous-reply.md).</span></span>

 

 




