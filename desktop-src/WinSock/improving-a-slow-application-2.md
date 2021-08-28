---
description: En esta sección se examina una parte de una aplicación de ejemplo que funciona a través de la red muy lentamente. A lo largo de esta sección, se realizan modificaciones en el código inicial para mejorar su rendimiento.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Mejora de una aplicación lenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff8f996267328805dc120d39218784a08383fb68ae9f6927e8983b6e1bec2d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097895"
---
# <a name="improving-a-slow-application"></a>Mejora de una aplicación lenta

En esta sección se examina una parte de una aplicación de ejemplo que funciona a través de la red muy lentamente. A lo largo de esta sección, se realizan modificaciones en el código inicial para mejorar su rendimiento.

El ejemplo ficticio es la parte actualizada de un juego denominado Life. La aplicación está escrita de forma que el cliente realiza los cálculos de las actualizaciones y las envía al servidor. A continuación, el servidor muestra el campo Life resultante. La salida del cliente es una secuencia de bytes, agrupada en tres puntos (tripletes), cada triplete que representa una actualización de celda. Los bytes del triplete representan la fila, la columna y el valor, respectivamente, de la celda.

Este ejemplo comienza como una aplicación de rendimiento intencionadamente deficiente, que proporciona la línea base desde la que se pueden ilustrar las mejoras de rendimiento. A partir de ahí, el código se mejora tres veces para solucionar diversos problemas que afectan al rendimiento. Estos ejemplos deben leerse en orden, ya que cada iteración mejora con respecto a la versión anterior.

El código de línea base y las revisiones que mejoran ese código son los siguientes:

-   [La versión de línea base: una aplicación de muy bajo rendimiento](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Revisión 1: Limpieza de lo obvio](revision-1-cleaning-up-the-obvious-2.md)
-   [Revisión 2: Rediseño para menos conectos](revision-2-redesigning-for-fewer-connects-2.md)
-   [Revisión 3: Envío de bloque comprimido](revision-3-compressed-block-send-2.md)
-   [Mejoras futuras](future-improvements-2.md)

> [!WARNING]
> Los primeros ejemplos de la aplicación proporcionan un rendimiento deliberadamente deficiente, con el fin de ilustrar las mejoras de rendimiento posibles con los cambios en el código. No use estos ejemplos de código en la aplicación; son solo con fines ilustrativos.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



