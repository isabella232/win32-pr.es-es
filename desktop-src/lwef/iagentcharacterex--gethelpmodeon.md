---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb78cf535fbfd7e28ab797c887c8e1548d3fd18dce03fb6b64d888c7e304c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750793"
---
# <a name="iagentcharacterexgethelpmodeon"></a>IAgentCharacterEx::GetHelpModeOn

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Recupera si el modo de Ayuda contextual está en para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*
</dt> <dd>

Dirección de una variable que recibe **True si** el modo de Ayuda está en para el carácter y **False** si no es así.

</dd> </dl>

Cuando esta propiedad se establece en **True,** el puntero del mouse cambia a la imagen de Ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter. Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) y sale del modo ayuda.

En el modo ayuda, el servidor no envía los eventos [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::D ragStart,**](iagentnotifysink--dragstart.md) [**IAgentNotifySink::D ragComplete**](iagentnotifysink--dragcomplete.md)e [**IAgentNotifySink::Command,**](iagentnotifysink--command.md) a menos que la propiedad [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) devuelva **True.** En ese caso, el servidor enviará el evento **IAgentNotifySink::Click** (no sale del modo ayuda), pero solo para que el botón derecho del mouse le permita mostrar el menú emergente.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)


 

 




