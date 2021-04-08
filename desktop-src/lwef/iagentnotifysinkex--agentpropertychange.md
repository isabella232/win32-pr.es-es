---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994239"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT AgentPropertyChange(
);
```

Notifica a una aplicación cliente cuando el usuario cambia la configuración de la propiedad de un agente de Microsoft.

-   No de devuelve ningún valor.

Cuando el usuario cambia la configuración de una propiedad de agente de Microsoft en la hoja de propiedades del agente de Microsoft, el servidor envía este evento a todos los clientes a menos que el servidor esté suspendido actualmente.

## <a name="see-also"></a>Consulte también

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




