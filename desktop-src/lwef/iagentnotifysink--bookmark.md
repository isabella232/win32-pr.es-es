---
title: Marcador IAgentNotifySink
description: Marcador IAgentNotifySink
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02562b7cbf42c3445a25edc5071476da1b2d8dc53d80923ad875fddf09e5d31b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477101"
---
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink::Bookmark

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

Notifica a una aplicación cliente cuando se completa su marcador.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*
</dt> <dd>

Identificador del marcador que dio lugar a la activación del evento.

</dd> </dl>

Al incluir etiquetas de marcador en un [**método Speak,**](speak-method.md) puede realizar un seguimiento de cuándo se producen con este evento.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Etiquetas de salida de voz de Microsoft Agent](microsoft-agent-speech-output-tags.md)


 

 




