---
title: RPC asincrónico a través del protocolo Named-Pipe
description: Si usa canalizaciones con nombre (ncacn \_ NP) como protocolo de transporte, debe evitar permitir un gran número de llamadas pendientes de inactividad en el servidor.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995553"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a><span data-ttu-id="2ec52-103">RPC asincrónico a través del protocolo Named-Pipe</span><span class="sxs-lookup"><span data-stu-id="2ec52-103">Asynchronous RPC over the Named-Pipe Protocol</span></span>

<span data-ttu-id="2ec52-104">Si usa canalizaciones con nombre ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) como protocolo de transporte, debe evitar permitir un gran número de llamadas pendientes de inactividad en el servidor.</span><span class="sxs-lookup"><span data-stu-id="2ec52-104">If you use named pipes ([**ncacn\_np**](/windows/desktop/Midl/ncacn-np)) as your transport protocol, you should avoid allowing a large number of idle pending calls on the server.</span></span> <span data-ttu-id="2ec52-105">Con las canalizaciones con nombre, cada cliente que espera una respuesta tendrá una canalización con nombre pendiente leída en el servidor, cada una de las cuales requiere una determinada cantidad de memoria del kernel.</span><span class="sxs-lookup"><span data-stu-id="2ec52-105">With named pipes, each client waiting for a reply will have a pending named pipe read on the server, each of which requires a certain amount of kernel memory.</span></span>

<span data-ttu-id="2ec52-106">Por ejemplo, no querrá usar una llamada de notificación para nuevos mensajes de correo electrónico con el transporte de canalización con nombre, ya que dicha llamada permanecerá pendiente incluso cuando los clientes estén inactivos y se podría agotar la memoria del kernel.</span><span class="sxs-lookup"><span data-stu-id="2ec52-106">For example, you would not want to use a notification call for new e-mail with the named-pipe transport, because such a call would remain pending even when clients are idle, and kernel memory could be depleted.</span></span> <span data-ttu-id="2ec52-107">Tenga en cuenta que esto no es un problema con los demás protocolos orientados a la conexión, como [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).</span><span class="sxs-lookup"><span data-stu-id="2ec52-107">Note that this is not a problem with the other connection-oriented protocols, such as [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp).</span></span>

<span data-ttu-id="2ec52-108">Dado que las canalizaciones con nombre son un protocolo de transporte, la aplicación puede usarlas especificando [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) como protocolo en un enlace de cadenas.</span><span class="sxs-lookup"><span data-stu-id="2ec52-108">Since named pipes are a transport protocol, your application can use them by specifying [**ncacn\_np**](/windows/desktop/Midl/ncacn-np) as the protocol in a string binding.</span></span> <span data-ttu-id="2ec52-109">Para obtener más información sobre las canalizaciones con nombre, vea [canalizaciones con nombre](/windows/desktop/ipc/named-pipes).</span><span class="sxs-lookup"><span data-stu-id="2ec52-109">For more information on named pipes, see [Named Pipes](/windows/desktop/ipc/named-pipes).</span></span> <span data-ttu-id="2ec52-110">Para obtener más información sobre cómo crear enlaces de cadena, vea [usar enlaces de cadena](finding-server-host-systems.md).</span><span class="sxs-lookup"><span data-stu-id="2ec52-110">For details on creating string bindings, see [Using String Bindings](finding-server-host-systems.md).</span></span>

 

 