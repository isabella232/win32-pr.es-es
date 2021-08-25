---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43a092ddd9c50ff7aacb0254c4773a43005759ab23b6682aaf6484d5aef4839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725785"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

IAgentNotifySink notifica a los clientes cuándo se producen determinados cambios de estado. Estas funciones también están disponibles en [IAgentNotifySinkEx.](iagentnotifysinkex.md)

**Métodos en orden de Vtable**



| IAgentNotifySink                                                      | Descripción                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Comando**](command-method.md)                                     | Se produce cuando el servidor procesa un comando definido por el cliente.                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | Se produce cuando un carácter se convierte o deja de ser activo de entrada.                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Se produce cuando cambia el estado **Visible** del carácter.                                   |
| [**Evento de clic**](click-event.md)                                    | Se produce cuando se hace clic en un carácter.                                                      |
| [**Evento DblClick**](dblclick-event.md)                              | Se produce cuando se hace doble clic en un carácter.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Se produce cuando un usuario comienza a arrastrar un carácter.                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | Se produce cuando un usuario deja de arrastrar un carácter.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Se produce cuando el servidor comienza a procesar un [**objeto Request.**](/windows/desktop/lwef/the-request-object)    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | Se produce cuando el servidor completa el procesamiento de un [**objeto Request.**](/windows/desktop/lwef/the-request-object) |
| [**Marcador**](iagentnotifysink--bookmark.md)                        | Se produce cuando el servidor procesa un marcador.                                             |
| [**Inactivo**](iagentnotifysink--idle.md)                                | Se produce cuando el servidor inicia o finaliza el procesamiento inactivo.                                   |
| [**Mover**](iagentnotifysink--move.md)                                | Se produce cuando se ha movido un carácter.                                                  |
| [**Size**](iagentnotifysink---size.md)                               | Se produce cuando se ha cambiado el tamaño de un carácter.                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Se produce cuando cambia el estado de visibilidad de un globo de palabras de un carácter.                  |



 

Los eventos IAgentNotifySink::Restart e IAgentNotifySink::Shutdown, admitidos en versiones anteriores de Microsoft Agent, ahora están obsoletos. Aunque se admite por compatibilidad con versiones anteriores, el servidor ya no envía estos eventos.

 

 