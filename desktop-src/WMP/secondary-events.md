---
title: Eventos secundarios
description: Eventos secundarios
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Aspectos de Windows Media Player, eventos secundarios
- máscaras, eventos secundarios
- eventos, secundarios
- escribir código para máscaras, eventos secundarios
- eventos secundarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486959"
---
# <a name="secondary-events"></a>Eventos secundarios

Puede determinar qué otros eventos están teniendo lugar cuando se desencadena un evento específico. Por ejemplo, cuando se hace clic en un botón del mouse, es posible que desee saber si la tecla ALT estaba presionada al mismo tiempo.

## <a name="event-attributes"></a>Atributos de eventos

Se admiten los siguientes atributos de evento para las máscaras:

-   **altKey**
-   **botón**
-   **clientX**
-   **cliente de**
-   **ctrlKey**
-   **fromElement**
-   **offsetX**
-   **desplazamiento**
-   **screenX**
-   **pantalla**
-   **shiftKey**
-   **srcElement**
-   **toElement**
-   **x**
-   **y**
-   **keyCode**

Para obtener más información sobre estos atributos, vea la [referencia de programación](skin-programming-reference.md)de la máscara.

## <a name="using-secondary-events"></a>Usar eventos secundarios

Solo se pueden procesar atributos de evento en el código JScript. Debe usar la siguiente sintaxis:


```C++
event.eventattributename
```



*eventattributename* es el nombre del atributo de evento. Por ejemplo, para determinar si se presionó la tecla ALT durante un evento de clic, podría usar las líneas siguientes en el código JScript:


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Controlar eventos**](handling-events.md)
</dt> </dl>

 

 




