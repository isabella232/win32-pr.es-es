---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903641"
---
# <a name="iagentcharacterexshowpopupmenu"></a>IAgentCharacterEx::ShowPopupMenu

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

Muestra el menú emergente del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

La coordenada x del menú emergente del carácter, en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*sí*
</dt> <dd>

Coordenada y del menú emergente del carácter, en píxeles, con respecto al origen de la pantalla (parte superior izquierda).

</dd> </dl>

Al establecer [**IAgentCharacterEx:: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) en **false**, el servidor ya no muestra automáticamente el menú cuando se hace clic con el botón derecho en el carácter o el icono de la barra de tareas. Puede utilizar este método para mostrar el menú.

El menú se muestra hasta que el usuario selecciona un comando o muestra otro menú. Solo se puede mostrar un menú emergente a la vez; por lo tanto, las llamadas a este método cancelarán (quitará) el menú anterior.

Solo se debe llamar a este método cuando la aplicación cliente es el cliente activo del carácter; en caso contrario, se produce un error.

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)

 

 




