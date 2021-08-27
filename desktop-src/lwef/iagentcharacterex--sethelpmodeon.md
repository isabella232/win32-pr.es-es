---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacbdf9c0ea9737bb73ba7a99e0839e1435379e42536a82aa30c2ca034a28860
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062035"
---
# <a name="iagentcharacterexsethelpmodeon"></a>IAgentCharacterEx::SetHelpModeOn

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

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

Cuando se establece esta propiedad en **True**, el puntero del mouse cambia a la imagen de Ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter. Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) y sale del modo ayuda.

En el modo de Ayuda, el servidor no envía los eventos [**Click**](click-event.md), [**DragStart,**](/windows/desktop/lwef/dragstart-event) [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)y [**Command,**](command-event.md) a menos que la propiedad [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) devuelva **True.** En ese caso, el servidor enviará el evento **Click** (no sale del modo ayuda), pero solo para el botón derecho del mouse para que pueda mostrar el menú emergente.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)


 

 