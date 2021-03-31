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
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink:: Bookmark

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

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

Identificador del marcador que resultó en desencadenar el evento.

</dd> </dl>

Al incluir etiquetas de marcador en un método [**Speak**](speak-method.md) , puede realizar un seguimiento cuando se producen con este evento.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [etiquetas de salida de voz del agente de Microsoft](microsoft-agent-speech-output-tags.md)


 

 




