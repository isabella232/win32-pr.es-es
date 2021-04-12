---
description: 'La posición, velocidad y orientación de los orígenes de sonido y agentes de escucha en el espacio 3D se representan mediante coordenadas Cartesianas, que son valores en tres ejes: el eje x, el eje y y el eje z.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Coordenadas del espacio 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277599"
---
# <a name="coordinates-of-3d-space"></a>Coordenadas del espacio 3D

La posición, velocidad y orientación de los orígenes de sonido y agentes de escucha en el espacio 3D se representan mediante coordenadas Cartesianas, que son valores en tres ejes: el eje x, el eje y y el eje z.

Los ejes son relativos a un punto de vista establecido por la aplicación. Los valores del eje x se incrementan de izquierda a derecha, en el eje y, de abajo a arriba, y en el eje z, de Near a Far.

La estructura de **\_ Vector X3DAUDIO** contiene valores que describen la posición, la velocidad o la orientación en los tres ejes.

Convencionalmente, los vectores se expresan como tres valores entre paréntesis y separados por comas, en el orden (x, y, z).

En la posición, los valores están en unidades universales definidas por el usuario.

Para la velocidad, el vector describe la velocidad de movimiento a lo largo de cada eje en unidades universales por segundo.

En el caso de la orientación, los valores se encuentran en unidades arbitrarias y se relacionan entre sí. Por ejemplo, si la vista base del mundo 3D está orientada al norte hacia el horizonte y la orientación del agente de escucha es (-1, 0, 1), el agente de escucha está orientado al noroeste. Dado que los valores de un vector no están en unidades absolutas, el vector se podría expresar igualmente como (-5, 0, 5) o (-0,25, 0, 0,25).

los vectores 3D funcionan de forma muy similar a los vectores 2D, pero con un eje adicional en la dirección de arriba abajo. Para ver cómo funcionan los vectores en el espacio 2D, puede dibujarlos en una hoja de papel. Permita que los valores aumenten de la parte inferior a la parte superior del papel y de izquierda a derecha. Una línea dibujada de (0,0) a (1,1) tiene la misma orientación, o dirección, que una dibujada de (0,0) a (5, 5). Sin embargo, la segunda línea indica una distancia o velocidad mayor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de audio comunes](common-audio-concepts.md)
</dt> <dt>

[Información general de X3DAudio](x3daudio-overview.md)
</dt> </dl>

 

 



