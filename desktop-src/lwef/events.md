---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077674"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

IAgentNotifySink notifica a los clientes cuando se producen determinados cambios de estado. Estas funciones también están disponibles en [IAgentNotifySinkEx](iagentnotifysinkex.md).

**Métodos en orden de Vtable**



| IAgentNotifySink                                                      | Descripción                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Command**](command-method.md)                                     | Se produce cuando el servidor procesa un comando definido por el cliente.                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | Se produce cuando un carácter entra o deja de ser de entrada-activo.                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Se produce cuando cambia el estado **visible** del carácter.                                   |
| [**Evento de clic**](click-event.md)                                    | Se produce cuando se hace clic en un carácter.                                                      |
| [**Evento DblClick**](dblclick-event.md)                              | Se produce cuando se hace doble clic en un carácter.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Se produce cuando un usuario comienza a arrastrar un carácter.                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | Se produce cuando un usuario deja de arrastrar un carácter.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Se produce cuando el servidor comienza a procesar un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | Se produce cuando el servidor finaliza el procesamiento de un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) . |
| [**Marcador**](iagentnotifysink--bookmark.md)                        | Se produce cuando el servidor procesa un marcador.                                             |
| [**Activos**](iagentnotifysink--idle.md)                                | Se produce cuando el servidor inicia o finaliza el procesamiento inactivo.                                   |
| [**Move**](iagentnotifysink--move.md)                                | Se produce cuando se mueve un carácter.                                                  |
| [**Tamaño**](iagentnotifysink---size.md)                               | Se produce cuando se ha cambiado el tamaño de un carácter.                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Se produce cuando cambia el estado de visibilidad del globo de palabras de un carácter.                  |



 

Los eventos IAgentNotifySink:: restart y IAgentNotifySink:: shutdown, que se admiten en versiones anteriores de Microsoft Agent, ahora están obsoletos. Aunque se admite por compatibilidad con versiones anteriores, el servidor ya no envía estos eventos.

 

 