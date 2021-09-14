---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072372"
---
# <a name="iagentcharacterexsethelpmodeon"></a>IAgentCharacterEx::SetHelpModeOn

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

Establece el modo de Ayuda contextual en para el carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*
</dt> <dd>

Marca del modo de ayuda. Si este parámetro es **True,** Microsoft Agent activa el modo de Ayuda para el carácter.

</dd> </dl>

Al establecer esta propiedad en **True,** el puntero del mouse cambia a la imagen de Ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter. Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) y sale del modo de Ayuda.

En el modo de Ayuda, el servidor no envía los eventos [**Click**](click-event.md), [**DragStart,**](/windows/desktop/lwef/dragstart-event) [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)y [**Command,**](command-event.md) a menos que la propiedad [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) devuelva **True.** En ese caso, el servidor enviará el evento **Click** (no sale del modo de Ayuda), pero solo para el botón derecho del mouse para que pueda mostrar el menú emergente.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)


 

 