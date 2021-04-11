---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149202"
---
# <a name="iagentcharacterexsethelpmodeon"></a>IAgentCharacterEx::SetHelpModeOn

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

Establece el modo de ayuda contextual en para el carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*
</dt> <dd>

Marca de modo de ayuda. Si este parámetro es **true**, el agente de Microsoft activa el modo de ayuda para el carácter.

</dd> </dl>

Cuando se establece esta propiedad en **true**, el puntero del mouse cambia a la imagen de ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter. Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md) y sale del modo de ayuda.

En el modo de ayuda, el servidor no envía los eventos [**click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)y [**Command**](command-event.md) , a menos que la propiedad [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) devuelva **true**. En ese caso, el servidor enviará el evento de **clic** (no saldrá del modo de ayuda), sino solo para el botón secundario del mouse para que pueda mostrar el menú emergente.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:: GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx:: HelpComplete**](iagentnotifysinkex--helpcomplete.md)


 

 