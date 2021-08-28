---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67d01edae103bad10eb085c4bfd1f5ce559bf26ab030816d241367ec3c13763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105463"
---
# <a name="iagentcharacterexshowpopupmenu"></a>IAgentCharacterEx::ShowPopupMenu

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

Muestra el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x del menú emergente del carácter en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada y del menú emergente del carácter en píxeles, en relación con el origen de la pantalla (parte superior izquierda).

</dd> </dl>

Al establecer [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) en **False,** el servidor ya no muestra automáticamente el menú cuando se hace clic con el botón derecho en el carácter o en el icono de la barra de tareas. Puede usar este método para mostrar el menú.

El menú se muestra hasta que el usuario selecciona un comando o muestra otro menú. Solo se puede mostrar un menú emergente a la vez; Por lo tanto, las llamadas a este método cancelarán (quitarán) el menú anterior.

Solo se debe llamar a este método cuando la aplicación cliente es el cliente activo del carácter; de lo contrario, se produce un error.

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)

 

 




