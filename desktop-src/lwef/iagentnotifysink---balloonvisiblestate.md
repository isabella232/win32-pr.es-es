---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704706"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a><span data-ttu-id="fc7ad-103">IAgentNotifySink::BalloonVisibleState</span><span class="sxs-lookup"><span data-stu-id="fc7ad-103">IAgentNotifySink::BalloonVisibleState</span></span>

<span data-ttu-id="fc7ad-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc7ad-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

<span data-ttu-id="fc7ad-105">Notifica a una aplicación cliente cuando cambia el estado de visibilidad del globo de palabras del carácter.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-105">Notifies a client application when the visibility state of the character's word balloon changes.</span></span>

-   <span data-ttu-id="fc7ad-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="fc7ad-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="fc7ad-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="fc7ad-108">Identificador del carácter cuyo estado de visibilidad del globo de palabras ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-108">Identifier of the character whose word balloon's visibility state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="fc7ad-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="fc7ad-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="fc7ad-110">Marca de visibilidad.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-110">Visibility flag.</span></span> <span data-ttu-id="fc7ad-111">Este valor booleano es **true** cuando el globo de palabras del carácter está visible; y **false** cuando se oculta.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-111">This Boolean value is **True** when character's word balloon becomes visible; and **False** when it becomes hidden.</span></span>

</dd> </dl>

<span data-ttu-id="fc7ad-112">Este evento se envía a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="fc7ad-112">This event is sent to all clients of the character.</span></span>

 

 




