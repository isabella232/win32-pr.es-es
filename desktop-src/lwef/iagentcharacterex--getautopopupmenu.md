---
title: IAgentCharacterEx GetAutoPopupMenu
description: IAgentCharacterEx GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994430"
---
# <a name="iagentcharacterexgetautopopupmenu"></a>IAgentCharacterEx::GetAutoPopupMenu

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

Recupera si el servidor muestra automáticamente el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*
</dt> <dd>

Dirección de una variable que recibe **true** si el servidor de agente de Microsoft controla automáticamente la visualización del menú emergente del carácter y **false** en caso contrario.

</dd> </dl>

Cuando esta propiedad está establecida en **false**, la aplicación debe mostrar el menú emergente con el método [**IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) .

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [ **IAgentCharacterEx:: ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 




