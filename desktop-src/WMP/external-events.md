---
title: Eventos externos
description: Eventos externos
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Aspectos de Windows Media Player, eventos externos
- máscaras, eventos externos
- eventos, externos
- escribir código para máscaras, eventos externos
- eventos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa09a01b709f0da51d09fc2bec70cba0a1b07d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695448"
---
# <a name="external-events"></a>Eventos externos

Cuando los usuarios hacen clic en un botón o presionan una tecla, puede responder a su entrada con los controladores de eventos. Un controlador de eventos es una sección de código que se ejecuta cada vez que se desencadena el evento.

Los elementos de máscara admiten los siguientes eventos:

-   **carga**
-   **close**
-   **cambiar el tamaño**
-   **temporizador**
-   **hizo**
-   **dblclick**
-   **error**
-   **mousedown**
-   **mouseup**
-   **mousemove**
-   **mouseover**
-   **mouseout**
-   **keypress**
-   **keydown**
-   **keyup**

Vea la [referencia de programación](skin-programming-reference.md) de la máscara para obtener más detalles sobre eventos específicos.

Un controlador de eventos externo típico asignaría un nombre al evento y definiría el código que se ejecutará. Por ejemplo, si desea crear código para iniciar Windows Media Player cuando el usuario hace clic en un botón, colocaría la siguiente línea en el código del botón.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



Se reproducirá el archivo denominado Laure. WMA. Tenga en cuenta que agrega la palabra "ON" a eventos específicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Controlar eventos**](handling-events.md)
</dt> </dl>

 

 




