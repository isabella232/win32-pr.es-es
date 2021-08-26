---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d7a0737428d20b297d83ac92c3ce6957dac0390c719c17b96a00983a0a57af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961495"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT AgentPropertyChange(
);
```

Notifica a una aplicación cliente cuando el usuario cambia una configuración de propiedad de Microsoft Agent.

-   No de devuelve ningún valor.

Cuando el usuario cambia una configuración de propiedad de Microsoft Agent en la hoja de propiedades de Microsoft Agent, el servidor envía este evento a todos los clientes a menos que el servidor esté suspendido actualmente.

## <a name="see-also"></a>Consulte también

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




