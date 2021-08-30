---
description: 'La posición, la velocidad y la orientación de los orígenes de sonido y los agentes de escucha en el espacio 3D se representan mediante coordenadas cartesianas, que son valores en tres ejes: el eje X, el eje Y y el eje Z.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordenadas del espacio 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80cee9888d5dff446939e7b923626e01700405577bbe5ef1ddbbda2cb1bb085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926685"
---
# <a name="coordinates-of-3d-space"></a>Coordenadas del espacio 3D

La posición, la velocidad y la orientación de los orígenes de sonido y los agentes de escucha en el espacio 3D se representan mediante coordenadas cartesianas, que son valores en tres ejes: el eje X, el eje Y y el eje Z.

Los ejes son relativos a un punto de vista establecido por la aplicación. Los valores del eje X aumentan de izquierda a derecha, en el eje Y de abajo a arriba y en el eje Z de cerca a lejos.

La **estructura vector \_ X3DAUDIO** contiene valores que describen la posición, la velocidad o la orientación en los tres ejes.

Convencionalmente, los vectores se expresan como tres valores entre paréntesis y separados por comas, en el orden (x, y, z).

Para position, los valores están en unidades del mundo definidas por el usuario.

Para la velocidad, el vector describe la velocidad de movimiento a lo largo de cada eje en unidades del mundo por segundo.

Para la orientación, los valores están en unidades arbitrarias y son relativos entre sí. Por ejemplo, si la vista base del mundo 3D se dirige hacia el norte hacia el horizonte y la orientación del agente de escucha es (-1, 0, 1), el agente de escucha se dirige al noroeste. Dado que los valores de un vector no están en unidades absolutas, el vector podría expresarse igualmente como (-5, 0, 5) o (-0,25, 0, 0,25).

Los vectores 3D funcionan de forma muy parecido a los vectores 2D, pero con un eje adicional en la dirección hacia abajo. Puede ver cómo funcionan los vectores en el espacio 2D si los dibuja en una hoja de papel gráfico. Permita que los valores aumenten de la parte inferior a la parte superior del papel y de izquierda a derecha. Una línea dibujada de (0, 0) a (1, 1) tiene la misma orientación o dirección que una dibujada de (0, 0) a (5, 5). Sin embargo, la segunda línea indica una mayor distancia o velocidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos comunes de audio](common-audio-concepts.md)
</dt> <dt>

[Información general sobre X3DAudio](x3daudio-overview.md)
</dt> </dl>

 

 



