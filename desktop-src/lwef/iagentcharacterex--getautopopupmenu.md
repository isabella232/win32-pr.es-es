---
title: IAgentCharacterEx GetAutoPopupMenu
description: IAgentCharacterEx GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2b9e23f9c8d9f6fefcc7b2606ebd18ab31ff93c8f8f82c1faf692f92545662d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477983"
---
# <a name="iagentcharacterexgetautopopupmenu"></a>IAgentCharacterEx::GetAutoPopupMenu

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

Recupera si el servidor muestra automáticamente el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*
</dt> <dd>

Dirección de una variable que recibe **True si** el servidor de Microsoft Agent controla automáticamente la visualización del menú emergente del carácter y **False** si no es así.

</dd> </dl>

Cuando esta propiedad se establece en **False,** la aplicación debe mostrar el menú emergente mediante el método [**IAgentCharacterEx::ShowPopupMenu.**](iagentcharacterex--showpopupmenu.md)

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [ **IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 




