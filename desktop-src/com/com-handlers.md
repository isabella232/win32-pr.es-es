---
title: Controladores COM
description: El propósito de los controladores COM es proporcionar algún 0034; Smart \ 0034; código en el espacio de direcciones del cliente que puede optimizar las llamadas entre un cliente y un servidor. Los controladores pueden invalidar algunas interfaces mientras delegan a otras personas directamente en el servidor (a través del proxy).
ms.assetid: 390b0228-4c52-453c-82d8-466600d23a04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb66a94942cd46424339cfffbde925f62e20e5f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714123"
---
# <a name="com-handlers"></a><span data-ttu-id="2be61-104">Controladores COM</span><span class="sxs-lookup"><span data-stu-id="2be61-104">COM Handlers</span></span>

<span data-ttu-id="2be61-105">El propósito de los controladores COM es proporcionar código "inteligente" en el espacio de direcciones del cliente que puede optimizar las llamadas entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="2be61-105">The purpose of COM handlers is to provide some "smart" code in the client address space that can optimize calls between a client and server.</span></span> <span data-ttu-id="2be61-106">Los controladores pueden invalidar algunas interfaces mientras delegan a otras personas directamente en el servidor (a través del proxy).</span><span class="sxs-lookup"><span data-stu-id="2be61-106">Handlers can override some interfaces while delegating others directly to the server (through the proxy).</span></span>

<span data-ttu-id="2be61-107">Hay dos tipos de controladores COM:</span><span class="sxs-lookup"><span data-stu-id="2be61-107">There are two types of COM handlers:</span></span>

-   <span data-ttu-id="2be61-108">[El controlador OLE](the-ole-handler.md) es un archivo dll pesado que proporciona servicios importantes para la vinculación y la incrustación.</span><span class="sxs-lookup"><span data-stu-id="2be61-108">[The OLE handler](the-ole-handler.md) is a heavyweight DLL that provides important services for linking and embedding.</span></span> <span data-ttu-id="2be61-109">Normalmente se crea antes de que se inicie el servidor y se inicializa para que el servidor se active cuando el objeto incrustado entra en el estado de ejecución.</span><span class="sxs-lookup"><span data-stu-id="2be61-109">It is usually created before the server is launched and is initialized so that the server is activated when the embedded object enters the running state.</span></span>
-   <span data-ttu-id="2be61-110">[El controlador del lado cliente ligero](the-lightweight-client-side-handler.md) se puede crear para cualquier propósito, puede ser muy pequeño y no se puede crear antes que el servidor.</span><span class="sxs-lookup"><span data-stu-id="2be61-110">[The lightweight client-side handler](the-lightweight-client-side-handler.md) can be created for any purpose, can be very small, and cannot be created before the server.</span></span>

 

 




