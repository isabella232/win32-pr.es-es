---
title: IAgentNotifySink marcador)
description: IAgentNotifySink marcador)
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774845"
---
# <a name="iagentnotifysinkbookmark"></a><span data-ttu-id="62186-103">IAgentNotifySink:: Bookmark</span><span class="sxs-lookup"><span data-stu-id="62186-103">IAgentNotifySink::Bookmark</span></span>

<span data-ttu-id="62186-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62186-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

<span data-ttu-id="62186-105">Notifica a una aplicación cliente cuando se completa su marcador.</span><span class="sxs-lookup"><span data-stu-id="62186-105">Notifies a client application when its bookmark completes.</span></span>

-   <span data-ttu-id="62186-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="62186-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="62186-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span><span class="sxs-lookup"><span data-stu-id="62186-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span></span>
</dt> <dd>

<span data-ttu-id="62186-108">Identificador del marcador que resultó en desencadenar el evento.</span><span class="sxs-lookup"><span data-stu-id="62186-108">Identifier of the bookmark that resulted in triggering the event.</span></span>

</dd> </dl>

<span data-ttu-id="62186-109">Al incluir etiquetas de marcador en un método [**Speak**](speak-method.md) , puede realizar un seguimiento cuando se producen con este evento.</span><span class="sxs-lookup"><span data-stu-id="62186-109">When you include bookmark tags in a [**Speak**](speak-method.md) method, you can track when they occur with this event.</span></span>

## <a name="see-also"></a><span data-ttu-id="62186-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="62186-110">See Also</span></span>

<span data-ttu-id="62186-111">[**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [etiquetas de salida de voz del agente de Microsoft](microsoft-agent-speech-output-tags.md)</span><span class="sxs-lookup"><span data-stu-id="62186-111">[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md)</span></span>


 

 




