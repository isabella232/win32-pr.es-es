---
title: Eventos externos
description: Eventos externos
ms.assetid: d3fd8af6-8d7e-43b8-88fd-a59cf0cef609
keywords:
- Reproductor de Windows Media máscaras, eventos externos
- máscaras, eventos externos
- events,external
- escribir código para máscaras,eventos externos
- eventos externos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac91232447e37bc3970ea8dd0ec727fb9b5daae65e647809b129df3e0347c496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649195"
---
# <a name="external-events"></a>Eventos externos

Cuando los usuarios hacen clic en un botón o presionan una tecla, puede responder a su entrada con controladores de eventos. Un controlador de eventos es una sección de código que se ejecuta cada vez que se desencadena el evento.

Los elementos de máscara admiten los siguientes eventos:

-   **carga**
-   **close**
-   **Redimensionar**
-   **temporizador**
-   **Haga clic**
-   **dblclick**
-   **error**
-   **mousedown**
-   **mouseup**
-   **mousemove**
-   **Mouseover**
-   **mouseout**
-   **keypress**
-   **keydown**
-   **keyup**

Consulte la Referencia [de programación de máscaras](skin-programming-reference.md) para obtener más detalles sobre eventos específicos.

Un controlador de eventos externo típico daría nombre al evento y definiría el código que se ejecutará. Por ejemplo, si desea crear código para iniciar Reproductor de Windows Media cuando el usuario hace clic en un botón, colocaría la siguiente línea en el código del botón.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "

```



Esto reproducirá el archivo denominado laure.wma. Tenga en cuenta que agrega la palabra "on" a eventos específicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Control de eventos**](handling-events.md)
</dt> </dl>

 

 




