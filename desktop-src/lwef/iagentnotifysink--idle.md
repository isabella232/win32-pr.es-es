---
title: IAgentNotifySink Idle
description: IAgentNotifySink Idle
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8263bd9bc62d4fccfad74b18b189c6e4bae426245dd3d4d6a46c826ebacf498d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105190"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink::Idle

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Notifica a una aplicación cliente cuándo ha cambiado el estado **de idling de** un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador de la solicitud que se inició.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*
</dt> <dd>

Marca de inicio. Este valor booleano **es True cuando** el carácter comienza el idling y **False** cuando se detiene el idling.

</dd> </dl>

Este evento le permite realizar un seguimiento de cuándo el servidor de Microsoft Agent inicia o detiene el procesamiento inactivo de un carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




