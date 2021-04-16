---
description: En esta sección se examina una parte de una aplicación de ejemplo que funciona a través de la red muy lentamente. En esta sección, se realizan modificaciones en el código inicial para mejorar su rendimiento.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Mejora de una aplicación lenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705610"
---
# <a name="improving-a-slow-application"></a>Mejora de una aplicación lenta

En esta sección se examina una parte de una aplicación de ejemplo que funciona a través de la red muy lentamente. En esta sección, se realizan modificaciones en el código inicial para mejorar su rendimiento.

El ejemplo ficticio es la parte actualizada para un juego denominado Life. La aplicación se escribe de forma que el cliente realiza los cálculos de las actualizaciones y las envía al servidor. A continuación, el servidor muestra el campo de vida resultante. La salida del cliente es un flujo de bytes, agrupados en tres (triples), cada triple representa una actualización de celda. Los bytes del triple representan la fila, la columna y el valor respectivamente para la celda.

Este ejemplo comienza como una aplicación intencionadamente deficiente, que proporciona la línea base de la que se pueden ilustrar las mejoras de rendimiento. A partir de ahí, el código se mejora tres veces para solucionar diversos problemas que afectan al rendimiento. Estos ejemplos se deben leer en orden, ya que cada iteración mejora en la versión anterior.

El código de línea base y las revisiones que mejoran ese código son las siguientes:

-   [La versión de línea base: una aplicación con un rendimiento muy deficiente](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Revisión 1: limpieza del manifiesto](revision-1-cleaning-up-the-obvious-2.md)
-   [Revisión 2: rediseño para menos conexiones](revision-2-redesigning-for-fewer-connects-2.md)
-   [Revisión 3: envío de bloque comprimido](revision-3-compressed-block-send-2.md)
-   [Mejoras futuras](future-improvements-2.md)

> [!WARNING]
> Los primeros ejemplos de la aplicación proporcionan un rendimiento insuficiente intencionadamente, con el fin de mostrar las mejoras de rendimiento posibles con los cambios en el código. No use estos ejemplos de código en la aplicación; solo tienen fines ilustrativos.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



