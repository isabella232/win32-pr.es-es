---
title: Registro de IAgent
description: Registro de IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903522"
---
# <a name="iagentregister"></a><span data-ttu-id="c2cf9-103">IAgent:: Register</span><span class="sxs-lookup"><span data-stu-id="c2cf9-103">IAgent::Register</span></span>

<span data-ttu-id="c2cf9-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c2cf9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

<span data-ttu-id="c2cf9-105">Registra un receptor de notificaciones para la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c2cf9-105">Registers a notification sink for the client application.</span></span>

-   <span data-ttu-id="c2cf9-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c2cf9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c2cf9-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="c2cf9-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="c2cf9-108">Dirección de [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) para la interfaz del receptor de notificaciones.</span><span class="sxs-lookup"><span data-stu-id="c2cf9-108">Address of [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) for your notification sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="c2cf9-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span><span class="sxs-lookup"><span data-stu-id="c2cf9-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="c2cf9-110">Dirección del identificador del receptor de notificaciones (se usa para anular el registro del receptor de notificaciones).</span><span class="sxs-lookup"><span data-stu-id="c2cf9-110">Address of notification sink ID (used to unregister the notification sink).</span></span>

</dd> </dl>

<span data-ttu-id="c2cf9-111">Debe registrar el receptor de notificaciones (también conocido como receptor de notificaciones o receptores de eventos) para recibir eventos del servidor de agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c2cf9-111">You need to register your notification sink (also known as a notify sink or event sink) to receive events from the Microsoft Agent server.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2cf9-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c2cf9-112">See Also</span></span>

[<span data-ttu-id="c2cf9-113">**IAgent:: unregister**</span><span class="sxs-lookup"><span data-stu-id="c2cf9-113">**IAgent::Unregister**</span></span>](iagent--unregister.md)


 

 




