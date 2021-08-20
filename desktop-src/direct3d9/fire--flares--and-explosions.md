---
description: Puede usar Microsoft Direct3D para simular fenómenos naturales relacionados con las versiones de energía.
ms.assetid: a16af13d-3a38-42b5-900b-ff58a0c917b2
title: Fire, Fires, and Explosions (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4684f94932e7cc9db2560ae23b5be9a07af66727cf05967a5df82bb2e6b5158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095056"
---
# <a name="fire-flares-and-explosions-direct3d-9"></a>Fire, Fires, and Explosions (Direct3D 9)

Puede usar Microsoft Direct3D para simular fenómenos naturales relacionados con las versiones de energía. Por ejemplo, una aplicación puede generar la apariencia del incendio mediante la aplicación de texturas similar a una llama a un conjunto de potencias. Esto es especialmente eficaz si la aplicación usa una secuencia de texturas de incendio para animar las llamas en cada uno de los paneles del incendio. La variación de la velocidad de la reproducción de animación de la pantalla a la velocidad aumenta la apariencia de las llamas reales. La semánida de las llamas 3D entremezchas se puede lograr mediante la capa de las curvas y las texturas de las baterías.

Puede simular simulaciones y flashes aplicando mapas de luz sucesivamente más brillantes a todas las primitivas de una escena. Aunque se trata de una técnica computacionalmente de sobrecarga alta, permite que la aplicación simule una localización o flash localizada. Es decir, la parte de la escena en la que se origina el desenlace o el flash puede parpadear primero.

Otra técnica consiste en colocar una cámara delante de la escena para que se abarcar todo el área de destino de representación. La aplicación aplica texturas sucesivamente más blancas a los paneles y reduce la transparencia a lo largo del tiempo. Toda la escena se atenua a blanco a medida que pasa el tiempo. Se trata de un método de sobrecarga baja para crear un reboso. Sin embargo, con esta técnica, puede ser difícil generar la apariencia de un flash brillante a partir de una fuente de luz de un solo punto.

Las explosións se pueden mostrar en un procedimiento de escena 3D similar a los que se usan para el incendio, los flashes y los artefactos. Por ejemplo, la aplicación podría usar un teléfono móvil para mostrar una onda de impacto y una ola de humo creciente cuando se produce la explosión. Al mismo tiempo, la aplicación puede usar un conjunto de móvil para simular las llamas. Además, puede colocar una sola ruedas delante de la escena para agregar una gran cantidad de luz a toda la escena.

Los rayos de energía se pueden simular mediante contrabandos. La aplicación también puede mostrarlas mediante primitivas que se definen como listas de líneas o franjas de líneas. Para obtener más información, vea [Listas de líneas](line-lists.md) y [franjas de líneas.](line-strips.md)

La aplicación puede crear campos de fuerza mediante rectángulos o primitivos definidos como listas de triángulos. Para crear un campo de fuerza a partir de listas de triángulos, defina un conjunto de triángulos no unidos en una lista de triángulos espaciados por igual sobre la región cubierta por el campo de fuerza. Las brechas entre los triángulos permiten al usuario ver la escena detrás de los triángulos, como podría esperar al mirar un campo de fuerza. Aplique una textura a la lista de triángulos que proporciona a los triángulos la apariencia de un efecto de luz con energía. Para obtener más información, vea [Listas de triángulos.](triangle-lists.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos alfa](alpha-examples.md)
</dt> </dl>

 

 



