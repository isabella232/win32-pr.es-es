---
title: IAgentNotifySink inactivo
description: IAgentNotifySink inactivo
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704775"
---
# <a name="iagentnotifysinkidle"></a>IAgentNotifySink:: idle

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

Notifica a una aplicación cliente cuando ha cambiado el estado de **ralentí** de un carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador de la solicitud iniciada.

</dd> <dt>

<span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bInicio*
</dt> <dd>

Marca de inicio. Este valor booleano es **true** cuando el carácter comienza a ralentí y **false** cuando detiene el ralentí.

</dd> </dl>

Este evento le permite realizar un seguimiento cuando el servidor de agente de Microsoft inicia o detiene el procesamiento inactivo de un carácter.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: GetIdleOn**](iagentcharacter--getidleon.md), [ **IAgentCharacter:: SetIdleOn**](iagentcharacter--setidleon.md)


 

 




