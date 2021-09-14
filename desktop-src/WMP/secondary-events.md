---
title: Eventos secundarios
description: Eventos secundarios
ms.assetid: cc9eb382-82ca-4416-a04e-1572e4c69c90
keywords:
- Reproductor de Windows Media máscaras,eventos secundarios
- skins,secondary events
- events,secondary
- escribir código para máscaras,eventos secundarios
- eventos secundarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e04785a7468353665083287ac1b74bce5cbf0f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070867"
---
# <a name="secondary-events"></a>Eventos secundarios

Puede determinar qué otros eventos tienen lugar cuando se desencadena un evento específico. Por ejemplo, cuando se hace clic en un botón del mouse, es posible que quiera saber si la tecla ALT estaba presionada al mismo tiempo.

## <a name="event-attributes"></a>Atributos de eventos

Los siguientes atributos de evento son compatibles con las máscaras:

-   **altKey**
-   **Botón**
-   **clientX**
-   **clientY**
-   **ctrlKey**
-   **fromElement**
-   **offsetX**
-   **offsetY**
-   **screenX**
-   **screenY**
-   **shiftKey**
-   **srcElement**
-   **toElement**
-   **x**
-   **y**
-   **Keycode**

Para obtener más información sobre estos atributos, vea la [Referencia de programación de máscaras](skin-programming-reference.md).

## <a name="using-secondary-events"></a>Uso de eventos secundarios

Solo puede procesar atributos de evento en JScript código. Debe usar la sintaxis siguiente:


```C++
event.eventattributename
```



*eventattributename* es el nombre del atributo de evento. Por ejemplo, para determinar si se presionó la tecla ALT durante un evento de clic, podría usar las siguientes líneas en el código JScript clic:


```C++
wasAlt = event.altKey ;
if (wasAlt = true)
{
   // Do something here.
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Control de eventos**](handling-events.md)
</dt> </dl>

 

 




