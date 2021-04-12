---
title: Tamaño de IAgentNotifySink
description: Tamaño de IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532290"
---
# <a name="iagentnotifysinksize"></a><span data-ttu-id="c5767-103">IAgentNotifySink:: Size</span><span class="sxs-lookup"><span data-stu-id="c5767-103">IAgentNotifySink::Size</span></span>

<span data-ttu-id="c5767-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c5767-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

<span data-ttu-id="c5767-105">Notifica a una aplicación cliente cuando se ha cambiado el tamaño del carácter.</span><span class="sxs-lookup"><span data-stu-id="c5767-105">Notifies a client application when the character has been resized.</span></span>

-   <span data-ttu-id="c5767-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c5767-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="c5767-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="c5767-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="c5767-108">Identificador del carácter cuyo tamaño se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="c5767-108">Identifier of the character that has been resized.</span></span>

</dd> <dt>

<span data-ttu-id="c5767-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="c5767-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="c5767-110">Ancho del fotograma de animación del carácter en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c5767-110">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="c5767-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="c5767-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="c5767-112">Alto del fotograma de animación del carácter en píxeles.</span><span class="sxs-lookup"><span data-stu-id="c5767-112">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="c5767-113">Este evento se envía a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="c5767-113">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5767-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c5767-114">See Also</span></span>

<span data-ttu-id="c5767-115">[**IAgentCharacter::**](iagentcharacter--getsize.md), [ **IAgentCharacter:: setSize**](iagentcharacter--setsize.md)</span><span class="sxs-lookup"><span data-stu-id="c5767-115">[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md), [**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)</span></span>


 

 




